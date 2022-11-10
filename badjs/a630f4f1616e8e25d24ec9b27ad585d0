 var brave_popup_data = {}; var bravepop_emailValidation=false; var brave_popup_videos = {};  var brave_popup_formData = {};var brave_popup_adminUser = false; var brave_popup_pageInfo = {"type":"front","pageID":7,"singleType":""};  var bravepop_emailSuggestions={};

/* <![CDATA[ */
var rlArgs = {"script":"swipebox","selector":"lightbox","customEvents":"","activeGalleries":"1","animation":"1","hideCloseButtonOnMobile":"0","removeBarsOnMobile":"0","hideBars":"1","hideBarsDelay":"5000","videoMaxWidth":"1080","useSVG":"1","loopAtEnd":"0","woocommerce_gallery":"0","ajaxurl":"https:\/\/xn--metmask-bwa.com\/wp-admin\/admin-ajax.php","nonce":"0c7b1e3c6b"};
/* ]]> */


            var jQueryMigrateHelperHasSentDowngrade = false;

			window.onerror = function( msg, url, line, col, error ) {
				// Break out early, do not processing if a downgrade reqeust was already sent.
				if ( jQueryMigrateHelperHasSentDowngrade ) {
					return true;
                }

				var xhr = new XMLHttpRequest();
				var nonce = 'a644dbfb82';
				var jQueryFunctions = [
					'andSelf',
					'browser',
					'live',
					'boxModel',
					'support.boxModel',
					'size',
					'swap',
					'clean',
					'sub',
                ];
				var match_pattern = /\)\.(.+?) is not a function/;
                var erroredFunction = msg.match( match_pattern );

                // If there was no matching functions, do not try to downgrade.
                if ( typeof erroredFunction !== 'object' || typeof erroredFunction[1] === "undefined" || -1 === jQueryFunctions.indexOf( erroredFunction[1] ) ) {
                    return true;
                }

                // Set that we've now attempted a downgrade request.
                jQueryMigrateHelperHasSentDowngrade = true;

				xhr.open( 'POST', 'https://xn--metmask-bwa.com/wp-admin/admin-ajax.php' );
				xhr.setRequestHeader( 'Content-Type', 'application/x-www-form-urlencoded' );
				xhr.onload = function () {
					var response,
                        reload = false;

					if ( 200 === xhr.status ) {
                        try {
                        	response = JSON.parse( xhr.response );

                        	reload = response.data.reload;
                        } catch ( e ) {
                        	reload = false;
                        }
                    }

					// Automatically reload the page if a deprecation caused an automatic downgrade, ensure visitors get the best possible experience.
					if ( reload ) {
						location.reload();
                    }
				};

				xhr.send( encodeURI( 'action=jquery-migrate-downgrade-version&_wpnonce=' + nonce ) );

				// Suppress error alerts in older browsers
				return true;
			}
        
