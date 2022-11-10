nvg13574.makeRubicon=function(){var a={};var b=new Array("gender","age","education","interest","product","marital","brand","career","income","cluster","custom");var c=0;var d='';for(c=0;c<b.length;c++){d=nvg13574.getSegment(b[c]);if(d)a['nvg_'+b[c]]=nvg13574.getSegment(b[c]).replace(/-/g,",");};return a;};nvg13574.dfpnvg=function(){this.cokCache={};var a=this.version==7?this.segments:this.seg;for(nvg_i in a){var b='';var c=0;var d='nvg_'+a[nvg_i];d=d.substring(0,10);var e=this.getSegment(a[nvg_i]);if(e.search(',')!=-1){var b=e.split(',');c=1;}else if(e.search('-')!=-1){var b=e.split('-');c=1;}else if(e!=''){if(typeof googletag=="object")googletag.pubads().setTargeting(d,e);if(typeof GA_googleAddAttr=="function")GA_googleAddAttr(d,e);c=0;}if(c==1)if(b.length>=1){if(typeof googletag=="object")googletag.pubads().setTargeting(d,b);if(typeof GA_googleAddAttr=="function")GA_googleAddAttr(d,b);};}};nvg13574.krux_cookie_swap=function(){var a=new Date(),b=window.localStorage.getItem('nvgkrux13574');try{if(!b||((a-new Date(b))>=(24*60*60*1000))){this.include('//beacon.krxd.net/usermatch.gif?partner=navegg&partner_uid='+this.userId);window.localStorage.setItem('nvgkrux13574',a.toJSON());}}catch(c){window.localStorage.removeItem('nvgkrux13574');}};window.naveggReady=window.naveggReady||[];window.naveggReady.push(function(){nvg13574.krux_cookie_swap();});nvg13574.onboarding=function(a){var b=['prtusride','prtusridc','prtusridr','prtusridt'];var c,d,e=0;var f="cd.navdmp.com/cd?id="+(this.version==7?this.userId:this.usr);f+="&acc="+this.account;if(!a.hasOwnProperty('prtid')){if(this.debug)console.error("Navegg - OnBoard - missed prtid parms");return;}f+="&prtid="+a.prtid;for(d=0;d<b.length;d++){c=b[d];if(a.hasOwnProperty(c)){f+="&"+c+"="+a[c];e=1;}}if(a.hasOwnProperty('data'))f+="&data="+escape(JSON.stringify(a.data));if(!e&&this.debug)console.warn("Navegg - OnBoard - parms should contain at least one of:"+b);this.include(this.schema+f);};nvg13574.setOnboard=nvg13574.onboarding;try{nvg13574.url=window.location.href;window.onhashchange=function(){try{nvg13574.url=window.location.href;nvg13574.saveRequest(nvg13574.userId||nvg13574.usr);}catch(a){}};}catch(e){}try{var nvg_hosts=["casavogue.globo.com","revistaglamour.globo.com","gq.globo.com","vogue.globo.com","revistaautoesporte.globo.com","revistacasaejardim.globo.com","revistacrescer.globo.com","epoca.globo.com","epocanegocios.globo.com","revistagalileu.globo.com","revistagloborural.globo.com","revistamarieclaire.globo.com","revistamonet.globo.com","revistapegn.globo.com","revistaquem.globo.com","www.techtudo.com.br"];if(nvg_hosts.indexOf(window.location.host)>-1)nvg13574.include("//tag.navdmp.com/tm46169.js");}catch(e){}try{if(nvg13574.getCookie('Xt0aE3mT_r')=="cf82c")try{nvg13574.setCustom("120929");}catch(err){}if(nvg13574.getCookie('Xt0aE3mT_r')=="55feb")try{nvg13574.setCustom("120930");}catch(err){}if(nvg13574.getCookie('Xt0aE3mT_r')=="15bbe")try{nvg13574.setCustom("120931");}catch(err){}if(nvg13574.getCookie('Xt0aE3mT_r')=="3f5eb")try{nvg13574.setCustom("120932");}catch(err){}}catch(err){}nvg13574.ddp_cookie_swap=function(){if(window.location.host=="www.zapimoveis.com.br"){var a=new Date(),b=window.localStorage.getItem('nvgddp13574');try{if(!b||((a-new Date(b))>=(24*60*60*1000))){this.include('//cm.g.doubleclick.net/pixel?google_nid=navegg_ddp&google_cm');window.localStorage.setItem('nvgddp13574',a.toJSON());}}catch(c){window.localStorage.removeItem('nvgddp13574');}}};window.naveggReady=window.naveggReady||[];window.naveggReady.push(function(){nvg13574.ddp_cookie_swap();});nvg13574.setBeacons=function(){var a,b,c,d,e=[[211503,"beacon.krxd.net/event.gif?event_id=M6IkIfZM","Pixel"],[138176,"beacon.krxd.net/event.gif?event_id=M6Ij5wwD","Pixel"],[138183,"beacon.krxd.net/event.gif?event_id=M6IkT5Yu","Pixel"],[129094,"beacon.krxd.net/event.gif?event_id=M6Ik8xnI","Pixel"],[212807,"beacon.krxd.net/event.gif?event_id=M_irTDJF&event_type=default","Pixel"],[212808,"beacon.krxd.net/event.gif?event_id=M_irzpI_","Pixel"],[211648,"beacon.krxd.net/event.gif?event_id=NB644Bfa&event_type=default&homepage=1","Pixel"],[211649,"beacon.krxd.net/event.gif?event_id=NB65bCk5&event_type=default&compra=1","Pixel"],[214255,"beacon.krxd.net/event.gif?event_id=NB655vdh&event_type=default&revenda-home=1'","Pixel"],[214256,"beacon.krxd.net/event.gif?event_id=NB66rH_n&event_type=default&revenda-cadastro=1","Pixel"],[134696,"beacon.krxd.net/event.gif?event_id=NRIgrMgx&event_type=default","Pixel"],[216886,"beacon.krxd.net/event.gif?event_id=NRmrK9kZ&event_type=default","Pixel"]];b=this.getSegment('custom').split('-');for(c=0;c<e.length;c++){d=e[c];if(b.indexOf(d[0].toString())>=0){a=d[2]=='Script'?'script':'img';this.include('//'+d[1],a);}}};nvg13574.setBeacons();


  var cdaaas = window.cdaaas || {};
  cdaaas.SETTINGS = {"SITE_ID":"home-globo","SITE_NAME":"home-globo","CATEGORIAS":["home","backstage-pages"],"TAG_MANAGER_AD_UNIT":"tvg_Globo.com.Home","TAG_MANAGER_AD_CUSTOM_DATA":"tvg_pgStr=globocom","TAG_MANAGER_AD_CMS_ID":"11413","TAG_MANAGER_AD_ACCOUNT_ID":"95377733","TAG_MANAGER_AD_EXTRAS":[],"PRODUCT_UA":"","MOBILE_GROUP":"desktop"};

