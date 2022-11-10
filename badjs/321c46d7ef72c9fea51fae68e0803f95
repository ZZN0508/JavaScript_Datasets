var aTag = ["aside","figcaption","figure","footer","header","hgroup","nav","section"],i = 0;for(i in aTag){document.createElement(aTag[i]);}

function change1(){
    document.getElementById('163').style.opacity='1';
    document.getElementById('126').style.opacity='0.4';
	document.getElementById('yeah').style.opacity='0.4';
	document.getElementById('tel').style.opacity='0.4';
	document.getElementById('tu').style.top='32px';
	document.getElementById('login1').style.display='block';
	document.getElementById('login2').style.display='none';
	document.getElementById('login3').style.display='none';
	document.getElementById('login4').style.display='none';
}
function change2(){
    document.getElementById('163').style.opacity='0.4';
    document.getElementById('126').style.opacity='1';
	document.getElementById('yeah').style.opacity='0.4';
	document.getElementById('tel').style.opacity='0.4';
	document.getElementById('tu').style.top='115px';
	document.getElementById('login1').style.display='none';
	document.getElementById('login2').style.display='block';
	document.getElementById('login3').style.display='none';
	document.getElementById('login4').style.display='none';
}
function change3(){
    document.getElementById('163').style.opacity='0.4';
    document.getElementById('126').style.opacity='0.4';
	document.getElementById('yeah').style.opacity='1';
	document.getElementById('tel').style.opacity='0.4';
	document.getElementById('tu').style.top='205px';
	document.getElementById('login1').style.display='none';
	document.getElementById('login2').style.display='none';
	document.getElementById('login3').style.display='block';
	document.getElementById('login4').style.display='none';
}
function change4(){
    document.getElementById('163').style.opacity='0.4';
    document.getElementById('126').style.opacity='0.4';
	document.getElementById('yeah').style.opacity='0.4';
	document.getElementById('tel').style.opacity='1';
	document.getElementById('tu').style.top='288px';
	document.getElementById('login1').style.display='none';
	document.getElementById('login2').style.display='none';
	document.getElementById('login3').style.display='none';
	document.getElementById('login4').style.display='block';
}


// 全局异常日志
window.onerror=function(_msg,_url,_line,_col,_obj){
var _pd = window._$PRODUCT||'';
var _pkid = window._$PKID||'';
var _h = decodeURIComponent(location.search);
_h = _h.substring(1)||'';
_h = _h.split('&');
for(var i = 0,_temp; i < _h.length; i++){
_temp = _h[i].split('=');
if (_temp[0]=='pkid'){
_pkid = _temp[1]
}
if (_temp[0]=='product'){
_pd = _temp[1]
}
}
_msg = _msg.replace(/\^/g,'$');
_url = _url.replace(/\^/g,'$');
var _img = document.createElement('img'),
_params = 'pd='+_pd+'&pkid='+_pkid+'&msg='+encodeURIComponent(_msg||'')+'&url='+encodeURIComponent(_url||'');
var ext = [];
ext.push(window.navigator.userAgent);
var f = arguments && arguments.callee && arguments.callee.caller, c = 3;
// 只拿3层堆栈信息
if (!!arguments.callee){
while (f && (--c>0)) {
ext.push(f.toString());
if (f === f.caller) {
break;//如果有环
}
f = f.caller;
}
ext = ext.join("%%");
ext = ext.replace(/\^/g,'$');
_params += '&ext='+encodeURIComponent(ext);
}else{
_params += '&ext='+encodeURIComponent(window.navigator.userAgent);
}
var _log = '//dl.reg.163.com/pgErr?'+_params;
_log = _log.slice(0,2000);
_img.style.width = 0;
_img.style.height = 0;
setTimeout(function(){
_img.src = _log;
},0);
}
// url解析
var _u=decodeURIComponent(location.search);
var _ht=location.host;
window._$BGP=0;
if (_ht.indexOf('webzj2')>=0||_ht.indexOf('passport2')>=0||_ht.indexOf('reg2')>=0||_ht.indexOf('dl2')>=0){
window._$BGP=1;
}
window.wdaId = 0;
if(_u.indexOf('?')!=-1){
var _sl = _u.substring(1)||'';
var _s= _sl.split('&');
var _d,_c,_cssl;
for(var i= 0,_l=_s.length;i<_l;i++){
if(_s[i].indexOf('cd=')===0){
_d = _s[i].split('=')[1];
}else if(_s[i].indexOf('cf=')===0){
_cssl = _s[i].split('=');
_cssl.shift();
_c = _cssl.join('=');
}else if(_s[i].indexOf('MGID=')===0){
window.mgid = _s[i].split('=')[1];
}else if (_s[i].indexOf('wdaId=')===0){
window.wdaId = _s[i].split('=')[1];
}
}
_c = _c ? _c.split(',') : [];
for (var i = 0,_l=_c.length; i < _l; i++){
var link = document.createElement('link');
link.rel = 'stylesheet';
link.type = 'text/css';
var _uri = _d+_c[i];
link.href = _uri;
if (_uri.indexOf('reg.163.com/css2/login_index.css')>=0){
window.wdaId = 'UA1435545636633';
}
document.getElementsByTagName('head')[0].appendChild(link);
}
}


