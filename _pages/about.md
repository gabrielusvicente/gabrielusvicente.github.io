---
title: "About"
layout: default
sitemap: false
permalink: /about/
---

{% if site.author %}
    {% assign author = site.data.authors[site.author] %}
    {{ author.bio }}
    "I haven’t been everywhere, but it’s on my list." – Susan Sontag
{% endif %}

<!-- Styles -->
<style>
#chartdiv {
  width: 100%;
  height: 500px;
}
</style>

<!-- Resources -->
<script src="https://www.amcharts.com/lib/3/ammap.js"></script>
<script src="https://www.amcharts.com/lib/3/maps/js/worldLow.js"></script>
<script src="https://www.amcharts.com/lib/3/maps/js/worldHigh.js"></script>

<!-- Chart code -->
<script type="text/javascript">
/**
 * Define SVG path for target icon
 */
var targetSVG = "M9,0C4.029,0,0,4.029,0,9s4.029,9,9,9s9-4.029,9-9S13.971,0,9,0z M9,15.93 c-3.83,0-6.93-3.1-6.93-6.93S5.17,2.07,9,2.07s6.93,3.1,6.93,6.93S12.83,15.93,9,15.93 M12.5,9c0,1.933-1.567,3.5-3.5,3.5S5.5,10.933,5.5,9S7.067,5.5,9,5.5 S12.5,7.067,12.5,9z";

/**
 * Create the map
 */
var map = AmCharts.makeChart( "chartdiv", {
  "type": "map",
  "projection": "eckert5",
  "imagesSettings": {
    "rollOverColor": "#089282",
    "rollOverScale": 2,
    "selectedScale": 3,
    "selectedColor": "#089282",
	"color": "#5599FF",
  },
  "areasSettings": {
	"autoZoom" : false,
	"color" : "#B4B4B7",
	"colorSolid" : "#88DDEE",
	"selectedColor" : "#993366",
	"outlineColor" : "#666666",
	"rollOverColor" : "#888888",
	"rollOverOutlineColor" : "#888888",
    "unlistedAreasColor": "#15A892",
    "outlineThickness": 0.2
  },
  "dataProvider": {
    "map": "worldHigh",
	"getAreasFromMap" : true,
	"areas" :
	[
		{
			"id": "US",
			"showAsSelected": true
		},
		{
			"id": "BR",
			"showAsSelected": true
		},
		{
			"id": "IL",
			"showAsSelected": true
		},
		{
			"id": "JO",
			"showAsSelected": true
		},
		{
			"id": "PS",
			"showAsSelected": true
		},
		{
			"id": "CZ",
			"showAsSelected": true
		},
		{
			"id": "NL",
			"showAsSelected": true
		},
		{
			"id": "HU",
			"showAsSelected": true
		},
		{
			"id": "DE",
			"showAsSelected": true
		},
		{
			"id": "PL",
			"showAsSelected": true
		},
		{
			"id": "AT",
			"showAsSelected": true
		},
		{
			"id": "SK",
			"showAsSelected": true
		},
		{
			"id": "FR",
			"showAsSelected": true
		}
	],
	"images": 
	[
		{
			"svgPath": targetSVG,
			"zoomLevel": 5,
			"scale": 1.0,
			"title": "Miami",
			"latitude": 25.7617,
			"longitude": -80.1918
		}, 
		{
			"svgPath": targetSVG,
			"zoomLevel": 5,
			"scale": 1.0,
			"title": "São Paulo",
			"latitude": -23.5505,
			"longitude": -46.6333
		}, 
		{
			"svgPath": targetSVG,
			"zoomLevel": 5,
			"scale": 1.0,
			"title": "Prague",
			"latitude": 50.0755,
			"longitude": 14.4378
		},
		{
			"svgPath": targetSVG,
			"zoomLevel": 5,
			"scale": 1.0,
			"title": "New York",
			"latitude": 40.7128,
			"longitude": -74.0060
		}
	]
  },
});
</script>

<!-- HTML -->
<div id="chartdiv"></div>

