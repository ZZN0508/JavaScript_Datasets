var event = new Object();event.type ='1stparty-sociodem';event.age ='';event.gender ='';var opeCustomEvents = [event];


  function handleMeteringSuccess(response)
  {
    var DincamicCookie = JSON.parse(atob(Cookies.get('iduser')));
    DincamicCookie['userType'] = getUserTypeEvolok(response);
    DincamicCookie['userSegment'] = getUserSegmentEvolok(response);
    Cookies.set('iduser', btoa(JSON.stringify(DincamicCookie)), {path: '/', expires: 365, domain: '.hola.com' });
  }

  function getUserTypeEvolok(response)
  {
    var userType="guest";
    if (response.segments.filter(segment => segment === 'subscriber').length) {
      userType = 'subscriber';
    }
    else if (response.segments.filter(segment => segment === 'verified').length && response.segments.filter(segment => segment === 'known_user').length) {
      userType = 'registered';
    }

    return userType;
  }

  function getUserSegmentEvolok(response)
  {
    var userSegment = '';
    if (typeof response.segments != "undefined" && response.segments.length > 0){
      userSegment = response.segments;
    }

    return userSegment;
  }

  function handleMeteringError(error)
  {
    console.log('error', error);
  }

  EV.Em.init({
            url: 'https://hol.evolok.net/acd/api/3.0',
        sidCookieDomain: '.hola.com',
    brand: 'hola',
  });

  EV.Em.authorize('{"articleId":"","section":"","subSection":"","isPremium":false,"geo":"es"}', handleMeteringSuccess, handleMeteringError);


        _atrk_opts = { atrk_acct:"XbAUn1QolK10cv", domain:"hola.com",dynamic: true};
        (function() {
        var as = document.createElement('script');
        as.type = 'text/javascript';
        as.async = true;
                    as.src = "https://d31qbv1cthcecs.cloudfront.net/atrk.js";
                var s = document.getElementsByTagName('script')[0];
        s.parentNode.insertBefore(as, s);
    })();



    var _sf_async_config = _sf_async_config || {};

    _sf_async_config.uid = 51448;
    _sf_async_config.domain = 'hola.com';
    _sf_async_config.flickerControl = false;
    _sf_async_config.useCanonical = true;
    _sf_async_config.useCanonicalDomain = true;


    window._adftrack = Array.isArray(window._adftrack) ? window._adftrack : (window._adftrack ? [window._adftrack] : []);
    window._adftrack.push({
        pm: 1511358,
        divider: encodeURIComponent('|'),
        pagename: encodeURIComponent('HOLA'),
        order :
            { sv1: 'https://www.hola.com/' }
    });

    (function ()
        { var s = document.createElement('script'); s.type = 'text/javascript'; s.async = true; s.src = 'https://track.adform.net/serving/scripts/trackpoint/async/'; var x = document.getElementsByTagName('script')[0]; x.parentNode.insertBefore(s, x); }
    )();


    function loadScript(url) {
        var script = document.createElement('script');
        script.src = url;
        script.type = "application/javascript";
        script.onload = function () {

        };

        document.head.appendChild(script);
    }
    loadScript("//www.hola.com/js/comunes/outbrain.js?v3");


    var _prum = [['id', '5857a621aa69593849b95df8'],
        ['mark', 'firstbyte', (new Date()).getTime()]];
    (function() {
        var s = document.getElementsByTagName('script')[0]
                , p = document.createElement('script');
        p.async = 'async';
        p.src = '//rum-static.pingdom.net/prum.min.js';
        s.parentNode.insertBefore(p, s);
    })();