var _gaq = _gaq || [];
var _key = wdaId||'';
if (_key){
_gaq.push(['_setAccount', _key],['_setLocalGifPath', '/'+_key+'/__utm.gif'],['_setLocalServerMode']);
_gaq.push(['_addOrganic','baidu','word']);_gaq.push(['_addOrganic','soso','w']);_gaq.push(['_addOrganic','youdao','q']);
_gaq.push(['_addOrganic','sogou','query']);_gaq.push(['_addOrganic','so.360.cn','q']);
_gaq.push(['_trackPageview']);_gaq.push(['trackPageLoadTime']);
(function() {var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true; ga.src = '//urswebzj.nosdn.127.net/webzj_cdn/gaq.js';
var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);})();
}


// 全局异常日志
window.onerror=function(_msg,_url,_line,_col,_obj){
var _pd = window._$PRODUCT||'';
var _pkid = window._$PKID||'';
var _h = decodeURIComponent(location.search);
_h = _h.substring(1)||'';
_h = _h.split('&');
for(var i = 0,_temp; i < _h.length; i++){
_temp = _h[i].split('=');
if (_temp[0]=='pkid'){
_pkid = _temp[1]
}
if (_temp[0]=='product'){
_pd = _temp[1]
}
}
_msg = _msg.replace(/\^/g,'$');
_url = _url.replace(/\^/g,'$');
var _img = document.createElement('img'),
_params = 'pd='+_pd+'&pkid='+_pkid+'&msg='+encodeURIComponent(_msg||'')+'&url='+encodeURIComponent(_url||'');
var ext = [];
ext.push(window.navigator.userAgent);
var f = arguments && arguments.callee && arguments.callee.caller, c = 3;
// 只拿3层堆栈信息
if (!!arguments.callee){
while (f && (--c>0)) {
ext.push(f.toString());
if (f === f.caller) {
break;//如果有环
}
f = f.caller;
}
ext = ext.join("%%");
ext = ext.replace(/\^/g,'$');
_params += '&ext='+encodeURIComponent(ext);
}else{
_params += '&ext='+encodeURIComponent(window.navigator.userAgent);
}
var _log = '//dl.reg.163.com/pgErr?'+_params;
_log = _log.slice(0,2000);
_img.style.width = 0;
_img.style.height = 0;
setTimeout(function(){
_img.src = _log;
},0);
}
// url解析
var _u=decodeURIComponent(location.search);
var _ht=location.host;
window._$BGP=0;
if (_ht.indexOf('webzj2')>=0||_ht.indexOf('passport2')>=0||_ht.indexOf('reg2')>=0||_ht.indexOf('dl2')>=0){
window._$BGP=1;
}
window.wdaId = 0;
if(_u.indexOf('?')!=-1){
var _sl = _u.substring(1)||'';
var _s= _sl.split('&');
var _d,_c,_cssl;
for(var i= 0,_l=_s.length;i<_l;i++){
if(_s[i].indexOf('cd=')===0){
_d = _s[i].split('=')[1];
}else if(_s[i].indexOf('cf=')===0){
_cssl = _s[i].split('=');
_cssl.shift();
_c = _cssl.join('=');
}else if(_s[i].indexOf('MGID=')===0){
window.mgid = _s[i].split('=')[1];
}else if (_s[i].indexOf('wdaId=')===0){
window.wdaId = _s[i].split('=')[1];
}
}
_c = _c ? _c.split(',') : [];
for (var i = 0,_l=_c.length; i < _l; i++){
var link = document.createElement('link');
link.rel = 'stylesheet';
link.type = 'text/css';
var _uri = _d+_c[i];
link.href = _uri;
if (_uri.indexOf('reg.163.com/css2/login_index.css')>=0){
window.wdaId = 'UA1435545636633';
}
document.getElementsByTagName('head')[0].appendChild(link);
}
}


var _gaq = _gaq || [];
var _key = wdaId||'';
if (_key){
_gaq.push(['_setAccount', _key],['_setLocalGifPath', '/'+_key+'/__utm.gif'],['_setLocalServerMode']);
_gaq.push(['_addOrganic','baidu','word']);_gaq.push(['_addOrganic','soso','w']);_gaq.push(['_addOrganic','youdao','q']);
_gaq.push(['_addOrganic','sogou','query']);_gaq.push(['_addOrganic','so.360.cn','q']);
_gaq.push(['_trackPageview']);_gaq.push(['trackPageLoadTime']);
(function() {var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true; ga.src = '//urswebzj.nosdn.127.net/webzj_cdn/gaq.js';
var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);})();
}
