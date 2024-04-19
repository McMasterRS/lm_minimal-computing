---
layout: default
title: All-in-One WP Migration Plugin
parent: WordPress Site Preservation
nav_order: 1
---

## All-in-One WP Migration
A tool on WordPress allows users to import an entire WordPress site, including plugins, themes, content and user data. The generated backup of this tool can be stored externally or downloaded for archival purposes.

## Steps to use All-in-One WP Migration to preserve a WordPress website

1. **Install All-in-One WP Migration**
    1. Log in to your WordPress admin dashboard. 
    2. Navigate to "Plugins" -> "Add New Plugin" 
    3. Search for "All-in-One WP Migration" 
    4. Install and activate the "All-in-One WP Migration" plugin. 

2. **Export a WordPress site** 
    1. Select the Export option from the sidebar of the "All-in-One WP Migration" plugin. 
    2. Click on the "Advanced Options" and choose if you want to exclude certain files or database tables. 
    3. From the "EXPORT TO" list, select where to export the site to. E.g. File, FTP, Dropbox, etc. 
    4. If you chose the "File" option, a prompted message to download the file will be displayed. Click on the "Download" button if you want to save a copy of the backup file. 
    5. On the sidebar of the "All-in-One WP Migration" plugin, click on the Backups to view the new backup added to the list. 

3. **Import a WordPress site** 
    1. Select the Import option from the sidebar of the "All-in-One WP Migration" plugin.From the "IMPORT FROM" list, select where to import the site from. E.g. File, FTP, Dropbox, etc. 
    2. If you are importing from a file, click on "Import From" and choose "File." 
    3. Upload the backup file (`.wpress`) that has been exported from the source site. 
    4. Importing may take time depending on the size of the site. 

### How to import if the file size is more than 40M
1. Update these values in php.ini (`Xampp/php/php.ini`) file. E.g. 
    ```conf
    max_execution_time = 5000 
    max_input_time = 5000 
    memory_limit = 1000M 
    post_max_size = 750M 
    upload_max_filesize = 750M 
    ```
2. Restart Apache Module from XAMPP Control Panel. 
