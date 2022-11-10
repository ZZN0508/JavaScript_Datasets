(function () {var d = document, w = window, n = navigator, wp = w.performance, os, osMap, getCookie;if (!n || !n.sendBeacon || !wp || !wp.now) return;osMap = {'Win': 'Windows', 'Mac': 'MacOs', 'X11': 'Unix', 'Linux': 'Linux'};os = navigator.appVersion.match(/Win|Mac|X11|Linux/);getCookie = function (cookie) {var re = new RegExp('(?:(?:^|.*;\\s*)' + cookie + '\\s*\\=\\s*([^;]*).*$)|^.*$');return d.cookie.replace(re, '$1');};w.__trackAbandons = function () {d.removeEventListener('visibilitychange', w.__trackAbandons);n.sendBeacon('https://pixiedust.buzzfeed.com/events', w.JSON.stringify([{client_session_id: getCookie('bf-xdomain-session-uuid') || '00000000-0000-0000-0000-000000000000',client_uuid: getCookie('bf_visit') || '00000000-0000-0000-0000-000000000000',context_page_id: '1',context_page_type: 'feed',destination: 'buzzfeed_news',event_ts: Math.round(w.Date.now() / 1000),event_uri: w.location.href,event_uuid: '00000000-0000-0000-0000-000000000000',metric_name: 'load-abandonment',metric_type: 'custom',metric_value: wp.now(),mode: (w.matchMedia && w.matchMedia('screen and (max-width:51.9rem)').matches) ? 'mobile' : 'desktop',os: os ? osMap[os[0]] : 'Unknown',page_edition: 'ja-jp',page_session_id: '00000000-0000-0000-0000-000000000000',referrer_uri: d.referrer,source: 'web_bf',type: 'web_performance_metric',viewport_size: { width: w.screen.width, height: w.screen.height }}]));};d.addEventListener('visibilitychange', w.__trackAbandons);})();

