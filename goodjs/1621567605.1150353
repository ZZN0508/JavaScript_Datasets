window.webmd = window.webmd || {}; window.webmd.googleloaded = true; 
window.gdprMatch = false
 var webmdDomain = document.domain; var wot_origin = ""; 
if(typeof document.location != "undefined") {wot_origin = document.location.href;}
 
		var s_topic="1728", 
		s_business_reference="Nav - Home Page", 
		s_publication_source="webmd", 
		s_sponsor_brand="", 
		s_sponsor_program="", 
		s_package_type="Homepage", 
		s_package_name="Home Page", 
		s_channel_super_portal="", 
		s_channel_health="", 
		s_channel_topic_miniguide_guide="", 
		s_channel_mini="", 
		s_channel_micro="", 
		s_tug="", 
		s_topic_dir="", 
		s_mrt="", 
		s_site="core", 
		s_assetname="", 
		s_searchterm="", 
		image_server_url="https://img.webmd.com/dtmcms/live", 
		s_sensitive="false", 
		s_mblv="false", 
		s_tagemax="", 
		s_tagemin="", 
		s_cuih="", 
		s_cuil="", 
		s_cuim="", 
		s_sbtyp="", 
		s_tgender="", 
		s_furl="/", 
		s_uk_user="false", 
		s_account="webmdcom", 
		s_server_type="1b", 
		s_server="wfaws08l-con-25", 
		s_object_type="wbmd_pb_page", 
		s_page_number="", 
		s_site_class="ooc", 
		s_sponsored_uri="default.htm", 
		s_pagename="www.webmd.com/default.htm", 
		s_channel="", 
		s_intended_demographics="__", 
		s_stage_condition="", 
		s_asset_id="091e9c5e816558a8", 
		s_unique_id="091e9c5e816558a8", 
		s_company="webmd", 
		s_refpath="", 
		s_pbnm="", 
		s_pbtp="", 
		s_tpcot=""; 
		
window.s_responsive_design=!0,window.s_business_reference=window.s_business_reference||"",$("html").addClass("responsive"),webmd.url.getParam("print")&&(window.s_business_reference.toLowerCase().indexOf("recipe")>=0&&$("html").addClass("recipe"),window.s_business_reference.toLowerCase().indexOf("blog")>=0&&$("html").addClass("blog"),$("html").addClass("print"),window.print());
 
   webmd.ads2.sizes['121'] = [300,250];
   webmd.ads2.sizes['137'] = [300,250];


var wdlConfig = [
	{
		selector: '.module-f-idc',
		module: 1,
		count: 16,
		itemSel: 'li',
		template: '<li><a href="{{ url }}" data-metrics-link="{{ index }}">{{ title }}</a></li>',
		lazy: true,
	},
	{
		selector: '#sp_ft_rdr .prem_ed',
		module: 1,
		count: 16,
		itemSel: 'a',
		template: '<a onclick="return sl(this,\'\',\'f-idc_{{ index }}\');" href="{{ url }}">{{ title }}</a>',
		lazy: true,
	},
    {
		selector: '.module-f-hs, .module.healthSolutions',
		module: 2,
		count: 16,
		itemSel: 'li',
		template: '<li><a href="{{ url }}" data-metrics-link="{{ index }}">{{ title }}</a></li>',
		lazy: true,
	},
    {
		selector: '#sp_ft_rdr .hs_cols',
		module: 2,
		count: 15,
		itemSel: 'li',
		template: '<li><a href="{{ url }}" onclick="return sl(this,\'\',\'hicb f-hs_{{ index }}\');">{{ title }}</a></li>',
		lazy: true,
	}
];


try {
    document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) {
        window.ttMETA = typeof(window.ttMETA) != "undefined" ? window.ttMETA : [];

        var tokens = e.detail.responseTokens;

        if (isEmpty(tokens)) {
            return;
        }

        var uniqueTokens = distinct(tokens);

        uniqueTokens.forEach(function(token) {
            window.ttMETA.push({
                'CampaignName': token["activity.name"],
                'CampaignId': token["activity.id"],
                'RecipeName': token["experience.name"],
                'RecipeId': token["experience.id"],
                'OfferId': token["option.id"],
                'OfferName': token["option.name"],
                'MboxName': e.detail.mbox
            });
        });
    });

    function isEmpty(val) {
        return (val === undefined || val == null || val.length <= 0) ? true : false;
    }

    function key(obj) {
        return Object.keys(obj)
            .map(function(k) {
                return k + "" + obj[k];
            })
            .join("");
    }

    function distinct(arr) {
        var result = arr.reduce(function(acc, e) {
            acc[key(e)] = e;
            return acc;
        }, {});

        return Object.keys(result)
            .map(function(k) {
                return result[k];
            });
    }
}
catch(error) {}

