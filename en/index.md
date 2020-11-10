---
layout: default
---

<div class="home">

  <h1 class="page-heading">Posts</h1>

  (Il y a aussi des
    <a href="{{ site.url }}/fr/index.html">articles en français</a>.)

  <p></p>

  {%- if site.posts.size > 0 -%}
    <ul class="post-list">
      {%- for post in site.posts -%}
      {%- if post.lang == 'en' -%}
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