(function() {
  var host = window.location.hostname;
  // var element = document.createElement('script');
  // var firstScript = document.getElementsByTagName('script')[0];
  // var url = 'https://quantcast.mgr.consensu.org'
  //   .concat('/choice/', '3aud4J6uA4Z6Y', '/', host, '/choice.js?timestamp=', Date.now())
  var uspTries = 0;
  var uspTriesLimit = 3;
  // element.async = true;
  // element.type = 'text/javascript';
  // element.src = url;

  // firstScript.parentNode.insertBefore(element, firstScript);

  function makeStub() {
    var TCF_LOCATOR_NAME = '__tcfapiLocator';
    var queue = [];
    var win = window;
    var cmpFrame;

    function addFrame() {
      var doc = win.document;
      var otherCMP = !!(win.frames[TCF_LOCATOR_NAME]);

      if (!otherCMP) {
        if (doc.body) {
          var iframe = doc.createElement('iframe');

          iframe.style.cssText = 'display:none';
          iframe.name = TCF_LOCATOR_NAME;
          doc.body.appendChild(iframe);
        } else {
          setTimeout(addFrame, 5);
        }
      }
      return !otherCMP;
    }

    function tcfAPIHandler() {
      var gdprApplies;
      var args = arguments;

      if (!args.length) {
        return queue;
      } else if (args[0] === 'setGdprApplies') {
        if (
          args.length > 3 &&
          args[2] === 2 &&
          typeof args[3] === 'boolean'
        ) {
          gdprApplies = args[3];
          if (typeof args[2] === 'function') {
            args[2]('set', true);
          }
        }
      } else if (args[0] === 'ping') {
        var retr = {
          gdprApplies: gdprApplies,
          cmpLoaded: false,
          cmpStatus: 'stub'
        };

        if (typeof args[2] === 'function') {
          args[2](retr);
        }
      } else {
        queue.push(args);
      }
    }

    function postMessageEventHandler(event) {
      var msgIsString = typeof event.data === 'string';
      var json = {};

      try {
        if (msgIsString) {
          json = JSON.parse(event.data);
        } else {
          json = event.data;
        }
      } catch (ignore) {}

      var payload = json.__tcfapiCall;

      if (payload) {
        window.__tcfapi(
          payload.command,
          payload.version,
          function(retValue, success) {
            var returnMsg = {
              __tcfapiReturn: {
                returnValue: retValue,
                success: success,
                callId: payload.callId
              }
            };
            if (msgIsString) {
              returnMsg = JSON.stringify(returnMsg);
            }
            event.source.postMessage(returnMsg, '*');
          },
          payload.parameter
        );
      }
    }

    while (win) {
      try {
        if (win.frames[TCF_LOCATOR_NAME]) {
          cmpFrame = win;
          break;
        }
      } catch (ignore) {}

      if (win === window.top) {
        break;
      }
      win = win.parent;
    }
    if (!cmpFrame) {
      addFrame();
      win.__tcfapi = tcfAPIHandler;
      win.addEventListener('message', postMessageEventHandler, false);
    }
  };

  // 📋 8/15 TODO: Not really a todo, but these couple of lines
  // are sometimes finnicky.
  if (typeof module !== 'undefined') {
    module.exports = makeStub;
  } else {
    makeStub();
  }

  var uspStubFunction = function() {
    var arg = arguments;
    if (typeof window.__uspapi !== uspStubFunction) {
      setTimeout(function() {
        if (typeof window.__uspapi !== 'undefined') {
          window.__uspapi.apply(window.__uspapi, arg);
        }
      }, 500);
    }
  };

  var checkIfUspIsReady = function() {
    uspTries++;
    if (window.__uspapi === uspStubFunction && uspTries < uspTriesLimit) {
      console.warn('USP is not accessible');
    } else {
      clearInterval(uspInterval);
    }
  };

  if (typeof window.__uspapi === 'undefined') {
    window.__uspapi = uspStubFunction;
    var uspInterval = setInterval(checkIfUspIsReady, 6000);
  }
})();


  window.BZFD = {
    Config: {"cluster":"prod","facebook_app_id":"862012947269736","facebook_pages":"21898300328,1457722161221362,1412406255640941","imageServiceUrl":"https://img.buzzfeed.com/buzzfeed-static","pixiedustUrl":"https://pixiedust.buzzfeed.com","isConsentRequired":true,"webRoot":"https://www.buzzfeed.com","branchKey":"key_live_ceFzhmH1fxNfPm55351GdbnhwxioKRyh","base_url":"","staticRoot":"/static-assets","bfAppId":352969997,"bfwInfoCookie":"bf2-b_info","facebookApi":{"version":"v2.9","appId":"862012947269736"},"emailSignUpUrl":"https://www.buzzfeed.com/newsletter/v3/subscriptions","env":"prod","sentryUrl":"https://afa4961bdef04ae0ba22ae058bbf6685@sentry.io/136284","canaryDeploy":false,"abeagle":{"url":"https://abeagle-public.buzzfeed.com","isEnabled":"false"},"tracking":{"pixiedust":{"impression_sampling_rate":0.05,"instrumentation_sampling_rate":0.1,"page_view_url":"feed"},"googleAnalytics":{"id":"UA-1740781-1"},"pixels":{"facebook":{"custom_audience":260954170738952}}},"video_app_api":"https://videoapp-api-ng.buzzfeed.com/v2/videos","feeds_api_origin":"https://feeds.buzzfeed.com","recsys_api_origin":"https://recsys-api.buzzfeed.com","ads":{"sizes":{"NATIVE":[5,5],"FLUID":"fluid","RESEARCH_PIXEL":[1,1],"RESEARCH_SURVEY":[2,2],"PROGRAMMATIC_PREBID":[1,1],"PROGRAMMATIC_BILLBOARD":[970,250],"PROGRAMMATIC_HORIZONTAL_4to1":[970,250],"PROGRAMMATIC_SMARTPHONE_BANNER":[320,50],"PROGRAMMATIC_HORIZONTAL_6to1":[320,50],"PROGRAMMATIC_LEADERBOARD":[728,90],"PROGRAMMATIC_HORIZONTAL_8to1":[728,90],"PROGRAMMATIC_SUPER_LEADERBOARD":[970,90],"PROGRAMMATIC_HORIZONTAL_10to1":[970,90],"PROGRAMMATIC_VERTICAL":[300,600],"PROGRAMMATIC_VERTICAL_1to2":[300,600],"PROGRAMMATIC_MEDIUM_RECTANGLE":[300,250],"PROGRAMMATIC_TILE_1to1":[300,250],"BIGSTORY_LEGACY_PARTNER":[300,250]},"programmaticSizes":[[300,250],[728,90],[320,50],[300,600],[970,250],[970,90]]}},
    Context: {"page":{"id":1,"destination":"buzzfeed","edition":"jp","localization":{"country":"ja-jp","language":"ja","locale":"en_US","translations":{"ADVERTISE_WITH_BUZZFEED":"","ADVERTISE_WITH_URL":"","ADVERTISEMENT":"\u5e83\u544a","PAID_POST":"Sponsored","PROMOTED_BY":"Sponsored by","PROMOTED":"Sponsored","SPONSORED_BY":"Sponsored by","ABOUT_US":"About Us","AGAIN":"\u623b\u308b","AGAIN_SPAIN":"","BREAKING":"\u901f\u5831","BREAKING_NEWS":"\u901f\u5831","BUZZFEED_COM":"buzzfeed.com","BUZZFEED_HOME":"BuzzFeed Home","BUZZFEED_INC":"BuzzFeed, Inc","BUZZFEED_REPORTING_TO_YOU":"BuzzFeed, Reporting To You","BUZZFEED_QUIZZES":"BuzzFeed Quizzes","CLOSE":"\u9589\u3058\u308b","COOKIE_INFO":"\u30af\u30c3\u30ad\u30fc\u60c5\u5831","COPYRIGHT_BUZZFEED_INC":"Copyright BuzzFeed, Inc. All rights reserved.","CUTE":"Cute","DASHBOARD":"Dashboard","DAY_AGO":"1\u65e5\u524d","DAYS_AGO":"{}\u65e5\u524d","EMAIL":"Email","ENTER_VALID_EMAIL":"Please enter a valid email address","FAIL":"Fail","FOLLOW_US_ON":"\u3067\u30d5\u30a9\u30ed\u30fc\u3059\u308b","FOLLOW_US_ON_TWITTER":"Twitter\u3067\u30d5\u30a9\u30ed\u30fc\u3059\u308b","FOLLOW_US_ON_TWITTER_NEWS":"","GET_FIRST_EMAIL":"You're almost there! Check your inbox and confirm your subscription now!","GET_OUR_AWARD_WINNING_NEWS_APP":"Get our award-winning News App!","GET_OUR_NEWS_APP":"Get our News App!","GIVE_MORE_FEEDBACK":"\u3055\u3089\u306b\u30d5\u30a3\u30fc\u30c9\u30d0\u30c3\u30af\u3059\u308b","GO_TO_THE_RECIPE":"Go to the recipe!","GOT_A_TIP":"Got a tip?","GREAT":"Great!","HEY_BUZZFEED_COMMUNITY":"Hey BuzzFeed Community!","HOUR_AGO":"1\u6642\u9593\u524d","HOURS_AGO":"{}\u6642\u9593\u524d","JUST_NOW":"just now","LATEST":"\u6700\u65b0\u30b3\u30f3\u30c6\u30f3\u30c4","LET_US_KNOW_HOW_WE_CAN_MAKE_THE_NEW_HOMEPAGE_BETTER":"\u30db\u30fc\u30e0\u30da\u30fc\u30b8\u306e\u6539\u5584\u70b9\u3092\u304a\u805e\u304b\u305b\u304f\u3060\u3055\u3044\u3002","LIKE_US_ON":"\u3067\u3044\u3044\u306d\u3092\u62bc\u3059","LIKE_US_ON_FACEBOOK":"Facebook\u3067\u3044\u3044\u306d\u3059\u308b","LIKE_US_ON_FACEBOOK_NEWS":"","LIVE":"LIVE","LOAD_MORE":"\u3082\u3063\u3068\u8aad\u3080","LOG_IN_OR_SIGN_UP_TO_CREATE_YOUR_OWN_POSTS":"<a href=\"/signin\" data-bfa=\"@a:vertical-more;@d:login;\">Log in</a> or <a href=\"/signup\" data-bfa=\"@a:vertical-more;@d:signup;\"","LOG_IN_TO_BUZZFEED":"Log In To BuzzFeed","LOG_OUT":"Log Out","LOL":"LOL","MAKE_A_POST":"Make A Post!","MAKE_IT_YOUR_DEFAULT":"\u30c7\u30d5\u30a9\u30eb\u30c8\u306b\u3059\u308b","META_DESCRIPTION_HOME":"BuzzFeed\u306f\u3001\u30cb\u30e5\u30fc\u30b9\u901f\u5831\u3001\u92ed\u3044\u30b8\u30e3\u30fc\u30ca\u30ea\u30ba\u30e0\u3001\u30af\u30a4\u30ba\u3001\u52d5\u753b\u3001\u82b8\u80fd\u30cb\u30e5\u30fc\u30b9\u3001Tasty\u306e\u30d5\u30fc\u30c9\u52d5\u753b\u3001\u30ec\u30b7\u30d4\u3001DIY\u30cf\u30c3\u30af\u3001\u305d\u306e\u4ed6\u8a71\u984c\u306e\u30c8\u30d4\u30c3\u30af\u306a\u3069\u3001\u53cb\u4eba\u3068\u30b7\u30a7\u30a2\u3057\u305f\u304f\u306a\u308b\u30b3\u30f3\u30c6\u30f3\u30c4\u304c\u76db\u308a\u3060\u304f\u3055\u3093\u3067\u3059\u3002","META_DESCRIPTION_HOME_SPAIN":"","MINUTE_AGO":"1\u5206\u524d","MINUTES":"\u5206","MINUTES_AGO":"{}\u5206\u524d","MONTH_AGO":"1\u304b\u6708\u524d","MONTHS_AGO":"{}\u304b\u6708\u524d","MORE_PLEASE":"\u3082\u3063\u3068\u8aad\u3080","MORE":"More","MY_DRAFTS":"My Drafts","NEW_POST":"New Post","NEWS":"News","NEXT_PAGE":"Next page","OMG":"OMG","PIN":"Pin","PLAY":"\u518d\u751f","POPULAR_CATEGORIES":"Popular Categories","PREVIOUS_PAGE":"Previous page","QUICKLY_CATCH_UP":"Quickly Catch Up","QUIZZES":"\u30af\u30a4\u30ba\u30fb\u8a3a\u65ad","QUIZZES_ON_BUZZFEED":"\u3010\u30af\u30a4\u30ba\u3011\u96e3\u554f\u304b\u3089\u7c21\u5358\u306a\u8a3a\u65ad\u3001\u5b50\u4f9b\u304b\u3089\u5927\u4eba\u307e\u3067\u697d\u3057\u3081\u308b\u30af\u30a4\u30ba\u304c\u3044\u3063\u3071\u3044","READ_MORE":"\u3082\u3063\u3068\u8aad\u3080","REPORTING_TO_YOU":"Reporting To You","SEARCH":"\u691c\u7d22","SEARCH_ALL_QUIZZES":"\u5168\u3066\u306e\u30af\u30a4\u30ba\u3092\u898b\u308b","SECTIONS":"Sections","SHARE":"\u30b7\u30a7\u30a2\u3059\u308b","SIGN_UP":"\u767b\u9332","SMS":"SMS","SORRY_SOMETHING_WRONG":"Sorry! Something went wrong. Please try again.","SUBSCRIBE_TO_US_ON":"Subscribe To Us On","SUBSCRIBE_TO_OUR_RSS":"Subscribe to our RSS feed","SUPPORT_US":"Support Us","SWITCH_TO_ENGLISH":"US\u7248\u30db\u30fc\u30e0\u30da\u30fc\u30b8\u3092\u898b\u308b","SWITCH_TO_US":"Switch to US.","THANKS_FOR_YOUR_FEEDBACK":"\u30d5\u30a3\u30fc\u30c9\u30d0\u30c3\u30af\u3042\u308a\u304c\u3068\u3046\u3054\u3056\u3044\u307e\u3059\uff01","THATS_AWESOME":"\u3042\u308a\u304c\u3068\u3046\u3054\u3056\u3044\u307e\u3059\uff01","TOP_POSTS":"\u4eba\u6c17\u306e\u8a18\u4e8b","TOP_POSTS_THIS_WEEK":"\u4eca\u9031\u8a71\u984c\u306e\u8a18\u4e8b","TRENDING_NOW":"\u8a71\u984c\u306e\u8a18\u4e8b","TRENDING_NOW_SPAIN":"","TRENDING":"\u8a71\u984c\u306e\u8a18\u4e8b","TRENDING_QUIZZES":"\u8a71\u984c\u306e\u30af\u30a4\u30ba\u30fb\u8a3a\u65ad","TRENDING_VIDEOS":"\u8a71\u984c\u306e\u52d5\u753b","TRY":"\u300c{{name}}\u300d \u306e\u30af\u30a4\u30ba\u3092\u8a66\u3059","VIDEO_DURATION":"\u30d3\u30c7\u30aa\u306e\u9577\u3055","VIEW_PROFILE":"View Profile","VIEWS":"\u95b2\u89a7\u3059\u308b","WATCH":"\u898b\u308b","WATCH_IT_LIVE":"Watch it live in the Facebook App","WED_LOVE_TO_HEAR_WHAT_ELSE_YOU_HAVE_TO_SAY":"\u4ed6\u306b\u3082\u3054\u610f\u898b\u304c\u3042\u308c\u3070\u3001\u305c\u3072\u304a\u805e\u304b\u305b\u304f\u3060\u3055\u3044\u3002","WED_LOVE_TO_HEAR_WHAT_ELSE_YOU_HAVE_TO_SAY_SPAIN":"","WED_LOVE_YOUR_FEEDBACK":"We'd love your feedback!","WEEK_AGO":"1\u9031\u9593\u524d","WEEKS_AGO":"{}\u9031\u9593\u524d","WELCOME_TO_THE_NEW_BUZZFEED_HOMEPAGE":"\u65b0\u30c7\u30b6\u30a4\u30f3\u306eBuzzFeed Japan\u30db\u30fc\u30e0\u30da\u30fc\u30b8\u3078\u3088\u3046\u3053\u305d\uff01","WELCOME_TO_THE_NEW_BUZZFEED_HOMEPAGE_FEEDBACK":"\u65b0\u30c7\u30b6\u30a4\u30f3\u306eBuzzFeed Japan\u30db\u30fc\u30e0\u30da\u30fc\u30b8\u3078<br />\u3088\u3046\u3053\u305d\uff01","WERE_SORRY_TO_HEAR_THAT":"\u3054\u8ff7\u60d1\u3092\u304a\u304b\u3051\u3057\u3066\u7533\u3057\u8a33\u3042\u308a\u307e\u305b\u3093\u3002","WERE_SORRY_TO_HEAR_THAT_SPAIN":"","WHAT_DO_YOU_THINK":"\u3054\u611f\u60f3\u3092\u304a\u805e\u304b\u305b\u304f\u3060\u3055\u3044\u3002","WIN":"Win","WTF":"WTF","YEAR_AGO":"1\u5e74\u524d","YEARS_AGO":"{}\u5e74\u524d","YOUR_EMAIL":"Email address (required)"}},"name":"home","filter":null,"filters":{}}}
  };


  (function(w){
    w['bfa'] = w['bfa'] || function() {
      (w['bfa'].c = w['bfa'].c || []).push(arguments)
    };
  })(window);


  (function() {

    window.BZFD.Config.enhanced = (function() {
      if (location.search.match("nojs")) {
        return false;
      }

      
      if ('MutationObserver' in window) {

        
        if (navigator.userAgent.match(/iphone|ipad|ipod/i)) {

          
          return 'content' in document.createElement('template')
        }
        return true;

      }
    }());

    if (window.BZFD.Config.enhanced) {
      document.documentElement.classList.remove('core-ux');
      document.documentElement.classList.add('enhanced-ux');
    } else {
      
        (new Image()).src = 'https://pixiedust.buzzfeed.com/v1.gif?source=buzz_web&platform=feedpager&type=instrumentation&target=ux&value=core';
      
    }

  }());


  (function() {
    /*! loadCSS. [c]2017 Filament Group, Inc. MIT License */
    !function(a){"use strict";var b=function(b,c,d){function e(a){return h.body?a():void setTimeout(function(){e(a)})}function f(){i.addEventListener&&i.removeEventListener("load",f),i.media=d||"all"}var g,h=a.document,i=h.createElement("link");if(c)g=c;else{var j=(h.body||h.getElementsByTagName("head")[0]).childNodes;g=j[j.length-1]}var k=h.styleSheets;i.rel="stylesheet",i.href=b,i.media="only x",e(function(){g.parentNode.insertBefore(i,c?g:g.nextSibling)});var l=function(a){for(var b=i.href,c=k.length;c--;)if(k[c].href===b)return a();setTimeout(function(){l(a)})};return i.addEventListener&&i.addEventListener("load",f),i.onloadcssdefined=l,l(f),i};"undefined"!=typeof exports?exports.loadCSS=b:a.loadCSS=b}("undefined"!=typeof global?global:this);

    /*! loadCSS rel=preload polyfill. [c]2017 Filament Group, Inc. MIT License */
    !function(a){if(a.loadCSS){var b=loadCSS.relpreload={};if(b.support=function(){try{return a.document.createElement("link").relList.supports("preload")}catch(b){return!1}},b.poly=function(){for(var b=a.document.getElementsByTagName("link"),c=0;c<b.length;c++){var d=b[c];"preload"===d.rel&&"style"===d.getAttribute("as")&&(a.loadCSS(d.href,d,d.getAttribute("media")),d.rel=null)}},!b.support()){b.poly();var c=a.setInterval(b.poly,300);a.addEventListener&&a.addEventListener("load",function(){b.poly(),a.clearInterval(c)}),a.attachEvent&&a.attachEvent("onload",function(){a.clearInterval(c)})}}}(this);

    var createScript = function(options) {
      var head = document.getElementsByTagName('head')[0];
      var script = document.createElement('script');
      script.type = 'text/javascript';
      script.async = false;
      script.src = options.src;
      script.onerror = function() {
        
        
          var chunkName = options.src
            .split('/')
            .filter(function(path) { return /\.js$/.test(path); })
            .map(function(filename) { return filename.split('.')[0]; })[0];

          (new Image()).src = 'https://pixiedust.buzzfeed.com/v1.gif?source=buzz_web&platform=feedpager&type=instrumentation&target=chunk&value=timeout&tags=' + JSON.stringify({ chunk_name: chunkName });
        
      };

      if (typeof options.callback === 'function') {
        script.addEventListener('load', options.callback);
      }

      
      head.appendChild(script, head);
    };

    
    window.BZFD.Util = window.BZFD.Util || {};
    window.BZFD.Util.createScript = createScript;

  }());


  if (typeof navigator.connection !== 'undefined') {
    window.bfa('track/website/instrumentation', {
      data: {
        target: 'network_api',
        value: 'enabled',
        tags: {
          effective_type: navigator.connection.effectiveType
        }
      },
    });
  }


  (function(a,c,d,e){if(!a[c]){var b=a[c]={};b[d]=[];b[e]=function(a){b[d].push(a)}}})(window,'Scroll','_q','do');
  Scroll.config = {
    detected: document.cookie.indexOf("scroll0=") > -1
  };

