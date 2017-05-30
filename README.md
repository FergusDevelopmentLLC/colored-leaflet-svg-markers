# colored-leaflet-svg-markers

Attempt at creating dynamically colored leaflet svg markers using L.divIcon...
Basically read in the text of the svg (its just xml), then use javascript to replace the generic gray color with a css color. Kind of a hack, but if the svgs are are all the same it
seems like is it should work.

based on
https://stackoverflow.com/questions/23567203/leaflet-changing-marker-color

#### when running on localhost?

![alt text](http://storage5.static.itmages.com/i/17/0530/h_1496116404_5947757_4bf6e4a11c.png "random color on refresh, only last one in array?")

  1. why is it small, wrong size?

  2. why does only one work?
    has to do with doing everything in the jQuery $.get?
    maybe populate an array first, then pass array of them to marker placer function?

  3. this feels a bit hacky. maybe just use something like:
    https://github.com/lvoogdt/Leaflet.awesome-markers
    as suggested on the stackoverflow post

##### trying to get it working on bl.ocks...

1. http://bl.ocks.org/FergusDevelopmentLLC/3a3b79df9c2700d9fe448945e40d9f83
  no icons show...

2. how to get around error, after trying to use a public svg url like:

http://imgh.us/park-15.svg

![alt text](http://imgh.us/park-15.svg "here it is!")

//XMLHttpRequest cannot load http://imgh.us/park-15.svg. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://bl.ocks.org' is therefore not allowed access.

when i use a web accessable svg file...
http://imgh.us/park-15.svg


#### URLS

https://github.com/FergusDevelopmentLLC/colored-leaflet-svg-markers

to...

https://gist.github.com/FergusDevelopmentLLC/3a3b79df9c2700d9fe448945e40d9f83

generates automagically...

http://bl.ocks.org/FergusDevelopmentLLC/3a3b79df9c2700d9fe448945e40d9f83



Relevant stack overflow posts?

#### Basic AJAX request gets “No 'Access-Control-Allow-Origin' header is present on the requested resource” error

https://stackoverflow.com/questions/35304817/basic-ajax-request-gets-no-access-control-allow-origin-header-is-present-on-t/

But in general, cross-origin requests can do really bad things. Say that you, Zoltan, are using coolsharks.com. Say also that you are logged into mybank.com and there is a cookie for mybank.com in your browser. Now, suppose that coolsharks.com sends an AJAX request to mybank.com, asking to transfer all your money into another account. Because you have a mybank.com cookie stored, they successfully complete the request. And all of this happens without your knowledge, because no page reload occurred. This is the danger of allowing general cross-site AJAX requests.

#### A CORS POST request works from plain javascript, but why not with jQuery?

https://stackoverflow.com/questions/5584923/a-cors-post-request-works-from-plain-javascript-but-why-not-with-jquery