window._tfa = window._tfa || [];
window._tfa.push(

{notify: 'event', name: 'page_view', id: 1191390}
);
!function (t, f, a, x) {
if (!document.getElementById)

{ t.async = 1;t.src = a;t.id=x;f.parentNode.insertBefore(t, f); }
}(document.createElement('script'),
document.getElementsByTagName('script')[0],
'//cdn.taboola.com/libtrc/unip/1191390/tfa.js',
'tb_tfa_script');


  !function(n,e,i){if(!n){n=n||{},window.permutive=n,n.q=[],n.config=i||{},n.config.apiKey=e,n.config.environment=n.config.environment||"production";for(var o=["addon","identify","track","trigger","query","segment","segments","ready","on","once","user","consent"],r=0;r<o.length;r++){var t=o[r];n[t]=function(e){return function(){var i=Array.prototype.slice.call(arguments,0);n.q.push({functionName:e,arguments:i})}}(t)}}}(window.permutive,"c17156dc-7d81-4b5c-b28a-0c3766c9247d");
  window.googletag=window.googletag||{},window.googletag.cmd=window.googletag.cmd||[],window.googletag.cmd.push(function(){if(0===window.googletag.pubads().getTargeting("permutive").length){var g=window.localStorage.getItem("_pdfps");window.googletag.pubads().setTargeting("permutive",g?JSON.parse(g):[])}});

    permutive.addon('web', {
      page: {
        type: "home",
        documentType: "home",
        publication: "Hola ES",
        content: {
          categories: ["home"],
          subsection: [""],
          type: ""
        },
        classifications_watson: {
            concepts: "$alchemy_concepts",
            entities: "$alchemy_entities",
            keywords: "$alchemy_keywords",
            taxonomy: "$alchemy_taxonomy",
            emotion: "$alchemy_document_emotion",
            sentiment: "$alchemy_document_sentiment"
        }
      }
    });



  var idsLoaded = false;

  // initialize pbjs
  var pbjs = pbjs || {};
  pbjs.que = pbjs.que || [];

  // setup googletag
  var googletag = googletag || {};
  googletag.cmd = googletag.cmd || [];

  var adslot0, adslot1, adslot2, adslot3, adslot4;
  googletag.cmd.push(function() {

    googletag.pubads().disableInitialLoad();
    googletag.pubads().enableSingleRequest();
    googletag.enableServices();

    var mapping1 = googletag.sizeMapping().addSize([0,0], [[2,1],[300,100],[300,75],[320,50],[320,100],[320,480]]).addSize([728,0], [[2,1],[468,60],[728,90],[728,200]]).addSize([980,0], [[2,1],[970,90],[970,250],[728,90],[980,250],[980,90]]).build();

var mapping2 = googletag.sizeMapping().addSize([0,0], [[120,600],[200,200],[250,250],[300,250],[300,600],[320,50],[320,100],[320,480],[300,100],[300,75]]).addSize([728,0], [[728,90],[728,200],[468,60],[300,250],[300,600],[250,250],[200,200],[120,600]]).addSize([980,0], [[980,250],[980,90],[970,90],[970,250],[728,90]]).build();

var mapping3 = googletag.sizeMapping().addSize([0,0], []).addSize([970,0], [[2,1],[1,2]]).build();

var dm_mapping = {
	'mapping1': [
		{ minViewPort: [0,0], sizes: [[2,1],[300,100],[300,75],[320,50],[320,100],[320,480]]},
		{ minViewPort: [728,0], sizes: [[2,1],[468,60],[728,90],[728,200]]},
		{ minViewPort: [980,0], sizes: [[2,1],[970,90],[970,250],[728,90],[980,250],[980,90]]}
	],
	'mapping2': [
		{ minViewPort: [0,0], sizes: [[120,600],[200,200],[250,250],[300,250],[300,600],[320,50],[320,100],[320,480],[300,100],[300,75]]},
		{ minViewPort: [728,0], sizes: [[728,90],[728,200],[468,60],[300,250],[300,600],[250,250],[200,200],[120,600]]},
		{ minViewPort: [980,0], sizes: [[980,250],[980,90],[970,90],[970,250],[728,90]]}
	],
	'mapping3': [
		{ minViewPort: [0,0], sizes: []},
		{ minViewPort: [970,0], sizes: [[2,1],[1,2]]}
	]
};

adslot0 = googletag.defineOutOfPageSlot('/87824813/hola/home', 'div-hola-slot-outofpage1x1').
		setTargeting('position','outofpage1x1').
		setCollapseEmptyDiv(true).
		addService(googletag.pubads());

	adslot1 = googletag.defineSlot('/87824813/hola/home', [[980,250],[980,90],[970,250],[970,90],[728,200],[728,90],[468,60],[320,480],[320,100],[320,50],[300,100],[300,75],[2,1]], 'div-hola-slot-megabanner').
		setTargeting('position','megabanner').
		setTargeting('place','ATF').
		setCollapseEmptyDiv(true).
		defineSizeMapping(mapping1).
		addService(googletag.pubads());

	adslot2 = googletag.defineSlot('/87824813/hola/home', [[120,600],[160,600],[200,200],[250,250],[300,250],[300,600],[336,280]], 'div-hola-slot-robapaginas').
		setTargeting('position','robapaginas').
		setTargeting('place','ATF').
		setCollapseEmptyDiv(true).
		addService(googletag.pubads());

	adslot3 = googletag.defineSlot('/87824813/hola/home', ["fluid",[120,600],[160,600],[200,200],[250,250],[300,250],[300,600],[336,280]], 'div-hola-slot-robainferior').
		setTargeting('position','robainferior').
		setTargeting('place','BTF').
		setCollapseEmptyDiv(true).
		addService(googletag.pubads());

	adslot4 = googletag.defineSlot('/87824813/hola/home', [[980,250],[980,90],[970,250],[970,90],[728,200],[728,90],[468,60],[300,600],[320,480],[300,250],[300,100],[300,75],[320,100],[320,50],[250,250],[200,200],[120,600]], 'div-hola-slot-bannerinferior').
		setTargeting('position','bannerinferior').
		setTargeting('place','BTF').
		setCollapseEmptyDiv(true).
		defineSizeMapping(mapping2).
		addService(googletag.pubads());


    // function that calls the ad-server
    function callAdserver(gptSlots) {
      if (pbjs.adserverCalled) return;
      pbjs.adserverCalled = true;
      googletag.pubads().refresh(gptSlots);
    }

    var started = Date.now();
    var control = false;

    // make it loop every 50 milliseconds, until idsLoaded or after 2 seconds
    var interval = setInterval(function(){
      if (Date.now() - started > 2000 || control === true) {
        clearInterval(interval);
      } else {
        if (idsLoaded === true) {
          // request pbjs bids when it loads
          console.log("Calling to pbjs..");
          pbjs.que.push(function() {
            pbjs.rp.requestBids({
              callback: callAdserver,
              gptSlotObjects: [adslot0, adslot1, adslot2, adslot3, adslot4],
              //data: <optional_first_party_data_object>,
              sizeMappings: dm_mapping
            });
          });
          control = true;
        }
      }
    }, 50); // Check every 100 milliseconds



            googletag.pubads().addEventListener( 'slotRenderEnded', function(event) {
          if (!event.isEmpty && typeof dataLayer === "object") {
            dataLayer.push({
              'event': 'adhit',
              'eventAction': 'campaignid',
              'eventCategory': 'ad',
              'eventLabel': event.campaignId
            });
          }
        });
    
      // failsafe in case PBJS doesn't load
      setTimeout(function() {
          callAdserver([adslot0, adslot1, adslot2, adslot3, adslot4]);
      }, 3500);

  });


  var pub = "hola";
  var positions = {"OOP":true,"SKIN":false,"TOP":true,"MPU":true,"MPU2":true,"TOP2":true,"NAT":false,"IMG":false};
  var totalSlots = 8;
  var adUnit = "/87824813/hola/home";
    var isGallery = false;
  

  $(function() {

    var datosUsuario = {
      type: "guest"
    };

    if (Cookies.get(window.nameCookie) !== undefined) {

      var myCookie = JSON.parse(atob(Cookies.get(window.nameCookie)));

        datosUsuario.type = myCookie.userType;

      if (myCookie['genderUser'])
        datosUsuario.gender = (myCookie['genderUser'] === "H") ? "M" : "F";

      if (myCookie['ageUser'])
        datosUsuario.age = myCookie['ageUser'];
    }

    permutive.track("User", datosUsuario);

  });