{"adPos": "awareness", "adType": "awareness", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[970, 90], [320, 50], [5, 5], [728, 90], [970, 250], "fluid"], "targeting": {"pos": ["awareness"], "wid": 42}, "trackingData": {}, "viewability": "low", "wid": 42}

    {"adPos": "pixel", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[1, 1]], "targeting": {"pos": ["pixel"], "wid": 0}, "trackingData": {}, "viewability": "low", "wid": 0}
  

      window.BZFD = window.BZFD || {};
      window.BZFD.__HEADER_STATE__ = {"theme":"light","brand":"bfo","edition":"jp","showBadges":true,"config":{"bf_url":"https://www.buzzfeed.com","brand_urls":{"asis":"https://www.buzzfeed.com/asis","bfo":"https://www.buzzfeed.com","bringme":"https://www.buzzfeed.com/jp/badge/bringmejapan","goodful":"https://www.buzzfeed.com/goodful","news":"https://www.buzzfeed.com/news","nifty":"https://www.buzzfeed.com/nifty","adobe":"https://www.buzzfeed.com/makethefeed","lgbtq":"https://www.buzzfeed.com/lgbtq"},"cms_url":"https://cms.buzzfeed.com","community_url":"https://community.buzzfeed.com","contributors_url":"https://contributors.buzzfeed.com","dashbird_url":"https://dashbird.buzzfeed.io","dashbird_community_url":"https://community-dashbird.buzzfeed.com","image_service_url":"https://img.buzzfeed.com/buzzfeed-static","new_post_path":"/post","settings_path":"/settings","ga":"ga"},"navItems":{"topics":[{"url":"/jp/news","name":"News"},{"url":"https://www.buzzfeed.com/jp/badge/lifejp","name":"特集"},{"url":"/jp/videos","name":"動画"},{"url":"/jp/shopping","name":"お買い物"},{"url":"/jp/tastyjapan","name":"Tasty"},{"url":"/jp/quizzes","name":"クイズ・診断"}],"destinations":[{"url":"/jp/news","name":"bfn","label":"bfnews","description":"Reporting on what you care about. We hold major institutions accountable and expose wrongdoing."},{"url":"/jp/tastyjapan","name":"tasty","description":"Search, watch, and cook every single Tasty recipe and video ever - all in one place!"}],"badges":[{"name":"lol","url":"/jp/lol"},{"name":"wtf","url":"/jp/wtf"},{"name":"omg","url":"/jp/omg"},{"name":"kawaii","url":"/jp/badge/kawaii","label":"cute"},{"name":"trending","url":"/jp/trending"}],"about":[{"url":"/about","name":"会社情報","label":"About"},{"url":"/about/jobs","name":"採用情報","label":"Jobs"},{"url":"https://bzfd.it/2LP9eNo","name":"Merch","label":"merch"},{"url":"/newsletters?origin=nav","name":"Newsletters"}],"footer":[{"url":"/press","name":"プレスリリース","label":"Press"},{"url":"/rss","name":"RSS"},{"url":"/about/privacy","name":"プライバシーポリシー","label":"Privacy"},{"url":"/consent-preferences","name":"Consent Preferences"},{"url":"/about/useragreement","name":"ユーザー規約","label":"User Agreement"},{"url":"/about/privacy#adchoices","name":"Ad Choices"},{"url":"/help","name":"Help"},{"url":"/about/contact","name":"お問い合わせ","label":"Contact"},{"url":"/archive","name":"Sitemap"}],"trendingTopics":[]},"i18n":{"about":"会社情報","edition":"Edition","or":"または","sign_up":"サインアップ","log_in":"ログイン","browse_sections":"Browse Sections","browse_brands":"Browse Brands","view_profile":"プロフィールを見る","settings":"Settings","new_post":"New Post","my_drafts":"My Drafts","dashboard":"Dashboard","logout":"ログアウト","search":"検索 BuzzFeed","more_buzzfeed_brands":"more BuzzFeed brands","buzzfeed_badges":"BuzzFeed badges","hot_topics":"Hot Topics","skip_to_content":"スキップ","useful_information":"useful information","hamburger":"open menu to see more links","a11y_search":"open form to search"}};
    

    {
      "enabled_fe": false
    }
  

      {
        "feedName": "home",
        "feedParams": {},
        "flexproEnabled": "1",
        "ads": {"density": 7, "placements": [4, 8, 14], "units": [{"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story1", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story1"], "wid": 1}, "trackingData": {}, "viewability": "low", "wid": 1}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story2", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story2"], "wid": 2}, "trackingData": {}, "viewability": "low", "wid": 2}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story3", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story3"], "wid": 3}, "trackingData": {}, "viewability": "low", "wid": 3}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story4", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story4"], "wid": 4}, "trackingData": {}, "viewability": "low", "wid": 4}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story5", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story5"], "wid": 5}, "trackingData": {}, "viewability": "low", "wid": 5}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story6", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story6"], "wid": 6}, "trackingData": {}, "viewability": "low", "wid": 6}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story7", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story7"], "wid": 7}, "trackingData": {}, "viewability": "low", "wid": 7}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story8", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story8"], "wid": 8}, "trackingData": {}, "viewability": "low", "wid": 8}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story9", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story9"], "wid": 9}, "trackingData": {}, "viewability": "high", "wid": 9}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story10", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story10"], "wid": 11}, "trackingData": {}, "viewability": "low", "wid": 11}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story11", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story11"], "wid": 12}, "trackingData": {}, "viewability": "high", "wid": 12}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story12", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story12"], "wid": 16}, "trackingData": {}, "viewability": "low", "wid": 16}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story13", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story13"], "wid": 17}, "trackingData": {}, "viewability": "high", "wid": 17}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story14", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story14"], "wid": 18}, "trackingData": {}, "viewability": "high", "wid": 18}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story15", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story15"], "wid": 19}, "trackingData": {}, "viewability": "high", "wid": 19}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story16", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story16"], "wid": 20}, "trackingData": {}, "viewability": "high", "wid": 20}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story17", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story17"], "wid": 21}, "trackingData": {}, "viewability": "high", "wid": 21}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story18", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story18"], "wid": 22}, "trackingData": {}, "viewability": "high", "wid": 22}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story19", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story19"], "wid": 23}, "trackingData": {}, "viewability": "high", "wid": 23}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story20", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story20"], "wid": 24}, "trackingData": {}, "viewability": "high", "wid": 24}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story21", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story21"], "wid": 25}, "trackingData": {}, "viewability": "high", "wid": 25}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story22", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story22"], "wid": 28}, "trackingData": {}, "viewability": "high", "wid": 28}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story23", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story23"], "wid": 29}, "trackingData": {}, "viewability": "high", "wid": 29}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story24", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story24"], "wid": 30}, "trackingData": {}, "viewability": "high", "wid": 30}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story25", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story25"], "wid": 31}, "trackingData": {}, "viewability": "high", "wid": 31}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story26", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story26"], "wid": 32}, "trackingData": {}, "viewability": "low", "wid": 32}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story27", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story27"], "wid": 33}, "trackingData": {}, "viewability": "high", "wid": 33}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story28", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story28"], "wid": 34}, "trackingData": {}, "viewability": "high", "wid": 34}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story29", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story29"], "wid": 35}, "trackingData": {}, "viewability": "high", "wid": 35}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story30", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story30"], "wid": 36}, "trackingData": {}, "viewability": "low", "wid": 36}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story31", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story31"], "wid": 37}, "trackingData": {}, "viewability": "low", "wid": 37}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story32", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story32"], "wid": 38}, "trackingData": {}, "viewability": "low", "wid": 38}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story33", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story33"], "wid": 39}, "trackingData": {}, "viewability": "low", "wid": 39}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story34", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story34"], "wid": 40}, "trackingData": {}, "viewability": "low", "wid": 40}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story35", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story35"], "wid": 41}, "trackingData": {}, "viewability": "low", "wid": 41}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story36", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story36"], "wid": 43}, "trackingData": {}, "viewability": "low", "wid": 43}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story37", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story37"], "wid": 44}, "trackingData": {}, "viewability": "low", "wid": 44}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story38", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story38"], "wid": 50}, "trackingData": {}, "viewability": "high", "wid": 50}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story39", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story39"], "wid": 51}, "trackingData": {}, "viewability": "high", "wid": 51}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "story40", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[320, 50], [5, 5], [728, 90], "fluid", [300, 250]], "targeting": {"pos": ["story40"], "wid": 52}, "trackingData": {}, "viewability": "high", "wid": 52}, "with_companions": false}], "unitsRepeated": []},
        "hasNextPage": true
      }
    

    
      {"filter":"default","feedLoadedMsg":"feed-ready-for-ads--default-mod-feed-cards-1","density":7,"placements":[4,8,14],"units":[{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story1","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story1"],"wid":1},"trackingData":{},"viewability":"low","wid":1},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story2","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story2"],"wid":2},"trackingData":{},"viewability":"low","wid":2},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story3","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story3"],"wid":3},"trackingData":{},"viewability":"low","wid":3},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story4","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story4"],"wid":4},"trackingData":{},"viewability":"low","wid":4},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story5","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story5"],"wid":5},"trackingData":{},"viewability":"low","wid":5},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story6","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story6"],"wid":6},"trackingData":{},"viewability":"low","wid":6},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story7","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story7"],"wid":7},"trackingData":{},"viewability":"low","wid":7},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story8","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story8"],"wid":8},"trackingData":{},"viewability":"low","wid":8},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story9","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story9"],"wid":9},"trackingData":{},"viewability":"high","wid":9},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story10","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story10"],"wid":11},"trackingData":{},"viewability":"low","wid":11},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story11","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story11"],"wid":12},"trackingData":{},"viewability":"high","wid":12},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story12","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story12"],"wid":16},"trackingData":{},"viewability":"low","wid":16},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story13","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story13"],"wid":17},"trackingData":{},"viewability":"high","wid":17},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story14","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story14"],"wid":18},"trackingData":{},"viewability":"high","wid":18},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story15","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story15"],"wid":19},"trackingData":{},"viewability":"high","wid":19},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story16","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story16"],"wid":20},"trackingData":{},"viewability":"high","wid":20},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story17","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story17"],"wid":21},"trackingData":{},"viewability":"high","wid":21},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story18","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story18"],"wid":22},"trackingData":{},"viewability":"high","wid":22},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story19","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story19"],"wid":23},"trackingData":{},"viewability":"high","wid":23},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story20","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story20"],"wid":24},"trackingData":{},"viewability":"high","wid":24},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story21","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story21"],"wid":25},"trackingData":{},"viewability":"high","wid":25},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story22","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story22"],"wid":28},"trackingData":{},"viewability":"high","wid":28},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story23","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story23"],"wid":29},"trackingData":{},"viewability":"high","wid":29},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story24","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story24"],"wid":30},"trackingData":{},"viewability":"high","wid":30},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story25","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story25"],"wid":31},"trackingData":{},"viewability":"high","wid":31},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story26","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story26"],"wid":32},"trackingData":{},"viewability":"low","wid":32},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story27","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story27"],"wid":33},"trackingData":{},"viewability":"high","wid":33},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story28","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story28"],"wid":34},"trackingData":{},"viewability":"high","wid":34},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story29","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story29"],"wid":35},"trackingData":{},"viewability":"high","wid":35},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story30","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story30"],"wid":36},"trackingData":{},"viewability":"low","wid":36},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story31","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story31"],"wid":37},"trackingData":{},"viewability":"low","wid":37},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story32","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story32"],"wid":38},"trackingData":{},"viewability":"low","wid":38},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story33","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story33"],"wid":39},"trackingData":{},"viewability":"low","wid":39},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story34","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story34"],"wid":40},"trackingData":{},"viewability":"low","wid":40},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story35","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story35"],"wid":41},"trackingData":{},"viewability":"low","wid":41},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story36","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story36"],"wid":43},"trackingData":{},"viewability":"low","wid":43},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story37","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story37"],"wid":44},"trackingData":{},"viewability":"low","wid":44},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story38","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story38"],"wid":50},"trackingData":{},"viewability":"high","wid":50},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story39","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story39"],"wid":51},"trackingData":{},"viewability":"high","wid":51},"with_companions":false},{"companions":[],"is_enabled":true,"page":"home","slot":{"adPos":"story40","adType":"post","isInfinite":false,"platform":null,"position":null,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story40"],"wid":52},"trackingData":{},"viewability":"high","wid":52},"with_companions":false}],"unitsRepeated":[]}
    
  
{"throttle_timeout": 0,"render_lookahead": 1000}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5946273",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5948441",
      "show_new_labels": false
    }
  
