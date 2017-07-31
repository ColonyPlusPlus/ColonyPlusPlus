{% for release in site.github.releases %}
	## {{ release.name }}

	{{ release.body }}
	
	<a href="" class="download button"> {{ release.download_count }}</a>

{% endfor %}
