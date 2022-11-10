console.log("top.location:"+top.location);
console.log("self.location:"+self.location);
console.log("document.referrer:"+document.referrer);
console.log("window.location.href:"+window.location.href);
console.log("document.location.href:"+document.location.href);
console.log("top.location.href:"+top.location.href);
/*
if (top.location != self.location && document.referrer.search("ettoday.net") < 0) {
  top.location.href = window.location.href;
}
*/
/*
if (window.location.href.indexOf("moneylife.vip") > 0) {
  var oriURL = decodeURIComponent(window.location.href.split("url=")[1]);
  console.log("oriURL:"+oriURL);
  //window.location.href = oriURL;
  window.location.href = "https://www1.tipo.gov.tw/lp.asp?CtNode=7853&CtUnit=3885&BaseDSD=7&mp=1";
}
*/

/* 20210421
if (document.referrer.indexOf("google.com") > 0 && window.location.href.indexOf("dx688") > 0) {
 var AmpHtmlUrl_1 = "";
 var links = document.getElementsByTagName("link");
 for (var i = 0; i < links.length; i ++) {
     if (links[i].getAttribute("rel").toLowerCase() === "amphtml") {
         AmpHtmlUrl_1 = links[i].getAttribute("href")
     }
 }
 var fromStr_1 = "dx688.net"; 
 console.log("AmpHtmlUrl_1:"+AmpHtmlUrl_1);
 window.location.href = "https://www.ettoday.net"+AmpHtmlUrl_1+ "&from="+ fromStr_1;
}


if (window.location.href.indexOf("xn--uis76ch9al24a1k5b.net") > 0) {
 var canonicalUrl = "";
 var links = document.getElementsByTagName("link");
 for (var i = 0; i < links.length; i ++) {
     if (links[i].getAttribute("rel").toLowerCase() === "canonical") {
         canonicalUrl = links[i].getAttribute("href")
     }
 }
 var fromStr = "贏家娛樂城"; 
 console.log("canonicalUrl:"+canonicalUrl);
 window.location.href = "https://www.ettoday.net"+canonicalUrl+ "&from="+ fromStr;
}
*/

// ============================================================
var u = navigator.userAgent;
 isLineApp = u.indexOf("Line") > -1;
 isFbApp = u.indexOf("FB") > -1; 
 isNewsRepublic = u.indexOf("TopBuzz") > -1; 
 isPuffin = u.indexOf("Puffin") > -1; 
 isEdge = u.indexOf("Edg") > -1; 
 isXiaoMi = u.indexOf("XiaoMi") > -1; 
 isSamsung = u.indexOf("SamsungBrowser") > -1; 
 isWeixinApp = u.indexOf("MicroMessenger") > -1; 
 isOpera = u.indexOf("Opera") > -1 || u.indexOf("OPR/") > -1;
 isFF = u.indexOf("Firefox") > -1 || u.indexOf("FxiOS") > -1;

 isSafari = u.indexOf("Safari") > -1 && u.indexOf("Chrome") === -1 && u.indexOf("CriOS") === -1 && u.indexOf("FxiOS") === -1;

 isAndroid = u.indexOf("Android") > -1; 
 isIphone = u.indexOf("iPhone") > -1; 

var isMobile = false;
var isChrome = false;

if (isIphone){
  isMobile = true;
  isChrome = u.indexOf("CriOS") > -1;
} else if (isAndroid) {
  isMobile = true;
  if ( u.indexOf("wv") > -1 ) {
      isChrome = false;
  } else if ( u.indexOf("Safari") > -1 && u.indexOf("Chrome") > -1 ) {
      if (isEdge || isOpera || isXiaoMi || isSamsung || isPuffin) {
         isChrome = false;
      } else {
         isChrome = true;
      }
  } else {
      isChrome = false;
  }
} else {
  if ( u.indexOf("Mobile") > -1 ) {
      isMobile = true;
  } else {
      isMobile = false;
      isChrome = u.indexOf("Chrome") > -1 && !isWeixinApp && !isEdge && !isOpera && !isPuffin;
  }
}

