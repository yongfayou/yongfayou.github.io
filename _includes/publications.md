<h1 id="publications"></h1>

<h2 style="margin: 30px 0px 15px; padding-left: 15px;">Publications 
    <temp style="font-size:15px;">[</temp>
    <a href="https://scholar.google.com/citations?user=Bd5il3oAAAAJ&hl=en" target="_blank" style="font-size:15px;">Google Scholar</a>
    <temp style="font-size:15px;">]</temp>
    <temp style="font-size:15px;">[</temp>
    <a href="https://orcid.org/0000-0002-8916-2940" target="_blank" style="font-size:15px;">ORCID</a>
    <temp style="font-size:15px;">]</temp>
</h2>

<div class="publications" style="padding-left: 15px;">
  <ol class="bibliography" style="padding-left: 0; list-style: none; margin: 0;">
    {% assign gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/' %}
    {% assign url = gsDataBaseUrl | append: 'google-scholar-stats/gs_data.json' %}
    {% for link in site.data.publications.main %}

    <li style="margin-bottom: 0; padding: 10px 0; border-bottom: 1px solid #eaeaea;">
      <div style="text-align: left; margin: 0;">
        <div class="title" style="margin-bottom: 5px;">
          <a href="{{ link.pdf }}" style="text-decoration: none; font-weight: bold;">{{ link.title }}</a>
        </div>
        <div class="author" style="margin-bottom: 3px;">{{ link.authors }}</div>
        <div class="periodical" style="margin-bottom: 3px;"><em>{{ link.conference }}</em></div>
        <div class="links" style="margin-top: 5px;">
          {% if link.pdf %} 
          <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
          {% endif %}
          {% if link.code %} 
          <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
          {% endif %}
          {% if link.page %} 
          <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
          {% endif %}
          {% if link.bibtex %} 
          <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
          {% endif %}
          {% if link.notes %} 
          <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
          {% endif %}
          {% if link.others %} 
          {{ link.others }}
          {% endif %}
          {% if link.citation %} 
          <strong><a style="color:#e74d3c; font-weight:600;"> • <i class="total_citation_mtl" data-citation="{{ link.citation }}"></i> <i style="color:#e74d3c; font-weight:600;">Citations</i></a></strong>
          <script>
            $(document).ready(function () {
                var gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/';
                $.getJSON(gsDataBaseUrl + "google-scholar-stats/gs_data.json", function (data) {
                    var citationEles = document.getElementsByClassName('total_citation_mtl');
                    Array.prototype.forEach.call(citationEles, function(element) {
                        var citationKey = element.getAttribute('data-citation');
                        if (data['publications'][citationKey]) {
                            var numCitations = data['publications'][citationKey]['num_citations'];
                            element.innerHTML = numCitations;
                        } else {
                            element.innerHTML = 'N/A';
                        }
                    });
                });
            });
          </script>
          {% endif %}
        </div>
      </div>
    </li>

    {% endfor %}
  </ol>
</div>
