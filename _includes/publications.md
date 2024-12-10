---
layout: homepage
---

<h1 id="publications"></h1>
<h2 style="margin: 60px 0px 10px;">Publications</h2>

<div class="publications" style="padding-left: 15px;">
  <ol class="bibliography" style="padding: 0; margin: 0; list-style: none;">
    {% assign gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/' %}
    {% assign url = gsDataBaseUrl | append: 'google-scholar-stats/gs_data.json' %}
    {% for link in site.data.publications.main %}

    <li style="margin-bottom: 15px;">
      <div style="margin: 0; padding: 0;">
        <div class="title" style="font-weight: bold; font-size: 16px; margin-bottom: 5px;">
          <a href="{{ link.pdf }}" style="text-decoration: none; color: #0073e6;">{{ link.title }}</a>
        </div>
        <div class="author" style="font-size: 14px; color: #555; margin-bottom: 3px;">
          {{ link.authors }}
        </div>
        <div class="periodical" style="font-size: 13px; font-style: italic; color: #777; margin-bottom: 3px;">
          {{ link.conference }}
        </div>
        <div class="links" style="margin-top: 5px; font-size: 12px;">
          {% if link.pdf %}
          <a href="{{ link.pdf }}" target="_blank" style="text-decoration: none; color: #0073e6; margin-right: 10px;">PDF</a>
          {% endif %}
          {% if link.code %}
          <a href="{{ link.code }}" target="_blank" style="text-decoration: none; color: #0073e6; margin-right: 10px;">Code</a>
          {% endif %}
          {% if link.page %}
          <a href="{{ link.page }}" target="_blank" style="text-decoration: none; color: #0073e6; margin-right: 10px;">Project Page</a>
          {% endif %}
          {% if link.bibtex %}
          <a href="{{ link.bibtex }}" target="_blank" style="text-decoration: none; color: #0073e6; margin-right: 10px;">BibTex</a>
          {% endif %}
          {% if link.notes %}
          <span style="color: #e74d3c;">{{ link.notes }}</span>
          {% endif %}
          {% if link.citation %}
          <span style="color: #e74d3c;"> • {{ link.citation }} Citations</span>
          {% endif %}
        </div>
      </div>
    </li>

    {% endfor %}
  </ol>
</div>