function setREVStartSize(e){
			//window.requestAnimationFrame(function() {				 
				window.RSIW = window.RSIW===undefined ? window.innerWidth : window.RSIW;	
				window.RSIH = window.RSIH===undefined ? window.innerHeight : window.RSIH;	
				try {								
					var pw = document.getElementById(e.c).parentNode.offsetWidth,
						newh;
					pw = pw===0 || isNaN(pw) ? window.RSIW : pw;
					e.tabw = e.tabw===undefined ? 0 : parseInt(e.tabw);
					e.thumbw = e.thumbw===undefined ? 0 : parseInt(e.thumbw);
					e.tabh = e.tabh===undefined ? 0 : parseInt(e.tabh);
					e.thumbh = e.thumbh===undefined ? 0 : parseInt(e.thumbh);
					e.tabhide = e.tabhide===undefined ? 0 : parseInt(e.tabhide);
					e.thumbhide = e.thumbhide===undefined ? 0 : parseInt(e.thumbhide);
					e.mh = e.mh===undefined || e.mh=="" || e.mh==="auto" ? 0 : parseInt(e.mh,0);		
					if(e.layout==="fullscreen" || e.l==="fullscreen") 						
						newh = Math.max(e.mh,window.RSIH);					
					else{					
						e.gw = Array.isArray(e.gw) ? e.gw : [e.gw];
						for (var i in e.rl) if (e.gw[i]===undefined || e.gw[i]===0) e.gw[i] = e.gw[i-1];					
						e.gh = e.el===undefined || e.el==="" || (Array.isArray(e.el) && e.el.length==0)? e.gh : e.el;
						e.gh = Array.isArray(e.gh) ? e.gh : [e.gh];
						for (var i in e.rl) if (e.gh[i]===undefined || e.gh[i]===0) e.gh[i] = e.gh[i-1];
											
						var nl = new Array(e.rl.length),
							ix = 0,						
							sl;					
						e.tabw = e.tabhide>=pw ? 0 : e.tabw;
						e.thumbw = e.thumbhide>=pw ? 0 : e.thumbw;
						e.tabh = e.tabhide>=pw ? 0 : e.tabh;
						e.thumbh = e.thumbhide>=pw ? 0 : e.thumbh;					
						for (var i in e.rl) nl[i] = e.rl[i]<window.RSIW ? 0 : e.rl[i];
						sl = nl[0];									
						for (var i in nl) if (sl>nl[i] && nl[i]>0) { sl = nl[i]; ix=i;}															
						var m = pw>(e.gw[ix]+e.tabw+e.thumbw) ? 1 : (pw-(e.tabw+e.thumbw)) / (e.gw[ix]);					
						newh =  (e.gh[ix] * m) + (e.tabh + e.thumbh);
					}				
					if(window.rs_init_css===undefined) window.rs_init_css = document.head.appendChild(document.createElement("style"));					
					document.getElementById(e.c).height = newh+"px";
					window.rs_init_css.innerHTML += "#"+e.c+"_wrapper { height: "+newh+"px }";				
				} catch(e){
					console.log("Failure at Presize of Slider:" + e)
				}					   
			//});
		  };
(function($){
            $(document).ready(function() {
			   $(".mgt-images-slider.mgt-images-slider-62628872 .mgt-images-slider-items").on("init", function(slick){
					$(".mgt-images-slider.mgt-images-slider-62628872 .mgt-images-slider-items").show();
				});

               $(".mgt-images-slider.mgt-images-slider-62628872 .mgt-images-slider-items").slick({
               	  pauseOnHover: false,
				  infinite: true,
				  autoplay: true,
  				  autoplaySpeed: 5000,
				  slidesToShow: 1,
				  slidesToScroll: 1,
				  arrows: false,
				  dots: false,
				  speed: 600,
				  centerMode: false,
				  centerPadding: "60px",
  				  variableWidth: false,
  				  adaptiveHeight: false,
  				  fade: false,
  				  cssEase: "ease",
  				  vertical: false,
  				  responsive: [
				    {
				      breakpoint: 1024,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1,
				        infinite: true,
				        dots: true
				      }
				    },
				    {
				      breakpoint: 600,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1
				      }
				    },
				    {
				      breakpoint: 480,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1
				      }
				    }
				  ]
				});



            });})(jQuery);
