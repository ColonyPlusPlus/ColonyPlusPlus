{% for release in site.github.releases %}
	<h1> {{ release.name }} </h1>

	{{ release.body }}
	```
	
	<a href="" class="download button"> {{ release.download_count }}</a>

{% endfor %}
