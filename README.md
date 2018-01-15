[![npm version](https://badge.fury.io/js/napchart.svg)](https://badge.fury.io/js/napchart)

*Drag-and-drop time-planning library using HTML5 and the canvas element. Used by [napchart.com](https://napchart.com/)*

![enter image description here](https://larskarbo.no/napchart.PNG)

## Installation

You can download the latest version of Napchart from the [GitHub releases](https://github.com/larskarbo/napchart/releases/latest)

To install via npm:
```bash
npm install napchart --save
```

## Create a Chart

It is easy to create a Napchart on your page. All you need is a `canvas` element and some javascript code

```html
<canvas id="myNapchart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("myNapchart").getContext('2d')
var myNapchart = Napchart.init(ctx, {
	// data goes here
	elements: [{
		"start":720,
		"end": 790,
		"text": "Cool text"
	},{
		"start":1420,
		"end":400
	}]
}, {
	// options go here
)
</script>
```

## Data

The second *data* parameter of `napchart.init` defines what data should initially be drawn to the napchart. The structure is simple like this

```javascript
var defaultData = {
  elements: [],
  shape: 'circle',
  lanes: 1,
}
```

You don't need to specify shape or lanes if you don't want to. If you don't specify anything at all it will start with a blank napchart

## Options

The third parameter of `napchart.init` is an object where you can specify options. Here are the defaults

```javascript
{
	interaction: true,
	penMode: true,
	responsive: false,
	background: 'transparent',
	fontColor: '#aaaaaa'
}
```

## Contributing

See [CONTRIBUTING.md](https://github.com/larskarbo/napchart/blob/master/CONTRIBUTING.md) for a sweet introduction to the code-base
