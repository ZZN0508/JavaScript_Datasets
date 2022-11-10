 var pvDomain = 'pv.ltn.com.tw'; 
 var pvServer = 'pv.ltn.com.tw'; 
var interstitialSlot;
var staticSlot = false;

    var interstitial = 0;
    var userAgent = navigator.userAgent;
    var platform = navigator.platform;
    var iOSDevice = ['iPhone', 'iPad'];

    function isiPhone() {
        return (userAgent.indexOf('iPhone') >= 0) ? true : false;
    }

    function isAndroid() {
        return (userAgent.indexOf('Android') >= 0) ? true : false;
    }

    function isFB() {
        return (userAgent.indexOf('FB') >= 0) ? true : false;
    }

    function isLine() {
        return (userAgent.indexOf(' Line') >= 0) ? true : false;
    }

    function isChrome() {
        return (userAgent.indexOf('Chrome') >= 0 || userAgent.indexOf('CriOS') >= 0) ? true : false;
    }

    function isSimulator(device) {
        var i;
        var isDevice = true;
        for (i = 0; i < device.length; i++) {
            isDevice = (platform.indexOf(device[i]) >= 0) ? false : true;
            if (!isDevice) {
                break;
            }
        }
        return isDevice;
    }
    if (isFB()) {
        interstitial = 1;
    } else if (isLine()) {
        interstitial = 1;
    } else if (isAndroid() && !isChrome()) {
        interstitial = 1;
    } else if (isiPhone() && !isSimulator(iOSDevice) && !isChrome()) {
        interstitial = 1;
    }

    console.log('interstitial = ' + interstitial);
    var googletag = googletag || {}; googletag.cmd = googletag.cmd || [];
    googletag.cmd.push(function() {
        googletag.pubads().setTargeting("ltn_interstitial", [interstitial.toString()]);

    });


        var pvServer = 'pv.ltn.com.tw';
        var newsServer = 'news.ltn.com.tw';
        var wwwServer = 'https://www.ltn.com.tw/';
    

        var adDevice = 'P';
        if ($(window).outerWidth() <= 828) {
            adDevice = 'M';
        } else {
            adDevice = 'P';
        }
    


    var CriteoAdUnits = { "placements": [
            /* Criteo Placements List, slotid must match DFP Container ID */
            { "slotid": "ad-BD1", "zoneid": 815941 }, // Liberty Times - News - TW - CDB - SA - 300x250 - Top
            { "slotid": "ad-C1", "zoneid": 815942 }, // Liberty Times - News - TW - CDB - SA - 300x250 - Bottom-left
            { "slotid": "ad-C2", "zoneid": 815942 }, // Liberty Times - News - TW - CDB - SA - 300x250 - Bottom-right
            { "slotid": "ad-BD2", "zoneid": 815943 }, // Liberty Times - News - TW - CDB - SA - 300x600
            { "slotid": "ad-K1", "zoneid": 815944 }, // Liberty Times - News - TW - CDB - SA - 970x90
            { "slotid": "ad-K1", "zoneid": 815945 } // Liberty Times - News - TW - CDB - SA - 970x250

        ]};
    window.Criteo = window.Criteo || {}; window.Criteo.events = window.Criteo.events || [];
    if (cookies_m.isPC()) {
        var googletag = googletag || {};
        googletag.cmd = googletag.cmd || [];
        googletag.cmd.push(function () {
            googletag.pubads().disableInitialLoad();
        });
    }

    $(function(){
        if (cookies_m.isPC()) {
            var launchAdServer = function() {
                googletag.cmd.push(function() {
                    Criteo.SetDFPKeyValueTargeting();
                    googletag.pubads().refresh();
                });
            };

            Criteo.events.push(function() {
                Criteo.SetLineItemRanges("0..3:0.01;3..8:0.05;8..20:0.50;20..30:1.00");
                Criteo.RequestBids(CriteoAdUnits, launchAdServer, 1000);
            });
        }
    });



    var googletag = googletag || {};
    googletag.cmd = googletag.cmd || [];
    (function() {
        var gads = document.createElement('script');
        gads.async = true;
        gads.type = 'text/javascript';
        var useSSL = 'https:' == document.location.protocol;
        gads.src = (useSSL ? 'https:' : 'http:') +
            '//www.googletagservices.com/tag/js/gpt.js';
        var node = document.getElementsByTagName('script')[0];
        node.parentNode.insertBefore(gads, node);
    })();


    googletag.cmd.push(function() {
        var dfp = {"pc":{"BD1":{"slot":"\/21202031\/00-ltn-home-BD1","size":"[[300,250],[300,600]]","div":"ad-BD1","class":"ad-BD1","collapse":1},"BD2":{"slot":"\/21202031\/00-ltn-home-BD2","size":"[[300,250],[300,600]]","div":"ad-BD2","class":"ad-BD2","collapse":1},"K1":{"slot":"\/21202031\/00-ltn-home-K1","size":"[[1, 1], [970, 90], [970, 160], [970, 250], [1260, 90], [1260, 160], [1260, 250]]","div":"ad-K1","class":"ad-K1","collapse":1}},"m":{"B1":{"slot":"\/21202031\/02-mobile-home-B1","size":"['fluid', [1, 1], [300, 250], [336, 280]]","div":"ad-B1","class":"ad-B1","collapse":1},"B3":{"slot":"\/21202031\/02-mobile-home-B3","size":"['fluid', [1, 1], [300, 250], [336, 280]]","div":"ad-B3","class":"ad-B3","collapse":1},"B4":{"slot":"\/21202031\/02-mobile-home-B4","size":"['fluid', [1, 1], [300, 250], [336, 280]]","div":"ad-B4","class":"ad-B4","collapse":1},"B2":{"slot":"\/21202031\/02-mobile-home-B2","size":"['fluid', [1, 1], [300, 250], [336, 280]]","div":"ad-B2","class":"ad-B2","collapse":1}}};
        var device = cookies_m.isPC() ? 'pc' : 'm';
        dfp = dfp[device] || [];
        for (var key in dfp) {
            // 蓋台廣告由cache_ads_h1.php控制
            if (key === 'H1') { continue; }
            if (dfp.hasOwnProperty(key)) {
                var ad = dfp[key];
                var adSize = eval(ad['size']);
                var bodyWidth = $('body').width();
                ad['size'] = [];
                for (var i in adSize) {
                    if (adSize[i][0] > bodyWidth) { continue; }
                    ad['size'].push(adSize[i]);
                }
                googletag.defineSlot(
                    ad['slot'],
                    ad['size'],
                    ad['div']
                ).addService(googletag.pubads()).setCollapseEmptyDiv(true, true);
            }
        }

        googletag.pubads().addEventListener('slotRenderEnded', function(event) {
            // google回傳的廣告標籤(ex:ad-B1)
            var slotElementId = event.slot.getSlotElementId();

            // === 無廣告時要做的事 ===
            if (event.isEmpty) {
                // 記錄沒有廣告
                console.log('沒有'+slotElementId);
                // 移除廣告單元
                //$('#' + slotElementId).remove();
                return;
            }

            // === 有廣告時要做的事 ===
            // 置底浮水印廣告，調整畫面不要蓋住footer
            if (slotElementId == 'ad-I1-bottom') {
                // 廣告的高度
                var ad_height = event.size[1];
                var $adI1Bottom = $('#ad-I1-bottom');
                // 調整廣告位置與footer墊底高度
                $adI1Bottom.css('height', ad_height + 'px');
                $('.door-bottom-space').show().css('height', ad_height + 'px');

                // 顯示關閉按鈕並綁定關閉事件
                if (ad_height > 50) {
                    // 調整Top按鈕高度
                    $('#top').css('bottom', (ad_height + 20) + 'px');
                    // 監聽關閉按鈕
                    $adI1Bottom.prepend('<i class="close"></i>');
                    $adI1Bottom.find('.close').click(function () {
                        $adI1Bottom.fadeOut(100);
                        $('.door-bottom-space').fadeOut(100);
                        $('#top').css('bottom', '100px');
                    });
                }
                return;
            }

            // 有IR1時顯示「請繼續往下閱讀...」
            if (slotElementId == 'ad-IR1') {
                // 顯示「請繼續往下閱讀...」(class="before_ir"在cache中寫的)
                $('p.before_ir').fadeIn(200);
                $('p.after_ir').fadeIn(200);
            }
        });
        googletag.enableServices();
    });


    // 判斷裝置 並只呼叫相同裝置的廣告
    function displayDFP(div, dfpDevice) {
        var realDevice = cookies_m.isPC() ? 'pc' : 'm';
        if (dfpDevice !== realDevice) {
            $('#'+div).remove();
            return;
        }
        googletag.cmd.push(function() { googletag.display(div); });
    }


