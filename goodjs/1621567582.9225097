var Base, User, Page, App;

/*
 * Base
 */
Base = Class.create({
 _timeoutCounter: 0,
 _timeoutEvents: [],
 timeout: function(funct, duration){
  this._timeoutEvents[this._timeoutCounter] = setTimeout(funct.bind(this), duration * 1000);
  this._timeoutCounter += 1;
 },
 destroy: function(){
  this._timeoutEvents.each(function(event){
   clearTimeout(event);
  }.bind(this));
 },
 getBody: function(){
  return $$('body')[0];
 },
 css: function(text){
  this.getBody().previous().insert('<style type="text/css">'+text+'</style>');
 },
 _v: function(v){
  switch(v.toLowerCase()){
   case 'fqdn':
    return 'uploaded.to';
   break;
   case 'fqdns':
    return 'ul.to';
   break;
  }
 },
 go: function(url, add){
  if(typeof add != 'undefined')
   url = top.location.href + url;
  
  top.location.href = url;
 }
});

/*
 * User
 */
User = Class.create(Base, {
 initialize: function(data){
  this.data = data;
  this.data.contact = null;
  this.data.traffic = {hybrid:(1024*1024*1024*10),download:(1024*1024*1024*200),download_daily:(1024*1024*1024*50),download_max:(1024*1024*1024*800)};
  this.data.traffic.sum = (this.data.traffic.hybrid + this.data.traffic.download);
  this.data.space = {};
  this.data.space.membership = (1024*1024*1024*20);
  this.data.space.reward = (1024*1024*1024*5);
  this.data.space.sum = (this.data.space.membership+this.data.space.reward);
 },

 onRevLoad: function(){
  var contact = oBase._getStorage('contact');
  this.data.contact = contact;
 },
 
 get: function(key){
  if(Object.isUndefined(this.data[key]))
   return null;

  return this.data[key];
 },

 set: function(key, value){
  return this.data[key] = value;
 }
});

/*
 * Page
 */
Page = Class.create(Base, {
 _uri: '',
 initialize: function(options){
  var options = Object.extend({
   header: $('header') ? true : false,
       history: true,
       resize: true
    }, arguments[0] || { });
  
  if(options.resize)
   Event.observe(document.onresize ? document : window, 'resize', this.resize.bind(this));
  
  if(options.header)
   this.header('init');
  
  if(typeof unFocus == 'object' && options.history){
//   History.Adapter.bind(window, 'beforeunload', function(e){
//    alert("pop");
//    return false;
//   }.bind(this));
//   History.Adapter.bind(window, 'statechange', function(){
//          var State = History.getState(); // Note: We are using History.getState() instead of event.state
//   alert("State");
//          History.log(State.data, State.title, State.url);
//      });

   unFocus.History.addEventListener('historyChange', this.history.bind(this));
   this.history(unFocus.History.getCurrent());
  }
 },
 
 history: function(req){
  this._uri = req;
 },
 
 resize: function(){
  var vp = document.viewport.getDimensions();
  var so = document.viewport.getScrollOffsets();
 }
});

/*
 * App (Home/DL)
 */
App = Class.create(Page, {
 _bgOffset: 0,
 header: function(step){
  switch(step){
   case 'init':
    this._header = $('header');
    
    $('app').observe('mousemove', function(e){
     var y = Event.pointerY(e);
     var max = (document.viewport.getHeight()/2);
     var o = ((y/max)-1).abs();
     
     if(y > max) o = 0;
     this._header.select('div.left, div.right').invoke('setOpacity', o);
    }.bind(this));
   break;
  }
 },
 
 resize: function(options){
  var options = Object.extend({
       body:  $$('body')[0],
       bg:  $('senv'),
       center: $('center'),
       height: {min:500,max:700,offset:196}
    }, arguments[0] || { });
  
  var vp = document.viewport.getDimensions();
  var so = document.viewport.getScrollOffsets();
  
  if(vp.height < options.height.max){
   var bpT = ((vp.height>options.height.min)?((vp.height-(options.height.min+options.height.offset))*-1):options.height.offset);
   [options.body,options.bg].invoke('setStyle', 'background-position:center -'+(bpT-this._bgOffset)+'px');
  }
  else {
   [options.body,options.bg].invoke('setStyle', 'background-position:center '+this._bgOffset+'px');
  }
  
  if(options.center){
   if(vp.height < options.height.max && vp.height > options.height.min)
    options.center.setStyle('margin-top:'+((vp.height-(options.height.min))+this._bgOffset)+'px');
   else if(vp.height > options.height.max)
    options.center.setStyle('margin-top:'+(options.height.offset+this._bgOffset)+'px');
   else if(vp.height < options.height.min)
    options.center.setStyle('margin-top:'+(0+this._bgOffset)+'px');
  }
 }
});