(window.BOOMR_mq=window.BOOMR_mq||[]).push(["addVar",{"rua.upush":"false","rua.cpush":"false","rua.upre":"false","rua.cpre":"false","rua.uprl":"false","rua.cprl":"false","rua.cprf":"false","rua.trans":"","rua.cook":"false","rua.ims":"false","rua.ufprl":"false","rua.cfprl":"false","rua.isuxp":"","rua.texp":""}]);

        // Check and set vendors cookie to request in another tools. This code only run in already accepted consents.
        window.didomiOnReady = window.didomiOnReady || [];
        window.didomiOnReady.push(function (Didomi) {
          if (Didomi.isConsentRequired()) {
            // Consent is required: your visitor is from the EU or you are an EU company
            // Only enable the vendor when consent is given
            Didomi.getObservableOnUserConsentStatusForVendor('77') //Vendor = 77 is Comscore
              .subscribe(function (consentStatusForVendor) { // The consent status for the vendor has changed
                if (consentStatusForVendor === undefined) { // The vendor does not have consent
                  // The consent status for the vendor is unknown
                  document.cookie = "vendorconsents=; max-age=0; path=/; domain=.hola.com";
                } else {//} if (consentStatusForVendor === true) {
                  const currentDidomi = Didomi.getUserConsentStatusForAll();
                  const allowedVendors = [77,];
                  let vendorsEnabled = [];
                  let x = 0;
                  for(let i = 0; i < allowedVendors.length; i++) {
                    if (currentDidomi.vendors.enabled.includes(allowedVendors[i])) {
                      vendorsEnabled[x] = allowedVendors[i];
                      x++;
                    }
                  }
                  Cookies.set('vendorconsents', btoa(JSON.stringify(vendorsEnabled)), {
                    path: '/',
                    expires: 365,
                    domain: '.hola.com'
                  });
                }
              });
          } else { // Consent is not required, enable your vendor immediately
            document.cookie = "vendorconsents=; max-age=0; path=/; domain=.hola.com";
          }
        });
    
 dataLayer = [{"publication":"ES","countryEdition":"España","subdomain":"www","ageUser":"","extension":"","ageRange":"","comscoreGroup":"","editorialGroup":"hola actualidad","searchType":"","searchKeywords":"","contentType":"","section":"portada","subsection":"portada/portada","author":"","documentType":"portada","sourceUser":"","idUserA":"","idUser":"","genderUser":"","login":"no","dispositivo":"","wildCard":"","promocion":"","idUserB":"","ageUserB":"","ageRangeB":"","genderUserB":"","sourceUserB":"","userType":"guest","userSegment":"","contentPaidType":"free"}]


    // Begin Check vendorConsent cookie
  var cs_ucfr = '';
  function getCmpVendorsCookie(name) {
    let value = ';' + document.cookie;
    value = value.replace(/\s+/gm,'');
    const parts = value.split(';' + name + '=');

    return (parts.length === 2) ? parts.pop().split(";").shift() : null;
  }

  var vendorConsentsValue = getCmpVendorsCookie('vendorconsents');
  if(vendorConsentsValue !== null) {
    const vendorConsents = JSON.parse(atob(vendorConsentsValue));
    const comscoreExists = vendorConsents.includes(77);
    cs_ucfr = (typeof vendorConsents === 'object' && comscoreExists) ? 1 : 0;
  }
  // End Check vendorConsent cookie

  var _comscore = _comscore || [];
  var x =({ c1: "2", c2: "6035866",options:{url_append:"comscorekw=spain"}});
  x.cs_ucfr = cs_ucfr;

  _comscore.push(x);
  (function() {
    var s = document.createElement("script"), el = document.getElementsByTagName("script")[0]; s.async = true;
    s.src = (document.location.protocol == "https:" ? "https://sb" : "http://b") + ".scorecardresearch.com/cs/6035866/beacon.js";
    el.parentNode.insertBefore(s, el);
  })();

    (function() {
      if(typeof(dataLayer)=="object"){
          dataLayer.push({event: 'keyword_comscore',eventCategory: 'keyword_comscore',eventAction: 'keyword',eventLabel: 'spain'});
      }
  })();
  

