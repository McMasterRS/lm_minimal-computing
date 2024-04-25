---
layout: page
title: Customize Header and Navbar
parent: Customizing a Minima Jekyll theme
nav_order: 2
---

## Steps to modify the Header and include a custom Navbar 

### Create a `header_pages.yml` file

To configure our navigation bar (navbar), we utilize the `header_pages.yml` file to outline the structure of the navbar by specifying the header pages that we want to add in the navbar, and indicating any dropdown or nested dropdown menus to include.

In your Jekyll folder:

1. Create a new folder named `_data`.
2. In the `_data` folder, create a file named `header_pages.yml`.

    An example of the `header_pages.yml` file content is provided below:

    ```yaml
    links:
    - title: "Home"
    href: "/"
    - title: "Locations"
    href: "/locations/"
    - title: "Our Vision"
    href: "/vision"
    - title: "Resources"
    href: "/resources/"
    - title: "Articls"
    subcategories:
        - subtitle: "Popular Articles"
        subhref: "/popular-articles/"
        - subtitle: "Recent Articles"
        subhref: "/recent-articles/"
        subcategories:
            - subtitle: "article1"
            subhref: "/articles/article1/"
            - subtitle: "Article2"
            subhref: "/articles/article2/"
    - title: "About"
    href: "/about-us"
    ```

### Create a `nav.html` file

In your Jekyll folder:

1. Create a new folder named `_includes`.
2. In the `_includes` folder, create a file named `nav.html`.

    An example of the `nav.html` file content is provided below:
    ```html
    {% raw %}
    <ul class="menu">
        {% for item in site.data.header_pages.links %}
        {% if item.subcategories != null %}
        <!-- Start of dropdown menu -->
        <div class="dropdown">
            <li>
                <!-- Button to toggle submenu visibility -->
                <button class="dropbtn" onclick="toggleSubmenu('{{ item.title }}')"> {{ item.title }}
                    <span class="caret"></span>
                </button>
                <!-- Submenu for current item -->
                <ul class="sub-menu" id="home-{{ item.title }}">
                    {% for subcategory in item.subcategories %}
                    <li>
                        {% if subcategory.subcategories %}
                        <!-- Start of nested dropdown -->
                        <div class="dropdown drop-menu">
                            <button class="dropbtn" onclick="toggleSubmenu('{{ subcategory.title }}')"> {{
                                subcategory.subtitle }}
                                <span class="caret caret-sub"></span>
                            </button>
                            <!-- Submenu for nested subcategory -->
                            <ul class="sub-menu" id="home-{{ subcategory.title }}">
                                {% for nested_subcategory in subcategory.subcategories %}
                                <li>
                                    {% if nested_subcategory.subcategories %}
                                    <!-- Start of nested dropdown -->
                                    <div class="dropdown">
                                        <button class="dropbtn" onclick="toggleSubmenu('{{ nested_subcategory.title }}')">
                                            {{ nested_subcategory.subtitle }}
                                            <span class="caret"></span>
                                        </button>
                                        <!-- Submenu for nested nested subcategory -->
                                        <ul class="sub-menu" id="home-{{ nested_subcategory.title }}">
                                            {% for sub_subcategory in nested_subcategory.subcategories %}
                                            <!-- Submenu item -->
                                            <li><a href="{{site.baseurl}}{{ sub_subcategory.subhref }}">{{
                                                    sub_subcategory.subtitle }}</a></li>
                                            {% endfor %}
                                        </ul>
                                    </div>
                                    <!-- End of nested dropdown -->
                                    {% else %}
                                    <!-- Submenu item -->
                                    <a href="{{site.baseurl}}{{ nested_subcategory.subhref }}">{{
                                        nested_subcategory.subtitle }}</a>
                                    {% endif %}
                                </li>
                                {% endfor %}
                            </ul>
                        </div>
                        <!-- End of nested dropdown -->
                        {% else %}
                        <!-- Submenu item -->
                        <a href="{{site.baseurl}}{{ subcategory.subhref }}">{{ subcategory.subtitle }}</a>
                        {% endif %}
                    </li>
                    {% endfor %}
                </ul>
            </li>
        </div>
        <!-- End of dropdown menu -->
        {% else %}
        <!-- Regular menu item -->
        <li><a href="{{site.baseurl}}{{ item.href }}" class="page-link">{{ item.title }}</a></li>
        {% endif %}
        {% endfor %}
    </ul>

    <!-- JavaScript to handle submenu toggling -->
    <script>
        // Function to toggle submenu visibility
        function toggleSubmenu(title) {
            var targetId = "home-" + title;
            var submenu = document.getElementById(targetId);

            // Find all sub-menus at the same level as the clicked submenu
            if (submenu) {
                var parentLi = submenu.closest('.dropdown');
                var siblingSubmenus = parentLi.parentElement.querySelectorAll('.sub-menu');

                // Close all sibling submenus except the clicked one
                siblingSubmenus.forEach(function (otherSubmenu) {
                    if (otherSubmenu.id !== targetId) {
                        otherSubmenu.classList.remove('show');
                    }
                });

                // Toggle the clicked submenu
                submenu.classList.toggle("show");
            }
        }

        // Global event listener to handle clicks outside the submenus
        document.addEventListener('click', function (event) {
            if (!event.target.closest('.dropdown')) {
                // Close all submenus if the clicked area is outside of any dropdown
                document.querySelectorAll('.sub-menu').forEach(function (submenu) {
                    submenu.classList.remove('show');
                });
            }
        });
    </script>
    {% endraw %}
    ```

