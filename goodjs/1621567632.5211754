function ById(id){return document.getElementById(id)};
lib={
 show:function(o){if(ById(o))ById(o).style.display=''},
 hide:function(o){if(ById(o))ById(o).style.display='none'},
 hasClass:function(el,cls){return el&&el.className?el.className.match(new RegExp('(\\s|^)'+cls+'(\\s|$)')):!1},
 addClass:function(el,cls){if(el&&!this.hasClass(el,cls))el.className+=' '+cls},
 removeClass:function(el,cls){if(el&&this.hasClass(el,cls)){el.className=lib.trim(el.className.replace(new RegExp('(\\s|^)'+cls+'(\\s|$)'),' '))}},
 event:{
  add:function(el,event,handler){if(el.addEventListener)el.addEventListener(event,handler,!1);else if(el.attachEvent)el.attachEvent('on'+event,handler)},
  remove:function(el,event,handler){if(el.removeEventListener)el.removeEventListener(event,handler,!1);else if(el.detachEvent&&handler)el.detachEvent('on'+event,handler)}
  },
 trim:function(str){return str.replace(/^\s+/,'').replace(/\s+$/,'')},
 decode:function(str){return str==null?null:decodeURI(str).replace(/\+/g,' ')},
 EndsWith:function(str,suffix){return str.indexOf(suffix,str.length-suffix.length)!=-1},
 StartsWith:function(str,start){return str.slice(0,start.length)==start},
 isStor:function(){
  info=info||{};
  if(typeof(info.isStor)!=="undefined")return info.isStor;
  if(typeof(Storage)!=="undefined"){try{localStorage.setItem('tfd','tfd');localStorage.removeItem('tfd');info.isStor=1}catch(e){info.isStor=0}}
  else{info.isStor=0};
  return info.isStor;
 },
 cookie:{
  cookieName:function(permanent,domainWide){return'c'+(permanent?1:0)+(domainWide?1:0)},
  save:function(n,v,permanent,domainWide){
   var d=new Date();d.setFullYear(d.getFullYear()+10);
   document.cookie=n+'='+v+(permanent?'; expires='+d.toUTCString():'')+(domainWide?'; domain='+info.Domain:'')+'; path=/'+(domainWide?'; SameSite=None; secure':'');
  },
  set:function(name,value,permanent,domainWide){
   var n=this.cookieName(permanent,domainWide);
   var v=this.getRaw(n),nv=value?name+'='+value:null;
   if(v){
    var d=v.split('&');
    for(var i=0;i<d.length;i++)if(lib.StartsWith(d[i],name+'=')){if(nv==null)d.splice(i,1);else d[i]=nv;break};
    if(nv!=null&&i>=d.length)d.push(nv);
    v=d.join('&');
   }else v=nv;
   this.save(n,v,permanent,domainWide);
  },
  remove:function(name,permanent,domainWide){
   var n=this.cookieName(permanent,domainWide);
   var v=this.getRaw(n);
   if(v)this.save(n,v.replace(new RegExp(name+"=[^&]*[&]?"),"").replace(/&$/,''),permanent,domainWide);
  },
  get:function(name,permanent,domainWide){
   if(arguments.length==3){
    var n=this.cookieName(permanent,domainWide);
    var v=this.getRaw(n);
    if(!v)return null;
    v=v.split('&');p=name+'=';
    for(var i=0;i<v.length;i++)if(lib.StartsWith(v[i],p))return decodeURIComponent(v[i].substring(p.length));
    return null;
   }
   else return this.get(name,0,0)||this.get(name,1,0)||this.get(name,0,1)||this.get(name,1,1);
  },
  enabled:function(){var ce=(navigator.cookieEnabled)?1:0;if(typeof navigator.cookieEnabled=="undefined"&&!ce){document.cookie="tfdtc";ce=(document.cookie.indexOf("tfdtc")!=-1)?1:0;document.cookie="tfdtc;expires=Thu, 01 Jan 1970 00:00:01 GMT;"}return ce},
  getRaw:function(name){var d=document.cookie.split('; '),p=name+'=';for(var i=0;i<d.length;i++)if(lib.StartsWith(d[i],p))return d[i].substring(p.length);return null}
  },
 flashInstalled:function(){
  if(info.IsApp&&nav.andr)return false;
  if(navigator.plugins&&navigator.mimeTypes.length){if(navigator.plugins["Shockwave Flash"])return true}
  else{try{if(new ActiveXObject("ShockwaveFlash.ShockwaveFlash"))return true}catch(e){}}
  return false;
 },
 AsyncRequest:function(url,t,callback,onerror,id){
  var scr=document.createElement('script');
  scr.type='text/javascript';
  //scr.defer=true;
  scr.async=true;
  if(id)scr.id=id;
  if(t)scr.text=t;
  scr.src=url;
  if(callback){scr.onreadystatechange=callback;scr.onload=callback}
  if(onerror){scr.onerror=onerror}
  document.getElementsByTagName('head').item(0).appendChild(scr);
 },
 delayedFunctions:window.LocalFunctions||[],
 delayedPush:function(f){
 if(window.completed)f();else this.delayedFunctions.push(f)},
 delayedExec:function(){for(var i=0;i<this.delayedFunctions.length;i++){if(i<=3)this.delayedFunctions[i]();else setTimeout('lib.delayedFunctions['+i+']()',100+i*2)}}
};
if(window.completed)lib.delayedExec();
function showPopup(evt,id,cls,popupId){
 var to=evt.target||evt.toElement;
 if(evt.preventDefault)evt.preventDefault();
 var el=ById(id);
 if(lib.hasClass(el,cls))hidePopup(el,cls);
 else{
  el.och=function(e){
   e=e||window.event;
   if(!e.target)e.target=e.srcElement;
   var currentNode=(e.changedTouches?e.changedTouches[0]:e).target;
   var popup=(typeof popupId!=="undefined")?ById(popupId):el;

   while(currentNode.parentNode){
    if(currentNode===to||currentNode===popup)return;
    if(currentNode===ById('w1'))hidePopup(el,cls);
    currentNode=currentNode.parentNode;
   }
  };
  lib.addClass(el,cls);
  var c=document.querySelector('.hpCol0');
  if(id=='w1'&&c){c=c.style;c.top='230px';var dw=window.innerWidth||document.documentElement.clientWidth;c.left=dw+'px';c.width=(dw-80)+'px';c.zIndex=99}
  else{lib.event.add(document,'click',el.och);lib.event.add(document,'touchstart',el.och)};
  if(id=='w1'&&!c){var a=ById('ac5'),b=ById('accopy');if(a&&b){b.innerHTML=a.innerHTML;b.style.margin='10px 0';b.style.textAlign='center'}}
 }
}
function hidePopup(el,cls){
 lib.removeClass(el,cls);
 lib.event.remove(document,'click',el.och);
 lib.event.remove(document,'touchstart',el.och);
 try{delete el.och}catch(e){};
 var c=document.querySelector('.hpCol0');
 if(c){c=c.style;c.top=c.left=0;c.width=c.zIndex=''};
}

