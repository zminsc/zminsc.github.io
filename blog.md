---
layout: blog
title: Steven Chang's Blog
---

# Blog Posts

<div class="posts-container">
    {% for post in site.posts %}
        <a href="{{ post.url }}" class="post-link">
            <div class="post">
                    <h2>{{ post.title }}</h2>
                    <p class="post-description">{{ post.description }}</p>
                    <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
            </div>
        </a>
    {% endfor %}
</div>