var utag_data = {"structure_tree":"[\"home-globo\"]","editoria":"home-globo","ad_unit":"tvg_Globo.com.Home","complemento_ad_unit":"","ad_custom_data":"tvg_pgStr=globocom","cor_pagina":"#0669DE","page_name":"backstage-pages","tipo_pagina":"backstage-pages","content_type":"P\u00e1gina"};

    var linkTags = document.querySelectorAll("link[data-src]");
    for (var i = 0; i < linkTags.length; i++) {
      linkTags[i].setAttribute("href", linkTags[i].getAttribute("data-src"));
    }
   
  

  window.pageRefresh = window.pageRefresh || {};
  window.pageRefresh.timeInSec = parseInt('300', 10);


    window.googletag = window.googletag || {};
    window.googletag.cmd = window.googletag.cmd || [];

    (function (window, document) {
      const elementId = "banner_slb_topo";

      return document.addEventListener("DOMContentLoaded", function () {
        window.renderAdvertising(elementId);
      });
    })(window, document);
  

    window.googletag = window.googletag || {};
    window.googletag.cmd = window.googletag.cmd || [];

    (function (window, document) {
      const elementId = "banner_slb_meio";

      return document.addEventListener("DOMContentLoaded", function () {
        window.renderAdvertising(elementId);
      });
    })(window, document);
  

    window.googletag = window.googletag || {};
    window.googletag.cmd = window.googletag.cmd || [];

    (function (window, document) {
      const elementId = "banner_slb_fim";

      return document.addEventListener("DOMContentLoaded", function () {
        window.renderAdvertising(elementId);
      });
    })(window, document);
  

    window.googletag = window.googletag || {};
    window.googletag.cmd = window.googletag.cmd || [];

    (function (window, document) {
      const elementId = "banner_home4";

      return document.addEventListener("DOMContentLoaded", function () {
        window.renderAdvertising(elementId);
      });
    })(window, document);
  

    window.googletag = window.googletag || {};
    window.googletag.cmd = window.googletag.cmd || [];

    (function (window, document) {
      const elementId = "banner_vitrine";

      return document.addEventListener("DOMContentLoaded", function () {
        window.renderAdvertising(elementId);
      });
    })(window, document);
  

      var oidcSettings = {
        clientId: 'barra@apps.globoid',
        resource: 'barra@apps.globoid',
        authServerUrl: 'https://id.globo.com/auth/realms/globo.com/protocol/openid-connect/auth',
        oidcProvider: 'https://id.globo.com/auth/realms/globo.com',
        redirectUri: window.location.origin.concat('/login-callback.ghtml')
      };
  

  window.pages = window.pages || {};
  window.pages.SETTINGS = {
    ENV: "prod",
    CHANNEL: "desktop",
    CANONICAL_URL: "https://www.globo.com/",
    TITLE: "globo.com - Absolutamente tudo sobre not\u00edcias, esportes e entretenimento",
    SITE_ID: "home-globo",
    SITE_NAME: "home-globo",
    REALTIME_URL: "http://www.globo.com/",
    REALTIME_TENANT: "home_2016",
    RESOURCE: {
      ID: "b8c89b8b-53bf-4757-af2a-bf4ab38b271d",
      MODIFIED: "2021-05-21T03:11:16.972Z",
      CATEGORY: "27268f0a-f421-4488-bc76-69ed94c3b1c5"
    },
    IS_PREVIEW:  false  };
  window.glb_realtime_map = {
    categories: [
      "portal"
    ],
    hasFullUrl: false,
    site: "home_2016",
    url: "http://www.globo.com/",
  };