var nav={
 andr:navigator.userAgent.indexOf('Android')>0?1:0,
 IE:(navigator.appName=='Microsoft Internet Explorer'||navigator.userAgent.indexOf('Trident/')>0)&&navigator.userAgent.indexOf("Opera")==-1?1:0,
 IE11:!!navigator.userAgent.match(/Trident.*rv[ :]*11\./),
 Edge:(navigator.appName=="Netscape"&&/Edge\/12./i.test(navigator.userAgent)),
 init:function(){
  nav.dw=document.body.offsetWidth;
  nav.dh=document.body.offsetHeight;
  nav.ww=window.innerWidth||document.documentElement.clientWidth;
  nav.wh=window.innerHeight||document.documentElement.clientHeight;
 },
 sw:screen.width,
 sh:screen.height,
 loc:(function(){var l=document.location,s=l.toString();return s.substr(0,s.length-l.hash.length)})(),
 ref:document.referrer
};
lib.delayedPush(nav.init);
var Sticky={
o:[],
init:function(){
 this.o=[];
 var l=document.querySelectorAll('div.sticky');
 if(l.length==0||nav.ww<760)return 0;
 this.o=[];
 for(var i=0;i<l.length;i++){
  var e=l[i];e.style.position='';
  var d={id:e.id,y:0,x:0,op:e.offsetTop};
  while(e.offsetParent){d.y+=e.offsetTop-e.scrollTop;d.x+=e.offsetLeft;e=e.offsetParent}
  this.o.push(d);
 }
 if(this.o.length){lib.event.add(window,'scroll',Sticky.scroll);lib.event.add(window,'resize',Sticky.scroll)}
},
scroll:function(){
 var p=document.querySelector('.main-holder').offsetHeight+ById('main').offsetTop;
 for(var i in Sticky.o){
  var e=ById(Sticky.o[i].id);
  if(p>(e.offsetHeight+Sticky.o[i].y+100)){
  var s=e.style;ds=document.body.scrollTop+document.documentElement.scrollTop;
  if(ds>Sticky.o[i].y){s.position="fixed";s.top=Math.min(p-ds-e.offsetHeight,0)+"px"}
  else{s.position="absolute";s.zIndex=0;s.top=Sticky.o[i].op+"px"}}
 }}
};

var acs={
a:0,
bnrs:[],
ab:function(){
 var ad=document.querySelector('.afs_ads');if(!ad||ad.innerHTML.length==0||ad.clientHeight===0)return 1;
 ad=document.querySelector('.TopBannerAd');if(!ad||ad.innerHTML.length==0||ad.clientHeight===0)return 1;
},
frframe:function(p,h,w,b){var o=ById(info.a+p),f=document.createElement('iframe'),br=document.createElement('br');o.style.height=(Number(h)+15)+'px';if(p>9)o.style.display='';f.id=info.a+'xf'+p;f.setAttribute('style','border:none;width:'+w+'px;height:'+h+'px;overflow:hidden');f.setAttribute('scrolling','no');f.setAttribute('frameborder',0);o.insertBefore(f,o.firstChild);var d=f.contentWindow.document;d.open();d.write('<!DOCTYPE html><html><head><meta charset="UTF-8"><style>body{margin:0;background-color:white;font-family:Arial,Helvetica,sans-serif;overflow:hidden}</style></head><body>'+b+'</body></html>');d.close()},
adx:function(p,m,w,h){if(acs.adZ.l&&m>(nav.sw<760?3:5)&&(acs.adZ.c==0||p>9)){acs.adZ.l=0;lib.event.add(document,'scroll',acs.adZ.scroll)};
var xid=acs.adxid[acs.adxid.length-1];for(i=acs.adxid.length-2;i>=0;i-=2){if(acs.adxid[i]>m)xid=acs.adxid[i+1]};
acs.frframe(p,h,w,'<script>google_ad_client="ca-pub-5123191624605582";google_ad_slot="'+xid+'";google_ad_width='+w+';google_ad_height='+h+';google_alternate_ad_url=location.protocol+"//'+location.host+'/_/search/nobid.html#'+p+'"</'+'script><script src="//pagead2.googlesyndication.com/pagead/show_ads.js"></'+'script>')},
adZ:{scroll:function(){
 var s=document.querySelector("#MainTxt section[data-src]:not([data-ad])");
 if(!s||acs.adZ.c>9)return;
 var r=s.getBoundingClientRect();
 if(r.bottom>nav.wh)return;
 s.setAttribute('data-ad','');
 if(s.style.display=='none')return;
 lib.event.remove(document,'scroll',acs.adZ.scroll);acs.adZ.l=1;
 var d=document.createElement('div'),m=(nav.sw<760?1:0),w=r.width>=728?728:m?320:300,h=w==728?105:w==320?50:265;
 d.id=info.a+'1'+acs.adZ.c
 d.setAttribute('style','background-color:white;margin:7px -4px -7px -4px;overflow:hidden;display:none');
 d.innerHTML='<iframe id='+info.a+'af1'+acs.adZ.c+' FRAMEBORDER=0 SCROLLING=no MARGINHEIGHT=0 MARGINWIDTH=0 TOPMARGIN=0 LEFTMARGIN=0 ALLOWTRANSPARENCY=true src="'+top.location.protocol+'//a.farlex.com/_/bnrsrv.ashx?as=none&p=1'+acs.adZ.c+'&u='+encodeURIComponent(nav.loc)+'&w='+encodeURIComponent(info.word)+'&rf='+encodeURIComponent(nav.ref)+'&atf=1&s='+(h==265?0:h==105?1:3)+'&m='+m+'&r='+nav.r+'" style="overflow:hidden;width:'+w+'px;height:'+h+'px;margin:0 auto;display:block"></iframe>';
 window.setTimeout(function(){s.appendChild(d)},1000);
 acs.adZ.c+=1;
},
c:0,l:1
},
chk:function(){
 var d=ById('Definition'),l=document.querySelectorAll('div.'+info.a);this.a=[];
 if(l.length&&d&&nav.ww<760&&!ById(info.a+'7')&&d.scrollHeight>700&&(ById('Thesaurus')||ById('Translations'))){
  var e=document.createElement('div');  
  e.className=info.a;
  e.style.textAlign='center';
  e.id=info.a+'7';
  d.appendChild(e);
  l=document.querySelectorAll('div.'+info.a);
 }; 
 for(i=0;i<l.length;i++){
  var e=l[i],c=e.firstChild,d={id:e.id.substr(e.id.length-1,1),y:0,x:0,h:e.clientHeight,w:e.clientWidth,v:(e.innerHTML==''||(c&&c.style&&(c.style.display=='none'||c.style.visibility=='hidden'))?0:1)};
  if(Number(d.id)){
   while(e.offsetParent){d.y+=e.offsetTop;d.x+=e.offsetLeft;e=e.offsetParent}
   var q=d.id+'+'+d.x+'+'+d.y+'+'+d.h+'+'+d.w;
   this.a.push(q);
  }
 }
},
abb:function(){lib.cookie.set('abu',encodeURIComponent(nav.loc),0,0);lib.AsyncRequest(abu)},
geom:function (i){
  var e=ById(info.a+i);
  if(!e) return null;
  var b=e.getBoundingClientRect();
  return ''+nav.ww+'!'+nav.wh+'!'+b.left+'!'+b.top+'!'+e.clientWidth+'!'+e.clientHeight+'!'+(document.hasFocus() ? '1' : '0');
 },
fill:function(){
 if(!window.majorse&&(this.ab()||!window.adsbygoogle||!window.showAds)&&window.abu){this.abb();return};
 var u='//w'+'ww.thefreedictionary.com/_/tr.ashx?r='+Math.random()+'&';
 var d=ById('MainTxt');if(d)u+='ch='+d.clientHeight+'&';
 if(info.isExtDomain&&(nav.IE||nav.Edge)&&lib.cookie.get('premium',1,1)){
  var prm=lib.cookie.get('premium',1,1),usId=(lib.cookie.get('userNfo',1,1)?lib.cookie.get('userNfo',1,1).split('//')[0]:'');
  u+='prm='+prm+'&usid='+usId+'&';
 }
 this.chk();
 if(this.a.length){!function(a9,a,p,s,t,A,g){if(a[a9])return;function q(c,r){a[a9]._Q.push([c, r])}a[a9]={init:function(){q("i",arguments)},fetchBids:function(){q("f",arguments)},setDisplayBids:function(){},targetingKeys:function(){return[]},_Q:[]};A=p.createElement(s);A.async=!0;A.src=t;g=p.getElementsByTagName(s)[0]; g.parentNode.insertBefore(A,g)}("apstag",window,document,"script","//c.amazon-adsystem.com/aax2/apstag.js");apstag.init({pubID:'3386'})};
 if(this.a.length==0&&lib.cookie.get('track',0,1)&&(location.host!=='forum.thefreedictionary.com'||!document.querySelector('tr.postsep'))){Sticky.init();return};
 var s=lib.cookie.get('langTo',1,0);if(s)u+='lto='+s+'&';
 for(i in nav)if(i!='init')u+=i+'='+encodeURIComponent(nav[i])+'&';
 for(i in info)u+=i+'='+encodeURIComponent(info[i])+'&';
 u+='l='+this.a.join(',');
 lib.event.add(top,'message',function(e){
   var d=e.data.toString().split(',');
   if(e.origin!=location.protocol+'//a.farlex.com')return;
   if(d[0]=='amzShow')amz.show(d[1],d[2],d[3],d[4]);
   if(d[0]=='adx')acs.adx(d[1],+d[2],d[3],d[4]);
   if(d[0]=='bnrLoad'){acs.bnrs.push(+d[1]);amz.doSend(+d[1])}
  },!1);
 if(!window.majorse)(new Image).src='//'+location.host+'/_/search/nobid.html';
 lib.AsyncRequest(u);
}};

