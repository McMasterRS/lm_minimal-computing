---
layout: default
title: Building a Minimal Computing Site
has_children: true
has_toc: true
nav_order: 8
---

# Building a minimal computing site
Building a minimal computing site involves creating a website with a focus on simplicity, efficiency, and accessibility. It minimize the resources required to host and access the site, which make it more sustainable and accessible in environments that are having limited internet connectivity or technological infrastructure.​

**Jekyll** is a free open-source SSG that is built and runs on the Ruby programming language. It is a popular choice for building a minimal computing site due to its simplicity, flexibility, and efficiency.

### Prerequisites
Jekyll requires the following:
- Ruby version 2.5.0 or higher
- RubyGems
- GCC and Make

### Instructions
1. Install all [prerequisites](https://jekyllrb.com/docs/installation/).
2. Open Command Prompt CMD.
3. Install the jekyll and bundler gems.
  ```ts
  gem install jekyll bundler
  ```
4. Go to the directory where you want to save the site. For example, “C:\Users\user\Documents” 
5. Run the commands
  - Create a new Jekyll site -> Jekyll new "Name_of_site", For example, 
    ```ts
    Jekyll new minima-site
    ```
  - Change directory
    ```ts 
    cd minima-site 
    ```
  - Build the site and make it available on a local server.
    ```ts
    bundle exec jekyll serve
    ```
6. Browse to [http://localhost:4000](http://localhost:4000).

Notice that the created site will be using the default theme which is the ***Minima*** theme. You can choose your prefered theme and update the theme of your site.

### Understanding gem-based themes
<i>"When you **create a new Jekyll site** (by running the **jekyll new <PATH>** command), Jekyll installs a site that uses a gem-based theme called **Minima**.<i>

*With gem-based themes, some of the site’s directories (such as the **assets**, **_data**, **_layouts**, **_includes**, and **_sass** directories) are stored in the theme’s gem, hidden from your immediate view. Yet all of the necessary directories will be read and processed during Jekyll’s build process.*

*In the case of Minima, you see only the following files in your Jekyll site directory:*
```ts
.
├── Gemfile
├── Gemfile.lock
├── _config.yml
├── _posts
│   └── 2016-12-04-welcome-to-jekyll.markdown
├── about.markdown
└── index.markdown
```

*The **Gemfile** and **Gemfile.lock** files are used by Bundler to keep track of the required gems and gem versions you need to build your Jekyll site.*

*Gem-based themes make it easier for theme developers to make updates available to anyone who has the theme gem. When there’s an update, theme developers push the update to RubyGems.*

<i>If you have the theme gem, you can (if you desire) run **bundle update** to update all gems in your project. Or you can run **bundle update <<THEME>>**, replacing **<<THEME>>** with the theme name, such as **minima**, to just update the theme gem. Any new files or updates the theme developer has made (such as to stylesheets or includes) will be pulled into your project automatically.<i>

*The goal of gem-based themes is to allow you to get all the benefits of a robust, continually updated theme without having all the theme’s files getting in your way and over-complicating what might be your primary focus: creating content."* [Jekyll Doc](https://jekyllrb.com/docs/themes/#understanding-gem-based-themes)