_satellite["__runScript1"](function(event, target) {
(function() {
  // Load code here
}());
});

(function() {
  // Load code here
}());


function loadJs( src, callback, name) {
	if(typeof jQuery != 'undefined'){
		var $script = $('script[src*="'+src+'"]'),
			head = document.getElementsByTagName("head")[0];

		if ( $script.length ) {
			$script.attr('pending') ? $script.bind('scriptload',callback) : callback();
			return;
		};

		var s = document.createElement('script');
		s.setAttribute("type","text/javascript");
		s.setAttribute('charset', 'UTF-8');
		s.setAttribute("src", src);
		s.setAttribute('id', name);
		s.setAttribute('pending', 1);


		$(s).bind('scriptload',function(){
			$(this).removeAttr('pending');
			callback();
			 //unbind load event
			 //timeout because of pending callbacks
			setTimeout(function(){
				$(s).unbind('scriptload');
			},10);
		});

		// jQuery doesn't handles onload event special for script tag,
		var done = false;
		s.onload = s.onreadystatechange = function() {
			if ( !done && ( !this.readyState || /loaded|complete/.test(this.readyState) ) ) {
				done = true;
				// Handle memory leak in IE
				s.onload = s.onreadystatechange = null;
				$(s).trigger('scriptload');
			};
		};
		head.appendChild(s);
	}
};
loadJs('//native.sharethrough.com/assets/sfp.js', function(){$(document).trigger('sfpLoaded');},'sharethrough');


(function(){
    var b = document.createElement("script"),
    a = document.getElementsByTagName("script")[0];

    b.type = "text/javascript";
    b.async = !0;
    var c = _satellite.buildInfo.environment !== 'production' ? 'https://img.staging.webmd.com/dtmcms/staging' : 'https://img.webmd.com/dtmcms/live'
    b.src = c + '/webmd/consumer_assets/site_images/webmd-tracker/webmd-tracker.min.js';
    a.parentNode.insertBefore(b, a);
})();


// if (webmd && webmd.dfpNative) {
//   webmd.dfpNative.dynamicLead = function() {};
// }


                    var priTopId='1728', secTopId='';
                

    $(function(){
        require(["global_nav/1/global_nav"], function(global_nav) {
            global_nav.init();
        });
    });


                    var priTopId='1728', secTopId='';
                

                    var priTopId='1728', secTopId='';
                

	$(".pd-driver-module").insertBefore(".cfm-intnpromo-hp");

(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v3.1';
  fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));

                    var priTopId='1728', secTopId='';
                

                    var priTopId='1728', secTopId='';
                
require(["waypoints/2/waypoints"],function(){var t=$("#footer-certs");new Waypoint({element:document.getElementsByClassName("global-footer")[0],handler:function(e){"down"===e&&0===$(".global-footer-certificates").length&&(t.replaceWith(t.text()),window.webmd.externalLinks&&window.webmd.externalLinks.init())},offset:"100%"})})
$(function(){var n=function(){var e={};n=function(){},void 0!==window.google_trackConversion&&($.each(webmd.ads2.pageTargets,function(o,n){-1<n.indexOf(",")?e[o]=n.split(","):e[o]=n}),window.google_trackConversion({google_conversion_id:875612316,google_custom_params:e,google_remarketing_only:!0}))};googletag.cmd.push(function(){googletag.pubads().addEventListener("slotRenderEnded",function(o){n()})})})
require(["fly_in/2/fly_in"],function(i){i.init("#triggerFlyin")})

                    var priTopId='1728', secTopId='';
                
if(typeof _satellite != "undefined"){_satellite.pageBottom();}

var selectors = [
	'.global-footer-copyright > p:first-child', //responsive
	'.footer-container .copyright > p:first-child', // funded responsive
	'.footerContent .disclaimer', // harmony
	'.ft_text .copyright', // legacy/flexible
];

try {
	document.querySelectorAll(selectors.join(', ')).forEach(function (el) {
		el.innerHTML = el.innerHTML.replace('2019', new Date().getFullYear());
	})
} catch (err) {
	if(webmd && webmd.debug) {
		webmd.debug('could not update date');
	}
}