{"adPos":"story1","adType":"post","isInfinite":true,"platform":null,"position":4,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story1"],"wid":"1-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"1-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5946376",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5950911",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949284",
      "show_new_labels": false
    }
  
{"adPos":"story2","adType":"post","isInfinite":true,"platform":null,"position":8,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story2"],"wid":"2-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"2-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5939286",
      "show_new_labels": false
    }
  

    {
      "id": "132216"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953874",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958113",
      "show_new_labels": false
    }
  
{"adPos":"story3","adType":"post","isInfinite":true,"platform":null,"position":14,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story3"],"wid":"3-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"3-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5897746",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5924468",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5941283",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5931564",
      "show_new_labels": false
    }
  

    {
      "id": "131651"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5951854",
      "show_new_labels": false
    }
  
{"adPos":"story4","adType":"post","isInfinite":true,"platform":null,"position":21,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story4"],"wid":"4-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"4-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955988",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5959206",
      "show_new_labels": false
    }
  

    {
      "renderLookahead": -300
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949623",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5959283",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5950862",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955822",
      "show_new_labels": false
    }
  
{"adPos":"story5","adType":"post","isInfinite":true,"platform":null,"position":28,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story5"],"wid":"5-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"5-1"}

    {
      "id": "131307"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957142",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953755",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953822",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5952876",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957069",
      "show_new_labels": false
    }
  

    {
      "renderLookahead": -300
    }
  
