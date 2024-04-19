---
layout: default
title: Heritrix tool
parent: Website Preservation
nav_order: 1
---
## Heritrix Tool​

Heritrix is the Internet Archive's open-source, extensible web crawler designed for web archiving purposes.​

It is providing a web-based user interface for configuring, starting, pausing, and stopping the crawl. The interface also displays the current state of the crawl and generates logs and reports. The logs display the URI of the document downloaded, the time taken to download it, the document size and indicate any errors encountered.

## Steps to use Heritrix

1. **Installing Heritrix on Windows**
    1. Download the latest stable release of Heritrix (zip file). 
    2. Extract the contents of the downloaded zip file to a location on the computer (e.g., C:\Heritrix). 

2. **Configure Java**
    1. Ensure you have Java installed on your system. 
    2. Set up Environment Variables: 
        1. Under "System variables," find the "Path" variable and click "Edit." 
        2. Click "New" and add the path to the bin directory of your Java installation (e.g., C:\Program Files\Java\jdk1.8.0_281\bin). 

3. **Start Heritrix** 
    1. Open a Command Prompt in administrator mode. 
    2. Navigate to the Heritrix installation directory (e.g., cd C:\Heritrix). 
    3. Run the following command to start Heritrix:
    ```powershell
    bin\heritrix.cmd -a admin:admin
    ```
    4. Replace "admin" with your desired username and with your chosen password.

4. **Access the Heritrix Web UI** 
    1. Open your web browser and go to [https://localhost:8443](https://localhost:8443). 
    2. Log in with the username and password specified during Heritrix startup. 

5. **Use Heritrix**

    Follow the steps in [Heritrix Doc](https://heritrix.readthedocs.io/en/latest/getting-started.html) in Your First Crawl section to Configure and start crawls through the Heritrix web interface. 

6. **View the content of WARC file:**

    To view the content of a WARC (Web ARChive) file, you can use Webrecorder-player tool that support this file format: 

    [Webrecorder-player](https://github.com/webrecorder/webrecorder-player) is a browser-based tool that allows you to view and interact with WARC files. You can simply upload your WARC file to the Webrecorder-player, and it will provide a user interface to navigate through the archived content. 
