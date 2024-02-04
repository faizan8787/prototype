# prototype
[![Chart](https://img.shields.io/badge/dynamic/json?color=blue&label=Chart&query=%24.data1&url=https%3A%2F%2Fapi.apis.guru%2Fv2%2Fspec.json)](https://www.chartjs.org/)

<canvas id="myChart" width="400" height="200"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
    // Sample data for the chart
    var data = {
        labels: ["January", "February", "March", "April", "May"],
        datasets: [{
            label: "Monthly Data",
            data: [10, 20, 15, 25, 30],
            borderColor: "blue",
            fill: false
        }]
    };

    // Chart configuration
    var options = {
        responsive: true,
        maintainAspectRatio: false,
        tooltips: {
            mode: 'index',
            intersect: false
        },
    };

    // Create the chart
    var ctx = document.getElementById('myChart').getContext('2d');
    var myChart = new Chart(ctx, {
        type: 'line',
        data: data,
        options: options
    });
</script>