{"adPos":"story6","adType":"post","isInfinite":true,"platform":null,"position":35,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story6"],"wid":"6-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"6-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5951847",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953893",
      "show_new_labels": false
    }
  

    {
      "id": "131642"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5959243",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5927742",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955882",
      "show_new_labels": false
    }
  
{"adPos":"story7","adType":"post","isInfinite":true,"platform":null,"position":42,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story7"],"wid":"7-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"7-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953816",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958227",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5956965",
      "show_new_labels": false
    }
  

    {
      "renderLookahead": -300
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5954618",
      "show_new_labels": false
    }
  

    {
      "id": "130912"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5952953",
      "show_new_labels": false
    }
  
{"adPos":"story8","adType":"post","isInfinite":true,"platform":null,"position":49,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story8"],"wid":"8-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"8-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5956021",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955763",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953788",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953857",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953795",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955776",
      "show_new_labels": false
    }
  
{"adPos":"story9","adType":"post","isInfinite":true,"platform":null,"position":56,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story9"],"wid":"9-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"9-1"}

    {
      "id": "130510"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5959152",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953770",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5950531",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957015",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958303",
      "show_new_labels": false
    }
  
{"adPos":"story10","adType":"post","isInfinite":true,"platform":null,"position":63,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story10"],"wid":"11-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"11-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953216",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5951862",
      "show_new_labels": false
    }
  

    {
      "id": "131203"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953875",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5933615",
      "show_new_labels": false
    }
  

    {
      "renderLookahead": -300
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5952021",
      "show_new_labels": false
    }
  
