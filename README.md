# prototype
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chart Prototype</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>

<body>
    <canvas id="myChart" width="400" height="200"></canvas>

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
</body>

</html>