try {
  const green = 'color: green;'
  const yellow = 'color: #B1B14E;'
  const black = 'color: black;'
  const normal = 'background-color: white; color: black;'
  const pages = 'background-color: black; color: white; font-family: monospaced, width: 80px font-weight: bold;'
  // Please do not remove the empty spaces bellow...

  console.log(
`=============================================================================
Feito no %cB%cr%ca%cs%ci%cl%c
e orgulhosamente construido com
%c
 ____             _        _                     _____                       
|  _ \\           | |      | |                   |  __  \\                     
| |_) | __ _  ___| | _____| |_ __ _  __ _  ___  | |__) |_ _  __ _  ___  ___  
|  _ < / _- |/ __| |/ / __| __/ _- |/ _- |/ _  \ |  ___/ _- |/ _- |/ _  \/ __| 
| |_) | (_| | (__|   <\\__ \\ || (_| | (_| |  __/ | |  | (_| | (_| |  __/\\__ \\ 
|____/\\__,_|\\___|_|\\_\\___/\\__\\__,_|\\__,  |\\___| |_|  \\__,_|\\__, |\\___||___/  
                                    __/ |                   __/ |            
                                   |___/                   |___/             
%c=============================================================================`, green, yellow, green, yellow, green, yellow, black, pages, normal
)
  } catch (e) {}


 var _ibel = document.createElement('script');
 var prefix = window.location.protocol == 'https:' ? 'https:' : 'http:';
_ibel.type = 'text/javascript';
_ibel.src = prefix + '//ib.la.ib-ibi.com/ibiview.js?go=281717&id1={emailSha1Hash}';
(document.getElementsByTagName('body')[0] || document.getElementsByTagName('head')[0]).appendChild(_ibel); 


