# Highchart Border Radius

[![npm Version](https://img.shields.io/npm/v/highcharts-border-radius.svg)](https://www.npmjs.com/package/highcharts-border-radius)

### Installation
npm install highcharts-border-radius

### CDN
> [CDN](https://bluff-0.github.io/highcharts-border-radius/CDN.js)
```HTML
<!-- Paste below Highcharts CDN -->
<script src='https://bluff-0.github.io/highcharts-border-radius/CDN.js'></script>
```

### Usage
The plugin adds options for individual border radius to a highchart column chart.

* borderRadiusTopLeft
* borderRadiusTopRight
* borderRadiusBottomLeft
* borderRadiusBottomRight

### Node.JS Example
```javascript
const borderRadius = require('highcharts-border-radius')
borderRadius(Highcharts);

Highcharts.chart('.container', {
	chart: { type: 'column' },
	title: { text: 'Highcharts Border Radius' },
	xAxis: {
		categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
	},
	yAxis: {
		min: 0,
		title: {
			text: 'Example'
		}
	},
	plotOptions: {
		column: {
			borderRadiusTopLeft: 5,
			borderRadiusTopRight: 5
		}
	},
	series: [{
		name: 'Series 1',
		data: [1, 5, 9, 2, 4, 5, 7, 6]

	}, {
		name: 'Series 2',
		data: [8, 4, 6, 7, 1, 5, 4, 8]

	}, {
		name: 'Series 3',
		data: [9, 6, 7, 2, 6, 4, 7, 1]

	}]
});

```

### JavaScript Web Example
```Javascript
var columnChart = {
      chart: {
        type: 'column',
        renderTo: 'chart3',
      },
      title: {
        text: '',
      },
      credits: {
        enabled: false,
      },
      xAxis: {
        categories: ['17 Apr', '24 Apr', '1 May', '8 May', '15 May'],
        lineColor: 'transparent',
        labels: {
          style: {
            color: '#8F8F8F',
          },
        },
      },
      yAxis: {
        min: 0,
        gridLineColor: 'transparent',
        title: {
          enabled: false,
        },
        labels: {
          style: {
            color: '#8F8F8F',
          },
        },
        max: 300,
      },
      legend: {
        enabled: true,
        itemStyle: {
          color: '#8F8F8F',
        },
      },
      tooltip: {
        enabled: true,
        shared: true,
      },
      plotOptions: {
        series: {
          stacking: 'normal',
          pointWidth: 20,
          states: {
            hover: {
              enabled: false,
            },
          },
          events: {
            legendItemClick: function (e) {
              e.preventDefault();
            },
          },
          dataGrouping: {
            enabled: true,
            units: [['day', [1, 3, 6]]],
          },
        },
      },
      series: [
        {
          name: 'Dummy',
          data: [200, 150, 100, 150, 100],
          color: '#E9E9E9',
          showInLegend: false,
        },
        {
          name: 'Email',
          data: [80, 30, 120, 100, 40],
          borderRadiusTopLeft: 3,
          borderRadiusTopRight: 3,
          color: '#FC7500',
        },
        {
          name: 'Portal',
          data: [20, 120, 80, 50, 160],
          color: '#14AFF1',
        },
      ],
};

var chart = new Highcharts.chart(columnChart);
```
