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

 
