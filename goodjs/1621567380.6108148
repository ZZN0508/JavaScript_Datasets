!function(a){"use strict";function b(a,b){var c=(65535&a)+(65535&b),d=(a>>16)+(b>>16)+(c>>16);return d<<16|65535&c}function c(a,b){return a<<b|a>>>32-b}function d(a,d,e,f,g,h){return b(c(b(b(d,a),b(f,h)),g),e)}function e(a,b,c,e,f,g,h){return d(b&c|~b&e,a,b,f,g,h)}function f(a,b,c,e,f,g,h){return d(b&e|c&~e,a,b,f,g,h)}function g(a,b,c,e,f,g,h){return d(b^c^e,a,b,f,g,h)}function h(a,b,c,e,f,g,h){return d(c^(b|~e),a,b,f,g,h)}function i(a,c){a[c>>5]|=128<<c%32,a[(c+64>>>9<<4)+14]=c;var d,i,j,k,l,m=1732584193,n=-271733879,o=-1732584194,p=271733878;for(d=0;d<a.length;d+=16)i=m,j=n,k=o,l=p,m=e(m,n,o,p,a[d],7,-680876936),p=e(p,m,n,o,a[d+1],12,-389564586),o=e(o,p,m,n,a[d+2],17,606105819),n=e(n,o,p,m,a[d+3],22,-1044525330),m=e(m,n,o,p,a[d+4],7,-176418897),p=e(p,m,n,o,a[d+5],12,1200080426),o=e(o,p,m,n,a[d+6],17,-1473231341),n=e(n,o,p,m,a[d+7],22,-45705983),m=e(m,n,o,p,a[d+8],7,1770035416),p=e(p,m,n,o,a[d+9],12,-1958414417),o=e(o,p,m,n,a[d+10],17,-42063),n=e(n,o,p,m,a[d+11],22,-1990404162),m=e(m,n,o,p,a[d+12],7,1804603682),p=e(p,m,n,o,a[d+13],12,-40341101),o=e(o,p,m,n,a[d+14],17,-1502002290),n=e(n,o,p,m,a[d+15],22,1236535329),m=f(m,n,o,p,a[d+1],5,-165796510),p=f(p,m,n,o,a[d+6],9,-1069501632),o=f(o,p,m,n,a[d+11],14,643717713),n=f(n,o,p,m,a[d],20,-373897302),m=f(m,n,o,p,a[d+5],5,-701558691),p=f(p,m,n,o,a[d+10],9,38016083),o=f(o,p,m,n,a[d+15],14,-660478335),n=f(n,o,p,m,a[d+4],20,-405537848),m=f(m,n,o,p,a[d+9],5,568446438),p=f(p,m,n,o,a[d+14],9,-1019803690),o=f(o,p,m,n,a[d+3],14,-187363961),n=f(n,o,p,m,a[d+8],20,1163531501),m=f(m,n,o,p,a[d+13],5,-1444681467),p=f(p,m,n,o,a[d+2],9,-51403784),o=f(o,p,m,n,a[d+7],14,1735328473),n=f(n,o,p,m,a[d+12],20,-1926607734),m=g(m,n,o,p,a[d+5],4,-378558),p=g(p,m,n,o,a[d+8],11,-2022574463),o=g(o,p,m,n,a[d+11],16,1839030562),n=g(n,o,p,m,a[d+14],23,-35309556),m=g(m,n,o,p,a[d+1],4,-1530992060),p=g(p,m,n,o,a[d+4],11,1272893353),o=g(o,p,m,n,a[d+7],16,-155497632),n=g(n,o,p,m,a[d+10],23,-1094730640),m=g(m,n,o,p,a[d+13],4,681279174),p=g(p,m,n,o,a[d],11,-358537222),o=g(o,p,m,n,a[d+3],16,-722521979),n=g(n,o,p,m,a[d+6],23,76029189),m=g(m,n,o,p,a[d+9],4,-640364487),p=g(p,m,n,o,a[d+12],11,-421815835),o=g(o,p,m,n,a[d+15],16,530742520),n=g(n,o,p,m,a[d+2],23,-995338651),m=h(m,n,o,p,a[d],6,-198630844),p=h(p,m,n,o,a[d+7],10,1126891415),o=h(o,p,m,n,a[d+14],15,-1416354905),n=h(n,o,p,m,a[d+5],21,-57434055),m=h(m,n,o,p,a[d+12],6,1700485571),p=h(p,m,n,o,a[d+3],10,-1894986606),o=h(o,p,m,n,a[d+10],15,-1051523),n=h(n,o,p,m,a[d+1],21,-2054922799),m=h(m,n,o,p,a[d+8],6,1873313359),p=h(p,m,n,o,a[d+15],10,-30611744),o=h(o,p,m,n,a[d+6],15,-1560198380),n=h(n,o,p,m,a[d+13],21,1309151649),m=h(m,n,o,p,a[d+4],6,-145523070),p=h(p,m,n,o,a[d+11],10,-1120210379),o=h(o,p,m,n,a[d+2],15,718787259),n=h(n,o,p,m,a[d+9],21,-343485551),m=b(m,i),n=b(n,j),o=b(o,k),p=b(p,l);return[m,n,o,p]}function j(a){var b,c="";for(b=0;b<32*a.length;b+=8)c+=String.fromCharCode(a[b>>5]>>>b%32&255);return c}function k(a){var b,c=[];for(c[(a.length>>2)-1]=void 0,b=0;b<c.length;b+=1)c[b]=0;for(b=0;b<8*a.length;b+=8)c[b>>5]|=(255&a.charCodeAt(b/8))<<b%32;return c}function l(a){return j(i(k(a),8*a.length))}function m(a,b){var c,d,e=k(a),f=[],g=[];for(f[15]=g[15]=void 0,e.length>16&&(e=i(e,8*a.length)),c=0;16>c;c+=1)f[c]=909522486^e[c],g[c]=1549556828^e[c];return d=i(f.concat(k(b)),512+8*b.length),j(i(g.concat(d),640))}function n(a){var b,c,d="0123456789abcdef",e="";for(c=0;c<a.length;c+=1)b=a.charCodeAt(c),e+=d.charAt(b>>>4&15)+d.charAt(15&b);return e}function o(a){return unescape(encodeURIComponent(a))}function p(a){return l(o(a))}function q(a){return n(p(a))}function r(a,b){return m(o(a),o(b))}function s(a,b){return n(r(a,b))}function t(a,b,c){return b?c?r(b,a):s(b,a):c?p(a):q(a)}"function"==typeof define&&define.amd?define(function(){return t}):a.md5=t}(this);

