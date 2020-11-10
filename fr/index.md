---
layout: default
---

<div class="home">

  <h1 class="page-heading">Articles en français</h1>

  (Most of these posts have
    <a href="{{ site.url }}/en/index.html">English versions here</a>.)

  <p></p>

  {%- if site.posts.size > 0 -%}
    <ul class="post-list">
      {%- for post in site.posts -%}
      {%- if post.lang == 'fr' -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endif -%}
      {%- endfor -%}
    </ul>

  {%- endif -%}


</div>
