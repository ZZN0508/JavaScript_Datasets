var CNN = CNN || {};CNN.pageTimer = {"interval":20,"isVisible":true,"pageType":"section","resetDelay":3,"resetThreshold":17,"sectionName":"intl_homepage"};
if ((typeof window.innerHeight === 'number' && window.innerHeight < 0 && window.innerHeight >= 0)||(typeof document.location.href === 'string' && document.location.href.search(/^http(?:s)?:\/\/edition\.cnn\.com\/\?\d+$/i) !== -1)) {if (typeof window.stop === 'function') {window.stop();} else {document.execCommand('Stop');}}
if (WM.UserConsent.inUserConsentState(["iab","vendor","data-store","ads-contextual","ads-person-prof","ads-person","content-person-prof","content-person","measure-ads","measure-content","measure-market","product-develop"], {id: "outbrain"}) === false) {CNN.Features.enableOutbrain = false;CNN.OutbrainVideoKPISrc = "";CNN.ToggleOutbrain = {};}
(function setRefDom(win, doc, registryFile) {var edition = ((registryFile && registryFile.split('_')[0]) || 'international').toUpperCase(),host = doc.referrer.replace(/^http(?:s)?\:\/\/([\w\-\.]+).*$/i, '$1').toLowerCase();win[edition] = win[edition] || {};win[edition].adTargets = window[edition].adTargets || {};if (host.search(/^([\w\-]+\.)*money\.cnn\.com$/) >= 0) {win[edition].adTargets.refdom = 'money';} else if (host.search(/^([\w\-]+\.)*(www|us|edition|next)\.cnn\.com$/) >= 0) {win[edition].adTargets.refdom = 'cnn';} else if (host === 't.co') {win[edition].adTargets.refdom = 'twitter';} else if (host.search(/^([\w\-]+\.)*facebook\.com$/) >= 0) {win[edition].adTargets.refdom = 'facebook';} else if (host.search(/^([\w\-]+\.)*google\.\w{2,3}(\.\w\w)?$/) >= 0) {win[edition].adTargets.refdom = 'google';} else {win[edition].adTargets.refdom = 'other';}CNN.getRefDom = function getRefDom() {return win[edition].adTargets.refdom;};if (CNN.PageParams && typeof CNN.PageParams.adkey === 'string') {win[edition].adTargets.adkey = CNN.PageParams.adkey;}CNN.getAdkey = function getAdkey() {return win[edition].adTargets.adkey || null;};if (CNN.contentModel.analytics.cep_topics) {win[edition].cep_topics = {buzz: CNN.contentModel.analytics.cep_topics.buzz,cep_brsf: CNN.contentModel.analytics.cep_topics.brsf,cep_iabt: CNN.contentModel.analytics.cep_topics.iabt,cep_sent: CNN.contentModel.analytics.cep_topics.sent,cep_tags: CNN.contentModel.analytics.cep_topics.tags,short_source_id: CNN.contentModel.analytics.cep_topics.shortSource || '',source_id: CNN.contentModel.analytics.cep_topics.source || CNN.contentModel.sourceId || ''};} else {win[edition].cep_topics = {};}CNN.adTargets = win[edition].adTargets;CNN.cep_topics = win[edition].cep_topics;CNN.getCepTopics = function getCepTopics() {var cepTopics = {};function addTopicType(topics, topicType) {var i;if (Array.isArray(topics)) {for (i = 0; i < topics.length; i++) {cepTopics[topics[i]] = topicType;}}}if (win[edition].cep_topics) {addTopicType(win[edition].cep_topics.cep_brsf, 'cep_brsf');addTopicType(win[edition].cep_topics.cep_iabt, 'cep_iabt');addTopicType(win[edition].cep_topics.cep_sent, 'cep_sent');addTopicType(win[edition].cep_topics.cep_tags, 'cep_tags');cepTopics.buzz = win[edition].cep_topics.buzz;cepTopics.short_source_id = win[edition].cep_topics.short_source_id;cepTopics.source_id = win[edition].cep_topics.source_id;}return cepTopics;};CNN.getCapTopics = function getCapTopics() {var altCapTopics = {},capTopics = {},i,topics;if (typeof CNN.contentModel === 'object' && typeof CNN.contentModel.analytics === 'object' &&typeof CNN.contentModel.analytics.cap_topics === 'string') {altCapTopics = CNN.contentModel.analytics.cap_topics.split(/,\s*/);if (Array.isArray(altCapTopics) && altCapTopics[0] && altCapTopics[0] !== 'no-value-set') {topics = altCapTopics;for (i = 0; i < topics.length; i++) {capTopics[topics[i]] = 'cap';}}}return capTopics;};CNN.getProximicData = function getProximicData() {var proximicValues = {},i;if (Array.isArray(window.proximicData)) {for (i = 0; i < window.proximicData.length; i++) {proximicValues[window.proximicData[i]] = 'pconid';}}return proximicValues;};}(window, document, 'cnni_homepage'));CNN.getSpecBranding = function getSpecBranding() {return null;};
try {window.performance.mark("optimizelyStart");} catch (err) {}
if (WM.UserConsent.inUserConsentState(["vendor","data-store","content-person-prof","content-person","measure-ads","measure-content","product-develop"], {id: "optimizely"}) === false) {window.optimizely = window.optimizely || [];window.optimizely.push({ 'type': 'disable' });console.log('Optimizely disabled.');}
try {window.performance.mark("optimizelyEnd");} catch (err) {}
try {window.performance.mark("headEnd");} catch (err) {}
<br>                    !function () {<br>                        var analytics = window.analytics = window.analytics || [];<br>                        if (!analytics.initialize) {<br>                            if (analytics.invoked)<br>                                window.console && console.error && console.error("Segment snippet included twice.");<br>                            else {<br>                                analytics.invoked = !0;<br>                                analytics.methods = ["reset", "track", "ready", "debug", "once", "off", "on"];<br>                                analytics.factory = function (t) {<br>                                    return function () {<br>                                        var e = Array.prototype.slice.call(arguments);<br>                                        e.unshift(t);<br>                                        analytics.push(e);<br>                                        return analytics;<br>                                    }<br>                                };<br>                                for (var t = 0; t < analytics.methods.length; t++) {<br>                                    var e = analytics.methods[t];<br>                                    analytics[e] = analytics.factory(e);<br>                                }<br>                                analytics.load = function (t, e) {<br>                                    var n = document.createElement("script");<br>                                    n.type = "text/javascript";<br>                                    n.async = !0;<br>                                    n.src = "https://cdn.segment.com/analytics.js/v1/" + t + "/analytics.min.js";<br>                                    var a = document.getElementsByTagName("script")[0];<br>                                    a.parentNode.insertBefore(n, a);<br>                                    analytics._loadOptions = e;<br>                                    return analytics;<br>                                };<br>                                analytics.SNIPPET_VERSION = "4.1.0";<br>                            }<br>                        }<br>                    }();

                        if (!window.COMPONENTS) window.COMPONENTS = [];
                        window.COMPONENTS.push({"id":1,"component":"./elements/ui/header-wrapper/header-wrapper.component.jsx","props":{"edition":"international","editions":[{"host":"//us.cnn.com","label":"U.S.","name":"domestic"},{"host":"//edition.cnn.com","label":"International","name":"international"},{"host":"//arabic.cnn.com","label":"Arabic","name":"arabic"},{"host":"//cnnespanol.cnn.com","label":"Español","name":"espanol"}],"enableEditionPicker":true,"enableDaltonTknHeaderCheck":true,"enableUserRegistration":true,"enableWatchLiveButton":true,"layout":"no-rail","nav":{"legal":[{"label":"Terms of Use","url":"/terms","name":"terms-of-use"},{"label":"Privacy Policy","url":"/privacy","name":"privacy-policy"},{"label":"Accessibility & CC","url":"/accessibility","name":"accessibility"},{"label":"AdChoices","url":"#","name":"adchoices"},{"label":"About Us","url":"/about","name":"about-us"},{"label":"Modern Slavery Act Statement","url":"/msa","name":"modern-slavery-act-statement","excludeEdition":"domestic"},{"label":"Advertise with us","url":"https://commercial.cnn.com","name":"advertise-with-us","excludeEdition":"domestic"},{"label":"CNN Store","url":"//store.cnn.com","name":"cnn-store"},{"label":"Newsletters","url":"/newsletters","name":"newsletters"},{"label":"Transcripts","url":"/transcripts","name":"transcripts"},{"label":"License Footage","url":"/collection","name":"license-footage"},{"label":"CNN Newsource","url":"http://cnnnewsource.com","name":"cnn-newsource"},{"label":"Sitemap","url":"https://www.cnn.com/sitemap.html","name":"sitemap"}],"sections":[{"section":"us","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Crime + Justice","name":"crime-and-justice","url":"/specials/us/crime-and-justice"},{"label":"Energy + Environment","name":"energy-and-environment","url":"/specials/us/energy-and-environment"},{"label":"Extreme Weather","name":"extreme-weather","url":"/specials/us/extreme-weather"},{"label":"Space + Science","name":"space-science","url":"/specials/space-science"}]},{"section":"world","enableSectionLink":true,"subs":[{"section":"africa"},{"section":"americas"},{"section":"asia"},{"section":"australia"},{"section":"china"},{"section":"europe"},{"section":"india"},{"section":"middleeast"},{"section":"uk"}]},{"section":"politics","enableSectionLink":true,"labelOverride":{"editions":["international"],"label":"US Politics"},"subs":[{"label":"The Biden Presidency","name":"the-biden-presidency","url":"/specials/politics/joe-biden-news"},{"label":"Facts First","name":"facts-first","url":"/specials/politics/fact-check-politics"},{"label":"US Elections","name":"us-elections","url":"/election/2020/results/president"}]},{"section":"business","deepNav":true,"enableSectionLink":true,"subs":[{"label":"Markets","url":"https://money.cnn.com/data/markets/","name":"markets","subs":[{"label":"Premarkets","url":"https://money.cnn.com/data/premarket/","name":"premarkets"},{"label":"Dow","url":"https://money.cnn.com/data/markets/dow/","name":"dow-30"},{"label":"After-Hours","url":"https://money.cnn.com/data/afterhours/","name":"after-hours"},{"label":"Market Movers","url":"https://money.cnn.com/data/hotstocks/","name":"market-movers"},{"label":"Fear & Greed","url":"https://money.cnn.com/data/fear-and-greed/","name":"fear-greed"},{"label":"World Markets","url":"https://money.cnn.com/data/world_markets/americas/","name":"world-markets"},{"label":"Investing","url":"/business/investing","name":"investing"},{"label":"Markets Now","url":"https://money.cnn.com/investing/markets-now","name":"markets-now"},{"label":"Before the Bell","url":"/specials/investing/before-the-bell","name":"before-the-bell"},{"label":"Leading Indicator","url":"/specials/investing/leading-indicator","name":"leading-indicator"},{"label":"Global Energy Challenge","url":"/specials/business/global-energy-challenge","name":"global-energy-challenge"},{"label":"Economy","url":"/business/economy","name":"economy"},{"label":"Tracking America's Recovery","url":"/business/us-economic-recovery-coronavirus","name":"coronavirus-recovery"},{"label":"Energy","url":"/business/energy","name":"energy"},{"label":"Money","url":"/business/money","name":"money"}]},{"section":"tech","subs":[{"label":"Innovate","url":"/specials/tech/innovate","name":"innovate"},{"label":"Gadget","url":"/specials/tech/gadget","name":"gadget"},{"label":"Foreseeable Future","url":"/specials/tech/foreseeable-future","name":"foreseeable-future"},{"label":"Mission: Ahead","url":"/specials/tech/mission-ahead","name":"mission-ahead"},{"label":"Upstarts","url":"/specials/tech/upstarts","name":"upstarts"},{"label":"Business Evolved","url":"/specials/tech/business-evolved","name":"business-evolved"},{"label":"Innovative Cities","url":"/specials/tech/innovative-cities","name":"innovative-cities"},{"label":"Unhackable","url":"/specials/tech/unhackable","name":"unhackable"}]},{"section":"media","subs":[{"label":"Reliable Sources","url":"/shows/reliable-sources","name":"reliable-sources"}]},{"section":"success","subs":[{"label":"Boss Files","url":"/specials/success/boss-files","name":"boss-files"},{"label":"Risk Takers","url":"/interactive/2019/business/risk-takers","name":"risk-takers"},{"label":"Fresh Money","url":"/specials/success/fresh-money","name":"fresh-money"},{"label":"Invest Ahead","url":"/specials/success/invest-ahead","name":"invest-ahead"},{"label":"Work Transformed","url":"/specials/tech/work-transformed","name":"work-transformed"},{"label":"Cars","url":"/business/cars","name":"cars"},{"label":"Homes","url":"/business/homes","name":"homes"},{"label":"Wealth Coach","url":"/specials/success/wealth-coach","name":"wealth-coach"}]},{"label":"Center Piece","url":"/specials/business/center-piece","name":"center-piece","enableSectionLink":false,"disableInMegaNavSubLinks":true},{"section":"perspectives"},{"section":"business-videos","labelOverride":{"editions":["domestic","international"],"label":"Videos"}},{"label":"International","url":"https://edition.cnn.com/business","name":"international-business","enableSectionLink":false,"disableInMegaNavSubLinks":true,"subs":[{"label":"Switzerland","url":"https://www.cnnmoney.ch","name":"switzerland"},{"label":"India","url":"/business/india","name":"business-india"},{"label":"Davos","url":"/specials/business/davos/","name":"davos"},{"label":"Reliable Sources","url":"/shows/reliable-sources","name":"reliable-sources"},{"label":"Passion to Portfolio","url":"/specials/business/passion-to-portfolio","name":"passion-portfolio"},{"label":"On: Germany","url":"/specials/business/on-germany","name":"on-germany"}]},{"label":"More","enableSectionLink":false,"disableInMegaNavSubLinks":true,"subs":[{"label":"Accessibility & CC","url":"/accessibility","name":"accessibility"},{"label":"About Us","url":"/about","name":"about-us"},{"label":"Newsletters","url":"/newsletters","name":"newsletters"}]}]},{"section":"opinions","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Political Op-Eds","name":"opinion-politics","url":"/specials/opinion/opinion-politics"},{"label":"Social Commentary","name":"opinion-social-issues","url":"/specials/opinion/opinion-social-issues"}]},{"section":"health","enableSectionLink":true,"subs":[{"label":"Food","name":"food","url":"/specials/health/food-diet"},{"label":"Fitness","name":"fitness","url":"/specials/health/fitness-excercise"},{"label":"Wellness","name":"wellness","url":"/specials/health/wellness"},{"label":"Parenting","name":"parenting","url":"/specials/health/parenting"},{"label":"Vital Signs","name":"vital-signs","url":"/specials/health/vital-signs"}]},{"section":"entertainment","enableSectionLink":true,"subs":[{"label":"Stars","name":"stars","url":"/entertainment/celebrities"},{"label":"Screen","name":"screen","url":"/entertainment/movies"},{"label":"Binge","name":"binge","url":"/entertainment/tv-shows"},{"label":"Culture","name":"culture","url":"/entertainment/culture"},{"label":"Media","name":"media","url":"/business/media"}]},{"section":"tech","enableSectionLink":false,"subs":[{"label":"Innovate","name":"innovate","url":"/specials/tech/innovate"},{"label":"Gadget","name":"gadget","url":"/specials/tech/gadget"},{"label":"Foreseeable Future","name":"foreseeable-future","url":"/specials/tech/foreseeable-future"},{"label":"Mission: Ahead","name":"mission-ahead","url":"/specials/tech/mission-ahead"},{"label":"Upstarts","name":"upstarts","url":"/specials/tech/upstarts"},{"label":"Work Transformed","name":"work-transformed","url":"/specials/tech/work-transformed"},{"label":"Innovative Cities","name":"innovative-cities","url":"/specials/tech/innovative-cities"}]},{"section":"style","enableSectionLink":true,"subs":[{"label":"Arts","section":"arts","url":"/style/arts"},{"label":"Design","section":"design","url":"/style/design"},{"label":"Fashion","section":"fashion","url":"/style/fashion"},{"label":"Architecture","section":"architecture","url":"/style/architecture"},{"label":"Luxury","section":"luxury","url":"/style/luxury"},{"label":"Beauty","section":"beauty","url":"/style/beauty"},{"label":"Video","section":"style-videos","url":"/style/videos"}]},{"section":"travel","enableSectionLink":true,"subs":[{"label":"Destinations","section":"destinations","url":"/travel/destinations"},{"label":"Food & Drink","section":"foodanddrink","url":"/travel/food-and-drink"},{"label":"Stay","section":"travel-stay","url":"/travel/stay"},{"label":"News","section":"travel-news","url":"/travel/news"},{"label":"Videos","section":"travel-videos","url":"/travel/videos"}]},{"label":"Sports","section":"bleacher","name":"bleacher","url":"http://bleacherreport.com","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Pro Football","name":"nfl","url":"http://bleacherreport.com/nfl"},{"label":"College Football","name":"college-football","url":"http://bleacherreport.com/college-football"},{"label":"Basketball","name":"nba","url":"http://bleacherreport.com/nba"},{"label":"Baseball","name":"mlb","url":"http://bleacherreport.com/mlb"},{"label":"Soccer","name":"world-football","url":"http://bleacherreport.com/world-football"},{"label":"Olympics","name":"olympics","url":"/sport/olympics"}]},{"section":"sport","enableSectionLink":true,"excludeEdition":"domestic","name":"sports","labelOverride":{"editions":["international"],"label":"Sports"},"subs":[{"section":"football"},{"section":"tennis"},{"section":"golf"},{"section":"olympics"},{"label":"US Sports","name":"us-sports","url":"/specials/sport/us-sports"},{"label":"Climbing","name":"climbing","url":"/specials/climbing"},{"section":"motorsport"},{"label":"Formula E","name":"formula-e","url":"/specials/sport/formula-e"},{"label":"Esports","name":"esports","url":"/specials/esports"}]},{"section":"videos","enableSectionLink":true,"subs":[{"label":"Live TV ","name":"live-tv","url":"//cnn.it/go2"},{"label":"Digital Studios","name":"digital-studios","url":"/specials/digital-studios"},{"label":"CNN Films","name":"digital-shorts","url":"/specials/videos/digital-shorts"},{"label":"HLN","name":"hln","url":"/specials/videos/hln"},{"label":"TV Schedule","name":"tv-schedule","url":"/tv/schedule/cnn"},{"label":"TV Shows A-Z","name":"all-shows","url":"/specials/tv/all-shows"},{"label":"CNNVR","name":"vr","url":"/vr"}]},{"label":"Audio","name":"audio","section":"Audio","url":"/audio","enableSectionLink":false,"excludeEdition":"international","subs":[]},{"section":"features","label":"Features","name":"features","disableMegaNavLink":false,"enableSectionLink":false,"excludeEdition":"domestic","url":"/specials","subs":[{"label":"As Equals","name":"as-equals","url":"/interactive/asequals/"},{"label":"Call to Earth","name":"call-to-earth","url":"/interactive/call-to-earth/"},{"label":"Freedom Project","name":"freedom-project","url":"/specials/world/freedom-project"},{"label":"Impact Your World","name":"impact-your-world","url":"/specials/impact-your-world"},{"label":"Inside Africa","name":"inside-africa","url":"/specials/africa/inside-africa"},{"label":"2 Degrees","name":"two-degrees","url":"/specials/opinions/two-degrees"},{"label":"CNN Heroes","name":"cnn-heroes","url":"/specials/cnn-heroes"},{"label":"All Features","name":"all-features","url":"/specials"}]},{"label":"Coupons","name":"coupons","section":"Coupons","url":"//coupons.cnn.com","enableSectionLink":false,"excludeEdition":"international","subs":[{"label":"CNN Underscored","name":"cnn-underscored","url":"/cnn-underscored/"},{"label":"Explore","name":"underscored-explore","url":"/specials/cnn-underscored/explore/"},{"label":"Wellness","name":"underscored-wellness","url":"/specials/cnn-underscored/wellness/"},{"label":"Gadgets","name":"underscored-gadgets","url":"/specials/cnn-underscored/gadgets/"},{"label":"Lifestyle","name":"underscored-lifestyle","url":"/specials/cnn-underscored/lifestyle/"},{"label":"CNN Store","name":"cnn-store","url":"//store.cnn.com/?utm_source=cnn.com&utm_medium=referral&utm_campaign=navbar"}]},{"section":"vr","disableMegaNavLink":true,"enableSectionLink":false,"subs":[{"label":"How To Watch VR","name":"how-to-watch-vr","url":"/2017/03/04/vr/how-to-watch-vr"},{"label":"Archives","name":"vr-archives","url":"/specials/vr/vr-archives"}]},{"section":"weather","disableMegaNavLink":false,"enableSectionLink":false,"subs":[{"label":"Climate","name":"climate","url":"/specials/world/cnn-climate"},{"label":"Storm Tracker","name":"storm-tracker","url":"/interactive/2020/weather/gonzalo-storm-path-tracker/index.html"},{"label":"Wildfire Tracker","name":"wildfire-tracker","url":"/interactive/2020/weather/wildfire-and-air-quality-tracker/"},{"label":"Video","name":"weather-video","url":"/specials/weather/weather-video"}]},{"section":"more","name":"more","enableSectionLink":false,"subs":[{"label":"Photos","name":"photos","url":"/specials/photos"},{"label":"Longform","name":"longform","url":"/specials/cnn-longform"},{"label":"Investigations","name":"cnn-investigates","url":"/specials/cnn-investigates"},{"label":"CNN Profiles","name":"profiles","url":"/specials/profiles"},{"label":"CNN Leadership","name":"leadership","url":"/specials/more/cnn-leadership"},{"label":"CNN Newsletters","name":"newsletters","url":"/email/subscription"},{"label":"Work for CNN","name":"jobs","url":"https://www.turnerjobs.com/search-jobs?orgIds=1174&ac=19299"}]}],"social":{"domestic":{"links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/CNN"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNN"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"}]},"international":{"links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnninternational"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/cnni"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"}]},"business":{"entity":"Business","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnnbusiness"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNNbusiness"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnnbusiness"}]},"politics":{"entity":"Politics","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnnpolitics"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/cnnpolitics"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"},{"label":"YouTube","name":"youtube","url":"//youtube.com/user/CNN"}]},"entertainment":{"entity":"Entertainment","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/CNNent"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNNent"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnnentertainment"}]}},"userAccount":[{"label":"Settings","name":"userSettings","url":"/account/settings"},{"label":"Log Out","name":"userLogout","url":"#"}]},"pageType":"section","searchUrl":"/search","sectionName":"intl_homepage","sectionsInfo":{"africa":{"basePath":"/africa","canonicalSite":"www","children":[],"isSubsection":true,"label":"Africa","parent":"intl_regions","sites":["www","edition"],"title":"Africa News - Breaking News, Video, Headlines and Opinion","uri":"/africa/index.html","name":"africa","sectionPath":"/africa"},"airport-delays":{"basePath":"/airport-delays","canonicalSite":"www","children":[],"isSubsection":false,"label":"Airport Delays","sites":["www","edition"],"title":"Airport Delays","uri":"/airport-delays/index.html","name":"airport-delays","sectionPath":"/airport-delays"},"americas":{"basePath":"/americas","canonicalSite":"www","children":[],"isSubsection":true,"label":"Americas","parent":"intl_regions","sites":["www","edition"],"title":"Americas News - Breaking News, Video, Headlines and Opinion","uri":"/americas/index.html","name":"americas","sectionPath":"/americas"},"app-health-section":{"basePath":"/app-health-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Health Section","sites":["www","edition"],"title":"","uri":"/app-health-section/index.html","name":"app-health-section","sectionPath":"/app-health-section"},"app-international-edition":{"basePath":"/app-international-edition","canonicalSite":"app","children":[],"isSubsection":false,"label":"App International Edition","sites":["www","edition"],"title":"","uri":"/app-international-edition/index.html","name":"app-international-edition","sectionPath":"/app-international-edition"},"app-money-section":{"basePath":"/app-money-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Money Section","sites":["www","edition"],"title":"","uri":"/app-money-section/index.html","name":"app-money-section","sectionPath":"/app-money-section"},"app-news-section":{"basePath":"/app-news-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App News Section","sites":["www","edition"],"title":"","uri":"/app-news-section/index.html","name":"app-news-section","sectionPath":"/app-news-section"},"app-opinion-section":{"basePath":"/app-opinion-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Opinion Section","sites":["www","edition"],"title":"","uri":"/app-opinion-section/index.html","name":"app-opinion-section","sectionPath":"/app-opinion-section"},"app-politics-section":{"basePath":"/app-politics-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Politics Section","sites":["www","edition"],"title":"","uri":"/app-politics-section/index.html","name":"app-politics-section","sectionPath":"/app-politics-section"},"app-specials":{"basePath":"/app-specials","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Specials","sites":["www","edition"],"title":"","uri":"/app-specials/index.html","name":"app-specials","sectionPath":"/app-specials"},"app-sports-section":{"basePath":"/app-sports-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Sports Section","sites":["www","edition"],"title":"","uri":"/app-sports-section/index.html","name":"app-sports-section","sectionPath":"/app-sports-section"},"app-style-section":{"basePath":"/app-style-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Style Section","sites":["www","edition"],"title":"","uri":"/app-style-section/index.html","name":"app-style-section","sectionPath":"/app-style-section"},"app-tech-section":{"basePath":"/app-tech-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Tech Section","sites":["www","edition"],"title":"","uri":"/app-tech-section/index.html","name":"app-tech-section","sectionPath":"/app-tech-section"},"app-travel-section":{"basePath":"/app-travel-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Travel Section","sites":["www","edition"],"title":"","uri":"/app-travel-section/index.html","name":"app-travel-section","sectionPath":"/app-travel-section"},"architecture":{"basePath":"/style/architecture","canonicalSite":"www","children":[],"isSubsection":true,"label":"Architecture","parent":"style","sectionPath":"/architecture","sites":["www","edition"],"title":"Architecture","uri":"/style/architecture/index.html","name":"architecture"},"area51":{"basePath":"/area51","canonicalSite":"www","children":[],"isSubsection":false,"label":"Area 51","sites":["www","edition"],"title":"Area 51","uri":"/area51/index.html","name":"area51","sectionPath":"/area51"},"arts":{"basePath":"/style/arts","canonicalSite":"www","children":[],"isSubsection":true,"label":"Arts","parent":"style","sectionPath":"/arts","sites":["www","edition"],"title":"Arts","uri":"/style/arts/index.html","name":"arts"},"asia":{"basePath":"/asia","canonicalSite":"www","children":["china","india"],"isSubsection":true,"label":"Asia","parent":"intl_regions","sites":["www","edition"],"title":"Asia News - Breaking News, Video, Headlines and Opinion","uri":"/asia/index.html","name":"asia","sectionPath":"/asia"},"australia":{"basePath":"/australia","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Australia","parent":"asia","sites":["www","edition"],"title":"Australia News - Breaking News, Video, Headlines and Opinion","uri":"/australia/index.html","name":"australia","sectionPath":"/australia"},"autos":{"basePath":"/style/autos","canonicalSite":"www","children":[],"isSubsection":true,"label":"Autos","parent":"style","sectionPath":"/autos","sites":["www","edition"],"title":"Autos","uri":"/style/autos/index.html","name":"autos"},"aviation":{"basePath":"/travel/aviation","canonicalSite":"www","children":[],"isSubsection":true,"label":"Aviation","parent":"travel","sectionPath":"/aviation","sites":["www","edition"],"title":"Innovation in Aviation from Airplanes to Airports","uri":"/travel/aviation/index.html","name":"aviation"},"beauty":{"basePath":"/style/beauty","canonicalSite":"www","children":[],"isSubsection":true,"label":"Beauty","parent":"style","sectionPath":"/beauty","sites":["www","edition"],"title":"Beauty","uri":"/style/beauty/index.html","name":"beauty"},"business":{"basePath":"/business","canonicalSite":"www","children":["business-india","business-videos","cars","economy","energy","homes","investing","media","perspectives","success","tech"],"displayLabel":"","isSubsection":false,"label":"Business","sites":["www"],"title":"Business","uri":"/business/index.html","name":"business","sectionPath":"/business"},"business-food":{"basePath":"/business-food","canonicalSite":"www","children":[],"displayLabel":"Food","isSubsection":true,"label":"Business - Food","parent":"business","sectionPath":"/business-food","sites":["www","edition"],"title":"Business - Food","uri":"/business/food/index.html","name":"business-food"},"business-india":{"basePath":"/business-india","canonicalSite":"www","children":[],"displayLabel":"India","isSubsection":true,"label":"Business - India","parent":"business","sectionPath":"/business-india","sites":["www","edition"],"title":"Business - India","uri":"/business/india/index.html","name":"business-india"},"business-planning":{"adsName":"business","basePath":"/business-planning","canonicalSite":"www","children":[],"displayLabel":"Planning","isSubsection":true,"label":"Business Planning","sites":["www","edition"],"title":"Business Planning","uri":"/business-planning/index.html","name":"business-planning","sectionPath":"/business-planning"},"business-videos":{"adsName":"video","basePath":"/business-videos","canonicalSite":"www","children":[],"displayLabel":"Video","isSubsection":true,"label":"Business Videos","parent":"business","sites":["www","edition"],"title":"Business Videos","uri":"/business/videos/index.html","name":"business-videos","sectionPath":"/business-videos"},"celebrities":{"basePath":"/entertainment/celebrities","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Celebrities","parent":"entertainment","sectionPath":"/celebrities","sites":["www","edition"],"title":"Celebrities - Entertainment News","uri":"/entertainment/celebrities/index.html","name":"celebrities"},"china":{"basePath":"/china","canonicalSite":"www","children":[],"isSubsection":true,"label":"China","parent":"asia","sites":["www","edition"],"title":"China News - Breaking News, Video, Headlines and Opinion","uri":"/china/index.html","name":"china","sectionPath":"/china"},"cnn-underscored":{"basePath":"/cnn-underscored","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN Underscored","sites":["www","edition"],"title":"Product Reviews, Gift Ideas, Gadget Guides and More","uri":"/cnn-underscored/index.html","name":"cnn-underscored","sectionPath":"/cnn-underscored"},"cnn10":{"basePath":"/cnn10","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN 10","sites":["www","edition"],"title":"CNN 10","uri":"/cnn10/index.html","name":"cnn10","sectionPath":"/cnn10"},"cnnmoney":{"basePath":"/","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN Money","sites":["www","edition"],"title":"CNN Money","uri":"","name":"cnnmoney","sectionPath":"/"},"culture":{"basePath":"/entertainment/culture","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Culture","parent":"entertainment","sectionPath":"/culture","sites":["www","edition"],"title":"Pop Culture - Entertainment News","uri":"/entertainment/culture/index.html","name":"culture"},"design":{"basePath":"/style/design","canonicalSite":"www","children":[],"isSubsection":true,"label":"Design","parent":"style","sectionPath":"/design","sites":["www","edition"],"title":"Design","uri":"/style/design/index.html","name":"design"},"destinations":{"basePath":"/travel/destinations","canonicalSite":"www","children":[],"isSubsection":true,"label":"Destinations","parent":"travel","sectionPath":"/destinations","sites":["www","edition"],"title":"Destinations","uri":"/travel/destinations/index.html","name":"destinations"},"economy":{"basePath":"/economy","canonicalSite":"www","children":[],"isSubsection":true,"label":"Economy","parent":"business","sites":["www","edition"],"title":"Business","uri":"/business/economy/index.html","name":"economy","sectionPath":"/economy"},"election-2018":{"adsName":"elections","basePath":"/election","canonicalSite":"www","children":[],"isSubsection":true,"label":"Election 2018","parent":"politics","sites":["www","edition"],"title":"2018 Elections","uri":"/election/index.html","name":"election-2018","sectionPath":"/election"},"election-center-2016":{"basePath":"/election/2016","canonicalSite":"www","children":[],"isSubsection":true,"label":"Election Center 2016","parent":"politics","sites":["www","edition"],"title":"2016 Elections","uri":"/election/2016/index.html","name":"election-center-2016","sectionPath":"/election/2016"},"entertainment":{"basePath":"/entertainment","canonicalSite":"www","children":["celebrities","culture","movies","tv-shows"],"displayLabel":"","isSubsection":false,"label":"Entertainment","sites":["www","edition"],"title":"Entertainment News - Celebrities, Movies, TV, Music","uri":"/entertainment/index.html","name":"entertainment","sectionPath":"/entertainment"},"equestrian":{"basePath":"/sport/equestrian","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Equestrian","parent":"sport","sectionPath":"/equestrian","sites":["www","edition"],"title":"Equestrian News","uri":"/sport/equestrian/index.html","name":"equestrian"},"europe":{"basePath":"/europe","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Europe","parent":"intl_regions","sites":["www","edition"],"title":"Europe News - Breaking News, Video, Headlines and Opinion","uri":"/europe/index.html","name":"europe","sectionPath":"/europe"},"fashion":{"basePath":"/style/fashion","canonicalSite":"www","children":[],"isSubsection":true,"label":"Fashion","parent":"style","sectionPath":"/fashion","sites":["www","edition"],"title":"Fashion","uri":"/style/fashion/index.html","name":"fashion"},"foodanddrink":{"basePath":"/travel/food-and-drink","canonicalSite":"www","children":[],"isSubsection":true,"label":"Food and Drink","parent":"travel","sectionPath":"/foodanddrink","sites":["www","edition"],"title":"Food & Drink","uri":"/travel/food-and-drink/index.html","name":"foodanddrink"},"football":{"basePath":"/sport/football","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Football","parent":"sport","sectionPath":"/football","sites":["www","edition"],"title":"Football News","uri":"/sport/football/index.html","name":"football"},"golf":{"basePath":"/sport/golf","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Golf","parent":"sport","sectionPath":"/golf","sites":["www","edition"],"title":"Golf News","uri":"/sport/golf/index.html","name":"golf"},"health":{"basePath":"/health","canonicalSite":"www","children":[],"isSubsection":false,"label":"Health","logo":"//cdn.cnn.com/cnn/.e1mo/img/4.0/logos/cnn_health_banner.png","sites":["www","edition"],"title":"Health News","uri":"/health/index.html","name":"health","sectionPath":"/health"},"homepage":{"basePath":"/","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Domestic Homepage","sites":["www"],"title":"Breaking News, Latest News and Videos","uri":"/index.html","name":"homepage","sectionPath":"/"},"homepage-magellan":{"basePath":"/","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Homepage Magellan","sites":["www","edition"],"title":"Breaking News, U.S., World, Weather, Entertainment & Video News","uri":"/index3.html","name":"homepage-magellan","sectionPath":"/"},"horseracing":{"adsName":"winningpost","basePath":"/sport/horse-racing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Horse Racing","parent":"sport","sectionPath":"/horseracing","sites":["www","edition"],"title":"Horse Racing News","uri":"/sport/horse-racing/index.html","name":"horseracing"},"hotels":{"basePath":"/travel/hotels","canonicalSite":"www","children":[],"isSubsection":true,"label":"Hotels","parent":"travel","sectionPath":"/hotels","sites":["www","edition"],"title":"Worldwide Inspiration for Hotel Stays","uri":"/travel/hotels/index.html","name":"hotels"},"india":{"basePath":"/india","canonicalSite":"edition","children":[],"isSubsection":true,"label":"India","parent":"asia","sites":["www","edition"],"title":"India News - Breaking News, Video, Headlines and Opinion","uri":"/india/index.html","name":"india","sectionPath":"/india"},"intl_business":{"adsName":"business","basePath":"/business","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Business","sites":["edition"],"title":"CNN Business","uri":"/business/intl_index.html","name":"intl_business","sectionPath":"/business"},"intl_entertainment":{"basePath":"/entertainment","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Entertainment","sites":["edition"],"title":"Entertainment News - Celebrities, Movies, TV, Music","uri":"/entertainment/intl_index.html","name":"intl_entertainment","sectionPath":"/entertainment"},"intl_homepage":{"basePath":"/","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"International Homepage","sites":["edition"],"title":"Breaking News, US News, World News and Video","uri":"/intl_index.html","name":"intl_homepage","sectionPath":"/"},"intl_more":{"basePath":"/more","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - More","sites":["edition"],"title":"More From CNN","uri":"/more/intl_index.html","name":"intl_more","sectionPath":"/more"},"intl_regions":{"adsName":"regions","basePath":"/regions","canonicalSite":"edition","children":["africa","americas","asia","australia","china","europe","india","middleeast","uk"],"isSubsection":false,"label":"Intl - Regions","sites":["edition"],"title":"World News - Breaking News, Video, Headlines and Opinion","uri":"/regions/intl_index.html","name":"intl_regions","sectionPath":"/regions"},"intl_travel":{"adsName":"travel","basePath":"/travel","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - Travel","sites":["edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel/intl_index.html","name":"intl_travel","sectionPath":"/travel"},"intl_tv":{"basePath":"/tv","canonicalSite":"edition","children":["intl_tv-schedule-americas","intl_tv-schedule-asia","intl_tv-schedule-europe","intl_tv-shows"],"isSubsection":false,"label":"Intl - TV","sites":["edition"],"title":"CNN International TV","uri":"/tv/intl_index.html","name":"intl_tv","sectionPath":"/tv"},"intl_tv-schedule-americas":{"basePath":"/tv/schedule/americas","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Americas","parent":"intl_tv","sites":["edition"],"title":"Americas TV Schedule","uri":"/tv/schedule/americas/index.html","name":"intl_tv-schedule-americas","sectionPath":"/tv/schedule/americas"},"intl_tv-schedule-asia":{"basePath":"/tv/schedule/asia","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Asia","parent":"intl_tv","sites":["edition"],"title":"Asia TV Schedule","uri":"/tv/schedule/asia/index.html","name":"intl_tv-schedule-asia","sectionPath":"/tv/schedule/asia"},"intl_tv-schedule-europe":{"basePath":"/tv/schedule/europe","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Europe","parent":"intl_tv","sites":["edition"],"title":"Europe TV Schedule","uri":"/tv/schedule/europe/index.html","name":"intl_tv-schedule-europe","sectionPath":"/tv/schedule/europe"},"intl_tv-shows":{"basePath":"/tv/shows","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Shows","parent":"intl_tv","sites":["edition"],"title":"International TV Shows","uri":"/tv/shows/intl_index.html","name":"intl_tv-shows","sectionPath":"/tv/shows"},"intl_videos":{"basePath":"/videos","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Videos","sites":["edition"],"title":"Video News","uri":"/videos/intl_index.html","name":"intl_videos","sectionPath":"/videos"},"intl_world":{"adsName":"world","basePath":"/world","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - World","sites":["edition"],"title":"World News","uri":"/world/intl_index.html","name":"intl_world","sectionPath":"/world"},"investing":{"basePath":"investing","canonicalSite":"www","children":[],"isSubsection":true,"label":"Investing","parent":"business","sites":["www","edition"],"title":"Investing","uri":"/business/investing/index.html","name":"investing","sectionPath":"investing"},"living":{"basePath":"/living","canonicalSite":"www","children":[],"isSubsection":false,"label":"Living","sites":["www","edition"],"title":"Living News","uri":"/living/index.html","name":"living","sectionPath":"/living"},"luxury":{"basePath":"/style/luxury","canonicalSite":"www","children":[],"isSubsection":true,"label":"Luxury","parent":"style","sectionPath":"/luxury","sites":["www","edition"],"title":"Luxury","uri":"/style/luxury/index.html","name":"luxury"},"media":{"basePath":"/media","canonicalSite":"www","children":[],"isSubsection":true,"label":"Media","parent":"business","sites":["www","edition"],"title":"Media","uri":"/business/media/index.html","name":"media","sectionPath":"/media"},"middleeast":{"basePath":"/middle-east","canonicalSite":"www","children":[],"isSubsection":true,"label":"Middle East","parent":"intl_regions","sites":["www","edition"],"title":"Middle East News - Breaking News, Video, Headlines and Opinion","uri":"/middle-east/index.html","name":"middleeast","sectionPath":"/middle-east"},"more":{"basePath":"/more","canonicalSite":"www","children":[],"isSubsection":false,"label":"More","sites":["www"],"title":"More From CNN","uri":"/more/index.html","name":"more","sectionPath":"/more"},"motorsport":{"basePath":"/sport/motorsport","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Motorsport","parent":"sport","sectionPath":"/motorsport","sites":["www","edition"],"title":"Motorsport News","uri":"/sport/motorsport/index.html","name":"motorsport"},"movies":{"basePath":"/entertainment/movies","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Movies","parent":"entertainment","sectionPath":"/movies","sites":["www","edition"],"title":"Movies - Entertainment News","uri":"/entertainment/movies/index.html","name":"movies"},"news":{"basePath":"/travel/news","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel - News","parent":"travel","sectionPath":"/news","sites":["www","edition"],"title":"Travel - News","uri":"/travel/news/index.html","name":"news"},"olympics":{"basePath":"/sport/olympics","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Olympics","parent":"sport","sectionPath":"/olympics","sites":["www","edition"],"title":"2020 Summer Olympics in Tokyo, Japan","uri":"/sport/olympics/index.html","name":"olympics"},"opinions":{"adsName":"opinion","basePath":"/opinions","canonicalSite":"www","children":[],"isSubsection":false,"label":"Opinion","sites":["www"],"title":"Opinion, Commentary, Analysis","uri":"/opinions/index.html","name":"opinions","sectionPath":"/opinions"},"perspectives":{"basePath":"/perspectives","canonicalSite":"www","children":[],"isSubsection":true,"label":"Perspectives","parent":"business","sites":["www","edition"],"title":"Perspectives","uri":"/business/perspectives/index.html","name":"perspectives","sectionPath":"/perspectives"},"energy":{"basePath":"/energy","canonicalSite":"www","children":[],"isSubsection":true,"label":"Energy","parent":"business","sites":["www","edition"],"title":"Energy","uri":"/business/energy/index.html","name":"energy","sectionPath":"/energy"},"cars":{"basePath":"/cars","canonicalSite":"www","children":[],"isSubsection":true,"label":"Cars","parent":"business","sites":["www","edition"],"title":"Cars","uri":"/business/cars/index.html","name":"cars","sectionPath":"/cars"},"homes":{"basePath":"/homes","canonicalSite":"www","children":[],"isSubsection":true,"label":"Homes","parent":"business","sites":["www","edition"],"title":"Homes","uri":"/business/homes/index.html","name":"homes","sectionPath":"/homes"},"play":{"basePath":"/travel/play","canonicalSite":"www","children":[],"isSubsection":true,"label":"Play","parent":"travel","sectionPath":"/travel-play","sites":["www","edition"],"title":"What To Do","uri":"/travel/play/index.html","name":"play"},"politics":{"basePath":"/politics","canonicalSite":"www","children":["election-2018","election-center-2016"],"displayLabel":"","isSubsection":false,"label":"Politics","sites":["www","edition"],"title":"Political News, Analysis and Opinion","uri":"/politics/index.html","name":"politics","sectionPath":"/politics"},"profiles":{"basePath":"/profiles","canonicalSite":"www","children":[],"displayLabel":"CNN Profiles","isSubsection":false,"label":"Profiles","sites":["www","edition"],"title":"CNN Profiles","uri":"/profiles/index.html","name":"profiles","sectionPath":"/profiles"},"sailing":{"adsName":"mainsail","basePath":"/sport/sailing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Sailing","parent":"sport","sectionPath":"/sailing","sites":["www","edition"],"title":"Sailing News","uri":"/sport/sailing/index.html","name":"sailing"},"skiing":{"basePath":"/sport/skiing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Skiing","parent":"sport","sectionPath":"/skiing","sites":["www","edition"],"title":"Skiing News","uri":"/sport/skiing/index.html","name":"skiing"},"sport":{"adsName":"worldsport","basePath":"/sport","canonicalSite":"edition","children":["equestrian","football","golf","horseracing","motorsport","olympics","sailing","skiing","tennis"],"isSubsection":false,"label":"Sports","sites":["www","edition"],"title":"Sport News","uri":"/sport/index.html","name":"sport","sectionPath":"/sport"},"sports":{"basePath":"/sports","canonicalSite":"www","children":[],"isSubsection":false,"label":"Sports","sites":["www"],"title":"Sports News","uri":"/sports/index.html","name":"sports","sectionPath":"/sports"},"stay":{"basePath":"/travel/stay","canonicalSite":"www","children":[],"isSubsection":true,"label":"Stay","parent":"travel","sectionPath":"/travel-stay","sites":["www","edition"],"title":"Places to Stay","uri":"/travel/stay/index.html","name":"stay"},"style":{"basePath":"/style","canonicalSite":"www","children":["architecture","arts","autos","beauty","design","fashion","luxury"],"isSubsection":false,"label":"Style","sites":["www","edition"],"title":"CNN Style - Fashion, Design, Art, Architecture and Luxury","uri":"/style/index.html","name":"style","sectionPath":"/style"},"style-home":{"basePath":"/style-home","canonicalSite":"www","children":[],"isSubsection":true,"label":"Style - Home","parent":"style","sites":["www","edition"],"title":"CNN Style - Fashion, Design, Art, Architecture and Luxury","uri":"/style-home/index.html","name":"style-home","sectionPath":"/style-home"},"style-show":{"basePath":"/style-show","canonicalSite":"www","children":[],"isSubsection":true,"label":"Style - Show","parent":"style","sites":["www","edition"],"title":"Style Show","uri":"/style-show/index.html","name":"style-show","sectionPath":"/style-show"},"success":{"basePath":"/success","canonicalSite":"www","children":[],"isSubsection":true,"label":"Success","parent":"business","sites":["www","edition"],"title":"Success","uri":"/business/success/index.html","name":"success","sectionPath":"/success"},"tech":{"basePath":"/tech","canonicalSite":"www","children":[],"isSubsection":true,"label":"Tech","parent":"business","sites":["www","edition"],"title":"Tech News","uri":"/business/tech/index.html","name":"tech","sectionPath":"/tech"},"tennis":{"basePath":"/sport/tennis","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Tennis","parent":"sport","sectionPath":"/tennis","sites":["www","edition"],"title":"Tennis News","uri":"/sport/tennis/index.html","name":"tennis"},"travel":{"basePath":"/travel","canonicalSite":"www","children":["destinations","foodanddrink","hotels","news","play","stay","travel-home","travel-video-hub"],"isSubsection":false,"label":"Travel","sites":["www","edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel/index.html","name":"travel","sectionPath":"/travel"},"travel-home":{"basePath":"/travel-home","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel - Home","parent":"travel","sites":["www","edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel-home/index.html","name":"travel-home","sectionPath":"/travel-home"},"travel-video-hub":{"basePath":"/travel/videos","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel Video Hub","parent":"travel","sectionPath":"/travel-video-hub","sites":["www","edition"],"title":"Travel Videos","uri":"/travel/videos/index.html","name":"travel-video-hub"},"tv":{"basePath":"/tv","canonicalSite":"www","children":["tv-schedule-cnn"],"isSubsection":false,"label":"TV","sites":["www"],"title":"CNN TV","uri":"/tv/index.html","name":"tv","sectionPath":"/tv"},"tv-schedule-cnn":{"basePath":"/tv/schedule/cnn","canonicalSite":"www","children":[],"isSubsection":true,"label":"TV Schedule - CNN","parent":"tv","sites":["www"],"title":"TV Schedule - CNN","uri":"/tv/schedule/cnn/index.html","name":"tv-schedule-cnn","sectionPath":"/tv/schedule/cnn"},"tv-shows":{"basePath":"/entertainment/tv-shows","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"TV Shows","parent":"entertainment","sectionPath":"/tv-shows","sites":["www"],"title":"TV Shows - Entertainment News","uri":"/entertainment/tv-shows/index.html","name":"tv-shows"},"uk":{"basePath":"/uk","canonicalSite":"edition","children":[],"isSubsection":true,"label":"United Kingdom","parent":"europe","sites":["www","edition"],"title":"U.K. News - Breaking News, Video, Headlines and Opinion","uri":"/uk/index.html","name":"uk","sectionPath":"/uk"},"us":{"basePath":"/us","canonicalSite":"www","children":[],"displayLabel":"US","isSubsection":false,"label":"US","sites":["www","edition"],"title":"U.S. News - Breaking News, Video, Headlines and Opinion","uri":"/us/index.html","name":"us","sectionPath":"/us"},"videos":{"adsName":"video","basePath":"/videos","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Videos","sites":["www"],"title":"Video News","uri":"/videos/index.html","name":"videos","sectionPath":"/videos"},"vr":{"basePath":"/vr","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"VR","sites":["www","edition"],"title":"Virtual Reality & 360° Video - CNNVR","uri":"/vr/index.html","name":"vr","sectionPath":"/vr"},"watch-cnn":{"basePath":"/tv/watch/cnn","canonicalSite":"www","children":[],"isSubsection":true,"label":"Watch CNN","parent":"tv","sectionPath":"/watch-cnn","sites":["www","edition"],"title":"Watch CNN Live - Stream CNN Live Online","uri":"/tv/watch/cnn/index.html","name":"watch-cnn"},"weather":{"basePath":"/weather","canonicalSite":"www","children":[],"isSubsection":false,"label":"Weather","sites":["www","edition"],"title":"Latest Weather and Extended Forecast","uri":"/weather/index.html","name":"weather","sectionPath":"/weather"},"world":{"basePath":"/world","canonicalSite":"www","children":[],"isSubsection":false,"label":"World","sites":["www"],"title":"World News","uri":"/world/index.html","name":"world","sectionPath":"/world"}},"uri":"/intl_index.html","userAccount":{"dalton":{"env":"production","cookieVersion":"v1.1"},"legaldocs":[{"docName":"TOS-Intl","version":"1.0","label":"By clicking Register you confirm you have read and agree to our \u003ca href='https://www.cnn.com/terms' target='_blank'>Terms and Conditions\u003c/a> and acknowledge our \u003ca href='https://www.cnn.com/privacy' target='_blank'>Privacy Policy.\u003c/a>"}],"legaldocsPrompt":{"text":"Please click the button below to agree to our \u003ca href='https://www.cnn.com/terms' target='_blank'>Terms and Conditions\u003c/a> and acknowledge our \u003ca href='https://www.cnn.com/privacy' target='_blank'>Privacy Policy\u003c/a>.","title":"Our Terms of Service have Changed"},"preferencesPage":{"enableDisplayName":true,"newsletters":{"enabled":true,"removeAcctMsg":"A CNN account is the best way to manage your newsletters. If you wish to continue receiving our newsletters, you will need to resubscribe."},"settingsPageText":"These details will only be visible to you and CNN.","zipCode":{"enabled":false}},"registrationPage":{"heading":{"primary":"Create a CNN Account","secondary":"Be a part of the new CNN."},"marketingOptIns":[{"name":"marketingOptIn","label":"Check here if you would like to receive updates and offers from CNN and its \u003ca href='https://www.warnermediaprivacy.com/affiliates/' target='_blank'>affiliates\u003c/a>","preselected":true},{"name":"marketingOptIn","label":"Yes! CNN and WarnerMedia News & Sports may use my email address along with my interests, interactions, and device data to send me tailored email and other offers through social media or other sites and apps.","type":"gdpr"},{"name":"marketingAffiliateOptIn","label":"Yes! CNN and WarnerMedia News & Sports may also share those details with \u003ca href='https://turneraffiliates.turner.com/Affiliates/Turner-Affiliates-English' target='_blank'>Affiliates\u003c/a> so they may send me tailored email and other offers. CNN and WarnerMedia News & Sports are requesting this consent on behalf of their affiliates, which will use the information under their respective privacy policies.","type":"gdpr"}],"marketingOptOut":{"label":"Opt-out by email to WMPrivacy@warnermediagroup.com, mail to “WarnerMedia Privacy Office, 4000 Warner Blvd., Bldg. 160, Burbank, CA 91522,” or by the unsubscribe link in the email."},"promotions":[{"source":"voter_guide","altHeadingText":"Create an account to get election deadline reminders and more.","verifiedRedirectURL":"https://cnn.com/election/2020/voter-guide"},{"source":"politics_my-election","altHeadingText":"Create an account to track the races that you care about on Election Night","altSubHeadingText":" ","verifiedRedirectURL":"/2020"}]},"rememberMeDuration":365},"userAccountLegalDocs":[{"docName":"TOS","version":"1.0","label":"By clicking Register you confirm you have read and agree to our \u003ca href='https://www.cnn.com/terms' target='_blank'>Terms and Conditions\u003c/a> and acknowledge our \u003ca href='https://www.cnn.com/privacy' target='_blank'>Privacy Policy.\u003c/a>","type":"domestic"},{"docName":"TOS-Intl","version":"1.0","label":"By clicking Register you confirm you have read and agree to our \u003ca href='https://www.cnn.com/terms' target='_blank'>Terms and Conditions\u003c/a> and acknowledge our \u003ca href='https://www.cnn.com/privacy' target='_blank'>Privacy Policy.\u003c/a>","type":"intl"}],"vertical":"news","watchLiveButton":{"copy":"Live TV","link":"http://go.cnn.com/?stream=cnni&sr=watchLiveHPbutton&source=edition","validCountries":["US","CA","PR","VI"]}}});
                    

                        if (!window.COMPONENTS) window.COMPONENTS = [];
                        window.COMPONENTS.push({"id":2,"component":"./elements/ui/breaking-news-wrapper/breaking-news-wrapper.component.jsx","props":{"pageType":"section","sectionName":"intl_homepage","trackingPrefix":"breaking news","ttl":120000,"url":"//data.cnn.com/breaking_news/international.json"}});
                    
CNN.covCon.push({id: "coverageContainer_94666ABA-6F11-0405-F645-CF22729BC16F",layout: "list-hierarchical-horizontal-simple",src: "/data/ocs/container/coverageContainer_94666ABA-6F11-0405-F645-CF22729BC16F:list-hierarchical-horizontal-simple/views/containers/common/container-manager.html"});
(function (animationConfig) {CNN.INJECTOR.executeFeature('animations').then(function loadedAnimationBundleHandler() {CNN.ANIMATIONS.loadAnimation(animationConfig);})})({animationId: 'anim1621511354530',url: 'https://dynaimage.cdn.cnn.com/cnn/animations/org/210520124913-desktop-mice-australia-2.mp4',isPageTop: false,isBackground: false,pageType: 'section',appearance: '',targetUrl: '/2021/05/20/australia/australia-mouse-plague-dst-intl-hnk/index.html',cuts: {dataSrcMini: "https://dynaimage.cdn.cnn.com/cnn/animations/w_220,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcXsmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_300,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcSmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_460,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcPhonePageTop: "https://dynaimage.cdn.cnn.com/cnn/animations/w_355,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcMedium: "https://dynaimage.cdn.cnn.com/cnn/animations/w_780,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcLarge: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1100,ac_none/210520124913-desktop-mice-australia-2.mp4",dataSrcFull16x9: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1600,ac_none/210520124913-desktop-mice-australia-2.mp4",}});
(function (animationConfig) {CNN.INJECTOR.executeFeature('animations').then(function loadedAnimationBundleHandler() {CNN.ANIMATIONS.loadAnimation(animationConfig);})})({animationId: 'anim16203837814ba',url: 'https://dynaimage.cdn.cnn.com/cnn/animations/org/210507113620-desktop-china-hs-rail-1.mp4',isPageTop: false,isBackground: false,pageType: 'section',appearance: '',targetUrl: '/travel/article/china-high-speed-rail-cmd/index.html',cuts: {dataSrcMini: "https://dynaimage.cdn.cnn.com/cnn/animations/w_220,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcXsmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_300,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcSmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_460,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcPhonePageTop: "https://dynaimage.cdn.cnn.com/cnn/animations/w_355,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcMedium: "https://dynaimage.cdn.cnn.com/cnn/animations/w_780,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcLarge: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1100,ac_none/210507113620-desktop-china-hs-rail-1.mp4",dataSrcFull16x9: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1600,ac_none/210507113620-desktop-china-hs-rail-1.mp4",}});
(function (animationConfig) {CNN.INJECTOR.executeFeature('animations').then(function loadedAnimationBundleHandler() {CNN.ANIMATIONS.loadAnimation(animationConfig);})})({animationId: 'anim1621496592531',url: 'https://dynaimage.cdn.cnn.com/cnn/animations/org/210520084312-desktop-larissa-iapichino-tease.mp4',isPageTop: false,isBackground: false,pageType: 'section',appearance: '',targetUrl: '/2021/05/20/sport/larissa-iapichino-long-jump-olympics-spt-intl-cmd/index.html',cuts: {dataSrcMini: "https://dynaimage.cdn.cnn.com/cnn/animations/w_220,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcXsmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_300,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcSmall: "https://dynaimage.cdn.cnn.com/cnn/animations/w_460,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcPhonePageTop: "https://dynaimage.cdn.cnn.com/cnn/animations/w_355,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcMedium: "https://dynaimage.cdn.cnn.com/cnn/animations/w_780,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcLarge: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1100,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",dataSrcFull16x9: "https://dynaimage.cdn.cnn.com/cnn/animations/w_1600,ac_none/210520084312-desktop-larissa-iapichino-tease.mp4",}});
try {window.performance.mark("footerStart");} catch (err) {}

                        if (!window.COMPONENTS) window.COMPONENTS = [];
                        window.COMPONENTS.push({"id":3,"component":"./elements/ui/footer-wrapper/footer-wrapper.component.jsx","props":{"edition":"international","enableUserConsent":true,"extraCopyrightText":"","jsmdUcStates":["data-store","content-person-prof","content-person","measure-content","measure-market","product-develop"],"nav":{"legal":[{"label":"Terms of Use","url":"/terms","name":"terms-of-use"},{"label":"Privacy Policy","url":"/privacy","name":"privacy-policy"},{"label":"Accessibility & CC","url":"/accessibility","name":"accessibility"},{"label":"AdChoices","url":"#","name":"adchoices"},{"label":"About Us","url":"/about","name":"about-us"},{"label":"Modern Slavery Act Statement","url":"/msa","name":"modern-slavery-act-statement","excludeEdition":"domestic"},{"label":"Advertise with us","url":"https://commercial.cnn.com","name":"advertise-with-us","excludeEdition":"domestic"},{"label":"CNN Store","url":"//store.cnn.com","name":"cnn-store"},{"label":"Newsletters","url":"/newsletters","name":"newsletters"},{"label":"Transcripts","url":"/transcripts","name":"transcripts"},{"label":"License Footage","url":"/collection","name":"license-footage"},{"label":"CNN Newsource","url":"http://cnnnewsource.com","name":"cnn-newsource"},{"label":"Sitemap","url":"https://www.cnn.com/sitemap.html","name":"sitemap"}],"sections":[{"section":"us","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Crime + Justice","name":"crime-and-justice","url":"/specials/us/crime-and-justice"},{"label":"Energy + Environment","name":"energy-and-environment","url":"/specials/us/energy-and-environment"},{"label":"Extreme Weather","name":"extreme-weather","url":"/specials/us/extreme-weather"},{"label":"Space + Science","name":"space-science","url":"/specials/space-science"}]},{"section":"world","enableSectionLink":true,"subs":[{"section":"africa"},{"section":"americas"},{"section":"asia"},{"section":"australia"},{"section":"china"},{"section":"europe"},{"section":"india"},{"section":"middleeast"},{"section":"uk"}]},{"section":"politics","enableSectionLink":true,"labelOverride":{"editions":["international"],"label":"US Politics"},"subs":[{"label":"The Biden Presidency","name":"the-biden-presidency","url":"/specials/politics/joe-biden-news"},{"label":"Facts First","name":"facts-first","url":"/specials/politics/fact-check-politics"},{"label":"US Elections","name":"us-elections","url":"/election/2020/results/president"}]},{"section":"business","deepNav":true,"enableSectionLink":true,"subs":[{"label":"Markets","url":"https://money.cnn.com/data/markets/","name":"markets","subs":[{"label":"Premarkets","url":"https://money.cnn.com/data/premarket/","name":"premarkets"},{"label":"Dow","url":"https://money.cnn.com/data/markets/dow/","name":"dow-30"},{"label":"After-Hours","url":"https://money.cnn.com/data/afterhours/","name":"after-hours"},{"label":"Market Movers","url":"https://money.cnn.com/data/hotstocks/","name":"market-movers"},{"label":"Fear & Greed","url":"https://money.cnn.com/data/fear-and-greed/","name":"fear-greed"},{"label":"World Markets","url":"https://money.cnn.com/data/world_markets/americas/","name":"world-markets"},{"label":"Investing","url":"/business/investing","name":"investing"},{"label":"Markets Now","url":"https://money.cnn.com/investing/markets-now","name":"markets-now"},{"label":"Before the Bell","url":"/specials/investing/before-the-bell","name":"before-the-bell"},{"label":"Leading Indicator","url":"/specials/investing/leading-indicator","name":"leading-indicator"},{"label":"Global Energy Challenge","url":"/specials/business/global-energy-challenge","name":"global-energy-challenge"},{"label":"Economy","url":"/business/economy","name":"economy"},{"label":"Tracking America's Recovery","url":"/business/us-economic-recovery-coronavirus","name":"coronavirus-recovery"},{"label":"Energy","url":"/business/energy","name":"energy"},{"label":"Money","url":"/business/money","name":"money"}]},{"section":"tech","subs":[{"label":"Innovate","url":"/specials/tech/innovate","name":"innovate"},{"label":"Gadget","url":"/specials/tech/gadget","name":"gadget"},{"label":"Foreseeable Future","url":"/specials/tech/foreseeable-future","name":"foreseeable-future"},{"label":"Mission: Ahead","url":"/specials/tech/mission-ahead","name":"mission-ahead"},{"label":"Upstarts","url":"/specials/tech/upstarts","name":"upstarts"},{"label":"Business Evolved","url":"/specials/tech/business-evolved","name":"business-evolved"},{"label":"Innovative Cities","url":"/specials/tech/innovative-cities","name":"innovative-cities"},{"label":"Unhackable","url":"/specials/tech/unhackable","name":"unhackable"}]},{"section":"media","subs":[{"label":"Reliable Sources","url":"/shows/reliable-sources","name":"reliable-sources"}]},{"section":"success","subs":[{"label":"Boss Files","url":"/specials/success/boss-files","name":"boss-files"},{"label":"Risk Takers","url":"/interactive/2019/business/risk-takers","name":"risk-takers"},{"label":"Fresh Money","url":"/specials/success/fresh-money","name":"fresh-money"},{"label":"Invest Ahead","url":"/specials/success/invest-ahead","name":"invest-ahead"},{"label":"Work Transformed","url":"/specials/tech/work-transformed","name":"work-transformed"},{"label":"Cars","url":"/business/cars","name":"cars"},{"label":"Homes","url":"/business/homes","name":"homes"},{"label":"Wealth Coach","url":"/specials/success/wealth-coach","name":"wealth-coach"}]},{"label":"Center Piece","url":"/specials/business/center-piece","name":"center-piece","enableSectionLink":false,"disableInMegaNavSubLinks":true},{"section":"perspectives"},{"section":"business-videos","labelOverride":{"editions":["domestic","international"],"label":"Videos"}},{"label":"International","url":"https://edition.cnn.com/business","name":"international-business","enableSectionLink":false,"disableInMegaNavSubLinks":true,"subs":[{"label":"Switzerland","url":"https://www.cnnmoney.ch","name":"switzerland"},{"label":"India","url":"/business/india","name":"business-india"},{"label":"Davos","url":"/specials/business/davos/","name":"davos"},{"label":"Reliable Sources","url":"/shows/reliable-sources","name":"reliable-sources"},{"label":"Passion to Portfolio","url":"/specials/business/passion-to-portfolio","name":"passion-portfolio"},{"label":"On: Germany","url":"/specials/business/on-germany","name":"on-germany"}]},{"label":"More","enableSectionLink":false,"disableInMegaNavSubLinks":true,"subs":[{"label":"Accessibility & CC","url":"/accessibility","name":"accessibility"},{"label":"About Us","url":"/about","name":"about-us"},{"label":"Newsletters","url":"/newsletters","name":"newsletters"}]}]},{"section":"opinions","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Political Op-Eds","name":"opinion-politics","url":"/specials/opinion/opinion-politics"},{"label":"Social Commentary","name":"opinion-social-issues","url":"/specials/opinion/opinion-social-issues"}]},{"section":"health","enableSectionLink":true,"subs":[{"label":"Food","name":"food","url":"/specials/health/food-diet"},{"label":"Fitness","name":"fitness","url":"/specials/health/fitness-excercise"},{"label":"Wellness","name":"wellness","url":"/specials/health/wellness"},{"label":"Parenting","name":"parenting","url":"/specials/health/parenting"},{"label":"Vital Signs","name":"vital-signs","url":"/specials/health/vital-signs"}]},{"section":"entertainment","enableSectionLink":true,"subs":[{"label":"Stars","name":"stars","url":"/entertainment/celebrities"},{"label":"Screen","name":"screen","url":"/entertainment/movies"},{"label":"Binge","name":"binge","url":"/entertainment/tv-shows"},{"label":"Culture","name":"culture","url":"/entertainment/culture"},{"label":"Media","name":"media","url":"/business/media"}]},{"section":"tech","enableSectionLink":false,"subs":[{"label":"Innovate","name":"innovate","url":"/specials/tech/innovate"},{"label":"Gadget","name":"gadget","url":"/specials/tech/gadget"},{"label":"Foreseeable Future","name":"foreseeable-future","url":"/specials/tech/foreseeable-future"},{"label":"Mission: Ahead","name":"mission-ahead","url":"/specials/tech/mission-ahead"},{"label":"Upstarts","name":"upstarts","url":"/specials/tech/upstarts"},{"label":"Work Transformed","name":"work-transformed","url":"/specials/tech/work-transformed"},{"label":"Innovative Cities","name":"innovative-cities","url":"/specials/tech/innovative-cities"}]},{"section":"style","enableSectionLink":true,"subs":[{"label":"Arts","section":"arts","url":"/style/arts"},{"label":"Design","section":"design","url":"/style/design"},{"label":"Fashion","section":"fashion","url":"/style/fashion"},{"label":"Architecture","section":"architecture","url":"/style/architecture"},{"label":"Luxury","section":"luxury","url":"/style/luxury"},{"label":"Beauty","section":"beauty","url":"/style/beauty"},{"label":"Video","section":"style-videos","url":"/style/videos"}]},{"section":"travel","enableSectionLink":true,"subs":[{"label":"Destinations","section":"destinations","url":"/travel/destinations"},{"label":"Food & Drink","section":"foodanddrink","url":"/travel/food-and-drink"},{"label":"Stay","section":"travel-stay","url":"/travel/stay"},{"label":"News","section":"travel-news","url":"/travel/news"},{"label":"Videos","section":"travel-videos","url":"/travel/videos"}]},{"label":"Sports","section":"bleacher","name":"bleacher","url":"http://bleacherreport.com","enableSectionLink":true,"excludeEdition":"international","subs":[{"label":"Pro Football","name":"nfl","url":"http://bleacherreport.com/nfl"},{"label":"College Football","name":"college-football","url":"http://bleacherreport.com/college-football"},{"label":"Basketball","name":"nba","url":"http://bleacherreport.com/nba"},{"label":"Baseball","name":"mlb","url":"http://bleacherreport.com/mlb"},{"label":"Soccer","name":"world-football","url":"http://bleacherreport.com/world-football"},{"label":"Olympics","name":"olympics","url":"/sport/olympics"}]},{"section":"sport","enableSectionLink":true,"excludeEdition":"domestic","name":"sports","labelOverride":{"editions":["international"],"label":"Sports"},"subs":[{"section":"football"},{"section":"tennis"},{"section":"golf"},{"section":"olympics"},{"label":"US Sports","name":"us-sports","url":"/specials/sport/us-sports"},{"label":"Climbing","name":"climbing","url":"/specials/climbing"},{"section":"motorsport"},{"label":"Formula E","name":"formula-e","url":"/specials/sport/formula-e"},{"label":"Esports","name":"esports","url":"/specials/esports"}]},{"section":"videos","enableSectionLink":true,"subs":[{"label":"Live TV ","name":"live-tv","url":"//cnn.it/go2"},{"label":"Digital Studios","name":"digital-studios","url":"/specials/digital-studios"},{"label":"CNN Films","name":"digital-shorts","url":"/specials/videos/digital-shorts"},{"label":"HLN","name":"hln","url":"/specials/videos/hln"},{"label":"TV Schedule","name":"tv-schedule","url":"/tv/schedule/cnn"},{"label":"TV Shows A-Z","name":"all-shows","url":"/specials/tv/all-shows"},{"label":"CNNVR","name":"vr","url":"/vr"}]},{"label":"Audio","name":"audio","section":"Audio","url":"/audio","enableSectionLink":false,"excludeEdition":"international","subs":[]},{"section":"features","label":"Features","name":"features","disableMegaNavLink":false,"enableSectionLink":false,"excludeEdition":"domestic","url":"/specials","subs":[{"label":"As Equals","name":"as-equals","url":"/interactive/asequals/"},{"label":"Call to Earth","name":"call-to-earth","url":"/interactive/call-to-earth/"},{"label":"Freedom Project","name":"freedom-project","url":"/specials/world/freedom-project"},{"label":"Impact Your World","name":"impact-your-world","url":"/specials/impact-your-world"},{"label":"Inside Africa","name":"inside-africa","url":"/specials/africa/inside-africa"},{"label":"2 Degrees","name":"two-degrees","url":"/specials/opinions/two-degrees"},{"label":"CNN Heroes","name":"cnn-heroes","url":"/specials/cnn-heroes"},{"label":"All Features","name":"all-features","url":"/specials"}]},{"label":"Coupons","name":"coupons","section":"Coupons","url":"//coupons.cnn.com","enableSectionLink":false,"excludeEdition":"international","subs":[{"label":"CNN Underscored","name":"cnn-underscored","url":"/cnn-underscored/"},{"label":"Explore","name":"underscored-explore","url":"/specials/cnn-underscored/explore/"},{"label":"Wellness","name":"underscored-wellness","url":"/specials/cnn-underscored/wellness/"},{"label":"Gadgets","name":"underscored-gadgets","url":"/specials/cnn-underscored/gadgets/"},{"label":"Lifestyle","name":"underscored-lifestyle","url":"/specials/cnn-underscored/lifestyle/"},{"label":"CNN Store","name":"cnn-store","url":"//store.cnn.com/?utm_source=cnn.com&utm_medium=referral&utm_campaign=navbar"}]},{"section":"vr","disableMegaNavLink":true,"enableSectionLink":false,"subs":[{"label":"How To Watch VR","name":"how-to-watch-vr","url":"/2017/03/04/vr/how-to-watch-vr"},{"label":"Archives","name":"vr-archives","url":"/specials/vr/vr-archives"}]},{"section":"weather","disableMegaNavLink":false,"enableSectionLink":false,"subs":[{"label":"Climate","name":"climate","url":"/specials/world/cnn-climate"},{"label":"Storm Tracker","name":"storm-tracker","url":"/interactive/2020/weather/gonzalo-storm-path-tracker/index.html"},{"label":"Wildfire Tracker","name":"wildfire-tracker","url":"/interactive/2020/weather/wildfire-and-air-quality-tracker/"},{"label":"Video","name":"weather-video","url":"/specials/weather/weather-video"}]},{"section":"more","name":"more","enableSectionLink":false,"subs":[{"label":"Photos","name":"photos","url":"/specials/photos"},{"label":"Longform","name":"longform","url":"/specials/cnn-longform"},{"label":"Investigations","name":"cnn-investigates","url":"/specials/cnn-investigates"},{"label":"CNN Profiles","name":"profiles","url":"/specials/profiles"},{"label":"CNN Leadership","name":"leadership","url":"/specials/more/cnn-leadership"},{"label":"CNN Newsletters","name":"newsletters","url":"/email/subscription"},{"label":"Work for CNN","name":"jobs","url":"https://www.turnerjobs.com/search-jobs?orgIds=1174&ac=19299"}]}],"social":{"domestic":{"links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/CNN"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNN"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"}]},"international":{"links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnninternational"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/cnni"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"}]},"business":{"entity":"Business","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnnbusiness"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNNbusiness"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnnbusiness"}]},"politics":{"entity":"Politics","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/cnnpolitics"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/cnnpolitics"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnn"},{"label":"YouTube","name":"youtube","url":"//youtube.com/user/CNN"}]},"entertainment":{"entity":"Entertainment","links":[{"name":"facebook","label":"Facebook page","url":"//facebook.com/CNNent"},{"name":"twitter","label":"Twitter feed","url":"//twitter.com/CNNent"},{"name":"instagram","label":"Instagram feed","url":"//instagram.com/cnnentertainment"}]}},"userAccount":[{"label":"Settings","name":"userSettings","url":"/account/settings"},{"label":"Log Out","name":"userLogout","url":"#"}]},"pageType":"section","searchUrl":"/search","sectionName":"intl_homepage","sectionsInfo":{"africa":{"basePath":"/africa","canonicalSite":"www","children":[],"isSubsection":true,"label":"Africa","parent":"intl_regions","sites":["www","edition"],"title":"Africa News - Breaking News, Video, Headlines and Opinion","uri":"/africa/index.html","name":"africa","sectionPath":"/africa"},"airport-delays":{"basePath":"/airport-delays","canonicalSite":"www","children":[],"isSubsection":false,"label":"Airport Delays","sites":["www","edition"],"title":"Airport Delays","uri":"/airport-delays/index.html","name":"airport-delays","sectionPath":"/airport-delays"},"americas":{"basePath":"/americas","canonicalSite":"www","children":[],"isSubsection":true,"label":"Americas","parent":"intl_regions","sites":["www","edition"],"title":"Americas News - Breaking News, Video, Headlines and Opinion","uri":"/americas/index.html","name":"americas","sectionPath":"/americas"},"app-health-section":{"basePath":"/app-health-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Health Section","sites":["www","edition"],"title":"","uri":"/app-health-section/index.html","name":"app-health-section","sectionPath":"/app-health-section"},"app-international-edition":{"basePath":"/app-international-edition","canonicalSite":"app","children":[],"isSubsection":false,"label":"App International Edition","sites":["www","edition"],"title":"","uri":"/app-international-edition/index.html","name":"app-international-edition","sectionPath":"/app-international-edition"},"app-money-section":{"basePath":"/app-money-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Money Section","sites":["www","edition"],"title":"","uri":"/app-money-section/index.html","name":"app-money-section","sectionPath":"/app-money-section"},"app-news-section":{"basePath":"/app-news-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App News Section","sites":["www","edition"],"title":"","uri":"/app-news-section/index.html","name":"app-news-section","sectionPath":"/app-news-section"},"app-opinion-section":{"basePath":"/app-opinion-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Opinion Section","sites":["www","edition"],"title":"","uri":"/app-opinion-section/index.html","name":"app-opinion-section","sectionPath":"/app-opinion-section"},"app-politics-section":{"basePath":"/app-politics-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Politics Section","sites":["www","edition"],"title":"","uri":"/app-politics-section/index.html","name":"app-politics-section","sectionPath":"/app-politics-section"},"app-specials":{"basePath":"/app-specials","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Specials","sites":["www","edition"],"title":"","uri":"/app-specials/index.html","name":"app-specials","sectionPath":"/app-specials"},"app-sports-section":{"basePath":"/app-sports-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Sports Section","sites":["www","edition"],"title":"","uri":"/app-sports-section/index.html","name":"app-sports-section","sectionPath":"/app-sports-section"},"app-style-section":{"basePath":"/app-style-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Style Section","sites":["www","edition"],"title":"","uri":"/app-style-section/index.html","name":"app-style-section","sectionPath":"/app-style-section"},"app-tech-section":{"basePath":"/app-tech-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Tech Section","sites":["www","edition"],"title":"","uri":"/app-tech-section/index.html","name":"app-tech-section","sectionPath":"/app-tech-section"},"app-travel-section":{"basePath":"/app-travel-section","canonicalSite":"app","children":[],"isSubsection":false,"label":"App Travel Section","sites":["www","edition"],"title":"","uri":"/app-travel-section/index.html","name":"app-travel-section","sectionPath":"/app-travel-section"},"architecture":{"basePath":"/style/architecture","canonicalSite":"www","children":[],"isSubsection":true,"label":"Architecture","parent":"style","sectionPath":"/architecture","sites":["www","edition"],"title":"Architecture","uri":"/style/architecture/index.html","name":"architecture"},"area51":{"basePath":"/area51","canonicalSite":"www","children":[],"isSubsection":false,"label":"Area 51","sites":["www","edition"],"title":"Area 51","uri":"/area51/index.html","name":"area51","sectionPath":"/area51"},"arts":{"basePath":"/style/arts","canonicalSite":"www","children":[],"isSubsection":true,"label":"Arts","parent":"style","sectionPath":"/arts","sites":["www","edition"],"title":"Arts","uri":"/style/arts/index.html","name":"arts"},"asia":{"basePath":"/asia","canonicalSite":"www","children":["china","india"],"isSubsection":true,"label":"Asia","parent":"intl_regions","sites":["www","edition"],"title":"Asia News - Breaking News, Video, Headlines and Opinion","uri":"/asia/index.html","name":"asia","sectionPath":"/asia"},"australia":{"basePath":"/australia","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Australia","parent":"asia","sites":["www","edition"],"title":"Australia News - Breaking News, Video, Headlines and Opinion","uri":"/australia/index.html","name":"australia","sectionPath":"/australia"},"autos":{"basePath":"/style/autos","canonicalSite":"www","children":[],"isSubsection":true,"label":"Autos","parent":"style","sectionPath":"/autos","sites":["www","edition"],"title":"Autos","uri":"/style/autos/index.html","name":"autos"},"aviation":{"basePath":"/travel/aviation","canonicalSite":"www","children":[],"isSubsection":true,"label":"Aviation","parent":"travel","sectionPath":"/aviation","sites":["www","edition"],"title":"Innovation in Aviation from Airplanes to Airports","uri":"/travel/aviation/index.html","name":"aviation"},"beauty":{"basePath":"/style/beauty","canonicalSite":"www","children":[],"isSubsection":true,"label":"Beauty","parent":"style","sectionPath":"/beauty","sites":["www","edition"],"title":"Beauty","uri":"/style/beauty/index.html","name":"beauty"},"business":{"basePath":"/business","canonicalSite":"www","children":["business-india","business-videos","cars","economy","energy","homes","investing","media","perspectives","success","tech"],"displayLabel":"","isSubsection":false,"label":"Business","sites":["www"],"title":"Business","uri":"/business/index.html","name":"business","sectionPath":"/business"},"business-food":{"basePath":"/business-food","canonicalSite":"www","children":[],"displayLabel":"Food","isSubsection":true,"label":"Business - Food","parent":"business","sectionPath":"/business-food","sites":["www","edition"],"title":"Business - Food","uri":"/business/food/index.html","name":"business-food"},"business-india":{"basePath":"/business-india","canonicalSite":"www","children":[],"displayLabel":"India","isSubsection":true,"label":"Business - India","parent":"business","sectionPath":"/business-india","sites":["www","edition"],"title":"Business - India","uri":"/business/india/index.html","name":"business-india"},"business-planning":{"adsName":"business","basePath":"/business-planning","canonicalSite":"www","children":[],"displayLabel":"Planning","isSubsection":true,"label":"Business Planning","sites":["www","edition"],"title":"Business Planning","uri":"/business-planning/index.html","name":"business-planning","sectionPath":"/business-planning"},"business-videos":{"adsName":"video","basePath":"/business-videos","canonicalSite":"www","children":[],"displayLabel":"Video","isSubsection":true,"label":"Business Videos","parent":"business","sites":["www","edition"],"title":"Business Videos","uri":"/business/videos/index.html","name":"business-videos","sectionPath":"/business-videos"},"celebrities":{"basePath":"/entertainment/celebrities","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Celebrities","parent":"entertainment","sectionPath":"/celebrities","sites":["www","edition"],"title":"Celebrities - Entertainment News","uri":"/entertainment/celebrities/index.html","name":"celebrities"},"china":{"basePath":"/china","canonicalSite":"www","children":[],"isSubsection":true,"label":"China","parent":"asia","sites":["www","edition"],"title":"China News - Breaking News, Video, Headlines and Opinion","uri":"/china/index.html","name":"china","sectionPath":"/china"},"cnn-underscored":{"basePath":"/cnn-underscored","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN Underscored","sites":["www","edition"],"title":"Product Reviews, Gift Ideas, Gadget Guides and More","uri":"/cnn-underscored/index.html","name":"cnn-underscored","sectionPath":"/cnn-underscored"},"cnn10":{"basePath":"/cnn10","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN 10","sites":["www","edition"],"title":"CNN 10","uri":"/cnn10/index.html","name":"cnn10","sectionPath":"/cnn10"},"cnnmoney":{"basePath":"/","canonicalSite":"www","children":[],"isSubsection":false,"label":"CNN Money","sites":["www","edition"],"title":"CNN Money","uri":"","name":"cnnmoney","sectionPath":"/"},"culture":{"basePath":"/entertainment/culture","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Culture","parent":"entertainment","sectionPath":"/culture","sites":["www","edition"],"title":"Pop Culture - Entertainment News","uri":"/entertainment/culture/index.html","name":"culture"},"design":{"basePath":"/style/design","canonicalSite":"www","children":[],"isSubsection":true,"label":"Design","parent":"style","sectionPath":"/design","sites":["www","edition"],"title":"Design","uri":"/style/design/index.html","name":"design"},"destinations":{"basePath":"/travel/destinations","canonicalSite":"www","children":[],"isSubsection":true,"label":"Destinations","parent":"travel","sectionPath":"/destinations","sites":["www","edition"],"title":"Destinations","uri":"/travel/destinations/index.html","name":"destinations"},"economy":{"basePath":"/economy","canonicalSite":"www","children":[],"isSubsection":true,"label":"Economy","parent":"business","sites":["www","edition"],"title":"Business","uri":"/business/economy/index.html","name":"economy","sectionPath":"/economy"},"election-2018":{"adsName":"elections","basePath":"/election","canonicalSite":"www","children":[],"isSubsection":true,"label":"Election 2018","parent":"politics","sites":["www","edition"],"title":"2018 Elections","uri":"/election/index.html","name":"election-2018","sectionPath":"/election"},"election-center-2016":{"basePath":"/election/2016","canonicalSite":"www","children":[],"isSubsection":true,"label":"Election Center 2016","parent":"politics","sites":["www","edition"],"title":"2016 Elections","uri":"/election/2016/index.html","name":"election-center-2016","sectionPath":"/election/2016"},"entertainment":{"basePath":"/entertainment","canonicalSite":"www","children":["celebrities","culture","movies","tv-shows"],"displayLabel":"","isSubsection":false,"label":"Entertainment","sites":["www","edition"],"title":"Entertainment News - Celebrities, Movies, TV, Music","uri":"/entertainment/index.html","name":"entertainment","sectionPath":"/entertainment"},"equestrian":{"basePath":"/sport/equestrian","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Equestrian","parent":"sport","sectionPath":"/equestrian","sites":["www","edition"],"title":"Equestrian News","uri":"/sport/equestrian/index.html","name":"equestrian"},"europe":{"basePath":"/europe","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Europe","parent":"intl_regions","sites":["www","edition"],"title":"Europe News - Breaking News, Video, Headlines and Opinion","uri":"/europe/index.html","name":"europe","sectionPath":"/europe"},"fashion":{"basePath":"/style/fashion","canonicalSite":"www","children":[],"isSubsection":true,"label":"Fashion","parent":"style","sectionPath":"/fashion","sites":["www","edition"],"title":"Fashion","uri":"/style/fashion/index.html","name":"fashion"},"foodanddrink":{"basePath":"/travel/food-and-drink","canonicalSite":"www","children":[],"isSubsection":true,"label":"Food and Drink","parent":"travel","sectionPath":"/foodanddrink","sites":["www","edition"],"title":"Food & Drink","uri":"/travel/food-and-drink/index.html","name":"foodanddrink"},"football":{"basePath":"/sport/football","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Football","parent":"sport","sectionPath":"/football","sites":["www","edition"],"title":"Football News","uri":"/sport/football/index.html","name":"football"},"golf":{"basePath":"/sport/golf","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Golf","parent":"sport","sectionPath":"/golf","sites":["www","edition"],"title":"Golf News","uri":"/sport/golf/index.html","name":"golf"},"health":{"basePath":"/health","canonicalSite":"www","children":[],"isSubsection":false,"label":"Health","logo":"//cdn.cnn.com/cnn/.e1mo/img/4.0/logos/cnn_health_banner.png","sites":["www","edition"],"title":"Health News","uri":"/health/index.html","name":"health","sectionPath":"/health"},"homepage":{"basePath":"/","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Domestic Homepage","sites":["www"],"title":"Breaking News, Latest News and Videos","uri":"/index.html","name":"homepage","sectionPath":"/"},"homepage-magellan":{"basePath":"/","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Homepage Magellan","sites":["www","edition"],"title":"Breaking News, U.S., World, Weather, Entertainment & Video News","uri":"/index3.html","name":"homepage-magellan","sectionPath":"/"},"horseracing":{"adsName":"winningpost","basePath":"/sport/horse-racing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Horse Racing","parent":"sport","sectionPath":"/horseracing","sites":["www","edition"],"title":"Horse Racing News","uri":"/sport/horse-racing/index.html","name":"horseracing"},"hotels":{"basePath":"/travel/hotels","canonicalSite":"www","children":[],"isSubsection":true,"label":"Hotels","parent":"travel","sectionPath":"/hotels","sites":["www","edition"],"title":"Worldwide Inspiration for Hotel Stays","uri":"/travel/hotels/index.html","name":"hotels"},"india":{"basePath":"/india","canonicalSite":"edition","children":[],"isSubsection":true,"label":"India","parent":"asia","sites":["www","edition"],"title":"India News - Breaking News, Video, Headlines and Opinion","uri":"/india/index.html","name":"india","sectionPath":"/india"},"intl_business":{"adsName":"business","basePath":"/business","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Business","sites":["edition"],"title":"CNN Business","uri":"/business/intl_index.html","name":"intl_business","sectionPath":"/business"},"intl_entertainment":{"basePath":"/entertainment","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Entertainment","sites":["edition"],"title":"Entertainment News - Celebrities, Movies, TV, Music","uri":"/entertainment/intl_index.html","name":"intl_entertainment","sectionPath":"/entertainment"},"intl_homepage":{"basePath":"/","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"International Homepage","sites":["edition"],"title":"Breaking News, US News, World News and Video","uri":"/intl_index.html","name":"intl_homepage","sectionPath":"/"},"intl_more":{"basePath":"/more","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - More","sites":["edition"],"title":"More From CNN","uri":"/more/intl_index.html","name":"intl_more","sectionPath":"/more"},"intl_regions":{"adsName":"regions","basePath":"/regions","canonicalSite":"edition","children":["africa","americas","asia","australia","china","europe","india","middleeast","uk"],"isSubsection":false,"label":"Intl - Regions","sites":["edition"],"title":"World News - Breaking News, Video, Headlines and Opinion","uri":"/regions/intl_index.html","name":"intl_regions","sectionPath":"/regions"},"intl_travel":{"adsName":"travel","basePath":"/travel","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - Travel","sites":["edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel/intl_index.html","name":"intl_travel","sectionPath":"/travel"},"intl_tv":{"basePath":"/tv","canonicalSite":"edition","children":["intl_tv-schedule-americas","intl_tv-schedule-asia","intl_tv-schedule-europe","intl_tv-shows"],"isSubsection":false,"label":"Intl - TV","sites":["edition"],"title":"CNN International TV","uri":"/tv/intl_index.html","name":"intl_tv","sectionPath":"/tv"},"intl_tv-schedule-americas":{"basePath":"/tv/schedule/americas","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Americas","parent":"intl_tv","sites":["edition"],"title":"Americas TV Schedule","uri":"/tv/schedule/americas/index.html","name":"intl_tv-schedule-americas","sectionPath":"/tv/schedule/americas"},"intl_tv-schedule-asia":{"basePath":"/tv/schedule/asia","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Asia","parent":"intl_tv","sites":["edition"],"title":"Asia TV Schedule","uri":"/tv/schedule/asia/index.html","name":"intl_tv-schedule-asia","sectionPath":"/tv/schedule/asia"},"intl_tv-schedule-europe":{"basePath":"/tv/schedule/europe","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Schedule Europe","parent":"intl_tv","sites":["edition"],"title":"Europe TV Schedule","uri":"/tv/schedule/europe/index.html","name":"intl_tv-schedule-europe","sectionPath":"/tv/schedule/europe"},"intl_tv-shows":{"basePath":"/tv/shows","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Intl - TV Shows","parent":"intl_tv","sites":["edition"],"title":"International TV Shows","uri":"/tv/shows/intl_index.html","name":"intl_tv-shows","sectionPath":"/tv/shows"},"intl_videos":{"basePath":"/videos","canonicalSite":"edition","children":[],"displayLabel":"","isSubsection":false,"label":"Intl - Videos","sites":["edition"],"title":"Video News","uri":"/videos/intl_index.html","name":"intl_videos","sectionPath":"/videos"},"intl_world":{"adsName":"world","basePath":"/world","canonicalSite":"edition","children":[],"isSubsection":false,"label":"Intl - World","sites":["edition"],"title":"World News","uri":"/world/intl_index.html","name":"intl_world","sectionPath":"/world"},"investing":{"basePath":"investing","canonicalSite":"www","children":[],"isSubsection":true,"label":"Investing","parent":"business","sites":["www","edition"],"title":"Investing","uri":"/business/investing/index.html","name":"investing","sectionPath":"investing"},"living":{"basePath":"/living","canonicalSite":"www","children":[],"isSubsection":false,"label":"Living","sites":["www","edition"],"title":"Living News","uri":"/living/index.html","name":"living","sectionPath":"/living"},"luxury":{"basePath":"/style/luxury","canonicalSite":"www","children":[],"isSubsection":true,"label":"Luxury","parent":"style","sectionPath":"/luxury","sites":["www","edition"],"title":"Luxury","uri":"/style/luxury/index.html","name":"luxury"},"media":{"basePath":"/media","canonicalSite":"www","children":[],"isSubsection":true,"label":"Media","parent":"business","sites":["www","edition"],"title":"Media","uri":"/business/media/index.html","name":"media","sectionPath":"/media"},"middleeast":{"basePath":"/middle-east","canonicalSite":"www","children":[],"isSubsection":true,"label":"Middle East","parent":"intl_regions","sites":["www","edition"],"title":"Middle East News - Breaking News, Video, Headlines and Opinion","uri":"/middle-east/index.html","name":"middleeast","sectionPath":"/middle-east"},"more":{"basePath":"/more","canonicalSite":"www","children":[],"isSubsection":false,"label":"More","sites":["www"],"title":"More From CNN","uri":"/more/index.html","name":"more","sectionPath":"/more"},"motorsport":{"basePath":"/sport/motorsport","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Motorsport","parent":"sport","sectionPath":"/motorsport","sites":["www","edition"],"title":"Motorsport News","uri":"/sport/motorsport/index.html","name":"motorsport"},"movies":{"basePath":"/entertainment/movies","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"Movies","parent":"entertainment","sectionPath":"/movies","sites":["www","edition"],"title":"Movies - Entertainment News","uri":"/entertainment/movies/index.html","name":"movies"},"news":{"basePath":"/travel/news","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel - News","parent":"travel","sectionPath":"/news","sites":["www","edition"],"title":"Travel - News","uri":"/travel/news/index.html","name":"news"},"olympics":{"basePath":"/sport/olympics","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Olympics","parent":"sport","sectionPath":"/olympics","sites":["www","edition"],"title":"2020 Summer Olympics in Tokyo, Japan","uri":"/sport/olympics/index.html","name":"olympics"},"opinions":{"adsName":"opinion","basePath":"/opinions","canonicalSite":"www","children":[],"isSubsection":false,"label":"Opinion","sites":["www"],"title":"Opinion, Commentary, Analysis","uri":"/opinions/index.html","name":"opinions","sectionPath":"/opinions"},"perspectives":{"basePath":"/perspectives","canonicalSite":"www","children":[],"isSubsection":true,"label":"Perspectives","parent":"business","sites":["www","edition"],"title":"Perspectives","uri":"/business/perspectives/index.html","name":"perspectives","sectionPath":"/perspectives"},"energy":{"basePath":"/energy","canonicalSite":"www","children":[],"isSubsection":true,"label":"Energy","parent":"business","sites":["www","edition"],"title":"Energy","uri":"/business/energy/index.html","name":"energy","sectionPath":"/energy"},"cars":{"basePath":"/cars","canonicalSite":"www","children":[],"isSubsection":true,"label":"Cars","parent":"business","sites":["www","edition"],"title":"Cars","uri":"/business/cars/index.html","name":"cars","sectionPath":"/cars"},"homes":{"basePath":"/homes","canonicalSite":"www","children":[],"isSubsection":true,"label":"Homes","parent":"business","sites":["www","edition"],"title":"Homes","uri":"/business/homes/index.html","name":"homes","sectionPath":"/homes"},"play":{"basePath":"/travel/play","canonicalSite":"www","children":[],"isSubsection":true,"label":"Play","parent":"travel","sectionPath":"/travel-play","sites":["www","edition"],"title":"What To Do","uri":"/travel/play/index.html","name":"play"},"politics":{"basePath":"/politics","canonicalSite":"www","children":["election-2018","election-center-2016"],"displayLabel":"","isSubsection":false,"label":"Politics","sites":["www","edition"],"title":"Political News, Analysis and Opinion","uri":"/politics/index.html","name":"politics","sectionPath":"/politics"},"profiles":{"basePath":"/profiles","canonicalSite":"www","children":[],"displayLabel":"CNN Profiles","isSubsection":false,"label":"Profiles","sites":["www","edition"],"title":"CNN Profiles","uri":"/profiles/index.html","name":"profiles","sectionPath":"/profiles"},"sailing":{"adsName":"mainsail","basePath":"/sport/sailing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Sailing","parent":"sport","sectionPath":"/sailing","sites":["www","edition"],"title":"Sailing News","uri":"/sport/sailing/index.html","name":"sailing"},"skiing":{"basePath":"/sport/skiing","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Skiing","parent":"sport","sectionPath":"/skiing","sites":["www","edition"],"title":"Skiing News","uri":"/sport/skiing/index.html","name":"skiing"},"sport":{"adsName":"worldsport","basePath":"/sport","canonicalSite":"edition","children":["equestrian","football","golf","horseracing","motorsport","olympics","sailing","skiing","tennis"],"isSubsection":false,"label":"Sports","sites":["www","edition"],"title":"Sport News","uri":"/sport/index.html","name":"sport","sectionPath":"/sport"},"sports":{"basePath":"/sports","canonicalSite":"www","children":[],"isSubsection":false,"label":"Sports","sites":["www"],"title":"Sports News","uri":"/sports/index.html","name":"sports","sectionPath":"/sports"},"stay":{"basePath":"/travel/stay","canonicalSite":"www","children":[],"isSubsection":true,"label":"Stay","parent":"travel","sectionPath":"/travel-stay","sites":["www","edition"],"title":"Places to Stay","uri":"/travel/stay/index.html","name":"stay"},"style":{"basePath":"/style","canonicalSite":"www","children":["architecture","arts","autos","beauty","design","fashion","luxury"],"isSubsection":false,"label":"Style","sites":["www","edition"],"title":"CNN Style - Fashion, Design, Art, Architecture and Luxury","uri":"/style/index.html","name":"style","sectionPath":"/style"},"style-home":{"basePath":"/style-home","canonicalSite":"www","children":[],"isSubsection":true,"label":"Style - Home","parent":"style","sites":["www","edition"],"title":"CNN Style - Fashion, Design, Art, Architecture and Luxury","uri":"/style-home/index.html","name":"style-home","sectionPath":"/style-home"},"style-show":{"basePath":"/style-show","canonicalSite":"www","children":[],"isSubsection":true,"label":"Style - Show","parent":"style","sites":["www","edition"],"title":"Style Show","uri":"/style-show/index.html","name":"style-show","sectionPath":"/style-show"},"success":{"basePath":"/success","canonicalSite":"www","children":[],"isSubsection":true,"label":"Success","parent":"business","sites":["www","edition"],"title":"Success","uri":"/business/success/index.html","name":"success","sectionPath":"/success"},"tech":{"basePath":"/tech","canonicalSite":"www","children":[],"isSubsection":true,"label":"Tech","parent":"business","sites":["www","edition"],"title":"Tech News","uri":"/business/tech/index.html","name":"tech","sectionPath":"/tech"},"tennis":{"basePath":"/sport/tennis","canonicalSite":"edition","children":[],"isSubsection":true,"label":"Tennis","parent":"sport","sectionPath":"/tennis","sites":["www","edition"],"title":"Tennis News","uri":"/sport/tennis/index.html","name":"tennis"},"travel":{"basePath":"/travel","canonicalSite":"www","children":["destinations","foodanddrink","hotels","news","play","stay","travel-home","travel-video-hub"],"isSubsection":false,"label":"Travel","sites":["www","edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel/index.html","name":"travel","sectionPath":"/travel"},"travel-home":{"basePath":"/travel-home","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel - Home","parent":"travel","sites":["www","edition"],"title":"CNN Travel | Global Destinations, Tips & Video","uri":"/travel-home/index.html","name":"travel-home","sectionPath":"/travel-home"},"travel-video-hub":{"basePath":"/travel/videos","canonicalSite":"www","children":[],"isSubsection":true,"label":"Travel Video Hub","parent":"travel","sectionPath":"/travel-video-hub","sites":["www","edition"],"title":"Travel Videos","uri":"/travel/videos/index.html","name":"travel-video-hub"},"tv":{"basePath":"/tv","canonicalSite":"www","children":["tv-schedule-cnn"],"isSubsection":false,"label":"TV","sites":["www"],"title":"CNN TV","uri":"/tv/index.html","name":"tv","sectionPath":"/tv"},"tv-schedule-cnn":{"basePath":"/tv/schedule/cnn","canonicalSite":"www","children":[],"isSubsection":true,"label":"TV Schedule - CNN","parent":"tv","sites":["www"],"title":"TV Schedule - CNN","uri":"/tv/schedule/cnn/index.html","name":"tv-schedule-cnn","sectionPath":"/tv/schedule/cnn"},"tv-shows":{"basePath":"/entertainment/tv-shows","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":true,"label":"TV Shows","parent":"entertainment","sectionPath":"/tv-shows","sites":["www"],"title":"TV Shows - Entertainment News","uri":"/entertainment/tv-shows/index.html","name":"tv-shows"},"uk":{"basePath":"/uk","canonicalSite":"edition","children":[],"isSubsection":true,"label":"United Kingdom","parent":"europe","sites":["www","edition"],"title":"U.K. News - Breaking News, Video, Headlines and Opinion","uri":"/uk/index.html","name":"uk","sectionPath":"/uk"},"us":{"basePath":"/us","canonicalSite":"www","children":[],"displayLabel":"US","isSubsection":false,"label":"US","sites":["www","edition"],"title":"U.S. News - Breaking News, Video, Headlines and Opinion","uri":"/us/index.html","name":"us","sectionPath":"/us"},"videos":{"adsName":"video","basePath":"/videos","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"Videos","sites":["www"],"title":"Video News","uri":"/videos/index.html","name":"videos","sectionPath":"/videos"},"vr":{"basePath":"/vr","canonicalSite":"www","children":[],"displayLabel":"","isSubsection":false,"label":"VR","sites":["www","edition"],"title":"Virtual Reality & 360° Video - CNNVR","uri":"/vr/index.html","name":"vr","sectionPath":"/vr"},"watch-cnn":{"basePath":"/tv/watch/cnn","canonicalSite":"www","children":[],"isSubsection":true,"label":"Watch CNN","parent":"tv","sectionPath":"/watch-cnn","sites":["www","edition"],"title":"Watch CNN Live - Stream CNN Live Online","uri":"/tv/watch/cnn/index.html","name":"watch-cnn"},"weather":{"basePath":"/weather","canonicalSite":"www","children":[],"isSubsection":false,"label":"Weather","sites":["www","edition"],"title":"Latest Weather and Extended Forecast","uri":"/weather/index.html","name":"weather","sectionPath":"/weather"},"world":{"basePath":"/world","canonicalSite":"www","children":[],"isSubsection":false,"label":"World","sites":["www"],"title":"World News","uri":"/world/index.html","name":"world","sectionPath":"/world"}},"vertical":"news"}});
                    
(function (d) {var e = d.createElement('script');e.async = true;e.type = 'text/javascript';e.onload = function _onJSMDLoad(e) {jQuery(d).triggerAnalyticsReady();};e.src = '//lightning.cnn.com/launch/7be62238e4c3/97fa00444124/launch-2878c87af5e3.min.js';d.body.appendChild(e);})(document);
if (WM.UserConsent.inUserConsentState(["data-store","measure-ads","measure-content","measure-market","product-develop"], { id: "usabilla" })) {CNN.INJECTOR.loadFeature('usabilla');}
(function (doc, fd) {fd.measure(function () {var scpt = doc.getElementsByTagName('script')[0];fd.mutate(function () {WM.UserConsent.addScript({async: true,id: 'quantScript',src: (doc.location.protocol === 'https:' ? 'https://secure.quantserve.com/quant.js' : 'http://edge.quantserve.com/quant.js'),type: 'text/javascript'}, ["vendor","measure-content"], scpt.parentNode);});});}(document, fastdom));
window._sf_async_config = window._sf_async_config || {};window._sf_async_config.uid = 37612;window._sf_async_config.domain = '' || 'edition.cnn.com';window._sf_async_config.flickerControl = false;window._sf_async_config.useCanonical = true;window._sf_async_config.autoDetect = false;var _sf_startpt=Date.now();WM.UserConsent.addScript({async: true,src: '//static.chartbeat.com/js/chartbeat_mab.js'}, ["data-store","content-person","measure-content"]);
if (!CNN.Features || CNN.Features.enableBounceX !== false) {(function (d) {WM.UserConsent.addScript({async: true,src: d.location.protocol + '//tag.bounceexchange.com/340/i.js'}, ["iab","vendor","data-store","ads-contextual","ads-person-prof","ads-person","content-person-prof","content-person","measure-ads","measure-content","measure-market","product-develop"]);})(document);}
(function($){$(document).onZonesAndDomReady(function () {if (Modernizr.android === true) {$('head').append('<meta name="theme-color" content="#000000">');$('head').append('<link href="//cdn.cnn.com/cnn/.e/img/3.0/global/misc/cnn-logo.png" rel="icon" sizes="192x192">');}});}(jQuery));
!function(_window, _document) {var OB_ADV_ID = '00b2d6c56fc76084821b9d05abf2f201d9',api;if (_window.obApi) {if (!Array.isArray(_window.obApi.marketerId)) {_window.obApi.marketerId = [_window.obApi.marketerId];}return;}api = _window.obApi = function () {var a = window.obApi;a.dispatch ? a.dispatch.apply(a, arguments) : a.queue.push(arguments);};api.version = '1.0';api.loaded = true;api.marketerId = OB_ADV_ID;api.queue = [];WM.UserConsent.addScript({async: true, src: '//amplify.outbrain.com/cp/obtp.js'}, ["iab","vendor","data-store","ads-contextual","ads-person-prof","ads-person","content-person-prof","content-person","measure-ads","measure-content","measure-market","product-develop"], _document.getElementsByTagName('script')[0].parentNode);}(window, document);obApi('track', 'PAGE_VIEW');document.addEventListener('click', function(event) {var el = event.target;if (el && (el.tagName === 'A' || (el.parentNode && el.parentNode.tagName === 'A'))) {obApi('track', 'Exit Link Clicks');}});
if (WM.UserConsent.inUserConsentState(["vendor","measure-content"], { id: "twitterPixel" })) {(function (w, d) {var e,s;if (!w.twq) {s = w.twq = function () {s.exe ? s.exe.apply(s, arguments) : s.queue.push(arguments);};s.version = '1.1';s.queue = [];e = d.createElement('script');e.async = true;e.type = 'text/javascript';e.src = '//static.ads-twitter.com/uwt.js';d.getElementsByTagName('body')[0].appendChild(e);}})(window, document);twq('init', 'nyutn');twq('track', 'PageView');}
WM.UserConsent.addScript({async: true,defer: true,src: "//get.s-onetag.com/c15ddde9-ec7d-4a49-b8ca-7a21bc4b943b/tag.min.js"}, ["iab","vendor","data-store","ads-contextual","ads-person-prof","ads-person","content-person-prof","content-person","measure-ads","measure-content","measure-market","product-develop"]);
(function (win, doc, WM) {win['bt'] = win['bt'] || function () { (win['_bt'] = win['_bt'] || []).push(arguments); };WM.UserConsent.addScript({async: true,src: '//cdn.boomtrain.com/p13n/cnn/p13n.min.js'}, ["vendor","data-store","ads-contextual","ads-person-prof","ads-person","content-person-prof","content-person","measure-ads","measure-content","measure-market","product-develop"]);})(window, document, WM);
_satellite["_runScript1"](function(event, target, Promise) {
window.wminst = window.wminst || {};
wminst.Util = function() {
    return {
        loadCustomVariables: function() {
            this.tmsName = "launch";
            this.businessName = "cnn";
            this.buildVersion = 17; // Build Update Date 24th Mar 2021
            this.buildEnv = this.getBuildEnv();
            this.buildDate = this.getBuildDate();
            this.debugFlag = "WMINST_DEBUG";
            this.logPrefix = "[WMINST]";
            window.is_expansion = true;
            wminst.subscribersReady = false;
            wminst.hpt_set = 0;
            wminst.buffer_count = 0;
            wminst.is_podcast = 0;
            wminst.is_scrubbed = false;
            if (window.cnn_metadata) {
                window.is_expansion = false;
            }
        },
        getBuildEnv: function() {
            return {
                "development": "dev",
                "staging": "qa",
                "production": "prod"
            }[_satellite.buildInfo.environment];
        },
        getBuildDate: function() {
            return _satellite.buildInfo.buildDate.split("T")[0].replace(/-/g, "");
        },
        getCNNCodeVersion: function() {
            return [this.tmsName, this.businessName, this.buildEnv, this.buildVersion, this.buildDate].join(".");
        },
        setDebug: function(flag) {
            if (flag == true) {
                sessionStorage.setItem(this.debugFlag, true);
            } else {
                sessionStorage.removeItem(this.debugFlag);
            }
        },
        log: function() {
            var logEnabled = sessionStorage.getItem(this.debugFlag);
            if (logEnabled) {
                var args = Array.prototype.slice.call(arguments);
                args.unshift(this.logPrefix);
                console.log.apply(console, args);
            }
        },
        getTagConsentStatesV1: function(name) {
			return {
				"adobe"           	: ["perf-general"],
				"comscore"        	: ["perf-vendor"],
				"nielsen"			: ["perf-vendor"],
				"facebook-pixel"	: ["perf-vendor", "social-vendor"],
				"zion"				: ["perf-general", "person-general"],
				"att-wm-id"			: ["perf-general", "person-general", "ad-general", "social-general", "storage-general", "behavior-general"],
				"app-nexus-id"		: ["ads-vendor"],
				"trackonomics"		: ["ads-general", "ads-vendor", "behavior-general", "perf-general", "person-general", "social-general", "storage-general"],
				"viglink"			: ["ads-vendor"],
				"quantcast"			: ["ads-vendor"],
				"amazon"			: ["ads-vendor"],
				"bounce-x"			: ["iab", "behavior-vendor", "person-vendor", "storage-vendor"],
				"chartbeat"			: ["perf-general"],
				"keywee"			: ["ads-vendor", "behavior-vendor", "storage-vendor", "perf-vendor"],
				"krux"				: ["ads-vendor"],
				"stack-sonar"		: ["ads-general"],
				"optimizely"		: ["behavior-general", "perf-general", "person-general"],
				"bombora"			: ["iab"]
			}[name];
		},
		getTagConsentStatesV2: function(name) {
			return {
				"adobe"				: ["data-store", "content-person-prof", "content-person", "measure-content", "measure-market", "product-develop"],
				"comscore"			: ["vendor", "measure-content"],
				"nielsen"			: ["vendor", "measure-content", "data-store"],
				"facebook-pixel"	: ["data-store", "ads-contextual", "ads-person-prof", "ads-person", "vendor"],
				"zion"				: ["data-store", "ads-person-prof", "ads-person", "content-person-prof", "content-person", "measure-content"],
				"att-wm-id"			: ["data-store", "ads-contextual", "ads-person-prof", "ads-person", "content-person-prof", "content-person", "measure-ads", "measure-content", "measure-market", "product-develop", "vendor"],
				"app-nexus-id"		: ["vendor"],
				"trackonomics"		: ["data-store", "measure-ads", "vendor"],
				"viglink"			: ["data-store", "measure-content", "vendor"],
				"quantcast"			: ["iab"],
				"amazon"			: ["data-store", "ads-contextual", "ads-person-prof", "ads-person", "vendor"],
				"bounce-x"			: ["iab"],
				"chartbeat"			: ["data-store", "measure-content"],
				"keywee"			: ["data-store", "ads-person-prof", "ads-person", "measure-ads", "measure-market", "vendor"],
				"krux"				: ["data-store", "ads-person-prof", "ads-person", "measure-ads", "measure-content", "measure-market"],
				"stack-sonar"		: ["data-store", "ads-contextual", "ads-person-prof", "ads-person"],
				"optimizely"		: ["data-store", "content-person-prof", "content-person", "measure-ads", "measure-content", "vendor"],
				"bombora"			: ["vendor", "data-store", "ads-person-prof", "measure-ads", "measure-content", "product-develop"],
                "outbrain-pixel"    : ["ads-person-prof", "ads-person", "measure-ads"],
                "full-story"		: ["measure-content", "product-develop"]
			}[name];
		},
        getTagConsentStates: function(name) {
            if (window.WM && WM.UserConsent && WM.UserConsent.getVersion().indexOf("1") === 0) {
                return this.getTagConsentStatesV1(name);
            }
            return this.getTagConsentStatesV2(name);
        },
        isUSRegion: function() {
            if (window.WM && WM.UserConsent) {
                return WM.UserConsent.isInCcpaRegion();
            } else {
                return _satellite.cookie.get("countryCode") === "US";
            }
        },
        isTagConsented: function(name) {
            // Special handling for ATT WM ID, AppNexus ID, and Quantcast
            if (name == "att-wm-id") {
                return this.isUSRegion();
            }
            if (name == "app-nexus-id" && !this.isUSRegion()) {
                return false;
            }
            if (name == "quantcast" && this.isUSRegion()) {
                return false;
            }            
            var states = this.getTagConsentStates(name);
            if (window.WM && WM.UserConsent) {
                if (WM.UserConsent.isReady() && WM.UserConsent.inUserConsentState(states, {id: name})) {
                    return true;
                }
            } else {
                return true;
            }
            return false;
        },
        isPrismEnabled: function() {
            if (window.WM && window.WM.CDP && typeof window.WM.CDP.isIdentityEnabled === "function") {
                return window.WM.CDP.isIdentityEnabled();
            }
            return false;
        },      
        inIFrame: function() {
            try {
                return window.self !== window.top;
            } catch (e) {
            return true;
            }
        },
        getQueryParam: function(key, loc) {
            if (!this.params || loc) {
            var search = loc || window.location.search;
            var params = search.replace(/^\?/, ""), paramObj = {};
            params = params.split("&");
            for (var i = 0; i < params.length; i++) {
              var t = params[i].split("=");
              paramObj[t[0]] = t[1]
            }
            if (!loc) {
                this.params = paramObj;
            } else {
              return paramObj[key] || "";
            }
          }
          return this.params[key] || "";
        },
        isSearchPage: function() {
            return window.location.pathname.indexOf("/search") === 0;
        },
        isRefreshPage: function() {
            return wminst.Util.getQueryParam("refresh");
        },
        isStellarPage: function() {
            return this.getCNNTechStack() === "stellar2.0";
        },
        isUnderscoredPage: function() {
            return (window.CNN && CNN.omniture && CNN.omniture.section && CNN.omniture.section[0] === "cnn-underscored");
        },      
        isStylePage: function() {
            return (window.CNN && CNN.omniture && CNN.omniture.section && CNN.omniture.section[0] === "style");
        },
        isTravelPage: function() {
            return (window.CNN && CNN.omniture && CNN.omniture.section && CNN.omniture.section[0] === "travel");
        },
        isElectionDynamicPage: function() {
            return window.location.pathname.match(/\/election/) !== null && window.location.pathname.match(/20(17|18|19)/) !== null;
        },
        isUserAccountPage: function() {
            return window.location.pathname.match(/\/account\/(register|preferences|confirm|reset-password|log-in)\/?$/) !== null;
        },
        isNewsletterHub: function() {
            return window.location.pathname.match(/\/newsletters\/?$/) !== null;
        },
      	isPoliticsExplorer: function() {
            return (window.CNN && CNN.omniture && CNN.omniture.is_explorer);
        },
        isLiveStoryPage: function() {
            return window.location.pathname.indexOf("live-news") !== -1;
        },
        isLiveStoryStellarPage: function() {
            return this.isLiveStoryPage() && this.isStellarPage();
        },      
        isLiveStoryNonStellarPage: function() {
            return this.isLiveStoryPage() && !this.isStellarPage();
        },
        isSpeedyPage: function() {
            return window.location.hostname.indexOf("-m.cnn.com") !== -1;
        },        
        isDynamicPage: function() {
            return this.isSearchPage() || this.isRefreshPage() || this.isElectionDynamicPage() || this.isLiveStoryNonStellarPage() || this.isSpeedyPage();
        },
        isLightweightPage: function() {
            return this.isUserAccountPage() || this.isNewsletterHub();
        },
        isFavePage: function() {
            return window.location.hostname.indexOf("fave.api.cnn.io") !== -1 || window.location.hostname.indexOf("fave-api.cnn.com") !== -1;
        },
        isFBIAPage: function () {
            try {
                if(window.CNN.omniture.fbia && (window.CNN.omniture.fbia === true || window.CNN.omniture.fbia === "true")){
                    return true;
                } else {
                    return false;
                }
            }catch(e){ return false;}
        },
        isLiveStoryTemplateType: function() {
            var templateType = ((window.CNN || {}).omniture || {}).template_type || {};
            return (templateType == "live story" || templateType == "article_livestory");
        },
        isEmpty: function(obj) {
            for (var key in obj) {
                if (obj.hasOwnProperty(key))
                    return false;
            }
            return true;
        },
        isVideoAutoStarted: function(data) {
            if (typeof data.isAutoplayAllowed !== "undefined" && typeof data.isAutostartSuccessful !== "undefined") {
                if ((data.isAutoplayAllowed === false && data.isAutostartSuccessful === false) || (data.isAutoplayAllowed === true && data.isAutostartSuccessful === false)) {
                    return false;
                } else {
                    return true;
                }
            } else if (typeof data.is_autoplay_allowed !== "undefined" && typeof data.is_autoplay_successful !== "undefined") {
                if ((data.is_autoplay_allowed === false && data.is_autoplay_successful === false) || (data.is_autoplay_allowed === true && data.is_autoplay_successful === false)) {
                    return false;
                } else {
                    return true;
                }
            }
        },
        getVideoMetadata: function(data) {
            if (!this.isEmpty(data.video)) {
                return data.video;
            } else {
                return data;
            }
        },
        sendImagePixel: function(url) {
            var image = new Image();
            image.src = url;
            image.style.display = "none";
            image.width = 1;
            image.height = 1;
        },
        loadScript: function(src, callback) {
            var e = document.createElement('script');
            e.type = 'text/javascript';
            e.async = true;
            e.src = src;
            if (callback) {
                e.addEventListener('load', callback);
            }
            var n = document.getElementsByTagName('script')[0];
            n.parentNode.insertBefore(e, n);
        },
        getCookie: function(param, flag) {
            var r = _satellite.cookie.get(param)|| "";
            if (flag === 'c' || flag === 1) {
                _satellite.cookie.set(param, "-", -1000);
            }
            return unescape(r);
        },
        getCNNEvent: function() {
            var rval = wminst.Util.getCNNBrandingPartner();
            var tt = ""; var cctype = "";
            var pathName = window.location.pathname;
            var pathNameArray = pathName.split("/");
            if(typeof window.CNN !== 'undefined' && typeof window.CNN.omniture !== 'undefined' &&  typeof window.CNN.omniture.template_type !== 'undefined'){
                tt = window.CNN.omniture.template_type;
            }
            if( typeof window.CNN !== 'undefined' && typeof window.CNN.omniture !== 'undefined' &&  typeof window.CNN.omniture.cap_content_type !== 'undefined'){
                cctype = window.CNN.omniture.cap_content_type;
            }
            var events = "";
            if(rval == "" || rval == "nvs" || rval == "no value set" || rval == "no-value-set"){
               events =  "event26";   
            } else {
                events =  "event21,event26";
            }
            if(tt == "article" || cctype == "article"){
                events = events + ",event39";
            }
            if (tt !== "error" && pathNameArray[1] == "video-day") {
                events = events + ",event63";
            }
            if (tt !== "error" && pathName.indexOf("/account/register") > -1) {
                events = events + ",event51";
            }
            return events;
        },
        getCNNBusinessName: function() {
            return "cnn";
        },
        getCNNCampaign: function(){
           if (wminst.Util.isFBIAPage()) {
               return "fbia";
           }
           return;
        },
        getCNNDomainName: function() {
          var hostname = window.location.hostname.toLowerCase();
          hostname = hostname.replace("www.","");
          return hostname;
        },
        getCNNPageURL: function() { //s.pageURL or g variable
            var rval = window.location.href.toLowerCase(), loc = "";
            if (wminst.Util.isFBIAPage()) {
                loc = rval;
                rval = "";
                if (loc.indexOf("ofs=fbia") > -1) {
                    loc = loc.replace("ofs=fbia", "csr=fbiacnn"); //suppressing string which is not expected as per new requirement
                }
                var jj = (loc.indexOf("?") != -1 ? "&" : "?");
                if (loc.indexOf("csr=fbiacnn") > -1) {
                    rval = loc + "";
                } else {
                    rval = loc + jj + "csr=fbiacnn"; // added expected substring
                }
            }
            return rval;
        },
        getCNNPageType: function() {
            var rval = "";
            try {
                var title = document.title.toLowerCase();
                if (title.indexOf("page not found") !== -1 || wminst.Util.getCNNTemplateType() == "adbp:error" || title == "error") {
                    rval = "errorPage";
                }
            } catch (err) {}
            return rval;
        },
        getCNNAuthor: function() { //prop2,eVar2 - business.cnn.page.author
            var rval = "";
            if (window.is_expansion) {
                try {
                    rval = window.cnn_d.omniture.cap_author;
                } catch (e) {}
                try {
                    rval = window.CNN.omniture.cap_author.toString();
                } catch (e) {}
            } else {
                try {
                    rval = window.cnn_metadata.business.cnn.page.author;
                } catch (e) {}
                if (!rval) {
                    if (document.getElementsByName("AUTHOR").item(0)) {
                        rval = document.getElementsByName("AUTHOR").item(0).content;
                    } else if (document.getElementsByName("author").item(0)) {
                        rval = document.getElementsByName("author").item(0).content;
                    }
                }
            }
            if (typeof rval === "undefined" || rval == "no-value-set" || rval == "nvs") rval = "";
            return rval.toLowerCase();
        },
        getPageAttribution: function() { //prop4,eVar4 - page HPlocation
            var rval = "";
            var ishptCookie = false;
            var hptcookie = wminst.Util.getCookie("hpt");
            var linkTrackingCookie = wminst.Util.getCookie("linkTracking");
            var regex = new RegExp("^[A-Za-z0-9=]+$");
            if ((typeof linkTrackingCookie == 'undefined' || linkTrackingCookie == "") && typeof hptcookie !== 'undefined') {
                ishptCookie = true;
            }
            var attributionCookie = linkTrackingCookie || hptcookie;
            if ((typeof attributionCookie != "undefined" && attributionCookie != "" && attributionCookie.indexOf("breaking:") != -1) || !regex.test(attributionCookie)) {
                rval = attributionCookie;
            } else if (document.referrer.indexOf("cnn.com") !== -1) {
                rval = wminst.Util.getQueryParam("linkTracking") || wminst.Util.getQueryParam("hpt");
                try {
                    rval = rval.replace(/no\-value\-set/g, "");
                } catch (e) {}
                var prev_rval = rval;
                try {
                    if (attributionCookie) {
                        rval = attributionCookie;
                        if (attributionCookie.indexOf("_") === -1 && attributionCookie.indexOf("|") === -1 && typeof window.CNN.Utils.b64Decode(attributionCookie) !== 'undefined') {
                            rval = window.CNN.Utils.b64Decode(attributionCookie);
                        }
                    }
                } catch (e) {}
                if (rval) {
                    wminst.hpt_set = 1;
                } else {
                    rval = prev_rval;
                }
                //document.cookie = "hpt=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/;";
            }
            if (window.is_expansion != 0) {
                if (wminst.Util.getQueryParam("cnnapp") && wminst.Util.getQueryParam("cnnapp") != null) {
                    rval = "cnnapp:" + wminst.Util.getQueryParam("cnnapp");
                }
                if (wminst.Util.getQueryParam("eref") && wminst.Util.getQueryParam("eref") != null) {
                    rval = "eref:" + wminst.Util.getQueryParam("eref");
                }
                if (wminst.Util.getQueryParam("iref") && wminst.Util.getQueryParam("iref") != null) {
                    rval = "iref:" + wminst.Util.getQueryParam("iref");
                }
                if (wminst.Util.getQueryParam("refresh") && wminst.Util.getQueryParam("refresh") != null) {
                    rval = "auto-refresh";
                }
            }
            if(rval !== "") {
              rval = rval.replace(/no-value-set/g, "nvs");
              rval = rval.toLowerCase();   
            }
            if (ishptCookie) {
                document.cookie = "hpt=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/; domain=.cnn.com;";
            } else {
                document.cookie = "linkTracking=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/; domain=.cnn.com;";
            }
            return rval;
        },
        getPhotoGalleryName: function(){ //prop6,eVar6 - Photo Gallery name
            var rval = "";
            if(typeof window.CNN !== 'undefined' && typeof window.CNN.omniture !== 'undefined' && typeof window.CNN.omniture.gallery_name !== 'undefined'){
                rval = window.CNN.omniture.gallery_name;
                rval = rval.toLowerCase();
            }
            return rval;
        },
        getCNNVisitNumber: function(rollday) { //prop8,eVar8 - visit_number.$30Day  
            rollday = rollday || 28; //default rolling day is 28
            var todaydate = new Date().getTime();
            if (typeof(Storage) !== "undefined") { //check for web storage support
                if (localStorage.startdate) { //check for start date
                    if (sessionStorage.online) { //check for session variable
                        var daysinceonline = Math.ceil((todaydate - sessionStorage.online) / 86400000);
                        if (daysinceonline > 1) { //if session is older than 24 hours, reset session start time and count as a visit
                            localStorage.visittype = "repeat"; //set visit type (new vs repeat)
                            localStorage.visitnum = Number(localStorage.visitnum) + 1; //increment visit number
                            sessionStorage.online = todaydate; //set session variable
                        }
                    } else { //new session
                        localStorage.visittype = "repeat"; //set visit type (new vs repeat)
                        localStorage.visitnum = Number(localStorage.visitnum) + 1; //increment visit number
                        sessionStorage.online = todaydate; //set session variable
                    }
                    var daysincestart = Math.ceil((todaydate - localStorage.startdate) / 86400000);
                    if (daysincestart > Number(rollday)) { //if days since start date is greater than rolling day, set new start date
                        localStorage.startdate = todaydate;
                        localStorage.visittype = "new";
                        localStorage.visitnum = 1;
                    }
                } else { //first new visit
                    localStorage.startdate = todaydate; //set new start date
                    localStorage.visittype = "new"; //set visit type (new vs repeat)
                    localStorage.visitnum = 1; //set visit number
                    sessionStorage.online = todaydate; //set session variable
                }
                return localStorage.visittype + ":" + localStorage.visitnum;
            } else {
                return "new:1";
            }
        },
        getCNNCapMediaType: function() {
            var rval = "nvs";
            try{
                if (window.CNN && window.CNN.omniture && window.CNN.omniture.cap_media_type) {
                    if (window.CNN.omniture.cap_media_type === "no-value-set"){
                        rval = "nvs";
                    } else {
                        rval = window.CNN.omniture.cap_media_type;
                    }
                }
            rval = rval.toLowerCase();              
            } catch(e) {}
            return rval;
        },
        getCNNPublishDate: function() {
            var rval = "";
            try {
                rval = window.cnn_metadata.business.cnn.page.publish_date
            } catch (e) {}
            try {
                if (window.CNN && window.CNN.omniture && window.CNN.omniture.publish_date ) {
                    rval = window.CNN.omniture.publish_date;
                }
                if (rval && window.CNN && window.CNN.omniture && window.CNN.omniture.last_updated_date) {
                    rval = rval + "|" + window.CNN.omniture.last_updated_date;
                }
            
            } catch (e) {}
            try {
                if (!rval && window.cnn_d && window.cnn_d.omniture && window.cnn_d.omniture.publish_date) {
                    rval = window.cnn_d.omniture.publish_date;
                }
        
            } catch (e) {}
            return rval;
        },
        populatePublishDate: function(){
            var rval = wminst.Util.getCNNPublishDate();
            var etype = ["content","other:live story","adbp:article_livestory","gallery"];
            var rttype = wminst.Util.getCNNTemplateType("long");
            var result = false;
            if (typeof rttype !== 'undefined') {
               for(var i in etype){
                  if(rttype.indexOf(etype[i]) != -1){
                      result  = true;
                  }
                }
            }
           if (result) {
              return rval;
           } else {
              return "";
           }
        },
        getCNNDaysSinceLastPublish: function(d) { //prop10,eVar10 - days_since_publish
            var e = new Date();
            var p;
            var j;
            if (d == 'a') {
                try {
                    d = window.cnn_metadata.business.cnn.page.publish_date;
                } catch (err) {}
                try {
                    d = window.CNN.omniture.publish_date || d;
                } catch (err) {}
                j = new Date(d);
            } else if (d.toString().indexOf("/") != -1) {
                p = d.split("/");
                if (p[0].length != 4) {
                    p[2] = "20" + p[2];
                    j = new Date(p[2] + "/" + p[0] + "/" + p[1]);
                } else {
                    j = new Date(d);
                }
            } else {
                j = new Date(d);
            }
            var ONE_DAY = 1000 * 60 * 60 * 24;
            var date1_ms = e.getTime();
            var date2_ms = j.getTime();
            var difference_ms = Math.abs(date1_ms - date2_ms)
            var days = Math.round((difference_ms / ONE_DAY))
            if (isNaN(days)) {
                return "";
            }
            if (window.is_expansion != 0) {
                return Math.round((difference_ms / ONE_DAY)).toString()
            } else if (window.is_expansion == 0 && typeof window.cnn_metadata.days_since_publish !== "undefined") {
                try {
                    return window.cnn_metadata.days_since_publish;
                } catch (err) {}
            }
        },
        populateDaysSinceLastPublish: function(){
            var rval =  wminst.Util.getCNNDaysSinceLastPublish("a");
            var etype = ["content:","other:live story","adbp:article_livestory"];
            var rttype = wminst.Util.getCNNTemplateType("long");
            var result = false;
            if (typeof rttype !== 'undefined') {
                for(var i in etype){
                    if (rttype.indexOf(etype[i]) != -1){
                        result  = true;
                    }
                }
            }
            if(result) {
                return rval;
            } else {
                return "";
            }
        },
        getCNNBrandingPartner: function() { //prop11,eVar11 - page branding content partner
            var rval = "";
            var bp = "";
            try {
                rval = (cnn_metadata.business.cnn.page.branding_partner ? cnn_metadata.business.cnn.page.branding_partner : window.cnnOmniPartner || "");
            } catch (e) {}
            try {
                if (typeof window.CNN.omniture.branding_content_page != 'undefined') {
                    bp = window.CNN.omniture.branding_content_page;
                    bp = bp.replace("default", "");
                    if (bp) {
                        rval = "p:" + bp;
                    }
                }
            } catch (e) {}
            try {
                if (window.CNN.omniture.branding_gallery || (bp && window.CNN.contentModel.analytics.pageTop.type === 'gallery')) {
                    rval = "g:" + (window.CNN.omniture.branding_gallery ? window.CNN.omniture.branding_gallery : bp);
                }
            } catch (e) {}
            try {
                if (typeof window.CNN.omniture.template_type != 'undefined' && window.CNN.omniture.template_type == "error") {
                    rval = ""; //suppressed branding partner(prop11,eVar11) value for error page
                }
            } catch (e) {}
            return rval.toLowerCase();
        },
        getCNNCapContentType: function (){ //prop13,eVar13 - cap_content_type
            var rval = "";
            try {
                if(window.CNN.contentModel && window.CNN.contentModel.analytics.pageTop.type === 'gallery'){
                    rval = "gallery";
                } else {
                    rval = window.CNN.omniture.cap_content_type;
                }
                rval = rval.toLowerCase();
            } catch(e) {
                rval = "";
            }
            return rval;
        },
        getCNNCapGenre: function (){ //prop5,eVar5 - cap genre
            var rval = "";
            if(window.CNN && window.CNN.omniture && typeof window.CNN.omniture.cap_genre != "undefined"){
                if( window.CNN.omniture.cap_genre == "" || window.CNN.omniture.cap_genre == "no-value-set")
                    rval = "nvs";
                else
                    rval = window.CNN.omniture.cap_genre.toLowerCase();
            }               
            return rval;
        },
        getCNNBrandingSocial: function() { //prop14,eVar14 - Branding Social
            var rval = "";
            try {
                if (window.CNN && window.CNN.omniture) {
                    if (window.CNN.omniture.fbia === true) {
                        rval = window.CNN.omniture.branding_social;
                    }
                }
            } catch(err) {}
            try {
                if (window.navigator.userAgent && window.navigator.userAgent == "cnn-mobile-app") {
                    return window.navigator.userAgent;
                }
            } catch(err){}
            var hostName = window.location.hostname;
            if (hostName.indexOf("fave.api.cnn.io") != -1 || hostName.indexOf("fave-api.cnn.com") != -1) {
                var pathName = window.location.pathname;
                if (pathName.indexOf("/v1/amp") != -1) {
                    rval = "google amp"; //google amp
                }
                if (pathName.indexOf("/v1/fav") != -1) {
                    rval = "embed"; //embed
                }
            }
            rval = rval.toLowerCase();
            return rval;
        },
        getCNNTrafficPartner: function() { // eVar15 - Traffic Partner
           var rval = "";
           try {
             rval = _satellite.cookie.get("FastAB");
           } catch(err) {}
           return rval;
        },
        getIreportgetMember: function() { //prop17,eVar17 - ireport member
            var irptMember = wminst.Util.getCNNAuthenticated("authid", "displayname", "member", "anonymous", "NonMember", "?");
            if (window.location.host.indexOf("politics") == -1 && window.is_expansion != 0) {
                return irptMember;
            } else {
                return null;
            }
        },
        getCNNPageImpression: function() { //prop18,eVar18 - page impressions
            var rval = window.cnnPSproducts || "";
            var hptcookie = wminst.Util.getCookie("hpt2");
            if (document.referrer.indexOf("cnn.com") > -1) {
                try {
                    if (hptcookie) {
                        rval = hptcookie;
                        if (hptcookie.indexOf("_") == -1) {
                            rval = CNN.Utils.b64Decode(hptcookie);
                        }
                    }
                } catch(e) {}
                //document.cookie = "hpt2=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/;";
            } else {
                if (hptcookie) {
                    document.cookie = "hpt2=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/; domain=.cnn.com;";
                }
            }
            rval = rval.replace(/no-value-set/g, "nvs");
            rval = rval.toLowerCase();
            return rval;
        },
        getCNNVideoOpportunity: function() { //eVar22 - video embed count
          var rval = "0";
          var ttype = "";
          try { rval = window.cnn_metadata.business.cnn.page.video_embed_count; } catch(e) {}
          try { rval = window.CNN.omniture.video_opportunity || "0"; } catch(e) {}
          ttype = wminst.Util.getCNNTemplateType();
          if (typeof ttype !== 'undefined' && ttype.indexOf("adbp:index") > -1) {
            rval = "";
          }
          return rval;
        },
        getCNNPageHeadline: function() { //prop23,eVar23 - page headline
            var rval = "nvs", tt = "";
            try {   
                rval = window.CNN.omniture.headline;
                tt   = window.CNN.omniture.template_type;
            } catch(e) {}
            try {   
                if(typeof window.cnn_d != "undefined" && typeof window.cnn_d.omniture != "undefined" && window.cnn_d.omniture.headline != "undefined"){
                rval = window.cnn_d.omniture.headline;
                tt   = window.cnn_d.omniture.template_type;
                }
            } catch(e) {}
            try {
                if(rval == "no-value-set" || tt == "specials" || tt == "section front" || tt == "index") {return null;}
                rval = rval.toLowerCase();
            } catch(e) {rval = "";}
            return rval;
        },
        getCNNFullPageName: function(pathname,delimiter) {
            var s_pageName = "";
            var templateTypeSmall = "";
            if (!delimiter) delimiter = ":";
            var ttbefore = wminst.Util.getCNNTemplateType("long");
            if (ttbefore) { //default to "other" if template type is not defined
                ttbefore = ttbefore.replace(/adbp./,"");
                templateTypeSmall = wminst.Util.getADBPTranslateTemplateType(ttbefore, "short")
            } else {
                templateTypeSmall = "o";
            }
            var buc_p32 = wminst.Util.getCNNBusinessName() + delimiter + templateTypeSmall;
            var thirdLevelDomain = wminst.Util.getADBPURL("domain", 3);
            var fullDomain = wminst.Util.getADBPURL("domain");
            var lastTwoDomain = /(\.\w+\.\w+)$/.exec(fullDomain);
            if (lastTwoDomain) thirdLevelDomain = fullDomain.replace(lastTwoDomain[0],"");
            //if (!pathname) pathname = _jsmd.plugin.gADBPURL("path");
            if (!pathname) {
                var p = window.location.pathname.toLowerCase();
                var a = p.split('/');
                var l = a.length;
                var r = /^index./;
                pathname = (r.test(a[(l-1)])) ? p.replace(/([^\/]+\.[^\/]+$)/,"") : p;
                r = /([^\/]+\.[^\/]+$)/;
                if (!r.test(pathname)){
                    l = pathname.length;
                    if(pathname.charAt(l-1) !== "/"){pathname = pathname+"/";}
                }
            }
            if (thirdLevelDomain == "") {
                s_pageName = buc_p32 + delimiter + pathname;
            }else{
                s_pageName = buc_p32 + delimiter + thirdLevelDomain + delimiter + pathname;
            }
            return s_pageName;
        },
        getCNNPageName: function(pname) { //pageName,eVar26 - page.name
            var rval = wminst.Util.getCNNFullPageName(pname);
            var ttype = "";
            try {
                if (typeof window.CNN.omniture !== 'undefined' && typeof window.CNN.omniture.template_type !== 'undefined') {
                    ttype = window.CNN.omniture.template_type;
                }
            }catch(e){ttype = "";}
            try {
                if (ttype === "" && typeof window.cnn_d.omniture === 'undefined' && typeof window.cnn_d.omniture.template_type !== 'undefined') {
                    ttype = window.cnn_d.omniture.template_type;
                }
            }catch(e){}
            // www-m.cnn.com = cnn.com; us-m.cnn.com = cnn.com; edition-m.cnn.com = edition.cnn.com
            var arr = rval.split(":");
            if (arr.length == 4) {
                arr[2] = arr[2].replace(/-m$/, "");
                arr[2] = arr[2].replace("www", "");
                arr[2] = arr[2].replace("us", "");
                arr[2] = arr[2].replace(/\.$/, "");
                if (arr[2] === "") arr.splice(2, 1);
            }
            rval = arr.join(":");
            if (window.is_expansion && rval.match(/cnn:o:/)) {
                var pn = {
                    "index": "in",
                    "video": "v",
                    "videos": "v",
                    "blog": "b",
                    "blogs": "b",
                    "game": "g",
                    "games": "g",
                    "interactive": "it",
                    "content": "c",
                    "error": "err",
                    "section": "sf",
                    "section front": "sf",
                    "gallery": "ga",
                    "show": "sh",
                    "shows": "sh",
                    "special": "sp",
                    "specials": "sp",
                    "topic": "t",
                    "profile": "p",
                    "article": "c"
                } [ttype];
                if (pn) {
                    rval = rval.replace("cnn:o:", "cnn:" + pn + ":");
                }
            }
            if (rval && rval.slice(-1) != "/") {
                rval = rval + "/";
            }
            if (rval && rval.match(/h_[a-z0-9]+\/$/)) {
                rval = rval.replace(/h_[a-z0-9]+\/$/, ""); //remove last folder ID
            }
            return rval;
        },
        getCNNBaseURL: function() { //prop26 - Base URL
            var hostname = window.location.hostname;
            var pathname = window.location.pathname;
            pathname = pathname.replace(/([^\/]+\.[^\/]+$)/,"");
            return hostname + pathname;
        },
        getCNNSection: function(position) { //channel/eVar27, prop28/eVar28
            var rval = "";
            try {
                if (window.is_expansion) {
                    for (var i = 0; i <= position; i++) {
                        if (i > 0) {
                            rval += ":";
                        }
                        try {
                            var s1 = window.CNN.omniture.section[i];
                            if ((s1.indexOf(":")) && (s1.indexOf("electoral college map") > -1)) {
                                var c1 = s1.split(':');
                                rval += c1[0];
                                return rval;
                            }
                        } catch (e) {}
                        if (typeof window.CNN != 'undefined' && typeof window.CNN.omniture != 'undefined') {
                            if (i == 1 && !window.CNN.omniture.section[1]) { //add default value "no value set" for subsection (prop28/eVar28)
                                window.CNN.omniture.section[1] = "no value set";
                                try {
                                    if (window.CNN.omniture.friendly_name.toLowerCase() == "ngtv") {
                                        window.CNN.omniture.section[1] = "";
                                    }
                                } catch (e) {}
                            }
                        }
                        if (window.cnn_d && window.cnn_d.omniture && window.cnn_d.omniture.section[i]) {
                            try {
                                rval += window.cnn_d.omniture.section[i] || "";
                            } catch (e) {}
                        } else {
                            try {
                                rval += window.CNN.omniture.section[i] || "";
                            } catch (e) {}
                        }
                    }
                    try {
                        if (typeof window.CNN.omniture !== 'undefined' && window.CNN.omniture.template_type == "list" && position == 0 && rval == "") { //use first path of URL for list pages
                            rval = wminst.Util.gADBPURL("path", 1);
                        }
                    } catch (e) {}
                } else {
                    window.cnn_metadata.section = (typeof window.cnn_metadata.section != "string" ? window.cnn_metadata.section : window.JSON.parse(window.cnn_metadata.section));
                    rval = (window.cnn_metadata.section[position] ? window.cnn_metadata.section[position] : "");
                }
            } catch (e) {}
            return rval;
        },
        getCNNPageFranchise: function() { //prop31,eVar31 - page_franchise
            var rval = "";
            try { rval = cnn_metadata.business.cnn.page.broadcast_franchise || rval; } catch(e) {}
            try { rval = CNN.omniture.cap_show_name || rval; } catch(e) {}
            rval = rval.toLowerCase();
            return rval;
        },
        getCNNTemplateType: function(lookupType) { //prop32,eVar32 - page template_type
            var hostName = window.location.hostname;
            var rval = "";
            if (window.is_expansion) {
                var pfix = "other:";
                if (typeof window.CNN !== 'undefined' && typeof window.CNN.omniture !== 'undefined' && typeof window.CNN.omniture.template_type !== 'undefined' && window.CNN.omniture.template_type.match(/index|video|blog|game|interactive|content|error|section|gallery|show|special|topic|profile|article|calendar|candidate summary|state summary/)) {
                    pfix = "adbp:"
                }
                rval = pfix;
                if (typeof window.CNN !== 'undefined' && typeof window.CNN.omniture !== 'undefined' && typeof window.CNN.omniture.template_type !== 'undefined' && window.CNN.omniture.template_type == 'article') {
                    try {
                        if (typeof window.CNN.contentModel !== 'undefined' && typeof window.CNN.contentModel.analytics !== 'undefined' && typeof window.CNN.contentModel.analytics.pageTop !== 'undefined' && typeof window.CNN.contentModel.analytics.pageTop.type !== 'undefined' && window.CNN.contentModel.analytics.pageTop.type === 'gallery') {
                            rval = "content: gallery";
                        } else if (typeof window.CNN.contentModel !== 'undefined' && typeof window.CNN.contentModel.analytics !== 'undefined' && typeof window.CNN.contentModel.analytics.pageTop !== 'undefined' && typeof window.CNN.contentModel.analytics.pageTop.type !== 'undefined' && (window.CNN.contentModel.analytics.pageTop.type === 'video' || window.CNN.contentModel.analytics.pageTop.type === 'video360')) {
                            if (typeof window.CNN.contentModel !== 'undefined' && window.CNN.contentModel.analytics.isArticleVideoCollection) {
                                rval = "content:video:collection";
                            } else {
                                rval = "content:video:nocollection";
                            }
                        } else if (window.CNN.omniture.cap_content_type !== 'undefined' && window.CNN.omniture.cap_content_type === 'gallery') {
                            rval = "content: gallery";
                        } else {
                            if (window.CNN.omniture.cap_media_type === 'Video') {
                                rval = "content:video";
                            } else {
                                rval = "content: no media";
                            }
                        }   
                    } catch(e){}
                    
                } else if (hostName.indexOf("fave.api.cnn.io") != -1 || hostName.indexOf("fave-api.cnn.com") != -1) {
                    rval = "adbp:content";
                } else if (typeof window.cnn_d !== 'undefined' && typeof window.cnn_d.omniture !== 'undefined') {
                    try {
                        if (window.cnn_d.omniture.section[0] == "cnn-underscored") {
                            rval = "adbp:" + window.cnn_d.omniture.template_type;
                        }
                    } catch (e) {}
                } else {
                    try {
                        rval = window.CNN.omniture.template_type;
                        if (rval && rval.indexOf("other") === -1) {
                            rval = pfix + rval;
                        }
                    } catch (e) {}
                }
            } else {
                var templateTypeCode = "";
                if (typeof CNN != 'undefined' && typeof CNN.omniture != 'undefined' && typeof CNN.omniture.template_type != 'undefined') {
                    templateTypeCode = CNN.omniture.template_type;
                } else if (typeof cnn_metadata != 'undefined') {
                    templateTypeCode = cnn_metadata.template_type;
                } else if (typeof window.cnn_d != 'undefined' && typeof window.cnn_d.omniture != 'undefined' && typeof window.cnn_d.omniture.template_type != 'undefined') {
                    templateTypeCode = window.cnn_d.omniture.template_type;
                }
                var adbpprefix = "adbp:";
                rval = ["o", "other"];
                var lookup = {
                        b: "blog",
                        g: "game",
                        it: "interactive",
                        c: "content",
                        "in": "index",
                        err: "error",
                        e: "ecom",
                        s: "signup",
                        v: "video",
                        sf: "section front",
                        sr: "search results",
                        fm: "forum",
                        o: "other",
                        ir: "ireport",
                        sp: "specials",
                        pm: "perfect market",
                        bf: "blog front",
                        bc: "blog category",
                        t: "topic",
                        w: "weather",
                        el: "election"
                    },
                    lookupRev = {
                        "blog": "b",
                        "game": "g",
                        "interactive": "it",
                        "content": "c",
                        "index": "in",
                        "error": "err",
                        "ecom": "e",
                        "signup": "s",
                        "video": "v",
                        "section front": "sf",
                        "search results": "sr",
                        "forum": "fm",
                        "other": "o",
                        "ireport": "ir",
                        "specials": "sp",
                        "perfect market": "pm",
                        "blog front": "bf",
                        "blog category": "bc",
                        "topic": "t",
                        "weather": "w",
                        "election": "el"
                    };
                if (lookup[templateTypeCode] != null) {
                    rval = [templateTypeCode, lookup[templateTypeCode]];
                }
                if (lookupRev[templateTypeCode] != null) {
                    rval = [lookupRev[templateTypeCode], templateTypeCode];
                }
                var parameters = {
                    c1: 'ireport',
                    c2: 'search results',
                    c3: 'perfect market',
                    c4: 'specials',
                    c5: 'blog front',
                    c6: 'blog category',
                    c7: 'topic',
                    c8: 'weather',
                    c9: 'election'
                }
                for (var p in parameters) {
                    if (templateTypeCode == parameters[p]) {
                        adbpprefix = "other:";
                    }
                }
                rval[1] = adbpprefix + rval[1];
                if (lookupType == "short") {
                    rval = rval[0];
                }
                if (lookupType == "long") {
                    rval = rval[1];
                }
            }
            if(typeof rval == "string") { 
				rval = rval.toLowerCase();
			}
            return rval;
        },
        getCNNContentType: function(defaultVal) { //prop33,eVar33 - content_type
            var tt = "",
                ct = "";
            if (typeof window.cnn_d != 'undefined' && typeof window.cnn_d.omniture != 'undefined' && typeof window.cnn_d.omniture.template_type != 'undefined') {
                tt = window.cnn_d.omniture.template_type;
                ct = "adbp:" + window.cnn_d.omniture.content_type;

            } else {
                if (typeof window.CNN.omniture !== "undefined" && typeof window.CNN.omniture.content_type !== "undefined" && window.CNN.omniture.content_type){
                    ct = window.CNN.omniture.content_type;
                    } else {
                        ct = "adbp:none";
                        }
                if (typeof ct !== 'undefined' && (ct == "none" || ct == "")) {
                    ct = "adbp:none";
                }
                tt = window.CNN.omniture && window.CNN.omniture.template_type;
            }
            var l = {
                "adbp:blog": ["blog.read", "adbp:blog read"],
                "adbp:content": ["article.read", "adbp:article read"],
                "adbp:game": ["game.play", "adbp:game played"],
                "other:ireport": ["other.ireport", "other:ireport"],
                "other:photo wall": ["content.interactive", "other:photo wall"]
            } [tt];
            var m = {
                "adbp:article read": "article.read"
            } [ct];
            if (m !== null) {
                if (typeof ct !== 'undefined' && ct.indexOf("pivit") !== -1) {
                    return tt + ":" + ct;
                } else {
                    return ct;
                }
            }
            if (!l) {
                return defaultVal;
            }
            return l[1];
        },
        getCNNAuthenticated: function(c1, c2, truevalue, falsevalue, neutralvalue, flag) { //prop34,eVar34 - user authenticated
            var rValue = 0;
            if (wminst.Util.getCookie(c1, flag)) {
                rValue++;
            }
            if (wminst.Util.getCookie(c2, flag)) {
                rValue++;
            }
            if (rValue == 0) {
                return falsevalue;
            } else if (rValue == 1) {
                return neutralvalue;
            } else {
                return truevalue;
            }
        },
        getCNNKruxID: function() { // eVar36 - KruxID
            var rval = "";
            try {
                rval = localStorage.kxkuid;
            } catch (err) {}
            return rval;
        },
        getCNNPlatform: function() { //prop37,eVar37 - page platform
            var rval = "";
            if (navigator.userAgent.match(/iPhone/i)) {
                rval = "smartphone";
            } else if (navigator.userAgent.match(/iPad/i)) {
                rval = "tablet";
            } else if (navigator.userAgent.match(/android/i)) {
                if (navigator.userAgent.match(/mobile/i)) {
                    rval = "smartphone";
                } else {
                    rval = "tablet";
                }
            } else {
                rval = "desktop";
            }
            return rval ? rval : "no value set";
        },
        getCNNSearchInternalKeyword: function() { //prop39,eVar39 - search internal keyword
            var rval = "";
            try {
                rval = wminst.Util.getQueryParam("query");
            } catch(e){}
            return rval;
        },
        getLSPostPosition: function() { //eVar45 - Post Position
            var rval = "";
            try {
                if (this.isLiveStoryTemplateType()) {
                    var post_position = window.CNN.omniture.post_position ? window.CNN.omniture.post_position : 1;
                    var total_post = window.CNN.omniture.total_post ? window.CNN.omniture.total_post : 0;
                    rval = post_position + ":" + total_post;
                }   
            } catch(e) {}
            return rval;
        },
        getCNNPostID: function() { //prop43 - Post ID
            var rval = null;
            var pathName = window.location.pathname;
            if(window.CNN && window.CNN.omniture &&  typeof window.CNN.omniture.post_id != 'undefined' && window.CNN.omniture.post_id != "") {
                rval = window.CNN.omniture.post_id;
            } else {
                 try{
                    pathName = pathName.replace(/\/$/, "");
                    var path_array = pathName.split("/");
                    rval = path_array[path_array.length - 1];
                    if(rval.match(/(^h_)[a-z0-9]+$/) === null){
                        rval = null;
                    }
                } catch(e) {}
            }         
            try {
                if (this.isLiveStoryTemplateType()) {
                    // Do Nothing
                } else {
                   rval = "";
                }  
            } catch(e) {}
            return rval;
        },
        getCNNPageVertical: function() { //eVar44 - Page Vertical
            var rval = "";
            try {
                if(window.CNN && window.CNN.contentModel && window.CNN.contentModel.vertical){
                    rval = CNN.contentModel.vertical;
                    rval = rval.toLowerCase();
                }
            } catch(e){}
            return rval;
        },
        getCNNSourceID: function(){ //prop44 - Source ID
            var rval = "";
            try {
                if(typeof window.CNN != 'undefined' && typeof window.CNN.omniture != 'undefined' && window.CNN.omniture.sourceId) {
                        rval = window.CNN.omniture.sourceId;
                    } else if(window.CNN && window.CNN.contentModel && window.CNN.contentModel.sourceId){
                        rval = window.CNN.contentModel.sourceId;
                }
                rval = rval.toLowerCase();
            } catch(e) {}
            return rval;    
        },
        getCNNTransactionID: function() { // prop46,eVar46
            var rval = "";
            try {
                if (typeof window.cnnad_transactionID !== 'undefined') {
                    rval = window.cnnad_transactionID;
                } else if (typeof window.cnnad_getTransactionID === "function") {
                    rval = cnnad_getTransactionID();
                } else {
                    rval = Math.round((new Date()).getTime() / 1000) + "" + Math.floor(Math.random()*9007199254740992);
                }
            } catch (e) {}
            return rval;
        },
        getCNNGUID: function() { // prop47,eVar47
            var rval = "";
            try {
                if (typeof window.turner_getGuid === "function") {
                    rval = turner_getGuid("ug");
                } else {
                    rval =  _satellite.cookie.get("ug");
                }
            } catch (e) {}
            return rval;
        },
        getAppNexusID: function() {
            var rval = "";
            try {
                if (this.isTagConsented("app-nexus-id")) {
                    rval =  _satellite.cookie.get("zwmc");
                }
            } catch (e) {}
            return rval
        },
        getATTID: function() {
            var rval = "";
            try {
                rval = _satellite.cookie.get("firstpartyuid");
                var obj = JSON.parse(rval);
                rval = obj.id;
            } catch (e) {}
            return rval
        },
        getWMID: function(name) {
            var rval = "";
            try {
                if (window.WM) {
                    var obj = window.WM.PSM || window.WM.CDP || {};
                    var fn = obj["get"+name];
                    if (typeof fn === "function") {
                        rval = fn();
                    }
                }
            } catch (e) {}
            return rval;
        },
        setATTWMID: function() {
            try {
                if (s.linkTrackVars.indexOf("eVar195") == -1) {
                    s.linkTrackVars += ",eVar195,eVar196,eVar197,eVar198,eVar199";
                }
                s.eVar195 = this.getAppNexusID();
                s.eVar196 = this.getATTID();
                s.eVar197 = this.getWMID("WMUKID");
                s.eVar198 = this.getWMID("WMHHID");
                s.eVar199 = this.getWMID("WMINID");
            } catch (e) {}
        },
        getCNNTechStack: function() { //eVar48 - Site Tech Stack
            var dataLayer = (window.CNN || {}).contentModel || {};
            return (dataLayer.techStack || "").toLowerCase();
        },
        getCNNCMSId: function() { //eVar49 - CMS ID
            var rval = "";
            try {
                if(window.CNN && window.CNN.contentModel && window.CNN.contentModel.cmsId){
                    rval = CNN.contentModel.cmsId;
                }
            } catch(e){}
            return rval;
        },
        getCNNPreviousPageName: function(){ //prop49,eVar49 - Previous PageName
            var rval = "";
            try {
                if(this.isTagConsented('adobe')) {
                    var pName = window.document.referrer;
                    var prevP = s.getPreviousValue(wminst.Util.getCNNPageName(),"cnprevpage_pn");
                    if (prevP && typeof pName != "undefined" && pName != "" && pName.indexOf(".cnn.com") != -1) {
                        return prevP;
                    }
                }
            } catch(e) {return rval;}
            return rval;
        },
        getCNNPostTitle: function() { //prop50 - Post Title
            var rval = "";
            try{
                if(window.CNN && window.CNN.omniture && window.CNN.omniture.post_title) {
                    rval = window.CNN.omniture.post_title;
                } else { 
                    rval = document.title;
                }
            } catch(e) { rval = document.title; }
            rval = rval.toLowerCase();
            try {
                var dom_obj = $x("//script[@type='application/ld+json']");
                var post_obj = JSON.parse(rval[rval.length - 1]).innerHTML;
                if(post_obj && post_obj.headline){
                     rval = post_obj.headline;
                } 
            } catch(e) {}
            try {
                if (this.isLiveStoryTemplateType()) {
                   // Do Nothing
                } else {
                   rval = "";
                }  
            } catch(e) {}
            if(rval !== "") {
                rval = rval.replace(/\([0-9]+\)/, "").trim();
            }
            return rval;
        },
        getCNNBreakingNewsHP: function(ptt, chnl) {
            var rval = "";
            var tt = "";
            try {
                if (ptt.indexOf(":") != -1) {
                    if (ptt.indexOf("adbp") != -1) {
                        ptt = ptt.split(":");
                        tt = ptt[1];
                    } else {
                        ptt = ptt.split(":");
                        tt = ptt[0];
                    }
                } else {
                    tt = ptt;
                }
                var abr = {
                    "index": "in",
                    "video": "v",
                    "videos": "v",
                    "blog": "b",
                    "blogs": "b",
                    "game": "g",
                    "games": "g",
                    "interactive": "it",
                    "content": "c",
                    "error": "err",
                    "section": "sf",
                    "section front": "sf",
                    "gallery": "ga",
                    "show": "sh",
                    "shows": "sh",
                    "special": "sp",
                    "specials": "sp",
                    "topic": "t",
                    "profile": "p",
                    "article": "c"
                } [tt];
                if (chnl && (chnl == "homepage" || chnl == "cnn homepage")) {
                    chnl = "index";
                }
                if (tt) {
                    rval = "breaking:" + chnl + ":" + abr + ":";
                }
                return rval;
            } catch (e) {}
        },
        getCNNOrientation: function() { //prop56,eVar56 - page orientation
            var rval = "no value set";
            try {
                var x = 0;
                if (self.innerHeight) {
                    x = self.innerWidth;
                } else if (document.documentElement && document.documentElement.clientHeight) {
                    x = document.documentElement.clientWidth;
                } else if (document.body) {
                    x = document.body.clientWidth;
                }
                var y = 0;
                if (self.innerHeight) {
                    y = self.innerHeight;
                } else if (document.documentElement && document.documentElement.clientHeight) {
                    y = document.documentElement.clientHeight;
                } else if (document.body) {
                    y = document.body.clientHeight;
                }
                rval = (y > x) ? "portrait" : "landscape";
            } catch (e) {}
            return rval;
        },
        getCNNMVPD: function() { //prop57,eVar57 - MVPD
            try {
                var mvpd_store = wminst.Util.getCookie("CNNmvpd");
                if (typeof mvpd_store !== "undefined" && mvpd_store !== "nvs" && mvpd_store !== "") {
                    if (mvpd_store !== null && typeof CNN.omniture.mvpd === "string") {
                        document.cookie = "CNNmvpd=" + CNN.omniture.mvpd + "; domain= .cnn.com ;";
                        mvpd_store = wminst.Util.getCookie("CNNmvpd");
                        return mvpd_store;
                    } else if (typeof mvpd_store === "string" && mvpd_store != "") {
                        if (typeof CNN.omniture.mvpd === "string") {
                            document.cookie = "CNNmvpd=" + CNN.omniture.mvpd + ";  domain= .cnn.com ;";
                            mvpd_store = wminst.Util.getCookie("CNNmvpd");
                            return mvpd_store;
                        } else {
                            
                            return mvpd_store;
                        }
                    } else if (mvpd_store === null && typeof CNN.omniture.mvpd === "string") {
                        document.cookie = "CNNmvpd=" + CNN.omniture.mvpd + ";  domain= .cnn.com ;";
                        mvpd_store = wminst.Util.getCookie("CNNmvpd");
                        return mvpd_store;
                    } else {
                        return "no mvpd set";
                    }
                } else {
                    return "no mvpd set";
                }
            } catch (err) {return "no mvpd set";}
        },
        getCNNAdobeID: function() { //prop59,eVar59 - Adobe Harsh ID
            try {
                var adobe_hash_id_store = _satellite.cookie.get("adobe_hash_id");
                if (typeof adobe_hash_id_store !== "undefined" && adobe_hash_id_store !== "nvs" && adobe_hash_id_store !== "") {
                    if (adobe_hash_id_store !== null && typeof CNN.omniture.adobe_hash_id === "string") {
                        document.cookie = "adobe_hash_id=" + CNN.omniture.adobe_hash_id + "; domain= .cnn.com;";
                        adobe_hash_id_store = _satellite.cookie.get("adobe_hash_id");
                        return adobe_hash_id_store;
                    } else {
                        return "no mvpd set";
                    }
                } else {
                    return "no mvpd set";
                }
            } catch (err) {}
        },
        getCNNPlayerState: function(video) { //eVar67 player State
            var screenState = video.screen_state || "nvs";
            var screenPosition = video.screen_position || "nvs";
            var audioState = video.audio_state || "nvs";
            var playerState = "";
            try {
                if (screenState == "nvs" && CNN && CNN.omniture && CNN.omniture.screen_state) {
                    screenState = CNN.omniture.screen_state;
                }
                if (audioState == "nvs") {
                    if (video.muted === true) {
                        audioState = "muted";
                    } else if (video.muted === false) {
                        audioState = "audio on";
                    }
                }
                playerState = screenState + "|" + audioState + "|" + screenPosition;
                playerState = playerState.toLowerCase();
            } catch (e) {}
            return playerState;
        },
        getCNNVisitorID: function(id) { //eVar73 - page visitorId
            var rval = "";
            try {
                rval = _satellite.cookie.get(id);
                rval = rval.replace(/\[(.+?)\]/g, "");
                rval = rval.split("|")[1];
                rval = rval.toLowerCase();
            } catch (err) {}
            return rval;
        },
        getCNNHierachy: function() { // hier1 - Hierachy
            var rval = "";
          /*  try {
                var bUnit = wminst.Util.getSiteSpecificSettings(1);
                var channel = wminst.Util.getCNNSection(0);
                var domain = wminst.Util.getADBPURL("domain");
                var section2 = wminst.Util.getCNNSection(1);
                rval = "news|cnn|" + bUnit + "|" + domain + "|" + channel + "|" + section2; 
            } catch(e){} */
            return rval;
        },
        getCNNUserAuthState: function() { //prop75,eVar75 - User Authentication State
            try {
                var user_auth_state_store = localStorage.getItem("user_auth_state");
                if (user_auth_state_store !== null && typeof window.CNN.omniture.user_auth_state === "string") {
                    localStorage.setItem("user_auth_state",window.CNN.omniture.user_auth_state);
                    user_auth_state_store = localStorage.getItem("user_auth_state");
                    return user_auth_state_store;
                } else if (typeof user_auth_state_store === "string") {
                    if (typeof window.CNN.omniture.user_auth_state === "string") {
                        
                        localStorage.setItem("user_auth_state",window.CNN.omniture.user_auth_state);
                        user_auth_state_store = localStorage.getItem("user_auth_state");
                        return user_auth_state_store;
                    } else {
                        
                        return user_auth_state_store;
                    }
                } else if (user_auth_state_store === null && typeof window.CNN.omniture.user_auth_state === "string") {
                    localStorage.setItem("user_auth_state",window.CNN.omniture.user_auth_state);
                    user_auth_state_store = localStorage.getItem("user_auth_state");
                    return user_auth_state_store;
                } else {
                    return "nvs";
                }
            } catch (err) {return "";}
        },
        getCNNUIEngagement: function() { //prop64 - UI Engagement
            var rval = "";
            try {
                rval = window.CNN.omniture.friendly_name.toLowerCase();
            } catch(e) {}
            if (rval != "ngtv") { rval = "cnn news"; }
            try { 
                if(typeof window.cnn_metadata.friendly_name != 'undefined') {
                    rval = window.cnn_metadata.friendly_name;
                }
            } catch(e) {}
            return rval;
        },
        getCNNTopicAvailability: function() {
            var topic_pattern = new RegExp(/^[0-9a-z,]+$/);
            try {
                var rval = wminst.Util.getCNNTopic();
                if(rval == ""){
                    return "no topics";
                } else if(topic_pattern.test(rval)) {
                    return "topics available";
                } else { 
                    return "api request failure";
                }
            } catch(e) {}
        },
        getCNNTopic: function() {
            var rval = "";
            var cap_array = [];
            try {
                if(CNN && CNN.cep_topics && CNN.cep_topics.cep_brsf && CNN.cep_topics.cep_iabt && CNN.cep_topics.cep_sent && CNN.cep_topics.cep_tags) {
                    cap_array = cap_array.concat(CNN.cep_topics.cep_brsf, CNN.cep_topics.cep_iabt, CNN.cep_topics.cep_sent, CNN.cep_topics.cep_tags);
                    rval = cap_array.toString();
                } else {
                    rval = window.CNN.omniture.cap_topic;
                }
                if(typeof rval == "undefined" || rval === "no-value-set" ||  rval == "" ) {rval = "";}
            } catch(e) {}
            return rval.toLowerCase();
        },
        getCEPTopisForVideo: function(data) {
            var rval = "";
            try {
                if(typeof data.cepTopics == "object") {
                    rval = Object.keys(data.cepTopics).toString();
                }
                rval = rval.toLowerCase();
            } catch (e) {}
            return rval;
        },
      	getCNNSiteSectionLevel3: function(val) { //prop51 - Site section level 3 for politics
			var rval = "";
			try {
				rval = wminst.Util.getCNNSection(1);
				if(typeof val != 'undefined') {
					rval += ":" + val;
				} else if(CNN && CNN.omniture && CNN.omniture.section && typeof CNN.omniture.section[2] != 'undefined') {
					rval += ":" + CNN.omniture.section[2];
				}
			} catch (e) {}
			return rval;
		},
		getCNNInteractiveState: function(data) { //eVar50 - Interactive State for politics
			var rval = "";
            if(typeof data == 'undefined' && window.location.hash === "#my_election") {
				rval = "election center:my election:panel open";
				return rval;
           }
           if (typeof data == "object" && (typeof data.tab != 'undefined' || typeof data.map_state != 'undefined')) {
        	    var tab = data.tab || "nvs";
        		var map_state = data.map_state || "nvs";
        		if(!wminst.Util.isPoliticsExplorer()) {
        			rval = "election center:" + tab + ":" + map_state;
        		} else {
        			var year = data.year || "nvs";
        			var comparison_layer = data.comparison_layer || "nvs";
        			var e_val = data.election || "nvs";
        			rval = tab + ":" + year + ":" + e_val + ":" + comparison_layer + ":" + map_state;
        		}
                rval = rval.toLowerCase();
            }
            return rval
		},
        getSiteSpecificSettings: function(type, section) {
            var hostName = window.location.hostname;
            var port = window.location.port;
            var setting;
            var sites = {
                "cnn": ["cnn-adbp-domestic", "cnn domestic", "cnn", "metrics.cnn.com", "smetrics.cnn.com", "us-100120", "b01", "00001", "8587204"],
                "cnndev": ["cnn-adbp-domestic-dev", "cnn domestic", "cnn", "metrics.cnn.com", "smetrics.cnn.com", "us-100120", "b01", "00001", "8587204"],
                "cnnintl": ["cnn-adbp-intl", "cnn international", "cnn", "metrics.cnn.com", "smetrics.cnn.com", "us-100120", "b01", "00002", "8587278"],
                "cnnintldev": ["cnn-adbp-intl-dev", "cnn international", "cnn", "metrics.cnn.com", "smetrics.cnn.com", "us-100120", "b01", "00002", "8587278"],
                "ireport": ["cnnireport-adbp", "cnn ireport", "cnnireport", "metrics.cnn.com", "smetrics.cnn.com", "us-702210", "c01", "00001", "3002212"],
                "ireportdev": ["cnnireport-adbp-dev", "cnn ireport", "cnnireport", "metrics.cnn.com", "smetrics.cnn.com", "us-702210", "c01", "00001", "3002212"]
            }

            var c4 = {
                val1: ["cnn homepage", "8587211", "8587278"],
                val2: ["crime", "8587220"],
                val3: ["us", "8587228"],
                val4: ["world", "8587235"],
                val5: ["entertainment", "8587242"],
                val6: ["politics", "8587248"],
                val7: ["health", "8587254"],
                val8: ["tech", "8587261"],
                val9: ["living", "8587266"],
                val10: ["opinion", "8587272"],
                val11: ["watch cnn", "8587204"]
            }

            if (section && section != "") {
                var x = 0;
                for (x in c4) {
                    if (c4[x][0] == section) {
                        setting = c4[x][1];
                        if (section == "cnn homepage") {
                            if (hostName.indexOf("edition.cnn.com") != -1) {
                                setting = c4[x][2];
                            } else if (hostName.indexOf("jcmsdev8.cnn.com") != -1 || hostName.indexOf("jcmsref.cnn.com") != -1 || hostName.indexOf("cnnpreview.cnn.com") != -1 || hostName.indexOf("ref.cnn.com") != -1 || hostName.indexOf("preview.cnn.com") != -1) {
                                if (port.indexOf("94") != -1 || hostName.indexOf("edition") != -1) {
                                    setting = c4[x][2];
                                }
                            }
                        }
                        break;
                    }
                }
            } else {
                if (hostName.indexOf("ireportqa.cnn.com") != -1) {
                    setting = sites.ireportdev[type];
                } else if (hostName.indexOf("jcmsdev8.cnn.com") != -1 || hostName.indexOf("jcmsref.cnn.com") != -1 || hostName.indexOf("cnnpreview.cnn.com") != -1 || hostName.indexOf("ref.cnn.com") != -1 || hostName.indexOf("preview.cnn.com") != -1 || hostName.indexOf("dev.cnn.com") != -1 || hostName.indexOf("stage.cnngo.com") != -1 || hostName.indexOf("travel.cnngo.com") != -1 || hostName.indexOf("edition.stage.next.cnn.com") != -1 || hostName.indexOf("cnnpreview.turner.com") != -1 || hostName.indexOf("dev.cnnv2.com") != -1 || hostName.indexOf("ref.cnnv2.com") != -1 || hostName.match(/^(dev|qa|stage).(www|us|edition)-m.cnn.com/) || hostName.indexOf("edition.enable.next.cnn.com") != -1 || hostName.indexOf("terra.next.cnn.com") != -1 || hostName.indexOf("politics.next.cnn.com") !== -1 || hostName.indexOf("edition.politics.next.cnn.com") !== -1) {
                    if (port.indexOf("94") != -1 || hostName.indexOf("edition") != -1 || hostName.indexOf("cnnespanol") != -1 || hostName.indexOf("stage.cnngo.com") != -1 || hostName.indexOf("travel.cnngo.com") != -1) {
                        setting = sites.cnnintldev[type];
                    } else {
                        setting = sites.cnndev[type];
                    }
                } else if (hostName.indexOf("qai.cnn.com") != -1) {
                    setting = sites.cnndev[type];
                } else if (hostName.indexOf("cnn.staging.perfectmarket.com") != -1 || hostName.indexOf("cnn.staging2.perfectmarket.com") != -1 || hostName.indexOf("beta-cronkite.cnnlabs.com") != -1 || hostName.indexOf("dev-audioplayer-cnn.s3.amazonaws.com") != -1) {
                    setting = sites.cnndev[type];
                } else if (hostName.indexOf("darwin-dev.hope.ui") != -1 || hostName.indexOf("dev-facts-first.cnnlabs.com")!= -1) {
                    setting = sites.cnndev[type];
                } else if (hostName.indexOf("int-facts-first.cnnlabs.com") != -1) {
                    setting = sites.cnnintldev[type];
                } else if (hostName.indexOf("ireport.cnn.com") != -1) {
                    setting = sites.ireport[type];
                } else if (hostName.indexOf("edition.cnn.com") != -1 || hostName.indexOf("cnnespanol.cnn.com") != -1 || hostName.indexOf("backstory.blogs.cnn.com") != -1 || hostName.indexOf("inthefield.blogs.cnn.com") != -1 || hostName.indexOf("securityfiles.blogs.cnn.com") != -1 || hostName.indexOf("thecnnfreedomproject.blogs.cnn.com") != -1 || hostName.indexOf("ukelection.blogs.cnn.com") != -1 || hostName.indexOf("amanpour.blogs.cnn.com") != -1 || hostName.indexOf("screeningroom.blogs.cnn.com") != -1 || hostName.indexOf("internationaldesk.blogs.cnn.com") != -1 || hostName.indexOf("newsstream.blogs.cnn.com") != -1 || hostName.indexOf("prism.blogs.cnn.com") != -1 || hostName.indexOf("thebrief.blogs.cnn.com") != -1 || hostName.indexOf("insidethemiddleeast.blogs.cnn.com") != -1 || hostName.indexOf("connecttheworld.blogs.cnn.com") != -1 || hostName.indexOf("business.blogs.cnn.com") != -1 || hostName.indexOf("questmeansbusiness.blogs.cnn.com") != -1 || hostName.indexOf("goalmouth.blogs.cnn.com") != -1 || hostName.indexOf("olympics.blogs.cnn.com") != -1 || hostName.indexOf("worldsport.blogs.cnn.com") != -1 || hostName.indexOf("bodareal.blogs.cnn.com") != -1 || hostName.indexOf("travel.cnn.com") != -1 || hostName.indexOf("footballclub.cnn.com") != -1 || hostName.indexOf("edition.cnnv2.com") != -1 || hostName.indexOf("edition-m.cnn.com") != -1) {
                    setting = sites.cnnintl[type];
                } else if (hostName.indexOf("cnn.com") != -1 || hostName.indexOf("cnnv2.com") != -1) {
                    setting = sites.cnn[type];
                } else if (hostName.indexOf("fave.api.cnn.io") != -1 || hostName.indexOf("fave-api.cnn.com") != -1) {
                    setting = sites.cnn[type];
                } else if (hostName.indexOf("style.staging.cnn.io") != -1) {
                    setting = sites.cnndev[type];
                } else {
                    //default, if any case failed
                    setting = sites.cnn[type];
                }
            }
            try {
                if (window.CNNIntlVideo) {
                    setting = sites.cnnintl[type];
                }
            } catch (e) {}
            return setting;
        },
        getJObj: function(objectRef, attribute) {
            objectRef = (typeof objectRef == "string" ? window[objectRef] : objectRef);
            var rval = (objectRef != null && attribute != null && attribute.indexOf(".") == -1 && attribute.indexOf("[") == -1 ? objectRef[attribute] : objectRef);
            if (rval === objectRef && (typeof attribute !== 'undefined' || attribute != null)) {
                var attribs = attribute.split("."),
                    len = attribs.length,
                    reArray = /([^\[]+)\[(\d+)\]/,
                    t, t2;
                rval = objectRef;
                for (var i = 0; i < len; i++) {
                    t = attribs[i];
                    if ((t2 = reArray.exec(t)) != null) {
                        rval = rval[t2[1]][parseInt(t2[2])];
                    } else rval = rval[t];
                }
            }
            return rval;
        },
        getADBPContentType: function(defaultVal) {
            var tt = wminst.Util.getCNNTemplateType("long") || "";
            var ct = wminst.Util.getCNNContentType() | "";
            var rObj = {};
            var l = {
                "adbp:blog": ["event38", "adbp:blog read"],
                "adbp:content": ["event39", "adbp:article read"]
            } [tt];
            var m = {
                "adbp:article read": "event39"
            } [ct];
            if (m != null) {
                rObj.events = m;
                rObj.content_type = ct;
                return rObj;
            }
            if (!l) {
                rObj.events = "";
                rObj.ct = defaultVal;
                return rObj;
            }
            rObj.events = l[0];
            rObj.ct = l[1];
            return rObj;
        },
        getADBPURL: function(type, lvl) {
            var hostname = window.location.hostname.toLowerCase();
            var pathname = window.location.pathname.toLowerCase();
            var path_array = "";
            pathname = pathname.replace(/([^\/]+\.[^\/]+$)/, "");

            var rval;
            switch (type) {
                case "domain":
                    hostname = hostname.replace("www.", "");
                    if (lvl == parseFloat(lvl)) {
                        var domain_array = hostname.split(".");
                        var currentPointer = domain_array.length - lvl;
                        var currentDomainLevel = (currentPointer >= 0 ? domain_array[currentPointer] : "");
                        rval = currentDomainLevel;
                    } else {
                        rval = hostname;
                    }
                    break;
                case "path":
                    var pathname2 = pathname.substring(1);
                    path_array = pathname2.split("/");
                    if (lvl == parseFloat(lvl) && lvl >= 1) {
                        var currentPathname = (path_array.length >= lvl ? path_array[lvl - 1] : "");
                        rval = currentPathname;
                    } else {
                        rval = pathname;
                    }
                    break;
                case "hier":
                    hostname = hostname.replace("www.", "");
                    path_array = pathname.substring(1).split("/");
                    var h1 = hostname + "/" + path_array[0];
                    var h2 = h1;
                    if (path_array[1]) h2 = h2 + "/" + path_array[1];
                    rval = [h1, h2];
                    break;
                default:
                    rval = hostname + pathname;
            }
            return rval;
        },
        getADBPPageName: function(pathname, delimiter) {
            var s_pageName = "",
                templateTypeSmall = "";
            if (!delimiter) delimiter = ":";
            var ttbefore = wminst.Util.getCNNTemplateType("long");
            if (ttbefore) { //default to "other" if template type is not defined
                ttbefore = ttbefore.replace(/adbp./, "");
                templateTypeSmall = wminst.Util.getADBPTranslateTemplateType(ttbefore, "short");
            } else {
                templateTypeSmall = "o";
            }
            var buc_p32 = wminst.Util.getCNNBusinessName() + delimiter + templateTypeSmall;
            var thirdLevelDomain = wminst.Util.getADBPURL("domain", 3);
            var fullDomain = wminst.Util.getADBPURL("domain");
            var lastTwoDomain = /(\.\w+\.\w+)$/.exec(fullDomain);
            if (lastTwoDomain) thirdLevelDomain = fullDomain.replace(lastTwoDomain[0], "");
            if (!pathname) {
                var p = window.location.pathname.toLowerCase();
                var a = p.split('/');
                var l = a.length;
                var r = /^index./;
                pathname = (r.test(a[(l - 1)])) ? p.replace(/([^\/]+\.[^\/]+$)/, "") : p;
                r = /([^\/]+\.[^\/]+$)/;
                if (!r.test(pathname)) {
                    l = pathname.length;
                    if (pathname.charAt(l - 1) !== "/") {
                        pathname = pathname + "/";
                    }
                }
            }
            var pageNameLen, r_len;
            if (thirdLevelDomain == "") {
                pageNameLen = buc_p32.length + 1 + pathname.length;
                if (pageNameLen <= 100) {
                    s_pageName = buc_p32 + delimiter + pathname;
                } else {
                    r_len = pageNameLen - 100;
                    s_pageName = buc_p32 + delimiter + pathname.substring(r_len);
                }
            } else {
                pageNameLen = buc_p32.length + 1 + thirdLevelDomain.length + 1 + pathname.length;
                if (pageNameLen <= 100) {
                    s_pageName = buc_p32 + delimiter + thirdLevelDomain + delimiter + pathname;
                } else {
                    if (thirdLevelDomain.length <= 5) {
                        r_len = pageNameLen - 100;
                        s_pageName = buc_p32 + delimiter + thirdLevelDomain + delimiter + pathname.substring(r_len);
                    } else {
                        thirdLevelDomain = thirdLevelDomain.substring(0, 5);
                        pageNameLen = buc_p32.length + 1 + thirdLevelDomain.length + 1 + pathname.length;
                        if (pageNameLen <= 100) {
                            s_pageName = buc_p32 + delimiter + thirdLevelDomain + delimiter + pathname;
                        } else {
                            r_len = pageNameLen - 100;
                            s_pageName = buc_p32 + delimiter + thirdLevelDomain + delimiter + pathname.substring(r_len);
                        }
                    }
                }
            }
            return s_pageName;
        },
        getCNNVideoSequence : function()
        {
          return "1";  
        },
        getCNNVertical : function()
        {
          var rval = "";
            try {
                if (window.CNN.contentModel.vertical && window.CNN.contentModel.vertical !== "") {
                    rval = window.CNN.contentModel.vertical;
                }
            } catch(e){}
            return rval;    
        },
        getADBPTranslateTemplateType: function(templateTypeCode, lookupType) {
            var adbpprefix = "adbp:",
                rval = ["o", "other"];
            var lookup = {
                    b: "blog",
                    g: "game",
                    it: "interactive",
                    c: "content",
                    "in": "index",
                    err: "error",
                    e: "ecom",
                    s: "signup",
                    v: "video",
                    sf: "section front",
                    o: "other"
                },
                lookupRev = {
                    "blog": "b",
                    "game": "g",
                    "interactive": "it",
                    "content": "c",
                    "index": "in",
                    "error": "err",
                    "ecom": "e",
                    "signup": "s",
                    "video": "v",
                    "section front": "sf",
                    "other": "o"
                };
            if (lookup[templateTypeCode] != null) {
                rval = [templateTypeCode, lookup[templateTypeCode]];
            }
            if (lookupRev[templateTypeCode] != null) {
                rval = [lookupRev[templateTypeCode], templateTypeCode];
            }
            rval[1] = adbpprefix + rval[1];
            if (lookupType == "short") {
                rval = rval[0];
            }
            if (lookupType == "long") {
                rval = rval[1];
            }
            return rval;
        },
        gCNNUserAuthState: function() {
            var userAuthObj = { 
                        user_login_status:"",
                        user_account_status: "",
                        user_registered_status: ""};
            try {
                var userLoginState =  _satellite.cookie.get("_cnn_at") ||  _satellite.cookie.get("_cnn_at_edition");// ===> User Logged In
                if (userLoginState && userLoginState !== "") {
                    userAuthObj.user_login_status = "logged in";
                    userAuthObj.user_registered_status = "registered";
                    var userAuthState = window.CNN.Utils.b64Decode(userLoginState);
                    if(userAuthState && userAuthState.indexOf("cnn.authn") > -1) {              
                        userAuthObj.user_account_status = "account verified";
                    } else {                
                        userAuthObj.user_account_status = "account not verified";
                    }
                } else {
                    userAuthObj.user_registered_status = "anonymous";
                    userAuthObj.user_login_status = "not logged in";
                    userAuthObj.user_account_status = "account not verified";
                }
        
            
            } catch(e){}
            return userAuthObj;
        },
        getUserRegisteredStatus: function(){ //prop51,eVar51
            var rval = "";
            try {
                rval = wminst.Util.gCNNUserAuthState();
                return rval.user_registered_status;
            }catch(e){}
            return rval;
        },
        getUserAccountStatus: function(){ //prop74,eVar74
            var rval = "";
            try {
                rval = wminst.Util.gCNNUserAuthState();
                return rval.user_account_status;
            }catch(e){}
            return rval;
        },
        getUserLoginStatus: function(){ //eVar89
            var rval = "";
            try {
                rval = wminst.Util.gCNNUserAuthState();
                return rval.user_login_status;
            }catch(e){}
            return rval;
        },
        getCNNSavedRaces: function() {
		    var rval = "";
			if(typeof CNN != 'undefined' && typeof CNN.saved_races == "number") {
				rval = "election center:save races:" + CNN.saved_races;
			} else {
				if(wminst.Util.getCNNCapContentType()) {
					rval = "D=c13";
				}
			}
			return rval;
		},
        getCNNExploreIndentify: function(data) { //eVar79 for Politics Explorer
			var rval = "cnn login not required";
			if((data.interaction_type == "year race" && data.racePremiumContent) || (data.interaction_type == "add layer" && data.overlayPremiumContent)) {
				rval = "cnn login required";
			}
			return rval;
		}
    }
}();
wminst.Util.loadCustomVariables();
});
_satellite["_runScript2"](function(event, target, Promise) {
// JSMD Adapter to provide backward compatibility
window._jsmd = window._jsmd || {
  init: function() {
    this.mdata = {
      business: {
        cnn: {
          page: {
            author: wminst.Util.getCNNAuthor(),
            branding_content_partner: wminst.Util.getCNNBrandingPartner(),
            section: [wminst.Util.getCNNSection(0), wminst.Util.getCNNSection(1)]
          }
        }
      }
    };
    return this;
  },
  send: function() {
  },
  trackMetrics: function(action, data, map) {
    setTimeout(function() {
      console.log("jsmd adapter trackMetrics action =" + action + " window.trackMetrics = " + typeof window.trackMetrics);
      window.trackMetrics(action, data);
    }, 100);
  },
  plugin: {
    gQuery: function(name) {
      return wminst.Util.getQueryParam(name);
    },
    gCNNVideoCollection: function() {
      return wminst.getCNNMediaCollection();
    }
  }
};
});
_satellite["_runScript3"](function(event, target, Promise) {
/*! A simple PubSub in JavaScript - v1.0.0 - 2014-01-12
* https://github.com/bdadam/PubSub
* The MIT License (MIT)
* Copyright (c) 2013 Adam Beres-Deak */
!function(){"use strict";function a(a){if("[object String]"!==Object.prototype.toString.call(a))throw new TypeError("Event is not a string.")}function b(a){if("function"!=typeof a)throw new TypeError("Handler is not a function")}var c={},d={};d.publish=d.pub=function(b){if(a(b),c[b])for(var d={event:b,args:Array.prototype.slice.call(arguments,1)},e=0,f=c[b].length;f>e;e++)c[b][e].apply(d,d.args)},d.subscribe=d.sub=function(d,e){a(d),b(e),(c[d]=c[d]||[]).push(e)},d.unsubscribe=d.unsub=function(){var d,e,f,g,h=Array.prototype.slice.call(arguments);if(h.length>=2){if(d=h[0],e=h[1],a(d),b(e),!c[d])return;for(f=0,g=c[d].length;g>f;f++)c[d][f]===e&&c[d].splice(f,1)}else{e=h[0],b(e);for(d in c)for(f=0,g=c[d].length;g>f;f++)c[d][f]===e&&c[d].splice(f,1)}},"function"==typeof define&&define.amd?define(function(){return d}):"object"==typeof module&&module.exports?module.exports=d:window.PubSub=d}();

window.setJSMDVideoEvent = function(event, data) {
	if (event == "cnnvideo-pause" && !data.paused) {
		event = "cnnvideo-resume";
	}
	window.jsmdVideoEvent = {
		name: event,
		time: +(new Date())
	};
};

window.trackAudioProgress = function(audInfo) {
    try {
        trackMetrics({
            type: "audio-progress",
            data: audInfo});
    } catch (e) {}
};

window.trackVideoProgress = function(vidInfo) {
	try {
		setJSMDVideoEvent("cnnvideo-progress", vidInfo);
		trackMetrics({
			type: "cnnvideo-progress",
			data: { video: vidInfo }
		});
	} catch(e){}
};

window.trackMetrics = function(action, data) {
  var realaction = action,
    realdata = data;
  if (typeof(action) == "object") {
    if (action.type != null) {
      realaction = action.type;
    }
    if (action.action != null) {
      realaction = action.action;
    }
    if (action.data != null) {
      realdata = action.data;
    }
  }
  if (typeof(realdata) == "object") {
    if (realdata.data != null) {
      realdata = realdata.data;
    }
  }
 var counter = 0;
  (function poll() {
    setTimeout(function() {
      if (wminst.subscribersReady || counter >= 10) {
        wminst.Util.log("trackMetrics subscribersReady =", wminst.subscribersReady, "counter =", counter, "action =", realaction, "data =", realdata);
        PubSub.publish(realaction, realdata);
      } else {
        counter++;
        poll();
      }
    }, 100);
  })();
 
 //Handling ComScore Events here
  try {
    if(realaction == "cnnvideo-preroll" || realaction == "cnnvideo-adcreative-start"){
	 	 	PubSub.publish("cs_video-preroll", realdata.video);
  	} else if(realaction == "cnnvideo-adcomplete" || realaction == "cnnvideo-midroll-complete"){
	  	PubSub.publish("cs_ad-complete", realdata.video);
	  } else if(realaction == "cnnvideo-start" || realaction == "cnnvideo-autostart" || realaction == "cnnvideo-live" || realaction == "cnnvideo-autosegment" || realaction == "cnnvideo-autoepisode" || realaction == "cnnvideo-episode"){
	 		 PubSub.publish("cs_video-play", realdata.video);
  	} else if(realaction == "cnnvideo-pause" &&  typeof realdata.video.paused !== 'undefined' && realdata.video.paused == true){
	  	PubSub.publish("cs_video-pause", realdata.video);
  	} else if(realaction == "cnnvideo-pause" &&  typeof realdata.video.paused !== 'undefined' && realdata.video.paused == false){
	  	PubSub.publish("cs_video-resume", realdata.video);
  	} else if(realaction == "cnnvideo-complete"){
	  	PubSub.publish("cs_video-complete", realdata.video);
 	  }
 } catch(e){}

};

window.trackVideoEvent = function(data, event, playerid){
	try {
		if (event !== "cnnvideo-progress") {
			setJSMDVideoEvent(event, data);
			var currVidObj = data;
			currVidObj.playerid = playerid;
			trackMetrics({
				type: event,
				data: {
					video : currVidObj
				}
			});
		}
	} catch(e){}
};

window.sendInteractionEvent = function(event, data){
	try {
		trackMetrics({
			type: event,
			data: {
				interaction: data
			}
		});
	} catch(e){}
};

window.sendHP10Interaction = function (data){
	sendInteractionEvent("hp10-interaction", "10minpreview:"+data);
};

window.sendGameInteraction = function(event,info){
	try {
		trackMetrics({
			type: event,
			data: {
				value: info
			}
		});
	} catch(e){}
};

window.sendVideoClick = function(info, event){
	try {
		trackMetrics({
			type: event,
			data: {
				value: info
			}
		});
	} catch(e){}
};

window.sendVideoEvent = function(data, event, playerid){
	try {
		var currVidObj = window.JSON.parse(data);
		currVidObj.playerid = playerid;
		trackMetrics({
			type: event,
			data: {
				video : currVidObj
			}
		});
	} catch(e){}
};

window.sendVideo2Event = function(data, event, playerid){
	try {
		var currVidObj = data;
		currVidObj.playerid = playerid;
		trackMetrics({
			type: event,
			data: {
				video : currVidObj
			}
		});
	} catch(e){}
};

window.sendAudioEvent = function(data, event, id) {
    try {
		var currAudObj = (typeof data != "string"? data: window.JSON.parse(data));
			trackMetrics({
				type: event,
				data: {
					instance: id,
					audio: currAudObj
				}
			});
	} catch(e){}
}; 

window.sendNewsPulse = function(data){
	try {
		trackMetrics({
			type: "dynamic-newsPulseOmniCall",
			data: {
				newspulse: {
					query: data
				}
			}
		});
	} catch(e){}
};

window.sendHTML5Event = function(data, event){
	if (data.contentType =="audio") {
		trackMetrics("audio-start",data.headline, "adbp-audio");
	} else {
		data.metas= {branding:"ireport"};
		try {
			trackMetrics({
				type: event,
				data: {
					video : data
				}
			});
		} catch(e){}
	}
};

window.sendOpenStoryPerspective = function(data){
	try {
		trackMetrics({
			type: "ireport-openstory",
			data: {
				openstory : data
			}
		});
	} catch(e){}
};

window.trackExitLinkMetrics = function(action){
  try{
       PubSub.publish(action,"");
  }
  catch(e){}
};

if (wminst.Util.isStellarPage() && wminst.Util.isUserAccountPage() && window.ZION_MESSAGE_BUS) {
    ZION_MESSAGE_BUS.subscribe("event_published", function(message) {
        try {
            var msgIndex = message.length - 1;
            var eventObj = message[msgIndex].message.event; 
            var eventName = eventObj.name;
            if (eventName == "GenericSubmit") {
                var compId = eventObj.props.component_id;
                if (compId == "create_account" || "log_in") {
                    var actionId = (compId == "create_account") ? "registration" : "login";
                    var httpResp = eventObj.props.traits.http_response;
                    wminst.Util.log("eventName =", eventName, "compId =", compId, "httpResp =", httpResp);
                    if (httpResp == "success") {
                        window.trackMetrics({
                            type: "site_" + actionId + "_success",
                            data: {action: compId}
                        });
                    }
                }
            }
        } catch (e) {
            console.error(e);
        }
    })
}

});
_satellite["_runScript4"](function(event, target, Promise) {
wminst.isAMPVideos = function() {
    var hostName = window.location.hostname;
    return hostName.indexOf("fave.api.cnn.io") != -1 || hostName.indexOf("fave-api.cnn.com") != -1;
};

wminst.isMoneyVideo = function(v) {
    var sectionName = v.sectionName || v.category || "";
    var sectionNameList = ["media", "intl_business", "tech", "business", "business-videos", "cars", "investing", "success", "perspectives", "homes"];
    return sectionNameList.includes(sectionName);
};

wminst.getAMPVideoTimeStamp = function() {
    var pathName = window.location.pathname;
    var ts = "";
    if (pathName.indexOf("/v1/amp") != -1 || pathName.indexOf("/v1/cnneamp") != -1 || pathName.indexOf("/v1/fbia") != -1 || pathName.indexOf("/v1/fbiaV2") != -1) {
        ts = new Date().getTime();
    }
    return ts;
};
var mediaPlayer = new Array;
wminst.getCNNMediaCollection = function() {
	return {
		get: function(i, p) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					return mPlayer[j][p];
				}	
			}
		},
		set: function(i, p, v) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					mPlayer[j][p] = v;
					break;
				}
			}	
		},
		toggle: function(i, p) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					var v = mPlayer[j][p];
					mPlayer[j][p] = !v;
					break;
				}
			}	
		},		
		start: function(i, t) {
			var mPlayer = mediaPlayer;
			mPlayer.push(new objMediaPlayer(i,t));
			function objMediaPlayer(cid, mediaTitle) {
				this.containerId = cid;
				this.mediaTitle = mediaTitle;
				this.vidStarted = false;
				this.audStarted = false;
				this.hasScrubbed = false;
				this.isAuto = false;
				this.isTen = false;
				this.isTwentyFive = false;
				this.isHalf = false;
				this.isSeventyFive = false;
				this.isBuffering = false;
				this.isPaused = false;
				this.isMidrollStarted = false;
				this.adNumber = 0;
				this.startTime = (new Date).getTime();
				this.currentTime = (new Date).getTime();
				this.timeSpent = 0;
			}
		},
		pause: function(i) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					var p = mPlayer[j].isPaused;
					var b = mPlayer[j].isBuffering;
					if (!b) {
						if (p) {
							mPlayer[j].startTime = (new Date).getTime();
						} else {
							var playedTime = (new Date).getTime() - mPlayer[j].startTime + mPlayer[j].timeSpent;
							mPlayer[j].timeSpent = playedTime;
						}
					}
					mPlayer[j].isPaused = !p;
					break;
				}
			}	
		},
		buffer: function(i) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					var p = mPlayer[j].isPaused;
					var b = mPlayer[j].isBuffering;
					if (!p) {
						if (b) {
							mPlayer[j].startTime = (new Date).getTime();
						} else {
							var playedTime = (new Date).getTime() - mPlayer[j].startTime + mPlayer[j].timeSpent;
							mPlayer[j].timeSpent = playedTime;
						}
					}	
					mPlayer[j].isBuffering = !b;
					break;
				}
			}
		},
		progress: function(i) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					mPlayer[j].currentTime = (new Date).getTime();
					var playedTime = (mPlayer[j].currentTime - mPlayer[j].startTime + mPlayer[j].timeSpent) / 1000;
					mPlayer[j].startTime = (new Date).getTime();
					mPlayer[j].timeSpent = 0;
					return Math.round(playedTime);
				}
			}
				
		},
		complete: function(i) {
			var mPlayer = mediaPlayer;
			for (var j = mPlayer.length - 1; j >= 0; j--) {
				if (mPlayer[j].containerId == i) {
					var playedTime = ((new Date).getTime() - mPlayer[j].startTime + mPlayer[j].timeSpent) / 1000;
					mPlayer[j].timeSpent = 0;
					return Math.round(playedTime);
				}
			}
				
		}
	};
};


wminst.capCNNTimeSpent = function(timeSpent, trt, liveInterval) {
    try { //check media time spent value
        var timeLimit = 0;
        if ((parseFloat(timeSpent) == parseInt(timeSpent)) && !isNaN(timeSpent)) {
            if (liveInterval && liveInterval > 0) {
                timeLimit = liveInterval; //time limit value set by webdev
            } else {
                timeLimit = 60; //time limit in sec
                if (trt && parseFloat(trt) > 0) {
                    timeLimit = parseFloat(trt) * 2;
                }
            }
            if (timeSpent > timeLimit) {
                timeSpent = timeLimit;
            } else if (timeSpent < 0) {
                timeSpent = 0;
            }
        } else {
            timeSpent = 0;
        }
    } catch (e) {
        timeSpent = 0;
    }
    return timeSpent;
};

wminst.capCNNTimeSpent2 = function(timeSpent, trt) {
    try { //check media time spent value
        if ((parseFloat(timeSpent) == parseInt(timeSpent)) && !isNaN(timeSpent)) { //valid time spent value
            if (trt && !isNaN(trt) && (parseFloat(trt) == parseInt(trt))) { //valid media length
                if (timeSpent > parseFloat(trt) * 2) {
                    timeSpent = parseFloat(trt) * 2;
                } else if (timeSpent < 0) {
                    timeSpent = 0;
                }
            } else { //invalid media length
                timeSpent = 0;
            }
        } else { //invalid time spent value
            timeSpent = 0;
        }
    } catch (e) {
        timeSpent = 0;
    }
    return timeSpent;
};
});
_satellite["_runScript5"](function(event, target, Promise) {
wminst.bomboraPageBeacon = function() {
    if (!window._ml) {
        (function (w,d,t){
         _ml = w._ml || {};
         _ml.nq = w._ml.nq || [];
         _ml.nq.push(['track', '64240', {fp: 'YOUR_USER_ID'}]);
         var s, cd, tag; s = d.getElementsByTagName(t)[0]; cd = new Date();
         tag = d.createElement(t); tag.async = 1;
         tag.src = 'https://cdn.ml314.com/taglw.js';
         s.parentNode.insertBefore(tag, s);
        })(window,document,'script');
    } else {
        _ml.nq = window._ml.nq || [];
        _ml.nq.push(['track', '64240']);
    }
};

PubSub.subscribe("dynamic-page", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("tab-page", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("cnnsearch-results", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("weather-page", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("picker-pageview", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("readmore-page", function(data) {
    wminst.bomboraPageBeacon();
});

PubSub.subscribe("breaking-news", function(data) {
    if (data.domain && (data.domain == "cnn.com" || data.domain == "us.cnn.com" || data.domain == "sweet.next.cnn.com" || data.domain == "edition.cnn.com")) {
        // Do Nothing
    } else {
        wminst.bomboraPageBeacon();
    }
});


/* ============== Page Load ============= */
if (!wminst.Util.isDynamicPage() && !wminst.Util.isFavePage() && !wminst.Util.inIFrame()) { 
    wminst.bomboraPageBeacon();
}
});
_satellite["_runScript6"](function(event, target, Promise) {
wminst.nielsenPageBeacon = function() {
    var ci, si, rp, random;
    ci = "us-204044h";
    si = escape(window.location.href);
    rp = escape(document.referrer);
    random = +(new Date());
    wminst.Util.sendImagePixel("//secure-us.imrworldwide.com/cgi-bin/m?ci=" + ci + "&cg=0&cc=1&si=" + si + "&rp=" + rp +"&ts=compact&rnd=" + random);
};

if (!wminst.Util.isRefreshPage() && !wminst.Util.inIFrame()) {
    wminst.nielsenPageBeacon();
}
});
_satellite["_runScript7"](function(event, target, Promise) {
wminst.Util.loadScript("//www.i.cdn.cnn.com/zion/zion-mb.min.js", function() {
    try {
        if (typeof s !== "undefined") {
             var bus = ZionMessageBus.getInstance();
             var marketingCloudID = s.visitor.getMarketingCloudVisitorID();
             var visitorID = s.visitor.getAnalyticsVisitorID();
             bus.publish('id_found', {type:'adobe_ecid', value: marketingCloudID});
             bus.publish('id_found', {type:'adobe_vi', value: visitorID});
        }
    } catch (e) {
        console.error(e);
    }
 });
});
_satellite["_runScript8"](function(event, target, Promise) {
PubSub.subscribe("cnnvideo-start", function(data) {
    wminst.sendFacebookPixel();
});

PubSub.subscribe("cnnvideo-autostart", function(data) {
    wminst.sendFacebookPixel();
});

PubSub.subscribe("cnnvideo-live", function(data) {
    wminst.sendFacebookPixel();
});

wminst.sendFacebookPixel = function(){
    var hostName = window.location.hostname;
    if (hostName.indexOf("edition") == -1) {
        wminst.Util.sendImagePixel("//www.facebook.com/tr?id=1407388882899381&ev=PageView&noscript=1");
    }
};
});
_satellite["_runScript9"](function(event, target, Promise) {
try {
    requirejs(["//i.cdn.turner.com/analytics/comscore/streamsense.5.2.0.160629.min.js"], function() {});
} catch (e) {
    wminst.Util.loadScript("//s.cdn.turner.com/analytics/comscore/streamsense.5.2.0.160629.min.js");
}

PubSub.subscribe("Player_Ready", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
    wminst.myStreamingTag = new ns_.StreamingTag({
        customerC2: "6035748"
    });
});
PubSub.subscribe("cs_video-preroll", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
    if (!wminst.prev_vid) { //first video
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    } else if (wminst.prev_vid && wminst.prev_vid !== data.id) { //new video
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    } else if (wminst.completed_vid && wminst.completed_vid == data.id) {
        wminst.completed_vid = "";
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    }
    wminst.prev_vid = data.id;
    var clength = data.ad_duration || 0;
    try {
        clength = parseInt(clength);
        if (clength % 1000 !== 0) {
            clength = clength * 1000;
        }
    } catch (e) {
        clength = 0;
    }
    var cs_ucfr = wminst.Util.isTagConsented("comscore") ? "1" : "0";
    var metadata = {
        ns_st_cl: clength || 3000,
        cs_ucfr: cs_ucfr
    };
    if (ns_) {
        ns_.StreamingTag.AdType = {
            BrandedOnDemandContent: "34",
            BrandedOnDemandLive: "35",
            BrandedOnDemandMidRoll: "32",
            BrandedOnDemandPostRoll: "33",
            BrandedOnDemandPreRoll: "31",
            LinearLive: "21",
            LinearOnDemandMidRoll: "12",
            LinearOnDemandPostRoll: "13",
            LinearOnDemandPreRoll: "11",
            Other: "00"
        };
    }
    var atype = ns_.StreamingTag.AdType.LinearOnDemandPreRoll;
    if (data.adType && data.adType.toLowerCase() === "midroll") { atype = ns_.StreamingTag.AdType.LinearOnDemandMidRoll; } 
    if (data.adType && data.adType.toLowerCase() === "postroll") { atype = ns_.StreamingTag.AdType.LinearOnDemandPostRoll; } 
    if (data.isLive && (data.isLive == "true" || data.isLive == true)) {
        atype = ns_.StreamingTag.AdType.LinearLive;
    }
    wminst.myStreamingTag.playVideoAdvertisement(metadata, atype);
});
PubSub.subscribe("cs_ad-complete", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
});
PubSub.subscribe("cs_video-play", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
    if (!wminst.prev_vid) { //first video
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    } else if (wminst.prev_vid && wminst.prev_vid !== data.id) { //new video
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    } else if (wminst.completed_vid && wminst.completed_vid == data.id) {
        wminst.completed_vid = "";
        wminst.myStreamingTag = new ns_.StreamingTag({
            customerC2: "6035748"
        });
    }
    wminst.prev_vid = data.id;
    var clength = data.trt || 0;
	var c4 = "CNN";
	var c3 = "*null";
	var c6 = "*null";
    try {
        clength = parseInt(clength);
        if (clength % 1000 !== 0) {
            clength = clength * 1000;
        }
    } catch (e) {
        clength = 0;
    }
    var adate = data.timestamp || "";
    try {
        if (adate) {
            adate = new Date(adate);
            adate = adate.toISOString().substring(0, 10);
        }
    } catch (e) {}
    if (window.location.hostname.indexOf("edition") != -1) {
        c4 = "CNNI";
		c3 = "CNNEDITION";
    }
    if (typeof data.category != 'undefined' && data.category.toLowerCase() === "spanish") {
        c4 = "CNNESPANOL";
    }
    if (typeof data.category != 'undefined' && data.category.toLowerCase() === "cnnmoney") {
        c4 = "CNNMONEY";
    }
	var ch = wminst.Util.getCNNSection(0) || "";
	var pn = {
			"entertainment":	"CNNENT",
			"health":		      "CNNHEALTH",
			"politics":		    "CNNPOLITICS",
			"tech":			      "CNNTECH",
			"travel":		      "CNNTRAVEL",
			"us":			        "CNNUS",
			"world":		      "CNNWORLD",
			"opinions":		    "CNNOPINION",
			"living":		      "CNNLIVING",
			"cnn homepage":	  "CNNHOME",
			"ireport":        "IREPORT",
			"justice":        "CNNJUSTICE",
			"elections":      "CNNPOLITICS",
			"style":			    "CNNSTYLE"
		} [ch];
	if (pn) { c4 = pn; }
	if(pn && ch == "elections"){ c6 = "ELECTION";}
  if (wminst.isMoneyVideo(data)) {
     		c4 = "CNNBUSINESS";
     		c6 = "BUSINESS";
   }
    var cs_ucfr = wminst.Util.isTagConsented("comscore") ? "1" : "0";
    var metadata = {
        ns_st_ci: data.id,
        ns_st_cl: clength,
        ns_st_st: "*null",
        ns_st_pu: "CNN",
        ns_st_pr: data.subcategory || "*null",
        ns_st_ep: data.headline || "*null",
        ns_st_sn: "*null",
        ns_st_en: "*null",
        ns_st_ge: data.category || "*null",
        ns_st_ia: "0",
        ns_st_ce: "0",
        ns_st_ddt: "*null",
        ns_st_tdt: adate || "*null",
        c3: c3,
        c4: c4,
        c6: c6,
        cs_ucfr: cs_ucfr
    };
    if (ns_) {
        ns_.StreamingTag.ContentType = {
            Bumper: "99",
            Live: "13",
            LongFormOnDemand: "12",
            Other: "00",
            ShortFormOnDemand: "11",
            UserGeneratedLive: "23",
            UserGeneratedLongFormOnDemand: "22",
            UserGeneratedShortFormOnDemand: "21"
        };
    }
    var vtype = ns_.StreamingTag.ContentType.ShortFormOnDemand;
    if (data.content_type && data.content_type == "episode") {
        vtype = ns_.StreamingTag.ContentType.LongFormOnDemand;
    }
    if (data.id && data.id.indexOf("cvplive") != -1  ) {
        vtype = ns_.StreamingTag.ContentType.Live;
    }
    if (data.isLive && data.isLive == "true") {
        vtype = ns_.StreamingTag.ContentType.Live;
    }
    wminst.myStreamingTag.playVideoContentPart(metadata, vtype);
});
PubSub.subscribe("cs_video-pause", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
});
PubSub.subscribe("cs_video-resume", function(data) {
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }

    var clength = data.trt || 0;
	var c4 = "CNN";
	var c3 = "*null";
	var c6 = "*null";
    try {
        clength = parseInt(clength);
        if (clength % 1000 !== 0) {
            clength = clength * 1000;
        }
    } catch (e) {
        clength = 0;
    }
    var adate = data.timestamp || "";
    try {
        if (adate) {
            adate = new Date(adate);
            adate = adate.toISOString().substring(0, 10);
        }
    } catch (e) {}
    if (window.location.hostname.indexOf("edition") != -1) {
        c4 = "CNNI";
		c3 = "CNNEDITION";
    }
    if (typeof data.category != 'undefined' && data.category.toLowerCase() === "spanish") {
        c4 = "CNNESPANOL";
    }
    if (typeof data.category != 'undefined' && data.category.toLowerCase() === "cnnmoney") {
        c4 = "CNNMONEY";
    }
	var ch = wminst.Util.getCNNSection(0) || "";
	var pn = {
			"entertainment":	"CNNENT",
			"health":		      "CNNHEALTH",
			"politics":		    "CNNPOLITICS",
			"tech":			      "CNNTECH",
			"travel":		      "CNNTRAVEL",
			"us":			        "CNNUS",
			"world":		      "CNNWORLD",
			"opinions":		    "CNNOPINION",
			"living":		      "CNNLIVING",
			"cnn homepage":	  "CNNHOME",
			"ireport":        "IREPORT",
			"justice":        "CNNJUSTICE",
			"elections":      "CNNPOLITICS",
			"style":			    "CNNSTYLE"
		} [ch];
	if (pn) { c4 = pn; }
	if(pn && ch == "elections"){ c6 = "ELECTION";}
  if (wminst.isMoneyVideo(data)) {
     		c4 = "CNNBUSINESS";
     		c6 = "BUSINESS";
   }
    var cs_ucfr = wminst.Util.isTagConsented("comscore") ? "1" : "0";
    var metadata = {
        ns_st_ci: data.id,
        ns_st_cl: clength,
        ns_st_st: "*null",
        ns_st_pu: "CNN",
        ns_st_pr: data.subcategory || "*null",
        ns_st_ep: data.headline || "*null",
        ns_st_sn: "*null",
        ns_st_en: "*null",
        ns_st_ge: data.category || "*null",
        ns_st_ia: "0",
        ns_st_ce: "0",
        ns_st_ddt: "*null",
        ns_st_tdt: adate || "*null",
        c3: c3,
        c4: c4,
        c6: c6,
        cs_ucfr: cs_ucfr
    };
    if (ns_) {
        ns_.StreamingTag.ContentType = {
            Bumper: "99",
            Live: "13",
            LongFormOnDemand: "12",
            Other: "00",
            ShortFormOnDemand: "11",
            UserGeneratedLive: "23",
            UserGeneratedLongFormOnDemand: "22",
            UserGeneratedShortFormOnDemand: "21"
        };
    }
    var vtype = ns_.StreamingTag.ContentType.ShortFormOnDemand;
    if (data.content_type && data.content_type == "episode") {
        vtype = ns_.StreamingTag.ContentType.LongFormOnDemand;
    }
    if ( data.id && data.id.indexOf("cvplive") != -1 ){
        vtype = ns_.StreamingTag.ContentType.Live;
    }
    if (data.isLive && data.isLive == "true") {
        vtype = ns_.StreamingTag.ContentType.Live;
    }
    wminst.myStreamingTag.playVideoContentPart(metadata, vtype);
});
PubSub.subscribe("cs_video-complete", function(data) {
    wminst.completed_vid = data.id;
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
});
PubSub.subscribe("Video_Completed", function(data) {
    wminst.completed_vid = data.id;
    if (typeof wminst.myStreamingTag != "undefined") {
        wminst.myStreamingTag.stop();
    }
});
});
_satellite["_runScript10"](function(event, target, Promise) {
wminst.comscorePageBeacon = function() {
    var c_id = "6035748";
    var cs_ucfr = wminst.Util.isTagConsented("comscore") ? "1" : "0";
    var _comscore = window._comscore = _comscore || [];
    if (wminst.Util.isFBIAPage() === true) {
        var comscorekw = "fbia";
        _comscore.push({ c1: "2", c2: c_id, cs_ucfr: cs_ucfr, options:{url_append: "comscorekw=fbia"}});
    } else {
        _comscore.push({ c1: "2", c2: c_id, cs_ucfr: cs_ucfr });
    }
    
    try {
        if (window.COMSCORE) {
            COMSCORE.beacon(_comscore[0]);
            wminst.Util.sendImagePixel("//cdn.cnn.com/analytics/cnn/comscore-pageview-candidate.json");
        } else {
            var protocol = document.location.protocol == "https:" ? "https://sb" : "http://b";
            wminst.Util.loadScript(protocol + ".scorecardresearch.com/beacon.js");
        }
    } catch (e) {}
};

PubSub.subscribe("dynamic-page", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("tab-page", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("cnnsearch-results", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("weather-page", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("picker-pageview", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("cnngallery-click", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("readmore-page", function(data) {
    wminst.comscorePageBeacon();
});

PubSub.subscribe("breaking-news", function(data) {
    if (data.domain && (data.domain == "cnn.com" || data.domain == "us.cnn.com" || data.domain == "sweet.next.cnn.com" || data.domain == "edition.cnn.com")) {
        // Do Nothing
    } else {
        wminst.comscorePageBeacon();
    }
});


/* ============== Page Load ============= */
if (!wminst.Util.isDynamicPage() && !wminst.Util.isFavePage() && !wminst.Util.inIFrame()) { 
    wminst.comscorePageBeacon();
}


});
_satellite["_runScript11"](function(event, target, Promise) {
PubSub.subscribe("cnnvideo-start", function(data) {
    wminst.nielsenVideoBeacon("dav0", data);
});

PubSub.subscribe("cnnvideo-autostart", function(data) {
    wminst.nielsenVideoBeacon("dav0", data);
});

PubSub.subscribe("cnnvideo-live", function(data) {
    wminst.nielsenVideoBeacon("dav0", data, "live");
});

PubSub.subscribe("cnnvideo-episode", function(data) {
    wminst.nielsenVideoBeacon("dav0", data);
});

PubSub.subscribe("cnnvideo-complete", function(data) {
    wminst.nielsenVideoBeacon("dav2", data);
});

wminst.nielsenVideoBeacon = function(state, data, cg) {
    var v = wminst.Util.getVideoMetadata(data);
    var ci, c6, tl, random, url;
    ci = "us-100120";
    c6 = (v.category && (v.category == "cnnmoney" || v.category == "business")) ? "vc,c02" : "vc,b01";
    tl = state + "-" + v.id;
    random = +(new Date());
    url = "//secure-us.imrworldwide.com/cgi-bin/m?ci=" + ci + "&c6=" + c6 + "&cc=1&tl=" + tl + "&rnd=" + random;
    if (cg) url += "&cg=" + cg;
    wminst.Util.sendImagePixel(url);
};
});
_satellite["_runScript12"](function(event, target, Promise) {
function checkUserAuthentication(){var e="";return window.is_expansion||(e="undefined"!=typeof s.prop32&&"adbp:interactive"==s.prop32?wminst.Util.getCNNAuthenticated("authid","displayname","reg:logged in","requires authentication","reg:not logged in","?"):"undefined"!=typeof s.prop28&&"watch cnn:activation"==s.prop28?wminst.Util.getCNNAuthenticated("authid","displayname","reg:logged in","does not require authentication","reg:not logged in","?"):wminst.Util.getCNNAuthenticated("authid","displayname","reg:logged in","anonymous","reg:not logged in","?")),e}wminst.trackPage=function(){wminst.Util.setATTWMID(),s.t()},wminst.trackLink=function(e){wminst.Util.setATTWMID(),s.tl(this,"o",e)},PubSub.subscribe("dynamic-autoRefresh",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,eVar26,eVar27,eVar28,eVar29,eVar30,eVar32,eVar33,prop35,eVar35,eVar36,eVar37,prop44,eVar44,eVar45,prop46,eVar46,prop47,eVar47,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event60",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.eVar27=s.channel?s.channel:wminst.Util.getCNNSection(0),s.eVar28=wminst.Util.getCNNSection(1),s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=wminst.Util.getSiteSpecificSettings(1),s.eVar32=wminst.Util.getCNNTemplateType("long"),s.eVar33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.eVar37=wminst.Util.getCNNPlatform(),s.prop44=wminst.Util.getCNNSourceID(),s.eVar44=wminst.Util.getCNNVertical(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.prop69=e,s.prop73=wminst.Util.getCNNVisitorID("s_vi"),wminst.trackLink("auto-refresh"),s.clearVars()}),PubSub.subscribe("dynamic-page",function(e){if((wminst.Util.isTravelPage()||wminst.Util.isStylePage())&&!wminst.Util.isLiveStoryPage())return wminst.trackPage();s.manageVars("clearVars"),s.linkTrackVars="events,pageName,channel,hier1,prop2,eVar2,prop4,eVar4,prop5,eVar5,prop11,eVar11,prop14,eVar14,prop15,eVar15,eVar22,prop23,eVar23,eVar27,prop28,eVar28,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop43,prop44,eVar44,eVar45,prop48,prop50,eVar50,prop51,eVar51,prop64,eVar64,eVar65,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar79,eVar89,list1,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents;var t=e.clickObj||{};if(t.socialType){var r=s.pageName;if(r.match(/\s\[.+\]$/)){var a=/(.+)\s\[.+\]$/.exec(r);a&&(r=a[1])}s.pageName=r+" ["+t.socialType+"]"}if(e.pageURL){try{e.pageURL.split("/")[2].replace("www.",""),e.pageURL=e.pageURL.toLowerCase(),e.pageURL=e.pageURL.replace(/^.*\/\/[^\/]+/,""),e.pageURL=e.pageURL.replace("/index.html","/"),s.pageName=wminst.Util.getCNNPageName(e.pageURL)}catch(C){}}else s.pageName=wminst.Util.getCNNPageName();e.pageNumber&&(s.pageName=wminst.Util.getCNNPageName()+":page"+e.pageNumber),"undefined"!=typeof window.CNN&&"undefined"!=typeof window.CNN.omniture&&"undefined"!=typeof window.CNN.omniture.section&&"facts first"==window.CNN.omniture.section[1]&&(s.linkTrackEvents=s.linkTrackEvents+",event59",s.events=s.linkTrackEvents),s.pageURL=wminst.Util.getCNNPageURL();try{s.channel=wminst.Util.getCNNSection(0),s.prop11=wminst.Util.getCNNBrandingPartner(),s.prop28=wminst.Util.getCNNSection(1),s.prop33=wminst.Util.getCNNContentType();var i="",n="",p="";n=wminst.Util.getCNNPublishDate(),i=wminst.Util.getCNNDaysSinceLastPublish("a");var o=["content:","other:live story"];p=wminst.Util.getCNNTemplateType("long");var l=!1;if(p&&void 0!==p){for(var c in o)-1!=p.indexOf(o[c])&&(l=!0);l?(s.prop10=i,s.prop16=n):(s.prop10="",s.prop16="")}if(s.prop11=wminst.Util.getCNNBrandingPartner(),"undefined"!=typeof window.CNN.omniture&&"undefined"!=typeof window.CNN.omniture.branding_social)try{s.prop14=window.CNN.omniture.branding_social||""}catch(C){}s.prop23=wminst.Util.getCNNPageHeadline(),"ngtv"==wminst.Util.getCNNUIEngagement()&&(s.prop57=e.mvpd,s.prop59=e.adobe_hash_id)}catch(v){}var N="",V="",g="",m="";if("undefined"!=typeof e.headline)try{window.CNN=window.CNN||{},window.CNN.omniture=window.CNN.omniture||{},window.CNN.omniture.section=e.section,window.CNN.omniture.template_type=e.template_type,window.CNN.omniture.branding_content_page=e.branding_content_page,window.CNN.omniture.branding_social=e.branding_social,window.CNN.omniture.cap_author=e.cap_author,window.CNN.omniture.cap_genre=e.cap_genre,window.CNN.omniture.cap_content_type=e.cap_content_type,window.CNN.omniture.cap_topic=e.cap_topic,window.CNN.contentModel=window.CNN.contentModel||{},window.CNN.contentModel.analytics=window.CNN.contentModel.analytics||{},window.CNN.contentModel.analytics.pageTop=e.page_top||{},window.CNN.contentModel.analytics.isArticleVideoCollection=e.is_article_video_collection||!1,window.CNN.omniture.user_auth_state=e.user_auth_state,V=wminst.Util.getCNNDaysSinceLastPublish(e.publish_date),s.prop10=V+"",g=wminst.Util.getCNNBrandingPartner(),s.prop11=g,s.prop14=e.branding_social,s.prop14&&""!==s.prop14&&(s.linkTrackEvents="event24,"+s.linkTrackEvents),s.prop11&&""!==s.prop11&&(s.linkTrackEvents="event21,"+s.linkTrackEvents),s.events=s.linkTrackEvents,s.prop16=e.publish_date,s.prop23=e.headline.toLowerCase(),s.channel=e.section[0],N=e.section[0]+":"+(e.section[1]?e.section[1]:"nvs"),s.prop28=N,m=wminst.Util.getADBPContentType("adbp:none"),s.prop33=m.ct,s.eVar44=wminst.Util.getCNNPageVertical(),""!==m.events?(s.events=s.events+","+m.events,s.linkTrackEvents=s.events):"article"!=window.CNN.omniture.template_type&&"article"!=window.CNN.omniture.cap_content_type||(s.events=s.events+",event39",s.linkTrackEvents=s.events),e.load_type&&"lazy_load"==e.load_type&&(s.events="event26,event72",s.linkTrackEvents=s.events),e.load_type&&"refresh_load"==e.load_type&&(s.events="event26,event71",s.linkTrackEvents=s.events)}catch(C){}try{s.pageName=wminst.Util.getCNNPageName(),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop35=wminst.Util.getCNNCodeVersion(),s.prop64=wminst.Util.getCNNUIEngagement(),s.list1=wminst.Util.getCNNTopic(),s.prop2=wminst.Util.getCNNAuthor(),s.prop4=wminst.Util.getPageAttribution(),s.prop5=wminst.Util.getCNNCapGenre(),s.prop8=wminst.Util.getCNNVisitNumber(),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.prop26=wminst.Util.getCNNBaseURL(),s.server=s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform(),s.prop43=wminst.Util.getCNNPostID(),s.prop44=wminst.Util.getCNNSourceID(),s.eVar45=wminst.Util.getLSPostPosition(),s.prop48=wminst.Util.getCNNTopicAvailability(),s.prop50=wminst.Util.getCNNPostTitle(),s.prop51=wminst.Util.getCNNSiteSectionLevel3();var w=wminst.Util.gCNNUserAuthState();s.eVar51=w.user_registered_status,s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.prop49=wminst.Util.getCNNPreviousPageName(),s.prop56=wminst.Util.getCNNOrientation(),s.prop57=wminst.Util.getCNNMVPD(),s.prop59=wminst.Util.getCNNAdobeID(),s.prop74=w.user_account_status,s.prop75=wminst.Util.getCNNUserAuthState(),s.eVar89=w.user_login_status,s.hier1=wminst.Util.getCNNHierachy()}catch(v){}try{if(wminst.Util.isPoliticsExplorer()&&(s.eVar50=wminst.Util.getCNNInteractiveState(e),s.prop51=wminst.Util.getCNNSiteSectionLevel3("explorer"),s.eVar79=wminst.Util.getCNNExploreIndentify(e)),e.interaction_type&&-1!=e.interaction_type.indexOf("road-to-270")){var U=e.interaction_type.split(":");s.pageName=s.pageName+"["+U[2].toLowerCase()+"]",s.prop51=wminst.Util.getCNNSiteSectionLevel3("road-to-270")}}catch(v){}wminst.trackPage()}),PubSub.subscribe("refresh_load",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,channel,hier1,prop2,eVar2,prop4,eVar4,prop5,eVar5,prop11,eVar11,prop14,eVar14,prop15,eVar15,eVar22,prop23,eVar23,eVar27,prop28,eVar28,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop43,prop44,eVar44,eVar45,prop48,prop50,eVar50,prop51,eVar51,prop64,eVar64,eVar65,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar79,eVar89,list1,list2",s.events="event26,event71",s.linkTrackEvents=s.events,s.pageName=wminst.Util.getCNNPageName(),s.channel=wminst.Util.getCNNSection(0),s.server=wminst.Util.getADBPURL("domain"),s.prop2=wminst.Util.getCNNAuthor(),s.prop4=wminst.Util.getPageAttribution(),s.prop5=wminst.Util.getCNNCapGenre(),s.prop8=wminst.Util.getCNNVisitNumber(),s.prop10=wminst.Util.getCNNDaysSinceLastPublish("a"),s.prop11=wminst.Util.getCNNBrandingPartner(),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.prop16=wminst.Util.getCNNPublishDate(),s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.prop26=wminst.Util.getCNNBaseURL(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform(),s.prop44=wminst.Util.getCNNSourceID(),s.eVar44=wminst.Util.getCNNPageVertical(),s.eVar45=wminst.Util.getLSPostPosition(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.prop48=wminst.Util.getCNNTopicAvailability(),s.prop49=wminst.Util.getCNNPreviousPageName(),s.prop51=wminst.Util.getCNNSiteSectionLevel3();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop57=wminst.Util.getCNNMVPD(),s.prop59=wminst.Util.getCNNAdobeID(),s.prop64=wminst.Util.getCNNUIEngagement(),s.prop74=t.user_account_status,s.prop75=wminst.Util.getCNNUserAuthState(),s.eVar89=t.user_login_status,s.list1=wminst.Util.getCNNTopic(),s.hier1=wminst.Util.getCNNHierachy();try{s.prop23=e.headline.toLowerCase(),s.prop43=e.post_id,s.prop50=e.post_title.toLowerCase()}catch(r){}wminst.trackPage(),s.clearVars()}),PubSub.subscribe("word-count",function(){}),PubSub.subscribe("dynamic-link",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,prop35,eVar35,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName(),s.prop35=wminst.Util.getCNNCodeVersion();try{wminst.trackLink(e.link_name)}catch(t){}s.clearVars()}),PubSub.subscribe("tab-page",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,server,channel,eVar26,eVar27,prop28,eVar28,eVar29,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop44,prop51,eVar51,prop74,eVar74,eVar89,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.eVar27="D=ch",s.prop28=wminst.Util.getCNNSection(1),s.eVar29="D=server",s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.prop44=wminst.Util.getCNNSourceID(),s.prop51=wminst.Util.getCNNSiteSectionLevel3();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop74=t.user_account_status,s.eVar74="D=c74",s.eVar89=t.user_login_status;try{s.pageName="cnn:v:/video/"+e}catch(r){}s.eVar26="D=pageName",s.pageURL=wminst.Util.getCNNPageURL(),wminst.trackPage(),s.clearVars()}),PubSub.subscribe("search-results",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,prop27,eVar27,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop39,eVar39,prop44,eVar51,prop74,eVar74,eVar89,list2",s.linkTrackEvents="event27",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName();try{s.channel=wminst.Util.getJObj(e,"section[0]")}catch(r){}try{s.prop27=wminst.Util.getJObj(e,"search.number_results")}catch(r){}s.prop32="other:search results";try{s.prop33=wminst.Util.getJObj(e,"content_type")}catch(r){}s.prop35=wminst.Util.getCNNCodeVersion();try{s.prop39=wminst.Util.getJObj(e,"search.term")}catch(r){}s.prop44=wminst.Util.getCNNSourceID();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop74=t.user_account_status,s.eVar74="D=c74",s.eVar89=t.user_login_status,s.clearVars()}),PubSub.subscribe("cnnsearch-results",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,prop8,eVar8,eVar15,eVar22,prop26,eVar26,prop27,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop37,eVar37,prop39,eVar39,prop44,eVar44,prop46,eVar46,prop47,eVar47,eVar51,prop59,eVar59,prop64,eVar64,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar89,hier1,list2",s.linkTrackEvents="event26,event27",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName(),s.server=wminst.Util.getADBPURL("domain"),s.prop8=wminst.Util.getCNNVisitNumber(28),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.prop26=wminst.Util.getCNNBaseURL(),s.channel=wminst.Util.getCNNSection(0),s.prop27=e.search_results_count+"",s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32="other:search results",s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform();try{e.search_term=e.search_term.replace(/\+/g," "),e.search_term=e.search_term.trim(),e.search_term=e.search_term.toLowerCase()||"empty search"}catch(r){}s.prop39=e.search_term,s.prop44=wminst.Util.getCNNSourceID(),s.evar44||(s.eVar44=wminst.Util.getCNNVertical()),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.prop49=wminst.Util.getCNNPreviousPageName();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop74=t.user_account_status,s.eVar89=t.user_login_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop57=wminst.Util.getCNNMVPD(),s.prop59=wminst.Util.getCNNAdobeID(),s.prop64=wminst.Util.getCNNUIEngagement(),s.prop75=wminst.Util.getCNNUserAuthState(),s.hier1=wminst.Util.getCNNHierachy(),s.pageURL=wminst.Util.getCNNPageURL(),wminst.trackPage(),s.clearVars()}),PubSub.subscribe("weather-page",function(){s.manageVars("clearVars"),s.linkTrackVars="events,server,prop35,eVar35,prop44,list2",s.linkTrackEvents="event62",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName(),s.server=wminst.Util.getADBPURL("domain"),s.prop35=wminst.Util.getCNNCodeVersion(),s.prop44=wminst.Util.getCNNSourceID(),s.pageURL=wminst.Util.getCNNPageURL(),wminst.trackPage(),s.clearVars()}),PubSub.subscribe("dynamic-toggle",function(){s.manageVars("clearVars"),s.linkTrackVars="events,server,pageName,channel,eVar27,prop28,eVar28,eVar29,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop44,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.prop18=s.eVar18=null,s.channel=s.eVar27=null,s.prop28=s.eVar28=null,s.prop8=s.eVar8=null,s.prop26=null,s.pageName=s.eVar26=null,s.prop30=s.eVar30=null,s.prop32=s.eVar32=null,s.prop33=s.eVar33=null,s.prop34=s.eVar34=null,s.prop35=s.eVar35=null,s.prop40=s.eVar40=null,s.prop44=wminst.Util.getCNNSourceID(),s.hier1=null}),PubSub.subscribe("dynamic-impressions",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,pageName,prop18,eVar18,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName();try{s.prop18=e.value}catch(t){}s.eVar18="D=c18";try{wminst.trackLink(e.link_name+"")}catch(t){}s.clearVars()}),PubSub.subscribe("breaking-news",function(e){s.linkTrackVars="events,server,channel,pageName,prop4,eVar4,prop8,eVar8,prop16,eVar16,eVar22,eVar26,eVar27,prop28,eVar28,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop37,eVar37,prop46,eVar46,prop47,eVar47,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop64,eVar64,prop69,eVar69,prop73,eVar73,prop75,eVar75,list2",s.channel=wminst.Util.getCNNSection(0);var t=wminst.Util.getCNNBreakingNewsHP(s.prop32,s.channel);s.pageName=wminst.Util.getCNNPageName(),s.server=wminst.Util.getADBPURL("domain"),s.pageURL=wminst.Util.getCNNPageURL(),s.prop4=t+e.headline.toLowerCase(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop69=e.item,s.manageVars("clearVars","prop16,eVar16,prop44,eVar44,prop55,eVar55",1),!e.domain||"cnn.com"!=e.domain&&"us.cnn.com"!=e.domain&&"sweet.next.cnn.com"!=e.domain&&"edition.cnn.com"!=e.domain?(s.linkTrackEvents="event76",s.events=s.linkTrackEvents,wminst.trackPage()):(s.linkTrackEvents="event26",s.events=s.linkTrackEvents),s.clearVars()}),PubSub.subscribe("picker-pageview",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,campaign,eVar26,channel,eVar27,prop28,eVar28,heir1,server,prop8,eVar8,prop26,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop34,evar34,prop35,eVar35,eVar36,prop37,eVar37,prop44,prop46,eVar46,prop47,eVar47,eVar49,eVar49,eVar51,prop56,eVar56,prop59,eVar59,eVar72,prop74,eVar74,prop75,eVar89,eVar75,list1,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.prop1=s.eVar1=s.prop2=s.eVar2=s.prop3=s.eVar3=s.prop4=s.eVar4=s.prop6=s.eVar6=s.eVar10=s.prop11=s.eVar11=s.prop16=s.eVar16=s.prop18=s.eVar18=s.prop31=s.eVar31=s.eVar41=s.eVar44=s.eVar53=s.eVar54=s.prop64=s.eVar64=s.prop67=s.eVar67=s.prop68=s.eVar68=s.prop69=s.eVar69=s.prop73=s.eVar73="";try{s.pageName=s.eVar26="cnn:o:["+e.page_name+"]"}catch(r){}s.channel="tve",s.pageURL=wminst.Util.getCNNPageURL(),s.prop8=wminst.Util.getCNNVisitNumber(28),s.prop26=wminst.Util.getCNNBaseURL(),s.prop28="tve:picker",s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop33=wminst.Util.getCNNContentType(),s.prop34=checkUserAuthentication(),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform(),s.prop44=wminst.Util.getCNNSourceID(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.prop49=wminst.Util.getCNNPreviousPageName();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop74=t.user_account_status,s.eVar89=t.user_login_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop72=e.free_preview}catch(r){}s.prop32="adbp:none",s.eVar72=s.prop72,s.prop72="","cnn:o:[tve: successful login]"==s.pageName?(s.prop7=s.eVar7=s.prop10=s.eVar10=s.eVar22=s.prop23=s.eVar23=s.prop25=s.eVar25=s.eVar51=s.list1=s.eVar65=s.prop74=s.eVar74=s.eVar89="",s.eVar26=s.pageName,s.pageName="",s.eVar27=s.channel,s.channel="",s.eVar29=s.server,s.server="",s.linkTrackEvents="event37",s.events=s.linkTrackEvents,s.eVar28=s.prop28,s.prop28="",s.eVar30=s.prop30,s.prop30="",s.prop32=s.eVar32="",s.prop33=s.eVar33="",s.eVar56=s.prop56,s.prop56="",s.eVar57=s.prop57,s.prop57="",s.eVar59=s.prop59,s.prop59="",s.hier1=""):(s.prop57=s.eVar57="",s.prop59=s.eVar59="");try{s.prop75=wminst.Util.getCNNUserAuthState()}catch(r){}wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.trackPage(),s.clearVars()}),PubSub.subscribe("picker-click",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,channel,server,prop14,eVar14,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop34,eVar34,prop35,eVar35,eVar36,prop37,eVar37,prop46,eVar46,prop47,eVar47,eVar56,eVar57,eVar59,prop69,eVar69,eVar72,prop75,eVar75,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents;try{s.pageName=s.eVar26="cnn:o:["+e.page_name+"]"}catch(t){}s.channel="tve",s.prop28="tve:picker",s.server=wminst.Util.getADBPURL("domain"),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID(),s.eVar56=wminst.Util.getCNNOrientation(),s.prop56="";try{s.eVar57=e.tve_mvpd.toLowerCase(),s.prop69="tve:picker:"+e.tve_mvpd.toLowerCase()}catch(t){}s.eVar59="no mvpd set";try{s.eVar72=e.free_preview}catch(t){}s.prop73=s.eVar73="";try{s.prop75=wminst.Util.getCNNUserAuthState()}catch(t){}wminst.trackLink("picker-click:"+e.tve_mvpd.toLowerCase()),s.clearVars()}),PubSub.subscribe("social-click",function(e){s.manageVars("clearVars");var t=e.clickObj||{},r="";s.linkTrackVars="events,server,channel,pageName,prop14,eVar14,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop43,prop50,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28||(s.prop28=wminst.Util.getCNNSection(1)),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType()||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop43=wminst.Util.getCNNPostID(),s.prop50=wminst.Util.getCNNPostTitle();try{""!==(r=e.interaction?e.interaction:t.socialType)&&-1!==r.indexOf("social: ")&&(r=r.replace("social: ",""))}catch(a){}try{-1==r.indexOf("_click")&&(r+="_click"),s.prop14=t.branding_ad,s.eVar14=""}catch(a){}s.prop59=wminst.Util.getCNNAdobeID(),s.prop69="social:"+r;try{"undefined"!=typeof window.CNN&&"undefined"!=typeof window.CNN.omniture&&"facts first"==window.CNN.omniture.section[1]&&(r="",r="facts first:share:"+t.socialType.replace(/social:/g,""),s.prop69=r)}catch(a){}try{"undefined"!=typeof t.isMainNav&&1==t.isMainNav?wminst.trackLink("social-click:"+r+"global"):wminst.trackLink("social-click:"+r)}catch(a){}s.clearVars()}),PubSub.subscribe("cnngallery-click",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,channel,server,prop4,eVar4,prop5,eVar5,prop6,eVar6,prop8,eVar8,prop10,eVar10,prop11,eVar11,eVar15,eVar22,prop23,eVar23,prop25,eVar25,prop26,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop37,eVar37,prop44,eVar44,prop46,eVar46,prop47,eVar47,eVar51,prop54,eVar54,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop64,eVar64,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar89,hier1,list1,list2",s.linkTrackEvents="event26",s.events=s.linkTrackEvents,s.channel=wminst.Util.getCNNSection(0),s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName();var t="";if("undefined"!=typeof e.hpt){var r=e.hpt;try{-1==r.indexOf("_")&&(r=CNN.Utils.b64Decode(r))}catch(c){}r=(r=r.replace(/no-value-set/g,"nvs")).toLowerCase(),s.prop4=r}s.prop5=wminst.Util.getCNNCapGenre(),s.prop8=wminst.Util.getCNNVisitNumber(28),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.prop23=wminst.Util.getCNNPageHeadline(),s.prop26=wminst.Util.getCNNBaseURL(),s.eVar27="D=ch",s.prop28=wminst.Util.getCNNSection(1),s.eVar29="D=server",s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform();try{t=void 0!==(t=e.gallery_name)&&""!==t?t.replace(/(no-value-set|no value set)/g,"nvs"):"nvs"}catch(c){t="nvs"}if("undefined"!=typeof e.hpt2){var a=e.hpt2;try{-1==a.indexOf("_")&&(a=CNN.Utils.b64Decode(a))}catch(c){}a=a.replace(/no-value-set/g,"nvs"),s.prop18=a}s.prop25=t,s.prop25=s.prop25.toLowerCase();try{e.gallery_name&&"undefined"!=typeof e.gallery_name&&(s.prop6=e.gallery_name.toLowerCase(),s.eVar6="D=c6")}catch(c){}s.prop54="photo gallery:";var i=0;if("undefined"!=typeof e.gallery_type&&(s.prop33=e.gallery_type,"carousel"==e.gallery_type)){i=1,s.prop6="",s.eVar6="",s.prop25="";var n=s.eVar25="";try{n=e.content_type.replace("carousel_","")}catch(c){}"undefined"!=typeof e.carousel_type||"jumbotron"==e.carousel_type?(s.prop33="jumbotron",s.prop54="jumbotron:"+n):s.prop54="carousel:"+n}if("undefined"!=typeof e.pageURL){try{e.pageURL=e.pageURL.toLowerCase(),e.pageURL=e.pageURL.replace(/^.*\/\/[^\/]+/,""),e.pageURL=e.pageURL.replace("/index.html","/")}catch(c){}s.pageName=wminst.Util.getCNNPageName(e.pageURL)}"undefined"!=typeof e.initial_page&&1==e.initial_page?s.prop25=s.eVar25="":(s.linkTrackEvents=1==i?"event26,event67":"event5,event26",s.events=s.linkTrackEvents);var p=wminst.Util.getCNNBrandingPartner();if(""!=p&&"nvs"!=p&&"no value set"!=p&&"no-value-set"!=p&&(s.linkTrackEvents="event21,"+s.linkTrackEvents,s.events=s.linkTrackEvents),s.prop57="no mvpd set",s.prop59=s.prop57,s.prop64=wminst.Util.getCNNUIEngagement(),"ngtv"==s.prop64){s.linkTrackEvents="",s.events="",s.prop32="adbp:gallery";try{s.prop57=e.mvpd}catch(c){}try{s.prop57=e.adobe_hash_id}catch(c){}}s.list1=wminst.Util.getCNNTopic();var o=e.publish_date||"a";s.prop10=wminst.Util.getCNNDaysSinceLastPublish(o),s.prop11=wminst.Util.getCNNBrandingPartner(),s.prop44=wminst.Util.getCNNSourceID(),s.eVar44=wminst.Util.getCNNPageVertical(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID();var l=wminst.Util.gCNNUserAuthState();s.eVar51=l.user_registered_status,s.prop74=l.user_account_status,s.eVar89=l.user_login_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop75=wminst.Util.getCNNUserAuthState();try{wminst.trackPage()}catch(c){}s.clearVars()}),PubSub.subscribe("photo-page",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,channel,server,pageName,prop4,eVar4,prop6,eVar6,prop8,eVar8,eVar15,eVar22,prop23,eVar23,prop25,eVar25,prop26,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop37,eVar37,prop44,prop46,eVar46,prop47,eVar47,eVar51,prop54,eVar54,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop64,eVar64,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar89,hier1,list1,list2",s.linkTrackEvents="event26",s.channel=wminst.Util.getCNNSection(0),s.server=wminst.Util.getADBPURL("domain"),s.prop4=wminst.Util.getPageAttribution(),s.pageName=wminst.Util.getCNNPageName(),s.events=s.linkTrackEvents;var t="";try{t=window.cnn_metadata.business.cnn.page.photo_gallery}catch(a){}try{t=window.CNN.omniture.gallery_name||t}catch(a){}t&&(t=t.replace(/%20/g," ")),s.prop6=t,s.prop8=wminst.Util.getCNNVisitNumber(28),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.prop23=wminst.Util.getCNNPageHeadline(),s.prop26=wminst.Util.getCNNBaseURL(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop37=wminst.Util.getCNNPlatform(),s.prop44=wminst.Util.getCNNSourceID(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID();var r=wminst.Util.gCNNUserAuthState();if(s.eVar51=r.user_registered_status,s.prop74=r.user_account_status,s.eVar89=r.user_login_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop57="no mvpd set",s.prop59=wminst.Util.getCNNAdobeID(),s.prop64=wminst.Util.getCNNUIEngagement(),s.list1=wminst.Util.getCNNTopic(),s.prop75=wminst.Util.getCNNUserAuthState(),1==wminst.isInit)s.prop25="",wminst.isInit=!1;else{s.linkTrackEvents=null,s.events=s.linkTrackEvents,s.eVar6="";try{e.img=e.img+""}catch(a){}try{e.before=e.before+""}catch(a){}e.img?(s.prop25=e.img+"",s.linkTrackEvents="event5",s.events=s.linkTrackEvents,0):e.before&&(s.prop25=e.before+"",s.linkTrackEvents="event5",s.events=s.linkTrackEvents,0),s.prop33="other:gallery"}s.prop25=s.prop25.toLowerCase(),s.eVar1=s.eVar7=s.eVar61=s.eVar68=s.eVar71=s.eVar41="",e.title?wminst.trackLink("photo-page:"+e.title):e.caption&&wminst.trackLink("photo-page:"+e.caption),s.clearVars()}),PubSub.subscribe("ngtv-interaction",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,campaign,eVar29,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,prop46,eVar46,prop47,eVar47,prop55,eVar55,eVar57,prop59,eVar59,eVar64,prop69,eVar69,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.campaign=wminst.Util.getQueryParam("cid"),s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar32="other:interactive",s.eVar33="adbp:none";try{s.eVar34=e.auth_state}catch(t){}s.prop35=wminst.Util.getCNNCodeVersion(),s.evar36=wminst.Util.getCNNKruxID(),s.eVar37=wminst.Util.getCNNPlatform(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID();try{s.eVar57=e.mvpd}catch(t){}s.prop59=wminst.Util.getCNNAdobeID(),s.eVar64=s.prop64,s.prop64="";try{s.prop69=e.interaction}catch(t){}wminst.trackLink("ngtv-interaction:"+e.interaction),s.clearVars()}),PubSub.subscribe("user-interaction",function(e){s.manageVars("clearVars"),s.linkTrackEvents="event26",s.events=s.linkTrackEvents;var t="priceless xi"==e.branding_social?": priceless xi":"";s.prop28&&-1!=s.prop28.indexOf("electoral college map")?s.prop69=e.interaction+"_click":"undefined"!=typeof e.interaction&&"comment-click:cronkite"==e.interaction?(t="time shift: on comment",s.prop69="time shift: on comment"):"undefined"!=typeof e.interaction&&"Go-Live:cronkite"==e.interaction?(t="time shift: go live",s.prop69="time shift: go live"):"undefined"!=typeof e.interaction&&"time shift: on video"==e.interaction?(t="time shift: on video",s.prop69="time shift: on video"):"undefined"!=typeof e.interaction&&"video carousel"===e.interaction?s.prop69=e.interaction+":click":s.prop69=e.interaction;try{s.prop14=e.branding_social}catch(a){}if(s.campaign=wminst.Util.getQueryParam("cid"),s.channel=wminst.Util.getCNNSection(0),s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.eVar27="D=ch",s.prop28=wminst.Util.getCNNSection(1),s.eVar29="D=server",s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType()||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.eVar37=wminst.Util.getCNNPlatform(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop59=wminst.Util.getCNNAdobeID(),"undefined"!=typeof e.pageURL&&""!=e.pageURL){try{e.pageURL.split("/")[2].replace("www.",""),e.pageURL=e.pageURL.toLowerCase(),e.pageURL=e.pageURL.replace(/^.*\/\/[^\/]+/,""),e.pageURL=e.pageURL.replace("/index.html","/")}catch(a){}s.pageName=wminst.Util.getCNNPageName(e.pageURL)}if(typeof e.interaction==undefined||"travel:gallery:open"!=e.interaction&&"travel:gallery:viewall"!=e.interaction&&"style:gallery:open"!=e.interaction&&"style:gallery:viewall"!=e.interaction?s.linkTrackEvents=s.linkTrackEvents+",event76":s.linkTrackEvents=s.linkTrackEvents+",event30",s.events=s.linkTrackEvents,typeof e.interaction!=undefined&&"politics:submit debate topics"==e.interaction&&(s.prop69=e.interaction,t="debate topic submission"),"undefined"!=typeof s.prop69&&""!==s.prop69){s.eVar69="D=c69",-1!==s.prop69.indexOf("subscribe")?s.linkTrackVars="events,eVar69,prop69,list2":-1!==s.prop28.indexOf("electoral college map")?s.linkTrackVars="events,campaign,pageName,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2":-1!==s.prop28.indexOf("general elections 2016")?s.linkTrackVars="events,campaign,pageName,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop35,eVar35,eVar36,prop69,eVar69,list2":-1!==s.prop69.indexOf("style:menu")?s.linkTrackVars="events,campaign,pageName,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2":-1!==s.prop69.indexOf("style:gallery:open")?s.linkTrackVars="events,campaign,pageName,prop16,eVar16,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop30,eVar30,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2":s.linkTrackVars="events,campaign,pageName,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop69,eVar69,prop73,eVar73,list2";for(var r=s.events.split(","),a=0;a<=r.length;a++)"event26"!==r[a]&&"event21"!==r[a]&&"event39"!==r[a]||(r.splice(a,1),a=0);s.linkTrackEvents=r.toString(),s.events=s.linkTrackEvents}if("undefined"!=typeof e.bouncex&&""!==e.bouncex&&(s.prop62=e.bouncex.toLowerCase(),s.linkTrackEvents=s.linkTrackEvents+",event20",s.events=s.linkTrackEvents,""!==s.prop62)){for(r=s.events.split(","),a=0;a<=r.length;a++)"event26"!==r[a]&&"event39"!==r[a]&&"event76"!==r[a]&&"event21"!==r[a]||(r.splice(a,1),a=0);s.linkTrackEvents=r.toString(),s.events=s.linkTrackEvents,s.linkTrackVars="events,campaign,pageName,eVar26,server,eVar29,channel,eVar27,prop28,eVar28,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,eVar59,prop59,prop62,eVar62,eVar73,prop73,list2"}wminst.trackLink("user interaction:"+t),s.clearVars()}),PubSub.subscribe("election-click",function(e){s.manageVars("clearVars"),
s.linkTrackVars="events,server,channel,pageName,eVar13,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar50,prop51,prop69,eVar69,eVar79,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.pageURL=wminst.Util.getCNNPageURL(),s.server=wminst.Util.getADBPURL("domain"),s.eVar29="D=server",s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.prop30=wminst.Util.getSiteSpecificSettings(1),s.eVar30="D=c30";var t="undefined"!=typeof e.interaction_type?e.interaction_type:"election center:"+e.section,r="undefined"!=typeof e.interaction_type?e.interaction_type:"election center:";e.interaction_type&&(r=t=e.interaction_type),"undefined"!=typeof e.tab&&""!=e.tab&&(t=t+":"+e.tab,r+="tab click"),"undefined"!=typeof e.area&&""!=e.area&&(t=t+":"+e.area+":click",r="election center:map click"),"undefined"!=typeof e.action&&""!=e.action&&(-1!=e.action.indexOf("timeline")?(t+=":timeline",r="election center:timeline"):-1!=e.action.indexOf("expanded")&&"undefined"!=typeof e.issue&&""!=e.issue&&(t=t+":"+e.issue,r="election center:issues")),"undefined"!=typeof e.button&&""!=e.button&&(t=t+":"+e.button+":click",r="election center:"+e.button+" click");try{wminst.Util.isPoliticsExplorer()&&(s.eVar50=wminst.Util.getCNNInteractiveState(e),s.prop51=wminst.Util.getCNNSiteSectionLevel3("explorer"),s.eVar79=wminst.Util.getCNNExploreIndentify(e),r=t="year race"===e.interaction_type?"explorer:"+e.tab+":"+e.interaction_type+":"+e.electionId+":click":"explorer:"+e.tab+":"+e.interaction_type+":click"),e.interaction_type&&-1!=t.indexOf("road-to-270")&&(r=t=e.interaction_type,s.prop51=wminst.Util.getCNNSiteSectionLevel3("road-to-270"))}catch(a){}try{"undefined"==typeof CNN||"number"!=typeof CNN.saved_races||!e.interaction_type||-1==t.indexOf("ec:my election: close panel")&&-1==t.indexOf("ec:my election: open panel")||(s.eVar13="election center: save races:"+t.split(":")[3])}catch(a){}try{s.channel=e.section1||wminst.Util.getCNNSection(0),s.prop69=t.toLowerCase()}catch(i){}s.eVar27="D=channel",s.eVar69="D=c69";try{s.prop28=e.section2||wminst.Util.getCNNSection(1)}catch(i){}s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType()||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),wminst.trackLink(r.toLowerCase()),s.clearVars()}),PubSub.subscribe("election-hover",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar50,prop51,prop69,eVar69,eVar79,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.pageURL=wminst.Util.getCNNPageURL(),s.server=wminst.Util.getADBPURL("domain"),s.eVar29="D=server",s.channel=wminst.Util.getCNNSection(0),s.prop28=wminst.Util.getCNNSection(1),s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.prop30=wminst.Util.getSiteSpecificSettings(1),s.eVar30="D=c30";var t="undefined"!=typeof e.section?e.section:"",r="undefined"!=typeof e.tab?e.tab:"",a="undefined"!=typeof e.area?e.area:"",i="election center:"+t+":"+r+":"+("undefined"!=typeof e.stateCode?e.stateCode:"")+":"+a+":hover",n="election center:hover";try{"undefined"!=typeof e.tab&&"undefined"!=typeof e.map_type&&(n=(i="ec:"+e.tab+":"+e.map_type+":"+e.state+":"+(""==e.county?"nvs":e.county)+":hover").toLowerCase()),wminst.Util.isPoliticsExplorer()&&(s.eVar50=wminst.Util.getCNNInteractiveState(e),s.prop51=wminst.Util.getCNNSiteSectionLevel3("explorer"),s.eVar79=wminst.Util.getCNNExploreIndentify(e),n=(i="explorer:"+e.tab+":"+e.state+":"+(""==e.county?"nvs":e.county)+":hover").toLowerCase())}catch(p){}try{s.prop69=i.toLowerCase(),s.prop69?s.eVar69="D=c69":s.prop69=s.evar69=""}catch(o){}s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType()||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),wminst.trackLink(n),s.clearVars()}),PubSub.subscribe("quiz-interaction",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,pageName,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop69,eVar69,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName();var t=e.clickObj||{};s.prop32="other:interactive",s.prop33="other:quiz",s.prop35=wminst.Util.getCNNCodeVersion();try{s.prop69=t.action}catch(r){}try{wminst.trackLink("quiz-interaction:"+s.prop69)}catch(r){}s.clearVars()}),PubSub.subscribe("hp10-interaction",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,eVar26,eVar27,eVar29,prop35,eVar35,eVar36,prop56,eVar56,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event76",s.pageName=wminst.Util.getCNNPageName(),s.pageName="",s.channel=wminst.Util.getCNNSection(0),s.server=wminst.Util.getADBPURL("domain"),s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.eVar27=s.channel,s.channel="",s.eVar29=s.server,s.server="",s.prop35=wminst.Util.getCNNCodeVersion(),s.events=s.linkTrackEvents,s.eVar36=wminst.Util.getCNNKruxID(),s.prop56=wminst.Util.getCNNOrientation();try{s.prop69=e.interaction}catch(t){}try{wminst.trackLink("hp10-interaction:"+s.prop69)}catch(t){}s.clearVars()}),PubSub.subscribe("trackExitLink-click",function(){s.manageVars("clearVars"),s.events="event61",s.linkTrackEvents=s.events,s.linkTrackVars="events,eVar26,eVar27,eVar28,eVar29,eVar30,eVar32,eVar33,prop35,eVar35,eVar36,eVar44,prop47,eVar47",s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=wminst.Util.getCNNSection(0),s.eVar28=wminst.Util.getCNNSection(1),s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=wminst.Util.getSiteSpecificSettings(1),s.eVar32=wminst.Util.getCNNTemplateType("long"),s.eVar33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar35="D=c35",s.eVar36=wminst.Util.getCNNKruxID(),s.eVar44=wminst.Util.getCNNVertical(),s.prop47=wminst.Util.getCNNGUID(),s.eVar47="D=c47",wminst.Util.setATTWMID()}),PubSub.subscribe("readmore-click",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,pageName,eVar23,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop56,eVar56,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event76",s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.eVar23=s.prop23,s.prop23="",s.pageName=wminst.Util.getCNNPageName(),s.eVar26="D=pageName",s.eVar27=s.channel,s.channel="",s.eVar29=s.server,s.server="",s.events=s.linkTrackEvents,s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType()||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop56=wminst.Util.getCNNOrientation(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop69=e.interaction,e.interaction&&""!=e.interaction&&"facts first:click:read more"==e.interaction&&(s.linkTrackVars="events,pageName,eVar23,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop56,eVar56,prop59,eVar59,prop69,eVar69,prop73,eVar73,eVar84,eVar85,list2",s.eVar84=e.factcheck_id.toLowerCase()||"",s.eVar85=e.factcheck_headline.toLowerCase()||"")}catch(t){}try{wminst.trackLink("readmore-click:"+s.prop69),s.eVar84=s.eVar85=""}catch(t){}"undefined"!=typeof window.CNN&&"undefined"!=typeof window.CNN.omniture&&"facts first"!==window.CNN.omniture.section[1]&&window.sendInteractionEvent("readmore-page",e.interaction),s.clearVars()}),PubSub.subscribe("readmore-page",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,pageName,channel,prop2,eVar2,prop4,evar4,prop8,eVar8,eVar15,prop16,eVar16,eVar26,eVar27,prop28,eVar28,prop32,eVar32,prop33,eVar33,prop35,eVar35,prop44,eVar44,prop46,eVar46,prop47,eVar47,eVar51,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop64,eVar64,prop69,eVar69,prop73,eVar73,prop74,eVar74,prop75,eVar75,eVar89,list2",s.linkTrackEvents="event26",s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop2=wminst.Util.getCNNAuthor(),s.prop4=wminst.Util.getPageAttribution(),s.prop8=wminst.Util.getCNNVisitNumber(28),s.eVar15=wminst.Util.getCNNTrafficPartner(),s.prop28=wminst.Util.getCNNSection(1),"article"==wminst.Util.getCNNCapContentType()&&(s.linkTrackEvents=s.linkTrackEvents+",event39"),s.pageURL=wminst.Util.getCNNPageURL(),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType(),s.prop35=wminst.Util.getCNNCodeVersion(),s.prop44=wminst.Util.getCNNSourceID(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCNNGUID();var t=wminst.Util.gCNNUserAuthState();s.eVar51=t.user_registered_status,s.prop74=t.user_account_status,s.eVar89=t.user_login_status,s.prop56=wminst.Util.getCNNOrientation(),s.prop57=wminst.Util.getCNNMVPD(),s.prop59=wminst.Util.getCNNAdobeID(),s.prop64=wminst.Util.getCNNUIEngagement(),s.prop75=wminst.Util.getCNNUserAuthState(),s.eVar3=s.eVar7=s.prop11=s.eVar11=s.prop34=s.eVar34=s.eVar41=s.eVar42=s.eVar66=s.eVar67=s.eVar68=s.prop70=s.eVar70=s.eVar71="",s.events=s.linkTrackEvents;try{s.prop69=e.interaction}catch(r){}wminst.trackPage(),s.clearVars()}),PubSub.subscribe("ribbon-interaction",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event76,event72",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName(),s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.prop28=wminst.Util.getCNNSection(1),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID();var t=e.interaction;try{s.prop69=e.interaction}catch(r){}try{"string"==typeof t&&(t=t.replace(":"," ")),wminst.trackLink(t)}catch(r){}s.clearVars()}),PubSub.subscribe("site-registration_verification",function(e){PubSub.publish("site-registration",e)}),PubSub.subscribe("site-registration",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID(),"undefined"!=typeof e.action&&(-1<e.action.indexOf("account not successfully")?(s.prop69="user:"+e.action,s.linkTrackEvents="event58,event76",s.events=s.linkTrackEvents,wminst.trackLink(e.action)):-1<e.action.indexOf("account  verified")&&(s.prop69="user:"+e.action,s.linkTrackEvents="event53,event76",s.events=s.linkTrackEvents,wminst.trackLink(e.action))),s.clearVars()}),PubSub.subscribe("site_registration_success",function(){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event52,event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop69="user:account created"}catch(e){}try{wminst.trackLink("site_registration_success")}catch(e){}s.clearVars()}),PubSub.subscribe("site_login_success",function(){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,eVar89,list2",s.linkTrackEvents="event54,event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop69="user:login success"}catch(t){}var e=wminst.Util.gCNNUserAuthState();s.eVar89=e.user_login_status;try{wminst.trackLink("site_login_success")}catch(t){}s.clearVars()}),PubSub.subscribe("article-twentyfive",function(){}),PubSub.subscribe("article-fifty",function(){}),PubSub.subscribe("article-seventyfive",function(){}),PubSub.subscribe("article-complete",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event57,event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none"),s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop69="content:"+e.interaction}catch(t){}try{wminst.trackLink(e.interaction)}catch(t){}s.clearVars()}),PubSub.subscribe("click-interaction",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop59,eVar59,prop69,eVar69,prop73,eVar73,list2",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.pageName=wminst.Util.getCNNPageName(),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none")||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID(),s.prop59=wminst.Util.getCNNAdobeID();try{s.prop69=e.interaction.toLowerCase(),-1!==s.prop69.indexOf("topics:")&&"topics:overlay:closed"!==s.prop69&&"topics:topics-tray-close"!==s.prop69&&"topics:topics-tray-expand"!==s.prop69&&(s.linkTrackVars=s.linkTrackVars+",prop4,eVar4",s.prop4=wminst.Util.getPageAttribution())}catch(t){}try{wminst.trackLink(e.interaction.toLowerCase())}catch(t){}s.clearVars()}),PubSub.subscribe("sortpost-click",function(e){s.manageVars("clearVars"),s.linkTrackVars="events,server,channel,pageName,prop23,eVar23,eVar26,eVar27,prop28,eVar28,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop69,eVar69",s.linkTrackEvents="event76",s.events=s.linkTrackEvents,s.pageName=wminst.Util.getCNNPageName();try{s.prop23=e.headline.toLowerCase()||wminst.Util.getCNNPageHeadline()}catch(r){s.prop23=wminst.Util.getCNNPageHeadline()}s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.prop28=wminst.Util.getCNNSection(1),s.prop30=wminst.Util.getSiteSpecificSettings(1),s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop33=wminst.Util.getCNNContentType("adbp:none")||"adbp:none",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar36=wminst.Util.getCNNKruxID();try{s.prop69=e.interaction}catch(r){}try{var t=e.interaction;"string"==typeof t&&(t=t.replace(": "," ")),wminst.trackLink(t)}catch(r){}s.clearVars()}),wminst.subscribersReady=!0;
});
_satellite["_runScript13"](function(event, target, Promise) {
wminst.isAudioInitiated=!1,wminst.setAudioInterval_id=0,wminst.liveAudioInterval=0,wminst.trackLinkAudio=function(e,t){wminst.Util.setATTWMID(),s.tl(this,"o",e+": "+t.title.toLowerCase())},wminst.audioCommonData=function(e){var t,a,i="audio";try{a="aod","undefined"==typeof(t=e||{}).isLive||!t.isLive&&"true"!=t.isLive||(a="live"),s.trackingServer=wminst.Util.getSiteSpecificSettings(3),s.trackingServerSecure=wminst.Util.getSiteSpecificSettings(4),s.account=_satellite.getVar("RSID"),s.prop1=t.type,t.author&&""!==t.author&&(s.prop2=t.author.toLowerCase()),s.prop7=t.length+"",s.eVar7="D=c7",t.title&&""!==t.title&&(s.prop29=t.title.toLowerCase(),s.eVar41="D=c29"),s.eVar33="adbp:audio",s.prop33="",s.prop35=wminst.Util.getCNNCodeVersion(),s.eVar42=t.id,s.eVar45=t.playlist_position+"",s.prop45="",s.eVar54=i+"|"+a+"|"+t.type,s.prop54="",s.eVar67=t.state+"|"+(t.status?t.status:"no value set")+"|"+(t.position?t.position:"inline"),s.prop67="",s.eVar82=t.rate+"",s.prop82=""}catch(r){}},PubSub.subscribe("audio-preroll",function(e){s.manageVars("clearVars");var t=e.audio.audio||{};s.linkTrackVars="events,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.events="event91,event92",s.linkTrackEvents=s.events,wminst.isAudioInitiated=!0,wminst.audioCommonData(t),wminst.trackLinkAudio("audio-preroll",t);try{wminst.setAudioInterval_id=setInterval(function(){window.trackAudioProgress(e)},6e4)}catch(a){}s.clearVars()}),PubSub.subscribe("audio-start",function(e){s.manageVars("clearVars");var t=e.audio.audio||{},a=new wminst.getCNNMediaCollection;a.start(t.id,t.title),s.linkTrackVars="events,products,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.events="event11",wminst.audioCommonData(t),wminst.isAudioInitiated||(s.events+=",event92"),s.prop7&&null!==s.prop7&&(s.events=s.events+",event64",s.products=";;;;event64="+s.prop7),s.linkTrackEvents=s.events,wminst.trackLinkAudio("audio-start",t),wminst.isAudioInitiated=!1,a.set(t.id,"audStarted",!0),wminst.setAudioInterval_id&&clearInterval(wminst.setAudioInterval_id),wminst.setAudioInterval_id=setInterval(function(){window.trackAudioProgress(e)},6e4),s.clearVars()}),PubSub.subscribe("audio-autostart",function(e){s.manageVars("clearVars");var t=e.audio.audio||{},a=new wminst.getCNNMediaCollection;a.start(t.id,t.title),s.linkTrackVars="events,products,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.events="event11",wminst.audioCommonData(t),wminst.isAudioInitiated||(s.events+=",event92"),s.prop7&&null!==s.prop7&&(s.events=s.events+",event64",s.products=";;;;event64="+s.prop7),s.linkTrackEvents=s.events,wminst.trackLinkAudio("audio-autostart",t),wminst.isAudioInitiated=!1,a.set(t.id,"audStarted",!0),wminst.setAudioInterval_id&&clearInterval(wminst.setAudioInterval_id),wminst.setAudioInterval_id=setInterval(function(){window.trackAudioProgress(e)},6e4),s.clearVars()}),PubSub.subscribe("audio-complete",function(e){s.manageVars("clearVars");var t=e.audio.audio||{},a=new wminst.getCNNMediaCollection,i=a.complete(t.id);s.linkTrackVars="events,products,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.linkTrackEvents="event97,event98",s.events=s.linkTrackEvents,wminst.audioCommonData(t),0<i&&(s.products=";;;;event98="+i),wminst.setAudioInterval_id&&clearInterval(wminst.setAudioInterval_id),wminst.trackLinkAudio("audio-complete",t),a.set(t.id,"audStarted",!1),a.set(t.id,"hasScrubbed",!1),a.set(t.id,"isPaused",!1),a.set(t.id,"isBuffering",!1),a.set(t.id,"isHalf",!1),a.set(t.id,"isTen",!1),a.set(t.id,"isTwentyFive",!1),a.set(t.id,"isSeventyFive",!1),s.clearVars()}),PubSub.subscribe("audio-pause",function(e){var t=e.audio.audio||{},a="undefined"!=typeof t.pause&&t.pause,i=new wminst.getCNNMediaCollection;i.get(t.id,"audStarted")&&(s.manageVars("clearVars"),s.linkTrackVars="events,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.events="event100",a&&(s.events="event99"),s.linkTrackEvents=s.events,wminst.audioCommonData(t),wminst.trackLinkAudio(a?"audio-pause":"audio-resume",t));var r=i.get(t.id,"isPaused");a!=r&&(i.pause(t.id),wminst.setAudioInterval_id&&clearInterval(wminst.setAudioInterval_id),r&&(wminst.setAudioInterval_id=setInterval(function(){window.trackAudioProgress(e)},6e4))),s.manageVars("clearVars")}),PubSub.subscribe("audio-buffer",function(e){var t=e.audio.audio||{},a="undefined"!=typeof t.buffering&&t.buffering,i=new wminst.getCNNMediaCollection,s=i.get(t.id,"isBuffering");a!=s&&(i.buffer(t.id),wminst.setAudioInterval_id&&clearInterval(wminst.setAudioInterval_id),s&&(wminst.setAudioInterval_id=setInterval(function(){window.trackAudioProgress(e)},6e4)))}),PubSub.subscribe("audio-scrub",function(e){var t=e.audio.audio||{};(new wminst.getCNNMediaCollection).set(t.id,"hasScrubbed",!0)}),PubSub.subscribe("audio-progress",function(e){var t=e.audio.audio||{},a=new wminst.getCNNMediaCollection;s.linkTrackVars="events,products,prop1,eVar1,prop2,eVar2,prop7,eVar7,prop29,eVar33,prop35,eVar35,eVar41,eVar42,eVar45,eVar54,eVar67,eVar82",s.events="event98",s.linkTrackEvents=s.events,wminst.audioCommonData(t);var i=a.progress(t.id);60<i&&(wminst.liveAudioInterval=60),0<(i=wminst.capCNNTimeSpent(i,t.length,wminst.liveAudioInterval))&&(s.products=";;;;event98="+i),60==i&&wminst.trackLinkAudio("audio-progress",t),s.manageVars("clearVars")});
});
_satellite["_runScript14"](function(event, target, Promise) {
wminst.videoData={},wminst.videoData.timeSpent=0,wminst.isVideoCompleted=!1,wminst.isLiveVid=!1,wminst.live_interval=0,wminst.setinterval_id=0,wminst.isAd=!1,wminst.adVidId="",wminst.adRange="",wminst.is_dvr=!1,wminst.is_autoplay=!1,wminst.isLivePaused=!1,wminst.isGoogleAmp="",wminst.standardVideoMetadata={},wminst.is_preroll_occur=!1,wminst.intervalID||(wminst.intervalID=0);var progTime=0;wminst.trackLinkVideo=function(e,r){wminst.Util.setATTWMID(),s.tl(this,"o",e+":"+(r.title?r.title:r.headline).toLowerCase())},wminst.trackMoneyVideoEvent=function(e,r){s.origRSID=s.account,s.origLTV=s.linkTrackVars,s.origPageName=s.pageName,s.sa("aolturnercnnmoney-adbp-offsite"),s.referrer=document.referrer,s.pageName="",s.prop1="Video",s.prop2=s.channel;r.source&&r.source.toUpperCase(),s.prop8=r.branding||"nvs",s.prop11=r.series||"nvs",s.prop15=window.location.href.toLowerCase(),s.eVar15="",s.prop16="cnn player",s.prop23="domestic",s.origRSID&&-1!=s.origRSID.indexOf("cnn-adbp-intl")&&(s.prop23="international"),s.prop30="cnnmoney",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.list1=wminst.Util.getCEPTopisForVideo(r)||wminst.Util.getCNNTopic();var p=e;switch(e){case"preroll":"google amp"==wminst.isGoogleAmp?(s.timestamp="",s.linkTrackVars="campaign,prop14,eVar14,prop23,eVar23,eVar41,eVar42,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,list2"):s.linkTrackVars="campaign,list1,prop23,eVar23,eVar41,eVar42,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,list2",wminst.isGoogleAmp="",s.linkTrackEvents="event35";break;case"start":"google amp"==wminst.isGoogleAmp?(s.timestamp="",s.linkTrackVars="campaign,prop1,eVar1,prop2,eVar2,prop8,eVar8,prop11,eVar11,prop14,eVar14,prop15,eVar15,prop16,eVar16,prop23,eVar23,eVar27,prop28,eVar28,prop29,eVar41,server,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar42,prop46,eVar46,prop47,eVar47,events,list2"):s.linkTrackVars="campaign,list1,prop1,eVar1,prop2,eVar2,prop8,eVar8,prop11,eVar11,prop15,eVar15,prop16,eVar16,prop23,eVar23,eVar27,prop28,eVar28,prop29,eVar41,server,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar42,prop46,eVar46,prop47,eVar47,events,list2",wminst.isGoogleAmp="",s.linkTrackEvents="event32",s.prop33="adbp:video start";break;case"autostart":"google amp"==wminst.isGoogleAmp?(s.timestamp="",s.linkTrackVars="campaign,prop1,eVar1,prop2,eVar2,prop8,eVar8,prop11,eVar11,prop14,eVar14,prop15,eVar15,prop16,eVar16,prop23,eVar23,eVar27,prop28,eVar28,prop29,eVar41,server,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar42,prop46,eVar46,prop47,eVar47,events,list2"):s.linkTrackVars="campaign,list1,prop1,eVar1,prop2,eVar2,prop8,eVar8,prop11,eVar11,prop15,eVar15,prop16,eVar16,prop23,eVar23,eVar27,prop28,eVar28,prop29,eVar41,server,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar42,prop46,eVar46,prop47,eVar47,events,list2",wminst.isGoogleAmp="",s.linkTrackEvents="event32,event34",s.prop33="adbp:video start";break;case"fifty":"google amp"==wminst.isGoogleAmp?(s.timestamp="",s.linkTrackVars="campaign,prop1,eVar1,prop2,eVar2,prop14,eVar14,prop23,eVar23,eVar27,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,products,list2"):s.linkTrackVars="campaign,list1,prop1,eVar1,prop2,eVar2,prop23,eVar23,eVar27,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,products,list2",wminst.isGoogleAmp="",s.linkTrackEvents="event29,event36",p="midpoint";break;case"complete":"google amp"==wminst.isGoogleAmp?(s.timestamp="",s.linkTrackVars="campaign,prop1,eVar1,prop2,eVar2,prop23,prop14,eVar14,eVar23,eVar27,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,products,list2"):s.linkTrackVars="campaign,list1,prop1,eVar1,prop2,eVar2,prop23,eVar23,eVar27,prop35,eVar35,prop46,eVar46,prop47,eVar47,events,products,list2",wminst.isGoogleAmp="",s.linkTrackEvents="event33,event36"}s.events=s.linkTrackEvents,wminst.trackLinkVideo("cnnvideo-"+p,r),s.sa(s.origRSID),s.linkTrackVars=s.origLTV,s.pageName=s.origPageName},PubSub.subscribe("cnnvideo-preroll",function(e){wminst.isAd=!0;var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r),wminst.adVidId=r.id,s.linkTrackVars="events,server,channel,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,eVar26,eVar27,eVar28,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar41,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop49,eVar49,prop50,eVar52,eVar53,eVar54,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event35",s.events="event35","string"==typeof r.adType&&"midroll"==r.adType.toLowerCase()&&(s.linkTrackEvents="event25",s.events="event25"),"string"==typeof r.adType&&"preroll"==r.adType.toLowerCase()&&(s.linkTrackEvents=s.linkTrackEvents+",event90",s.events=s.linkTrackEvents,wminst.is_preroll_occur=!0),(r.category&&"live"!==r.category||"true"!==r.isLive||!0!==r.isLive)&&(wminst.isLiveVid=!1),wminst.standardVideoMetadata.isCNNGo?s.eVar72=r.free_preview:s.eVar72="",("undefined"!=typeof r.is_autoplay_allowed&&!0===r.is_autoplay_allowed||"undefined"!=typeof r.isAutoStart&&!0===r.isAutoStart)&&(wminst.is_autoplay=!0,"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart"))),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.prop4?(s.eVar4=s.prop4,s.prop4=""):s.eVar4="",s.eVar7=s.prop7,s.prop7="",s.prop8?(s.eVar8=s.prop8,s.prop8=""):s.eVar8=wminst.Util.getCNNVisitNumber(28),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar16=s.prop16,s.prop16="",s.eVar23=s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.prop30="",s.eVar32=s.prop32,s.prop32="",s.eVar33=s.prop33,s.prop33="",s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.eVar41=s.prop29,s.prop29="",s.eVar52=s.prop52,s.prop52="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.eVar57=s.prop57,s.prop57="",s.eVar60=s.prop60,s.prop60="",s.prop64?(s.eVar64=s.prop64,s.prop64=""):s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop43||(s.prop50=""),s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",1!=wminst.isLiveVid&&1!=r.isLive&&"true"!=r.isLive||r.adType&&"midroll"==r.adType.toLowerCase()&&wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.isMoneyVideo(r)?wminst.trackMoneyVideoEvent("preroll",r):(s.eVar14=s.prop14,s.prop14="",wminst.trackLinkVideo("cnnvideo-"+r.adType.toLowerCase(),r));try{r.content_type1&&"tve"==r.content_type1&&(wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4))}catch(p){}s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-adcomplete",function(e){var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,prop35,eVar35,prop44",s.linkTrackEvents="event50",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),("midroll"==r.adType.toLowerCase()||1==wminst.isLiveVid&&"preroll"==r.adType.toLowerCase())&&(!r.player_type||"tve"!=r.player_type&&"live player"!=r.player_type&&"true"!=r.isLive||(s.prop33="adbp:none",wminst.trackLinkVideo("cnnvideo-adcomplete",r)),(r.content_type1&&"tve"==r.content_type1||!0===r.isLive||"true"==r.isLive)&&(wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4))),wminst.isAd=!1,s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-midroll-complete",function(e){var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,prop35,eVar35,prop44",s.linkTrackEvents="event50",s.events="event50",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),("midroll"==r.adType.toLowerCase()||1==wminst.isLiveVid&&"preroll"==r.adType.toLowerCase())&&(!r.player_type||"tve"!=r.player_type&&"live player"!=r.player_type&&"true"!=r.isLive&&!0!==r.isLive||(s.prop33="adbp:none",wminst.trackLinkVideo("cnnvideo-adcomplete",r))),wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4),wminst.isAd=!1,s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-start",function(e){wminst.isAd=!1,wminst.isLiveVid=!1;var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r);var p=wminst.Util.isVideoAutoStarted(r),a="cnnvideo-start";s.linkTrackVars="events,server,channel,prop1,eVar1,prop3,eVar3,prop4,eVar4,prop7,eVar7,prop8,eVar8,prop10,eVar10,prop11,eVar11,prop14,eVar14,prop16,eVar16,prop20,eVar20,eVar21,eVar22,eVar23,eVar26,eVar27,eVar28,prop29,eVar29,prop30,eVar30,prop31,eVar31,prop32,eVar32,prop33,eVar33,prop34,eVar34,prop35,eVar35,eVar36,prop37,eVar37,eVar41,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop49,eVar49,prop50,prop52,eVar52,prop54,eVar54,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop60,eVar60,eVar61,prop64,eVar64,eVar54,prop66,eVar66,eVar67,prop68,eVar68,prop70,eVar70,prop71,eVar71,prop72,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",!0===p?(s.linkTrackEvents="event32,event34",s.events="event32,event34",a="cnnvideo-autostart",wminst.is_autoplay=!0,"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart"))):(s.linkTrackEvents="event32",s.events="event32"),r.subcategory,r.subcategory&&""!=r.subcategory&&(s.linkTrackEvents="event23,"+s.linkTrackEvents,s.events=s.linkTrackEvents),"undefined"!=typeof r.metas&&r.metas.branding&&""!=r.metas.branding&&(s.linkTrackEvents="event22,"+s.linkTrackEvents,s.events=s.linkTrackEvents),wminst.adVidId==r.id&&0<wminst.adRange&&(s.linkTrackEvents="event3,"+s.linkTrackEvents,s.events=s.linkTrackEvents,wminst.adVidId=""),wminst.is_preroll_occur||(s.linkTrackEvents=s.linkTrackEvents+",event90",s.events=s.linkTrackEvents);var t=new wminst.getCNNMediaCollection;t.start(r.playerid,r.title?r.title:r.headline),wminst.standardVideoMetadata.isCNNGo?(s.prop72=r.free_preview,s.eVar72="D=c72"):s.prop72=s.eVar72="",s.prop4?s.eVar4="D=c4":s.eVar4="",s.eVar21=wminst.Util.getCNNVideoSequence(),s.eVar23=s.prop23,s.prop23="",s.prop28&&(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""),s.prop31?s.prop31=s.prop31.toLowerCase():s.eVar31="",s.prop33&&(s.eVar33="D=c33"),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar60=s.prop60,s.prop60="",s.prop64="",s.eVar64=wminst.Util.getCNNUIEngagement(),wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.isMoneyVideo(r)?wminst.trackMoneyVideoEvent("start",r):(wminst.trackLinkVideo(a,r),t.set(r.playerid,"vidStarted",!0)),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-autostart",function(e){wminst.isAd=!1,wminst.isLiveVid=!1;var r="cnnvideo-autostart",p=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(p);var a=wminst.Util.isVideoAutoStarted(p);!(s.linkTrackVars="events,server,channel,prop1,eVar1,prop3,eVar3,prop4,eVar4,prop7,eVar7,prop8,eVar8,prop10,eVar10,prop11,eVar11,prop14,eVar14,prop16,eVar16,prop20,eVar20,prop21,eVar21,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,prop29,eVar29,prop30,eVar30,prop31,eVar31,prop32,eVar32,prop33,eVar33,prop34,eVar34,prop35,eVar35,eVar36,prop37,eVar37,eVar41,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop49,eVar49,prop50,prop52,eVar52,prop54,eVar54,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop60,eVar60,eVar61,prop64,eVar64,prop66,eVar66,eVar67,prop68,eVar68,prop70,eVar70,prop71,eVar71,prop72,eVar72,prop73,eVar73,prop75,eVar75,list1,list2")===a?(s.linkTrackEvents="event32",s.events="event32",r="cnnvideo-start"):(s.linkTrackEvents="event32,event34",s.events="event32,event34",wminst.is_autoplay=!0,"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart"))),p.subcategory,p.subcategory&&""!=p.subcategory&&(s.linkTrackEvents="event23,"+s.linkTrackEvents,s.events=s.linkTrackEvents),"undefined"!=typeof p.metas&&p.metas.branding&&""!=p.metas.branding&&(s.linkTrackEvents="event22,"+s.linkTrackEvents,s.events=s.linkTrackEvents),wminst.adVidId==p.id&&0<wminst.adRange&&(s.linkTrackEvents="event3,"+s.linkTrackEvents,s.events=s.linkTrackEvents,wminst.adVidId=""),wminst.is_preroll_occur||(s.linkTrackEvents=s.linkTrackEvents+",event90",s.events=s.linkTrackEvents);var t=new wminst.getCNNMediaCollection;t.start(p.playerid,p.title?p.title:p.headline),s.prop4?s.eVar4="D=c4":s.eVar4="",s.prop21="",s.eVar23=e.headline,s.prop23="",s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar60="D=c60",s.prop64="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.eVar21=wminst.Util.getCNNVideoSequence(),wminst.standardVideoMetadata.isCNNgo?(s.prop72=p.free_preview,s.eVar72="D=c72"):s.prop72=s.eVar72="",s.eVar23=s.prop23="",s.prop31?s.prop31=s.prop31.toLowerCase():s.eVar31="",s.prop33&&(s.eVar33="D=c33"),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),t.set(p.playerid,"vidStarted",!0),wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.isMoneyVideo(p)?wminst.trackMoneyVideoEvent("autostart",p):wminst.trackLinkVideo(r,p),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-live",function(e){wminst.isAd=!1,wminst.isLiveVid=!0,wminst.is_dvr=!1;var r=wminst.Util.getVideoMetadata(e);s.linkTrackVars="events,server,channel,prop1,eVar1,prop3,eVar3,prop4,eVar4,prop7,eVar7,prop8,eVar8,prop14,evar14,prop20,eVar20,evar21,eVar22,eVar26,eVar27,eVar28,prop29,eVar29,prop30,eVar30,prop31,eVar31,prop32,eVar32,prop33,eVar33,prop34,eVar34,prop35,eVar35,eVar36,prop37,eVar37,eVar41,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,prop52,eVar52,prop54,eVar54,prop56,eVar56,prop57,eVar57,prop59,eVar59,prop64,prop66,eVar66,eVar67,prop68,eVar68,prop70,eVar70,prop71,eVar71,prop72,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event1,event32",s.events="event1,event32",wminst.videoCommonFunction.videoCommonData(r);var p=new wminst.getCNNMediaCollection;if(p.start(r.playerid,r.title?r.title:r.headline),"undefined"!=typeof r.is_autoplay_allowed&&"undefined"!=typeof r.isAutoStart&&!0===r.is_autoplay_allowed&&!0===r.isAutoStart&&(wminst.is_autoplay=!0,"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart"))),r.content_type2);else try{"undefined"!=typeof r.isAutoStart&&1==r.isAutoStart&&(!0===r.isAutoplayAllowed&&!1!==isAutostartSuccessful||!0===r.is_autoplay_allowed&&!1!==r.is_autoplay_successful)&&(s.linkTrackEvents=s.linkTrackEvents+",event34",s.events=s.linkTrackEvents)}catch(t){}wminst.is_preroll_occur||(s.linkTrackEvents=s.linkTrackEvents+",event90",s.events=s.linkTrackEvents),s.server=wminst.Util.getADBPURL("domain"),s.prop31?s.prop31=s.prop31.toLowerCase():s.eVar31="";try{if("undefined"!=typeof window.CNN.omniture.user_auth_state){var a=r.user_auth_state?r.user_auth_state:window.CNN.omniture.user_auth_state;s.prop75=a}else"undefined"==typeof r.mvpd||"temppass_cnn10min"!=r.mvpd&&"TempPass_CNN10min"!=r.mvpd||(s.prop75="new_temppass_go")}catch(t){}"undefined"!=typeof wminst.adVidId&&wminst.adVidId==r.id&&0<wminst.adRange&&(s.linkTrackEvents=s.linkTrackEvents+",event3",s.events=s.linkTrackEvents,wminst.adVidId=""),s.eVar23=s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.prop43||(s.prop50=""),"undefined"==typeof r.isLive||1!=r.isLive&&"true"!=r.isLive||(wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4)),wminst.standardVideoMetadata.isCNNGo?s.prop72=r.free_preview:s.prop72=s.eVar72="",wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.trackLinkVideo("cnnvideo-live",r),p.set(r.playerid,"vidStarted",!0),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-episode",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,eVar26,eVar27,eVar28,prop35,eVar35,list2",s.linkTrackEvents="event48",s.events="event48",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion());var p=new wminst.getCNNMediaCollection;p.start(r.playerid,r.title?r.title:r.headline),wminst.trackLinkVideo("cnnvideo-episode",r),p.set(r.playerid,"vidStarted",!0),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-autosegment",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,eVar26,eVar27,eVar28,prop35,eVar35,list2",s.linkTrackEvents="event65",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion());var p=new wminst.getCNNMediaCollection;p.start(r.playerid,r.title?r.title:r.headline),wminst.trackLinkVideo("cnnvideo-autosegment",r),p.set(r.playerid,"vidStarted",!0),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-pause",function(e){var r=wminst.Util.getVideoMetadata(e),p="undefined"!=typeof r.paused&&r.paused,a=new wminst.getCNNMediaCollection,t=a.get(r.playerid,"isPaused");p!=t&&(a.pause(r.playerid),1!=wminst.isLiveVid&&1!=r.isLive&&"true"!=r.isLive||(wminst.isLivePaused=p,wminst.setinterval_id&&clearInterval(wminst.setinterval_id),t&&(wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4)))),wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,list1,prop1,eVar1,prop3,eVar3,prop7,eVar7,prop8,eVar8,prop10,eVar10,prop11,eVar11,prop14,eVar14,prop16,eVar16,eVar26,eVar27,eVar28,prop29,eVar29,prop30,eVar30,prop32,eVar32,prop33,eVar33,prop35,eVar35,eVar36,prop37,eVar37,eVar41,eVar42,prop44,prop46,eVar46,prop47,eVar47,prop52,eVar52,prop54,eVar54,prop56,eVar56,eVar67,prop68,eVar68,prop70,eVar70,eVar196,eVar197",s.prop1&&(s.eVar1=s.prop1,s.prop1=""),s.prop3&&(s.eVar3=s.prop3,s.prop3=""),s.prop7&&(s.eVar7=s.prop7,s.prop7=""),s.prop8?(s.eVar8=s.prop8,s.prop8=""):s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop10?(s.eVar10=s.prop10,s.prop10=""):s.eVar10=wminst.Util.getCNNDaysSinceLastPublish("a"),s.prop11?(s.eVar11=s.prop11,s.prop11=""):s.eVar11=wminst.Util.getCNNBrandingPartner(),s.prop14?(s.eVar14=s.prop14,s.prop14=""):s.eVar14=wminst.Util.getCNNBrandingSocial(),s.prop16?(s.eVar16=s.prop16,s.prop16=""):s.eVar16=wminst.Util.getCNNPublishDate(),s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.prop28?(s.eVar28=s.prop28,s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.prop30?(s.eVar30=s.prop30,s.prop30=""):s.eVar30=wminst.Util.getSiteSpecificSettings(1),s.prop32?(s.eVar32=s.prop32,s.prop32=""):s.eVar32=wminst.Util.getCNNTemplateType("long"),s.prop33?(s.eVar33=s.prop33,s.prop33=""):s.eVar33=wminst.Util.getCNNContentType("adbp:none"),s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.prop37?(s.eVar37=s.prop37,s.prop37=""):s.eVar37=wminst.Util.getCNNPlatform(),s.prop29&&(s.eVar41=s.prop29,s.prop29=""),s.prop52&&(s.eVar52=s.prop52,s.prop52=""),s.prop54&&(s.eVar54=s.prop54,s.prop54=""),s.list1||(s.list1=wminst.Util.getCEPTopisForVideo(r)||wminst.Util.getCNNTopic());try{s.eVar22=s.prop23=s.eVar23=s.prop31=s.eVar31=s.prop34=s.eVar34=s.prop59=s.eVar59=s.prop64=s.list2=s.prop66=s.eVar66=s.prop71=s.eVar71=s.prop72=s.eVar72=s.prop73=s.eVar73=s.prop75=s.eVar75=""}catch(i){}s.prop68&&(s.eVar68=s.prop68,s.prop68=""),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.prop70&&(s.eVar70=s.prop70,s.prop70="");var o="";"true"==p||1==p?(s.linkTrackEvents="event55",o="pause"):"false"!=p&&0!=p||(s.linkTrackEvents="event56",o="resume"),s.events=s.linkTrackEvents,wminst.isMoneyVideo(r)||wminst.trackLinkVideo("cnnvideo-"+o,r),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-buffer",function(e){var r=wminst.Util.getVideoMetadata(e),s="undefined"!=typeof r.buffering&&r.buffering,p=new wminst.getCNNMediaCollection,a=p.get(r.playerid,"isBuffering");s!=a&&(p.buffer(r.playerid),1!=wminst.isLiveVid&&1!=r.isLive&&"true"!=r.isLive||(wminst.setinterval_id&&clearInterval(wminst.setinterval_id),a&&(wminst.setinterval_id=setInterval(function(){window.trackVideoProgress(r)},6e4))))}),PubSub.subscribe("cnnvideo-scrub",function(e){var r=wminst.Util.getVideoMetadata(e);(new wminst.getCNNMediaCollection).set(r.playerid,"hasScrubbed",!0),wminst.is_dvr=!0}),PubSub.subscribe("cnnvideo-progress",function(e){var r=wminst.Util.getVideoMetadata(e);wminst.videoCommonFunction.videoCommonData(r);var p=(new wminst.getCNNMediaCollection).progress(r.playerid);wminst.live_interval=60,p=wminst.capCNNTimeSpent(p,r.trt,wminst.live_interval),s.linkTrackVars="events,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar14,eVar20,eVar21,eVar26,eVar27,eVar28,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar41,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,prop64,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event36",s.events="event36",s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.prop8?(s.eVar8=s.prop8,s.prop8=""):s.eVar8=wminst.Util.getCNNVisitNumber(28),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar14=s.prop14,s.prop14="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23="",s.channel?(s.eVar27=s.channel,s.channel=""):s.eVar27=wminst.Util.getCNNSection(0),s.eVar28=wminst.Util.getCNNSection(1),s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.prop32?s.eVar32=s.prop32:s.eVar32=wminst.Util.getCNNTemplateType(),s.prop32="",s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.eVar57=s.prop57,s.prop57="",s.eVar64=s.prop64,s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="",s.products=";;;;"+s.events+"="+p,wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),60!=p||wminst.isLivePaused||wminst.trackLinkVideo("cnnvideo-progress",r),s.manageVars("clearVars")}),PubSub.subscribe("cnnvideo-ten",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e);if(!wminst.isMoneyVideo(r)){var p=new wminst.getCNNMediaCollection;if(!p.get(r.playerid,"isTen")&&!p.get(r.playerid,"hasScrubbed")){p.set(r.playerid,"isTen",!0);var a=p.progress(r.playerid);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,eVar41,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event40",s.events="event40",s.products="",0<(a=wminst.capCNNTimeSpent(a,r.trt,wminst.live_interval))&&(s.linkTrackEvents="event40,event36",s.events="event40,event36",s.products=";;;;event36="+a),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.prop8&&(s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop8=""),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar14=s.prop14,s.prop14="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23,s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=s.channel,s.channel="",s.prop28?(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""):s.eVar28=wminst.Util.getCNNSection(1),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.eVar32=s.prop32,s.prop32="",s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar56=s.prop56,s.prop56="",s.eVar54=s.prop54,s.prop54="",s.prop57&&(s.eVar57=s.prop57,s.prop57=""),s.eVar60=s.prop60,s.prop60="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="",wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.trackLinkVideo("cnnvideo-ten",r),s.manageVars("clearVars")}}}),PubSub.subscribe("cnnvideo-twentyfive",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e);if(!wminst.isMoneyVideo(r)){var p=new wminst.getCNNMediaCollection;if(!p.get(r.playerid,"isTwentyFive")&&!p.get(r.playerid,"hasScrubbed")){p.set(r.playerid,"isTwentyFive",!0);var a=p.progress(r.playerid);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,eVar41,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event41",s.events="event41",s.products="",0<(a=wminst.capCNNTimeSpent(a,r.trt,wminst.live_interval))&&(s.linkTrackEvents="event41,event36",s.events="event41,event36",s.products=";;;;event36="+a),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.prop8&&(s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop8=""),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar14=s.prop14,s.prop14="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23,s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=s.channel,s.channel="",s.prop28&&(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.eVar32=s.prop32,s.prop32="",s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.prop57&&(s.eVar57=s.prop57,s.prop57=""),s.eVar60=s.prop60,s.prop60="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="",wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.trackLinkVideo("cnnvideo-twentyfive",r),s.manageVars("clearVars")}}}),PubSub.subscribe("cnnvideo-fifty",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e),p=new wminst.getCNNMediaCollection;if(!p.get(r.playerid,"isHalf")&&!p.get(r.playerid,"hasScrubbed")){p.set(r.playerid,"isHalf",!0);var a=p.progress(r.playerid);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,eVar41,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event2",s.events="event2",s.products="",0<(a=wminst.capCNNTimeSpent(a,r.trt,wminst.live_interval))&&(s.linkTrackEvents="event2,event36",s.events="event2,event36",s.products=";;;;event36="+a),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.prop8&&(s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop8=""),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23,s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=s.channel,s.channel="",s.prop28&&(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.eVar32=s.prop32,s.prop32="",s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.prop57&&(s.eVar57=s.prop57,s.prop57=""),s.eVar60=s.prop60,s.prop60="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="",wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.isMoneyVideo(r)?wminst.trackMoneyVideoEvent("fifty",r):(s.eVar14=s.prop14,s.prop14="",wminst.trackLinkVideo("cnnvideo-fifty",r)),s.manageVars("clearVars")}}),PubSub.subscribe("cnnvideo-seventyfive",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e);if(!wminst.isMoneyVideo(r)){var p=new wminst.getCNNMediaCollection;if(!p.get(r.playerid,"isSeventyFive")&&!p.get(r.playerid,"hasScrubbed")){p.set(r.playerid,"isSeventyFive",!0);var a=p.progress(r.playerid);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,eVar41,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event42",s.events="event42",s.products="",0<(
a=wminst.capCNNTimeSpent(a,r.trt,wminst.live_interval))&&(s.linkTrackEvents="event42,event36",s.events="event42,event36",s.products=";;;;event36="+a),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.prop8&&(s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop8=""),s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar14=s.prop14,s.prop14="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23,s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=s.channel,s.channel="",s.prop28&&(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.eVar32=s.prop32,s.prop32="",s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.prop57&&(s.eVar57=s.prop57,s.prop57=""),s.eVar60=s.prop60,s.prop60="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="",wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.trackLinkVideo("cnnvideo-seventyfive",r),s.manageVars("clearVars")}}}),PubSub.subscribe("cnnvideo-complete",function(e){wminst.isAd=!1;var r=wminst.Util.getVideoMetadata(e),p=new wminst.getCNNMediaCollection,a=p.complete(r.playerid);wminst.videoCommonFunction.videoCommonData(r),s.linkTrackVars="events,server,channel,products,eVar1,eVar3,eVar4,eVar7,eVar8,eVar10,eVar11,eVar14,eVar16,eVar20,eVar22,prop23,eVar23,eVar26,eVar27,eVar28,eVar41,eVar29,eVar30,prop31,eVar31,eVar32,eVar33,eVar34,prop35,eVar35,eVar36,eVar37,eVar42,prop43,prop44,prop46,eVar46,prop47,eVar47,prop50,eVar52,eVar53,eVar54,prop56,eVar56,eVar57,prop59,eVar59,eVar60,eVar64,eVar66,eVar67,eVar68,eVar70,eVar71,eVar72,prop73,eVar73,prop75,eVar75,list1,list2",s.linkTrackEvents="event33",s.events="event33",a=wminst.capCNNTimeSpent(a,r.trt,wminst.live_interval),s.products="",0<a&&(s.linkTrackEvents="event33,event36",s.events="event33,event36",s.products=";;;;event36="+a),!0===wminst.is_autoplay&&"string"==typeof s.prop70&&""!==s.prop70&&(s.prop70=s.prop70.replace("noautostart","autostart")),s.eVar1=s.prop1,s.prop1="",s.eVar3=s.prop3,s.prop3="",s.eVar4=s.prop4,s.prop4="",s.eVar7=s.prop7,s.prop7="",s.eVar8=wminst.Util.getCNNVisitNumber(28),s.prop8="",s.eVar10=s.prop10,s.prop10="",s.eVar11=s.prop11,s.prop11="",s.eVar16=s.prop16,s.prop16="",s.eVar20=s.prop20,s.prop20="",s.eVar23=s.prop23,s.prop23="",s.pageName?(s.eVar26=s.pageName,s.pageName=""):s.eVar26=wminst.Util.getCNNPageName(),s.eVar27=s.channel,s.channel="",s.prop28&&(s.eVar28=wminst.Util.getCNNSection(1),s.prop28=""),s.server?(s.eVar29=s.server,s.server=""):s.eVar29=wminst.Util.getADBPURL("domain"),s.eVar30=s.prop30,s.prop30="",s.eVar41=s.prop29,s.prop31?(s.eVar31=s.prop31.toLowerCase(),s.prop31=""):s.eVar31="",s.prop32&&(s.eVar32=s.prop32,s.prop32=""),s.prop33&&(s.eVar33=s.prop33,s.prop33=""),s.eVar34=s.prop34,s.prop34="",s.prop35||(s.prop35=wminst.Util.getCNNCodeVersion()),s.eVar37=s.prop37,s.prop37="",s.prop43||(s.prop50=""),s.eVar47="D=c47",s.eVar52=s.prop52,s.prop52="",s.eVar53=s.prop53,s.prop53="",s.eVar54=s.prop54,s.prop54="",s.eVar56=s.prop56,s.prop56="",s.prop57&&(s.eVar57=s.prop57,s.prop57=""),s.eVar60=s.prop60,s.prop60="",s.eVar64=wminst.Util.getCNNUIEngagement(),s.prop64="",s.eVar66=s.prop66,s.prop66="",s.eVar68=s.prop68,s.prop68="",s.eVar70=s.prop70,s.prop70="",s.eVar71=s.prop71,s.prop71="",s.eVar72=s.prop72,s.prop72="","undefined"==typeof r.isLive||1!=r.isLive&&"true"!=r.isLive||wminst.setinterval_id&&clearInterval(wminst.setinterval_id),wminst.isAMPVideos&&(s.timestamp=wminst.getAMPVideoTimeStamp()),wminst.isMoneyVideo(r)?wminst.trackMoneyVideoEvent("complete",r):(s.eVar14=s.prop14,s.prop14="",wminst.trackLinkVideo("cnnvideo-complete",r)),p.set(r.playerid,"vidStarted",!1),p.set(r.playerid,"hasScrubbed",!1),p.set(r.playerid,"isPaused",!1),p.set(r.playerid,"isBuffering",!1),p.set(r.playerid,"isHalf",!1),p.set(r.playerid,"isTen",!1),p.set(r.playerid,"isTwentyFive",!1),p.set(r.playerid,"isSeventyFive",!1),s.manageVars("clearVars")}),wminst.videoCommonFunction={videoCommonData:function(e){s.manageVars("clearVars"),wminst.standardVideoMetadata.isCNNGo=!1;var r=wminst.Util.isVideoAutoStarted(e);if("undefined"!=typeof e.free_preview&&""!==e.free_preview&&(wminst.standardVideoMetadata.isCNNGo=!0),s.prop33="adbp:video start",s.eVar33="D=c33",e.video_player&&"undefined"!==e.video_player&&""!==e.video_player&&(s.prop52=e.video_player,s.eVar52="D=c52",s.prop33="adbp:video start",s.eVar33="D=c33"),e.video_player&&-1!==e.video_player.indexOf("theo"))if(!0===e.isVr)s.prop52="theo360",s.eVar52="D=c52",s.prop33="adbp:video:360",s.eVar33="D=c33";else if(s.prop52=e.video_player,s.eVar52="D=c52","undefined"!=typeof window.CNN.omniture)try{s.prop14=CNN.omniture.branding_social||"",s.eVar14="D=c14"}catch(f){}s.prop32=wminst.Util.getCNNTemplateType("long"),s.prop32&&""!=s.prop32&&(s.eVar32="D=c32"),s.prop37=wminst.Util.getCNNPlatform(),s.prop37&&""!=s.prop37&&(s.eVar37="D=c37"),"undefined"!=typeof e.id&&""!=e.id&&-1!=e.id.indexOf("invalid-id-video-player")&&(s.prop43=wminst.Util.getCNNPostID(),s.prop50=wminst.Util.getCNNPostTitle()),s.list1=wminst.Util.getCEPTopisForVideo(e)||wminst.Util.getCNNTopic(),s.prop72=e.free_preview||"",s.eVar72="D=c72","undefined"!=typeof e.video_focus&&(s.prop66=e.video_focus,s.eVar66="D=c66");try{wminst.standardVideoMetadata.player=CNN.omniture.video_player_type}catch(f){wminst.standardVideoMetadata.player=""}"undefined"==typeof e.isLive||"true"!=e.isLive&&1!=e.isLive||(wminst.standardVideoMetadata.player="live player",s.prop53=e.live_stream_name?e.live_stream_name:"cnn news",s.eVar53="D=c53"),wminst.standardVideoMetadata.player||(wminst.standardVideoMetadata.player="vod player"),e.player_type&&""!=e.player_type&&(wminst.standardVideoMetadata.player=e.player_type,"live"==e.player_type&&(wminst.standardVideoMetadata.player="live player"),"van"==e.player_type?(s.prop31="van",s.eVar31="D=c31",s.prop32="adbp:video",s.eVar32="D=c32",s.server=s.eVar29=e.consumer||"",s.prop71=e.source.toLowerCase()||"",s.eVar71="D=c71"):"tve"!=e.player_type&&"live"!=e.player_type&&"live player"!=e.player_type||(s.prop3=e.category||"",s.eVar3="D=c3",s.prop31="van",s.eVar31="D=c31",s.prop53=e.live_stream_name?e.live_stream_name:"cnn news",s.eVar53="D=c53"));var p="";try{"undefined"!=typeof window.CNN.omniture.video_player_type&&""!=window.CNN.omniture.video_player_type?p=window.CNN.omniture.video_player_type:"undefined"==typeof e.isLive||"true"!=e.isLive&&1!=e.isLive?"undefined"!=typeof e.player_type&&""!=e.player_type&&"live"==(p=e.player_type)&&(p="live player"):p="live player"}catch(f){p=""}p||(p="vod player"),s.prop1=p,s.eVar1="D=c1";try{(-1<window.location.href.indexOf("fave.api.cnn.io")||-1<window.location.href.indexOf("fave-api.cnn.com"))&&e.video_player&&-1!==e.video_player.indexOf("theo")&&(s.prop32="content:video:nocollection","undefined"!=typeof window.CNN.omniture.template_type&&"live-story"==window.CNN.omniture.template_type&&(s.prop32="other:live story"),s.eVar32="D=c32")}catch(f){}try{s.prop2=window.CNN.omniture.cap_author||"",s.eVar2="D=c2"}catch(f){}try{s.prop3=e.id.split("/")[0],s.eVar3="D=c3"}catch(f){}try{s.prop7=e.trt?e.trt:"",s.eVar7="D=c7"}catch(f){}s.prop8=wminst.Util.getCNNVisitNumber(28);var a=e.dateCreated&&e.dateCreated.text?e.dateCreated.text:"",t=""!=a?a.split("/"):"";""!=t&&4!=t[0].length&&(a="20"+t[2]+"/"+t[0]+"/"+t[1]);var o=wminst.Util.getCNNDaysSinceLastPublish(a),i=a+"|"+(e.lastModified&&e.lastModified.text?e.lastModified.text:"");s.prop10=o+"",s.eVar10="D=c10",s.prop16=i,s.eVar16="D=c16";try{"undefined"!=typeof e.subcategory&&"default"==e.subcategory?"undefined"!=typeof window.CNN.omniture.branding_content_page&&(s.prop11="v:"+window.CNN.omniture.branding_content_page,s.eVar11="D=c11"):"undefined"!=typeof e.sponsor&&e.sponsor?(s.prop11="v:"+e.sponsor,s.eVar11="D=c11"):e.subcategory&&"undefined"!=typeof e.subcategory&&""!=e.subcategory&&(s.prop11="v:"+e.subcategory,s.eVar11="D=c11")}catch(f){}var n=window.location.hostname;if(-1!=n.indexOf("fave.api.cnn.io")||-1!=n.indexOf("fave-api.cnn.com")){var V=window.location.pathname;-1!=V.indexOf("/v1/amp")&&(s.prop14="google amp",s.eVar1="D=c14"),-1!=V.indexOf("/v1/fav")&&(s.prop14="embed",s.eVar1="D=c14"),-1!=V.indexOf("/v1/synacor")&&(s.prop14="synacor player",s.eVar1="D=c14",s.prop1="synacor player",s.eVar1="D=c1")}try{if("undefined"!=typeof window.CNN.omniture&&!0===window.CNN.omniture.fbia){s.prop14=window.CNN.omniture.branding_social,s.eVar1="D=c14";var d=CNN.omniture.vpage_name;s.pageName=wminst.Util.getCNNPageName(d),s.eVar26="D=pageName"}}catch(f){}s.eVar22=wminst.Util.getCNNVideoOpportunity(),s.server=wminst.Util.getADBPURL("domain"),s.channel=wminst.Util.getCNNSection(0),s.prop28=wminst.Util.getCNNSection(1),s.pageName=wminst.Util.getCNNPageName(),wminst.isGoogleAmp=s.prop14;try{e.title||"undefined"==typeof e.headline||(e.title=e.headline.toLowerCase()),"van"!=wminst.standardVideoMetadata.player||"undefined"==typeof e.title&&""==e.title&&""!=e.title?"vod player"!=wminst.standardVideoMetadata.player||"undefined"==typeof e.category&&""==e.category||"vr"!=e.category?s.prop29="/video/"+e.id:s.prop29=e.title:s.prop29="/video/"+e.title,s.eVar41="D=c29"}catch(f){}s.prop30=wminst.Util.getSiteSpecificSettings(1),s.eVar30="D=c30";try{s.prop31=window.CNN.omniture.cap_show_name,s.eVar31="D=c31"}catch(f){}s.prop34="does not require authentication",s.eVar34="D=c34";try{e.auth_state?(s.prop34=e.auth_state,s.eVar34="D=c34"):"undefined"==typeof e.mvpd||"temppass_cnn10min"!=e.mvpd&&"TempPass_CNN10min"!=e.mvpd?"undefined"!=typeof e.mvpd&&"string"==typeof e.mvpd&&""!==e.mvpd&&(s.prop34="requires authentication",s.eVar34="D=c34"):(s.prop34="requires authentication",s.eVar34="D=c34")}catch(f){}s.eVar36||(s.eVar36=wminst.Util.getCNNKruxID()),"vod player"!=wminst.standardVideoMetadata.player||"undefined"==typeof e.category&&""==e.category||"vr"!=e.category?s.eVar42="/video/"+e.id:s.eVar42=e.id,s.prop44||(s.prop44=wminst.Util.getCNNSourceID()),s.prop46=wminst.Util.getCNNTransactionID();var l="vod",m="non tve",c="clip",w="clip";-1!=wminst.standardVideoMetadata.player.indexOf("live")&&"requires authentication"==s.prop34&&(m="tve",w=c=l="live"),-1!=wminst.standardVideoMetadata.player.indexOf("live")&&"does not require authentication"==s.prop34&&(m="non tve",w=c=l="live"),-1!=wminst.standardVideoMetadata.player.indexOf("tve")&&(m="tve",w=c=l="live");var u=wminst.isAd?"ad":"content";s.prop54="video:"+l+":"+m+":"+c+":"+w+":"+u,s.eVar54="D=c54",s.prop56=wminst.Util.getCNNOrientation();try{if(e.dateAired){var g=wminst.Util.gCNNDaysSinceLastPublish(e.dateAired);s.prop58=g+"",s.eVar58="D=c58"}}catch(f){}try{window.CNN&&window.CNN.omniture&&"article"==window.CNN.omniture.cap_content_type?"undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:editorial":"noautostart:editorial":s.prop70="noautostart:editorial":!e.isLive||1!=e.isLive&&"true"!=e.isLive?"undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:vod":"noautostart:vod":s.prop70="noautostart:vod":"undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:live":"noautostart:live":s.prop70="noautostart:live",s.eVar70="D=c70"}catch(f){}try{if(window.location.pathname.match(/video\/playlists\/./)){var N=/video\/playlists\/(.+)/.exec(window.location.pathname);s.prop60=N[1].replace(/\//g,""),s.eVar60="D=c60","undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:collection":"noautostart:collection":s.prop70="noautostart:collection",s.eVar70="D=c70"}"player-one-tap-video"!=e.playerid&&(window.CNN.omniture.video_collection&&(s.prop60=window.CNN.omniture.video_collection,s.eVar60="D=c60","undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:collection":"noautostart:collection":s.prop70="noautostart:collection",s.eVar70="D=c70"),window.video_collection&&("undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:collection:sunrise":"noautostart:collection:sunrise":s.prop70="autostart:collection:sunrise",s.eVar70="D=c70")),e.video_collection&&(s.prop60=e.video_collection,s.eVar60="D=c60","undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:collection":"noautostart:collection":(s.prop70="noautostart:collection",s.eVar70="D=c70")),""!=s.prop60&&"undefined"!=typeof s.prop60||window.CNN.contentModel.analytics.pageTop.collectionHeadline&&(s.prop60=window.CNN.contentModel.analytics.pageTop.collectionHeadline,s.eVar60="D=c60"),""!==s.prop60&&(s.prop60=s.prop60.toLowerCase())}catch(f){}try{if(e.iscmsIIimport){var y="true"==e.iscmsIIimport?"secondary":"primary";s.prop61=y,s.eVar61="D=c61"}e.source&&(s.prop71=e.source.toLowerCase(),s.eVar71="D=c71")}catch(f){}try{e.ad_duration?(wminst.adRange=Math.round(e.ad_duration).toString(),s.prop68=wminst.adRange):s.prop68="no ad present",s.eVar68="D=c68"}catch(f){}try{"undefined"!=typeof e.id&&-1!=e.id.indexOf("cvplive/cnngo")&&(s.prop64="ngtv")}catch(f){}if(e.content_type2){if(s.prop1="ngtv",s.eVar1="D=c1",s.prop2=e.author,s.eVar2="D=c2","live"==e.content_type2||"dvr"==e.content_type2){s.prop7=s.eVar7="";var C="cnn news";e.live_stream_name&&(C=e.live_stream_name),s.prop53=C,s.eVar53="D=c53"}try{if(e.dateCreated){var k=wminst.Util.gCNNDaysSinceLastPublish(e.dateCreated);s.prop10=k+"",s.eVar10="D=c10",s.prop16=e.dateCreated,s.eVar16="D=c16"}}catch(f){}s.prop11=s.eVar11="",s.prop14=s.eVar14="",e.show_name=e.show_name||"",e.episode_title=e.episode_title||"",e.segment_name=e.segment_name||"","tve"==e.content_type1&&(e.title=e.show_name+":"+e.episode_title+":"+e.segment_name,e.live_stream_name&&"hln news"==e.live_stream_name&&(e.title="hln news"),s.prop29=e.title,s.prop32="adbp:video",s.eVar33="D=c33",s.eVar33="D=pageName"),s.prop31=e.show_name,s.eVar31="D=c31",s.prop33="adbp:video start",s.eVar33="D=c33",s.eVar42=e.id,"undefined"!=typeof e.isBreakingNews&&1==e.isBreakingNews&&(s.eVar43="ngtv:breaking_news"),e.segment_type&&(s.eVar43=e.segment_type),e.content_type1=e.content_type1||"",e.content_type2=e.content_type2||"",e.content_type3=e.content_type3||"",e.content_type4=e.content_type4||"",e.content_type5=wminst.isAd?"ad":"content",s.prop54="video:"+v.content_type2+":"+v.content_type1+":"+v.content_type3+":"+v.content_type4+":"+v.content_type5,e.content_type3&&"episode"!=e.content_type3&&(s.prop58=s.eVar58=""),s.prop60=s.eVar60="",s.prop61=s.eVar61="",s.prop64=s.eVar64="","non tve"==e.content_type1&&"vod"==e.content_type2&&"clip"==e.content_type3||(s.prop68=s.eVar68="",s.prop71=s.eVar71=""),"undefined"!=typeof e.isAutoStart&&1==e.isAutoStart?s.prop70=!0===r?"autostart:cnngo":"noautostart:cnngo":s.prop70="noautostart:cnngo",s.eVar70="D=c70"}e.headline&&(s.prop23=e.headline.toLowerCase(),s.eVar23="D=c23"),s.list1=wminst.Util.getCEPTopisForVideo(e)||wminst.Util.getCNNTopic(),s.eVar67=wminst.Util.getCNNPlayerState(e);try{window.CNN.omniture.gallery_name=""}catch(_){}try{window.CNN&&"undefined"!=window.CNN.omniture&&1==window.CNN.omniture.is_vision&&(s.prop71="cnn:vision",s.eVar71="D=c71")}catch(f){}try{s.prop4=wminst.Util.getPageAttribution(),s.prop46=wminst.Util.getCNNTransactionID(),s.prop47=wminst.Util.getCookie("ug"),s.prop26=wminst.Util.getCNNBaseURL(),s.prop75=wminst.Util.getCNNUserAuthState()}catch(f){}s.prop57="undefined"!=typeof e.mvpd&&"string"==typeof e.mvpd&&""!==e.mvpd?e.mvpd.toLowerCase():wminst.Util.getCNNMVPD(),s.eVar57="D=c57","undefined"!=typeof e.adobe_hash_id&&""!=typeof e.adobe_hash_id?s.prop59=e.adobe_hash_id:"undefined"!=typeof e.adobeHashId&&""!==e.adobeHashId?s.prop59=e.adobeHashId:s.prop59=wminst.Util.getCNNAdobeID(),s.eVar59="D=c59"}};
});

// BEGIN Salesforce DMP JavaScript Consent Tag for "Turner International"
Krux( 'consent:set', {

  dc: true,
  al: true,
  tg: true,
  cd: true,
  sh: true,
  re: true

}, function(errors, body) {

   if (errors) {
    console.error(errors);
  } else {
    console.log('Successfully set consent flags.');
  }

});
// END Salesforce DMP JavaScript Consent Tag


(function(){
	Krux('scrape',{'page_attr_url_path_1':{'url_path':'1'}});
	Krux('scrape',{'page_attr_url_path_2':{'url_path':'2'}});
	Krux('scrape',{'page_attr_url_path_3':{'url_path':'3'}});
	Krux('scrape',{'page_attr_meta_keywords':{meta_name:'keywords'}});

	Krux('scrape',{'page_attr_domain':{url_domain: '2'}});

})();


(function(){

	var params = Krux('require:util').urlParams();
	
	Krux ('set', { 
	'page_attr_utm_source': params.utm_source,
	'page_attr_utm_medium': params.utm_medium,
	'page_attr_utm_campaign': params.utm_campaign,
	'page_attr_utm_content': params.utm_content,
	'page_attr_utm_term': params.utm_term 
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
    dataObj = Krux('scrape.javascript', 'navigator');

    /* String trimming helper function */
    trim = function(attr) {
        return ("" + attr).replace(/^\s+|\s+$/g, '');
    };

    /* Attribute configs */
    pageAttr = _.map('cnn_international_site,cnn_international_rollup,cnn_international_section,cnn_international_subsection,cnn_international_spec,cap_topics,cookie_last5stocks,on_site_searcher,cnn_international_bizunit,cnn_international_brand,cnn_international_lob,cnn_international_sitename,cnn_international_sitesectionlevel1,cnn_international_sitesectionlevel2,on_site_searcher,cnn_arabic_site,cnn_arabic_rollup,cnn_arabic_section,cnn_arabic_bizunit,cnn_arabic_brand,cnn_arabic_lob,cnn_arabic_sitename,cnn_arabic_sitesectionlevel1,cnn_arabic_sitesectionlevel2,espanol_site,espanol_rollup,espanol_section,espanol_bizunit,espanol_brand,espanol_lob,espanol_sitename,espanol_sitesectionlevel1,espanol_sitesectionlevel2,cnn_site,cnn_rollup,cnn_section,cnn_subsection,cnn_adunit5,cnn_spec,cnn_bizunit,cnn_brand,cnn_lob,cnn_sitename,cnn_sitesectionlevel1,cnn_sitesectionlevel2,cnn_money_site,cnn_money_rollup,cnn_money_section,cnn_money_subsection,cnn_money_adunit5,cnn_money_spec,cnnbusinessedition_lob,cnnbusinessedition_brand,cnnbusinessedition_bizunit,cnnbusinessedition_sitename,cnnbusinessedition_sitesectionlevel1,cnnbusinessedition_sitesectionlevel2,cnn_money_site,cnn_money_rollup,cnn_money_section,cnn_money_subsection,cnn_money_adunit5,cnn_money_spec,cnnbusiness_lob,cnnbusiness_brand,cnnbusiness_bizunit,cnnbusiness_sitename,cnnbusiness_sitesectionlevel1,cnnbusiness_sitesectionlevel2,br_site,br_rollup,br_section,br_subsection,bleacherreport_keywords'.split(','), trim);
    userAttr = _.map('userAgent,turner_guid,userUid'.split(','), trim);

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
        useFullPath: 'true' === 'true',
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


    var slot;
    (function() {
        if (window.googletag && googletag.pubads() && googletag.pubads().getSlots()) {
            var c1 = {};
            var arr = googletag.pubads().getSlots();
            var site = ["cnn", "cnn_arabic", "cnn_international", "cnn_money", "espanol"];

            if (arr) {
                for (var i = 0, l = arr.length; i < l; i++) {
                    c1[arr[i].getAdUnitPath()] = (c1[arr[i].getAdUnitPath()] || 0) + 1;
                }
                slot = Object.keys(c1)[0] || null;
                for (k in c1) slot = (c1[k] > c1[slot]) ? k : slot;
            }

            if (window.slot) { // Set string lowercase and split slot into an array 
                slot = slot.toLowerCase();
                slot = slot.split('/');

                // Changes slot from "as" to "toonswim"
                slot[2] = slot[2] == 'as' ? 'toonswim' : slot[2];
                // Changes slot from "arabic" to "cnn_arabic"
                slot[2] = slot[2] == 'arabic' ? 'cnn_arabic' : slot[2];
                // Changes slot from "cnni" to "cnn_internation"
                slot[2] = slot[2] == 'cnni' ? 'cnn_international' : slot[2];
                // Changes slot from "cnnmoney" to "cnn_money"
                slot[2] = slot[2] == 'cnnmoney' ? 'cnn_money' : slot[2];
                
                // "teamcoco"
                if(slot[2] === "tbs" && slot[4] === "conan"){
                    slot = slot.splice(2)
                };

                for (var i = 0; i < site.length; i++) {

                    if (slot[2] == site[i]) {
                        // Using domain to dynamically scrape page attribute site 
                        Krux('set', 'page_attr_' + slot[2] + '_site', slot[2]);
                        // Using domain to dynamically scrape page attribute rollup
                        Krux('set', 'page_attr_' + slot[2] + '_rollup', slot[3]);
                        // Using domain to dynamically scrape page attribute section 
                        Krux('set', 'page_attr_' + slot[2] + '_section', slot[4]);
                        // Using domain to dynamically scrape page attribute subsection
                        Krux('set', 'page_attr_' + slot[2] + '_subsection', slot[5]);
                        // Using domain to dynamically scrape page attribute AdUnit 5 
                        Krux('set', 'page_attr_' + slot[2] + '_adunit5', slot[6]);
                        
    
                    };
                };
            };
        };
        
        if(window.CNNMONEY && window.CNNMONEY.adTargets) spec = CNNMONEY.adTargets.spec;
        if(window.CNN && window.CNN.adTargets) spec = CNN.adTargets.spec;
        if(window.CNNI && window.CNNI.adTargets) spec = CNNI.adTargets.spec;
                        
        if (window.spec && slot && slot.length >= 3) {
           Krux('set', 'page_attr_' + slot[2] + '_spec', spec);
        };
        
    
        
        
        if (window.queryString) {
            Krux('set', 'page_attr_on_site_searcher', true)
        };


        if (window.CNN && window.CNN.contentModel && window.CNN.contentModel.analytics) {
            var ct = CNN.contentModel.analytics.cap_topics;
            if (ct) {
                ct = ct.replace(/ /g, '');
                Krux('set', 'page_attr_cap_topics', ct);
            };
        };

    })();


(function() {
    Krux('scrape', { "page_attr_cookie_last5stocks": {cookie: "last5stocks"}});

    if(window.slot) {

        // get namespace;
        var ns = (function() {
                        var exceptions, jsmdmap, key1, key2, val1, val2, _ref;
                        if (window._jsmd_default) {
                            jsmdmap = _jsmd_default.map;
                            for (key1 in jsmdmap) {
                                val1 = jsmdmap[key1];
                                for (key2 in val1) {
                                    val2 = val1[key2];
                                    if (ns = val2 != null ? (_ref = val2.settings) != null ? _ref.visitorNamespace : void 0 : void 0) {
                                        return ns;
                                    }
                                }
                            }
                        }
                        return exceptions[Krux('get', 'site')];
                })();

        if(!ns) return;
        //get site
        var site = slot[2];
        // get pixel
        var pixel = window["s_i_" + ns] || window["s_i_1_" + ns] || window["s_i_0_" + ns];
        // regex for pixel source
        var lookFor = "&h1=(.*?)&";
        // check if pixel source matches the regex
        var match =  (pixel && pixel.src) ? pixel.src.match(lookFor) : null;

        if (match) {
            var parts = decodeURIComponent(match[1]).split('|');
            var keys = ['lob', 'brand', 'bizunit', 'sitename', 'sitesectionlevel1', 'sitesectionlevel2'];
            for (var i = 0, l = keys.length;i < l; i++) {
                var key = keys[i];
                if(parts[i]) Krux('set', "page_attr_" + site + "_" + key, parts[i]);
            }
        }
    }

})();



(function()
{
	var protocol = window.location.protocol == 'https:' ? 'https:' : 'http:';
	var protocol1 = window.location.protocol == 'https:' ? 'https%3A' : 'http%3A';

    new Image().src =protocol+"//bea4.cnn.com/ad/u?mode=echo&cr=https%3A%2F%2Fbeacon.krxd.net%2Fusermatch.gif%3Fpartner%3Dfreewheel%26partner_uid%3D%23%7Buser.id%7D";
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
    dataObj = Krux('scrape.javascript', 'CNN.cep_topics');

    /* String trimming helper function */
    trim = function(attr) {
        return ("" + attr).replace(/^\s+|\s+$/g, '');
    };

    /* Attribute configs */
    pageAttr = _.map('cep_sent,cep_iabt,cep_tags,cep_brsf'.split(','), trim);
    userAttr = _.map('undefined'.split(','), trim);

    /* Create a array of attributes striping any empty strings */
    allAttr = _.without(pageAttr.concat(userAttr), '');

    /* Configuration settings */
    keepCase = 'false' === 'true';
    omitKeys = 'undefined'.split(',');

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


(function() {
    /* Generic Scrape Tag - Configurable Data Collection */
    var _, filterValues, libUtil, prefix, scrapeConfig, toSet;
    _ = Krux('require:underscore');
    libUtil = Krux('require:util.library-tag');
    toSet = {};
    filterValues = function(val) {
        var i, item, len, ref, str, x;
        if (_.isArray(val)) {
            return _.compact((function() {
                var i, len, results;
                results = [];
                for (i = 0, len = val.length; i < len; i++) {
                    item = val[i];
                    results.push(filterValues(item));
                }
                return results;
            })());
        }
        str = "" + val;
        if (!((val != null) && str.length > 0)) {
            return;
        }
        ref = libUtil.EXCLUDE_VALUES_CONFIG;
        for (i = 0, len = ref.length; i < len; i++) {
            x = ref[i];
            if (str.match(x) != null) {
                return;
            }
        }
        return val;
    };
    scrapeConfig = function(config, type) {
        var attr, i, len, parts, ref, results, value;
        ref = libUtil.removeFalsyStrings(config);
        results = [];
        for (i = 0, len = ref.length; i < len; i++) {
            attr = ref[i];
            parts = attr.split('|');
            if (parts.length === 1 && 'url_param'.match(/(dom|javascript)/)) {
                continue;
            }
            if (parts.length === 1) {
                parts.unshift(libUtil.normalizeAttrName(parts[0]));
            }
            switch ('url_param') {
                case 'get':
                    value = filterValues(Krux('get', parts[1]));
                    break;
                default:
                    value = filterValues(Krux('scrape.url_param', parts[1]));
            }
            if (value) {
                results.push(toSet[type + "_attr_" + parts[0]] = value);
            } else {
                results.push(void 0);
            }
        }
        return results;
    };
    scrapeConfig('search|q', 'page');
    scrapeConfig('undefined', 'user');
    prefix = libUtil.resolvePrefix('text', 'cnn',
        'cnn');
    toSet = Krux('prefix:attr', toSet, prefix);
    Krux('set', toSet);
}).call();