var myCountry = $.cookie("et_client_country");

// 台灣 or 海外★
isNotChrome = (myCountry === "TW") && !isChrome;
//isNotChrome = (myCountry === "TW" || myCountry === "HK" || myCountry === "MO" || myCountry === "CN" || myCountry === "MY" || myCountry === "SG") && !isChrome;

//Get amphtml 的值======================*/
var AmpHtmlUrl = "";
var links = document.getElementsByTagName("link");
for (var i = 0; i < links.length; i ++) {
    if (links[i].getAttribute("rel").toLowerCase() === "amphtml") {
        AmpHtmlUrl = links[i].getAttribute("href")
    }
}
console.log("amphtml:"+AmpHtmlUrl);

if(isChrome) {// Chrome
 var toAMP = true;
}else{// 非 Chrome
 if (myCountry === "" || myCountry === null || myCountry === "TW") {//無國家cookie 或 台灣
  if($.cookie("etAMP")===null){ // ★沒有 cookie 時★
   var toAMP = true;
   //var toAMP = false;
  }else{
   if($.cookie("etAMP")==="On"){ //cookie 設為 On 時
    var toAMP = true;
   } else {
    var toAMP = false;
   }
  }
 }else{//非台灣
  var toAMP = true;
 }
}
console.log("toAMP:" + toAMP);
console.log("etAMP:" + $.cookie("etAMP"));

if (isMobile) {//手機
 // etInterstitialAd ===================================
 var etInterstitialAd_JS = document.createElement("script");
 etInterstitialAd_JS.type = "text/javascript";
 etInterstitialAd_JS.src = "https://cdn1.ettoday.net/banners/0/3-4.js";
 document.head.appendChild(etInterstitialAd_JS);
}

//取得 from 值
var fromStr = "";

if (isMobile && window.location.href.indexOf("boba.ettoday.net") === -1 && window.location.href.indexOf("fashion.ettoday.net") === -1 && document.referrer.indexOf("facebook.com") === -1) {//手機 & 非播吧, 非時尚, 非 FB
 (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
 (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
 m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
 })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
 ga('create', 'UA-42712477-6', 'auto', {'name': 'AmpReferer'});
 ga('AmpReferer.require', 'displayfeatures');
 ga('AmpReferer.send', 'pageview');
 ga("AmpReferer.send", "event", "AmpRefererTest", ""+document.referrer+"", ""+document.location.href+"", {'nonInteraction': 0});
}

