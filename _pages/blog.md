---
layout: default
permalink: /blog/
title: blog
nav: true
nav_order: 1
---

<div class="post">
  <header class="post-header">
    <h1 class="post-title">{{ page.title }}</h1>
  </header>

  <article>
    {% assign only_post = site.posts | where: "slug", "how-i-prepare-research-presentation" %}
    {% if only_post and only_post.size > 0 %}
      <div class="table-responsive">
        <table class="table table-sm table-borderless">
          {% for item in only_post %}
            <tr>
              <th scope="row" style="width: 20%">{{ item.date | date: '%b %d, %Y' }}</th>
              <td>
                {% if item.redirect == blank %}
                  <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                {% elsif item.redirect contains '://' %}
                  <a class="news-title" href="{{ item.redirect }}" target="_blank">{{ item.title }}</a>
                  <svg width="2rem" height="2rem" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
                    <path
                      d="M17 13.5v6H5v-12h6m3-3h6v6m0-6-9 9"
                      class="icon_svg-stroke"
                      stroke="#999"
                      stroke-width="1.5"
                      fill="none"
                      fill-rule="evenodd"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    ></path>
                  </svg>
                {% else %}
                  <a class="news-title" href="{{ item.redirect | relative_url }}">{{ item.title }}</a>
                {% endif %}
              </td>
            </tr>
          {% endfor %}
        </table>
      </div>
    {% else %}
      <p>No blog posts available.</p>
    {% endif %}
  </article>
</div>
