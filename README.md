# ShadowExtension
**ShadowExtension - A forensic tool to detect potentially malicious browser extensions in Chrome, Edge, Firefox, Brave, Vivaldi, and Opera. The tool analyzes extension permissions, host access, and suspicious code behavior, exporting detailed findings to CSV and JSON formats for efficient analysis and investigation.

## Features

- Detects potentially malicious browser extensions by analyzing permissions, host access, and code behavior.
- Supports Google Chrome, Microsoft Edge, Mozilla Firefox, Brave, Vivaldi, and Opera extensions.
- Scans every active user account on the system for installed extensions.
- Supports scanning both live systems and offline forensic collections.
- Exports results to CSV or JSON reports for documentation and forensic analysis.


## Usage

**Syntax:**

**Usage:**

    ShadowExtension.exe -s
    ShadowExtension.exe -csv <output_path> -s
    ShadowExtension.exe -json <output_path> -s
    ShadowExtension.exe -d <user_path> -s
    ShadowExtension.exe -d <user_path> -csv <output_path> -s
    ShadowExtension.exe -d <user_path> -json <output_path> -s


**Examples:**

    ShadowExtension.exe -s
    ShadowExtension.exe -csv C:\Users\<Username>\Desktop -s
    ShadowExtension.exe -json C:\Users\<Username>\Desktop -s
    ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -s
    ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -csv C:\Users\<Username>\Desktop -s
    ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -json C:\Users\<Username>\Desktop -s

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

## Optional Arguments

| Argument           | Description                                                                                       |
|--------------------|---------------------------------------------------------------------------------------------------|
| -s                 | Start the scan                                                                                    |
| -d <path>          | Path to browser User Data/Profiles folder                                                         |
| -csv <output_path> | Export results to CSV. If a folder is provided, creates one CSV per browser/user. If a filename is provided, combines all into one CSV. |
| -json <output_path>| Export results to JSON. If a folder is provided, creates one JSON per browser/user. If a filename is provided, combines all into one JSON. |

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

## Important Notice

Some antivirus software may flag the executable version of this tool as a false positive. This is due to the way the tool interacts with system files and browser extension data. The tool is built using Python and PyInstaller, which can sometimes trigger heuristic detections.

If you encounter warnings, please consider the following:

- Running the tool in a sandbox environment.
- Adding an exclusion rule for the executable in your antivirus software.
- Temporarily disabling your antivirus software.

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

## Contact

For questions or feedback, please contact me via https://www.linkedin.com/in/guy-eldad/

─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

© 2025 Guy Eldad. All rights reserved.

Created by: github.com/GuyEldad