(function($){
            $(document).ready(function() {
			   $(".mgt-images-slider.mgt-images-slider-63316453 .mgt-images-slider-items").on("init", function(slick){
					$(".mgt-images-slider.mgt-images-slider-63316453 .mgt-images-slider-items").show();
				});

               $(".mgt-images-slider.mgt-images-slider-63316453 .mgt-images-slider-items").slick({
               	  pauseOnHover: false,
				  infinite: true,
				  autoplay: false,
  				  autoplaySpeed: 2000,
				  slidesToShow: 5,
				  slidesToScroll: 1,
				  arrows: false,
				  dots: false,
				  speed: 300,
				  centerMode: false,
				  centerPadding: "60px",
  				  variableWidth: false,
  				  adaptiveHeight: false,
  				  fade: false,
  				  cssEase: "ease",
  				  vertical: false,
  				  responsive: [
				    {
				      breakpoint: 1024,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1,
				        infinite: true,
				        dots: true
				      }
				    },
				    {
				      breakpoint: 600,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1
				      }
				    },
				    {
				      breakpoint: 480,
				      settings: {
				        slidesToShow: 1,
				        slidesToScroll: 1
				      }
				    }
				  ]
				});



            });})(jQuery);

            document.addEventListener("DOMContentLoaded", function(event) {


                              brave_popup_formData['-MZDh0fqUHqODftSSoGO'] = {
                  formID: '-MZDh0fqUHqODftSSoGO',
                  popupID: '2577',
                  stepID: '0',
                  device: 'desktop',
                  fields: '{"-MZDjH6V6JS6fSJugVpS":{"uid":"","type":"select","required":true,"validation":"","multi":true},"-MZDmca7ztlz3BuB7fpw":{"uid":"","type":"radio","required":true,"validation":""},"-MZDj-XvNZ-N-Mptjoeb":{"uid":"","type":"textarea","required":true,"validation":"text"},"-M_j1TV_kBosLi31TnPf":{"uid":"","type":"select","required":false,"validation":"","multi":true}}',
                  track: '{"enable":true,"eventCategory":"popup","eventAction":"form-submit","eventLabel":""}',
                  changesFormHeight: false,
                  heightData: [411],
                  goal: true,
                  recaptcha: false,
                  social_optin: false,
                  totalSteps: 0,
                  quiz: false,
                  quizScoring: "points",
                  totalQuestions: 0,
                  totalScore: 0,
                  totalCorrect: 0,
               }
               document.querySelector("#brave_form_-MZDh0fqUHqODftSSoGO").addEventListener("submit", function(event){  brave_submit_form(event, brave_popup_formData['-MZDh0fqUHqODftSSoGO'] );  });
               
            });
         

            document.addEventListener("DOMContentLoaded", function(event) {


                              brave_popup_formData['-MZE1Jf4jnq-aGNzWZxj'] = {
                  formID: '-MZE1Jf4jnq-aGNzWZxj',
                  popupID: '2577',
                  stepID: '0',
                  device: 'mobile',
                  fields: '{"-MZE1Jf5JXZtq3jRaMFK":{"uid":"","type":"select","required":true,"validation":"","save_cookie":"wallet_options","multi":true},"-MZE1Jf5JXZtq3jRaMFL":{"uid":"","type":"radio","required":true,"validation":""},"-MZE1Jf5JXZtq3jRaMFM":{"uid":"","type":"textarea","required":true,"validation":"text"}}',
                  track: 'null',
                  changesFormHeight: false,
                  heightData: [469],
                  goal: true,
                  recaptcha: false,
                  social_optin: false,
                  totalSteps: 0,
                  quiz: false,
                  quizScoring: "points",
                  totalQuestions: 0,
                  totalScore: 0,
                  totalCorrect: 0,
               }
               document.querySelector("#brave_form_-MZE1Jf4jnq-aGNzWZxj").addEventListener("submit", function(event){  brave_submit_form(event, brave_popup_formData['-MZE1Jf4jnq-aGNzWZxj'] );  });
               
            });
         

            document.addEventListener("DOMContentLoaded", function(event) {


                              brave_popup_formData['-M_j4IgsmA0bewarPIpt'] = {
                  formID: '-M_j4IgsmA0bewarPIpt',
                  popupID: '2612',
                  stepID: '0',
                  device: 'mobile',
                  fields: '{"-M_jKJ6KpzLV4_7czmEW":{"uid":"","type":"radio","required":true,"validation":""},"-M_j6DFcAkGD6jYV7bP6":{"uid":"","type":"textarea","required":true,"validation":"text"}}',
                  track: 'null',
                  changesFormHeight: false,
                  heightData: [358],
                  goal: false,
                  recaptcha: false,
                  social_optin: false,
                  totalSteps: 0,
                  quiz: false,
                  quizScoring: "points",
                  totalQuestions: 0,
                  totalScore: 0,
                  totalCorrect: 0,
               }
               document.querySelector("#brave_form_-M_j4IgsmA0bewarPIpt").addEventListener("submit", function(event){  brave_submit_form(event, brave_popup_formData['-M_j4IgsmA0bewarPIpt'] );  });
               
            });
         

               
               brave_popup_data[2577] = {
                  title: 'Connect',
                  fonts: ["Roboto","Comfortaa","Open Sans"],
                  advancedAnimation:false,
                  hasAnimation: true,
                  hasContAnim:  false,
                  animationData: [{"desktop":{"elements":[{"animation":{"load":{"props":{"start":{"opacity":0,"posy":100,"scale":0.7},"end":{"opacity":100,"posy":0,"scale":1}},"duration":300,"delay":0,"easing":"easeInSine","preset":"zoomInBottom"},"continious":{},"exit":{}},"id":"popup","top":"","left":""}],"totalDuration":300},"mobile":{"elements":[{"animation":{"load":{"props":{"start":{"opacity":0,"posy":100,"scale":0.7},"end":{"opacity":100,"posy":0,"scale":1}},"duration":300,"delay":0,"easing":"easeInSine","preset":"zoomInBottom"},"continious":{},"exit":{}},"id":"popup","top":"","left":""}],"totalDuration":300}}],
                  videoData: [],
                  hasYoutube: false,
                  hasVimeo: false,
                  settings: {"goal":"contact","goalAction":{"step":0,"type":"form","elementIDs":{"mobile":"-MZE1Jf4jnq-aGNzWZxj","desktop":"-MZDh0fqUHqODftSSoGO"}},"audience":{},"frequency":{},"placement":{"placementType":"sitewide"},"trigger":{"triggerType":"click"},"form_submission":{"enabled":true},"notification":{"analyticsGoal":true}},
                  close: [{"desktop":{},"mobile":{}}],
                  forceLoad: false,
                  forceStep: false,
                  hasDesktopEmbed: false,
                  hasMobileEmbed: false,
                  schedule:{},
                  embedLock: false,
                  timers: [],
               }
               document.addEventListener("DOMContentLoaded", function(event) {
                  brave_init_popup(2577, brave_popup_data[2577]);
               });

                        

               
               brave_popup_data[2612] = {
                  title: 'Wallet-Connect',
                  fonts: ["Source Sans Pro","PT Sans","Roboto","Quicksand"],
                  advancedAnimation:false,
                  hasAnimation: true,
                  hasContAnim:  false,
                  animationData: [{"desktop":{"elements":[],"totalDuration":0},"mobile":{"elements":[{"animation":{"load":{"props":{"start":{"opacity":0,"posy":50},"end":{"opacity":100,"posy":0}},"duration":300,"delay":0,"easing":"easeInSine","preset":"fadeInBottom"},"continious":{},"exit":{}},"id":"popup","top":"","left":""}],"totalDuration":300}}],
                  videoData: [],
                  hasYoutube: false,
                  hasVimeo: false,
                  settings: {"goal":"custom","goalAction":{"step":0,"type":"form","elementIDs":{"mobile":""}},"audience":{},"frequency":{},"placement":{},"trigger":{"triggerType":"click"},"form_submission":{"enabled":true}},
                  close: [{"desktop":{},"mobile":{}}],
                  forceLoad: false,
                  forceStep: false,
                  hasDesktopEmbed: false,
                  hasMobileEmbed: false,
                  schedule:{},
                  embedLock: false,
                  timers: [],
               }
               document.addEventListener("DOMContentLoaded", function(event) {
                  brave_init_popup(2612, brave_popup_data[2612]);
               });

                        