// this tag is intentionally blank



(function() {
    Krux('scrape', {
        'page_attr_url_path_1': {
            url_path: '1'
        },
        'page_attr_url_path_2': {
            url_path: '2'
        },
        'page_attr_url_path_3': {
            url_path: '3'
        },
        'page_attr_url_path_4': {
            url_path: '4'
        },
        'page_attr_url_path_5': {
            url_path: '5'
        }
    });
    if (window.localStorage.kxglobo_user) {
        Krux('set', 'user_attr_kxuser', localStorage.kxglobo_user);
    }

    var krux_utag = JSON.parse(localStorage.getItem('krux_utag'));
    if (krux_utag) {
        Krux('set', {
            page_attr_content_type: krux_utag.content_type,
            page_attr_page_name: krux_utag.page_name,
            page_attr_meta_keywords: krux_utag["meta.keywords"],
            page_attr_meta_site_name: krux_utag["meta.og:site_name"],
            page_attr_verticle: krux_utag.vertical
        });
        if (krux_utag.structure_tree) {
            var sTree = krux_utag.structure_tree;
        }
        if (sTree) {
            if (typeof(sTree) === "string" && sTree.match(/"/)) {
                sTree = JSON.parse(sTree);
                for (var i = 0; i < sTree.length; i++) {
                    Krux('set', 'page_attr_structure_tree_' + [i + 1], sTree[i]);
                }
            }
        }

    }
    if (window.pageOptions) {
        Krux('set', 'page_attr_searchQuery', pageOptions.query);
    }

    Krux('set', 'page_attr_title', document.title);
    Krux('scrape', {
        'page_attr_meta_editoria': {
            meta_name: 'editoria'
        },
        'page_attr_meta_article_section': {
            meta_property: 'article:section'
        },
        'page_attr_meta_video_series': {
            meta_property: 'video:series'
        }
    });
    if (window.location) {
        var hn = document.location.hostname,
            pn = document.location.pathname,
            dm, sd;
        if (pn) {
            if (pn.match('.html')) {
                pn = pn.replace('.html', '');
            }
            if (hn) {
                Krux('set', 'page_attr_full_path', hn + pn);
                hn = hn.split('.');
                if (hn[0] == "www") {
                    dm = hn[1];
                    sd = "";
                }
                if (hn[0] != "www") {
                    dm = hn[1];
                    sd = hn[0];
                }
                if (dm == "com") {
                    dm = "";
                }
                if (sd == "www") {
                    sd = "";
                }

                Krux('set', {
                    page_attr_subdomain: sd,
                    page_attr_domain: dm,
                });
            }
        }
    }
})();


(function() {

    /* Data Transfer Code for globo */
    Krux('scrape', {
        page_attr_info_assin_id_parc: {
            js_global: 'info_assin_id_parc'
        },
        page_attr_info_assin_cod_prod: {
            js_global: 'info_assin_cod_prod'
        },
        page_attr_info_assin_cod_prods_vitrine: {
            js_global: 'info_assin_cod_prods_vitrine'
        },
        page_attr_info_assin_campanha: {
            js_global: 'info_assin_campanha'
        },
        page_attr_info_assin_utm_source: {
            js_global: 'info_assin_utm_source'
        },
        page_attr_info_assin_utm_medium: {
            js_global: 'info_assin_utm_medium'
        },
        page_attr_info_assin_utm_campaign: {
            js_global: 'info_assin_utm_campaign'
        }
    });

})();


(function() {
    Krux('scrape', {
        page_attr_utag_editoria: { 'js_global': 'utag_data.editoria' },
        page_attr_utag_page_type: { 'js_global': 'utag_data.tipo_pagina' },
        page_attr_utag_produto: { 'js_global': 'utag_data.produto' },
        page_attr_searchQuery: { 'js_global': 'busca.q' }
    });
})();


(function() {

    Krux('scrape', {
        user_attr_utag_cadun_gender: { 'js_global': 'localStorage.gdmp_gender' },
        user_attr_glbdt_utype: { 'js_global': 'localStorage.gdmp_utype' },
        user_attr_glbdt_city: { 'js_global': 'localStorage.gdmp_city' },
        user_attr_utag_cadun_state: { 'js_global': 'localStorage.gdmp_state' },
        user_attr_utag_cadun_age: { 'js_global': 'localStorage.gdmp_age' },
        user_attr_dmp_globo_id: { 'js_global' : 'localStorage.glbdt_globoid' }
    });
    
})();


(function() {
    /* Selective Attribute DataLayer Library Tag */
    var _, allAttr, allowedList, attr, attributes, dataLayerIngester, dataObj,
        isAllowed, keepCase, libUtil, omitKeys, pageAttr, prefix, toSet, trim,
        userAttr, util, value,
        hasProp = {}.hasOwnProperty;
    _ = Krux('require:underscore');
    util = Krux('require:util');
    libUtil = Krux('require:util.library-tag');
    dataLayerIngester = Krux('require:scrape').ingestDataLayer;

    /* Safe copy of dataLayer object */
    dataObj = Krux('scrape.javascript', 'nvg13574');

    /* String trimming helper function */
    trim = function(attr) {
        return ("" + attr).replace(/^\s+|\s+$/g, '');
    };

    /* Attribute configs */
    pageAttr = _.map('none'.split(','), trim);
    userAttr = _.map('gender,age,income'.split(','), trim);

    /* Create a array of attributes striping any empty strings */
    allAttr = _.without(pageAttr.concat(userAttr), '');

    /* Configuration settings */
    keepCase = 'undefined' === 'true';
    omitKeys = 'false'.split(',');

    /* Resolve Prefix */
    prefix = libUtil.resolvePrefix('undefined', 'undefined',
        'undefined');

    /* Function to varify if attribute should be used */
    isAllowed = function(value, whitelist) {
        var i, len, str, x;
        str = "" + value;
        if (!((value != null) && str.length > 0)) {
            return false;
        }
        for (i = 0, len = whitelist.length; i < len; i++) {
            x = whitelist[i];
            if (value.match(x) != null) {
                return true;
            }
        }
        return false;
    };

    /* Get a full list of attributes usting the dataLayer tool */
    attributes = dataLayerIngester(dataObj, {
        omitKeys: libUtil.removeFalsyStrings(omitKeys.concat(libUtil.EXCLUDE_KEYS_CONFIG)),
        omitValues: libUtil.EXCLUDE_VALUES_CONFIG,
        caseSensitive: keepCase,
        useFullPath: 'false' === 'true',
        useLastValue: 'false' === 'true',
        customDelimited: [/./],
        altDelimiter: ',',
        userKeys: _.map(userAttr, function(exp) {
            return new RegExp("(^|\\.)" + exp + "$");
        }),
        optimizeNames: true
    });

    /* Only set Attributes in the allowed list */
    allowedList = _.map(allAttr, function(name) {
        return new RegExp("(_attr_|_attr_" + prefix + "|\\.)" + (keepCase ?
            name : libUtil.normalizeAttrName(name, {
                removeDot: false
            })) + "$");
    });
    toSet = {};
    for (attr in attributes) {
        if (!hasProp.call(attributes, attr)) continue;
        value = attributes[attr];
        if (isAllowed(attr, allowedList)) {
            toSet[attr] = value;
        }
    }
    toSet = Krux('prefix:attr', toSet, prefix);
    Krux('set', toSet);
}).call();


(function(){

	var params = Krux('require:util').urlParams();
	
	Krux ('set', { 
	'page_attr_globo_utm_origem': params.utm_origem || params.utm_source,
	'page_attr_globo_utm_midia': params.utm_midia || params.utm_medium,
	'page_attr_globo_utm_campanha': params.utm_campanha || params.utm_campaign,
	'page_attr_globo_utm_content': params.utm_content,
	'page_attr_globo_utm_term': params.utm_term, 
    'page_attr_globo_campanha': params.campanha
	});
	
})();


(function() {
    var clickURL = Krux('get', 'url_click'),
        _ = Krux('require:underscore'),
        libUtil = Krux('require:util.library-tag'),
        pixelParam, store, sent,
        confid, campaignid, siteid;

    // Function to retrieve capping info from sessionStorage
    function get(key) {
        try {
            return JSON.parse(sessionStorage.getItem(key) || '[]');
        } catch (e) {
            return [];
        }
    }

    // Function to add capping info to sessionStorage
    function set(key, value) {
        try {
            sessionStorage.setItem(key, JSON.stringify(value));
        } catch (e) {}
    }

    // Function to check if tag is valid by comparing aginst capping info
    function configValidate(config) {
        var allowedSource = libUtil.removeFalsyStrings('newsletter'.toLowerCase()),
            i = 0;
        for (; i < store.length; i++) {
            if (_.isEqual(store[i], config)) return false;
        }
        // Cater for client not using allowedSource
        if (!allowedSource.length) allowedSource.push(config.kxsiteid.toLowerCase());
        // Invalid if source is not in the allowed list
        if (_.indexOf(allowedSource, config.kxsiteid.toLowerCase()) < 0) return false;
        return true;
    }

    // Function to collect and normalize values
    function getParameter(method, path) {
        var value;

        if (!(method && path)) return;

        switch (method) {
            case 'none':
                break;
            case 'text':
                value = path;
                break;
            case 'get':
                value = Krux('get', path);
                break;
            default:
                value = Krux('scrape.' + method, path);
        }

        if (value && !_.isArray(value)) return ('' + value)
            .replace(/[^a-zA-Z0-9_-]+/g, '_')
            .replace(/_+/g, '_')
            .replace(/^_/, '')
            .replace(/_$/, '');
        // Use null if no result as it is included in JSON.stringify
        return null;
    }

    // Scrape Media Attributes
    confid = getParameter('text', 'vbxfh7yb4');
    campaignid = getParameter('url_param', 'utm_campaign');
    siteid = getParameter('url_param', 'utm_source');

    // Ensure minimum requirements are met
    if (confid && campaignid && siteid) {
        // Use omit to remove undefined values to match validation object
        pixelParam = _.omit({
            'kxconfid': confid,
            'kxcampaignid': campaignid,
            'kxsiteid': siteid,
            'kxadvertiserid': getParameter('none', 'undefined'),
            'kxplacementid': getParameter('url_param', 'utm_medium'),
            'kxadid': getParameter('url_param', 'utm_content'),
            'kxcreativeid': getParameter('url_param', 'term'),
            'kxbrand': getParameter('none', 'undefined'),
            'clk': 'https://beacon.krxd.net/click_landing.gif'
        }, function(value) {
            return !value
        });

        // Retrieve capping info
        store = get('k_utm_store');

        if (configValidate(pixelParam)) {
            // Update capping info to prevent re-fires
            store.push(pixelParam);
            set('k_utm_store', store);
            sent = Krux('require:http').pixel({
                url: clickURL,
                data: pixelParam
            });
        }
    }
}).call();


(function(){
	var Nav = window.navigator.userAgent;

	// based on https://developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent
	// and https://developers.whatismybrowser.com/useragents/explore/software_name

	// otherwise it looks like Chrome...
	if (Nav.match(/Instagram\/[0-9]*/)){
		Krux('set',{page_attr_browser_name:'Instagram'});
	}
	// Firefox
	else if (Nav.match(/Firefox\/[0-9]*/) && ! (Nav.match(/Seamonkey\//))){
		Krux('set',{page_attr_browser_name:'Firefox'});
	}

	// Edge
	else if (Nav.match(/Edge\/[0-9]*/)){
		Krux('set',{page_attr_browser_name:'Edge'});
	}

	// UC Browser (mimicks Safari/Google check)
	else if (Nav.match(/UC ?Browser\/[0-9]*/)){
		Krux('set',{page_attr_browser_name:'UCBrowser'});
	}

	// Safari 
	else if (Nav.match(/Safari\/[0-9.]*$/) && ! (Nav.match(/Chrome\//) || Nav.match(/Chromium\//))){
		Krux('set',{page_attr_browser_name:'Safari'});
	}

	// Chrome 
	else if (Nav.match(/Chrome\/[0-9]*/) && ! (Nav.match(/Chromium\//))){
		Krux('set',{page_attr_browser_name:'Chrome'});
	}
	// Chrome
	else if (Nav.match(/Chrome\/[0-9]*/) && (Nav.match(/Chromium\//))){
		Krux('set',{page_attr_browser_name:'Chromium'});
	}

	// MSIE 11
	else if (Nav.match(/Trident\/[0-9]*/) && Nav.match(/like Gecko/)){
		Krux('set',{page_attr_browser_name:'Internet Explorer 11'});
	}

	// MSIE 6-10
	else if (Nav.match(/MSIE [0-9.]*;/)){
		Krux('set',{page_attr_browser_name:'Internet Explorer'});
	}

	// Opera >15
	else if (Nav.match(/OPR\/[0-9]*/)){
		Krux('set',{page_attr_browser_name:'Opera 15+'});
	}

	// Opera <=12
	else if (Nav.match(/Opera\/[0-9]*/)){
		Krux('set',{page_attr_browser_name:'Opera 12 (and below)'});
	}

	// should be rarer browsers
	else{
		Krux('set',{page_attr_browser_name:'Other'});
	}

})(); 


(function() {
    /* Selective Attribute DataLayer Library Tag */
    var _, allAttr, allowedList, attr, attributes, dataLayerIngester, dataObj,
        isAllowed, keepCase, libUtil, omitKeys, pageAttr, prefix, toSet, trim,
        userAttr, util, value,
        hasProp = {}.hasOwnProperty;
    _ = Krux('require:underscore');
    util = Krux('require:util');
    libUtil = Krux('require:util.library-tag');
    dataLayerIngester = Krux('require:scrape').ingestDataLayer;

    /* Safe copy of dataLayer object */
    dataObj = Krux('scrape.javascript', 'utag.data');

    /* String trimming helper function */
    trim = function(attr) {
        return ("" + attr).replace(/^\s+|\s+$/g, '');
    };

    /* Attribute configs */
    pageAttr = _.map('produtosCarrinho,origemID,step,lproducts,period,payment,retention'.split(','), trim);
    userAttr = _.map('undefined'.split(','), trim);

    /* Create a array of attributes striping any empty strings */
    allAttr = _.without(pageAttr.concat(userAttr), '');

    /* Configuration settings */
    keepCase = 'false' === 'true';
    omitKeys = ''.split(',');

    /* Resolve Prefix */
    prefix = libUtil.resolvePrefix('none', 'undefined',
        'undefined');

    /* Function to varify if attribute should be used */
    isAllowed = function(value, whitelist) {
        var i, len, str, x;
        str = "" + value;
        if (!((value != null) && str.length > 0)) {
            return false;
        }
        for (i = 0, len = whitelist.length; i < len; i++) {
            x = whitelist[i];
            if (value.match(x) != null) {
                return true;
            }
        }
        return false;
    };

    /* Get a full list of attributes usting the dataLayer tool */
    attributes = dataLayerIngester(dataObj, {
        omitKeys: libUtil.removeFalsyStrings(omitKeys.concat(libUtil.EXCLUDE_KEYS_CONFIG)),
        omitValues: libUtil.EXCLUDE_VALUES_CONFIG,
        caseSensitive: keepCase,
        useFullPath: 'false' === 'true',
        useLastValue: 'false' === 'true',
        customDelimited: [/./],
        altDelimiter: ',',
        userKeys: _.map(userAttr, function(exp) {
            return new RegExp("(^|\\.)" + exp + "$");
        }),
        optimizeNames: true
    });

    /* Only set Attributes in the allowed list */
    allowedList = _.map(allAttr, function(name) {
        return new RegExp("(_attr_|_attr_" + prefix + "|\\.)" + (keepCase ?
            name : libUtil.normalizeAttrName(name, {
                removeDot: false
            })) + "$");
    });
    toSet = {};
    for (attr in attributes) {
        if (!hasProp.call(attributes, attr)) continue;
        value = attributes[attr];
        if (isAllowed(attr, allowedList)) {
            toSet[attr] = value;
        }
    }
    toSet = Krux('prefix:attr', toSet, prefix);
    Krux('set', toSet);
}).call();
