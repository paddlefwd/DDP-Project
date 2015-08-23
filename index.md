---
title       : Whitewater Streamflow 
subtitle    : Popular Western US Sections
author      : Chris Rank
job         : 
framework   : html5slides   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---



<h1>Whitewater Streamflow Application</h1>

<br>
<br>
Chris Rank

Developing Data Products

Aug. 23, 2015

---

### Background - National Water Information System
The National Water Information System (NWIS) provides a single point of access for near real-time data from water gauging stations from local, state and federal agencies all across the United States.


The specific set of data returned by a station depends on the source type (stream or reservoir) and the particular sensor package installed but stations commonly report:

* streamflow volume or reservoir level
* air and water temperatures
* water quality indicators


---

### Whitewater Boating and Streamflow

Whitewater boaters consider many factor when assessing the difficulty of a river section:
* gradient  - how steep is it?
* obstructions - is the channel rocky or smooth?
* streamflow - how much water is going down the channel?


The first two elements are fairly constant; unless there are major floods or other changes these characteristics of a section do not change much from year to year. 

As the daily or seasonal streamflow changes mean that obstacles are exposed or covered and wave sizes increase or decrease. Boaters use this streamflow information to determine whether a run is within their capabilities depending on the level of hazard associated with a given flow.

---

#### Whitewater Streamflow Application
The Whitewater Streamflow application retrieves flow information for a selection of popular stream gauges and allows the user to place a simple regression line on the data to see the trend over time.


<!-- Map generated in R 3.2.1 by googleVis 0.5.9 package -->
<!-- Sat Aug 22 17:10:31 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataMapID3515271b9a72 () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 40.03665248,
-106.4400324,
"Section: Gore Canyon<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?09058000>09058000</a><BR>Location: Colorado River near Kremmling, CO" 
],
[
 38.4872189,
-105.373604,
"Section: Royal Gorge<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?07094500>07094500</a><BR>Location: Arkansas River at Parkdale, CO" 
],
[
 36.3200333,
-105.7544444,
"Section: Taos Box<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?08276500>08276500</a><BR>Location: Rio Grande Below Taos Junction Bridge near Taos, NM" 
],
[
 40.90829296,
-109.422914,
"Section: Dinosaur (Lodore)<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?09234500>09234500</a><BR>Location: Green River near Greendale, UT" 
],
[
 36.8647099,
-111.588216,
"Section: Grand Canyon<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?09380000>09380000</a><BR>Location: Colorado River at Lee's Ferry AZ" 
],
[
 45.75027778,
-116.3238889,
"Section: Main Salmon<BR>Station: <a href=http://waterdata.usgs.gov/nwis/uv?13317000>13317000</a><BR>Location: Salmon River at White Bird ID" 
] 
];
data.addColumn('number','Latitude');
data.addColumn('number','Longitude');
data.addColumn('string','Info');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartMapID3515271b9a72() {
var data = gvisDataMapID3515271b9a72();
var options = {};
options["showTip"] = true;
options["tooltip"] = {isHtml:'True'};
options["enableScrollWheel"] = true;
options["mapType"] = "terrain";
options["useMapTypeControl"] = true;

    var chart = new google.visualization.Map(
    document.getElementById('MapID3515271b9a72')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "map";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartMapID3515271b9a72);
})();
function displayChartMapID3515271b9a72() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartMapID3515271b9a72"></script>
 
<!-- divChart -->
  
<div id="MapID3515271b9a72" 
  style="width: 500; height: automatic;">
</div>

Note: If map does not draw full width please refresh this slide.

---

### Using the Whitewater Streamflow Application


Run the [Whitewater Streamflow Application](http://paddlefwd.shinyapps.io/Streamflows).

To retrieve streamflow data and view flow trend:

1. From the pulldown, select the river section
2. Set the number of days to retrieve on the slider
3. Once the data is back you can adjust the number of days used for trendline with the lower slider.

Note that this application retrieves live data from the NWIS server, it may take a few seconds to update the streamflow graph!