_atrk_opts = { atrk_acct:"LS4hj1a8Dy002+", domain:"ltn.com.tw",dynamic: true};
(function() { var as = document.createElement('script'); as.type = 'text/javascript'; as.async = true; as.src = "https://certify-js.alexametrics.com/atrk.js"; var s = document.getElementsByTagName('script')[0];s.parentNode.insertBefore(as, s); })();


    var _comscore = _comscore || [];
    _comscore.push({ c1: "2", c2: "18368781" });
    (function() {
        var s = document.createElement("script"), el = document.getElementsByTagName("script")[0]; s.async = true;
        s.src = (document.location.protocol == "https:" ? "https://sb" : "http://b") + ".scorecardresearch.com/beacon.js";
        el.parentNode.insertBefore(s, el);
    })();


    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'DC-9530821');


// GA 點擊事件統計
$(function(){
    ga_news_event();
});

function ga_news_event()
{
    var base_root_org = 'http://'+newsServer;

    var deviceDesc = $("meta[name='ltn:device']").attr('content') || 'U';
    /*取頁面說明*/
    var _pageDesc = $('.page-name').attr('data-desc');

    var pageDesc =deviceDesc+':'+_pageDesc;

    $(document.body).on('click.ga', '.boxInput', function(){
        var obj = $(this);
        var objDesc = obj.attr('data-desc');

        var par = obj.parents('.boxTitle');
        var boxDesc = par.attr('data-desc');

        var category = pageDesc;
        var action = boxDesc;
        var label = objDesc || ''; /*使用自定義說明*/

        ga_send_event(category,action,label);

    });

    $('.boxTitle').on('click.count', 'a', function(e){
        if(e.button!=0){return;}
        if(getinfo($(this), false)) e.preventDefault();
    }).on('mouseup.count', 'a', function(e){
        if(e.button!=1){return;}
        getinfo($(this), true);
        e.preventDefault();
    });

    function setltncookies(area, item, elem){
        var ov_sec = 30;
        ltncookies_news("ltn_device", deviceDesc, ov_sec);
        ltncookies_news("ltn_page", _pageDesc, ov_sec);
        ltncookies_news("ltn_area", area, ov_sec);
        ltncookies_news("ltn_item", item, ov_sec);
        ltncookies_news("ltn_elem", elem, ov_sec);
    }
    function getinfo(obj, SendOnly){

        var objText = obj.text();
        var objDesc = obj.attr('data-desc');

        var par = obj.parents('.boxTitle');
        /*取區塊說明*/
        var boxDesc = par.attr('data-desc');
        /*是否用連結文字*/
        var useText = par.hasClass('boxText');

        var category = pageDesc;
        var action = boxDesc;
        var label = objDesc || ''; /*使用自定義說明*/
        if(useText && label==''){
            label = objText || ''; /*使用連結文字*/
        }

        var labelA = label;
        var idx = $('a', par).index(obj);
        if(label==''){
            /*記錄該區塊第幾則*/
            label = '第'+idx+'則';
        }

        var target = obj.attr('target');
        var href = '';
        var _href = obj.attr('href');

        if(_href){
            href = check_url(_href);
        }

        var send_type = 'send';

        if(!target && href!=''){
            send_type = 'redirect';
        }

        if(SendOnly) send_type = 'send';

        setltncookies(action, idx, labelA);  // Add area, item,
        if(send_type=='send'){
            ga_send_event(category,action,label);
            return false;
        }else{
            send2ga2page(category,action,label,href);
            return true;
        }
    }

    function check_url(_url){
        if((/^http:/).test(_url)){
            return _url;
        }else if((/^https:/).test(_url)){
            return _url;
        }else if((/^\/\//).test(_url)){
            return _url;
        }else if((/^javascript/).test(_url)){
            return '';
        }else if((/^#/).test(_url)){
            return '';
        }else{
            var base_root = $('base').attr('href') || base_root_org;
            return base_root+_url;
        }
    }

    /*GA事件追蹤:頁面不轉換*/
    function ga_send_event(category, title, label){
        ga_send_event_callback(category, title, label, function(){});
    }

    /*GA事件追蹤:頁面轉換*/
    function ga_send_event_callback(category, title, label, fn_callback){
        //return fn_callback();
        ga('send', 'event', category, title, label, {'hitCallback':
                function() {
                    fn_callback();
                }
        });
        //console.log(category+'-'+title+'-'+label);
        //return false;
    }

    /*GA事件追蹤:連結點擊*/
    function send2ga2page(category, title, label, url) {
        var redirectTriggered = false;

        ga_send_event_callback(category, title, label, function(){
            redirectTriggered = true;
            document.location = url;
        });

        setTimeout(function() {
            if (!redirectTriggered) {
                document.location = url;
            }
        }, 1500);
    }
};


    let webPushOrigin = 'https://www.ltn.com.tw';
    let webPushFile = webPushOrigin + '/webNotificationCheck';
    let webPushNotification = webPushOrigin + '/webNotification';

    // 監聽檢查回應
    window.addEventListener('message',function(e) {
        if (e.origin == webPushOrigin) {
            if (e.data == 'isOK') {
                let checkIframe = document.getElementById('checkIframe');
                checkIframe.contentWindow.postMessage('getPermission', webPushOrigin);
            } else if (e.data == 'granted') {
                $("#checkIframe").remove();
                console.log(e.data);
            } else if (e.data == 'denied' || e.data == 'default') { //default or denied
                $("#checkIframe").remove();
                console.log(e.data);
                softConfirm();
            }
        }
    },false);

    $(function() {
        let webPush = getCookie("softPush");
        if (webPush === undefined || webPush < 1) {
            if (userAgent.indexOf('Chrome') >= 0 || userAgent.indexOf('Firefox') >= 0 || userAgent.indexOf('Edge/') >= 0) {
                initFcm();
            } else if (userAgent.indexOf('Safari') >= 0) {
            }
        }
    });

    //檢查notification
    function initFcm()
    {
        console.log('check notification');
        if ('Notification' in window) {
            checkFcm();
        }
    }

    //檢查notification permission
    function checkFcm()
    {
        console.log('checkFcm');
        let checkIframe = document.createElement('iframe');
        checkIframe.setAttribute('id', 'checkIframe');
        checkIframe.setAttribute('src', webPushFile);
        checkIframe.setAttribute('allow', 'payment');
        document.body.appendChild(checkIframe);
    }

    //觸發軟詢問
    function softConfirm()
    {
        let softPushNotificaton = document.createElement('div');
        softPushNotificaton.setAttribute('class', 'softPush_notification');

        let softPushNotificationImg = document.createElement('img');
        softPushNotificationImg.setAttribute('src', 'https://news.ltn.com.tw/assets/images/all/ltn.png');
        softPushNotificaton.appendChild(softPushNotificationImg);

        let softPushNotificationSpan = document.createElement('span');
        softPushNotificationSpan.setAttribute('class', 'softPush_word');
        let softPushNotificationText = document.createTextNode('感謝您的訂閱 自由時報電子報隨時提供您最即時、熱門的新聞訊息。');
        softPushNotificationSpan.appendChild(softPushNotificationText);
        softPushNotificaton.appendChild(softPushNotificationSpan);

        let softPushNotificationButton = document.createElement('button');
        softPushNotificationButton.setAttribute('class', 'softPush_confirm');
        softPushNotificationText = document.createTextNode('訂閱');
        softPushNotificationButton.appendChild(softPushNotificationText);
        softPushNotificaton.appendChild(softPushNotificationButton);

        softPushNotificationButton = document.createElement('button');
        softPushNotificationButton.setAttribute('class', 'softPush_refuse');
        softPushNotificationText = document.createTextNode('暫時不要');
        softPushNotificationButton.appendChild(softPushNotificationText);
        softPushNotificaton.appendChild(softPushNotificationButton);

        document.body.appendChild(softPushNotificaton);
    }

    //設定軟詢問時間
    function setSoftPushCookie(extension = 0)
    {
        let st = "";
        let expires = new Date();
        //延展時間
        extension = (extension == 0) ? 7 * 24 * 60 * 60 * 1000 : extension;
        expires.setTime(expires.getTime() + extension);
        let ti = getCookie("softPush");
        if (ti === undefined) ti = 0;
        st = "softPush=" + (Number(ti)+1) +"; domain=ltn.com.tw;expires=" + expires.toGMTString() +"; path=/";
        document.cookie = st;
    }

    $(document).on("click",".softPush_confirm",function() {
        window.open(webPushNotification);
        getScrNews('www.webPush.ask', 'ask', '', '1');
        $(".softPush_notification").remove();
    });

    $(document).on("click",".softPush_refuse",function(){
        $(".softPush_notification").remove();
        getScrNews('www.webPush.ask', 'ask', '', '0');
        setSoftPushCookie();
    });


    $("#checkIE").hide();
	if (isIE(6) || isIE(7) || isIE(8) || isIE(9) || isIE(10) || isIE(11)) {
		$("#checkIE").show();
	}
	$('.close').click(function () {
		$("#checkIE").hide();
	})


applyWeather();

// 天氣主程式
function applyWeather()
{
    if(!/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        isWeather();
    }
}

function setCity(lat, lon) {
    let url = "https://api.bigdatacloud.net/data/reverse-geocode-client?latitude="+lat+"&longitude="+lon+"&localityLanguage=zh";
    let request = new XMLHttpRequest();
    request.open('GET', url, true);

    request.onload = function () {
        let data = JSON.parse(this.response);
        let cityName = '臺北市';
        if (request.status >= 200 && request.status < 400) {
            let cityArr = data.localityInfo.administrative;
            let result = cityArr.find(obj => {return obj.order == 4;});

            if (result == undefined) {
                result = cityArr.find(obj => {return obj.order == 3;});
            }
            cityName = result.name;
        }

        addWeather(cityName, 1);
    };
    request.send();
}

function isWeather()
{
    var isWeather = document.getElementById('ltnRWD') ? 1 : 0; // 判斷是否顯示天氣

    if (isWeather) {
        $( document ).ready(function() {
            // 先取用cookie先前天氣資料
            if (getCookie('city') && getCookie('temperature') && getCookie('icon') && getCookie('status')) {
                let data = {temperature: getCookie('temperature'), icon: getCookie('icon'), status: getCookie('status')};
                let city = getCookie('city');
                setAttribute(city, data);
                return;
            }
            // 還沒確認地理位置前先預設
            addWeather('臺北市', 1);
            // cookie沒值則抓取user位置天氣
            if (window.navigator.geolocation) {
                geo = window.navigator.geolocation;
                geo.getCurrentPosition(function(position) {setCity(position.coords.latitude, position.coords.longitude);},
                    addWeather('臺北市', 0)
                );
            }
        });
    }
}

function addWeather(city, isGEO) { // isGEO 0:無法取得定位 1:可以取得定位
    let weatherUrl = 'https://cache.ltn.com.tw' + '/getWeather/' + city;

    let xmlHttp = new XMLHttpRequest();
    xmlHttp.open( "GET", weatherUrl, true); // false for synchronous request

    xmlHttp.onload = function () {
        let data = JSON.parse(this.response);
        data.city = city;
        setCookie(data, isGEO);// 設定cookie
        setAttribute(city, data);// 設定天氣html
    };

    xmlHttp.send();
}

function setCookie(data, isGEO) {
    let cityNow = new Date();
    let weatherNow = new Date();
    var expireCityTime = (isGEO == 0)? 24 : 2;
    var expireWeatherTime = 8;
    cityNow.setTime(cityNow.getTime() + expireCityTime * 3600 * 1000);
    weatherNow.setTime(weatherNow.getTime() + expireWeatherTime * 3600 * 1000);
    for (let key in data) {
        document.cookie = (key == 'city')? key + '=' + data[key] + '; expires=' + cityNow.toUTCString() + '; domain=.ltn.com.tw; path=/' : key + '=' + data[key] + '; expires=' + weatherNow.toUTCString() + '; domain=.ltn.com.tw; path=/';
    }
}

function setAttribute(city, data) { //設定天氣html
    document.getElementById('weather_text').innerHTML = city + '  ' + data.temperature;
    document.getElementById('weather_img').setAttribute("src", 'https://cache.ltn.com.tw/images/weather/' + data.icon);
    document.getElementById('weather_img').setAttribute("alt", data.status);
    document.getElementById('weather_img').setAttribute("title", data.status);
}

function getCookie(name) { // 依名字取cookie
  const value = `; ${document.cookie}`;
  const parts = value.split(`; ${name}=`);
  if (parts.length === 2) return parts.pop().split(';').shift();
}


    var count = 0;
    function send() {
        if (count == 0) {
            count++;
            key = document.getElementById("cacheSearch").value.replace(/(　)+/g, ' ');
            key = key.replace(/( )+/g, ' ');
            key = key.replace(/^[\s]*/gi, ""); //去除左邊空白
            key = key.replace(/[\s]*$/gi, ""); //去除右邊空白
            document.getElementById("cacheSearch").value = key;

            kw = key.split(" ");

            if (key.length > 50) {
                alert("關鍵字數過長");
                count = 0;
                return false;
            }
            else if (kw.length > 3) {
                alert("超過三組關鍵字");
                count = 0;
                return false;
            }
            else if ((kw.length == 1 && kw[0].length < 2)) {
                alert("關鍵字需兩個字以上");
                count = 0;
                return false;
            }
            else
                return true;
        }
    }


    /*滑動隱藏header*/
    var startScroll = false;
    var firstScrollTop = 0;
    $(window).on('scroll', function() {
        if (!startScroll || this.scrollY <= $('#marquee').find('li').outerHeight(true)) {
            $('body').removeClass('hideUp');
            return;
        }
        if (firstScrollTop == 0) {
            firstScrollTop = this.scrollY;
        }
        firstScrollTop = hideUp(firstScrollTop, this.scrollY);
    });
    setTimeout(function () {
       startScroll = true;
    }, 3000);
    function hideUp(startY,  endY)
    {
        var moveY = endY - startY;
        var targetUp = 0;
        var targetDown = 0;
        if ($(window).outerWidth(true) <= 828) {
            //手機版條件
            targetUp = 5;
            targetDown = -100;
        }
        if (moveY > targetUp) {
            // 往上滑
            $('body').addClass('hideUp');
            startY = 0;
        } else if (moveY < targetDown) {
            // 往下滑 body移除hideUp以顯示header
            $('body').removeClass('hideUp');
            startY = 0;
        }
        return startY;
    }


  [{
    "@context": "http://schema.org",
    "@type": "WebSite",
    "name": "自由時報電子報",
    "alternateName": ["LTN","自由時報"],
    "url": "https://www.ltn.com.tw/",
    "keywords": ["自由時報","自由時報電子報","Liberty Times Net","LTN"],
    "potentialAction": {
      "@type": "SearchAction",
      "target": "https://search.ltn.com.tw/list?keyword={search_term_string}",
      "query-input": "required name=search_term_string"
    }
  },
  {
	"@context": "http://schema.org",
	"@type": "Organization",
	"name": "自由時報電子報",
	"url": "https://www.ltn.com.tw",
	"logo": "https://www.ltn.com.tw/assets/images/all/250_ltn.png",
	"sameAs": "https://www.facebook.com/m.ltn.tw/"
  },
  {
	"@context": "http://schema.org",
	"@type": "BreadcrumbList",
	"itemListElement": [
		{
			"@type": "ListItem",
			"position": 1,
			"item": {
				"@id": "https://www.ltn.com.tw",
				"name": "自由時報電子報"
			}
		}
	]
  }]


        var videoData = [{"videoId":"F91Hg5_Aaj0","pic":"https:\/\/img.ltn.com.tw\/Upload\/Module\/3\/709\/2708937.jpg","url":"https:\/\/video.ltn.com.tw\/article\/F91Hg5_Aaj0\/PLI7xntdRxhw3Qcbd70QE2FRWgpOQ-hBHO","title":"\u65b0\u589e286\u4f8b\u672c\u571f1\u4f8b\u6b7b\u4ea1 \u65b0\u5317157\u4f8b\u6700\u591a \u5883\u5916\u79fb\u5165+9"},{"videoId":"uAESP8DTwQA","pic":"https:\/\/img.ltn.com.tw\/Upload\/Module\/3\/710\/2709145.jpg","url":"https:\/\/video.ltn.com.tw\/article\/uAESP8DTwQA\/PLI7xntdRxhw3Qcbd70QE2FRWgpOQ-hBHO","title":"\u5361\u62c9OK\u9055\u898f\u71df\u696d\u3001\u5ba2\u4eba\u4e0d\u6234\u53e3\u7f69 \u5c4f\u6771\u8b66\u4e00\u4f75\u8209\u767c (\u8b66\u65b9\u63d0\u4f9b)"},{"videoId":"0uPlixq-7l4","pic":"https:\/\/img.ltn.com.tw\/Upload\/Module\/3\/710\/2709137.jpg","url":"https:\/\/video.ltn.com.tw\/article\/0uPlixq-7l4\/PLI7xntdRxhw3Qcbd70QE2FRWgpOQ-hBHO","title":"\u65b0\u805e360\u300b\u539f\u6c11\u72e9\u7375\u932f\u4e86\u55ce\uff1f\u7279\u8d66\u5f8c\u539f\u5718\u558a\u8a71\uff1a\u5feb\u505a\u4e00\u4ef6\u4e8b\n"},{"videoId":"mt3iq9EVegc","pic":"https:\/\/img.ltn.com.tw\/Upload\/Module\/3\/709\/2708935.jpg","url":"https:\/\/video.ltn.com.tw\/article\/mt3iq9EVegc\/PLI7xntdRxhw3Qcbd70QE2FRWgpOQ-hBHO","title":"\u540c\u9910\u5ef3\u4e0d\u540c\u5305\u5ec2\u4e5f\u78ba\u8a3a\uff01\u9ad8\u96c4\u51fa\u73fe\u9996\u8d77\u9910\u5ef3\u7fa4\u805a\u611f\u67d3\u6848\u4ef6"},{"videoId":"cWdUXuCBt-4","pic":"https:\/\/img.ltn.com.tw\/Upload\/Module\/3\/709\/2708934.jpg","url":"https:\/\/video.ltn.com.tw\/article\/cWdUXuCBt-4\/PLI7xntdRxhw3Qcbd70QE2FRWgpOQ-hBHO","title":"\u9673\u6642\u4e2d\u6307\u65b0\u5317\u7be9\u6aa2\u6578\u5c11 \u4faf\u53cb\u5b9c\uff1a\u660e\u518d\u8a2d3\u8655\u5feb\u7be9\u7ad9"}]; //指定影片ID
        var count = Math.floor(Math.random() * 5); //回傳0或1或2或3或4
        var play = false; //是否播放
        $('div.pc_YouTube').find('a.linkMask').attr({
            'href' : videoData[count]['url'],
            'data-desc' : videoData[count]['title'],
            'title' : videoData[count]['title'],
        });
        $('div.pc_YouTube').find('p.videoLiveTit').html(videoData[count]['title']);
        $(function() {
            writeLtnVideoNews(videoData, count); //一開始先排除第一則影片去隨機取一篇
        });
        function newVideoBoxApi() {
            var player = new YT.Player('muteYouTubeVideoPlayer', {
                videoId: videoData[count]['videoId'], // YouTube 影片 ID
                width: 440, // 播放器寬度 (in px)
                height: 247, // 播放器長度 (in px)
                playerVars: {
                    autoplay: 0, // 取消自動播放功能
                    controls: 0, // 顯示播放/暫停按鈕
                    showinfo: 0, // 隱藏影片標題
                    modestbranding: 1, // 隱藏YouTube LOGO
                    loop: 0, // 循環播放
                    cc_load_policty: 0, // 隱藏關閉字幕
                    iv_load_policy: 3, // 隱藏影片註釋
                    autohide: 1, // 播放時隱藏影片控制按鈕
                    rel: 0, //不顯示相關影片
                    fs: 0, //隱藏全螢幕按鈕
                },
                events: {
                    onReady: function(e) {
                        if (!navigator.userAgent.match(/(iphone|ipad|ipod);?/i) && $('.pc_YouTube').css('display') != 'none') {
                            play = true;
                        }
                        playAndMute(e, play);
                        $('.news2').on('click', '#videoBtnPrev', function(){
                            count = prevVideo(e, videoData, count, play);
                        });
                        $('.news2').on('click', '#videoBtnNext', function(){
                            count = nextVideo(e, videoData, count, play);
                        });
                    },
                    onStateChange: function(e){
                        if (e.data === 0) {
                            count = nextVideo(e, videoData, count, play);
                        }
                    }
                }
            });
        }

        //播放且靜音
        function playAndMute(e, play)
        {
            if (play) {
                e.target.playVideo();
            }
            e.target.mute(); // 靜音
        }

        //除了正在播放的影片以外隨機取一則放在自由影音Video左側區塊
        function writeLtnVideoNews(videoData, count)
        {
            var othervideoData = videoData.slice(0); //copy
            othervideoData.splice(count, 1);
            var randIdx = Math.floor(Math.random() * 4);
            var url = othervideoData[randIdx]['url'];
            var pic = othervideoData[randIdx]['pic'];
            var vid = othervideoData[randIdx]['videoId'];
            var title = othervideoData[randIdx]['title'];
            $('.ltn_video .big_v #boxVideoUrl').attr('href', url);
            $('.ltn_video .big_v #boxVideoUrl').attr('title', title);
            $('.ltn_video .big_v #boxVideoUrl').attr('data-desc', 'P:0:' + title);
            $('.ltn_video .big_v #boxVideoImg').attr('src', pic);
            $('.ltn_video .big_v #boxVideoImg').attr('alt', title);
            $('.ltn_video .big_v #boxVideoImg').attr('title', title);
            $('.ltn_video .big_v #boxVideoTitle').text(title);
        }

        //下一則
        function nextVideo(e, videoData, count, play)
        {
            count++;
            if (count >= videoData.length) {
                count = 0;
            }
            e.target.cueVideoById(videoData[count]['videoId']);
            playAndMute(e, play);
            $('div.pc_YouTube').find('a.linkMask').attr({
                'href' : videoData[count]['url'],
                'data-desc' : videoData[count]['title'],
                'title' : videoData[count]['title'],
            });
            $('div.pc_YouTube').find('p.videoLiveTit').html(videoData[count]['title']);
            writeLtnVideoNews(videoData, count);
            return count;
        }

        //上一則
        function prevVideo(e, videoData, count, play)
        {
            count--;
            if (count < 0) {
                count = videoData.length - 1;
            }
            e.target.cueVideoById(videoData[count]['videoId']);
            playAndMute(e, play);
            $('div.pc_YouTube').find('a.linkMask').attr({
                'href' : videoData[count]['url'],
                'data-desc' : videoData[count]['title'],
                'title' : videoData[count]['title'],
            });
            $('div.pc_YouTube').find('p.videoLiveTit').html(videoData[count]['title']);
            writeLtnVideoNews(videoData, count);

            return count;
        }
        // Written by @labnol
    

            var swiperVideo = initSwiperVideo(); //影音框1 Swiper
            swiperVideo.slideTo(count + 1, 0);

            $(window).resize(function(){
                swiperVideo.destroy();
                swiperVideo = initSwiperVideo();
                swiperVideo.slideTo(count + 1, 0);
            });

            function initSwiperVideo()
            {
                return new Swiper('#news2_video .swiper-container', {
                    direction: 'horizontal',
                    slidesPerView: 1,
                    spaceBetween: 0,
                    loop : true,
                    navigation: {
                        nextEl: '.news2 .ltn_video .swiper-button-next',
                        prevEl: '.news2 .ltn_video .swiper-button-prev',
                    },
                    autoplay: {
                        delay: 8000,//8秒切换一次
                    },
                });
            }
    
 displayDFP('ad-B2', 'm'); 
 displayDFP('ad-B3', 'm'); 
 displayDFP('ad-B4', 'm'); 

    $(function(){
        $("div.breakingnews > ul > li > a.L1ad").each(function () {
            var adHref = $(this).attr('href');
            $(this).attr('href', adHref + '&device=' + adDevice + '&source=' + document.URL);
        });
    });


        $(function(){
            var maxWidth = 828;
            var swiperLive = initSwiperLive(maxWidth); //自由影音 Swiper

            $(window).resize(function(e){
                swiperLive.destroy();
                swiperLive = initSwiperLive(maxWidth);
            });
        });
        function initSwiperLive(maxWidth)
        {
            var direct, perView;
            if ($(window).width() <= maxWidth) {
                direct = 'horizontal';
                perView = 1;
                spacebetween = 0;
            } else {
                direct = 'vertical';
                perView = 2;
                spacebetween = 9;
            }
            return new Swiper('#ltn_video .swiper-container', {
                direction: direct,
                slidesPerView: perView,
                spaceBetween: spacebetween,
                loop : true,
                mousewheel : true,
                pagination: {
                    el: '#ltn_video .swiper-pagination',
                    clickable: true,
                },
                autoplay: {
                    delay: 3000,//3秒切换一次
                },
            });
        }
    

    $(function(){
        $('li.adMarket').find('a').each(function () {
            var adHref = $(this).attr('href');
            $(this).attr('href', adHref + '&device=' + adDevice + '&source=' + document.URL);
        });
    });


    $(function () {
        var cover_legislature_ads = setTimeout("$('.gov_live .boxTitle .legislature_cover').hide()", 35000);
    })


        $(function () {
            $('.foraward').hide();
            $.extend({
                right: function (s, n) {
                    if (n <= 0) {
                        return "";
                    } else if (n > s.length) {
                        return s;
                    } else {
                        var iLen = s.length;
                        return s.substring(iLen, iLen - n);
                    }

                },
                left: function (s, n) {

                    if (n <= 0) {
                        return "";
                    } else if (n > s.length) {
                        return s;
                    } else {
                        return s.substring(0, n);
                    }

                },
                mid: function (s, starnum, endnum) {
                    return s.substr(starnum, endnum);
                }
            });

            var itemData = [{"time":"110-01-02","data":[{"note":"\u7279\u5225\u734e","no":"80325690","type":"A"},{"note":"\u7279\u734e","no":"95201943","type":"A"},{"note":"\u982d\u734e","no":"64613291","type":"B"},{"note":"\u982d\u734e","no":"00581856","type":"B"},{"note":"\u982d\u734e","no":"63105417","type":"B"},{"note":"\u589e\u958b\u516d\u734e","no":"295","type":"C"}],"starttime":"110-04-06","overtime":"110-07-05"},{"time":"109-11-12","data":[{"note":"\u7279\u5225\u734e","no":"77815838","type":"A"},{"note":"\u7279\u734e","no":"39993297","type":"A"},{"note":"\u982d\u734e","no":"59028801","type":"B"},{"note":"\u982d\u734e","no":"02813820","type":"B"},{"note":"\u982d\u734e","no":"06896234","type":"B"},{"note":"\u589e\u958b\u516d\u734e","no":"011","type":"C"},{"note":"\u589e\u958b\u516d\u734e","no":"427","type":"C"}],"starttime":"110-02-06","overtime":"110-05-05"}];

            var item1 = itemData[0]['data'];
            var item2 = itemData[1]['data'];

            var mk = [0, item1, item2];

            $('.invoice #tab .j-tab-nav').on('click', 'a', function () {
                var idx = $.right($(this).attr('id'), 1)-0*1;
                $('#lottery' + idx).parent('.tab-con-item').show().siblings().hide();
                $('#date_award' + idx).show().siblings('.date_award').hide();
                var str = '最新:開啟對獎功能';
                if (idx == 2) {
                    str = '上次:開啟對獎功能';
                }
                $('#redemption').data('desc', str);
                data = mk[idx];
                chang_data();
                $input.val('');
                move.css({ 'margin-top': 0 });

            });

            $('.lottery-over-time-close').on('click', function () {
                $('.lottery-over-time').hide();
            });

            $("#lot1").show();

            var data = mk[1];

            var $root = $('.foraward');
            var $input = $('.foraward .for_award_no');

            var time;
            var move = $('.lst_award_move');

            var isclose = true;

            $('.foraward_sw').on('click', function () {
                if (isclose) {
                    $(this).text('關閉對獎功能');
                    isclose = false;
                    $('.foraward').show().animate({
                        opacity: 1,
                        height: 485
                    }, 500);
                    load_init();
                } else {
                    $(this).text('開啟對獎功能');
                    isclose = true;
                    $('.foraward').animate({
                        opacity: 0,
                        height: 1
                    }, 500, function () {
                        $('.foraward').hide();
                    });
                }
            });

            //run_d4open();

            function run_d4open()
            {
                $('.foraward_sw').text('關閉對獎功能');
                isclose = false;
                $('.foraward').show().css({
                    opacity: 0.95,
                    height: 500
                });
                load_init();
            }

            $root.on('click.clear', '.clear_text', function () {
                //清除文字
                $input.val('');
                move.css({ 'margin-top': 0 });
            }).on('click.input', '.input_no', function () {
                //輸入文字
                add_no($(this).val());
            }).on('keydown', '.for_award_no', function (e) {
                //手動輸入
                var code = e.which;

            });

            /*
            type desc
            A:完全符合
            B:{
                完全符合, 中20萬元
                末7碼, 中4萬元
                末6碼, 中1萬元
                末5碼, 中4千元
                末4碼, 中1千元
                末3碼, 中2百元
            }
            C:末3碼, 中2百元
            */

            function chang_data()
            {
                var lst_award_no_items = '';
                each_data(function (obj, idx) {
                    var no =  (obj.no.length == 8) ? $.left(obj.no, 5) + '<b>' + $.right(obj.no, 3) + '</b>' : '<b>' + obj.no + '</b>';
                    $('.lst_award_no_item' + idx).html('<span>' + obj.note + '</span>'+no);

                    if ($('.lst_award_no .lst_award_no_item' + idx) . length <= 0) {
                        lst_award_no_items += '<div class="lst_award_no_item lst_award_no_item' + idx + '"><span>' + obj.note + '</span>' + no + '</div>';
                        $('.foraward .lst_award_no .lst_award_move').append(lst_award_no_items);
                    }
                });
            }
            var isinit = false;
            function load_init()
            {
                if (isinit) {
                    chang_data();
                    return;
                }

                isinit = true;

                var lst_award_no_items = '';

                each_data(function (obj, idx) {
                    var no = (obj.no.length == 8) ? $.left(obj.no, 5) + '<b>' + $.right(obj.no, 3) + '</b>' : '<b>' + obj.no + '</b>';
                    lst_award_no_items += '<div class="lst_award_no_item lst_award_no_item' + idx + '"><span>' + obj.note + '</span>' + no + '</div>';
                });

                $('.foraward .lst_award_no .lst_award_move').append(lst_award_no_items);
            }


            function each_data(fn)
            {
                for (var idx in data) {
                    var obj = data[idx];
                    fn(obj, idx);
                }
            }

            function merge_no(v, fn)
            {
                /*
                len<=0 && len>8, 不處理
                len=1, 比對倒數第三個數字
                len=2, 比對倒數第三個及第二個數字
                len=3, 比對後面三個數字
                len=4, 比對後面四個數字
                len=5, 比對後面五個數字
                len=6, 比對後面六個數字
                len=7, 比對後面七個數字
                len=8, 比對後面八個數字
                */
                var len = v.length;
                if (len <= 0 && len > 8) {
                    return;
                }

                for (var idx in data) {
                    var obj = data[idx];
                    if (_merge_no(obj, len, v)) {
                        return fn(obj,idx);
                    }
                }
                return fn(null, -1);
            }

            function _merge_no(obj, len, v)
            {
                if (len == 1) {
                    return $.left($.right(obj.no, 3), 1) == v ? true : false;
                } else if (len == 2) {
                    return $.left($.right(obj.no, 3), 2) == v ? true : false;
                } else {
                    //console.log(v);
                    return $.right(obj.no, 3) == $.right(v, 3) ? true : false;
                }
            }

            function add_no(no)
            {
                var v = $input.val();
                if (v.length == 8) {
                    return;
                }

                if (v.length < 3) {
                    //加後面
                    v += '' + no;
                } else {
                    //加前面
                    v = no+''+v;
                }
                $input.val(v);
                if (time) {
                    clearTimeout(time);
                }
                setTimeout(function () {
                    merge_no(v, function (obj, idx) {
                        var moveTop = 0;
                        if (idx == -1) {
                            //沒中
                            //moveTop = 45;
                            //console.log(idx);
                            $('.lst_award_no_item').each(function () {
                                var item = $(this);
                                if (item.hasClass('lst_award_no_item_next')) {
                                    return false;
                                }
                                moveTop += item.outerHeight(true);
                            });

                        } else {
                            //moveTop = 45*(idx-0+2);
                            //console.log(idx);
                            //移到中獎位置
                            $('.lst_award_no_item').each(function () {
                                var item = $(this);
                                if (item.hasClass('lst_award_no_item' + idx)) {
                                    return false;
                                }
                                moveTop+=item.outerHeight(true);
                            });
                        }
                        //console.log(obj);
                        //console.log(idx);
                        //console.log(moveTop);
                        move.css({ 'margin-top': 0-moveTop });

                    });
                }, 100);
            }
        });
    

    $(function() {
        showRandomAgoodItem();
        // 隨機出一則
        function showRandomAgoodItem() {
            var agood_items = $('.agoods').find('.agood_item');
            var random_index = Math.floor(Math.random() * agood_items.length);
            $(agood_items[random_index]).css('display', 'block');
        }
    })
    

                $(document).ready(function() {
                    window.setTimeout(function(){
                        $('#hot_keyword_area').children().each(function() {
                            if ( $(this).attr("class") == 'w10' ||
                                $(this).attr("class") == 'w9' ||
                                $(this).attr("class") == 'w8' ||
                                $(this).attr("class") == 'w7' ||
                                $(this).attr("class") == 'w6')
                            {
                                var colorbase = ["#e60017", "#8a541f", "#00791C", "#C56202", "#CB18BB","#000000"];
                                var cols = [];
                                cols = hotkeyword_shuffle(colorbase);
                                var cPos = 0;
                                swapC($(this), cols, cPos);
                            }
                        });
                    }, 500);
                });

                function swapC(dom, cols, cPos)
                {
                    var move_sec = ( Math.floor((Math.random() * 3) + 1) * 500 );
                    dom.animate(
                        {
                            color: cols[cPos]
                        },
                        500
                    );

                    cPos++;
                    if (cPos == cols.length)
                    {
                        cPos = 0;
                    }
                    window.setTimeout(function(){
                        swapC(dom, cols, cPos);
                    }, move_sec);
                }

                function hotkeyword_shuffle(o)
                {
                    for(var j, x, i = o.length; i; j = Math.floor(Math.random() * i), x = o[--i], o[i] = o[j], o[j] = x);
                    return o;
                };

                var hot_keyword_words = [{"text":"\u6b66\u6f22\u80ba\u708e","weight":19,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u6b66\u6f22\u80ba\u708e","data-desc":"\u6b66\u6f22\u80ba\u708e","title":"\u6b66\u6f22\u80ba\u708e"},"html":{"data-desc":"\u6b66\u6f22\u80ba\u708e"}},{"text":"COVID-19","weight":18,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/COVID-19","data-desc":"COVID-19","title":"COVID-19"},"html":{"data-desc":"COVID-19"}},{"text":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2","weight":17,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2","data-desc":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2","title":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2"},"html":{"data-desc":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2"}},{"text":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2\u75c5","weight":16,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2\u75c5","data-desc":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2\u75c5","title":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2\u75c5"},"html":{"data-desc":"\u65b0\u578b\u51a0\u72c0\u75c5\u6bd2\u75c5"}},{"text":"\u68d2\u7403","weight":15,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u68d2\u7403","data-desc":"\u68d2\u7403","title":"\u68d2\u7403"},"html":{"data-desc":"\u68d2\u7403"}},{"text":"\u9632\u75ab","weight":14,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u9632\u75ab","data-desc":"\u9632\u75ab","title":"\u9632\u75ab"},"html":{"data-desc":"\u9632\u75ab"}},{"text":"\u65e5\u8077","weight":13,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u65e5\u8077","data-desc":"\u65e5\u8077","title":"\u65e5\u8077"},"html":{"data-desc":"\u65e5\u8077"}},{"text":"MLB","weight":12,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/MLB","data-desc":"MLB","title":"MLB"},"html":{"data-desc":"MLB"}},{"text":"\u75ab\u60c5","weight":11,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u75ab\u60c5","data-desc":"\u75ab\u60c5","title":"\u75ab\u60c5"},"html":{"data-desc":"\u75ab\u60c5"}},{"text":"\u9632\u75ab\u5347\u7d1a","weight":10,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u9632\u75ab\u5347\u7d1a","data-desc":"\u9632\u75ab\u5347\u7d1a","title":"\u9632\u75ab\u5347\u7d1a"},"html":{"data-desc":"\u9632\u75ab\u5347\u7d1a"}},{"text":"\u505c\u96fb","weight":9,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u505c\u96fb","data-desc":"\u505c\u96fb","title":"\u505c\u96fb"},"html":{"data-desc":"\u505c\u96fb"}},{"text":"\u672c\u571f\u75ab\u60c5\u7206\u767c","weight":8,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u672c\u571f\u75ab\u60c5\u7206\u767c","data-desc":"\u672c\u571f\u75ab\u60c5\u7206\u767c","title":"\u672c\u571f\u75ab\u60c5\u7206\u767c"},"html":{"data-desc":"\u672c\u571f\u75ab\u60c5\u7206\u767c"}},{"text":"\u75ab\u60c5\u5347\u6eab","weight":7,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u75ab\u60c5\u5347\u6eab","data-desc":"\u75ab\u60c5\u5347\u6eab","title":"\u75ab\u60c5\u5347\u6eab"},"html":{"data-desc":"\u75ab\u60c5\u5347\u6eab"}},{"text":"\u4e09\u7d1a\u8b66\u6212","weight":6,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u4e09\u7d1a\u8b66\u6212","data-desc":"\u4e09\u7d1a\u8b66\u6212","title":"\u4e09\u7d1a\u8b66\u6212"},"html":{"data-desc":"\u4e09\u7d1a\u8b66\u6212"}},{"text":"\u53f0\u7063","weight":5,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u53f0\u7063","data-desc":"\u53f0\u7063","title":"\u53f0\u7063"},"html":{"data-desc":"\u53f0\u7063"}},{"text":"\u8208\u9054\u96fb\u5ee0","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u8208\u9054\u96fb\u5ee0","data-desc":"\u8208\u9054\u96fb\u5ee0","title":"\u8208\u9054\u96fb\u5ee0"},"html":{"data-desc":"\u8208\u9054\u96fb\u5ee0"}},{"text":"\u78ba\u8a3a","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u78ba\u8a3a","data-desc":"\u78ba\u8a3a","title":"\u78ba\u8a3a"},"html":{"data-desc":"\u78ba\u8a3a"}},{"text":"\u4ee5\u8272\u5217","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u4ee5\u8272\u5217","data-desc":"\u4ee5\u8272\u5217","title":"\u4ee5\u8272\u5217"},"html":{"data-desc":"\u4ee5\u8272\u5217"}},{"text":"\u5929\u6c23","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u5929\u6c23","data-desc":"\u5929\u6c23","title":"\u5929\u6c23"},"html":{"data-desc":"\u5929\u6c23"}},{"text":"\u4e2d\u570b","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u4e2d\u570b","data-desc":"\u4e2d\u570b","title":"\u4e2d\u570b"},"html":{"data-desc":"\u4e2d\u570b"}},{"text":"\u53f0\u96fb","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u53f0\u96fb","data-desc":"\u53f0\u96fb","title":"\u53f0\u96fb"},"html":{"data-desc":"\u53f0\u96fb"}},{"text":"\u75ab\u82d7","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u75ab\u82d7","data-desc":"\u75ab\u82d7","title":"\u75ab\u82d7"},"html":{"data-desc":"\u75ab\u82d7"}},{"text":"\u5927\u8c37\u7fd4\u5e73","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u5927\u8c37\u7fd4\u5e73","data-desc":"\u5927\u8c37\u7fd4\u5e73","title":"\u5927\u8c37\u7fd4\u5e73"},"html":{"data-desc":"\u5927\u8c37\u7fd4\u5e73"}},{"text":"\u505c\u8ab2","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u505c\u8ab2","data-desc":"\u505c\u8ab2","title":"\u505c\u8ab2"},"html":{"data-desc":"\u505c\u8ab2"}},{"text":"\u5df4\u52d2\u65af\u5766","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u5df4\u52d2\u65af\u5766","data-desc":"\u5df4\u52d2\u65af\u5766","title":"\u5df4\u52d2\u65af\u5766"},"html":{"data-desc":"\u5df4\u52d2\u65af\u5766"}},{"text":"\u53f0\u80a1","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u53f0\u80a1","data-desc":"\u53f0\u80a1","title":"\u53f0\u80a1"},"html":{"data-desc":"\u53f0\u80a1"}},{"text":"\u738b\u67cf\u878d","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u738b\u67cf\u878d","data-desc":"\u738b\u67cf\u878d","title":"\u738b\u67cf\u878d"},"html":{"data-desc":"\u738b\u67cf\u878d"}},{"text":"\u4e2d\u8077","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u4e2d\u8077","data-desc":"\u4e2d\u8077","title":"\u4e2d\u8077"},"html":{"data-desc":"\u4e2d\u8077"}},{"text":"\u78ba\u8a3a\u8db3\u8de1","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u78ba\u8a3a\u8db3\u8de1","data-desc":"\u78ba\u8a3a\u8db3\u8de1","title":"\u78ba\u8a3a\u8db3\u8de1"},"html":{"data-desc":"\u78ba\u8a3a\u8db3\u8de1"}},{"text":"\u5be6\u806f\u5236","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u5be6\u806f\u5236","data-desc":"\u5be6\u806f\u5236","title":"\u5be6\u806f\u5236"},"html":{"data-desc":"\u5be6\u806f\u5236"}},{"text":"\u842c\u83ef\u963f\u516c\u5e97","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u842c\u83ef\u963f\u516c\u5e97","data-desc":"\u842c\u83ef\u963f\u516c\u5e97","title":"\u842c\u83ef\u963f\u516c\u5e97"},"html":{"data-desc":"\u842c\u83ef\u963f\u516c\u5e97"}},{"text":"\u570b\u4e2d\u6703\u8003","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u570b\u4e2d\u6703\u8003","data-desc":"\u570b\u4e2d\u6703\u8003","title":"\u570b\u4e2d\u6703\u8003"},"html":{"data-desc":"\u570b\u4e2d\u6703\u8003"}},{"text":"\u7f8e\u570b","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u7f8e\u570b","data-desc":"\u7f8e\u570b","title":"\u7f8e\u570b"},"html":{"data-desc":"\u7f8e\u570b"}},{"text":"\u54c8\u746a\u65af","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u54c8\u746a\u65af","data-desc":"\u54c8\u746a\u65af","title":"\u54c8\u746a\u65af"},"html":{"data-desc":"\u54c8\u746a\u65af"}},{"text":"\u5feb\u7be9","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u5feb\u7be9","data-desc":"\u5feb\u7be9","title":"\u5feb\u7be9"},"html":{"data-desc":"\u5feb\u7be9"}},{"text":"\u65b0\u805e360","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u65b0\u805e360","data-desc":"\u65b0\u805e360","title":"\u65b0\u805e360"},"html":{"data-desc":"\u65b0\u805e360"}},{"text":"\u842c\u83ef","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u842c\u83ef","data-desc":"\u842c\u83ef","title":"\u842c\u83ef"},"html":{"data-desc":"\u842c\u83ef"}},{"text":"\u8db3\u8de1","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u8db3\u8de1","data-desc":"\u8db3\u8de1","title":"\u8db3\u8de1"},"html":{"data-desc":"\u8db3\u8de1"}},{"text":"\u516b\u5927\u884c\u696d","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/\u516b\u5927\u884c\u696d","data-desc":"\u516b\u5927\u884c\u696d","title":"\u516b\u5927\u884c\u696d"},"html":{"data-desc":"\u516b\u5927\u884c\u696d"}},{"text":"NBA","weight":4,"link":{"href":"https:\/\/news.ltn.com.tw\/topic\/NBA","data-desc":"NBA","title":"NBA"},"html":{"data-desc":"NBA"}}];
                $('#hot_keyword_area').jQCloud(
                    hot_keyword_words,
                    {
                        colors: ["#e60017", "#8a541f", "#f69757", "#7acd8d", "#37b6d1", "#977BE4", "#888888"],
                        delay : 1,
                        center: {x:0.4,y:0.5},
                        autoResize: true,
                        shape: 'rectangular',
                        fontSize: {
                            from: 0.11,
                            to: 0.04
                        }
                    }
                );
            

    $(function(){
        /* 手機版切換 */
        $("#tom, #tomf").click(function() {
            cookies_m.write('MOBILE');
            setTimeout('gotoMobile_cache()', 800);
        });
    });

    function gotoMobile_cache() {
        $(window).scrollTop(0);
        location.reload();
    }


    var idleAds = {
    // 'IB1':['/21202031/01-news-idle-B1', [300, 250], 'ad-IB1'],
    'IC1':['/21202031/01-news-idle-C1', [300, 100], 'ad-IC1']
};


        window.ppnio = window.ppnio || [];


    $(function(){
        try {
            getScrNews(newsServer, '', '', '');
        }catch(e) {

        }
    });


        if ($(window).width() > 856 && window.innityShowTag) {
            innityShowTag();
        }
        // 處理圖片延遲
        $(document).ready(function(){
            lazyImg = $('img.lazy_imgs_ltn');
            lazyload(lazyImg);
        });
    