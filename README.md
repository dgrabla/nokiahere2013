okay just let's try to use the Nokia Map API,
for making an App to "Job location visualization" alias jobLocalizer.

Configuration:
- host on branch project-GitHub-page http://dgrabla.github.com/nokiahere2013
- As this little program grabs json from the server, the server needs to send this header
 Header set Access-Control-Allow-Origin "*"


Starting from an simple example code.
 - display 100% a Map on Screen
 - add functionality like move and zoom the Map, an overlay Info Container
 - at first call this page use the location where it called from
    - by Hardware (GPS-Sensor)
    - or a Browser-Geolocalisations detection (HTML5) js code
 - link to open a textfield for type in an other Citty name and jump to after send
 - set a marker on position and center it

next step
 - use meteor.com to have a client/server site and a public folder for images css
 - setup mongodb
 - put json sampledata in DB
 - add code read json in the page 
 - create maker for each dataitem and add an onclick for more info if available


-------------

var clickHandler = function(a,b,c){
  alert(a + b + c);
};


// Create several StandardMarkers with the properties object defined above and placed around the map center
while (i--) {
	var marker = new nokia.maps.map.StandardMarker(
		/* We use  nokia.maps.geo.Coordinate.walk to generate
		 * geoCoordinate for created StandardMarker;
		 * 
		 * Coordinate.walk takes 3 arguments
		 * 		- bearing: The bearing to use in the calculation in degrees 
		 * 		- distance: The distance to the destination in meters 
		 * 		- [overGreatCircle]: Optional argument
		 * 				By default false. 
		 * 				If set true the computation uses the "Great Circle" algorithm otherwise "Rhumb Line". 
		 */
		map.center.walk(360 / standardMarkerProps.length * i, 6000), 
		// Initial values for StandardMarker properties
		standardMarkerProps[i] 
	);
	map.objects.add(marker);
	marker.addListener('click', (function(a,b,c){
		return function(){
			clickHandler(a,b,c);
		};
	}(i,'a','b')));
	
}