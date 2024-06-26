# DaVinci Resolve Video Downloader


## About
A python script for DaVinci Resolve (Studio) for macOS (support for other platforms may come in the future). Intended to be started from within Resolve.
The script starts a GUI where you can paste a link to a YouTube, TikTok, Instagram, or other web video. Click the Download-button to download to a specified location using yt-dlp.

Once Download is complete, the script will re-encode non-mp4 files to .mp4 using ffmpeg, to ensure compatibility.

Then the script automatically imports the video into DaVinci Resolve Media Pool.



## Installation

### 1 – Copy the Video_Downloader.py-file into the folder into DaVinci Resolves script-folder
Do this so that Resolve can find it. You may need to restart Resolve for it to show up.

#### Blackmagic Design-installer version:
`~/Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion/Scripts/Utility/`

#### Mac App Store version:
NOTE – this version seems to have problems because of macOS Sandboxing. The script may not work.
`~/Library/Containers/com.blackmagic-design.DaVinciResolveAppStore/Data/Library/Application\ Support/Fusion/Scripts/Utility/`
Note that this directory may not be directly accessible from Finder in normal ways. Another way to access it, is to right click DaVinci Resolve Studio.app in the Applications directory, click Show Package Contents, then Contents -> Resources -> Fusion -> Scripts -> Utility

### 2 – Install Homebrew:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

### 3 – Install ffmpeg and yt-dlp with homebrew:
`brew install ffmpeg && brew install yt-dlp`

### 4 – Install python
Important! Do not install this via Homebrew. It creates problems for DaVinci Resolve linking to pip-packages.
Install via python.org:
`https://www.python.org/downloads/`



## Usage
- Run this script from DaVinci Resolve's dropdown menu: Workspace -> Scripts


## Goals
- [ ] Make it remember your chosen download-folder.
	- Work not started.
- [ ] Update UI to display download and conversion process
	- Work not started.
- [ ] Make script work on Windows and Linux
	- [ ] Windows
		- [ ] Create install instructions for ffmpeg and yt-dlp based on os
		- [ ] Make script link to correcd binary path based on os
	- [ ] Linux
		- [ ] Create install instructions for ffmpeg and yt-dlp based on os
		- [ ] Make script link to correct binary path based on os



#### Inspired by
This project is inspired by a similar project by neezr: https://github.com/neezr/YouTube-Downloader-for-DaVinci-Resolve.
I started by just doing small improvements in a fork, but now the code changes are so significant that it feels more like a separate project. I still wanted to give some credit to the original project.
