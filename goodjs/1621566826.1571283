var tagManagerConfig = { tagServer: "https://www.chase.com" };
var analyticsLiteConfig = { svcDomain: "https://analytics.chase.com" };

        <!--Disabling PAGE LOAD event of reporting.js. As report event is called explicitly from dynamic page creation. Hence avoiding duplication.-->
        document.addEventListener('DOMContentLoaded', function(event){CHASE.analytics.disablePageLevelReporting();});
    
var langRedirectURL = "https://www.chase.com/espanol";
var tagManagerConfig = { tagServer: "https://www.chase.com" };

                  requirejs.config({
                    baseUrl: '/c/041721/etc/designs/chase-ux/clientlibs/chase-ux/js',
                    paths: {
                      "adservice": "https://static.chasecdn.com/web/marketing-ui/web-configs/prd/marketing-loader",
                      "content/conf/appsconfig": tagManagerConfig.tagServer + "/etc/chase/appsconfig",
                      "main": "main-index/main"
                    }
                  });
                  define("jquery", [], function () { return jQuery; });
                  define("slotplacement/clientconfig", function() {
                    return {
                      timeout : "4000"
                    }
                  });
                

        require([ "main" ], function() {});
        /* Check for XFS */
        if (top != self) {
            require(["amd/xfs"], function(XFS) {
                XFS.init();
            });
        }
    

            require(["main"], function () {

                var cookieConfig = {
                    homeEquityCookie: false,
                    mortgageCookie: true
                };
                require(["amd/cookie.chase-campaign"], function (ChaseCampaign) {
                    ChaseCampaign.init(cookieConfig);
                });

            });
        
