# wordpress-backup

## General
Backup script for Wordpress websites. Script generates a SQL dump from database, creates a TAR package and copy it with scp to another server. scp part is optional.

This script works only if your folder structure is same than mine. My websites are stored like this:
```/home/stargazers/sites/websitenamehere.com/www/```

This also requires SSH-keys already configured between two servers.

## Usage

Just change websitenamehere.com to correct one and run:
```./backup-wordpress websitenamehere.com```

If you want to run script without copying anything to another server run like this:
```USE_SCP=false ./backup-wordpress websitenamehere.com```

## Required settings

You need to change the settings in script to make it work
* SITES_BASEPATH - Path where websites are stored
* TEMP_PATH - Where we create temporary tar file before scp
* BACKUP_SSH_USER - Username we 
* BACKUP_SERVER - Server where we copy files with scp. Add those in ```~/.ssh/config```
* BACKUP_SERVER_PATH - On remote server where we save the file