/*
 * Orginal: http://adomas.org/javascript-mouse-wheel/
 * prototype extension by "Frank Monnerjahn" themonnie @gmail.com
 */
Object.extend(Event, {
 wheel:function (event){
  var delta = 0;
  if (!event) event = window.event;
  if (event.wheelDelta) {
   delta = event.wheelDelta/120;
//   if (window.opera) delta = -delta;
  } else if (event.detail) { delta = -event.detail/3;     }
  return Math.round(delta); //Safari Round
 }
});


Element.prototype.appearIE = function(data){
 if(Prototype.Browser.IE)
  this.show();
 else
  this.appear(data);
};

Element.prototype.fadeIE = function(data){
 if(Prototype.Browser.IE)
  this.hide();
 else
  this.fade(data);
};

Number.prototype.toSizeString = function(options){
 if(typeof options == 'number')
  options = {decimals:options};

 var options = Object.extend({
      decimals: 2,
      labels: ['KiB', 'MiB', 'GiB', 'TiB'] 
   }, arguments[0] || { });
 var size = this;
 
 if(size <= 1024)
  return size.number(options.decimals)+' '+options.labels[0];

 var i = -1;
 while(size > 1024){
  size = size / 1024;
  i++;
 }
 
 return size.number(options.decimals)+' '+options.labels[i];
};

Number.prototype.number = function(c, d, t){
 var n = this, c = isNaN(c = Math.abs(c)) ? 2 : c, d = d == undefined ? "," : d, t = t == undefined ? "." : t, s = n < 0 ? "-" : "", i = parseInt(n = Math.abs(+n || 0).toFixed(c)) + "", j = (j = i.length) > 3 ? j % 3 : 0;
 return s + (j ? i.substr(0, j) + t : "") + i.substr(j).replace(/(\d{3})(?=\d)/g, "$1" + t) + (c ? d + Math.abs(n - i).toFixed(c).slice(2) : "");
};

String.prototype.toURL = function(){ 
 return encodeURI(this.gsub(' ', '+'));
};

String.prototype.fromURL = function(){ 
 return decodeURI(this.gsub('+', ' '));
};

String.prototype.isMail = function(){
 var mailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
 return mailPattern.test(this)
}

String.prototype.parseDate = function(){
 var date = new Date();
 var parts = String(this).split(/[- :]/);

 date.setFullYear(parts[0]);
 date.setMonth(parts[1] - 1);
 date.setDate(parts[2]);
 date.setHours(parts[3]);
 date.setMinutes(parts[4]);
 date.setSeconds(parts[5]);
 date.setMilliseconds(0);

 return date;
}


Array.prototype.numerus = function(i){
 var n = i;
 while(typeof this[i] == 'undefined')
  i--;

 return this[i].gsub('%n', n);
};

Array.prototype.shuffle = function(){
 var tmp, rand;
 for(var i =0; i < this.length; i++){
  rand = Math.floor(Math.random() * this.length);
  tmp = this[i];
  this[i] = this[rand];
  this[rand] =tmp;
 }

 return this;
};

// Elastic (adapted from “EaseOutElastic”)
Effect.Transitions.Elastic = function(pos) {
 return -1*Math.pow(4,-8*pos) * Math.sin((pos*6-1)*(2*Math.PI)/2) + 1;
};
Effect.Transitions.BouncePast = function(pos) {
 if (pos < (1/2.75)) {
  return (7.5625*pos*pos);
 } else if (pos < (2/2.75)) {
  return 2 - (7.5625*(pos-=(1.5/2.75))*pos + .75);
 } else if (pos < (2.5/2.75)) {
  return 2 - (7.5625*(pos-=(2.25/2.75))*pos + .9375);
 } else {
  return 2 - (7.5625*(pos-=(2.625/2.75))*pos + .984375);
 }
};

