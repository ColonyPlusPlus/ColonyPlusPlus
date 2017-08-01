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
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
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