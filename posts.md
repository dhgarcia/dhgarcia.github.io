---
layout: default
---

# [](#my-posts)Posts


{% if site.posts.size > 0 %}
<!-- <h1 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h1> -->
  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      {% if site.show_excerpts %}
        {{ post.excerpt }}
      {% endif %}
    </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
{% endif %}



<!-- #### [jump to top](#my-posts)
#### [back](javascript:history.back()) -->

[:arrow_heading_up:](#about-me) [:leftwards_arrow_with_hook:](javascript:history.back())
