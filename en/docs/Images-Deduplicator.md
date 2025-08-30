---
lang: en
lang-niv: fonto
lang-ref: 014-jbk
layout: doc
order: 5
title: 'Images Deduplicator'
---

# Images Deduplicator

Images Deduplicator is a powerful Python application designed for efficient management and removal of duplicate images. Leveraging the Wand library (ImageMagick) for image processing, this tool provides advanced visual comparison techniques to identify and manage duplicate images with high accuracy.

## Key Features

- **Advanced Image Processing**: Powered by Wand/ImageMagick for superior image format support
- **Visual Duplicate Detection**: Perceptual hashing to identify visually similar images
- **Comprehensive Format Support**: Handles all major image formats including JPEG, PNG, WEBP, PSD, and more
- **Intuitive Interface**: User-friendly graphical interface with dark/light theme support
- **Multi-language Support**: Built-in internationalization with English and Italian languages
- **Batch Processing**: Efficiently process thousands of images
- **Preview & Comparison**: Side-by-side image comparison before taking action
- **Safe Operations**: Move to trash instead of permanent deletion
- **Detailed Logging**: Comprehensive operation logging for traceability

## System Requirements

- **Python**: 3.8 or higher (3.10+ recommended)
- **ImageMagick**: Required for Wand image processing
  - Windows: Install from [ImageMagick Windows](https://imagemagick.org/script/download.php#windows)
  - macOS: `brew install imagemagick`
  - Linux: `sudo apt-get install libmagickwand-dev`
- **Memory**: 4GB minimum, 8GB+ recommended for large image collections
- **Storage**: Sufficient space for images being processed + temporary files
- **Operating Systems**:
  - Windows 10/11
  - macOS 10.15+
  - Linux with X11/Wayland

## Why Wand/ImageMagick?

Images Deduplicator uses Wand (a Python binding for ImageMagick) for several advantages:

- Broader format support including PSD, GIF, and BMP
- Better memory management for large images
- More consistent behavior across different platforms
- Advanced image manipulation capabilities
- Active maintenance and security updates

## Usage

### Main Interface

The application features a modern, user-friendly interface with the following key components:

1. **Menu Bar**: Access to all application functions and settings
2. **Toolbar**: Quick access to frequently used functions
3. **Folder Browser**: Navigate and select directories to scan
4. **Preview Pane**: View and compare images side by side
5. **Results Panel**: Displays found duplicates with similarity scores
6. **Status Bar**: Shows operation progress and system information

### Basic Workflow

1. **Select Source Folder**
   - Click the "Open Folder" button or use `File > Open Folder`
   - The application will scan for supported image formats
   - Supported formats: JPEG, PNG, WEBP, PSD, BMP, GIF, and more (via Wand/ImageMagick)

2. **Configure Scan Settings**
   - Adjust similarity threshold (default: 90%)
   - Set minimum image size to consider
   - Choose which image properties to compare (size, date, content hash)

3. **Start the Scan**
   - Click "Start Scan" to begin duplicate detection
   - Progress is shown in the status bar
   - Pause or stop the scan at any time

4. **Review Results**
   - Duplicate groups are displayed with previews
   - Sort by file size, date, or similarity score
   - Use the side-by-side comparison tool for verification

5. **Manage Duplicates**
   - Select images to keep or delete
   - Move duplicates to trash (recoverable) or delete permanently
   - Export results to CSV/JSON for reference

### Advanced Features

#### Batch Processing

- Process multiple folders in sequence
- Save and load scan configurations
- Schedule automatic scans

#### Smart Selection

- Auto-select images by criteria (oldest, smallest, etc.)
- Keep highest resolution version
- Preserve images with specific naming patterns

#### Image Comparison Tools

- Side-by-side and overlay comparison modes
- Zoom and pan synchronized between images
- Histogram and EXIF data comparison

#### Custom Filters

- Filter by image dimensions
- Filter by creation/modification date
- Filter by image format or color profile

#### Wand/ImageMagick Integration

- Advanced image format support
- Better handling of color profiles and metadata
- Support for RAW camera formats when enabled in ImageMagick

### Keyboard Shortcuts

| Shortcut      | Action                           |
|---------------|----------------------------------|
| `Ctrl+O`     | Open folder                      |
| `Ctrl+F`     | Start new scan                   |
| `Space`      | Toggle selection of current image |
| `Del`        | Move selected to trash           |
| `Ctrl+Z`     | Undo last action                 |
| `F5`         | Refresh view                     |
## Performance Optimization

### For Large Collections

- Use the "Quick Compare" mode for initial filtering
- Increase the minimum file size to skip thumbnails
- Schedule scans during off-hours for large collections

### Memory Management

- Close other memory-intensive applications
- Adjust ImageMagick's resource limits if needed (see Installation)
- Process images in smaller batches

### Storage Considerations

- Ensure sufficient free space for temporary files
- Process images directly from the source drive when possible
- Consider using a fast SSD for better performance

## Troubleshooting

### Slow Performance

- Check ImageMagick's policy settings (see Installation)
- Reduce the number of concurrent operations
- Disable real-time preview for large collections

### Missing Images

- Verify ImageMagick supports the image format
- Check file permissions
- Look for error messages in the log viewer

### Unexpected Results

- Adjust the similarity threshold
- Check if filters are too restrictive
- Verify image metadata is being read correctly

## Configuration

### Main Options

#### Comparison Precision

- **Precision level (1-100)**:
  - Lower values find more duplicates
  - Higher values find only nearly identical duplicates

#### Minimum Sizes

- **Ignore images below**:
  - Minimum width (pixels)
  - Minimum height (pixels)
  - Minimum size (KB)

#### Supported Formats

- **Allowed extensions**:
  - .jpg, .jpeg
  - .png
  - .gif
  - .bmp
  - .webp

#### Excluded Folders

- **List of folders to ignore**:
  - System folders
  - Temporary folders
  - Specific folders

### Configuration Tips

1. **Precision**
   - Level 70-80 for good balance
   - Level 90+ for very strict comparisons

2. **Memory**
   - Monitor RAM usage
   - Reduce cache if needed

3. **Backup**
   - Always save configurations
   - Export reports before deleting images
