<h1 id="Research"></h1>

<h2 style="margin: 80px 0px -15px;">Research</h2>

<div class="publications">
  <ol class="bibliography">

    {% for link in site.data.research.main %}
    <li>
      <div class="pub-row">
        <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
          <abbr class="badge">{{ link.project_short }}</abbr>
        </div>
        <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
          <div class="title"><a href="{{ link.web }}">{{ link.title }}</a></div>
          <div class="author">{{ link.authors }}</div>
          <div class="abstract" style="font-style: normal;">{{ link.abstract }}</div>
          <div class="periodical"><em>{{ link.project }}</em></div>
        </div>
      </div>
    </li>

    <br>

    {% endfor %}

  </ol>
</div>
