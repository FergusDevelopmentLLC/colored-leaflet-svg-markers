# colored-leaflet-svg-markers

Attempt at creating dynamically colored leaflet svg markers using L.divIcon...
Basically read in the text of the svg (its just xml), then use javascript to replace the generic gray color with a css color. Kind of a hack, but if the svgs are are all the same it
seems like is it should work.

based on
https://stackoverflow.com/questions/23567203/leaflet-changing-marker-color

why is it small, wrong size?

why does only one work?
  has to do with doing everything in the jQuery $.get?
  maybe populate an array first, then pass array of them to marker placer function?

this feels a bit hacky. maybe just use something like:
https://github.com/lvoogdt/Leaflet.awesome-markers
as suggested on the stackoverflow post