var amz={
 bids:[],
 msgs:[],
 set:function(bids){
  amz.bids=bids;
  var b=bids.reduce(function(a,v){return(a?a+',':'')+v.amznbid+','+v.amznp},0);
  lib.AsyncRequest('//'+location.host+'/_/misc/azb.ashx?c='+b);
 },
 doSend:function(pos){
  if(amz.msgs[pos])ById(info.a+'af'+pos).contentWindow.postMessage(amz.msgs[pos],location.protocol+'//a.farlex.com');
 },
 send:function(prs){
  for(var i=0; i<amz.bids.length;i++){
   var b=amz.bids[i];
   var pos=+b.slotID.substring(2);
   if(!prs[i])continue;
   amz.msgs[pos]='amz!'+pos+'!'+prs[i]+"!"+b.amzniid+"!"+b.size;
   if(acs.bnrs.indexOf(pos)!=-1)amz.doSend(pos);
  }
 },
 show:function(p,h,w,iid){acs.frframe(p,h,w,'<script>window.parent.apstag.renderImp(document,"'+iid+'");</'+'script>')}
}
if(!info.IsApp)lib.delayedPush(function(){acs.fill()});
lib.delayedPush(function(){if(!document.location.hash&&ById('f1Word')&&nav.ww>760&&ById('f1Word').focus)ById('f1Word').focus()});

var snd={
 fill:function(d){
  var l=d||document.querySelectorAll('span.snd,span.snd2');
  var f=0,h5=0;
  var a=document.createElement('audio');
  function cp(t){return!!(a.canPlayType&&a.canPlayType('audio/'+t+';').replace(/no/,''))}
  if(cp('mpeg')||cp('mp3'))h5='mp3';else if(cp('wav'))h5='wav';
  if(h5)snd.play=function(s){a.src=s;if(nav.IE&&nav.IE11){a.autoplay=true;a.load()}else{a.load();a.play()}};
  else{
   f=lib.flashInstalled();
   if(!f){
    if(nav.IE&&navigator.platform=='Win32'){
     var a=document.createElement('bgsound');
     a.id='bgsound';
     document.lastChild.appendChild(a);
     snd.play=function(s){ById('bgsound').src=s.replace('/mp3/','/prons/').replace('.mp3','.wav')};
    }else{
     var a=document.createElement('iframe');
     a.style.display='none';
     a.id='bgsound';
     document.lastChild.appendChild(a);
     snd.play=function(s){if(snd.tm)clearTimeout(snd.tm);ById('bgsound').src=s;snd.tm=setTimeout('ById(\'bgsound\').src="about:blank"',8000)};
    }
   }
  }
  for(var i=0;i<l.length;i++){
   var e=l[i],s=e.getAttribute('data-snd'),ttl=e.getAttribute('data-ttl'),ph=e.getAttribute('data-ph'),c=e.className=='snd',h='',title='',img;
   var t=s.replace('-','/').substr(2,1)=='/'?s.substr(3,2):'';
   if(t=='UK'||t=='US')title=t;else if(t=='ES')title='España';else if(t=='BR')title='Brasil';else if(t=='41')title='Latinoamérica';else if(t=='PT')title='Portugal';else t='plain';
   if(ttl)title=ttl;
   if(c){if(s.indexOf('/')<0)s='hm/mp3/'+s;s=(info.IsApp?'http:':'')+'//img.tfd.com/'+s}
   else{
    ph=(ph?(ph=='1'?'phrase':ph):'pron');
    s=(info.IsApp?'http:':'')+'//img2.tfd.com/'+ph+'/mp3/'+s;
    img='//img.tfd.com/m/flags/18_'+t;
   };
   if(window.tfd&&tfd.playSound)h='<span title="'+title+'" class="i snd-icon-'+t+'" onclick="tfd.playSound(\''+s+'.mp3\')"></span> ';
   else if(f){var fv='"sound_src='+s+'.mp3'+(c?'':'&image_src='+img+'.jpg')+'"',sz='width="'+(c?13:28)+'" height="'+(c?21:18)+'"';h='<o'+'bject style="margin:0 0 -4px 0" title="'+title+'" classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="https://fpdownload.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,0,0" '+sz+'><param name="movie" value="https:/'+'/img.tfd.com/m/sound.swf"><param name="menu" value="false"><param name="wmode" value="transparent"><param name="FlashVars" value='+fv+'><embed style="margin:0 0 -4px 0" src="https:/'+'/img.tfd.com/m/sound.swf" FlashVars='+fv+' menu="false" '+sz+' wmode="transparent" type="application/x-shockwave-flash" pluginspage="https://get.adobe.com/flashplayer/"></object>'}
   else{s=(h5!='wav'?s+'.mp3':s.replace('/mp3/','/prons/')+'.wav');h='<span title="'+title+'" class="i snd-icon-'+t+'" onclick="snd.play(\''+s+'\')"></span> '}
   e.innerHTML=h;
  }
 },
 tm:null,
 play:function(s){
  var andr=navigator.userAgent.indexOf('Android')>0;
  if(!andr)s=s.replace('/mp3/','/prons/').replace('.mp3','.wav');
  if(snd.tm)clearTimeout(snd.tm);
  var sndfr=ById("sound_frame");
  if(IE&&navigator.platform=='Win32'){
   document.all.bgsound.src=File;
   sound_timeout=setTimeout('document.all.bgsound.src="about:blank"',8000);
  }else if(sndfr&&!andr){
   sndfr.src='about:blank';
   sndfr.src=File;
   sound_timeout=setTimeout('ById("sound_frame").src="about:blank"',8000);
  }else location=s;
 }
};
lib.delayedPush(snd.fill);


lib.delayedPush(function(){if(window.fullload)clearTimeout(fullload)});
if(!info.IsApp)lib.delayedPush(function(){
 var l=document.querySelectorAll('#MainTxt img'),c=0;
 if(l.length){for(var i=0;i<l.length;i++)if(l[i].width>200){c+=1;l[i].setAttribute('data-pin-hover',true)};
 if(c){
 var scr=document.createElement('script');
 scr.type='text/javascript';
 scr.async=true;
 scr.src='//assets.pinterest.com/js/pinit.js';
 scr.setAttribute('data-pin-hover',true);
 document.getElementsByTagName('head').item(0).appendChild(scr)}}
});

