# Audio Downloader

A versatile tool for downloading high-quality audio from online media sources in WAV format.

```
╔════════════════════════════════════════════════════════════════════════════╗
║ ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                                ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ║
║ ▓                 ▓                                ▓                   ▓ ║
║ ▓                 ▓                                ▓                   ▓ ║
║ ▓                                                                      ▓ ║
║ ▓                     ▄▄▄▄▄▄         ▄▄▄▄▄▄▄▄                          ▓ ║
║ ▓                  ▄█▀      ▀█▄   ▄█▀        ▀█▄                       ▓ ║
║ ▓                 █▀          ▀█ █▀            ▀█▄                     ▓ ║
║ ▓                █▀            ▀█▀               ▀█                    ▓ ║
║ ▓               █▀              ▀█                ▀█                   ▓ ║
║ ▓              █▀                ▀█                ▀█                  ▓ ║
║ ▓            ▄█▀                  ▀█                ▀█                 ▓ ║
║ ▓           █▀                     ▀█                ▀█▄               ▓ ║
║ ▓         ▄█▀                       ▀█                 ▀█              ▓ ║
║ ▓        █▀                          ▀█                 ▀█             ▓ ║
║ ▓       █▀                            ▀█                 ▀█            ▓ ║
║ ▓      █▀                             ▀█                  ▀█           ▓ ║
║ ▓      █                               █                   █           ▓ ║
║ ▓      █▄                             ▄█                  ▄█           ▓ ║
║ ▓       ▀█                           █▀                  █▀            ▓ ║
║ ▓        ▀█▄                       ▄█▀                 ▄█▀             ▓ ║
║ ▓          ▀█▄                   ▄█▀                 ▄█▀               ▓ ║
║ ▓            ▀█▄               ▄█▀                 ▄█▀                 ▓ ║
║ ▓              ▀█▄            █▀                 ▄█▀                   ▓ ║
║ ▓                ▀█▄        ▄█▀                ▄█▀                     ▓ ║
║ ▓                  ▀█▄▄▄▄▄▄█▀               ▄█▀                        ▓ ║
║ ▓                                                                      ▓ ║
║ ▓                 ▓                                ▓                   ▓ ║
║ ▓                 ▓                                ▓                   ▓ ║
║ ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                                ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ║
╚═══════════════ A U D I O  D O W N L O A D E R  F O R  W A V ═══════════════╝
```

## Overview

This script allows you to easily extract high-quality audio from various online sources including YouTube videos, Twitter/X Spaces, podcasts, and more. It creates clean, organized filenames based on the source URL.

## Features

- **High-Quality WAV Extraction**: Downloads the best available audio quality and converts to WAV format
- **Multiple URL Support**: Process several downloads with a single command
- **Clean Filenames**: Generates filenames based on the source domain and video ID (`youtube.com_watch?v=dQw4w9WgXcQ.wav`)
- **Google Colab Integration**: Optimized for use within Google Colab notebooks
- **Local Mode**: Also works in regular Python environments

## Requirements

- Python 3.6+
- yt-dlp
- tqdm
- ffmpeg (for audio conversion)

For Google Colab users, these dependencies are automatically managed.

## Installation

```bash
# Install required packages
pip install yt-dlp tqdm
```

Make sure `ffmpeg` is installed on your system:

```bash
# On Ubuntu/Debian
apt-get install ffmpeg

# On macOS with Homebrew
brew install ffmpeg
```

## Usage

### Basic Usage

```bash
python audio_downloader.py --urls "https://youtube.com/watch?v=..." "https://x.com/username/status/..."
```

### Keep Original Files

Use the `-k` flag to keep the original media files alongside the extracted audio and save them in the current directory:

```bash
python audio_downloader.py -k --urls "https://youtube.com/watch?v=..." "https://x.com/username/status/..."
```

### Google Colab Usage

In Google Colab, the script will automatically detect the environment and provide download links for the resulting files.

```python
!python audio_downloader.py -k --urls "https://youtube.com/watch?v=..." "https://x.com/username/status/..."
```

## Examples

Download audio from a YouTube video:
```bash
python audio_downloader.py --urls "https://youtube.com/watch?v=dQw4w9WgXcQ"
```

Download audio from multiple sources:
```bash
python audio_downloader.py --urls "https://youtube.com/watch?v=dQw4w9WgXcQ" "https://x.com/username/status/1234567890"
```

## Note

This tool is designed for educational and personal use only. Please respect copyright and terms of service for all content sources.

## License

MIT License 