### Include the navbar in the header file

1. In the `_includes` folder, create a file named `header.html`.

    An example of the header.html file content is provided below:

    ```html
    <header class="site-header" role="banner">
    <div class="wrapper">
        <a class="site-title" rel="author" href="{{ "/" | relative_url }}">{{ site.title | escape }}</a>
    </div>
    </header>

    <nav class="site-nav">
        {% include nav.html  %}
    </nav>
    ```

### Add custom stylesheet for the navbar

1. In the `custom.scss` file add the code below to customize your navbar stylesheet.

    ```css
    .site-nav {
        padding: 0;
        box-shadow: 0 0 36px rgba(94, 106, 113, 0.4);
        background-color: #adc1c7 !important;
        z-index: 10;
        display: flex;
        justify-content: center;
    }

    .site-nav .menu {
        display: flex;
        margin: 0;
    }

    .site-nav ul li a {
        color: #ffffff;
        text-decoration: none;
    }
    .menu a {
        padding: 14px 16px;
        line-height: 1em;
    }

    .dropdown .dropbtn {
        cursor: pointer;
        border: none;
        outline: none;
        color: rgb(0, 0, 0);
        padding: 14px 16px;
        background-color: inherit;
        font-family: inherit;
        text-transform: uppercase;
        letter-spacing: 1px;
        line-height: 1em;
        font-weight: 500;
        list-style-type: none;
        font-family: 'Roboto', sans-serif;
    }

    .drop-menu .dropbtn {
        color: #ffffff;
    }

    .sub-menu {
        display: none;
        position: absolute;
        border-style: solid;
        border-radius: 5px;
        border-color: rgb(80, 79, 79);
        background-color: black;
        margin: 0em;
    }

    .sub-menu a {
        float: none;
        color: rgb(255, 255, 255);
        text-decoration: none;
        display: block;
        text-align: left;
        text-transform: uppercase;
        padding: 1em !important;
        transition: color 0.5s ease;

    }

    .show {
        display: block;
    }

    .caret {
        display: inline-block;
        width: 0;
        height: 0;
        vertical-align: middle;
        border-top: 4px solid;
        border-right: 4px solid transparent;
        border-left: 4px solid transparent;
    }

    .dropdown ul ul {
        position: absolute;
        left: 100%;
        bottom: -35px;
    }

    .caret-sub {
        border-top: 4px solid transparent;
        border-left: 4px solid;
        border-bottom: 4px solid transparent;
    }
    ```