if (toAMP && isMobile && AmpHtmlUrl !== ""){ 
 if (document.referrer.indexOf("yahoo.com") > 0){ 
  fromStr = "yahoo.com"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("bing.com") > 0){ 
  fromStr = "bing.com"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf(".cc") > 0 && document.referrer.indexOf("popin") === -1){ 
  fromStr = ".cc"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("amp_news") > 0){ 
  fromStr = "amp_news"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("amp-logo") > 0){ 
  fromStr = "amp-logo"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("amp-hnav") > 0){ 
  fromStr = "amp-hnav"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("amp-sidenav") > 0){ 
  fromStr = "amp-sidenav"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("ampproject.org") > 0){ 
  fromStr = "ampproject.org"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("googleapis.com") > 0){ 
/*
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
  ga('create', 'UA-42712477-6', 'auto', {'name': 'AmpReferer'});
  ga('AmpReferer.require', 'displayfeatures');
  ga('AmpReferer.send', 'pageview');
  ga("AmpReferer.send", "event", "AmpReferer", ""+document.referrer+"", ""+document.location.href+"", {'nonInteraction': 0});
*/
  fromStr = "googleapis.com"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("news.google.com") > 0){ 
  fromStr = "news.google.com"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("googlequicksearchbox") > 0){ 
/*
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
  ga('create', 'UA-42712477-6', 'auto', {'name': 'AmpReferer'});
  ga('AmpReferer.require', 'displayfeatures');
  ga('AmpReferer.send', 'pageview');
  ga("AmpReferer.send", "event", "AmpReferer", ""+document.referrer+"", ""+document.location.href+"", {'nonInteraction': 0});
*/
  fromStr = "googlequicksearchbox"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("google.com") > 0){ 
/*
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
  ga('create', 'UA-42712477-6', 'auto', {'name': 'AmpReferer'});
  ga('AmpReferer.require', 'displayfeatures');
  ga('AmpReferer.send', 'pageview');
  ga("AmpReferer.send", "event", "AmpReferer", ""+document.referrer+"", ""+document.location.href+"", {'nonInteraction': 0});
*/
  if (window.location.href.indexOf("dx688") > 0) {
   var fromStr = "dx688.net"; 
   window.location.href = "https://www.ettoday.net"+AmpHtmlUrl_1+ "&from="+ fromStr;
  } else {
   fromStr = "google.com"; 
   window.location.href = AmpHtmlUrl + "&from="+ fromStr;
  }
 } else if (document.referrer.indexOf("m.facebook.com") > 0 && window.location.href.indexOf("from=") === -1){ 
  fromStr = "m.facebook.com"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("socialife") > 0){ 
  fromStr = "socialife"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf("taoo.in") > 0){ 
  fromStr = "taoo.in"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf(".org") > 0){ 
  fromStr = ".org"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 } else if (document.referrer.indexOf(".edu") > 0){ 
  fromStr = ".edu"; 
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 //} else if (document.referrer.indexOf("nativeapp.toutiao.com") > 0){ 
 } else if (isNewsRepublic){
  if (isIphone) {
   fromStr = "NewsRepublic"; 
   window.location.href = AmpHtmlUrl + "&from="+ fromStr;
  }
 }
}


//取得今日日期
var todays = new Date();
if (todays.getMonth() + 1<10) {
    var month = "0" + (todays.getMonth() + 1);
} else {
    var month = todays.getMonth() + 1;
}
if (todays.getDate() <10) {
    var day = "0" + todays.getDate();
} else {
    var day = todays.getDate();
}
today = todays.getFullYear().toString() + month.toString() + day.toString();
console.log("today:"+today);

var targetDay = Number(today.toString())-0; //★-1是前天轉, -0是昨天轉
console.log("targetDay:"+targetDay);


//取得新聞日期
var newsDate = today;
if (window.location.href.indexOf("www.ettoday.net/news/20") > 0) { //是主頻新聞頁
  var newsDate = window.location.href.split("/news/")[1]; //用/news/分隔網址，取出/news/右邊的字串
  if(newsDate.indexOf("/") >= 0){//如果/news/右邊的字串中有/號時
    newsDate = newsDate.split("/")[0];//用/分隔網址，取出/左邊的字串，即為新聞日期
  }
}
console.log("newsDate:"+newsDate);

if (toAMP && isMobile && window.location.href.indexOf("from=") > 0 && AmpHtmlUrl !== ""){ 
 fromStr = window.location.href.split("from=")[1];//用from=分隔網址，取出from=右邊的字串
 if(fromStr.indexOf("&") >= 0){//如果from=右邊的字串中有&號時
  fromStr = fromStr.split("&")[0];//用&分隔網址，取出&左邊的字串，即為 from 值
 }
 var toAMP1 = (window.location.href.indexOf("from=dable") > 0) && (fromStr !=="dable_Customised_bottom");
 var toAMP2 = window.location.href.indexOf("from=popin") > 0 || window.location.href.indexOf("from=mwebtaglist") > 0 || window.location.href.indexOf("from=rss") > 0 || window.location.href.indexOf("from=feature") > 0 || window.location.href.indexOf("from=etstar_app") > 0 || window.location.href.indexOf("from=amp_newslist") > 0;
 //var toAMP3 = window.location.href.indexOf("from=ettoday_app") > 0 && window.location.href.indexOf("forum.ettoday.net") === -1;
 var toAMP4 = (window.location.href.indexOf("from=line") > 0) && (newsDate < targetDay);
 var toAMP5 = (window.location.href.indexOf("from=fb") > 0) && (newsDate < targetDay);
 var toAMP6 = (window.location.href.indexOf("from=ig") > 0) && (newsDate < targetDay);
 var toAMP7 = window.location.href.indexOf("newsshare") > 0 && window.location.href.indexOf("forum.ettoday.net") === -1;
 if ( toAMP1 || toAMP2  || toAMP4 || toAMP5 || toAMP6 || toAMP7){
  window.location.href = AmpHtmlUrl + "&from="+ fromStr;
 }
}