{"adPos":"story11","adType":"post","isInfinite":true,"platform":null,"position":70,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story11"],"wid":"12-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"12-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5954565",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5939299",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955228",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949833",
      "show_new_labels": false
    }
  

    {
      "id": "130785"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953944",
      "show_new_labels": false
    }
  
{"adPos":"story12","adType":"post","isInfinite":true,"platform":null,"position":77,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story12"],"wid":"16-1","infinite_index":1},"trackingData":{},"viewability":"low","wid":"16-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955934",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953152",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5951817",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958093",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5954645",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958217",
      "show_new_labels": false
    }
  
{"adPos":"story13","adType":"post","isInfinite":true,"platform":null,"position":84,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story13"],"wid":"17-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"17-1"}

    {
      "id": "130922"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5950521",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955978",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5946551",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955997",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5950713",
      "show_new_labels": false
    }
  
{"adPos":"story14","adType":"post","isInfinite":true,"platform":null,"position":91,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story14"],"wid":"18-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"18-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957284",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5931398",
      "show_new_labels": false
    }
  

    {
      "renderLookahead": -300
    }
  

    {
      "id": "130516"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957029",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949778",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5952880",
      "show_new_labels": false
    }
  
{"adPos":"story15","adType":"post","isInfinite":true,"platform":null,"position":98,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story15"],"wid":"19-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"19-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5958122",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5954670",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5946493",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5952960",
      "show_new_labels": false
    }
  

    {
      "id": "130497"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5938177",
      "show_new_labels": false
    }
  
