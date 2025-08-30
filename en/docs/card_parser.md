---
lang: en
lang-niv: fonto
lang-ref: 011-jbk
layout: doc
order: 2
title: 'Credit Card Stripe Parser'
---

# Credit Card Stripe Parser

**Credit Card Stripe Parser** is a Python library and command-line tool for parsing and analyzing magnetic stripe data from credit cards. It supports both Track 1 and Track 2 formats as specified in ISO/IEC 7811-2 and ISO/IEC 7813 standards.

> **Note**
> This tool is intended for educational and testing purposes only. Always handle payment card data in compliance with PCI DSS requirements and applicable laws and regulations.

## Usage Guide

This guide provides examples of how to use the Credit Card Stripe Parser library.

### Basic Usage

#### Parsing Full Track Data

```python
from credit_card_stripe_parser import FullTrackParser

# Create a parser instance
parser = FullTrackParser()

# Example track data
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# Parse the track data
result = parser.parse(track_data)

# Access parsed data
if result.is_track_one_valid and result.track_one:
    print(f"Cardholder: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"Expiry: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"Service Code: {result.track_two.service_code}")
```

### Parsing Individual Tracks

#### Track 1 Parsing

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"Track 1 Data: {track1}")
except Exception as e:
    print(f"Error parsing Track 1: {e}")
```

#### Track 2 Parsing

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"Track 2 Data: {track2}")
except Exception as e:
    print(f"Error parsing Track 2: {e}")
```

### Error Handling

The library provides specific exceptions for different error scenarios:

```python
from credit_card_stripe_parser import (
    FullTrackParser,
    InvalidTrackOneException,
    InvalidTrackTwoException,
    InvalidTrackDataException
)

parser = FullTrackParser()

try:
    result = parser.parse(invalid_track_data)
except InvalidTrackOneException as e:
    print(f"Invalid Track 1 data: {e}")
except InvalidTrackTwoException as e:
    print(f"Invalid Track 2 data: {e}")
except InvalidTrackDataException as e:
    print(f"Invalid track data: {e}")
except Exception as e:
    print(f"Unexpected error: {e}")
```

### Using the Data Models

The library provides data models for working with parsed track data:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# Create a TrackOneModel instance
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='JOHN DOE',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^JOHN DOE^251212312345678901234567890?'
)

# Create a TrackTwoModel instance
track2 = TrackTwoModel(
    pan='5168755544412233',
    expiration_date='2512',
    service_code='123',
    pvki=None,
    pvv_or_cvv='1234',
    discretionary_data='123456789012345678901234567890',
    source_string=';5168755544412233=2512123123412345678901234567890?'
)
```

## Advanced Usage

### Custom Validation

You can implement custom validation by subclassing the parser:

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # Custom validation logic for Track 1
        if not super().validate_track_one(track_data):
            return False
        # Add custom validation here
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # Custom validation logic for Track 2
        if not super().validate_track_two(track_data):
            return False
        # Add custom validation here
        return True
```

### LRC Validation

To enable LRC (Longitudinal Redundancy Check) validation:

```python
parser = FullTrackParser(validate_lrc=True)

# This will raise an exception if LRC validation fails
try:
    result = parser.parse(track_data_with_lrc)
except Exception as e:
    print(f"LRC validation failed: {e}")
```
> **Note**
> LRC validation requires the track data to include the LRC character at the end.

## Frequently Asked Questions (FAQ)

### General Questions

#### What is the purpose of this library?
This library is designed to parse and analyze magnetic stripe data from credit cards for educational and testing purposes.

#### Is it safe to use in production?
This tool should be used in compliance with PCI DSS requirements and applicable laws. Always ensure proper security measures are in place when handling payment card data.

### Technical Questions

#### What track formats are supported?
The library supports both Track 1 and Track 2 formats as specified in ISO/IEC 7811-2 and ISO/IEC 7813 standards.

#### How do I handle errors during parsing?
The library provides specific exceptions for different error scenarios. See the Error Handling section for examples.

### Security Considerations

#### How should I handle sensitive card data?
Always follow PCI DSS requirements when handling payment card data. The library includes helper functions for masking sensitive information.

#### Example of masking PAN:

```python
def mask_pan(pan):
    if len(pan) <= 4:
        return pan
    return '*' * (len(pan) - 4) + pan[-4:]
```

## License

This project is licensed under the GPLv3 License - see the [LICENSE](LICENSE) file for details.
