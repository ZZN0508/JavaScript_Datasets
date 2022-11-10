var sbaseURL="hbsearch.senseforth.com/";
var pageUrl = window.location.href;
//var sbaseURL="localhost:8080/PredictiveSearchHDFCBank/";


var jsFile="/js/smartsearch-newui-V3.min.js";
//var rateplugin  ="/js/jquery.rateyo.js"
var cssfile = "/css/smartsearch-newui-V3.min.css";

// if (window.location.protocol == "https:") {
// baseURL = "https://"+baseURL;
// } else {
// baseURL = "http://"+baseURL;
// } 
try
{
 if(pageUrl.indexOf("portaluat.hdfcbank.com")>-1 || pageUrl.indexOf("portalnetuat.hdfcbank.com")>-1 )
 {
  sbaseURL = "hbankuat.senseforth.com/PredictiveSearchHDFCBank/";
  jsFile="/js/smartsearch-newui.min.js";
  cssfile = "/css/smartsearch-newui.min.css";
 }
}
catch(err)
{
 console.log(err);
}


 sbaseURL = "//"+sbaseURL;

function getStyleSheet(href){
 var link = document.createElement('link');
 link.type = 'text/css';
 link.rel = 'stylesheet';
 link.href = href;
 $("head").append(link);
}           
getStyleSheet(sbaseURL+cssfile);

function getScript(src) {
 var script = document.createElement("script");
 script.type = "text/javascript";
 script.src = sbaseURL+src;
 $("head").append(script);
}
//getScript(rateplugin);
getScript(jsFile);