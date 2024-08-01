---
layout: default
title: Building a Minimal Computing Site
nav_order: 5
---

## Building a minimal computing site
Websites are a common type of software developed for research. With modern web browsers, HTML5 and minimal computing design, much of the complexity of websites can be removed, supporting the FAIR principles of reproducible software. It also results in a clean, modern design.  

These next sections detail how to build a minimal computing website using available open source technologies.

We will be demonstrating this development using Jekyll, a free open source static site generator that is built and runs on the Ruby programming language. It is a popular choice for building a minimal computing site due to its simplicity, flexibility, and efficiency.

### Prerequisites
Jekyll requires the following:
- Ruby version 2.5.0 or higher
- RubyGems

### Instructions
1. Install all [prerequisites](https://jekyllrb.com/docs/installation/). 
2. Open a command-line terminal. 
3. Install Jekyll and the bundler gems.

    ```bash
    gem install jekyll bundler
    ```
4. Go to the directory where you want to save the site. For example, "C:\Users\user\Documents".
5. Run the commands.

    ```bash
    jekyll new minima-site
    cd minima-site

    # build the site and make it available on a local server
    bundle exec jekyll serve
    ```
6. Browse to [http://localhost:4000](http://localhost:4000). 

## Steps to customize a minima Jekyll theme

To customize your theme, you need to understand the structure of your theme, so you can edit it.

### Understanding theme structure

These excerpts from the [Jekyll Doc](https://jekyllrb.com/docs/themes/#understanding-gem-based-themes) provide a clear description of the structure of themes: 

When you create a new Jekyll site (by running the `jekyll new <PATH>` command), Jekyll installs a site that uses a gem-based theme called Minima.

With gem-based themes, some of the site’s directories (such as the `assets`, `_data`, `_layouts`, `_includes`, and `_sass` directories) are stored in the theme’s gem, hidden from your immediate view. Yet all of the necessary directories will be read and processed during Jekyll’s build process.

In the case of Minima, you see only the following files in your Jekyll site directory:

```bash
├── Gemfile 
├── Gemfile.lock 
├── _config.yml 
├── _posts 
│   └── 2016-12-04-welcome-to-jekyll.markdown 
├── about.markdown 
└── index.markdown
```

The `Gemfile` and `Gemfile.lock` files are used by Bundler to keep track of the required gems and gem versions you need to build your Jekyll site.

Gem-based themes make it easier for theme developers to make updates available to anyone who has the theme gem. When there’s an update, theme developers push the update to RubyGems.

If you have the theme gem, you can (if you desire) run `bundle update` to update all gems in your project. Or you can run `bundle update <THEME>`, replacing `<THEME>` with the theme name, such as minima, to just update the theme gem. Any new files or updates the theme developer has made (such as to stylesheets or includes) will be pulled into your project automatically.

The goal of gem-based themes is to allow you to get all the benefits of a robust, continually updated theme without having all the theme’s files getting in your way and over-complicating what might be your primary focus: creating content. 
