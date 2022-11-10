var scriptTag = document.getElementById('bx-tag');

function getHashParam(name) {
 var matches = window.location.hash.match(new RegExp(name + '=([^&]*)'));
 return matches ? matches[1] : '';
}

function canReachTopWindow() {
 try { return window.top.document && true; } catch (e) {}
 return false;
}

function addIframeBuster(filePath, websiteId) {
 var iframe = document.createElement('iframe');
 iframe.src = filePath + '#isIframeBuster=1&id=' + websiteId;
 iframe.async = true;
 document.body.appendChild(iframe);
}

function addTag(websiteId) {
 var doc = window.top.document;
 var script = doc.createElement('script');
 script.src = doc.location.protocol + '//tag.bounceexchange.com/' + websiteId + '/i.js';
 script.async = true;
 doc.getElementsByTagName('head')[0].appendChild(script);
}

if (!!getHashParam('isIframeBuster')) {
 addTag(getHashParam('id'));
} else if (scriptTag) {
 var websiteId = scriptTag.getAttribute('data-website-id');
 var iframeBusterPath = scriptTag.getAttribute('data-buster-path');

 if (canReachTopWindow()) {
  addTag(websiteId);
 } else {
  addIframeBuster(iframeBusterPath, websiteId);
 }
}