console.log("document.referrer:"+document.referrer);
console.log("from:"+fromStr);

//廣告個別處理=================================================
if (window.location.href.indexOf("1565046") > 0){ //2019/12/20
 var adCustomziedCss = '.adM14 {display:none!important}';
 head = document.head || document.getElementsByTagName('head')[0];
 adCustomziedStyle = document.createElement('style');
 adCustomziedStyle.type = 'text/css';
 adCustomziedStyle.appendChild(document.createTextNode(adCustomziedCss));
 head.appendChild(adCustomziedStyle); 
}

//Adsense Auto Ads =========================== Start

//指定時段設定
var etStartHour = 2;//<--開始：時
var etStartMinute = 00;//<---開始：分
var etPlayStopHour = 5;//<---結束：時
var etPlaySopMinute = 59;//<---結束：分

//抓取現在時間
var RightNOW = new Date();
var this_hour = RightNOW.getHours();
var this_minute = RightNOW.getMinutes();
var this_second = RightNOW.getSeconds();

//靜音期間設定：以0時為0，分別計數出各時間點距0時幾秒
var AutoStartTime = (etStartHour*60*60)+(etStartMinute*60);
var AutoStopTime = (etPlayStopHour*60*60)+(etPlaySopMinute*60);
var RightTime = (this_hour*60*60)+(this_minute*60);

//依時段不同
if (AutoStartTime <= RightTime && RightTime <= AutoStopTime) {//現在時間在指定時段內
 if (fromStr === "") { fromStr = "redirect3" };
 var isAbroad = myCountry !== "" && myCountry !== null; //全球
 //var isAbroad = myCountry !== "" && myCountry !== null && myCountry !== "TW" && myCountry !== "US" && myCountry !== "HK"; //非台灣,非美國,非香港
 //if (toAMP && isMobile && window.location.href.indexOf("from=") > 0 && AmpHtmlUrl !== ""){ 
 if (toAMP && isMobile && AmpHtmlUrl !== ""){ 
  if (window.location.href.indexOf("from=") > 0){ 
   window.location.href = AmpHtmlUrl + "&redirect=3&from="+ fromStr;
  } else if (document.referrer.indexOf("m.facebook.com") > 0 && window.location.href.indexOf("from=") === -1){ 
   fromStr = "m.facebook.com"; 
   window.location.href = AmpHtmlUrl + "&redirect=3&from="+ fromStr;
  }
 }
} else {//其它時段
 var isAbroad = myCountry !== "" && myCountry !== null && myCountry !== "TW" && myCountry !== "US"; //非台灣,非美國
 //var isAbroad = myCountry !== "" && myCountry !== null && myCountry !== "TW" && myCountry !== "US" && myCountry !== "HK"; //非台灣,非美國,非香港
}

var myChannle = window.location.href.indexOf("travel") >0 || window.location.href.indexOf("pets") >0 || window.location.href.indexOf("game") >0;
console.log("isAbroad:"+isAbroad);
console.log("myChannle:"+myChannle);

