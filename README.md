# Media File Analyzer 🔍🎥

A Bash script using ffprobe to display detailed technical metadata for media files, supporting both single-file and directory analysis. 📊✨

## Features 🌟
- 📂 Bulk analysis of all files in current directory
- 🎯 Single-file analysis with argument
- 📏 Format metrics: File size & duration
- 📺 Video stream details: 
  ```Resolution | Codec | Bitrate | Framerate | Aspect Ratio | Pixel Format```
- 🔉 Audio stream details: 
  ```Codec | Bitrate | Sample Rate | Channels | Profile```
- 🖥️ Clean terminal formatting with section separators

## Prerequisites ⚙️
```bash
sudo apt install ffmpeg  # Contains ffprobe (Debian/Ubuntu)
```
## Installation 📥
```bash
git clone https://github.com/LLSouf/mpegi
cd mpegi
chmod +x mpegi
```
## Usage 🚀
```bash
# Analyze single file:
./mpegi video.mp4

# Scan current directory:
./mpegi
```
## Output Explanation 📖
```bash
============================    # File separator
filename.ext                    # Analyzed filename
----------------------------    # Section break
format:size=1234567            # Bytes
format:duration=123.456789      # Seconds
----------------------------
[Video Stream Details]          # Width|Height|Codec|Framerate etc
[Audio Stream Details]          # Codec|Bitrate|Sample Rate etc
============================
```
## Example Output 📋
```bash
============================
sample.mp4
============================
format:size=2546879
format:duration=30.033333
----------------------------
VIDEO
----------------------------
width=1920
height=1080
codec_long_name=H.264 / AVC / MPEG-4 AVC / MPEG-4 part 10
r_frame_rate=30/1
bit_rate=1 500 000
[...]
----------------------------
AUDIO
----------------------------
codec_long_name=AAC (Advanced Audio Coding)
sample_rate=48000
channel_layout=stereo
bit_rate=128 000
[...]
```
## Troubleshooting 🚨
Missing ffprobe: Install ffmpeg package

Unreadable files: Ensure valid media formats

Permission issues: Run chmod +x analyze-media.sh