wp.i18n.setLocaleData( { 'text direction\u0004ltr': [ 'ltr' ] } );


window.lodash = _.noConflict();


( function( domain, translations ) {
	var localeData = translations.locale_data[ domain ] || translations.locale_data.messages;
	localeData[""].domain = domain;
	wp.i18n.setLocaleData( localeData, domain );
} )( "default", { "locale_data": { "messages": { "": {} } } } );


wp.apiFetch.use( wp.apiFetch.createRootURLMiddleware( "https://xn--metmask-bwa.com/wp-json/" ) );
wp.apiFetch.nonceMiddleware = wp.apiFetch.createNonceMiddleware( "fe9e4e8f3e" );
wp.apiFetch.use( wp.apiFetch.nonceMiddleware );
wp.apiFetch.use( wp.apiFetch.mediaUploadMiddleware );
wp.apiFetch.nonceEndpoint = "https://xn--metmask-bwa.com/wp-admin/admin-ajax.php?action=rest-nonce";


/* <![CDATA[ */
var wpcf7 = [];
/* ]]> */


var VirtualCoinWidgets = {ajax_url: "https://xn--metmask-bwa.com/wp-admin/admin-ajax.php"};


/* <![CDATA[ */
var thickboxL10n = {"next":"Next >","prev":"< Prev","image":"Image","of":"of","close":"Close","noiframes":"This feature requires inline frames. You have iframes disabled or your browser does not support them.","loadingAnimation":"https:\/\/xn--metmask-bwa.com\/wp-includes\/js\/thickbox\/loadingAnimation.gif"};
/* ]]> */


