---
layout: default
title: Override Minima Stylesheet
parent: Customizing a Minima Jekyll theme
nav_order: 1
---

## Override minima stylesheet

Let’s say we want to add some custom stylesheet changes.

*"To modify any stylesheet, you must take the extra step of also copying the main sass file (`_sass/minima.scss` in the Minima theme) into the _sass directory in your site’s source."* [Jekyll Doc](https://jekyllrb.com/docs/themes/)

In your Jekyll folder: 

1. Create a `_sass` folder and add a file in it called `custom.scss`. 
2. In the `custom.scss` file add all your custom stylesheet changes and save it.

    Example of `custom.scss` stylesheet changes to customize the site header and footer: 
    ```css
    /* Put any custom CSS here */
        * {
        box-sizing: border-box;
        margin: 0;
        border: 0;
        padding: 0;
        text-decoration: none;
        list-style-type: none;
        }
        /*Site header*/
        .site-header {
            background: #fff;
            padding-top: 24px;
            padding-bottom: 16px;
            border-top: none;
            margin: 0 auto;
        }

        /*Site title*/
        .site-title {
            font-size: 2em;
            letter-spacing: 1px;
        }

        /*Site footer*/
        .site-footer {
            border-top: 1px solid #e8e8e8;
            padding: 30px 0;
            background: #adc1c7;
        }
    ```

3. Create an `assets` folder and add a file in it called `main.scss`. 
4. In the `main.scss` file add two lines, one is to load `_sass/minima.scss` file and the other is to import the custom.scss file as shown below:
    ```css
    --- 

    --- 
    /* load _sass/minima.scss */ 
    @import "minima";
    @import "custom" 
    ```

5. Build the site and make it available on a local server to check your changes.
    ```bash
    bundle exec jekyll serve
    ```

6. Browse to [http://localhost:4000](http://localhost:4000).
