OneDrive Backup Script

Overview
This PowerShell script automates the backup of OneDrive files to a local network drive. It verifies file updates and ensures synchronization by copying new or modified files while removing obsolete ones. Additionally, it logs operations and sends an email notification with the log summary.

Features
- Automatic Backup: Compares OneDrive and backup drive contents and updates accordingly.
- Logging: Captures and stores log messages in a text file.
- Email Notifications: Sends an email with log details upon script completion.
- File Synchronization: Copies new or updated files and removes obsolete files from the backup location.

Prerequisites
- Windows with PowerShell enabled
- Microsoft Outlook installed (for email functionality)
- OneDrive set up on the local machine
- Network drive available for backup storage

Installation & Setup
1. Clone or download this script to your preferred location.
2. Update the variables in the script as needed:
   - `$oneDrive` (OneDrive folder path)
   - `$netDrive` (Network backup folder path)
   - `$emailLog` (Log file location)
   - Email recipient in `Send-Email` function
3. Ensure you have the required permissions to access OneDrive and the network drive.

Usage
1. Open PowerShell.
2. Navigate to the script directory.
3. Run the script using:
   ```powershell
   .\Backup-Script.ps1
   ```
4. The script will:
   - Log all operations to the specified log file.
   - Synchronize files between OneDrive and the network backup location.
   - Send an email with the log file contents.

Error Handling
- The script includes a `try-catch` block to capture errors.
- Errors are logged and included in the email notification.

Future Improvements
- Add more robust error handling.
- Support multiple backup locations.
- Enhance email notification format (e.g., add attachments or HTML formatting).

License
This project is open-source and available for modification and distribution.
