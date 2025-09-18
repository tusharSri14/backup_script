Automated Backup & Recovery Script
Overview

This project provides a bash script to automate the backup and recovery of important Linux system files.
It creates compressed backups of specified directories, stores them locally, and optionally transfers them to a remote server.
The script also keeps only the last 7 backups to save disk space.

Features

Backup multiple directories (/home, /etc by default)

Compressed archive with timestamp (backup_YYYY-MM-DD_HH-MM-SS.tar.gz)

Automatic creation of backup directory

Remote backup using rsync

Cleanup of old backups (keeps only last 7)

Logs success and errors