var sources=[];
lib.delayedPush(function(){
 var l;
 if(info.PageLang!='es'){
  if(l=document.querySelector('div[data-periodicals]'))l.innerHTML='<a style="margin-top:12px;float:right" rel=nofollow href="https:/'+'/www.thefreelibrary.com/_/search/Search.aspx?By=0&SearchBy='+l.getAttribute('data-periodicals')+'&q='+encodeURIComponent(info.word)+'"><b>More results ►</b></a>';
 }
 l=ById('thes_link');if(l&&ById('Thesaurus'))l.style.display='inline-block';
 l=ById('trans_link');if(l&&ById('Translations'))l.style.display='inline-block';
 if(info.tab==16)sources.push('wiki');else{
  var scs=document.querySelectorAll('#MainTxt section');
  for(var i=0;i<scs.length;i++){
   var s=scs[i].getAttribute('data-src');
   if(s)sources.push(s);
  }
 }
 var acrDD=ById('acrDD');
 if (acrDD) acrDD.onchange=function(){
  var cat=+this.options[this.selectedIndex].value;
  var tr=document.querySelectorAll('#AcrFinder TR[data-cat]');
  for(var i=0;i<tr.length;i++){
   var n=tr[i];
   n.style.display=(!cat||(Number(n.getAttribute('data-cat'))&cat)?'':'none');
  }
 }
 var lnks = document.getElementsByClassName("cpr");
 for(var i = 0; i < lnks.length; i++) {
  lnks[i].onclick = function() {
   location='/_/cite.aspx?url='+encodeURIComponent(info.canonical)+'&word='+encodeURIComponent(info.word)+'&sources='+sources;
  }
 }
});

function t_i(id,event){
 var hlp=ById('Tp'+id);
 if(!hlp)return;
 hlp.style.top=((event.clientY||event.y)-ById('main').offsetTop+document.body.scrollTop+10)+'px';
 var nsx=(event.clientX||event.x)+document.body.scrollLeft;
 hlp.style.left=(document.body.offsetWidth-nsx>510&&nsx>105?nsx-100:5)+'px';
 hlp.style.width=Math.min(500,document.body.offsetWidth-10)+'px';
 hlp.style.visibility='visible';
}
function t_o(id){var hlp=ById('Tp'+id);if(hlp)hlp.style.visibility='hidden'}

window.Langs={
'af':['Afrikaans','Afrikaans',''],
'ar':['Arabic','العربية','اختر لغة'],
'bg':['Bulgarian','Български','Изберете език'],
'ca':['Catalan','Català',''],
'zh':['Chinese Simplified','中文简体','选择一种语言'],
'tw':['Chinese Traditional','中文繁體','選擇一種語言'],
'hr':['Croatian','Hrvatski','Odaberite jezik'],
'cs':['Czech','Česky','Zvolte si jazyk'],
'da':['Danish','Dansk','Vælg et sprog'],
'nl':['Dutch','Nederlands','Selecteer een taal'],
'en':['English','','Select a language'],
'eo':['Esperanto','Esperanto',''],
'et':['Estonian','eesti keel',''],
'fa':['Farsi','فارسی',''],
'fi':['Finnish','Suomi','Valitse kieli'],
'fr':['French','Français','Sélectionnez une langue'],
'de':['German','Deutsch','Wählen Sie eine Sprache'],
'el':['Greek','Ελληνική','Για χρήστες'],
'he':['Hebrew','עִבְרִית',''],
'hi':['Hindi','हिन्दी','कोई भाषा चुनें'],
'hu':['Hungarian','magyar',''],
'is':['Icelandic','íslenska',''],
'id':['Indonesian','Indonesia',''],
'ia':['Interlingua','Interlingua',''],
'it':['Italian','Italiano','Seleziona una lingua'],
'ja':['Japanese','日本語','希望の言語を選択'],
'ko':['Korean','한국어','언어를 선택'],
'la':['Latin','Lingua Latina',''],
'lv':['Latvian','Latviešu',''],
'lt':['Lithuanian','Lietuvių',''],
'ml':['Malay','Bahasa Melayu',''],
'no':['Norwegian','Norsk','Velg et språk'],
'ps':['Pashto','پښتو,پشتو',''],
'pl':['Polish','Polski','Wybierz język'],
'pt':['Portuguese','Português','Selecione um idioma'],
'ro':['Romanian','Română','Selectaţi o limbă'],
'ru':['Russian','Русский','Выберите язык'],
'sr':['Serbian','српски',''],
'sk':['Slovak','slovenčina',''],
'sl':['Slovenian','slovenski',''],
'es':['Spanish','Español','Seleccione un idioma'],
'sw':['Swahili','Kiswahili',''],
'sv':['Swedish','Svenska','Välj ett språk'],
'th':['Thai','ภาษาไทย',''],
'tr':['Turkish','Türkçe','Bir dil seç'],
'uk':['Ukrainian','українська',''],
'ur':['Urdu','اردو',''],
'vi':['Vietnamese','Tiếng Việt','']
};

lib.delayedPush(function(){
var t=document.querySelector('#translbody[data-lang]');
if(!t)return;
var list=t.getAttribute('data-lang');
if(!list)return;
window.lngbar={
tm:null,
LangNone:'-----------------------',
LangHideUnhide:function(Node,l){
 if(Node.getAttribute&&Node.getAttribute('lang')){Node.style.display=(Node.getAttribute('lang')==l?(Node.tagName=='SECTION'?'block':'inline'):'none');return};
 var children=Node.childNodes;
 for(i in children)this.LangHideUnhide(children[i],l);
},
LangChange:function(l){
 if(l&&l.length==2)lib.cookie.set('langTo',escape(l),1,0);
 else l=(info.PageLang=='en'?'es':'en');
 var a=Langs[l];
 if(ById('LangDropdownMob')){
  var cnt=0;
  for(var li in Langs){
   var a=Langs[li];
   if(a.active){
    if(li==l){
     ById('LangDropdownMob').selectedIndex=cnt;
     break;
    }
    cnt++;
   }
  }
 }
 else{
  this.LangHide();
  if(ById('selectedLang'))ById('selectedLang').innerHTML='<div>'+(Langs[l]&&Langs[l].active?'<span class="fl_'+l+'"></span>'+a[0]+(a[1]?(l=='tw'||l=='zh'?'/':' / ')+a[1]:''):lngbar.LangNone)+'</div>';
 }
 this.LangHideUnhide(ById('translbody'),l);
 window.resizeBy(0,0);
 return false;
},
ClearTM:function(){if(lngbar.tm)clearTimeout(lngbar.tm)},
ClearTMonScroll:function(){ 
 setTimeout("lngbar.ClearTM()",200);
 if(lngbar.tm)clearTimeout(lngbar.tm);
},
LangReveal:function(){
 if(lngbar.tm)clearTimeout(lngbar.tm);
 ById('LangDropdown').style.display='';
},
LangHide:function(){
 var langDropdown=ById('LangDropdown');
 if(langDropdown)langDropdown.style.display='none';
}
};
var div=document.createElement('span'),h,cnt=0,found=0;
div.id='LangBar';
var s=lib.cookie.get('langTo',1,0);if(!s||s=="null")s=(info.PageLang=='en'?'es':'en');
for(var i=0;i<list.length;i+=2){
 var l=list.substr(i,2);
 Langs[l].active=1;
}
h='';
if(window.IsGlass){
 for(var li in Langs){
  var a=Langs[li];
  if(a.active){
   h+='<a href="#" onclick="lngbar.LangChange(\''+li+'\');return false;" class="fl_'+li+'">'+a[0]+(a[1]?' / '+a[1]:'')+'</a>&nbsp; ';
   cnt++;
  }
 }
}else{
 if(info.IsApp||info.IsMob||info.tbl||window.outerWidth<760){
  h+='<select id=LangDropdownMob onChange="var s=this.options[this.selectedIndex].value;if(s!=lib.cookie.get(\'langTo\',1,0))lngbar.LangChange(s)">';
  for(var li in Langs){
   var a=Langs[li];
   if(a.active){
    if(li==s)found=1;
    h+='<option value='+li+(li==s?' selected':'')+'>'+a[0]+(a[1]&&li!='zh'&&li!='tw'?' / '+a[1]:'')+'</option>';
    cnt++;
   }
  }
  if(!found)h+='<option selected>----------</option>';
  h+='</select>';
 }
 else{
  h+='<span id=DropDownHolder><span id=LangDropdown style="display:none" onmousemove="lngbar.ClearTM()" onscroll="lngbar.ClearTMonScroll()" onmouseout="lngbar.tm=setTimeout(\'lngbar.LangHide()\',400)">';
  for(var li in Langs){
   var a=Langs[li];
   if(a.active){
    h+='<a onclick="javascript:lngbar.LangChange(\''+li+'\');return false;" href="#"><div class="lcd"><span class="fl_'+li+'"></span>'+a[0]+(a[1]?' / '+a[1]:'')+'</div></a>';
    cnt++;
   }
  }
  h+='</span><div id=selectedLang class=lcd onmouseover="lngbar.LangReveal()" onmouseout="if(lngbar.tm)clearTimeout(lngbar.tm);lngbar.tm=setTimeout(\'lngbar.LangHide()\',800)"><div>'+lngbar.LangNone+'</div></div></span>';
 }
}
if(!info.hideLangBar)div.innerHTML=h+'<span class=label>'+Langs[info.PageLang][2]+':</span>';
var p=ById('TranslationsHead');
if(p)p.appendChild(div); else ById('translbody').insertBefore(div,ById('translbody').firstChild);
lngbar.LangChange((info.hideLangBar?'en':lib.cookie.get('langTo',1,0)));
});

