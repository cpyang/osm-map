# `osm-map` element

An OpenStreetMap polymer implementation. Based on OpenLayers (v3.3.0) and written in polymer 1.0 style.

## Usage

### Basic

	<osm-map longitude="{{ longitude }}" latitude="{{ latitude }}" zoom="{{ zoom }}"></osm-map>
	
<img src="https://cloud.githubusercontent.com/assets/1525818/12798245/a2f8c61e-cac8-11e5-8ad5-e8ebb0dd781d.png" width="500"/>
	
### Marker

	<osm-map latitude="53.834089" longitude="10.703718" zoom="16">
		<osm-marker longitude="10.703718" latitude="53.834089" scale="0.2" image="../data/marker-blue-shadow.png"></osm-marker>
		<osm-marker longitude="10.705318" latitude="53.835789" image="../data/marker-green-icon-shadow.png"></osm-marker>
		<osm-marker longitude="10.702318" latitude="53.832789" image="../data/marker-red.png"></osm-marker>
		<!-- marker without image attribute are displayed as circles -->
		<osm-marker longitude="10.705318" latitude="53.830789"></osm-marker>
		<osm-marker longitude="10.709318" latitude="53.839789" scale="2.5"></osm-marker>
	</osm-map>

### Polygon

    	<osm-poly fill fill-color="rgba(0,10,150,0.4)">
        	<template is="dom-repeat" items="{{ points }}">
          		<osm-point longitude$="{{ item.longitude }}" latitude$="{{ item.latitude }}"></osm-point>
        	</template>
    	</osm-poly> 

## Add `osm-map` component in your project

* Add bower dependency

  	    "dependencies": {
  		...,
    	"osm-map": "FabianBormann/osm-map"
  	    }

2.  
        
         $ bower install
	
In your project.html

	<link rel="import" href="path_to_bower_components/osm-map/osm-map.html">
	<link rel="import" href="path_to_bower_components/osm-map/osm-marker.html">
	<link rel="import" href="path_to_bower_components/osm-map/osm-point.html">
	<link rel="import" href="path_to_bower_components/osm-map/osm-poly.html">
	<link rel="import" href="path_to_bower_components/osm-map/osm-layer.html">

Now you are ready to start using the components.

## Development

Fork the repository and start to implement a new feature.
I hope to accept your pull-request if you are finished! :)

### Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

### Playing With osm-map

It's recommend that you use [Polyserve](https://github.com/PolymerLabs/polyserve) to keep the
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at `http://localhost:8080/components/osm-map/`.