var etPath = window.location.href.split("ettoday.net/")[1];//用 ettoday.net/ 分隔網址，取出 ettoday.net/ 右邊的字串
var isHomepage = etPath === "";
var isNotHomepage = etPath !== "" && etPath !== "?from=logo" && etPath !== "?from=rf";
console.log("etPath:"+etPath);
console.log("isNotHomepage:"+isNotHomepage);

//if ( isAbroad && isMobile && myChannle && isHomepage ) { //非台灣 & 指定的頻道 & 非首頁 & 手機
//if ( isAbroad && isMobile && isNotHomepage ) { //非台灣 & 全頻道 & 非首頁 & 手機
//if ( isAbroad && isMobile && window.location.href.indexOf("star") === -1 ) { //非台灣 & ★非星光雲 & 手機
//if ( isAbroad && isMobile ) { //非台灣 & ★全頻道 & 手機 
if ( isAbroad && isMobile && isChrome ) { //非台灣 & ★全頻道 & 手機 & isChrome
 var script5 = document.createElement("script");
 script5.type = "text/javascript";
 script5.async = true;
 script5.id = "AdsenseAutoAd";
 script5.setAttribute("data-ad-client","ca-pub-7504183592568612");
 script5.src = "https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js";
 document.head.appendChild(script5);
 console.log("★Adsense JS Loaded!★");
}
//Adsense Auto Ads =========================== End

//DFP ============================== Start
var script0 = document.createElement("script");
script0.type = "text/javascript";
script0.async = true; //dfp async
script0.src = "https://securepubads.g.doubleclick.net/tag/js/gpt.js";
document.head.appendChild(script0);
window.googletag = window.googletag || {cmd: []};

//DFP ============================== End

if (isMobile) {//手機

 //新聞雲_全頻道_流量統計(MobileWeb)
 var ts = Math.random();
 var script3 = document.createElement("script");
 script3.type = "text/javascript";
 script3.src = "https://ad.ettoday.net/ads.php?bid=all_pageviews_mobileweb&rr="+ ts;
 document.head.appendChild(script3);

 // Avivid 禾多
 //var script_Avivid = document.createElement("script");
 //script_Avivid.type = "text/javascript";
 //script_Avivid.src = "https://cdn2.ettoday.net/ad/avivid/ettoday.js";
 //document.head.appendChild(script_Avivid);

}else{////非手機

 // AndBeyond JS =============================================
 /*
 var AndBeyond_JS = document.createElement("script");
 AndBeyond_JS.type = "text/javascript";
 AndBeyond_JS.async = true;
 AndBeyond_JS.src = "https://rtbcdn.andbeyond.media/prod-global-550782.js";
 document.head.appendChild(AndBeyond_JS);
 */

 //新聞雲_全頻道_流量統計(電腦版)
 var ts = Math.random();
 var script3 = document.createElement("script");
 script3.type = "text/javascript";
 script3.src = "https://ad.ettoday.net/ads.php?bid=all_pageviews_desktop&rr="+ ts;
 document.head.appendChild(script3);

 // 閒置廣告 =============================================================
 var myCountry = $.cookie("et_client_country");
 if (myCountry === "TW" || myCountry === "HK" || myCountry === "MO" || myCountry === "CN" || myCountry === "MY" || myCountry === "SG") { //台港澳中星馬
  if (window.location.href.indexOf("fashion") === -1 && window.location.href.indexOf("house") === -1 && window.location.href.indexOf("boba") === -1) { //非時尚, 且非房產, 且非播吧
   var script1 = document.createElement("script");
   script1.type = "text/javascript";
   script1.async = true;
   script1.src = "//static.ettoday.net/ad/idle-ad/idle-ad-970.js";
   document.head.appendChild(script1);
  }
 }

}

// Prebid (Truvid) ============================================
/*
var script6 = document.createElement("script");
script6.type = "text/javascript";
script6.src = "https://cnt.trvdp.com/prebid/ettoday/prebid.js";
document.head.appendChild(script6);
*/