{"adPos":"story16","adType":"post","isInfinite":true,"platform":null,"position":105,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story16"],"wid":"20-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"20-1"}

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5955889",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949754",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5956962",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953919",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5957060",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949576",
      "show_new_labels": false
    }
  
{"adPos":"story17","adType":"post","isInfinite":true,"platform":null,"position":112,"renderLookahead":"x0.25","size":[[320,50],[5,5],[728,90],"fluid",[300,250]],"targeting":{"pos":["story17"],"wid":"21-1","infinite_index":1},"trackingData":{},"viewability":"high","wid":"21-1"}

    {
      "id": "129588"
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5956131",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5953864",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5945522",
      "show_new_labels": false
    }
  

    {
      "throttle_timeout": 0 ,
      "render_lookahead": 1000,
      "id": "5949153",
      "show_new_labels": false
    }
  

    { "ads": {"density": 0, "placements": [4], "units": [{"companions": [], "idx_in_parent": 4, "is_enabled": true, "page": "home", "slot": {"adPos": "promo1", "adType": "ex", "isInfinite": false, "platform": "desktop", "position": null, "renderLookahead": "x0.25", "size": [[300, 600], "fluid", [300, 250]], "targeting": {"pos": ["promo1"], "wid": 230}, "trackingData": {}, "viewability": "low", "wid": 230}, "with_companions": false}], "unitsRepeated": []} }
  

    {"adPos": "bigstory", "adType": "post", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[300, 600], "fluid", [5, 5], [300, 250]], "targeting": {"pos": ["bigstory"], "wid": 13}, "trackingData": {}, "viewability": "low", "wid": 13}
  

    {
    "color": "pink",
    "imageCrop": "wide",
    "loadLarge": true,
    "loadMedium": true,
    "loadSmall": false,
    "loadXsmall": false,
    "pixiedust": {
        "position_in_unit": 2,
        "subunit_name": "trending_now",
        "subunit_type": "package",
        "unit_name": "right",
        "unit_type": "sidebar"
    },
    "showImage": true,
    "showNumber": true,
    "title": "\u8a71\u984c\u306e\u8a18\u4e8b",
    "titleIcon": "trending-icon",
    "unit": "trending",
    "unitName": "sidebar/trending",
    "unitType": "list"
}
    

    {
    "color": "purple",
    "imageCrop": "wide",
    "loadAds": true,
    "loadLarge": true,
    "loadMedium": true,
    "loadSmall": false,
    "loadXsmall": false,
    "pageSize": 40,
    "pixiedust": {
        "position_in_unit": 5,
        "subunit_name": "top_posts",
        "subunit_type": "package",
        "unit_name": "right",
        "unit_type": "sidebar"
    },
    "showImage": true,
    "showNumber": false,
    "title": "\u4eba\u6c17\u306e\u8a18\u4e8b",
    "unit": "morebuzz",
    "unitName": "sidebar/morebuzz",
    "unitType": "list"
}
    

    
      
      {
        
        
        

        
          "units": [{"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "promo4", "adType": "ex", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[300, 600], "fluid", [300, 250]], "targeting": {"pos": ["promo4"], "wid": 233}, "trackingData": {}, "viewability": "low", "wid": 233}, "with_companions": false}, {"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "promo5", "adType": "ex", "isInfinite": false, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[300, 600], "fluid", [300, 250]], "targeting": {"pos": ["promo5"], "wid": 234}, "trackingData": {}, "viewability": "low", "wid": 234}, "with_companions": false}],
        
      
        
        
        

        
      
        
        
        

        
      
        
        
        

        
      
        
        
        

        
      

        
        
        

        
          "unitsRepeated": [{"companions": [], "is_enabled": true, "page": "home", "slot": {"adPos": "promo-infinite", "adType": "ex", "isInfinite": true, "platform": null, "position": null, "renderLookahead": "x0.25", "size": [[300, 600], "fluid", [300, 250]], "targeting": {"pos": ["promo-infinite"], "wid": 2300}, "trackingData": {}, "viewability": "high", "wid": 2300}, "with_companions": false}],
        
      
        
        
        

        
      
        
        
        

        
      
        
        
        

        
      
        
        
        

        
      

        "density": 5,
        "placements": []
      }
    
  

  (function() {
    if (!window.BZFD.Config.enhanced) {
      
      window.BZFD.Util.createScript({
          src: "/static-assets/js/vendor.92f314e133d4e50b7a4d.js"
      });
    }

    
    window.BZFD.Util.createScript({
      src: "/static-assets/js/bfa.58f2533721f39f70654e.js"
    });

  }());


var linkback = linkback|| {};
(function() {
    var d = document, scr = d.createElement('script'), pro = d.location.protocol,
    tar = d.getElementsByTagName('head')[0];
    scr.type = 'text/javascript';  scr.async = true;
    scr.src = ((pro === 'https:') ? 'https' : 'http') + '://linkback.contentsfeed.com/src/lb4buzzf.min.js';
    scr.charset='utf-8';
    if(!linkback.l){linkback.l=true; tar.insertBefore(scr, tar.firstChild);}
})();
