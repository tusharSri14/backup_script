Automated Backup & Recovery Script
📌 Overview

This project provides a bash script to automate the backup and recovery of important Linux system files.
It creates compressed backups of specified directories, stores them locally, and optionally transfers them to a remote server.
The script also keeps only the last 7 backups to save disk space.

🛠 Features

Backup multiple directories (/home, /etc by default)

Compressed archive with timestamp (backup_YYYY-MM-DD_HH-MM-SS.tar.gz)

Automatic creation of backup directory

Remote backup using rsync

Cleanup of old backups (keeps only last 7)

Logs success and errors

📂 Backup Locations

Local Backup: /backup

Remote Backup (Optional): backupuser@192.168.1.100:/remote_backup

⚙️ Configuration

Edit the following variables in the script before running:

SOURCE_DIRS="/home /etc"         # Directories to back up
BACKUP_DIR="/backup"             # Local backup destination
REMOTE_USER="backupuser"         # Remote server username
REMOTE_HOST="192.168.1.100"      # Remote server IP/hostname
REMOTE_DIR="/remote_backup"      # Remote backup directory

▶️ Usage

Make script executable

chmod +x backup.sh


Run the script

./backup.sh


Verify backups

Local: ls /backup/

Remote: ssh backupuser@192.168.1.100 ls /remote_backup/

🧹 Cleanup

The script automatically deletes old backups, keeping only the last 7 backups.

🔒 Security Notes

Ensure remote server credentials are configured (SSH keys recommended).

Run with appropriate permissions (sudo may be required for /etc).

Store backups securely to avoid unauthorized access.

👨‍💻 Author

Tushar Srivastava
Project: Backup & Recovery (Linux Support)
