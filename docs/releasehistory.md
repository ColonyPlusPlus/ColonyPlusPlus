{% include downloadbox.html %}

## Release History

| Version              | Date                                           | Downloads                  | Links |
| -------------------- |:----------------------------------------------:| :------------------------: | :---- |{% for release in site.github.releases %}
| {{release.tag_name}} | {{ release.created_at | date_to_long_string }} | {{release.assets[0].download_count}} | <a href="{{release.html_url}}" class="dl-btn btn"><i class="fa fa-list"></i> Changelog</a> <a href="{{release.assets[0].browser_download_url}}" class="dl-btn btn"><i class="fa fa-download"></i> Download</a>      |{% endfor %}

## Release Download History

<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("myChart").getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: [
        	{% for release in site.github.releases %}
        	"{{release.tag_name}}",
        	{% endfor %}
        	],
        datasets: [{
            label: '# of Votes',
            data: [
        	{% for release in site.github.releases %}
        	"{{release.assets[0].download_count}}",
        	{% endfor %}
        	],
            backgroundColor: [
            {% for release in site.github.releases %}
        	'rgba(1, 81, 101, 0.69)',
        	{% endfor %}               
            ],
            borderColor: [
	            {% for release in site.github.releases %}
	        	'rgba(1, 81, 101, 1)',
	        	{% endfor %}     
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero:true
                }
            }]
        }
    }
});
</script>