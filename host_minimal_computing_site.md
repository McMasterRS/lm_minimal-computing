---
layout: default
title: Hosting Minimal Computing Site on GitHub Pages
nav_order: 7
---

## Host minimal computing site on GitHub pages 

### A. Creating a repository on GitHub
1. Login to GitHub. 
2. From the menu go to “Your repositories.” 
3. Click on “New” button to create a new repository. 
4. Select the Owner. 
5. Type the repository name. For example, “minima-template” 
6. Check the checkbox to add a README file. 
7. Click on “Create repository” button. 

### B. Uploading Files to the repository

1. On the new repository main page click on “add file” button and select “Upload files” option. 
2. Upload all the files that are in the “minima-site” folder. 
3. Click “Commit changes” button. 

### C. Edit the _config.yml file
1. Open `_config.yml` file. 
2. Click on the pencil edit icon in the corner to start editing the file. 
3. Edit the value of the baseurl to add the sub path of your site. For example,
```yaml
baseurl: "/minima-template". 
```
4. Edit the value of the url to add the base hostname for your site. For example,
```yaml
url: "https://example.github.io" 
```
5. Click on “commit changes” button 
6. Add a proper message to explain your changes. Then Click on “Commit changes” button. 

### D. Deploy the Site 

1. Navigate to “Settings.” 
2. Go to the “Pages” tab. 
3. In “Build and deployment” section, click on the “None” button and select “main” then Click on the “Save” button. 
4. Navigate to the “Actions” tab in the top menu to check the workflow of the building process. 

When the building process is done, go back to the pages tab and you will see at the top of the page a link provided to visit your site. 