/**
* @author jnf (http://github.com/jnf)
* @description Extends Scripty to include an element rotation effect. The implementation depends on browser detection
* @dependency Prototype.js 1.6.1 (http://www.prototypejs.org)
* @dependency Scriptaculous 1.8.3 (http://github.com/madrobby/scriptaculous)
* @version 0.1
*
* @todo Fix IE rotation
*/
Element.prototype.rotate = function(delta, options) {
 var browser = $H(Prototype.Browser).find(function (f) { return true == f[1] })[0];
 var element = $(this);
 if ("IE" == browser) {
  //get the current rotation
  var degree = element.degree ? element.degree * 1 : 0;
  //return the proper tween effect
  new Effect.Tween(element, degree, degree + delta, options,
   function(pos) {
    this.degree = pos;
    var radian = pos * (Math.PI / 180); //convert degree to radians
    var costheta = Math.cos(radian);
    var sintheta = Math.sin(radian);
    var style = "filter: progid:DXImageTransform.Microsoft.Matrix(SizingMethod='auto expand', "
    + "M11=" + costheta + ", M12=" + -sintheta + ", M21=" + sintheta + ", M22=" + costheta + ")";
    this.setStyle(style);
   }
  );
 } else {
  switch (browser) {
   case "Gecko": var rule = "-moz-transform"; break;
   case "WebKit": var rule = "-webkit-transform"; break;
   case "Opera": var rule = "-o-transform"; break; //supported in opera 10.5+
   default: var rule = false; break;
  }
  if(rule) {
   //get the current rotation
   var transform = element.getStyle(rule);
   var degree = transform ? transform.gsub(/[\(\)a-zA-Z:;\s]+/,'') * 1 : 0;
   //return the proper tween effect
   new Effect.Tween(element, degree, degree + delta, options,
    function(pos) {
     this.setStyle(rule + ": rotate(" + pos + "deg);");
    }
   );
  } else {
   //didn't match a browser
  }
 }
 return element;
};

Element.prototype.cloud = function(options){
 var options = Object.extend({
  duration: 2,
  divider: 3
 }, arguments[1] || { });
 
 var element = this;
 var letters = element.innerHTML.split('');
 var isTag = false;

 var duration = (options.duration / options.divider);

 element.update().show();
 
 letters.each(function(letter){
  if(letter == '<'){
   element.insert('<br />');
   return isTag = true;
  }
  if(letter == '>') return isTag = false;
  if(isTag) return;

  element.insert('<span>'+letter+'</span>');
  var delay  = (Math.random()*(options.duration*(options.divider/10)));
  element.select('span').last().setOpacity(0).appear({delay:delay,duration:duration}); //.setStyle('padding-right:0px').morph('padding-right:0px', {duration:duration,delay:delay});
 }.bind(this));
 
 return function(onComplete){
  options.duration = options.duration * .5;
  element.select('span').each(function(elem){
   var delay  = (Math.random()*(options.duration*(options.divider/10)));
   elem.fade({to:.01,delay:delay,duration:duration}); //.morph('padding-right:0px', {duration:duration,delay:delay})
  }.bind(this));

  setTimeout(function(){
   if(Object.isFunction(onComplete))
    onComplete();
  }.bind(this), options.duration * 1000);
 }.bind(this);
};

function generate(len) {
 var pwd = '';
 var con = new Array('b','c','d','f','g','h','j','k','l','m','n','p','r','s','t','v','w','x','y','z');
 var voc = new Array('a','e','i','o','u');

 for(i=0; i < len/2; i++)
 {
  var c = Math.ceil(Math.random() * 1000) % 20;
  var v = Math.ceil(Math.random() * 1000) % 5;
  pwd += con[c] + voc[v];
 }

 return pwd;
}