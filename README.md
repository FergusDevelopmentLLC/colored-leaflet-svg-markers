# colored-leaflet-svg-markers

Attempt at creating dynamically colored leaflet svg markers using L.divIcon...
Basically read in the text of the svg (its just xml), then use javascript to replace the generic gray color with a css color. Kind of a hack, but if the svgs are are all the same it
seems like is it should work.

based on
https://stackoverflow.com/questions/23567203/leaflet-changing-marker-color

![alt text](http://storage4.static.itmages.com/i/17/0530/h_1496167155_7515688_434b7e7677.png)

#### Issues

1. Feels hacky...
```javascript
var svg_code = props.svg_code.replace('rgba(17,34,51,0.88)',props.color);
svg_code = svg_code.replace('width="27"><title>','width="27" transform="scale(1.41)"><title>');//hacky, scale the svg code
```
2. Scaling doesn't work on firefox...
![alt text](http://storage7.static.itmages.com/i/17/0530/h_1496167571_9704904_123ff3edf3.png)

3. $.get svg code from svg in subfolder doesn't work on bl.ocks

#### URLS

https://github.com/FergusDevelopmentLLC/colored-leaflet-svg-markers

to...

https://gist.github.com/FergusDevelopmentLLC/3a3b79df9c2700d9fe448945e40d9f83

generates automagically...

http://bl.ocks.org/FergusDevelopmentLLC/3a3b79df9c2700d9fe448945e40d9f83