{ "@context" : "http://schema.org",
  "@type" : "Organization",
  "url" : "https://www.chase.com",
  "contactPoint" : [
    { "@type" : "ContactPoint",
      "telephone" : "+1-800-935-9935",
      "contactType" : "Customer support",
      "contactOption" : "TollFree",
      "availableLanguage" : ["English","Spanish"],
      "areaServed" : "US"
    } , {
      "@type" : "ContactPoint",
      "telephone" : "711",
      "contactType" : "Customer support",
      "contactOption" : "HearingImpairedSupported",
      "availableLanguage" : ["English","Spanish"],
      "areaServed" : "US"
    } ] }

    require(["main", "adservice"], function () {
        require(["slotplacement/topic", "amd/browser-message"], function (Topic, BrowserMessage) {
          var options = {
            url: "https://secure.chasecdn.com",
            audienceIds: ""
          };
          Topic.subscribe('adUpdate', function (pageId, data) {
            
            if (data._a) {
              options.audienceIds = data._a;
            }
            BrowserMessage.init(options);
                       
          });
          Topic.subscribe('adError', function () {
                        
            BrowserMessage.init(options)
                        
          });
        });
    });


    require(["main"], function (){
      require(["amd/header","amd/signin-btn","amd/header-navigation","amd/language"], function(Header,SignInBtn,HeaderNavigation,Language) {
        Header.init();
        HeaderNavigation.init();
        SignInBtn.init();
        Language.init();
      });
    });
  

                              require(["main"], function () {
                                require(["amd/dynamic-page-creation"], function (DynamicPage) {
                                  var options = {
                                    
                                    "baseAdPageId":"chasehome_3",
                                    "layouts": [
                                      
                                      {
                                        "id": "returning_a",
                                        "adPageId":"chasehome_3",
                                        "enableScrollAnimation": false,"disableOnMobile": false,
                                        "aboveFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/geoimage/ad-geo/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/carousel/carousel-single-images-10/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtriplet/primary-triplet/_jcr_content/module.html" }
                                        ],
                                        "belowFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile1_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile2_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile3_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bucket/personal/chase-stories/chase-stories-mosaic/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bodycopylite/index-alt-links/_jcr_content/module.html" }
                                        ]
                                      },
                                      {
                                        "id": "prospect_a",
                                        "adPageId":"chasehome_3",
                                        "enableScrollAnimation": false,"disableOnMobile": false,
                                        "aboveFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/geoimage/ad-geo/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/carousel/carousel-single-images/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtriplet/primary-triplet/_jcr_content/module.html" }
                                        ],
                                        "belowFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile1_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile2_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile3_hp/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bucket/personal/chase-stories/chase-stories-mosaic/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bodycopylite/index-alt-links/_jcr_content/module.html" }
                                        ]
                                      },
                                      {
                                        "id": "logoff_a",
                                        "adPageId":"cpo_sign_out",
                                        "enableScrollAnimation": false,"disableOnMobile": false,
                                        "aboveFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/main_tile/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/carousel/carousel-single-images-10/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtriplet/signout-triplet/_jcr_content/module.html" }
                                        ],
                                        "belowFoldModules": [
                                          
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile1_hp_signoff/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile2_hp_signoff/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/adtile2/tile3_hp_signoff/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bucket/personal/chase-stories/chase-stories-mosaic/_jcr_content/module.html" },
                                                    { "url" : "/content/chase-ux/en/structured/module/bodycopylite/index-alt-links/_jcr_content/module.html" }
                                        ]
                                      }
                                    ]
                                  };
                                  DynamicPage.init(options);
                                });
                              });
                            

            require(["main", "adservice"], function () {
              require(["amd/speedbump", "slotplacement/placement", "platform"], function (SpeedBump, Slot, Platform) {
                var loadingView = "placement-spinner";
                if (Platform.name === "IE" && parseFloat(Platform.version) < 10) {
                  loadingView = "none";
                }
                
                var data = {
                    pid : "hero",
                    failoverTreatment : "show",
                    failoverAdId : "50741_Static_Consumer_Multicard_hero_5649",
                    failoverAdUrl : "/content/Creatives/Public/Heroes/2017/Card/Multi-Card/50303_consumer_multicardherounknown5017.dynamic.html",
                    loadingView : loadingView,
                    responsive : true,
                    weblinkClickHandler : function (e) {
                      SpeedBump.execute(e, $(this));
                    }
                };
                var adslot = new Slot(data);
              });
            });
          

          require([ "main", "adservice" ], function() {
            require([ "amd/speedbump", "slotplacement/placement", "platform" ], function(SpeedBump, Slot, Platform) {
              var loadingView = "placement-spinner";
              if (Platform.name === "IE" && parseFloat(Platform.version) < 10) {
                loadingView = "none";
              }

              var data = {
                pid : "trip1",
                failoverTreatment : "hide",
                failoverAdId : "50748_Static_Checking_Awareness_triplet_5676",
                failoverAdUrl : "/content/Creatives/Public/Triplets/2017/Retail/50748_static_checkingawarenesstriplet5676.dynamic.html",
                loadingView : loadingView,
                responsive : true,
                weblinkClickHandler : function(e) {
                  SpeedBump.execute(e, $(this));
                }
              };
              var adslot = new Slot(data);
            });
          });
        

          require([ "main", "adservice" ], function() {
            require([ "amd/speedbump", "slotplacement/placement", "platform" ], function(SpeedBump, Slot, Platform) {
              var loadingView = "placement-spinner";
              if (Platform.name === "IE" && parseFloat(Platform.version) < 10) {
                loadingView = "none";
              }

              var data = {
                pid : "trip2",
                failoverTreatment : "hide",
                failoverAdId : "50743_Static_PropertyBrothers_trip_cwo5659",
                failoverAdUrl : "/content/Creatives/Public/Triplets/2017/HomeFinance/50743_static_propertybrotherstripletcwo5659.dynamic.html",
                loadingView : loadingView,
                responsive : true,
                weblinkClickHandler : function(e) {
                  SpeedBump.execute(e, $(this));
                }
              };
              var adslot = new Slot(data);
            });
          });
        

          require([ "main", "adservice" ], function() {
            require([ "amd/speedbump", "slotplacement/placement", "platform" ], function(SpeedBump, Slot, Platform) {
              var loadingView = "placement-spinner";
              if (Platform.name === "IE" && parseFloat(Platform.version) < 10) {
                loadingView = "none";
              }

              var data = {
                pid : "trip3",
                failoverTreatment : "hide",
                failoverAdId : "50759_Static_CarBuying_triplet_cwo5694",
                failoverAdUrl : "/content/Creatives/Public/Triplets/2017/Auto/50759_static_carbuyingtripletcwo5694.dynamic.html",
                loadingView : loadingView,
                responsive : true,
                weblinkClickHandler : function(e) {
                  SpeedBump.execute(e, $(this));
                }
              };
              var adslot = new Slot(data);
            });
          });
        