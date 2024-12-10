<h1 id="publications"></h1>

<h2 style="margin: 0; padding-left: 15px;">Publications 
    <temp style="font-size:15px;">[</temp>
    <a href="https://scholar.google.com/citations?user=Bd5il3oAAAAJ&hl=en" target="_blank" style="font-size:15px;">Google Scholar</a>
    <temp style="font-size:15px;">]</temp>
    <temp style="font-size:15px;">[</temp>
    <a href="https://orcid.org/0000-0002-8916-2940" target="_blank" style="font-size:15px;">ORCID</a>
    <temp style="font-size:15px;">]</temp>
</h2>

<div class="publications" style="padding-left: 15px;">
  <ol class="bibliography" style="padding: 0; margin: 0; list-style: none;">
    {% assign gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/' %}
    {% assign url = gsDataBaseUrl | append: 'google-scholar-stats/gs_data.json' %}
    {% for link in site.data.publications.main %}

    <li style="margin: 0; padding: 0;">
      <div style="text-align: left; margin: 0; padding: 0;">
        <div class="title" style="margin: 0; padding: 0; font-weight: bold;">
          <a href="{{ link.pdf }}" style="text-decoration: none; color: #0073e6;">{{ link.title }}</a>
        </div>
        <div class="author" style="margin: 0; padding: 0; font-size: 14px;">{{ link.authors }}</div>
        <div class="periodical" style="margin: 0; padding: 0; font-size: 13px; font-style: italic; color: #555;">{{ link.conference }}</div>
      </div>
    </li>

    {% endfor %}
  </ol>
</div>