// Prebid ===================================================
var script4 = document.createElement("script");
script4.type = "text/javascript";
script4.src = "https://static.ettoday.net/ad/prebid/prebid.js?v=4.38.0";
document.head.appendChild(script4);

// CRITEO CDB =============================================
var script2 = document.createElement("script");
script2.type = "text/javascript";
script2.async = true;
script2.src = "https://static.criteo.net/js/ld/publishertag.js";
document.head.appendChild(script2);
if (isMobile) {//手機
 var CriteoAdUnits = { "placements": [
     /* Criteo Placements List */
     { "slotid": "criteo_783188", "zoneid": 783188 }, // EtToday - TW - CDB - SA - MOBILE - 300x250 Top
     { "slotid": "criteo_783189", "zoneid": 783189 }, // EtToday - TW - CDB - SA - MOBILE - 300x250 Bottom
     { "slotid": "criteo_1191499", "zoneid": 1191499 }, // EtToday - TW - CDB - SA - MOBILE - 300x250 Inread
 ]};
}else{//非手機
 var CriteoAdUnits = { "placements": [
     /* Criteo Placements List */
     { "slotid": "criteo_1191499", "zoneid": 1191499 }, // EtToday - TW - CDB - SA - MOBILE - 300x250 Inread
     { "slotid": "criteo_943528", "zoneid": 943528 }, // EtToday - TW - CDB - SA - 300x250 - Article UP Left (PC)
     { "slotid": "criteo_1086336", "zoneid": 1086336 }, // EtToday - TW - CDB - SA - 970x250 - Top (PC)
     { "slotid": "criteo_806580", "zoneid": 806580 }, // EtToday - TW - CHB - SA - 300x250 (PC)
     { "slotid": "criteo_1086335", "zoneid": 1086335 }, // EtToday - TW - CDB - SA - 300x250 - #2  (PC)
     { "slotid": "criteo_806581", "zoneid": 806581 }, // EtToday - TW - CHB - SA - 300x600 (PC)
     { "slotid": "criteo_845893", "zoneid": 845893 }, // EtToday - TW - CDB - SA - 300x250 - Bottom Right (PC)
 ]};
}
window.Criteo = window.Criteo || {}; window.Criteo.events = window.Criteo.events || [];
var CriteoBids=CriteoBids||{},CriteoBidsReceived=function(){for(var t in CriteoAdUnits.placements){var e=CriteoAdUnits.placements[t],i=Criteo.GetBidsForAdUnit(e.slotid);CriteoBids[e.slotid]=i.length>0?i[0]:null}},CriteoDisplayAd=function(t,e,i){if(void 0===i&&(i=0),null!==CriteoBids[t])if(void 0===CriteoBids[t]&&null!==CriteoBids[t])100>i&&setTimeout(function(){CriteoDisplayAd(t,e,i+1)},200);else{var r=document.getElementById(t);if(r){var s=document.createElement("iframe");s.setAttribute("id",t+"_iframe"),s.setAttribute("frameborder","0"),s.setAttribute("allowtransparency","true"),s.setAttribute("hspace","0"),s.setAttribute("marginwidth","0"),s.setAttribute("marginheight","0"),s.setAttribute("scrolling","no"),s.setAttribute("vspace","0"),s.setAttribute("width",CriteoBids[t].width),s.setAttribute("height",CriteoBids[t].height),r.appendChild(s);var o='<script src="'+CriteoBids[t].displayUrl+'"></scr'+'ipt>',d=s.contentWindow.document;d.open(),d.write(o),d.close()}}else"function"==typeof e&&e()};
Criteo.events.push(function() { Criteo.RequestBids(CriteoAdUnits, CriteoBidsReceived, 2000); });