if($(window).width()<=768){
	$( "#firstCol" ).append( $( "aside[role='complementary'] .promohola" ) );
	//if($( ".teletipo" ).html())$( ".content.box" ).prepend( $( ".teletipo" ) );
	$( '#secondaryBar [data-layer-location]').insertAfter('.subsNews').css('display','block');$( '[data-layer-location] .hot-topics').css('display','block');
}

$('#runway .expand > a').click(function(e) {  e.preventDefault()});


    function createCookie(name,value,days) {
        if (days) {
            var date = new Date();
            date.setTime(date.getTime()+(days*24*60*60*1000));
            var expires = "; expires="+date.toGMTString();
        }
        else var expires = "";
        document.cookie = name+"="+value+expires+"; path=/";
    }
    function readCookie(name) {
        var nameEQ = name + "=";
        var ca = document.cookie.split(';');
        for(var i=0;i < ca.length;i++) {
            var c = ca[i];
            while (c.charAt(0)==' ') c = c.substring(1,c.length);
            if (c.indexOf(nameEQ) == 0) return c.substring(nameEQ.length,c.length);
        }
        return null;
    }

    function policyAcepted(){
        createCookie("cookie_policy", "true", 5 * 365);
        jQuery('#cookiesBanner').fadeOut();
    }

    if(readCookie("cookie_policy") != "true") {
        //Si no existe la cookie_policy, muestra banner y crea la cookie_policy con valor true y duracion de 5 años
        /*var contenido = "<style>body{ -webkit-text-size-adjust: 100%;-moz-text-size-adjust: 100%;-o-text-size-adjust: 100%; text-size-adjust: 100%; } #cookiesBanner {z-index: 999; width: 100%; position: fixed; bottom:0; left:0; background-color: #efefef; } #cookiesBanner p { font: 10px / 1.2em Arial, sans-serif; margin: 0; text-align: center; padding: .5em 1em;} @media screen and (min-width: 1024px)  {  #cookiesBanner p { font-size: 12px; padding: 1em;}  .cookieAccept{-moz-box-shadow:0 1px 0 0 #f0f7fa;-webkit-box-shadow:0 1px 0 0 #f0f7fa;box-shadow:0 1px 0 0 #f0f7fa;background-color:#c00;-moz-border-radius:6px;-webkit-border-radius:6px;border-radius:6px;border:1px solid #c00;display:inline-block;cursor:pointer;color:#fff;font:10px/1.2em Arial,sans-serif;padding:3px 6px;text-decoration:none;text-shadow:0 -1px 0 #0d0d0d}.cookieAccept:hover{background-color:#d60000}.cookieAccept:active{position:relative;top:1px}}</style><div id='cookiesBanner'><p>Utilizamos cookies propias y de terceros para mejorar nuestros servicios y mostrarle publicidad relacionada con sus preferencias mediante el análisis de sus hábitos de navegación y la generación de los correspondientes perfiles. Si continua navegando, consideramos que acepta su uso. Puede cambiar la configuración u obtener más información <a href='//www.hola.com/contacto/cookies/' target='_blank'>aquí</a> <button type='button' class='cookieAccept' id='cookieAccept'>Aceptar</button></p>\n</div>";

        jQuery("body").append(contenido);

        //Evento botón aceptar
        jQuery('#cookieAccept').click(function() {
            policyAcepted();
        });

        //Aceptar cookies en caso de scroll
        jQuery(window).scroll(function(){
            policyAcepted();
        });

        //Aceptar cookie en caso de pulsar en cualquier parte
        jQuery(window).click(function() {
            policyAcepted();
        });

        //Bloque el evento anterior en el banner de información de cookies
        jQuery('#cookiesBanner').click(function(event){
            event.stopPropagation();
        });*/

        createCookie("cookie_policy", "true", 5 * 365);

    }


