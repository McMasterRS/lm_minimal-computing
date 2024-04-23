---
layout: default
title: Customize Footer
parent: Customizing a Minima Jekyll theme
nav_order: 12
---

## 1. In the _data folder, create a file named "footer_pages.yml".

An example of the footer_pages.yml file content is provided below:

```ts
links:
  - contact.md
  - termandcondition.md
  - privacypolicy.md
```

## 2. In the _includes folder, create a file named "footer.html".

An example of the footer.html file content is provided below:

```ts
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