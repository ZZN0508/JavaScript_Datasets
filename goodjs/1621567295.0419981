var sbaseURL="icicibanksmartsearch.senseforth.com/ICICI/";    //should not use http://

var jsFile="smartsearch-v2.1.9.min.js"; //  minified js file

var cssfile = "smartsearch-v2.1.9.min.css"; // minfied css file

// var sbaseURL="localhost:8080/PredictiveSearchICICIBank/ICICI/";    //should not use http://

//  var jsFile="smartsearch-v2.1.9.js"; // for local testing 

//  var cssfile = "smartsearch-v2.1.9.css" // for local testing


 if (window.location.protocol == "https:") {
 sbaseURL = "https://"+sbaseURL;
 } else {
 sbaseURL = "http://"+sbaseURL;
 } 

function getStyleSheet(href){
 var link = document.createElement('link');
 link.type = 'text/css';
 link.rel = 'stylesheet';
 link.href = href;
 document.body.appendChild(link);
}           
getStyleSheet(sbaseURL+cssfile);

function getScript(src) {
 var script = document.createElement("script");
 script.type = "text/javascript";
 script.src = sbaseURL+src;
 document.body.appendChild(script);
}

getScript(jsFile);