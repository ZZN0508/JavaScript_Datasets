var _CLIENTTIMEOUTERROR = "Problem loading data.";
function tog(o, v) { if (ById(o)) ById(o).style.display = v ? '' : 'none'; return v }
function togg(o) {if (ById(o)) {var b = ById(o).style.display; ById(o).style.display = b ? '' : 'none'; return b}}
function setHtml(o, v) { if (ById(o)) ById(o).innerHTML = v }
function forAll(x, f) { var d = document.querySelectorAll(x); for (var i = 0; i < d.length; i++) f(d[i]) }
function fixArrIE8(a) {
 if (!a.indexOf) {
  a.indexOf = function(obj, start) {
   for (var i = (start || 0), j = this.length; i < j; i++) { if (this[i] === obj) { return i; }}
   return -1;
     }
 }
 if (!a.map) {
  a.map = function (callback, thisArg) {
   var T, A, k;
   var O = Object(this);
   var len = O.length >>> 0;
   if (arguments.length > 1) T = thisArg;
   A = new Array(len);
   k = 0;
   while (k < len) {
    var kValue, mappedValue;
    if (k in O) {
     kValue = O[k];
     mappedValue = callback.call(T, kValue, k, O);
     A[k] = mappedValue;
    }
    k++;
   }
   return A;
  };
 }
 if (!a.filter) {
  a.filter = function (fun) {
   var t = Object(this);
   var len = t.length >>> 0;
   var res = [];
   var thisp = arguments[1];
   for (var i = 0; i < len; i++) {
    if (i in t) {
     var val = t[i];
     if (fun.call(thisp, val, i, t))
      res.push(val);
    }
   }
   return res;
  };
 }
 if (!a.reduce) {
  a.reduce = function (cb, iv) {
   if (typeof cb != "function") throw new TypeError(cb + ' is not a function');
   var t = Object(this);
   var len = t.length >>> 0;
   if (len === 0 && arguments.length < 2) throw new TypeError('Reduce of empty array with no initial value');
   if (len === 1 && arguments.length < 2) return t[0];
   if (len === 0 && arguments.length > 1) return iv;

   var i = arguments.length > 1 ? 0 : 1;
   var pv = arguments.length > 1 ? iv : t[0];
   for (; i < len; i++) {
    pv = cb(pv, t[i], i, t);
   }

   return pv;
  };
 }
 return a;
}
if (typeof String.prototype.trim !== 'function') {
 String.prototype.trim = function () { return this.replace(/^\s+|\s+$/g, '') }
}
function setLocation(loc) { ById('txtLoc').value = loc; __doPostBack('', '') }
function ByQuery(el, q) { return el.querySelector(q); }
if (ById('fHP'))
var dragEvent = new function () {
 var th = this;
 this.columns = [];
 for (var i = 0; i <= 2; i++) {
  var c = ById('Content_CA_Column' + i);
  this.columns.push(c);
  c.appendChild(document.createElement("div"));
 }
 this.blocks = [];
 this.headers = [];
 this.DC = null;
 function getBrowserEvent(e) {
  var evt = new Object();
  if (navigator.userAgent.indexOf('MSIE') >= 0) { evt.target = event.srcElement; evt.event = event }
  else { evt.target = e.target; evt.event = e }
  return evt;
 }
 function init(e) {
  var evt = getBrowserEvent(e);
  th.target = evt.target;
  th.event = evt.event;
 };
 function saveConfig() {
  if (!th.control.Dragged) return;
  var strdata = "";
  var colIndex = 0;
  for (var i in th.columns) {
   var col = th.columns[i];
   var rowIndex = 0;
   if (col != null)
    for (var j = 0; j < col.childNodes.length; j++) {
     var el = col.childNodes[j];
     if (th.control.isSupported(el)) {
      var acid = el.getAttribute("ACID")
      strdata += acid + "=" + colIndex.toString() + rowIndex.toString() + ";";
      rowIndex++;
     }
    }
   colIndex++;
  }
  ById("Content_CA_dataTransfer").src=location.protocol+"//"+location.host+"/_/hp/UpdateClientConfiguration.aspx?data=" + strdata;
 }
 this.getDragContainer = function () {
  if (!th.DC) th.DC = ById("DragContainer");
  return th.DC;
 };
 this.start = function (e) {
  init(e);
  this.oldMouseMove = document.onmousemove;
  this.oldMouseUp = document.onmouseup;
  this.control = new DragControl(this);
  this.control.PrepareDrag();
  document.onmousemove = function (e) { return th.move(e) }
  document.onmouseup = function (e) { return th.end(e) }
  return false;
 };
 this.move = function (e) {
  init(e);
  this.control.Drag();
  if (document.selection) document.selection.empty();
  return false;
 };
 this.end = function (e) {
  document.onmousemove = this.oldMouseMove;
  document.onmouseup = this.oldMouseUp;
  this.control.EndDrag();
  saveConfig();
  this.control = null;
  this.event = null;
  this.target = null;
  if (document.selection) document.selection.empty();
  return false;
 }
 var hh = document.querySelectorAll('.trH');
 for (var i = 0; i < hh.length; i++) {
  this.headers.push(hh[i].id)
  var dc_id = hh[i].getAttribute('DC');
  this.blocks[dc_id] = ById(dc_id);
  hh[i].style.cursor = "move";
  hh[i].onmousedown = function (e) {
   e = e || window.event;
   var t = (e.target || e.srcElement).nodeName;
   if (t == 'A' || t == 'SPAN' || t == "path" || t == "svg") return false;
   return th.start(e)
  };
 }
}
function DragPoint(col, row) {
 this.Col = col;
 this.Row = row;
}
function DragControl(e) {
 this.dragEvent = e;
 this.mc = null;
 this.origNext = null;
 this.dragContainer = e.getDragContainer();
 this.dx = 0;
 this.dy = 0;
 this.mcPos = null;
}
DragControl.prototype = {
 "getOffset": function(a, b) {
  var c = a.getBoundingClientRect();
  var m = document.querySelector('.main-holder').getBoundingClientRect();
  return b ? c.left - m.left : c.top - m.top;
 },
 "getCoordinates": function (obj) {
  var x = 0;
  for (var i = 0; i < this.dragEvent.columns.length; i++) {
   var col = this.dragEvent.columns[i];
   var y = 0;
   for (var j = 0; j < col.childNodes.length; j++) {
    var el = col.childNodes[j];
    if (el == obj) return new DragPoint(x, y);
    if (this.isSupported(el)) y++;
   }
   x++;
  }
  return null;
 },
 "PrepareDrag": function () {
  var obj = this.dragEvent.target;
  var e = this.dragEvent.event;
  this.mc = this.getContainer(obj);
  this.origNext = this.mc.nextSibling;
  this.mcPos = this.getCoordinates(this.mc);
  var dc = this.dragContainer
  this.dx = e.clientX - this.getOffset(this.mc, true);
  this.dy = e.clientY - this.getOffset(this.mc, false);
  dc.innerHTML = this.mc.innerHTML;
  dc.className = this.mc.className;
  dc.backgroundColor = this.mc.backgroundColor
  var cc = e.clientX;
  dc.style.left = this.getOffset(this.mc, true) + "px";
  dc.style.top = this.getOffset(this.mc, false) + "px";
  dc.style.height = this.mc.offsetHeight + "px";
  dc.style.width = this.mc.offsetWidth + "px";
  if (navigator.platform == "Win32" || navigator.userAgent.indexOf('Gecko') >= 0) {
   dc.style.filter = "alpha(Opacity=75)"
   dc.style.opacity = 0.75;
  }

 },
 "Drag": function () {
  var obj = this.dragEvent.target;
  var e = this.dragEvent.event;
  var dc = this.dragContainer;
  dc.style.left = e.clientX - this.dx + "px";
  dc.style.top = e.clientY - this.dy + "px";
  this.DragOver();
 },
 "DragOver": function () {
  var dc = this.dragContainer;
  var e = this.dragEvent.event;
  var mode;
  var neighbour;
  var colparent;
  if (e.clientX == this.cacheX && e.clientY == this.cacheY)
   return;
  else {
   this.cacheX = e.clientX;
   this.cacheY = e.clientY;
  }
  var canAppend = false;
  var l1 = dc.offsetLeft;
  var t1 = dc.offsetTop;
  var l2 = this.getOffset(dc, true);
  var t2 = this.getOffset(dc, false);
  var minx = 1000000;
  var miny = 1000000;
  var bottom = 0;
  var nearestCol = null;
  var nearestColIndex = -1;
  for (var i in this.dragEvent.columns) {
   var col = this.dragEvent.columns[i];
   if (col != null) {
    var xx = l1 - this.getOffset(col, true);
    if (xx < 0) xx = -xx;
    if (xx < minx) {
     minx = xx;
     miny = this.getOffset(col, false);
     if (miny < 0) miny = -miny;
     nearestCol = col;
     nearestColIndex = i;
    } else if (xx == minx) {
     var top = this.getOffset(col, false);
     if (top < 0) top = -top;
     if (t1 > top && t1 < top + col.clientHeight) {
      miny = top;
      nearestCol = col;
      nearestColIndex = i;
     }
    }
   }
  }
  miny = 1000000;
  if (nearestCol != null) {
   for (var j = 0; j < nearestCol.childNodes.length; j++) {
    var el = nearestCol.childNodes[j];
    if (el.nodeName != 'DIV') continue;
    var yy = t1 - this.getOffset(el, false);
    if (yy < 0) yy = -yy;
    if (yy < miny) {
     miny = yy;
     neighbour = el;
    }
   }
  }

  if (!this.isAllowedToDropTo(this.mc.getAttribute('acid').split('|')[0], nearestColIndex)) {
   return;
  }
  if (neighbour != null && (this.mc.nextSibling != neighbour && this.mc != neighbour))
   neighbour.parentNode.insertBefore(this.mc, neighbour);
 },
 "Reset": function(){
  this.origNext.parentNode.insertBefore(this.mc, this.origNext);
 },
 "Contains": function (parent, child) {
  var i = 0;
  for (i = 0; i < parent.childNodes.length; i++)
   if (parent.childNodes[i] == child)
    return true;
  return false;
 },
 "EndDrag": function () {
  var mcPos = this.getCoordinates(this.mc);
  this.Dragged = false;
  if (this.mcPos != null && mcPos != null)
   this.Dragged = this.mcPos.Col != mcPos.Col || this.mcPos.Row != mcPos.Row;
  if (!this.isAllowedToDropTo(this.mc.getAttribute('acid').split('|')[0], mcPos.Col)) {
   this.Dragged = false;
   this.Reset();
  }
  this.mc = null;
  this.origNext = null;
  this.dragContainer.innerHTML = "";
  this.dragContainer.style.height = 0 + "px";
  this.dragContainer.style.width = 0 + "px";
 },
 "isAllowedToDropTo": function (id, col) {
  return col != 2 || ["WI", "ST", "WT", "WTHR", "RS", "DI", "LS"].indexOf(id) >= 0;
 },
 "getContainer": function (obj) {
  var t = obj;
  do {
   if (t.getAttribute('acid')) return t;
   t = t.parentNode;
  }
  while (t.parentNode);
  return null;
 },
 "isSupported": function (obj) {
  return obj.nodeName == 'DIV' && obj.getAttribute('acid');
 }
}
if (ById('fHP'))
var contentMenu = new function () {
 function saveMenuState(catId, v) { if (v) localStorage["menuState"] |= 1 << catId; else localStorage["menuState"] &= 0xFFFF ^ (1 << catId)}
 function loadMenu(m) {if ((dt = m.getAttribute('data-needtoload')) && !m.getAttribute('data-loaded')) ById('Content_CA_dataTransfer').src = location.protocol+"//"+location.host+'/_/hp/Controls/AsyncMenu.aspx?CID=' + m.id + '&Menu=' + dt}
 this.addCustomRSS = function () {
  ById('hdCustomRSS').value = "1";
  ById('fHP').submit();
  }
 this.tog = function (cid, catId, needToLoad) {
  var ch = cid + '_dvChild';
  var v = togg(ch);
  var t = ById(cid + '_dvGroupTitle');
  saveMenuState(catId + 1, v);
  if (v) lib.addClass(t, 'open'); else lib.removeClass(t, 'open');
  loadMenu(ById(ch));
 };
 forAll('[data-addblock]', function (d) {
  d.onclick = function () {
   ById('hnb').value = d.getAttribute("data-addblock");
   ById('fHP').submit();
   return false;
  }
 });
 ById('addContent').onclick = function () {
  var v = togg('addContentBlock');
  if (v) setHtml('addContentPlus', '&ndash;'); else setHtml('addContentPlus', '+');
  saveMenuState(0, v);
 }
 if ((m = document.querySelector('[data-needtoload]')) && !m.style.display) loadMenu(m);
}
if (ById('fHP'))
var hp = new function () {
 var th = this;
 this.failAfter = function (ctrl, sec) {setTimeout(function() { if(ctrl && ctrl.getAttribute("data-loaded")!='1') ctrl.innerHTML=_CLIENTTIMEOUTERROR}, sec*1000)};
 this.selBackground = function(th, id, col) {
  ById(id).value = col;
  for (var i in th.parentNode.childNodes) {
   var n = th.parentNode.childNodes[i];
   if (n.style) n.style.border = (n==th ? 'solid 2px black' : '');
  }
 };
 function toggleSettings(r) {
  var cont = ById(r + 'trDz');
  var ae = ById(r + 'ae');
  if (togg(r + 'trPz')) {
   ae.firstChild.className = "i close";
   cont.style.opacity = 0.4;
  } else {
   ae.firstChild.className = "i edit";
   cont.style.opacity = 1;
  }
 }
 forAll('.settings', function (d) {
  d.onclick = function () {
   toggleSettings(d.id.substr(0, d.id.length - 2));
   return false;
  }
 });
 this.openSettings = function (d) {
  while (d&&!d.getAttribute('acid')) d = d.parentNode;
  toggleSettings(d.id.substr(0, d.id.length - 2));
 }
 if (ById('hpWeather')) {
  setHtml('hpWeather', '<div style="display:none"><iframe src="'+location.protocol+'//'+location.host+'/_/hp/Controls/AsyncWeatherControl.aspx?' + ById('hpWeather').getAttribute('data-pars') + '" id="wrifrm" class="ifrm" style="display:' + (navigator.userAgent && navigator.userAgent.indexOf('Gecko') > 0 ? 'inline' : 'none') + '"></iframe></div>');
 }
 if (ById('hpHoroscope')) {
  var d = new Date();
  setHtml('hpHoroscope', '<div style="display:none"><iframe src="'+location.protocol+'//'+location.host+'/_/hp/Controls/AsyncHoroscopeControl.aspx?birthday=' + ById('hpHoroscope').getAttribute('data-birthday') + '&date=' + d.getDate() + '-' + (d.getMonth()+1) + '-' + d.getFullYear() + '" id="wrifrm" class="ifrm" style="display:' + (navigator.userAgent && navigator.userAgent.indexOf('Gecko') > 0 ? 'inline' : 'none') + '"></iframe></div>');
 }
 forAll('div.bgCells', function (d) {
  var id = d.getAttribute('data-inp');
  var cFact = ['White', '#F8F8F8', '#F0F0F0', '#FEF2F2', '#FFF6F1', '#FFFBF1', '#FEFFF1', '#F9FFF1', '#F4FFF1', '#F1FFF3', '#F1FFF8', '#F1FFFD', '#F1FDFF', '#F1F8FF', '#F1F3FF', '#F4F1FF', '#F9F1FF'];
  var cDisp = ['White', '#E4E4E4', '#C8C8C8', '#FECACA', '#FFDCC9', '#FFEFC9', '#FBFFC9', '#E8FFC9', '#D4FFC9', '#C9FFD1', '#C9FFE4', '#C9FFF7', '#C9F7FF', '#C9E4FF', '#C9D1FF', '#D4C9FF', '#E7C9FF'];
  var s = '';
  for (var j in cFact) s += '<span style="' + (ById(id).value == cFact[j] ? 'border:solid 2px black;' : '') + 'background:' + cDisp[j] + '" onclick="hp.selBackground(this, \'' + id + '\', \'' + cFact[j] + '\')"></span>';
  d.innerHTML = s;
 });
 forAll('[data-timeout]', function (d) {
  th.failAfter(d, d.getAttribute("data-timeout"));
 });
};
function toggleCode(r) {
 var content = ById('ctrContent_' + r);
 var gcb = ById('gc_' + r);
 if (togg('ctrCode_' + r)) {
  gcb.innerHTML = '<span>OK</span>';
  if (gcb.title) {gcb.setAttribute('data-title',gcb.title);gcb.title = ''}
  content.style.opacity = 0.4;
 } else {
  gcb.innerHTML = '<span>&lt;</span><span class="chCodeSlash">/</span><span>&gt;</span>';
  gcb.title = gcb.getAttribute('data-title');
  content.style.opacity = 1;
 }
}
forAll('.chbGetCode', function(d) {
 d.onclick = function() {
  toggleCode(d.id.replace('gc_', ''));
  return false;
 };
});
var diacriticsRemover = new function() {
 var map;
 function init() {
  if (map) return;
  var dd = [
   {b:'a',l:'\u0061\u24D0\uFF41\u1E9A\u00E0\u00E1\u00E2\u1EA7\u1EA5\u1EAB\u1EA9\u00E3\u0101\u0103\u1EB1\u1EAF\u1EB5\u1EB3\u0227\u01E1\u00E4\u01DF\u1EA3\u00E5\u01FB\u01CE\u0201\u0203\u1EA1\u1EAD\u1EB7\u1E01\u0105\u2C65\u0250'},
   {b:'b',l:'\u0062\u24D1\uFF42\u1E03\u1E05\u1E07\u0180\u0183\u0253'},
   {b:'c',l:'\u0063\u24D2\uFF43\u0107\u0109\u010B\u010D\u00E7\u1E09\u0188\u023C\uA73F\u2184'},
   {b:'d',l:'\u0064\u24D3\uFF44\u1E0B\u010F\u1E0D\u1E11\u1E13\u1E0F\u0111\u018C\u0256\u0257\uA77A'},
   {b:'e',l:'\u0065\u24D4\uFF45\u00E8\u00E9\u00EA\u1EC1\u1EBF\u1EC5\u1EC3\u1EBD\u0113\u1E15\u1E17\u0115\u0117\u00EB\u1EBB\u011B\u0205\u0207\u1EB9\u1EC7\u0229\u1E1D\u0119\u1E19\u1E1B\u0247\u025B\u01DD'},
   {b:'f',l:'\u0066\u24D5\uFF46\u1E1F\u0192\uA77C'},
   {b:'g',l:'\u0067\u24D6\uFF47\u01F5\u011D\u1E21\u011F\u0121\u01E7\u0123\u01E5\u0260\uA7A1\u1D79\uA77F'},
   {b:'h',l:'\u0068\u24D7\uFF48\u0125\u1E23\u1E27\u021F\u1E25\u1E29\u1E2B\u1E96\u0127\u2C68\u2C76\u0265'},
   {b:'hv',l:'\u0195'},
   {b:'i',l:'\u0069\u24D8\uFF49\u00EC\u00ED\u00EE\u0129\u012B\u012D\u00EF\u1E2F\u1EC9\u01D0\u0209\u020B\u1ECB\u012F\u1E2D\u0268\u0131'},
   {b:'j',l:'\u006A\u24D9\uFF4A\u0135\u01F0\u0249'},
   {b:'k',l:'\u006B\u24DA\uFF4B\u1E31\u01E9\u1E33\u0137\u1E35\u0199\u2C6A\uA741\uA743\uA745\uA7A3'},
   {b:'l',l:'\u006C\u24DB\uFF4C\u0140\u013A\u013E\u1E37\u1E39\u013C\u1E3D\u1E3B\u017F\u0142\u019A\u026B\u2C61\uA749\uA781\uA747'},
   {b:'m',l:'\u006D\u24DC\uFF4D\u1E3F\u1E41\u1E43\u0271\u026F'},
   {b:'n',l:'\u006E\u24DD\uFF4E\u01F9\u0144\u00F1\u1E45\u0148\u1E47\u0146\u1E4B\u1E49\u019E\u0272\u0149\uA791\uA7A5'},
   {b:'o',l:'\u006F\u24DE\uFF4F\u00F2\u00F3\u00F4\u1ED3\u1ED1\u1ED7\u1ED5\u00F5\u1E4D\u022D\u1E4F\u014D\u1E51\u1E53\u014F\u022F\u0231\u00F6\u022B\u1ECF\u0151\u01D2\u020D\u020F\u01A1\u1EDD\u1EDB\u1EE1\u1EDF\u1EE3\u1ECD\u1ED9\u01EB\u01ED\u00F8\u01FF\u0254\uA74B\uA74D\u0275'},
   {b:'p',l:'\u0070\u24DF\uFF50\u1E55\u1E57\u01A5\u1D7D\uA751\uA753\uA755'},
   {b:'q',l:'\u0071\u24E0\uFF51\u024B\uA757\uA759'},
   {b:'r',l:'\u0072\u24E1\uFF52\u0155\u1E59\u0159\u0211\u0213\u1E5B\u1E5D\u0157\u1E5F\u024D\u027D\uA75B\uA7A7\uA783'},
   {b:'s',l:'\u0073\u24E2\uFF53\u00DF\u015B\u1E65\u015D\u1E61\u0161\u1E67\u1E63\u1E69\u0219\u015F\u023F\uA7A9\uA785\u1E9B'},
   {b:'t',l:'\u0074\u24E3\uFF54\u1E6B\u1E97\u0165\u1E6D\u021B\u0163\u1E71\u1E6F\u0167\u01AD\u0288\u2C66\uA787'},
   {b:'u',l:'\u0075\u24E4\uFF55\u00F9\u00FA\u00FB\u0169\u1E79\u016B\u1E7B\u016D\u00FC\u01DC\u01D8\u01D6\u01DA\u1EE7\u016F\u0171\u01D4\u0215\u0217\u01B0\u1EEB\u1EE9\u1EEF\u1EED\u1EF1\u1EE5\u1E73\u0173\u1E77\u1E75\u0289'},
   {b:'v',l:'\u0076\u24E5\uFF56\u1E7D\u1E7F\u028B\uA75F\u028C'},
   {b:'w',l:'\u0077\u24E6\uFF57\u1E81\u1E83\u0175\u1E87\u1E85\u1E98\u1E89\u2C73'},
   {b:'x',l:'\u0078\u24E7\uFF58\u1E8B\u1E8D'},
   {b:'y',l:'\u0079\u24E8\uFF59\u1EF3\u00FD\u0177\u1EF9\u0233\u1E8F\u00FF\u1EF7\u1E99\u1EF5\u01B4\u024F\u1EFF'},
   {b:'z',l:'\u007A\u24E9\uFF5A\u017A\u1E91\u017C\u017E\u1E93\u1E95\u01B6\u0225\u0240\u2C6C\uA763'}
  ];
  map = {};
  for (var i = 0; i < dd.length; i++) {
   var letters = dd[i].l.split("");
   for (var j = 0; j < letters.length ; j++)
    map[letters[j]] = dd[i].b;
  }
 }
 this.remove = function(str) {
  init();
  return str.toLocaleLowerCase().replace(/[^\u0000-\u007E]/g, function (a) {
   return map[a] || a;
  });
 }
}
var hangman = new function () {
 this.guess = '';
 var th = this;
 var cnt = 0;
 var word, shKey, tr, wordND;
 var h = ById('hangman');
 var retFocus;
 if (!h) return;
 if ((t = h.getAttribute('data-tr'))) tr = JSON.parse(t); else tr = {lost: "Sorry, you lost. See if your friends can solve it!", won: "You won in {0} guesses. See if your friends can beat you!", shWon: "I beat Hangman in {0} guesses! Can you beat me?", shLost: "I couldn't figure out this word in Hangman. Can you?"};
 this.newGame = function (f) {
  lib.show('hmWait');
  word = '';
  wordND = '';
  shKey = '';
  retFocus = f;
  lib.AsyncRequest('/_/game/hangman.ashx?lang=' + info.PageLang + '&r=' + Math.random());
 }
 this.update = function() {
  var input = ById('tfd_hm_input');
  if (input.disabled) return;
  var c='', sc='';
  for (var i = 0; i < input.value.length; i++) {
   sc = input.value.substr(i, 1);
   c = diacriticsRemover.remove(sc).toLocaleUpperCase();
   if (sc.length!=c.length) c=sc;
   if (/[0-9,\.;\- =`\/\[\]#\!\?\$_\*\)\(\\\|\>\<@%\^&\+\~\{\}\:\"\']/.test(c)) continue;
   if (th.guess.indexOf(c) < 0) {
    th.guess += c;
    if (wordND.indexOf(c) < 0) ById('hm_wrong').innerHTML += c;
    break;
   }
  }
  input.value = c;
  for (var i = 0; i < ById('hm_wrong').innerHTML.length; i++)
   ById('tfd_hm_td' + i).style.backgroundColor = 'transparent';
  ById('hm_word').innerHTML = '';
  var gamelost = ById('tfd_hm_td9').style.backgroundColor == 'transparent';
  for (var i = 0; i < word.length; i++)
   ById('hm_word').innerHTML += (th.guess.indexOf(wordND.substr(i, 1)) >= 0 || gamelost ? word.substr(i, 1) : '_');
  if (ById('hm_word').innerHTML.indexOf('_') < 0) {
   if (gamelost) {
    goal.reset('gh');
    ById('tfd_hm_span').style.backgroundPosition = '0 -220px';
    ById('hm_result').innerHTML = tr.lost + tfdShare.getBtns('h' + shKey + '0', tr.shLost);
   } else {
    ById('tfd_hm_span').style.backgroundPosition = '0 0';
    for (var i = 0; i <= 9; i++)
     ById('tfd_hm_td' + i).style.backgroundColor = 'transparent';
    var l = ById('hm_wrong').innerHTML.length; for (var i = 0, x = ''; i < wordND.length; i++) { if (x.indexOf(wordND.charAt(i)) < 0) x += wordND.charAt(i) }
    if (!info.isLogin) {
     ById('hm_result').innerHTML = tfdShare.getBadgeHTML('gh');
     if (tfdShare.isBadge) lib.hide('hmWr')
    } else if (gg = goal.getMsg('gh')) {
     ById('hm_result').innerHTML = gg;
    } else
     ById('hm_result').innerHTML = tr.won.replace("{0}", (l + x.length)) + tfdShare.getBtns('h' + shKey + String.fromCharCode(65 + l), tr.shWon.replace("{0}", (l + x.length)));
    fconn.ev('gh');
   }
   input.disabled = true;
   ById('tfd_hm_a').style.visibility = '';
   if (window.sessionStorage) sessionStorage.hmPlayed = 1;
   setTimeout(function(){ById('tfd_hm_new_game').focus()},50);
  }
  if (c != '' && typeof (regShare) == "function") regShare('gh');
 };
 this.init = function (c) {
  if (!c && ById('tfd_hm_input').disabled) return;
  ById('tfd_hm_span').style.backgroundPosition = '0 -110px';
  var cont = ById('Content_CA_HM_0_BC');
  var bgcolor = cont != null ? cont.style.backgroundColor : null;
  if (!bgcolor) bgcolor = 'white';
  if (c || cnt == 1)
   for (var i = 0; i <= 9; i++)
    ById('tfd_hm_td' + i).style.backgroundColor = bgcolor;

  cnt += 1;
  lib.show('hmWr');
 };
 this.refresh = function () {
  lib.hide('hmWait');
  ById('hangman').style.visibility = 'visible';
  if (ById('hmShare')) ById('hmShare').innerHTML = '';
  th.guess = '';
  ById('tfd_hm_a').style.visibility = 'hidden';
  if (cnt) th.init(1);
  cnt++;
  var input = ById('tfd_hm_input');
  input.disabled = false;
  if (retFocus) {
   setTimeout(function(){input.focus()},50);
   retFocus = 0;
  }
  setHtml('hm_result', '');
  input.value = '';
  setHtml('hm_wrong', '');
  th.update();
 };
 this.learn = function () { top.location = '/' + encodeURIComponent(word.toLocaleLowerCase()) };
 function setWord(w) {
  word = w;
  wordND = diacriticsRemover.remove(w).toLocaleUpperCase();
 }
 this.callback = function (w, k) {
  setWord(w);
  shKey = k;
  th.refresh();
 };
 if (!window.sessionStorage || !sessionStorage.hmPlayed) {
  setWord(h.getAttribute('data-word'));
  shKey = h.getAttribute('data-key');
  th.refresh();
 } else th.newGame();
}
var bee = new function () {
 var word, lev = 2, shKey;
 var th = this;
 var b = ById('TfdBee');
 if (!b) return;
 this.newGame = function () {
  setHtml('beeShare','');
  lib.hide('tfd_bee_nt');
  setHtml('tfd_bee_answ', '');
  lib.show('beeAnsBtn');
  ById('tfd_bee_uword').style.backgroundColor = '';
  ById('tfd_bee_uword').value = '';
  lib.AsyncRequest("/_/game/bee.ashx?l=" + lev + '&r=' + Math.random());
 };
 this.level = function (l) {
  if (l.value == lev) return;
  lev = +l.value;
  th.newGame();
 };
 this.answer = function () {
  lib.show('beeNewWord');
  lib.show('beeNew');
  var a = ById('tfd_bee_uword'), LEV = ["Easy", "Hard", "Expert"];
  if (a.value.trim().toLowerCase() == word.toLowerCase()) {
   setHtml('tfd_bee_answ', '<a class=u href="/' + encodeURIComponent(word) + '">Learn the word</a>');
   ById('tfd_bee_nt').style.color = '#27937d';
   if (info.isLogin) {
    if (gg = goal.getMsg('gb')) ById('tfd_bee_nt').innerHTML = gg;
    else ById('tfd_bee_nt').innerHTML = "You got it right! See if your friends can spell it! " + tfdShare.getBtns('b' + shKey + (lev + 4), "I correctly spelled this " + LEV[lev - 1] + " Level word in Spelling Bee! Can you?");
   } else
    ById('tfd_bee_nt').innerHTML = tfdShare.getBadgeHTML('gb');
   a.style.backgroundColor = '#F1FFF3';
   fconn.ev('gb@' + lev);
  } else {
   setHtml('tfd_bee_answ', 'Correct answer: <a style="text-decoration:underline" href="/' + encodeURIComponent(word) + '">' + word + '</a>');
   ById('tfd_bee_nt').style.color = '#e76049';
   goal.reset('gb');
   ById('tfd_bee_nt').innerHTML = "Sorry, that's incorrect. See if your friends can spell it! " + tfdShare.getBtns('b' + shKey + lev, "I couldn't spell this " + LEV[lev - 1] + " Level word in Spelling Bee. Can you?");
   a.style.backgroundColor = '#FFC0CB';
  }
  lib.hide('beeAnsBtn');
  lib.show('tfd_bee_nt');
  lib.show('tfd_bee_difficulty');
  if (typeof (regShare) == "function") regShare('gb');
  if (window.sessionStorage) sessionStorage.beePlayed = 1;
 };
 this.keyDown = function (k, e) {
  if (e.ctrlKey && k == 13) {
   var s = document.querySelector("#tfd_bee_sound .snd-icon-plain");
   if (s) s.click();
   return false;
  }
  if (k != 13 && k != 10) return true;
  if (ById('beeAnsBtn').style.display) th.newGame(1); else { if (ById('tfd_bee_uword').value) th.answer(); }
  return false;
 };
 this.callback = function (w, p, d, k) {
  word = w;
  setHtml('tfd_bee_sound', "<span class=snd data-ttl='Ctrl+Enter' data-snd=" + p + "></span>");
  setHtml('tfd_bee_def', d);
  snd.fill([ById('tfd_bee_sound').firstChild]);
 };
 if (!window.sessionStorage || !sessionStorage.beePlayed) {
  word = b.getAttribute('data-word');
  shKey = b.getAttribute('data-key');
 } else th.newGame();
}
var matchUp = new function () {
 var y1 = -1, ans = [-1, -1, -1, -1, -1];
 var btnClr = ById('muClear');
 if (!btnClr) return;
 var btnSubmit = ById('muSubmit');
 function getY(div) { return +div.id.substr(4)}
 function titleL(s) {ById('muTitleL').style.visibility=s?'':'hidden'}
 function titleR(s) {ById('muTitleR').style.visibility=s?'':'hidden'}
 forAll("[id^=mu_a]", function (m) {
  m.onclick = function () {
   if (ans[getY(this)] >= 0) return;
   btnClr.disabled = false;
   titleL(0);titleR(1);
   y1 = getY(this);
   forAll("[id^=mu_a]", function (n) {
    if (ans[getY(n)] < 0) n.className = 'mu_' + (n == m ? 'S' : 'E') + getY(n);
   });
   forAll("[id^=mu_b]", function (n) {
    if (fixArrIE8(ans).indexOf(getY(n)) < 0) n.className = 'mu_H' + y1;
   });
  };
 });
 forAll("[id^=mu_b]", function (m) {
  m.onclick = function () {
   if (typeof (regShare) == "function") regShare('gm');
   if (fixArrIE8(ans).indexOf(getY(this)) >= 0) return;
   titleR(0);
   var y2 = +this.id.substr(4);
   m.className = 'mu_S' + y1;
   ans[y1] = y2;
   if (fixArrIE8(ans).indexOf(-1)>=0) titleL(1);
   forAll("[id^=mu_a]", function (n) {
    if (ans[getY(n)] < 0) n.className = 'mu_H' + getY(n);
   });
   forAll("[id^=mu_b]", function (n) {
    if (fixArrIE8(ans).indexOf(getY(n)) < 0) n.className = 'mu_E' + y1;
   });

  };
 });
 btnClr.onclick = function () {
  ans = [-1, -1, -1, -1, -1];
  forAll("[id^=mu_a]", function (n) { n.className = 'mu_D' + getY(n) });
  forAll("[id^=mu_b]", function (n) { n.className = 'mu_E' + getY(n) });
  btnClr.disabled = true;
  titleL(1);titleR(0);
 };
 btnSubmit.onclick = function () {
  var loc = '//'+(info.PageLang=='es'?'es':'www')+'.thefreedictionary.com/_/MatchUp.aspx?res=' + encodeURIComponent(ans);
  for (var i = 0; i <= 4; i++) {
   loc += '&tfd_a' + i + '=' + encodeURIComponent(ById('mu_a' + i).innerHTML)
   loc += '&tfd_b' + i + '=' + encodeURIComponent(ById('mu_b' + i).innerHTML)
  }
  top.location = loc;
 };
}
var mismatch = new function () {
 var y1 = -1, ans = [-1, -1, -1, -1, -1];
 var btnClr = ById('mmClear');
 if (!btnClr) return;
 var btnSubmit = ById('mmSubmit');
 function getY(div) { return +div.id.substr(4) }
 function titleL(s) {ById('mmTitleL').style.visibility=s?'':'hidden'}
 function titleR(s) {ById('mmTitleR').style.visibility=s?'':'hidden'}
 forAll("[id^=mm_a]", function (m) {
  m.onclick = function () {
   if (ans[getY(this)] >= 0) return;
   btnClr.disabled = false;
   titleL(0);titleR(1);
   y1 = getY(this);
   forAll("[id^=mm_a]", function (n) {
    if (ans[getY(n)] < 0) n.className = 'mm_' + (n == m ? 'S' : 'E') + getY(n);
   });
   forAll("[id^=mm_b]", function (n) {
    if (fixArrIE8(ans).indexOf(getY(n)) < 0) n.className = 'mm_H' + y1;
   });
  };
 });
 forAll("[id^=mm_b]", function (m) {
  m.onclick = function () {
   if (typeof (regShare) == "function") regShare('gm');
   if (fixArrIE8(ans).indexOf(getY(this)) >= 0) return;
   titleR(0);
   var y2 = +this.id.substr(4);
   m.className = 'mm_S' + y1;
   ans[y1] = y2;
   if (fixArrIE8(ans).indexOf(-1) >= 0) titleL(1);
   forAll("[id^=mm_a]", function (n) {
    if (ans[getY(n)] < 0) n.className = 'mm_H' + getY(n);
   });
   forAll("[id^=mm_b]", function (n) {
    if (fixArrIE8(ans).indexOf(getY(n)) < 0) n.className = 'mm_E' + y1;
   });
  };
 });
 btnClr.onclick = function () {
  ans = [-1, -1, -1, -1, -1];
  forAll("[id^=mm_a]", function (n) { n.className = 'mm_D' + getY(n) });
  forAll("[id^=mm_b]", function (n) { n.className = 'mm_E' + getY(n) });
  btnClr.disabled = true;
  titleL(1);titleR(0);
 };
 btnSubmit.onclick = function () {
  var loc = '//'+(info.PageLang=='es'?'es':'www')+'.thefreedictionary.com/_/MatchUp.aspx?mismatch=1&res=' + encodeURIComponent(ans);
  for (var i = 0; i <= 4; i++) {
   loc += '&tfd_a' + i + '=' + encodeURIComponent(ById('mm_a' + i).innerHTML)
   loc += '&tfd_b' + i + '=' + encodeURIComponent(ById('mm_b' + i).innerHTML)
  }
  top.location = loc;
 };
}
window.observables = new function () {
 var frames = [];

 function simpleObservable(initialValue) {
  function obs() {
   var a = arguments;
   if (a.length === 1) {
    var n = obs.chk(a[0]);
    obs.val !== n && (obs.val = n, obs.chgd());
   } else {
    if (frames.length) frames[frames.length - 1].callback(obs);
    return obs.val;
   }
  }

  obs.chk = function (v) { return v instanceof Array ? v.slice(0) : v; };
  obs.val = obs.chk(initialValue);
  obs.subs = [];
  obs.subscribe = function(n,i){typeof n=="function"&&obs.subs.push(n)&&i&&n(obs.val, obs);}
  obs.chgd = function () {
   var val = obs.val;
   for (var n = 0; n < obs.subs.length; n++) obs.subs[n](val, obs);

  };
  return obs;
 }
 function simpleComputedObservable(evaluator) {
  function cobs() { return cobs.val(); }

  cobs.subs = [];
  cobs.val = evaluator;
  cobs.subscribe = function (n, i) { typeof n == "function" && cobs.subs.push(n) && i && n(cobs.val(), cobs()); };
  cobs.chgd = function() {
   var val = cobs.val();
   for (var n = 0; n < cobs.subs.length; n++) cobs.subs[n](val, cobs);
  };

  var dependencies = [];
  frames.push({ callback: function (obs) { dependencies.push(obs); } });
  evaluator();
  frames.pop();
  for (var i in dependencies) dependencies[i].subscribe(cobs.chgd);

  return cobs;
 }

 this.observable = function (initialValue) {
  return typeof ko=="undefined"?simpleObservable(initialValue):ko.observable(initialValue);
 };

 this.computed = function(evaluator) {
  return typeof ko == "undefined" ? simpleComputedObservable(evaluator) : ko.computed(evaluator);
 };

 this.observableArray = function (initialValue) {
  if(typeof ko!="undefined")return ko.observableArray(initialValue);

  var result = simpleObservable();
  result.chk = function(n){return n instanceof Array?[].concat(n):[]}
  result.removeAll = function(){result([])}
  result.push = function(n){result(result().concat([n]))}
  result(initialValue);
  return result;
 };
};
var grammarQuiz = new function () {
 this.selected = function (el) {
  ById('gqAnsBtn').disabled = false;
 }
 this.submit = function () {
  lib.hide('gqBtnsStart');
  var l = document.querySelectorAll('#grammarQuiz input[type="radio"]');
  for (var i = 0; i < l.length; i++) {
   var inp = l[i];
   var lb = inp.nextSibling;
   var isCr = (inp.className == 'cr');
   if (inp.checked) {
    lb.className =  isCr ? "aCrU" : "aWr";
    lib.show(isCr ? 'gqBtnsRight' : 'gqBtnsWrong');
    if (isCr) fconn.ev("ggq"); else goal.reset('ggq');
   } else {
    lb.className = isCr ? "aCr" : "aOth";
   }
   inp.disabled = true;
  }
 }
 this.restart = function() {
  lib.AsyncRequest('/_/game/grammarQuiz.ashx?&r=' + Math.random());
 }
 this.callback = function(json) {
  var dt = JSON.parse(json);
  lib.hide('gqBtnsRight');
  lib.hide('gqBtnsWrong');
  lib.show('gqBtnsStart');
  ById('gqAnsBtn').disabled = true;
  ById("gqQuestion").innerHTML = dt.question;
  var s = "";
  for (var i = 0; i < dt.answers.length; i++) {
   var cls = (i + 1 == dt.corrAnsNum) ? " class=\"cr\"" : "";
   s += "<input type=\"radio\" name=\"gQuiz\" onclick=\"grammarQuiz.selected(this)\"" + cls + " id=\"opt" + i + "\"><label for=\"opt" + i + "\">" + dt.answers[i] + "</label><br>";
  }
  ById("gqAnswers").innerHTML = s;
  ById("grammarQuiz").setAttribute("data-url", dt.url);
 }
 this.learn = function () {
  location.href = "//www.thefreedictionary.com/" + ById("grammarQuiz").getAttribute("data-url") + ".htm";
 }
}
var wm = new function () {
 var data = [];
 var notSupported = (navigator.userAgent.indexOf('MSIE 8') >= 0);
 var isGameOver = 0;
 var isNewUser = 1;
 var sortABC = 0;
 var lastFoundIdx = 0;
 var foundCount = 0;
 var sh;
 var timedGame = null;
 var startTime = null;
 var timedScoreByLength = [0, 0, 0, 2, 3, 5, 8, 13, 21, 34, 55, 89];

 function saveToLocalStorage() {
  if (notSupported && timedGame) return;
  if (window.sessionStorage) sessionStorage['wm-timed'] = JSON.stringify({ sh: sh, data: data, sortABC: sortABC });
 }
 function restoreFromSessionStorage() {
  if (!notSupported && window.sessionStorage && sessionStorage['wm-timed']) {
   try {
    var d = JSON.parse(sessionStorage['wm-timed']);
    sh = d.sh;
    data = d.data;
    isGameOver = 1;
    sortABC = d.sortABC;
    isNewUser = 0;
    refresh();
   } catch (e) {
   }
  } else {
   refresh();
  }
 }
 var colorBlender = new function () {
  function hexToRgb(color) {
   var result=/^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(color);
   return result ? { r: parseInt(result[1], 16), g: parseInt(result[2], 16), b: parseInt(result[3], 16) } : null;
  }
  function rgbToHex(color) {
   function componentToHex(n){var t=n.toString(16);return t.length==1?"0"+t:t}
   return"#"+componentToHex(color.r)+componentToHex(color.g)+componentToHex(color.b);
  }
  function blendComponent(from, to, l) {
   return Math.round((to - from) * l + from);
  }
  this.blendColors = function (color1, color2, level) {
   color1 = hexToRgb(color1); color2 = hexToRgb(color2);
   return rgbToHex({ r: blendComponent(color1.r, color2.r, level), g: blendComponent(color1.g, color2.g, level), b: blendComponent(color1.b, color2.b, level) });
  };
 };

 function canvasTimer(canvas, timer, lineWidth) {
  if (typeof (canvas.getContext) != "function" || !canvas.getContext('2d')) return;

  function clearCanvas() {
   var context = canvas.getContext('2d');
   context.clearRect(0, 0, canvas.width, canvas.height);
  }

  function drawArc(elapsed, duration) {
   var ctx = canvas.getContext('2d'),
    startAngle = -Math.PI / 2,
    endAngle = 2 * Math.PI * elapsed / duration - Math.PI / 2,
    x = canvas.width / 2,
    y = canvas.height / 2,
    radius = Math.min(x, y) - lineWidth / 2;

   ctx.beginPath();
   ctx.arc(x, y, radius, startAngle, endAngle, true);
   ctx.lineWidth = lineWidth;
   var left = (duration - elapsed);
   ctx.strokeStyle = left > 30 ? "#2ecc71" : left > 15 ? colorBlender.blendColors("#2ecc71", "#ffdd00", (30 - left) / 15) : colorBlender.blendColors("#ffdd00", "#ff0000", (15 - left) / 15);
   ctx.stroke();
  }

  function onStartedChanged() {
   if (!timer.started()) clearCanvas();

  }
  function onElapsedChanged() {
   clearCanvas();
   drawArc(timer.elapsed(), timer.duration());
  }

  timer.started.subscribe(onStartedChanged);
  timer.elapsed.subscribe(onElapsedChanged);
 }

 function simpleTimer() {
  var self = this, timer = null, tick = null, initial = null, startTime = null;

  this.elapsed = observables.observable();
  this.duration = observables.observable();
  this.started = observables.observable();

  function onTick() {
   timer = null;

   var newElapsed = initial + (new Date() - startTime) / 1000;
   if (!self.started() || newElapsed >= self.duration()) {
    self.elapsed(self.duration());
    self.started(false);
    return;
   }

   self.elapsed(newElapsed);

   timer = setTimeout(onTick, tick * 1000);
  }

  this.start = function (elapsed, duration, tickValue) {
   tick = tickValue;
   if (timer != null) {
    clearTimeout(timer);
   }

   startTime = new Date();
   initial = elapsed;
   self.elapsed(elapsed);
   self.duration(duration);
   self.started(true);
   timer = setTimeout(onTick, tick * 1000);
  };
 }

 function wordwheel(width, height, letterWidth, letterHeight) {
  var self = this;

  function wheelLetter(n) {
   var t = this;
   this.character = observables.observable();
   this.selected = observables.observable(!1);
   this.position = observables.observable();
   this.top = observables.observable();
   this.left = observables.observable();
   this.tryToggle = function() { n.onletterclick(t) }
  }

  var centerX = width / 2;
  var centerY = height / 2;
  var selectedLetters = [];
  var selectedChars = [];

  this.disabled = observables.observable(false);
  this.letters = observables.observableArray();
  this.selectedChars = observables.observable(selectedChars);

  function getLetterCoordinates(n, t) {
   var i = 2 * Math.PI / (n - 1), r = width / 2 - (width - 3 * letterWidth) / 4 - letterWidth * .5, u = centerX - letterWidth / 2, f = centerY - letterHeight / 2, e, o;
   return t > 0 && (e = Math.cos(i * t) * r, o = Math.sin(i * t) * r, u -= e, f -= o), { left: u, top: f }
  }

  function addLetters(word) {
   var letters = self.letters();
   if (letters.length !== word.length) {
    self.letters.removeAll();

    var letter = null;

    for (var i = 0; i < word.length; i++) {
     letter = new wheelLetter(self);
     letter.position(i);
     var coords = getLetterCoordinates(word.length, i);

     letter.left(coords.left);
     letter.top(coords.top);

     letter.character(word[letter.position()]);
     self.letters.push(letter);
    }
   } else {
    for (var i in letters) {
     letters[i].character(word[letters[i].position()]);
    }
   }
  }

  this.setNewWord = function (word) {addLetters(word);};

  this.unselectLast = function () {
   if (selectedLetters.length > 0) {
    self.onletterclick(selectedLetters[selectedLetters.length - 1]);
   }
  };

  this.onletterclick = function (letter) {
   if (self.disabled()) return;
   if (!letter.selected()) {
    letter.selected(true);
    selectedLetters.push(letter);
    selectedChars.push(letter.character());
   } else
    for (var i = selectedLetters.length - 1; i >= 0; i--) {
     var selectedLetter = selectedLetters[i];
     selectedLetter.selected(false);
     selectedLetters.pop();
     selectedChars.pop();
     if (selectedLetter === letter) break;
    }

   self.selectedChars(selectedChars);
  };

  this.unselectAll = function () {
   for (var i in selectedLetters) selectedLetters[i].selected(false);

   selectedLetters = [];
   selectedChars = [];
   self.selectedChars(selectedChars);
  };
 }

 function timedRound(timerCircleCanvas, timerBorderWidth) {
  var self = this;

  var roundTimer = new simpleTimer();
  var timedCanvas = new canvasTimer(timerCircleCanvas, roundTimer, timerBorderWidth);
  var roundTimeInSeconds;
  var tickInSeconds = 0.04;
  this.roundStatus = observables.observable();
  this.timeLeftInSeconds = observables.observable();
  this.roundTimeInSeconds = function () { return roundTimeInSeconds; };

  roundTimer.elapsed.subscribe(function (elapsed) {
   self.timeLeftInSeconds(Math.floor(roundTimeInSeconds - elapsed));
  });
  roundTimer.started.subscribe(function (started) {
   if (!started) {
    if (self.roundStatus() == timedRound.roundStatusType.started) {
     self.timeLeftInSeconds(0);
     self.roundStatus(timedRound.roundStatusType.timePassed);
     self.timeLeftInSeconds(null);
    }
   }
  });

  this.timeLeftToString = observables.computed(function () {
   var totalSeconds = self.timeLeftInSeconds();
   if (totalSeconds == null) return "";

   var minutes = Math.floor(totalSeconds / 60);
   var seconds = totalSeconds % 60;
   return (minutes >= 10 ? minutes : '0' + minutes) + ":" + (seconds >= 10 ? seconds : '0' + seconds);
  });

  this.init = function (roundTimeInSecondsValue) {
   roundTimeInSeconds = roundTimeInSecondsValue;
   self.roundStatus(timedRound.roundStatusType.notStarted);
   self.timeLeftInSeconds(null);
  };

  this.start = function (elapsed) {
   self.timeLeftInSeconds(null);
   if (!isNaN(roundTimeInSeconds) && roundTimeInSeconds > 0) {
    roundTimer.start(elapsed || 0, roundTimeInSeconds, tickInSeconds);
   } else {
    roundTimeInSeconds = undefined;
   }
   self.roundStatus(timedRound.roundStatusType.started);
  };

  this.cancel = function (saved) {
   self.roundStatus(saved ? timedRound.roundStatusType.savedForLater : timedRound.roundStatusType.canceled);
   roundTimer.started(false);
  };
 }

 timedRound.roundStatusType = { notStarted: 0, started: 1, canceled: 2, savedForLater: 3, timePassed: 4, allWordsFound: 5, alreadyPlayed: 6 };

 function wordFormByNumber(number, singular, plural4, plural5) {
     var test = number % 100;
     if (test >= 11 && test <= 19) return plural5;
     test %= 10;
     switch (test) {
         case 1:
             return singular;
         case 2:
         case 3:
         case 4:
             return plural4;
         default:
             return plural5;
     }
 }

 function refresh(error) {
     ById('wm_error').innerHTML = error || '';
  if (sortABC) ById('rAlphabetical').checked = true; else ById('rChronological').checked = true;
  initRound();

  if (!timedGame)
   ById('wm_word').innerHTML = "<div class='wm_w'><a href='/" + data[0].word.toLowerCase() + "'>" + data[0].word.toUpperCase() + "</a></div>";
  foundCount = fixArrIE8(data).filter(function (e) { return e.found }).length;
  ById('wm_state').innerHTML = ById('wmStateString').innerHTML
   .replace('#f', foundCount)
   .replace('#t', data.length - 1) + ' (' + Math.round(100 * foundCount / (data.length - 1)) + '%)';
  if (timedGame)
  {
      var pointsScored = fixArrIE8(data).reduce(function (p, e) { return e.found ? (p + (timedScoreByLength[e.word.length] || 0)) : p }, 0);
      var wordsString = wordFormByNumber(foundCount, ById('wm_wh_n1word').innerHTML, ById('wm_wh_n4words').innerHTML, ById('wm_wh_n5words').innerHTML).replace('{0}', foundCount + '/' + (data.length - 1));
      var pointsString = wordFormByNumber(foundCount, ById('wm_wh_n1point').innerHTML, ById('wm_wh_n4points').innerHTML, ById('wm_wh_n5points').innerHTML).replace('{0}', pointsScored);

      ById('wm_wh_results').innerHTML = wordsString + '<br/>' + pointsString;
  }
  var dd = data.slice(1);
  if (sortABC)
   dd = dd.sort(function (a, b) { return a.word < b.word ? 1 : -1 });
  else
   dd = dd.sort(function (a, b) { return a.found == b.found ? (a.word < b.word ? 1 : -1) : (a.found > b.found ? 1 : -1) });
  var i = dd.length;
  var s = '';
  var ov = isGameOver || foundCount == data.length - 1;
  while (i-- > 0) {
   var d = dd[i];
   var word = d.word;
   var inTFD; if (!(inTFD = (word[0]!='*'))) word = word.substr(1);
   if (d.found > lastFoundIdx) lastFoundIdx = d.found;
   if (!timedGame && isGameOver || d.found) {
    var isLnk = (!timedGame || ov) && inTFD;
    s += "<div class='" + (timedGame ? 'wm_a wh' : d.found ? 'wm_a' : 'wm_ar') + "'>" + (timedGame ? '' : "<span class='wmhr'>&#9679;</span>&nbsp;") + "<a href='" + (isLnk ? ("/" + word.toLowerCase()) : "javascript:void(0)") + "' " + (!isLnk ? "style='cursor:default;'" : "") + ">" + word.toUpperCase() + "</a></div>";
   }
  }
  setHtml('wm_answers', s);
  lib.show('wm_game');
  tog('wm_addf', !ov);
  tog('wm_answer', !ov && !timedGame);
  tog('wm_wordhub-link', ov && timedGame && !isNewUser);

  tog('wmRegNote', foundCount >= 2 && !info.isLogin && !timedGame);
  if (tog('wmShNote', foundCount >= 2 && info.isLogin && !timedGame))
   setHtml('wmShNote0', tfdShare.getBtns('w' + foundCount + 'q' + sh.key, sh.msg.replace('#f', foundCount).replace('#t', data.length - 1)));
  tog('wm_wordwheel-mode', timedGame != null);
  tog('wm_state', timedGame == null);
  tog('wm_radio', timedGame == null);
  tog('wm_wh_wheel', timedGame != null && !isNewUser);
  tog('wm_wh_results', timedGame != null && !isNewUser);
  tog('wm_wh_time-left', timedGame != null && !isNewUser);
  tog('wm_wh_logo', timedGame != null && isNewUser);
  //tog('wh-answers', !isNewUser);
  tog('wm_wh_newuser', timedGame != null && isNewUser);
  tog('wm_answers', timedGame == null || !isNewUser);
  tog('wm_new_game', timedGame == null);
  tog('wm_wh_selected-chars', !ov);
  tog('wm_legacy-mode', timedGame == null);
  if (timedGame != null) {
   timedGame.wordwheel.disabled(ov);
   ById('wm_wordwheel-mode').className = ById('wm_wordwheel-mode').className.replace(' disabled', '') + (ov ? ' disabled' : '');
   if (!ov) {
    ById('wordMaker').focus();
   }
  }
 }
 function scrambleWord(n) { for (var i = "", t; n.length > 0;) t = Math.floor(Math.random() * n.length), i += n[t], n = n.substr(0, t) + n.substr(t + 1); return i }

 this.haveSavedSeed = function (seed) {
  lib.show('wmSaveNote');
  setHtml('wmSavedSeed', seed);
 }
 this.goToReg = function () {
  if (isGameOver) return;
  var f = document.createElement("form");
  f.setAttribute("method", "post");
  f.setAttribute("action", "https://secure.thefreedictionary.com/Registration.aspx?wm");
  var hf = document.createElement("input");
  hf.setAttribute("type", "hidden");
  hf.setAttribute("name", "wordMakerGameState");
  var gameDt = info.PageLang + ";" + data[0].word + ";" + fixArrIE8(data).filter(function (e) { return e.found }).map(function (e) { return e.word }).join();
  hf.setAttribute("value", gameDt);
  f.appendChild(hf);
  document.body.appendChild(f);
  f.submit();
 };

 function whGameOver(lang, seed, wordsFound, wordsTotal) {
  lib.AsyncRequest(fconn.URL + 'api/wordhub/endGame.ashx?lang=' + encodeURIComponent(lang) + "&seed=" + encodeURIComponent(seed) + "&wordsFound=" + encodeURIComponent(wordsFound.join(',')) + "&wordsTotal=" + encodeURIComponent(wordsTotal) + "&timed=True&tfd=1");
 }

 this.answer = function() {
  isGameOver = 1;
  refresh();
  if (timedGame != null) {
   whGameOver(info.PageLang, data[1].word, fixArrIE8(data).filter(function (e) { return e.found }).map(function (e) { return e.word }), data.length - 1);
  }
  else if (info.isLogin && fconn.isFC()) fc.wm.gameOver();
 };

 function tryAdd(w) {
  if (!w) return false;
  if (info.PageLang == "en") w = diacriticsRemover.remove(w);
  if (typeof (regShare) == "function") regShare('gw');
  var i = data.length - 1;
  while (i > 0) {
   if (data[i].word.toLowerCase() == w.toLowerCase()) {
    var found = data[i].found;
    if (!found) {
     data[i].found = lastFoundIdx + 1;
     refresh();
     if (timedGame == null && info.isLogin && fconn.isFC()) fc.wm.addWord(w,null, function() {
         data[i].found = 0;
         refresh("Couldn't record word. Please check your Internet connection.");
     });
     if (timedGame != null && (!info.isLogin || !fconn.isFC())) saveToLocalStorage();
    }

    ById('wm_new_word').value = '';
    return !found;
   }
   i--;
  }
  ById('wm_new_word').style.color = 'red';
  return false;
 }
 this.add = function () {
  tryAdd(ById('wm_new_word').value.trim());
 }
 this.newGame = function () {
  if (notSupported && timedGame) return;
  isNewUser = 0;
  lib.show('wm_wait');
  lastFoundIdx = 0;
  if (timedGame == null && info.isLogin && fconn.isFC())
   fc.wm.newGame(info.PageLang);
  else
   lib.AsyncRequest('/_/game/wordmaker.ashx?lang=' + info.PageLang + '&r=' + Math.random());
 }
 this.whCallbackFc = function (dt) {
  if (notSupported && timedGame) return;
  if (timedGame == null) return;
  if (!ById('wm_wait')) { setTimeout(function () { wm.whCallbackFc(dt) }, 500); return }

  lib.hide('wm_wait');
  if (dt) {
   data = fixArrIE8(dt.split(',')).map(function (e) { ee = e.split('@'); return { word: ee[0], found: ee.length == 1 ? 0 : +ee[1] }; });
   if (timedGame != null) data.splice(0, 0, { word: scrambleWord(data[0].word) });
   isGameOver = 1;
   isNewUser = 0;
  } else {
   isNewUser = 1;
  }

  refresh();
 };
 this.callBackFC = function (dt, key, share, isOver, sortA) {
  if (!ById('wm_wait')) { setTimeout(function () { wm.callBackFC(dt, key, share, isOver, sortA) }, 500); return }

  sh = { 'key': key, 'msg': share };
  lib.hide('wm_wait');
  data = fixArrIE8(dt.split(',')).map(function (e) { ee = e.split('@'); return { word: ee[0], found: ee.length == 1 ? 0 : +ee[1] }; });
  ById('wm_new_word').value = '';
  sortABC = +sortA;
  if (timedGame == null) {
   isGameOver = +isOver;
  } else {
   tog('wm_mode-btn', 1);
  }
  refresh();
 }
 this.callBackNewGame = function (words, key, share, keepIsGameOver) {
  lib.hide('wm_wait');
  sh = { 'key': key, 'msg': share };
  data = fixArrIE8(words.split(',')).map(function (e) { return { word: e, found: 0 }; });
  if (timedGame != null) data.splice(0, 0, { word: scrambleWord(data[0].word) });

  ById('wm_new_word').value = ''

  if (!keepIsGameOver)
   isGameOver = 0;
  if (timedGame != null) {
   startTime = new Date();
   timedGame.currentRound.cancel();
  }
  if (timedGame != null && (!info.isLogin || !fconn.isFC())) saveToLocalStorage();
  refresh();
 }
 this.sort = function (v) {
  sortABC = +v;
  if (timedGame == null && info.isLogin && fconn.isFC()) fc.wm.sort(sortABC);
  refresh();
 }
 var wmDiv = ById('wordMaker');

 function wwKeyDown(e) {
  if (timedGame == null || isGameOver) return;
  e = e || window.event;
  if (e.keyCode == 27) timedGame.wordwheel.unselectAll();
  else if (e.keyCode == 8) timedGame.wordwheel.unselectLast();
 }

 function wwKeyPress(e) {
  if (timedGame == null || isGameOver) return;
  var newChar = (String.fromCharCode((e || window.event).charCode)||'').toLowerCase()[0], foundSelected = null;
  for (var i = 0; i < timedGame.wordwheel.letters().length; i++) {
   var letter = timedGame.wordwheel.letters()[i];
   if (letter.character() == newChar) {
    if (!letter.selected()) {
     letter.tryToggle();
     foundSelected = null;
     break;
    } else foundSelected = letter;
   }
  }

  foundSelected != null && foundSelected.tryToggle();
 }

 function onWordWheelCharsChanged(chars) {
  tryAdd(chars.join("")) && timedGame.wordwheel.unselectAll();
 }

 function onRoundStatusChanged(status) {
  if (status == timedRound.roundStatusType.timePassed) {
   timedGame.wordwheel.unselectAll();
   wm.answer();
  }
 }

 function initRound() {
  if (timedGame == null) return;

  timedGame.wordwheel.unselectAll();
  if (isNewUser) return;
  if (notSupported) return;
  timedGame.wordwheel.setNewWord(data[0].word);
  if (isGameOver) return;
  if (timedGame.currentRound.roundStatus() != timedRound.roundStatusType.started) {
   timedGame.currentRound.init(120);
   timedGame.currentRound.start(startTime == null ? 0 : (new Date() - startTime) / 1000);
  }
 }

 function setupWordwheel() {
  var cont = ById("wm_wordwheel-mode"), timeLeft = ByQuery(cont, ".time-left"), wwCont = ByQuery(cont, ".wordwheel>.container"), wmCanv = ById("wm_timer-canvas"), wmChars = ByQuery(cont, ".selected-chars");
  timedGame = { wordwheel: new wordwheel(120, 120, 25, 25), currentRound: new timedRound(wmCanv, 6) };
  timedGame.currentRound.roundStatus.subscribe(onRoundStatusChanged);
  timedGame.currentRound.timeLeftToString.subscribe(function(n){timeLeft.innerHTML=n;wmCanv.style.display=n!=""?"":"none"},true);
  timedGame.currentRound.timeLeftInSeconds.subscribe(function (v) { timeLeft.className = v != null && v <= 15 ? 'time-left hurry-up' : 'time-left'; }, true);
  timedGame.wordwheel.letters.subscribe(function (ls) {
   wwCont.innerHTML = '';
   for (var i = 0; i < ls.length; i++) {
    (function(l, lc, lt) {
     lc.appendChild(lt);
     lc.className = 'wh_l l' + l.position() + (l.selected() ? ' sel' : '');
     lc.style.position = 'absolute';
     l.top.subscribe(function (t) { lc.style.top = t + 'px'; }, true);
     l.left.subscribe(function (t) { lc.style.left = t + 'px'; }, true);
     l.selected.subscribe(function (s) { lc.className = lc.className.replace(' sel', '') + (s ? ' sel' : ''); },true);
     lib.event.add(lc, 'click', l.tryToggle);
     l.character.subscribe(function (c) { lt.innerHTML = c }, true);
     wwCont.appendChild(lc);
    })(ls[i], document.createElement('div'), document.createElement('span'));
   }
  }, true);
  timedGame.wordwheel.selectedChars.subscribe(function (v) { wmChars.innerHTML = v.join(''); }, true);
  timedGame.wordwheel.selectedChars.subscribe(onWordWheelCharsChanged);

  lib.event.add(wmChars, 'click', function () { timedGame.wordwheel.unselectAll(true); });
  lib.event.add(ById('wordMaker'), 'keypress', wwKeyPress);
  lib.event.add(ById('wordMaker'), 'keydown', wwKeyDown);
  lib.event.add(document, 'keydown', function (e) {
   if (document.activeElement === ById('wordMaker') && (e || window.event).keyCode === 8) {
    e.preventDefault();
    e.stopPropagation();
    return false;
   }
  });
 }

 if (wmDiv != null) {
  if (wmDiv.getAttribute('data-whmode') == '1') {
   setupWordwheel();
   isGameOver = 1;
   tog('wm_mode-btn', 0);
  }
  if (timedGame != null && (!info.isLogin || !fconn.isFC())) restoreFromSessionStorage();
  else if ((words = wmDiv.getAttribute('data-words'))) this.callBackNewGame(words, wmDiv.getAttribute('data-sh-key'), wmDiv.getAttribute('data-sh-msg'), timedGame != null);
  else tog('wm_new_game', timedGame == null);
 } else {
  console.warn("!! ById('wordMaker') returned null.");
 }
}
var tfdShare = new function () {
 var th = this;
 this.tr = {playXMore: "You won! Win {0} more games to get the Bronze badge.",play1More: "You won! Win one more game to get the Bronze badge.",gotBadge: "Great job! You just earned the Bronze badge. Click {0} to collect it.",here:"here"};
 this.isBadge = false;
 this.getBtns = function (key, mg, p) {
   if (!key || key.length <= 3) return;
  var u = encodeURI(location.protocol + '//') + encodeURIComponent((info.PageLang == 'en' ? 'www' : info.PageLang) + '.' + info.Domain + (p ? '/_/archive.htm.aspx?shr=' : '/_/sh.aspx?t=') + key);
  var fb = '<li class="facebook"><a target="_blank" href="http:/' + '/www.facebook.com/share.php?u=' + u + '" title="Share on Facebook"></a></li>';
  var tw = '<li class="twitter"><a href="https:/' + '/twitter.com/share?url=' + u + '&text=' + encodeURIComponent(mg) + '" target="_blank" title="Share on Twitter"></a></li>';
  var email = '<li class="mail hide400"><a href="mailto' + ':?subject=' + encodeURIComponent(mg) + '&body=' + encodeURIComponent(mg) + '%0d%0a%0d%0aURL%3a ' + u + '" title="E-mail"></a></li>';
  var rss = '<li class="rss hide400"><a target=_blank href="/_/WoD/rss.aspx' + (p == 'wod' ? '' : '?type=' + p) + '" title="RSS feed"></a></li>';
  return '<ul class="social-networks">' + fb + tw + (p ? rss : '') + email + '</ul>';
 };
 this.getWonCnt = function (g) {
  if (g == 'gm' || g == 'gmm' || location.href.indexOf('sh.aspx') > 0) return 8;
  var cnt = lib.cookie.get('wonCnt',0,1);
  if (!cnt || cnt.substring(0, 2) != g) return 0; else return +cnt.substring(2);
 };
 this.getBadgeHTML = function (g) {
  this.isBadge = false;
  var cnt = this.getWonCnt(g);
  lib.cookie.set('wonCnt', g + (cnt + 1), 0, 1);
  if (cnt >= 3) {
   this.isBadge = true;
   return "<span class='img badge_" + g + "'></span>" + this.tr.gotBadge.replace("{0}", "<a class=u href='https://secure.thefreedictionary.com/Registration.aspx'>" + this.tr.here + "</a>");
  }
  return cnt == 2 ? this.tr.play1More : this.tr.playXMore.replace("{0}", 3 - cnt);
 };
 if ((h = ById('shareTr'))) this.tr = JSON.parse(h.getAttribute("data-tr"));
 forAll('.shareFeedBtns', function (d) {
  d.innerHTML = th.getBtns(d.getAttribute('data-feed-shkey'), d.getAttribute('data-feed-shmsg'), d.getAttribute('data-feed-type'));
 });
}
var goal = {
 reset: function (g) { fconn.ev(g+':gRS') },
 getMsg: function (g) { return fconn.isFC() ? fc.goal.getMsg(g) : null },
 getLev: function (g) { return fconn.isFC() ? fc.goal.getLev(g) : null }
}
if (d = ById('matchUpShare')) {
 var shBtns = tfdShare.getBtns(d.getAttribute('data-shkey'),d.getAttribute('data-shmsg'));
 var isMM = d.getAttribute('data-game') == 'mismatch';
 if (info.isLogin) {
  d.innerHTML = d.getAttribute('data-shlbl') + shBtns;
  fconn.ev("gm" + (isMM?'m@':'') + matchUpAns);
 } else
  d.innerHTML = (matchUpAns <= 2) ? d.getAttribute('data-shlbl') + shBtns : tfdShare.getBadgeHTML('gmm');
}
if (ById('dvLiveSearch')) {
 window.LiveSearch = new function () {
  var cnt = 0;
  var lst = ById('dvLiveSearch');
  var buff = [];
  var buff0;
  var reqSent = 0;
  this.IsPause = false;
  function request()
  {
   if (reqSent) return;
   reqSent = 1;
   var o = ById('ls' + cnt); if (o) o.parentNode.removeChild(o);
   lib.AsyncRequest(fconn.URL + "recentSearches.ashx?tab=" + info.tab + "&r=" + (new Date()).getTime(), null, null, function () { reqSent = 0; request(); }, 'ls' + (++cnt));
  }
  function show(txt, anim) {
   var typeWord = function (e, w, i) {
    if (i == w.length) {
     e.innerHTML = w;
    } else {
     e.innerHTML = w.substr(0, i) + "<span style='color:black'>|</span>";
     setTimeout(function () { typeWord(e, w, i + 1) }, 100);
    }
   }
   var e = document.createElement('a');
   e.setAttribute("href", encodeURI(txt).replace('%20', '+'));
   e.onmouseover = function () { LiveSearch.IsPause = true }
   e.onmouseout = function () { LiveSearch.IsPause = false }
   lst.insertBefore(e, lst.childNodes.length?lst.childNodes[0]:null);
   if (anim) setTimeout(function () {
    e.className = "sh";
    typeWord(e, txt, 1);
   }, 100);
   else {
    e.className = "sh";
    e.innerHTML = txt;
   }
   while (lst.children.length > 20) lst.removeChild(lst.children[lst.children.length - 1]);
  }
  function showNx() {
   if (buff.length > 0 && !LiveSearch.IsPause) {
    buff0 = buff[0];
    show(buff[buff.length-1], 1);
    buff.splice(buff.length - 1, 1);
   }
   if (buff.length < 4) request();
   setTimeout(showNx, 1000);
  }
  this.callback = function (x) {
   if (cnt == 1) {
    for (var i = 5; i < x.length-1; i++) {
     show(x[i]);
    }
    buff = x.slice(0, 5);
    setTimeout(showNx, 3000);
   } else {
    var p = fixArrIE8(x).indexOf(buff0);
    var xx;
    if (p == -1) xx = x; else if (p > 0) xx = x.slice(0, p);
    if (xx) Array.prototype.splice.apply(buff, [0, 0].concat(xx));
   }
   reqSent = 0;
  }
  request();
 }
};
if (info.isLogin && typeof fconn != "undefined" && !fconn.isFC()) lib.AsyncRequest(fconn.URL+'static/js/fc.ashx'+(window._cb?window._cb+'&':'?')+'lang='+(info.PageLang||'en'));
if (ById('spellCheckerFrame')) {
 window.SpellChecker = new function () {
  var ingoredErrs = [];
  this.hideErrorBox = function() {lib.hide('spellErrBox')}
  lib.event.add(document,'click',this.hideErrorBox);
  function onTextChanged() { ById('spellCheckerFrame').contentWindow.onChange() }

  this.showErrorBox = function(evt, el) {
   if (el.getAttribute('class') == 'spellErrFixed') return;
   ById('spellErrButtons').innerHTML = '';
   ById('spellErrHead').innerText = el.getAttribute('data-msg');
   rpls = el.getAttribute('data-rep').split('~~');
   for (var i = 0; i < rpls.length; i++) {
    if (!rpls[i]) continue;
    var e = document.createElement('div');
    e.setAttribute("class", "spellErrBoxBtn");
    e.innerText = rpls[i];
    e.onclick = function(t) {
     el.innerText = t.target.innerText;
     el.setAttribute("class", "spellErrFixed");
     el.onclick = null;
     lib.hide('spellErrBox');
     onTextChanged();
    }
    ById('spellErrButtons').appendChild(e);
   }
   var e = document.createElement('div');
   e.setAttribute("class", "spellErrBoxBtn");
   e.innerText = 'Ignore this error';
   e.onclick = function(t) {
    ingoredErrs.push(el.innerText);
    if(lib.isStor()) {
     sessionStorage.setItem("spellCheckIgnore", JSON.stringify(ingoredErrs));
    }
    el.setAttribute("class", "spellErrFixed");
    el.onclick = null;
    lib.hide('spellErrBox');
    onTextChanged();
   }
   ById('spellErrButtons').appendChild(e);
   var fr = ById('spellCheckerFrame'),
    x = Math.min(fr.clientWidth - 180, evt.clientX),
    y = fr.offsetTop + evt.clientY + 10;
    ById('spellErrBox').setAttribute('style', 'left:' + x + 'px;top:' + y + 'px');
   lib.show('spellErrBox');
   evt.preventDefault();
   evt.stopPropagation();
  }
  function setMsg(msg, isErr) {
   ById('spellCheckResult').innerHTML = msg;
   ById('spellCheckResult').className = isErr ? 'err' : 'no-err';
  }
  function parseData(dt, tx) {
   var ntx = '';
   var idx = 0;
   var errCnt = 0, ignCnt = 0;
   for (var i = 0; i < dt.matches.length; i++) {
    var d = dt.matches[i];
    var ofs = d.offset;
    var len = d.length;
    var word = tx.substr(ofs, len);
    var fIgn = false;
    for (var j = 0; j < ingoredErrs.length; j++) {
     if (ingoredErrs[j] == word) {
      fIgn = true;
      ignCnt++;
      break;
     }
    }
    if (fIgn) continue;
    function esc(s) { return s.replace(/\"/g, '&quot;') }
    var reps = "";
    for (var j = 0; j < d.replacements.length; j++) {
     if (reps) reps += "~~";
     reps += esc(d.replacements[j].value);
    }
    var msg = esc(d.message);
    errCnt++;
    ntx += tx.substring(idx, ofs);
    ntx += "<span class='spellErr' data-msg=\"" + msg + "\" data-rep=\"" +reps+ "\" onclick='parent.SpellChecker.showErrorBox(event, this);return false'>";
    ntx += word;
    ntx += "</span>";
    idx = ofs + len;
   }
   ntx += tx.substring(idx);
   ntx = ntx.replace(/\r\n/g, "<br>");
   ById('spellCheckerFrame').contentWindow.setText(ntx);
   var errTx;
   if (errCnt > 1) errTx = 'Found ' + errCnt + ' errors';
   else if (errCnt == 1) errTx = "Found one error";
   else errTx = 'No errors found';
   if (ignCnt) errTx += " (" + ignCnt + " ignored)";
   setMsg(errTx, errCnt)
  }
  var tx = '';
  this.check = function() {
   tx = ById('spellCheckerFrame').contentWindow.document.getElementById('txt').innerHTML;
   tx = tx.replace(/<br>/g, '\r\n');
   tx = tx.replace(/<div>/g, '\r\n');
   tx = tx.replace(/<.*?>/g, '');
   tx = tx.replace(/&nbsp;/g, ' ');
   tx = tx.replace(/ +/g, ' ').trim();
   if (!tx) return;
   if (info.isLogin&&lib.cookie.get('premium',1,1)) {
    if (tx.length > 100000) {
     setMsg('Text is too long. Please limit your text to less than 100,000 characters.',1);
     return;
    }
   } else {
    if (tx.length > 3000) {
     setMsg('Text is too long. Please limit your text to less than 3,000 characters. Or check up to 100,000 characters when you activate the <a href="https://secure.thefreedictionary.com/premium/subscribe">ad-free subscription</a>.', 1);
     return;
    }
   }
   setMsg('');
   lib.show('spellCheckWait');
   ById('spellCheckButton').disabled = true;
   var lg = ById('spellCheckLang');
   var rg = lg.options[lg.selectedIndex].value;

   var xmlhttp = new XMLHttpRequest();
   xmlhttp.onreadystatechange = function () {
    if (this.readyState == 4) {
     ById('spellCheckButton').disabled = false;
     lib.hide('spellCheckWait');
     if (this.status == 200) {
      var dt = JSON.parse(this.responseText);
      parseData(dt, tx);
     } else if (this.status == 403) {
      setMsg('Too many requests. Please try again later.', 1);
     } else {
      var ee = '';
      if (this.responseText) ee = ' (' + (this.responseText.length < 5?this.responseText:'?') + ')';
      setMsg('Error occurred' + ee + '. Please try again later.', 1);
     }
    }
   };
   xmlhttp.open("POST", "http://grammar.atstart.org/check.ashx", true);
   xmlhttp.send("text=" + encodeURIComponent(tx) + "&lang=en-" + rg + '&uid=' + fconn.userId() + '&prm=' + lib.cookie.get('premium', 1, 1));
  }
  window.onChangeTextSize = function () { ById('spellCheckerFrame').contentWindow.updFontSize(); }
  if(lib.isStor()) {
   var rg = localStorage["spellCheckRegion"];
   if (rg) ById('spellCheckLang').selectedIndex = rg;
   var sIgn = sessionStorage["spellCheckIgnore"];
   if (sIgn) ingoredErrs = JSON.parse(sIgn);
  }
  ById('spellCheckLang').addEventListener("change", function (e) { if (lib.isStor()) localStorage["spellCheckRegion"] = e.target.selectedIndex});
 }
};