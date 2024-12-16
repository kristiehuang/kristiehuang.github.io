---
layout: default
title: Blog
permalink: /blog/
---

<div class="home">
      <i>Occasionally I publish longer reflections here; occasionally I publish shorter-form prose from the heart at <a href="https://kristieintheworld.substack.com/">kristieintheworld.substack.com</a>.</i>

<br>
{%- if site.posts.size > 0 -%}
<ul class="post-list">
{%- for post in site.posts -%}
<li>
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
<div class="post-meta">{{ post.date | date: date_format }}</div>

          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>

        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    <p class="rss-subscribe">Subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>

{%- endif -%}

</div>