if(!/bot|crawl|spider|http/i.test(navigator.userAgent))lib.delayedPush(function(){
 var ens=["Content_CA_AOD_0_BC","Content_CA_DIH_0_BC","Content_CA_TB_0_BC","Content_CA_WOD_0_BC","Content_CA_TB_0_BC","Content_CA_QOD_0_BC","Definition","Thesaurus"];
 for(var ei=0;ei<ens.length;ei++){
  var el=ById(ens[ei]);
  if(!el)continue;
  if(!document.createTreeWalker||info.IsApp||nav.ww<760){
   var d=function(){opennewdictwin(window.getSelection?window.getSelection().toString():document.getSelection())};
   if(nav.IE)d=function(){var t=document.selection.createRange();if(document.selection.type!='Text'||!t.text)return;document.selection.empty();opennewdictwin(t.text)};
   lib.event.add(el,'dblclick',d);
   continue;
  }
  var node,textNodes=[];
  var walker=document.createTreeWalker(el,NodeFilter.SHOW_TEXT,Filter,false);
  while(node=walker.nextNode())textNodes.push(node);
  for(var i=0;i<textNodes.length;i++){
   var textNode=textNodes[i];
   var text=textNode.textContent;
   if(/\S/.test(text)&&/[\u00C0-\u1FFF\u2C00-\uD7FF\w]+/.test(text)){
    var pNode=textNode.parentNode;
    var words=text.split(" ");
    for(var j=words.length-1;j>=0;j--){
     var word=words[j];
     if(word){
      var prefix="www";
      if(pNode.hasAttribute("lang"))prefix=pNode.getAttribute("lang");
      var span=CreateSpan(word,prefix);
      var next=textNode.nextSibling;
      if(lib.StartsWith(text," "))pNode.insertBefore(document.createTextNode(" "),next);
      pNode.insertBefore(span,next);
      if(j!=words.length-1||lib.EndsWith(text," "))pNode.insertBefore(document.createTextNode(" "),next);
     }
    }
    pNode.removeChild(textNode);
   }
  }
 }
 function Filter(node){
  function bad(pn){return ',A,ASIDE,H1,H2,H3,H4,SCRIPT,STYLE,'.indexOf(','+pn.tagName+',')>=0||',hw,pron,brand_copy,lcd,'.indexOf(','+pn.className+',')>=0||pn.id=="Translations"||lib.EndsWith(pn.id,"Head")||pn.style.textDecoration=="underline"};
  return(bad(node.parentNode)||bad(node.parentNode.parentNode)?NodeFilter.FILTER_REJECT:NodeFilter.FILTER_ACCEPT);
 }
 function CreateSpan(str,prefix){
  var t=document.createTextNode(str);
  if(str.length<3)return t;
  var e=document.createElement("span");
  e.className="hvr";
  e.onclick=function(e){opennewdictwin(str,prefix)}
  e.appendChild(t);
  return e;
 }
});