if(!window.location.origin) {
    window.location.origin = window.location.protocol + "//" + window.location.hostname + (window.location.port ? ':' + window.location.port: '');
}

(function(){
    function ajax(json){

        if(window.XMLHttpRequest) {
            var ajax = new XMLHttpRequest();
        } else {
            var ajax = new ActiveXObject( "Microsoft.XMLHTTP" );
        }

        if(json.type=='GET') {
            ajax.open('get',json.url+'?'+JsonToString(json.data),true);
            ajax.send();
        }
        else if(json.type=='POST') {
            ajax.open('post',json.url,true);
            ajax.setRequestHeader("Content-Type","application/json");
            ajax.send(json.data);
        }

        ajax.onreadystatechange = function(){
            if(ajax.readyState == 4){
                if(ajax.status>=200 && ajax.status<300 || ajax.status == 304){
                    json.success && json.success(ajax.responseText);
                }
                else{
                    json.error && json.error(ajax.responseText);
                }
            };
        };


        function JsonToString(json){
            var arr = [];
            for(var i in json){
                arr.push(i+'='+json[i]);
            };
            return arr.join('&');
        }
    }

    function __dateFormat__(fmt, date) {
      var o = {
        "M+" : date.getMonth()+1,                 //æœˆä»½
        "d+" : date.getDate(),                    //æ—¥
        "h+" : date.getHours(),                   //å°æ—¶
        "m+" : date.getMinutes(),                 //åˆ†
        "s+" : date.getSeconds(),                 //ç§’
        "q+" : Math.floor((date.getMonth()+3)/3), //å­£åº¦
        "S"  : date.getMilliseconds()             //æ¯«ç§’
      };
      if(/(y+)/.test(fmt))
        fmt=fmt.replace(RegExp.$1, (date.getFullYear()+"").substr(4 - RegExp.$1.length));
      for(var k in o)
        if(new RegExp("("+ k +")").test(fmt))
      fmt = fmt.replace(RegExp.$1, (RegExp.$1.length==1) ? (o[k]) : (("00"+ o[k]).substr((""+ o[k]).length)));
      return fmt;
    }

    function getCookie(name) {
        var arr;
        var reg = new RegExp("(^| )" + name + "=([^;]*)(;|$)");
        if (arr = document.cookie.match(reg))
          return decodeURIComponent(arr[2]);
        else
          return null;
    };
    function setCookie(cname, cvalue, exdays) {
        var d = new Date();
        d.setTime(d.getTime() + (exdays*24*60*60*1000));
        var expires = "expires="+d.toUTCString();
        document.cookie = cname + "=" + encodeURIComponent(cvalue) + "; " + expires;
    }
 
    var host = '//applog.yiche.com';
    // var host = 'http://192.168.87.106:9115';

    var lastUid = md5(document.cookie + Math.random().toString(36) + (new Date()).getTime()), seq = 0;

    window.__getAjaxHeader = function () {
        var currentUid = md5(document.cookie + Math.random().toString(36) + (new Date()).getTime());
        var res = {
            dvid: getCookie('CIGUID') || md5(document.cookie + navigator.userAgent), // å–CIGUID
            gudslf: currentUid, // æœ¬æ¬¡å…¨å±€å”¯ä¸€IDï¼š36ä½å…¨å±€å”¯ä¸€ID
            gudpar: lastUid, // ä¸Šæ¬¡å…¨å±€å”¯ä¸€IDï¼šç”±è°ƒç”¨æ–¹ä¼ å…¥ï¼Œ36ä½å…¨å±€å”¯ä¸€ID
            // seq: ++seq,
            reqid: md5(document.cookie + Math.random().toString(36) + (new Date()).getTime()), // å”¯ä¸€å°±è¡Œidå°±è¡Œ
            uidl: (window.Bitauto && window.Bitauto.Login && window.Bitauto.Login.result && (window.Bitauto.Login.result.userId || window.Bitauto.Login.result.id))|| getCookie('userid') || '', // ç™»å½•ç”¨æˆ·çš„ç”¨æˆ·ID
            osvl: navigator.userAgent,
            ver: window.__appver__,
            osl: window.__osl__ || 3, // æ“ä½œç³»ç»Ÿï¼Œ1:androidï¼›2:iosï¼›3:PCï¼›4:Mï¼›5:H5
        }
        lastUid = currentUid;
        return res;
    }
    window._reportLog = function (data, type, headerParams) {
        if(!(window.baseConf && baseConf.env == "prd")) {
          return;
        }
        if(!data) {
            data = {
                url: '',
                dur: 0,
                lgin: '',
                lgout: '',
                inbyte: 0,
                outbyte: 0,
                st: new Date().toLocaleString(),
                osl: 3
            };
        }
        if(!headerParams) {
            headerParams = window.__getAjaxHeader();
        }
        data.href = location.href;

        // å¯¹lgoutåšé•¿åº¦é™åˆ¶
        // if(data.lgout) {
        //     data.lgout = (data.lgout + '').slice(0, 5000);
        //     data.outbyte = data.lgout.length;
        // }

        var _url = '';

        if (type == 'err') {
            _url = host + '/api/v1/upload_web_error';
        } else {
            _url = host + '/api/v1/upload_web_info';
        }
        var logInfo = {
            seq: ++seq, // æ¯æ¬¡è°ƒç”¨ï¼Œå–å‡º+1ï¼Œä¼ é€’ä¸‹åŽ»ï¼›å¹¶å‘æ— æ³•ä¿è¯å…¨å±€å”¯ä¸€ï¼Œçœ‹èµ·æ¥æ•´ä½“æœ‰åº
            ltype: 7,// 7ï¼šWebClientCallï¼Œå‰ç«¯å®¢æˆ·ç«¯è®¿é—®ï¼›8ï¼šWebClientErrorï¼Œå‰ç«¯å®¢æˆ·ç«¯é”™è¯¯ï¼›++++++++++++++++++++++++++++++++++++++++++++
            reqid: headerParams.reqid,//æœ¬æ¬¡è¯·æ±‚ID//
            dvid: headerParams.dvid,//è®¾å¤‡id
            itime: __dateFormat__("yyyy-MM-dd hh:mm:ss", new Date()),//æ—¥å¿—ç”Ÿæˆæ—¶é—´ï¼Œå½“å‰æ—¶é—´
            url: /^\//.test(data.url) ? (/^\/\//.test(data.url) ? window.location.protocol + data.url : window.location.origin + data.url) : data.url, //æŽ¥å£url
            dur: data.dur,//æœ¬æ¬¡æ–¹æ³•è€—æ—¶  ++++++++++++++++++++++++++++++++++++++++++++
            gudslf: headerParams.gudslf,//æœ¬æ¬¡å…¨å±€å”¯ä¸€IDï¼š36ä½å…¨å±€å”¯ä¸€ID
            gudpar: headerParams.gudpar, //ä¸Šæ¬¡å…¨å±€å”¯ä¸€IDï¼šç”±è°ƒç”¨æ–¹ä¼ å…¥ï¼Œ36ä½å…¨å±€å”¯ä¸€ID
            ver: window.__appver__ || '',//,//appç‰ˆæœ¬
            osl: window.__osl__ || 3, //æ“ä½œç³»ç»Ÿï¼Œ1:androidï¼›2:iosï¼›3:PCï¼›4:Mï¼›5:H5
            cid: window.__osl__ == 3 ? 508 : 601,
            aname: window.baseConf && baseConf.aname || '',
            osvl: navigator.userAgent, //ç”¨æˆ·æ“ä½œç³»ç»Ÿç‰ˆæœ¬
            hst: "", // æœåŠ¡å™¨å™¨çš„ip
            ip: (window.Bitauto && window.Bitauto.location && window.Bitauto.location.ip) || window.__cip__ || "",//å®¢æˆ·ç«¯è¯·æ±‚ip
            uidl: headerParams.uidl,//ç™»å½•ç”¨æˆ·çš„ç”¨æˆ·ID
            lgin: JSON.stringify(data.lgin),//{}å…¥å‚
            lgout: data.lgout,//{}å‡ºå‚ ++++++++++++++++++++++++++++++++++++++++++++
            inbyte: data.inbyte,//å…¥å‚å­—èŠ‚æ•°
            outbyte: data.outbyte, //å‡ºå‚å­—èŠ‚æ•° ++++++++++++++++++++++++++++++++++++++++++++
            refer: document.referrer,//æ¥æº
            st: data.st,
            cyu: window.Bitauto && window.Bitauto.location && window.Bitauto.location.cityId || '', //ç”¨æˆ·é€‰æ‹©åŸŽå¸‚id
            cya: window.Bitauto && window.Bitauto.location && window.Bitauto.location.address || '', //å®šä½åŸŽå¸‚
            //err:"å¼‚å¸¸log"//å¼‚å¸¸ä¼ æ­¤å­—æ®µ
            //msg: ''//log
        };
        var _data = JSON.parse(JSON.stringify(data));
        delete _data.url;
        delete _data.dur;
        delete _data.lgin;
        delete _data.lgout;
        delete _data.inbyte;
        delete _data.outbyte;
        delete _data.st;
        delete _data.osl;

        if(type == 'err') {
            logInfo.ltype = 8;
            logInfo.err = JSON.stringify(_data);
        } else {
            logInfo.msg = JSON.stringify(_data);
        }
        setTimeout(function(){
            if(!!window.logSwitch == false && type != 'err' && logInfo.lgout != '') {
                var _lgout =  {}
                try {
                  _lgout = JSON.parse(logInfo.lgout);
                  _lgout.data = {};
                  logInfo.lgout = JSON.stringify(_lgout);
                } catch (e) {
                  _lgout = String(logInfo.lgout);
                  logInfo.lgout = _lgout;
                }
            }
            logInfo.lgout = logInfo.lgout.slice(0, 200);
            logInfo.lgin = logInfo.lgin.slice(0, 200);
            logInfo.url = logInfo.url.replace(/\?.+$/, '');
            ajax({
                type: 'POST',
                url: _url,
                dataType: "json",
                contentType: "application/json",
                data: JSON.stringify(logInfo),
                success: function(res){
                },
                error: function(error){
                }
            });
        }, 3000)
    }

    window.onerror = function(msg, url, row, col, error) {
      if(!(window.baseConf && baseConf.env == "prd")) {
        return;
      }
      var msg = {
        type: 'javascript',
        row: row,
        col: col,
        msg: msg,
        stack: error && error.stack && error.stack.replace('\n', '/-->/'),
        url: url || window.location.href,
        time: (new Date()).toLocaleString(),
        name: location.href,
        referrer: document.referrer,
      };
      var cid = window.__osl__ == 3 ? 508 : 601, aname = window.baseConf && baseConf.aname || '';
      var lgout = JSON.stringify({
        ercd: cid + '_' + aname + ':10214',
      })
      ajax({
        type: 'POST',
        url: host + '/api/v1/upload_web_error',
        dataType: "json",
        contentType: "application/json",
        data: JSON.stringify({
          seq: ++seq,
          err: JSON.stringify(msg),
          lgout: lgout,
          ltype: 8,
          url: url ? url.replace(/\?.+$/, '') : window.location.origin , //æŽ¥å£url 
          itime: __dateFormat__("yyyy-MM-dd hh:mm:ss", new Date()),//æ—¥å¿—ç”Ÿæˆæ—¶é—´ï¼Œå½“å‰æ—¶é—´
          lgin: '',
          reqid: '',
          gudpar: '',
          gudslf: '',
          ver: window.__appver__ || '',//,//appç‰ˆæœ¬
          osl: window.__osl__ || 3, //æ“ä½œç³»ç»Ÿï¼Œ1:androidï¼›2:iosï¼›3:PCï¼›4:Mï¼›5:H5
          cid: window.__osl__ == 3 ? 508 : 601,
          aname: window.baseConf && baseConf.aname || '',
          osvl: navigator.userAgent, //ç”¨æˆ·æ“ä½œç³»ç»Ÿç‰ˆæœ¬
          hst: "",
          ip: (window.Bitauto && window.Bitauto.location && window.Bitauto.location.ip) || window.__cip__ || "",//å®¢æˆ·ç«¯è¯·æ±‚ip
          uidl: (window.Bitauto && window.Bitauto.Login && window.Bitauto.Login.result && (window.Bitauto.Login.result.userId || window.Bitauto.Login.result.id))|| getCookie('userid') || '', // ç™»å½•ç”¨æˆ·çš„ç”¨æˆ·ID
          inbyte: 0,//å…¥å‚å­—èŠ‚æ•°
          outbyte: lgout.length, //å‡ºå‚å­—èŠ‚æ•° ++++++++++++++++++++++++++++++++++++++++++++
          refer: document.referrer,//æ¥æº
          cyu: window.Bitauto && window.Bitauto.location && window.Bitauto.location.cityId || '', //ç”¨æˆ·é€‰æ‹©åŸŽå¸‚id
          cya: window.Bitauto && window.Bitauto.location && window.Bitauto.location.address || '', //å®šä½åŸŽå¸‚
        }),
        success: function(res){
        },
        error: function(error){
        }
      });
  }
})()