var google_tag_params = {
section: 'portada'
};


/* <![CDATA[ */
var google_conversion_id = 1064569246;
var google_custom_params = window.google_tag_params;
var google_remarketing_only = true;
/* ]]> */


if (typeof(FB) != 'undefined') {

FB.Event.subscribe('edge.create', function(targetUrl) {

  _gaq.push(['_trackSocial', 'facebook', 'like', targetUrl]);
});
FB.Event.subscribe('edge.remove', function(targetUrl) {
	_gaq.push(['_trackSocial', 'facebook', 'unlike', targetUrl]);
});

FB.Event.subscribe('message.send', function(targetUrl) {
  _gaq.push(['_trackSocial', 'facebook', 'send', targetUrl]);
});


<!-- End Google Analytics - Facebook -->

<!-- Google Analytics - Twitter -->

function trackTwitter(intent_event) {

    if (intent_event) {
      var opt_pagePath;
      if (intent_event.target && intent_event.target.nodeName == 'IFRAME') {
            opt_target = extractParamFromUri(intent_event.target.src, 'url');
      }

      _gaq.push(['_trackSocial', 'twitter', 'tweet', opt_pagePath]);
    }
  }

<!-- End Google Analytics - Twitter -->
}


	var iniWidth = innerWidth;
	window.addEventListener("touchend", function (e) {
		endWidth = innerWidth;
		if (endWidth < iniWidth) $('body').addClass('zoom').removeClass('shareBar');
		else $('body').removeClass('zoom');
	}, false);


    document.querySelectorAll("#button-no_push-modal,#button-close_push-modal").forEach(elem => elem.addEventListener("click", (e) => {
        document.querySelector("#no-push-modal").style.display = "none";
    }));

    document.querySelector("#button-yes_push-modal").addEventListener("click", (e) => {
        try {
            document.querySelector("#no-push-modal").style.display = "none";
            grantedPermission();
        } catch(error) {
            console.error(error);
        }
    });



    if (typeof navigator.serviceWorker !== 'undefined') {
        navigator.serviceWorker.getRegistrations().then((registrations) => {
            registrations.forEach((registration) => {
                console.log('registration:', registration);
                // incluir en el array todos los scopes donde sea necesario actuar
                if (['https://www.hola.com/', 'https://fashion.hola.com/', 'https://www.hellomagazine.com/', 'https://us.hola.com/', 'https://mx.hola.com/'].includes(registration.scope)) {
                    console.log('service worker on ' + registration.scope + ' unregistered');
                    registration.unregister();
                }
            });
        });
    }

    function ind_topicsSubscribe(topic_codes){

        return new Promise((resolve, reject) => {
            indigitall.topicsSubscribe(topic_codes, (topics) => resolve(topics));
        });
    }

    function ind_topicsUnsubscribe(topic_codes){

        return new Promise((resolve, reject) => {
            indigitall.topicsUnsubscribe(topic_codes, (topics) => resolve(topics));
        });
    }

    async function onIndigitallInitialized(permissions, device){

        if (permissions.push != "granted") {
            return;
        }

        var topicsOn = [];
        var topicsOff = [];

        /* Topic en base a navegación */
        var maxNavTopics = 5;
        var navTopicKey = 'navTopics';
        var prevNavTopics = JSON.parse(localStorage.getItem(navTopicKey) || "[]");
        var currentNavTopic = location.pathname;
        currentNavTopic = currentNavTopic.substring(currentNavTopic.indexOf("/") + 1);
        currentNavTopic = currentNavTopic.substring(0, currentNavTopic.indexOf("/"));
        if(currentNavTopic !== "" && currentNavTopic != null && !prevNavTopics.includes(currentNavTopic)){
            prevNavTopics.push(currentNavTopic);
            if(prevNavTopics.length > maxNavTopics){
                topicsOff.push(prevNavTopics[0]);
                prevNavTopics.splice(0, 1);
            }
            localStorage.setItem(navTopicKey, JSON.stringify(prevNavTopics));
            topicsOn.push(currentNavTopic);
        }

        /* Idioma */
        var defaultLang = 'en';
        var supportedLangs = ['es', defaultLang];
        var langKey = "pushLanguage";

        var lang = navigator.language.indexOf("-");
        var currentLang = (lang >= 0) ?  navigator.language.substring(0, lang) : navigator.language;

        currentLang = (supportedLangs.includes(currentLang)) ? currentLang : defaultLang;
        var prevLang = localStorage.getItem(langKey);
        if(currentLang !== prevLang){
            localStorage.setItem(langKey, currentLang);
            topicsOn.push(currentLang);
            if(prevLang){
                topicsOff.push(prevLang);
            }
        }

        /* Desplazamiento horario del navegador */
        var zone = 'europe';
        var zoneKey = 'zoneNavigation';
        if((new Date()).getTimezoneOffset() > 120){
            zone = 'america';
        }

        var prevZone = localStorage.getItem(zoneKey);
        if (zone !== prevZone) {
            localStorage.setItem(zoneKey, zone);
            topicsOn.push(zone);
            if (prevZone) {
                topicsOff.push(prevZone);
            }
        }

        /* Sync con backend */
        var topicSyncDays = 7;
        var topicLastSyncDateKey = 'topicLastSyncDate';
        var now = (new Date()).getTime();
        var topicLastSyncDate = JSON.parse(localStorage.getItem(topicLastSyncDateKey));

        if (topicLastSyncDate == null ) {
            topicLastSyncDate = now;
            localStorage.setItem(topicLastSyncDateKey, now);
        }

        if(now - topicLastSyncDate > (topicSyncDays * 24 * 3600 * 1000)){
            var allTopicsOn = prevNavTopics;
            allTopicsOn.push(currentLang);
            allTopicsOn.push(zone);
            localStorage.setItem(topicLastSyncDateKey, now);
            await ind_topicsSubscribe(allTopicsOn);
        }else if(topicsOn.length > 0){
            await ind_topicsSubscribe(topicsOn);
        }

        if(topicsOff.length > 0){
            await ind_topicsUnsubscribe(topicsOff);
        }
    }

    function onError(err){
        console.error(err);
    }

    function checkPermissions() {
        var p = window.Notification.permission;

        switch(p) {
            case 'denied':
                return false;
                break;
            case 'default':
                                window.setTimeout(() =>  {
                    document.querySelector("#no-push-modal").style.display = "block";
                }, 45000);
                return false;
                                break;
        }

        return true;
    }

    function grantedPermission() {
        window.Notification.requestPermission().then(function(result) {
            if (result == "granted") {
                onIndigitallLoaded();
            }

            return;
        });
    }

    function onIndigitallLoaded(){
        //Se quita por petición de Carmen Zavala por chat el día 15/09/2020
        //if (true === checkPermissions()) {
            indigitall.init({
                appKey: '5495612975784d3c8598f35.70129146',
                workerPath: '/indigitall/worker.min.js',
                requestLocation: true,
                onError: onError,
                onInitialized: onIndigitallInitialized
            });
        //}
    }

  (function () {

    // autor
    var autor = '';

    // section

            var section = 'portada';
    

    /** CONFIGURATION START **/
    var _sf_async_config = window._sf_async_config = (window._sf_async_config || {});
    _sf_async_config.sections = section;
    _sf_async_config.authors = autor;
    _sf_async_config.type = 'free';


    function getUserTypeChartbeat(userType) {
        switch (userType) {
            case 'registered':
                return 'lgdin';
                break;
            case 'subscriber':
                return 'paid';
                break;
            default:
                return 'anon';
                break;
        }
    }

    // get user type from cookie
    var userType = 'anon';
    try {
        var iduserDecoded = atob(Cookies('iduser'));
        var iduserData = JSON.parse(iduserDecoded);
        if(iduserData.hasOwnProperty('userType')) {
          userType =  getUserTypeChartbeat(iduserData.userType)  ;
        }
    } catch (error) {
        console.error('Error while try to decode iduser cookie. iduser content: ' + Cookies('iduser'));
    }

    var _cbq = window._cbq = (window._cbq || []);
    _cbq.push(['_acct', userType]);

    /** CONFIGURATION END **/
    function loadChartbeat() {
        var e = document.createElement('script');
        var n = document.getElementsByTagName('script')[0];
        e.type = 'text/javascript';
        e.async = true;
        e.src = '//static.chartbeat.com/js/chartbeat.js';
        n.parentNode.insertBefore(e, n);
    }

    loadChartbeat();
})();


    {
      "@context": "https://schema.org",
      "@type": "Organization",
      "url": "https://www.hola.com/",
      "logo": "https://www.himgs.com/imagenes/hola/comunes/logo.png"
    }
    

    {
      "@context" : "https://schema.org",
      "@type" : "WebSite",
      "name" : "HOLA SL",
      "url" : "https://www.hola.com/",
      "sameAs" : [
        "https://www.facebook.com/revistahola",
        "https://twitter.com/hola",
        "https://instagram.com/holacom/",
        "https://www.youtube.com/user/HolaTvES",
        "https://plus.google.com/+HolaRevistaES/posts"
      ]
    }
    