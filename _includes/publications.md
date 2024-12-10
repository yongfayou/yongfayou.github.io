<h1 id="publications"></h1>

<h2 style="margin: 30px 0px 15px; padding-left: 15px; font-family: Arial, sans-serif; font-size: 24px; color: #333;">Publications 
    <span style="font-size: 14px; color: #555;">[</span>
    <a href="https://scholar.google.com/citations?user=Bd5il3oAAAAJ&hl=en" target="_blank" style="font-size: 14px; color: #0073e6; text-decoration: none;">Google Scholar</a>
    <span style="font-size: 14px; color: #555;">]</span>
    <span style="font-size: 14px; color: #555;">[</span>
    <a href="https://orcid.org/0000-0002-8916-2940" target="_blank" style="font-size: 14px; color: #0073e6; text-decoration: none;">ORCID</a>
    <span style="font-size: 14px; color: #555;">]</span>
</h2>

<div class="publications" style="padding-left: 15px;">
  <ol class="bibliography" style="padding-left: 0; list-style: none; margin: 0;">
    {% assign gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/' %}
    {% assign url = gsDataBaseUrl | append: 'google-scholar-stats/gs_data.json' %}
    {% for link in site.data.publications.main %}

    <li style="margin-bottom: 15px; padding: 15px; border: 1px solid #ddd; border-radius: 8px; background-color: #f9f9f9;">
      <div style="text-align: left; margin: 0;">
        <!-- Title -->
        <div class="title" style="margin-bottom: 8px; font-size: 18px; font-weight: bold; font-family: Arial, sans-serif;">
          <a href="{{ link.pdf }}" style="text-decoration: none; color: #0073e6;">{{ link.title }}</a>
        </div>
        
        <!-- Authors -->
        <div class="author" style="margin-bottom: 5px; font-size: 14px; color: #555; font-family: Arial, sans-serif;">
          {{ link.authors }}
        </div>
        
        <!-- Conference -->
        <div class="periodical" style="margin-bottom: 5px; font-size: 14px; font-style: italic; color: #777;">
          {{ link.conference }}
        </div>
        
        <!-- Links -->
        <div class="links" style="margin-top: 10px;">
          {% if link.pdf %} 
          <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px; margin-right: 10px; text-decoration: none; color: white; background-color: #0073e6; padding: 6px 12px; border-radius: 4px;">PDF</a>
          {% endif %}
          {% if link.code %} 
          <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px; margin-right: 10px; text-decoration: none; color: white; background-color: #0073e6; padding: 6px 12px; border-radius: 4px;">Code</a>
          {% endif %}
          {% if link.page %} 
          <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px; margin-right: 10px; text-decoration: none; color: white; background-color: #0073e6; padding: 6px 12px; border-radius: 4px;">Project Page</a>
          {% endif %}
          {% if link.bibtex %} 
          <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px; margin-right: 10px; text-decoration: none; color: white; background-color: #0073e6; padding: 6px 12px; border-radius: 4px;">BibTex</a>
          {% endif %}
          {% if link.notes %} 
          <strong><i style="color: #e74d3c;">{{ link.notes }}</i></strong>
          {% endif %}
          {% if link.others %} 
          {{ link.others }}
          {% endif %}
          {% if link.citation %} 
          <strong><a style="color:#e74d3c; font-weight: 600;"> • <i class="total_citation_mtl" data-citation="{{ link.citation }}"></i> <i style="color:#e74d3c; font-weight:600;">Citations</i></a></strong>
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
