---
title: Steven Chang's Website
---
<h1 id="homepage-heading">Steven Chang's Website</h1>

<nav id="homepage-links">
    {% for link in site.data.homepage_links %}
        <a href="{{ link.url | relative_url }}">{{ link.name }}</a>
    {% endfor %}
</nav>

This website is currently a work in progress.
