<p align="center">
  <img src="ShadowExtension.jpg" alt="ShadowExtension Banner" width="700">
</p>

# ShadowExtension

**ShadowExtension** is a forensic tool for detecting potentially malicious browser extensions across all major browsers. The tool analyzes extension permissions, host permissions, and suspicious code patterns, exporting detailed findings to CSV and JSON for efficient analysis and investigation. It is built to streamline the investigation process and quickly report suspicious browser extensions and their associated risks, saving valuable time during security incident investigations and threat hunting.

## Features
- Detects potentially malicious browser extensions by analyzing permissions, host permissions, and code behavior.
- Supports Chrome, Edge, Firefox, Brave, Vivaldi, and Opera extensions.
- Scans every active user account and browser profile on the system for installed extensions.
- Supports scanning both live systems and offline forensic collections.
- Can be used in scripting and automation workflows.
- Exports results to CSV or JSON reports for documentation and forensic analysis.

## Download

| Platform | Interface | Download |
|----------|-----------|----------|
| Windows  | CLI       | [ShadowExtension.zip](./ShadowExtension.zip) |

## Usage
```
ShadowExtension.exe -s                                         Scan all local browsers (all users)
ShadowExtension.exe -csv <output_path> -s                      Scan all local browsers and export results to CSV
ShadowExtension.exe -json <output_path> -s                     Scan all local browsers and export results to JSON
ShadowExtension.exe -d <user_path> -s                          Scan a specific browser data folder
ShadowExtension.exe -d <user_path> -csv <output_path> -s       Scan a specific browser data folder and export results to CSV
ShadowExtension.exe -d <user_path> -json <output_path> -s      Scan a specific browser data folder and export results to JSON
```

## Examples
```
ShadowExtension.exe -s
ShadowExtension.exe -csv C:\Users\<Username>\Desktop -s
ShadowExtension.exe -json C:\Users\<Username>\Desktop -s
ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -s
ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -csv C:\Users\<Username>\Desktop -s
ShadowExtension.exe -d C:\Users\<Username>\AppData\Local\Google\Chrome\User Data\ -json C:\Users\<Username>\Desktop -s
```
## Optional Arguments

| Argument           | Description                                                                                       |
|--------------------|---------------------------------------------------------------------------------------------------|
| -s                 | Start the scan                                                                                    |
| -d <path>          | Path to browser User Data/Profiles folder                                                         |
| -csv <output_path> | Export results to CSV. If a folder is provided, creates one CSV per browser/user. If a filename is provided, combines all into one CSV. |
| -json <output_path>| Export results to JSON. If a folder is provided, creates one JSON per browser/user. If a filename is provided, combines all into one JSON. |


## Important Notice

Some antivirus software may flag the executable version of this tool as a false positive. This is due to the way the tool interacts with system files and browser history databases. The tool is built using **Python** and **PyInstaller**, which can sometimes trigger heuristic detections.

If you encounter warnings, please consider the following:

- Running the tool in a sandbox environment.
- Adding an exclusion rule for the executable in your antivirus software.
- Temporarily disabling your antivirus software.

## Contact

For questions or feedback, please contact me via https://www.linkedin.com/in/guy-eldad/


Copyright
© 2025 Guy Eldad. All rights reserved.
