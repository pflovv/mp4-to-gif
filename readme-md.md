# MP4 to GIF Converter

A bash script utility that converts MP4 video files to high-quality GIF animations.

## Features

- Batch processing of multiple MP4 files
- High-quality output using FFmpeg's palette generation technique
- Preserves original dimensions while maintaining reasonable file sizes
- Simple configuration with customizable input/output directories

## Requirements

- FFmpeg (must be installed and available in your PATH)
- Bash shell environment (Linux, macOS, or WSL on Windows)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/pflovv/mp4-to-gif.git
   cd mp4-to-gif
   ```

2. Make the script executable:
   ```bash
   chmod +x mp4_to_gif.sh
   ```

## Usage

### Basic Usage

1. Edit the script to set your input and output directories:
   ```bash
   INPUT_DIR="/path/to/your/mp4/files/"
   OUTPUT_DIR="/path/to/save/gifs/"
   ```

2. Run the script:
   ```bash
   ./mp4_to_gif.sh
   ```

### Advanced Usage

You can also specify input and output directories directly as command-line arguments:

```bash
./mp4_to_gif.sh -i /path/to/input -o /path/to/output
```

## How It Works

The script utilizes FFmpeg to:

1. Generate an optimized color palette for each video
2. Use that palette to create a high-quality GIF with optimal colors
3. Apply appropriate dithering techniques to maintain visual quality
4. Clean up temporary files after conversion

## Customization

You can edit the FFmpeg parameters in the script to customize:
- Frame rate (`fps=24`)
- Scaling options
- Dithering method (`dither=bayer`)

## License

MIT License - See [LICENSE](LICENSE) file for details.

## Contributing

Pull requests are welcome! Feel free to improve the script or documentation.
