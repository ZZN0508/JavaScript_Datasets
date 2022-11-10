const analyticsUrls={RUM:{E1:"https://cdaas-dev.aexp.com/one/rum-telemetry/0.3.0.js",E2:"https://qwww.aexp-static.com/cdaas/one/rum-telemetry/0.3.0.js",E3:"https://www.aexp-static.com/cdaas/one/rum-telemetry/0.3.0.js"},trackIt:{E1:"https://cdaas-dev.americanexpress.com/one/statics/@americanexpress/trackit/1.1.3/package/dist/trackit-dev.js",E2:"https://qwww.aexp-static.com/cdaas/akamai/one/statics/@americanexpress/trackit/1.1.3/package/dist/trackit-qa.js",E3:"https://www.aexp-static.com/cdaas/akamai/one/statics/@americanexpress/trackit/1.1.3/package/dist/trackit.js"}};
(function(){var e;
var d=function(){};
var b=["assert","clear","count","debug","dir","dirxml","error","exception","group","groupCollapsed","groupEnd","info","log","markTimeline","profile","profileEnd","table","time","timeEnd","timeline","timelineEnd","timeStamp","trace","warn"];
var c=b.length;
var a=(window.console=window.console||{});
while(c--){e=b[c];
if(!a[e]){a[e]=d
}}}());
const includeScriptHelper=function(b){let newScript=document.createElement("script");
newScript.type="text/javascript";
newScript.async=true;
const a=window.location.origin;
let src=b.E3;
if(a.includes("localhost")||a.includes("dev")){src=b.E1
}else{if(a.includes("qa")){src=b.E2
}else{src=b.E3
}}newScript.src=src;
let s=document.getElementsByTagName("script")[0];
s.parentNode.insertBefore(newScript,s)
};
includeScriptHelper(analyticsUrls.RUM);
includeScriptHelper(analyticsUrls.trackIt);