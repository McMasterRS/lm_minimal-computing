---
layout: default
title: Building a Minimal Computing Site with Idyll
nav_order: 7
---

## Idyll

Idyll is another static site generator like Jekyll. Idyll also takes markdown text files and converts them into a complete website. Unlike Jekyll, Idyll incorporated the ability to create interactive web documents. It allows you to write documents using a simple markup language that mixes HTML and Markdown, while also incorporating interactive components using ReactJS. Idyll is great for creating data-driven stories, interactive tutorials, and other documents where user engagement and interactivity are key.  

### Setup

To use Idyll you must first install it using `npm`. If you don't have `npm` or Node.js, first install it by following the instructions below.  

If you are using Windows or MacOS, use one of the installers from the [Node.js download page](https://nodejs.org/en/download/). Be sure to install the version labeled **LTS** (Long-Term Support).  

If you are using a Debian Linux/Ubuntu Linux distribution, you can install Node.js using the `apt` package manager.  

1. Start by refreshing your local package index: 
    ```bash
    sudo apt update
    ```
2. Install Node.js: 
    ```bash
    sudo apt install nodejs
    ```
3. Verify that the installation was successful: 
    ```bash
    node -v
    ```
    You should be presented with the version of Node.js that you just installed.
4. Install the `npm` package manager:
    ```bash
    sudo apt install npm
    ```

To install Idyll and create a basic Idyll project, simply run the following commands.
```bash
npm install -g idyll
idyll create
```

You will be asked to provide a name for your project.  

After the project has been created, navigate to the root of the new folder and you will see the following files:  
- `index.idyll`: the main Idyll file, write your markup text in here
- `styles.css`: add any custom styles
- `components/`: any componenet defined in this folders can be used in the Idyll markup
- `data/`: if you want to include a dataset in your project (supports CSV or JSON)
- `static/`: A folder for static file such as images
- `package.json`: this file contains all the configuration for your project

You can build your project in the root of project directory and run `idyll`. This will build the development website and serve it at [http://localhost:3000](http://localhost:3000).  
