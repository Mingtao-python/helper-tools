# Internet Utility Tool

A comprehensive command-line utility for file management and web browsing operations. This tool combines file handling capabilities with web automation and information lookup features.

## Features

### File Management (Section 1)
- **1.1 Create Text Files**: Create new `.txt` files in any directory
- **1.2 Edit Existing Files**: Append text content to existing `.txt` files
- **1.3 Delete Files**: Safely delete files and folders with confirmation prompts

### Web Browsing (Section 2)
- **2.1 Open Any Website**: Navigate to any custom web URL
- **2.2 Access Search Engines**: Quick access to popular search engines:
  - Google
  - Bing
  - DuckDuckGo
  - Firefox

### Utilities (Section 3)
- **3.1 Google Maps**: Search for locations and view maps
- **3.2 Weather Information**: Get current weather for any city

## Requirements

- Python 3.6+
- Required packages:
  - `selenium`
  - `requests`
  - `send2trash`

## Installation

1. Clone or download this repository
2. Install required dependencies:
```bash
pip install selenium requests send2trash
```

3. Download and install Firefox driver:
   - Download from: https://github.com/mozilla/geckodriver/releases
   - Add geckodriver to your system PATH, or place it in your project directory

## Usage

Run the script:
```bash
python internet.py.py
```

The program will display a menu with available operations:

```
-------------------------------------files-------------------------------------
1.1-create a text file.
1.2-edit a file that exist in your computer.
1.3-delete a file(you can't get it back).
--------------------------------------web--------------------------------------
2.1-open a web.
2.2-change search engine.
--------------------------------web you may use--------------------------------
3.1-google map.
3.2-weather
```

Enter the task number (e.g., `1.1`) to start the operation.

## Detailed Operations

### File Operations

#### 1.1 Create Text File
- Creates a new `.txt` file in a specified directory
- Prompts for folder location and filename
- Only supports `.txt` extension

#### 1.2 Edit Text File
- Append new content to an existing `.txt` file
- Enter text line by line
- Type `1234567890stop` to finish editing

#### 1.3 Delete File or Folder
- Permanently delete files or directories
- **Warning**: Deleted items cannot be recovered
- Requires confirmation with countdown timer

### Web Operations

#### 2.1 Open Custom Website
- Enter any URL to open in Firefox browser
- Use `https://` prefix for best results

#### 2.2 Open Search Engine
- Quick access to major search engines
- Supports: Google, Bing, DuckDuckGo, Firefox

### Utility Operations

#### 3.1 Google Maps Search
- Search for locations, addresses, or places
- Opens Google Maps with search results

#### 3.2 Weather Lookup
- Get current weather for any city
- Uses wttr.in API

## Examples

### Create a file
```
input the task number> 1.1
In which folder do you want to create your new file?
----> C:\Users\YourName\Documents
type the name of your file that you want to create
----> myfile.txt
saved correctly
```

### Edit a file
```
input the task number> 1.2
which file do you want to edit?
file> C:\Users\YourName\Documents\myfile.txt
Start typing---to stop, write:"1234567890stop"
> This is my first line
> This is my second line
> 1234567890stop
edit successfully
```

### Search weather
```
input the task number> 3.2
input the place where you want to know its weather: London
Weather forecast output...
```

## Technical Details

- **Browser Driver**: Uses Firefox with Selenium for web automation
- **File System**: Operates on Windows file systems with permission checking
- **API Integration**: Uses wttr.in API for weather information
- **Error Handling**: Includes protection against invalid inputs and access errors

## Limitations

- Windows-focused (file path handling is Windows-specific)
- Requires Firefox browser to be installed
- Some file operations have permission restrictions
- `.txt` files only for file creation/editing

## Troubleshooting

**"Chrome was closed!" error**
- The Firefox driver window was closed unexpectedly
- The script will automatically restart it

**"Invalid web" error**
- Make sure to include the full URL with `https://`
- Check your internet connection

**"Search time out" error**
- Check your internet connection
- The API server might be temporarily unavailable
- Try again after a moment

**Permission errors on file operations**
- File path must be accessible to your user account
- Avoid system protected directories
- Path must be higher than system user directories

## Notes

- File deletion is permanent - always confirm before deleting important files
- The countdown timer before deletion gives you time to reconsider
- Driver status is automatically checked before browser operations
- All file operations support absolute file paths

## Future Enhancements

- Comment indicates an incomplete feature for accessing AI chat (3.3)
- Could be expanded with additional utilities

---

**Disclaimer**: This tool provides direct file system and web access. Use responsibly and always backup important files before deletion operations.
