{% include downloadbox.html %}

## Past Releases

| Version              | Date                                           | Downloads                  | Links |
| -------------------- |:----------------------------------------------:| :------------------------: | :---- |{% for release in site.github.releases %}
| {{release.tag_name}} | {{ release.created_at | date_to_long_string }} | {{release.assets[0].download_count}} | <a href="" class="dl-btn btn"><i class="fa fa-list"></i>Changelog</a> <a href="" class="dl-btn btn"><i class="fa fa-github"></i>Source</a> <a href="" class="dl-btn btn"><i class="fa fa-download"></i>DLL</a>      |{% endfor %}