// Dable =============================================================
if (window.location.href.indexOf("fashion.ettoday.net") === -1) {//非時尚
 (function(d,a,b,l,e,_) {
 d[b]=d[b]||function(){(d[b].q=d[b].q||[]).push(arguments)};e=a.createElement(l);
 e.async=1;e.charset='utf-8';e.src='//static.dable.io/dist/plugin.min.js';
 _=a.getElementsByTagName(l)[0];_.parentNode.insertBefore(e,_);
 })(window,document,'dable','script');

 if (window.location.href.indexOf("star.ettoday.net") !== -1) {//星光雲
   dable('setService', 'star.ettoday.net');
 } else if (window.location.href.indexOf("boba.ettoday.net") !== -1) {//播吧
   dable('setService', 'boba.ettoday');
 } else if (window.location.href.indexOf("www.ettoday.net/dalemon") !== -1) {//大檸檬
   dable('setService', 'dalemon.ettoday');
 } else {//其它頻道
     if (isMobile) {//手機
       dable('setService', 'm.ettoday.net');
     }else{////非手機
       dable('setService', 'pc.ettoday.net');
     }
 }
 dable('sendLogOnce');
}

// CSS 修正 =========================================================
//var myHotTopicCss = '.block_1 .part_menu_3, .block_a .part_menu_3{display:none;} .ad_in_news {margin:10px auto;text-align:center} .ad_in_news img {display:inline!important} .ad_in_news .adIF01, .ad_in_news .adJS01 {margin:0 auto!important}/*修正新聞中圖片廣告置中問題*/';
//var myHotTopicCss = '#hot-trip{display:none!important} .ad_in_news {margin:10px auto;text-align:center} .ad_in_news img {display:inline!important} .ad_in_news .adIF01, .ad_in_news .adJS01 {margin:0 auto!important}/*隱藏出國趣*/ .ad_320x50_fixed { z-index:9999} /*修正 Trvuvid 問題，把置底廣告重在 Truvid 下方*/';
var myHotTopicCss = '#oneadICIPTag{margin-bottom:10px!important}.ad_in_news .ad_readmore{margin-bottom:5px}.ad_in_news {margin:10px auto;text-align:center} .ad_in_news img {display:inline!important} .ad_in_news .adIF01, .ad_in_news .adJS01 {margin:0 auto!important}/*修正新聞中圖片廣告置中問題*/ .ad_320x50_fixed { z-index:99999!important} /*修正 Trvuvid 問題，把置底廣告重在 Truvid 下方*/';
head = document.head || document.getElementsByTagName('head')[0];
myHotTopicStyle = document.createElement('style');

myHotTopicStyle.type = 'text/css';
myHotTopicStyle.appendChild(document.createTextNode(myHotTopicCss));
head.appendChild(myHotTopicStyle); 

/*
document.addEventListener("DOMContentLoaded", function(event) { 
  if (document.getElementsByClassName('ad_readmore').length >0) {
    //document.getElementsByClassName("ad_readmore")[0].innerHTML = "[廣告] 請繼續往下閱讀...";
    var InNewsNode=document.createElement("span");
    var InNewsTextnode=document.createTextNode("[廣告] ");
    InNewsNode.appendChild(InNewsTextnode);
    document.getElementsByClassName("ad_readmore")[0].prepend(InNewsNode);
  }
});
*/
/*
$(function(){
 if($(".part_menu_3 a:contains('★★★')").index() != -1 || $("#tag-cloud a:contains('★★★')").index() != -1){
  $(".part_menu_3 a:contains('★★★'), #tag-cloud a:contains('★★★')").css({"visibility":"hidden","position":"absolute","bottom":"0"});
 }
 $(".block_1 .part_menu_3, .block_a .part_menu_3").show();
});
*/

//變數 =========================================
console.log("navigator.userAgent:"+navigator.userAgent);
console.log("myCountry:"+myCountry);
console.log("isMobile:"+isMobile);
console.log("isChrome:"+isChrome);
console.log("isNotChrome:"+isNotChrome);
console.log("window.innerWidth:"+window.innerWidth);
console.log("window.screen.width:"+window.screen.width);