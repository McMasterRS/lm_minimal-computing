---
layout: default
title: Customize Footer
parent: Customizing a Minima Jekyll theme
nav_order: 3
---

## Create a File Named `footer_pages.yml` in `_data` folder

An example of the `footer_pages.yml` file content is provided below:

```yaml
links:
  - contact.md
  - termandcondition.md
  - privacypolicy.md
```

## Create a File Named `footer.html` in `_includes` folder

An example of the `footer.html` file content is provided below:

```html
{% raw %}
<footer class="site-footer h-card">
    <data class="u-url" href="{{ " /" | relative_url }}"></data>
      <div class="footer-links">
        <div class="trigger-footer">
          {%- for path in site.data.footer_pages.links -%}
          {%- assign my_page = site.pages | where: "path", path | first -%}
          {%- if my_page.title -%}
          <a class="page-link" href="{{ my_page.url | relative_url }}">{{ my_page.title | escape }}</a>
          {%- endif -%}
          {%- endfor -%}
        </div>
        <div class="line"></div>
        <div class="footer-social">
          {%- include social.html -%}
        </div>
        <p class="copyright"><a href="http://www.examole.com/">© 2024</a></p>
      </div>
  </footer>
{% endraw %}
```
