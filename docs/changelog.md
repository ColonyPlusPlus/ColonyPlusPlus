{% for release in site.github.releases %}
	<h1> {{ release.name }} </h1>

	<div class="release-body box">
	{{ release.body }}
	</div>
	
	<a href="" class="download button"> {{ release.download_count }}</a>

{% endfor %}