function opennewdictwin(text,prefix){
 if(text.slice(0,4)=='http'){window.open(text);return}
 if(text.slice(0,4)=='www.'){window.open('//'+text);return}
 prefix=prefix||'www';
 text=text.replace(/[́′!.:?,;"·\[\]\(\)]/g,'').replace(/[\n\t ]/g,' ').replace(/^\s+|\s+$/,'');
 if(!text||text.toUpperCase()==info.word.toUpperCase())return;
 var newloc;
 if(info.PageLang!='en')newloc='/'+encodeURIComponent(text);
 else newloc='/'+'/'+prefix+'.'+info.Domain+'/_/search.aspx?tab='+info.tab+'&word='+encodeURIComponent(text);
 if(document.location.toString().toLowerCase()!=newloc.toLowerCase())document.location=newloc;
}

function SelectVT(sel){
 var v=sel.options[sel.selectedIndex].value;
 if(v=="0")return;
 var i=1,tbl;
 while((tbl=ById("VerbTableN"+v.split("_")[0]+"_"+i))!=undefined){
  tbl.className="prettytable hiddenStructure";
  i++;
 }
 ById("VerbTableN"+v).className="prettytable";
}
lib.delayedPush(function(){
var l=document.querySelectorAll('#browsers .list-holder');
for(var i=0;i<l.length;i++){
 var e=l[i];
 if(e.childNodes.length!=3)continue;
 var c=e.querySelector('li.current');
 if(!c)continue;
 e.scrollTop=e.scrollHeight/2-e.clientHeight/2+c.scrollHeight/2;
}});

var searchTextfieldID="f1Word";
function ToggleKeyboard(){
 SAYT.disabled=true;
 ById(searchTextfieldID).onblur=null;
 if(!window.popKeyboard)lib.AsyncRequest('//img.tfd.com/m/keyboard.js')
 else{popKeyboard(!isKbVisible);restoreCaret()};
}

var iSavedCaretIndex=0;
function restoreCaret(){
 var tf=ById(searchTextfieldID);
 if(!tf.selectionStart)
 setCaretPos(tf,++iSavedCaretIndex,false);
}
function saveCaret(oField){
 if(nav.IE&&!oField.selectionStart){
  var Sel=document.selection.createRange();
  Sel.moveStart('character',-oField.value.length);
  iSavedCaretIndex=Sel.text.length;
 }
}
lib.delayedPush(function(){var f=document.querySelector('form.search-form');if(f){f.onsubmit=function(){return!!ById(searchTextfieldID).value}}});
function SAYTBind(fn,self,var_args){
 var ba=fn.boundArgs_||[];
 ba=ba.concat(Array.prototype.slice.call(arguments,2));
 if(typeof fn.boundSelf_!="undefined")self=fn.boundSelf_;
 if(typeof fn.foundFn_!="undefined")fn=fn.boundFn_;
 var nf=function(){
  var args=ba.concat(Array.prototype.slice.call(arguments));
  return fn.apply(self,args);
 }
 nf.boundArgs_=ba;
 nf.boundSelf_=self;
 nf.boundFn_=fn;
 return nf;
}
function SearchAhead(){
 this.disabled=!1;
 this.Tab=info.tab;
 this.HoverColor='#eeeeee';
 this.NormalBg='white';
 this.QueryURL='/'+'/www.thefreedictionary.com/_/search/suggest.ashx?jsonp=SAYT.Callback&query=';
 this.LinkURL;
 this.MIN_STRING=3;

 this.LastTF=null;
 this.SugDiv=null;
 this.SelIndex=-1;
 this.TimeID;
 this.Keys=[];
 this.Values=[];
 this.Count=[];
 this.rsp=null;
}
SearchAhead.prototype={
 Disable:function(){
  lib.cookie.set('sayt',1,1,1);
  location.reload();
 },
 OnBlur:function(event){
  if(this.disabled)return;
   if(this.LastTF&&this.LastTF.savedText!=null)setTimeout('SAYT.LastTF.value=SAYT.LastTF.savedText',800);
   this.JustHide();
 },
 Morph:function(){
  if(this.SugDiv!=null){
   this.SugDiv.style.width=(this.LastTF.offsetWidth)+"px";
   this.SugDiv.style.left=(this.GetLoc(this.LastTF,true))+"px";
   this.SugDiv.style.top=(this.GetLoc(this.LastTF,false)+this.LastTF.offsetHeight)+"px";
  }
 },
 Suggest:function(obj,event){
  if(lib.cookie.get('sayt',1,1))this.disabled=true;
  if(this.disabled)return;
  var tt=function(nm){var vv=document.querySelectorAll("input[name='"+nm+"']");for(var i=0;i<vv.length;i++){if(vv[i].checked)return vv[i].value}};
  this.LinkURL='/'+'/www.'+info.Domain+'/_/search.aspx?SearchBy='+tt("SearchBy")+'&TFDBy='+tt("TFDBy")+'&ScrBy='+tt("ScrBy")+'&Word=';
  if(event.keyCode==13){
   if(!ById(searchTextfieldID).value)return;
   var str=this.LinkURL+encodeURIComponent(this.LastTF.value)+'&tab='+this.Tab;
   window.location.href=str;
   return;
  }
  if(this.LastTF&&this.LastTF.found)clearTimeout(this.TimeID);
  this.LastTF=obj;
  this.LastTF.onblur=SAYTBind(this.OnBlur,this);
  this.Morph();

  if(event.keyCode==27){//esc
   if(this.LastTF!=null){
    if(typeof(this.LastTF.savedText)!='undefined')this.LastTF.value=this.LastTF.savedText;
    var elem=ById("SAYTk"+this.SelIndex);
    if(elem!=null)elem.style.backgroundColor=this.NormalBg;
   }
   this.Popup(null,false);
   return;
  }

  var sValue=obj.value;
  if(sValue.length<this.MIN_STRING){
   this.Popup(null,false);
   return;
  }

  if(this.SugDiv==null){
   this.SugDiv=document.createElement("DIV");
   this.SugDiv.className="sayt";
   document.body.appendChild(this.SugDiv);
   this.SugDiv.onmouseover=SAYTBind(this.Keep,this);
   this.SugDiv.onmouseout=SAYTBind(this.Hide,this);
  }

  var keyUp=event.keyCode==38;
  var keyDown=event.keyCode==40;

  if((keyUp||keyDown))this.KeyUp(keyUp);
  else{
   var sKey=this.LastTF.value;
   this.LastTF.savedText=sKey;

   for(var i=this.Keys.length-1;i>=0;i--){
    if(sKey==this.Keys[i]){
     this.SugDiv.innerHTML=this.Values[i];
     this.LastTF.elCount=this.Count[i];
     this.LastTF.found=true;
     if(event.type!="click")this.Popup(sKey,true);
     return;
    }
   }
   lib.AsyncRequest(this.QueryURL+encodeURIComponent(obj.value));
  }
 },
 Keep:function(evt){
  if(this.IsInside(evt||window.event))clearTimeout(this.TimeID);
 },
 Hide:function(evt){
  if(this.IsInside(evt||window.event))return;
  this.TimeID=setTimeout(SAYTBind(this.JustHide,this),2000);
 },
 IsInside:function(evt){
  var x=evt.clientX;
  var y=evt.clientY;

  var dx=this.GetLoc(this.SugDiv,true);
  var dy=this.GetLoc(this.SugDiv,false);

  var cornerX=dx+this.SugDiv.offsetWidth;
  var cornerY=dy+this.SugDiv.offsetHeight;

  if(x>dx&&x<cornerX&&y>dy&&y<cornerY)return true;
  return false;
 },
 JustHide:function(){
  if(this.SugDiv!=null){
   var elem=ById("SAYTk"+this.SelIndex);
   if(elem!=null)elem.style.backgroundColor=this.NormalBg;
   this.SelIndex=-1;
   this.SugDiv.style.display="none";
  }
 },
 GetLoc:function(elem,left){
  var ret=0;
  while(elem!=null){
   ret+=(left?elem.offsetLeft:elem.offsetTop);
   elem=elem.offsetParent;
  }
  return ret;
 },
 KeyUp:function(keyUp){
  if(this.LastTF.found)this.SugDiv.style.display="block";
  else return;
  var savedIndex=this.SelIndex;
  if(keyUp){
   if(this.SelIndex>0)this.SelIndex--;
   else this.Popup(null,false);
  }else{
   if(this.SelIndex==-1)this.SelIndex=0;
   else if(this.SelIndex<this.LastTF.elCount-1)this.SelIndex++;
  }
  if(savedIndex==this.SelIndex)return;
  this.UnSelectAll();
  ById("SAYTk"+this.SelIndex).style.backgroundColor=this.HoverColor;
  this.LastTF.value=this.LastTF.rsp[1][this.SelIndex][0];
 },
 UnSelectAll:function(){
  for(var i=0;i<this.LastTF.elCount;i++)
   ById("SAYTk"+i).style.backgroundColor=this.NormalBg;
 },
 Mouse:function(obj,isOver,idx){
  this.UnSelectAll();
  if(isOver){
   obj.style.backgroundColor=this.HoverColor;
   this.SelIndex=idx;
  }
 },
 Submit:function(idx){
  if(SAYT.LastTF.onblur){
   this.LastTF.onblur=null;
   location=this.LinkURL+encodeURIComponent(this.LastTF.rsp[1][idx][0])+'&tab='+this.Tab;
  }
 },
 Callback:function(rsp){
  var txt='';
  var iCount=0;
  var u=this.LinkURL;
  function link(tab,idx){return '<a href="'+u+encodeURIComponent(rsp[1][idx][0])+'&tab='+tab+'">'}
  for(var idx in rsp[1]){
   txt+='<div style="clear:both;height:18px;cursor:pointer;display:block;vertical-align:middle;padding-bottom:3px" onmousedown="SAYT.Submit('+idx+')" onmouseover="SAYT.Mouse(this,true,'+idx+')" onmouseout="SAYT.Mouse(this,false)" id="SAYTk'+idx+'">';
   txt+='<a onmousedown="SAYT.LastTF.onblur=null" style="float:left" href="'+u+encodeURIComponent(rsp[1][idx][0])+'&tab='+this.Tab+'">';
   txt+=rsp[1][idx][0]+'</a>';
   function p(n){return Math.pow(2,n)};
   var l=[['en',1919],['es',p(16)],['de',p(18)],['fr',p(17)],['it',p(19)],['pt',p(24)],['nl',p(22)],['no',p(21)],['el',p(20)],['zh',p(25)],['ru',p(23)],['ar',p(26)],['tr',p(27)],['pl',p(28)]];
   for(var i=l.length-1;i>=0;i--)if(rsp[1][idx][1]&l[i][1])txt+='<a onmousedown="SAYT.LastTF.onblur=null" style="float:right" href="'+u+encodeURIComponent(rsp[1][idx][0])+'&tab='+(rsp[1][idx][1]&l[i][1])+'" class="fl_'+l[i][0]+'" style="margin-bottom:4px"></a>';
   txt+='</div>';
   iCount++;
  }
  txt+='<a style="float:right;font-size:12px;text-decoration:underline" href="javascript'+':void()" onmousedown="SAYT.Disable()">Disable suggestions</a>';
  this.SugDiv.innerHTML=txt;
  this.LastTF.elCount=iCount;
  this.LastTF.rsp=rsp;
  this.LastTF.found=iCount>0;

  if(rsp[1].length){
   for(var ix=this.Keys.length-1;ix>=0;ix--){
    if(rsp[0]==this.Keys[ix]){
     this.Keys.push(rsp[0]);
     this.Values.push(txt);
     this.Count.push(iCount);
     break;
    }
   }
   this.Popup(rsp[0],true);
  }else this.Popup(null,false);
 },
 Popup:function(key,showElem){
  if(!showElem||(key!=this.LastTF.value)){
   this.JustHide();
   return;
  }
  this.Morph();
  this.SugDiv.style.display="block";
 }
};
lib.delayedPush(function(){window.SAYT=new SearchAhead});

function ChangeTextSize(s){
 if(info.PageLang=='ar')s+=3;
 lib.cookie.set('font',escape(s),1,1);
 document.documentElement.style.fontSize=s+'px';
 if(window.onChangeTextSize) onChangeTextSize(s);
};

function eml2(p,n){
 if(!p&&nav.loc.indexOf('medical-dictionary')>0)p='dorland';
 var url='/_/viewer'+(info.IsApp?'-app':'')+'.aspx?path='+encodeURIComponent(p)+'&name='+encodeURIComponent(n)+'&url='+encodeURIComponent(info.canonical);
 if(lib.StartsWith(nav.loc,'/_/viewer')||info.IsApp||nav.ww<760)
  location=url;
 else
  open(url,'img','');
};
function eml(p,n){eml2(p,n)};
function hil(n){eml2('hut',n)};
function hmil(n){eml2('hm',n)};
function hmil_med(n){eml2('hm/med',n)};
function hmil_wsw(n){eml2('hm/wsw',n)};
function hmil_sci(n){eml2('hm/sci',n)};

function pron_key(t){
var pkw=open('//www.thefreedictionary.com/_/pk'+(t==1?'_ipa':'')+'.htm'+(info.IsApp?'?h=1':''),'pk','width='+(t==1?'800':'630')+',height='+(t==1?'865':'710')+',statusbar=0,menubar=0');
if(window.focus)pkw.focus();
return false;
};

lib.delayedPush(function(){
window.fconn=new function(){
 var th=this;
 var evnts='';
 this.isFC=function(){return typeof fc!='undefined'};
 this.URL='//secure.thefreedictionary.com/';
 this.SURL='https://secure.thefreedictionary.com/';
 this.homepageChanged=function(){if(th.isFC())fc.sync()};
 this.ev=function(event){
  if(th.isFC())fc.regEv(event);
  else{if(evnts.length<500)evnts+=event+','}
 };
 this.pushEvts=function(FC){
  if(!evnts)return;
  var evs=evnts.split(',');
  for(var i in evs)if(evs[i])FC.regEv(evs[i]);
  evnts='';
 };
 this.evSh=function(nfo){lib.cookie.set('rff',escape(nfo),1,1);lib.AsyncRequest(th.URL+'api/regSh.ashx?d='+nfo)};
 this.userId=function(){return(info.isLogin&&lib.cookie.get('userNfo'))?lib.cookie.get('userNfo').split('/')[0]:""};
 this.shP=function(){return(info.isLogin)?"?sr="+th.userId():""};
 this.loginErr=function(){lib.hide('fcLoading');lib.show('loginErr')};
 this.loginClick=function(){
  var u=ById('fcUn').value,p=ById('fcPsw').value;
  if(!u||!p){th.loginErr()}
  else{
   if(info.isExtDomain){return true}
   var r=ById('fcRem').checked?"&rememberMe=1":"",hp2=lib.cookie.get('hp2',1,0);
   lib.AsyncRequest(th.SURL+'Login.aspx?js='+(th.isFC()?'1':'2')+'&usrName='+encodeURIComponent(u)+'&usrPwd='+encodeURIComponent(p)+'&d='+encodeURIComponent(document.domain.split('.')[0])+r+(hp2?'&hp2='+encodeURIComponent(hp2):'')+'&x='+(new Date()).getTime());
   lib.show('fcLoading');
   lib.hide('loginErr');
  }
  return false;
 };
 this.usrTicket=function(){return (info.isExtDomain&&(nav.IE||nav.Edge)?lib.cookie.get('userTicket',1,1):'')};
 this.init=function(){
  var b=+lib.cookie.get('brain',0,1);
  b+=20;if(b>60)b=60;
  lib.cookie.set('brain',escape(b),0,1);
  if(ById('regButton'))ById('regButton').className='reg-button br'+b;
  if(ById('fHP')||ById('shPg')||ById('matchUpShare')||window.requireHpJs||window.isCustomTfdHp)
   lib.AsyncRequest('//img.tfd.com/hp/hp.js'+(window._cb||''));
  else{
   if(info.isLogin&&!th.isFC())lib.AsyncRequest(th.URL+'static/js/fc.ashx'+(window._cb?window._cb+'&':'?')+'lang='+(info.PageLang||'en'));
  };
  if(!info.isLogin&&(rff=lib.cookie.get('rff',1,1)))lib.AsyncRequest(th.URL+'api/regSh.ashx?rff='+rff);
  if((x=location.search.indexOf("sr="))>=0)th.evSh('p@'+location.search.substring(x+3));
  if(!info.isLogin&&lib.cookie.get('occup',1,1)&&!lib.cookie.get('occSent',0,1)){
   lib.AsyncRequest(th.URL+'api/school/regStat.ashx');
   lib.cookie.set('occSent',1,0,1);
  }
 };
 th.init();
};

window.social={
 u:encodeURIComponent((info.canonical||nav.loc)+fconn.shP()),
 t:encodeURIComponent((function(){var t=document.querySelector('meta[property="og:title"]');if(t)return t.getAttribute('content')})()||document.title),
 s_u:encodeURIComponent(window.location.protocol+'//'+(info.PageLang=='en'?'www':info.PageLang)+'.thefreedictionary.com'),
 s_t:encodeURIComponent(hp_title),
 d:encodeURIComponent((function(){var t=document.querySelector('meta[property="og:description"]');if(t)return t.getAttribute('content')})()),
 facebook:function(s){this.open('https://www.facebook.com/sharer/sharer.php?u='+(s?this.s_u:this.u))},
 twitter:function(s){this.open('http://twitter.com/share?url='+(s?this.s_u+'&text='+this.s_t:this.u+'&text='+this.t)+'&via=farlex')}, 
 linkedin:function(){this.open('http://www.linkedin.com/shareArticle?mini=true&url='+this.s_u+'&title='+this.s_t+(this.d?'&summary'+this.d:'')+'&source=TheFreeDictionary.com')},
 email:function(){location='mailto'+':?subject='+encodeURIComponent(info.word+(info.word?' - ':'')+'TheFreeDictionary.com')+'&body='+(this.d||this.t)+'%0d%0a%0d%0aURL%3a '+this.u},
 feedback:function(){this.open('http://'+'app.thefreedictionary.com/feedback.aspx?url='+encodeURIComponent(nav.loc)+'&ref='+encodeURIComponent(nav.ref)+'&x='+info.x,info.x?600:null)},
 open:function(u,h){if(nav.ww<760||nav.d<760)location=u;else open(u,'_blank','width=600,height='+(h||400)+',resizable=1,top='+Math.max(0,screen.height/2-300)+',left='+Math.max(0,screen.width/2-200))}
};
});
if(window.safari&&window.safari.pushNotification)lib.delayedPush(function(){lib.AsyncRequest('//img.tfd.com/safariPush.js')});
if(!info.IsApp&&info.word&&nav.sw > 1000&&lib.cookie.enabled()){lib.delayedPush(function(){
 var slider,sEl;
 if((info.tab==1||info.tab==1024)&&!lib.cookie.get('hideSubscrSl',1,1))
 slider=window.subSl=new function(){
  var th=this,shown=0;
  this.closeSubscr=function(){
   lib.cookie.set('hideSubscrSl',1,1,1);
   var el=ById("SubscrSlider");
   if(el){
    el.style.visibility="hidden";
    el.style.opacity=0;
    el.style.filter="alpha(Opacity=0)";
   }
   return true;
  };
  this.get=function(){
   if(shown) return;
   var sl=document.createElement('div');
   sl.innerHTML='<div id="SubscrInner"><span id="SubscrClose" onclick="subSl.closeSubscr()"></span><h3>'+(info.tab==1?"Love words?":"Love idioms?")+'</h3><span>'+(info.tab==1?"Subscribe* to our free Word of the Day email!":"Subscribe to our free daily email with<br> Idiom of the Day!")+'</span><form name="ccoptin" id="SubscrForm" action="https://ui.constantcontact.com/d.jsp" target="_blank" method="post" style="margin-top:5px" onsubmit="subSl.closeSubscr();return true"><input id="SubscrEm" type=text name="ea" style="height:28px" placeholder="Email"><input type=hidden name="m" value="1100394066513"><input type=hidden name="p" value="oi"><input type=submit name="go" value="Go" style="height:28px"></form><div style="font-size:10px;line-height:10px">* By submitting your email address and clicking Go, you indicate that you have read and agree to the terms of our <a style="color:#ccc;text-decoration:underline" href="/privacy-policy.htm">Privacy Policy</a> and our <a href="/about.htm" style="color:#ccc;text-decoration:underline">Terms of Use</a></div></div>';
   sl.id="SubscrSlider";
   return sl;
  }
  this.go=function(){
   if(ById("VideoSubscrFrm"))lib.event.add(ById("VideoSubscrFrm"),'submit',th.closeSubscr);
   shown=1;
  }
 };
 if(slider){
  function onScroll(e){
   e=e||window.event;
   if(!e.target)e.target=e.srcElement;
   var eventDoc=e.target.ownerDocument||document,doc=eventDoc.documentElement,body=eventDoc.body;
   var docY=(doc&&doc.scrollTop||body&&body.scrollTop||0)-(doc&&doc.clientTop||body&&body.clientTop||0);
   var mt=ById("main");
   var hid=window.cmpBannerShown||!mt||!window.innerHeight||docY < mt.scrollHeight-window.innerHeight+370;
   if (sEl) {
    if(hid) sEl.style.bottom = '-180px'; else if (sEl.style.bottom) sEl.style.bottom = '0';
    return;
   } 
   if (!hid) {
    sEl=slider.get();
    if(sEl){
     document.body.appendChild(sEl);
     setTimeout(function(){
      sEl.style.bottom="0px";
      sEl.style.opacity=0.97;
      sEl.style.filter="alpha(Opacity=97)";
     },500);
     slider.go();
    }
   }
  }
  lib.event.add(document,'scroll',onScroll);
  lib.event.add(window,'resize',onScroll);
  lib.event.add(window,'cmp-ui',onScroll);
 }
})};
lib.delayedPush(function(){lib.loaded=1;if("quiz" in window&&quiz.init)quiz.init();if(window.thes)thes.init()});
(function(){if(document.addEventListener){
 var css="@font-face{font-family:'TFDfont';src: url('//img.tfd.com/font/TFDfont1.eot');src: url('//img.tfd.com/font/TFDfont1.eot#iefix') format('embedded-opentype'),url('//img.tfd.com/font/TFDfont1.woff') format('woff'),url('//img.tfd.com/font/TFDfont1.ttf') format('truetype'),url('//img.tfd.com/font/TFDfont1.svg') format('svg');font-weight: normal;font-style: normal} [class^=\"tab\"]:before{visibility:visible!important}";
 var style=document.createElement('style');
 style.type='text/css';
 if(style.styleSheet)style.styleSheet.cssText=css;else style.appendChild(document.createTextNode(css));
 document.getElementsByTagName('head').item(0).appendChild(style);
}})();
lib.delayedPush(function(){if(ById('main')){
 function sendMsg(id,gen){
  for (i=1;i<=8;i++){
   var e=ById(info.a+i);
   var ef=ById(info.a+'af'+i);
   if (e&&ef&&ef.contentWindow&&ef.src.indexOf('//a.farlex.com/')>0) 
    ef.contentWindow.postMessage('sf!'+id+'!'+i+'!'+gen(e),location.protocol+'//a.farlex.com');
  }
 }
 function updGeom(){
  sendMsg('geom', function (e){
   var b=e.getBoundingClientRect();
   return nav.ww+'!'+nav.wh+'!'+b.left+'!'+b.top+'!'+e.clientWidth+'!'+e.clientHeight;
  });
 }
 lib.event.add(window,'scroll',updGeom);lib.event.add(window,'resize',updGeom);
 lib.event.add(window,'focus',function(){sendMsg('focus', function(){return '1'})});
 lib.event.add(window,'blur',function(){sendMsg('focus', function(){return document.hasFocus()?'1':'0'})});
}});
(function(){
 var startTm=(new Date()).getTime(),rtbNfo='';
 lib.event.add(window,"unload",function(e){
  var tm=(new Date()).getTime();
  lib.cookie.set('uldUrl',location.href.split('?')[0],0,1);
  sessionStorage['uldTm']=tm;
  sessionStorage['uldDTm']=tm-startTm;
  sessionStorage['uldRTB']=rtbNfo;
 });
 setTimeout(function(){
  var url=lib.cookie.get('uldUrl',0,1);
  lib.cookie.remove('uldUrl',0,1);
  var tm=sessionStorage['uldTm'];
  var dtm=sessionStorage['uldDTm'];
  var rtb=sessionStorage['uldRTB'];
  sessionStorage['uldRTB']='';
  if(!rtb||url!=(location.href.split('?')[0])||!tm||(startTm - tm < 1000)||(startTm - tm > 120000)||dtm > 60000) return;
  lib.AsyncRequest('//secure.thefreedictionary.com/extra/logUld.ashx?dtm='+dtm+'&rtb='+encodeURIComponent(rtb));
 },500);
 lib.event.add(window,'message',function(e){
  var s=e.data.toString();
  if(s.indexOf('RTBNfo:')!==0)return;
  var v=+s.substr(7);
  if(v){if(rtbNfo)rtbNfo+=',';rtbNfo+=v}
 });
})();
setTimeout(function(){var e=document.querySelector('.icon-notif');if(e&&!lib.cookie.get('dailyfeed',0,1)){e=e.style;e.backgroundPosition='-137px 0px';e.fontSize='11px';e.textIndent='16px'}},2000);