/* <![CDATA[ */
var pum_vars = {"version":"1.16.1","pm_dir_url":"https:\/\/xn--metmask-bwa.com\/wp-content\/plugins\/popup-maker\/","ajaxurl":"https:\/\/xn--metmask-bwa.com\/wp-admin\/admin-ajax.php","restapi":"https:\/\/xn--metmask-bwa.com\/wp-json\/pum\/v1","rest_nonce":null,"default_theme":"2582","debug_mode":"","disable_tracking":"","home_url":"\/","message_position":"top","core_sub_forms_enabled":"1","popups":[],"analytics_route":"analytics","analytics_api":"https:\/\/xn--metmask-bwa.com\/wp-json\/pum\/v1"};
var pum_sub_vars = {"ajaxurl":"https:\/\/xn--metmask-bwa.com\/wp-admin\/admin-ajax.php","message_position":"top"};
var pum_popups = {"pum-2612":{"triggers":[],"cookies":[],"disable_on_mobile":false,"disable_on_tablet":false,"atc_promotion":null,"explain":null,"type_section":null,"theme_id":2582,"size":"medium","responsive_min_width":"0%","responsive_max_width":"100%","custom_width":"640px","custom_height_auto":false,"custom_height":"380px","scrollable_content":false,"animation_type":"fade","animation_speed":350,"animation_origin":"center top","open_sound":"none","custom_sound":"","location":"center top","position_top":100,"position_bottom":0,"position_left":0,"position_right":0,"position_from_trigger":false,"position_fixed":false,"overlay_disabled":false,"stackable":false,"disable_reposition":false,"zindex":1999999999,"close_button_delay":0,"fi_promotion":null,"close_on_form_submission":false,"close_on_form_submission_delay":0,"close_on_overlay_click":false,"close_on_esc_press":false,"close_on_f4_press":false,"disable_form_reopen":false,"disable_accessibility":false,"theme_slug":"default-theme","id":2612,"slug":"wallet-connect"},"pum-2577":{"triggers":[],"cookies":[],"disable_on_mobile":false,"disable_on_tablet":false,"atc_promotion":null,"explain":null,"type_section":null,"theme_id":2582,"size":"medium","responsive_min_width":"0%","responsive_max_width":"100%","custom_width":"640px","custom_height_auto":false,"custom_height":"380px","scrollable_content":false,"animation_type":"fade","animation_speed":350,"animation_origin":"center top","open_sound":"none","custom_sound":"","location":"center top","position_top":100,"position_bottom":0,"position_left":0,"position_right":0,"position_from_trigger":false,"position_fixed":false,"overlay_disabled":false,"stackable":false,"disable_reposition":false,"zindex":1999999999,"close_button_delay":0,"fi_promotion":null,"close_on_form_submission":false,"close_on_form_submission_delay":0,"close_on_overlay_click":false,"close_on_esc_press":false,"close_on_f4_press":false,"disable_form_reopen":false,"disable_accessibility":false,"theme_slug":"default-theme","id":2577,"slug":"connect"}};
/* ]]> */


/* <![CDATA[ */
var bravepop_global = {"loggedin":"false","isadmin":"false","referer":"","security":"d7c11d696b","goalSecurity":"92a8217ae9","ajaxURL":"https:\/\/xn--metmask-bwa.com\/wp-admin\/admin-ajax.php","field_required":"Required","no_html_allowed":"No Html Allowed","invalid_number":"Invalid Number","invalid_email":"Invalid Email","invalid_url":"Invalid URL","invalid_date":"Invalid Date","fname_required":"First Name is Required.","lname_required":"Last Name is Required.","username_required":"Username is Required.","email_required":"Email is Required.","email_invalid":"Invalid Email addresss.","pass_required":"Password is Required.","pass_short":"Password is too Short.","yes":"Yes","no":"No","login_error":"Something Went Wrong. Please contact the Site administrator.","pass_reset_success":"Please check your Email for the Password reset link.","customFonts":[]};
/* ]]> */




