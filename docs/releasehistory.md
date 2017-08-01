{% include downloadbox.html %}

## Past Releases

| Version              | Date                                           | Downloads                  | Links |
| -------------------- |:----------------------------------------------:| :------------------------: | :---- |{% for release in site.github.releases %}
| {{release.tag_name}} | {{ release.created_at | date_to_long_string }} | {{release.assets[0].download_count}} | <a href="" class="dl-btn btn">Changelog</a> <a href="" class="dl-btn btn">Source</a> <a href="" class="dl-btn btn">DLL</a>      |{% endfor %}
