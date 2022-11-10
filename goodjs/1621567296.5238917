var CstHistoryDomain  = "https://history.kakaku.com";

var isHistoryReady = false;
var pushcallback = function() {
 if (typeof jQuery === "undefined") return;
 if (isHistoryReady) {
  historyPush.init(jQuery);
 }
};

// load
if(window.addEventListener) {
 window.addEventListener('load', pushcallback, false);
} else if(window.attachEvent) {
 window.attachEvent('onload', pushcallback);
} else {
 window.onload = function() {
  pushcallback();
 };
}

document.addEventListener('DOMContentLoaded', function() {
 if (typeof jQuery === "undefined") return;
 window.addEventListener('message', function(event) {
  //push ready ok
  if (event.origin !== CstHistoryDomain) return;
  var response;
  try { response = JSON.parse(event.data || '{}'); } catch(e) { return; }
  if (response == null || response.Controler !== 'pushready') return;
  isHistoryReady = true;
 });
});

// namespace
var historyPush = window.historyPush || {};
new function() {
 var $historyfrm;
 var initialized = false;
 
 historyPush = {
  init: function($) {
   if (initialized) return;
   initialized = true;
   if (typeof s == "undefined") return;
   $('head link:last').after('<link rel="stylesheet" type="text/css" href="//css1.kakaku.k-img.com/css/push.css" media="all">');
   var param = {
    Controler: 'push',
    Referrer: document.referrer,
    Location: location.href,
    Identifier: s.prop1,
    CategoryName: s.prop20,
   };
   try {
    $historyfrm = $('iframe[src *= "/history/cookie2ls/"]')[0];
    if ($historyfrm == null) {
     var $idcorefrm = $('iframe[src *= "/auth/inc_idcore_top_v2.asp"]')[0];
     if ($idcorefrm != null) {
      var idcoredoc = $idcorefrm.contentWindow.document;
      $historyfrm = $('iframe[src *= "/history/cookie2ls/"]', idcoredoc)[0];
     }
    }
    if ($historyfrm != null) $historyfrm.contentWindow.postMessage(JSON.stringify(param), CstHistoryDomain);
   } catch(e) {}

   window.addEventListener('message', function(event) {
    if (event.origin !== CstHistoryDomain) return;
    var response;
    try { response = JSON.parse(event.data || '{}'); } catch(e) { return; }
    if (response == null || response.Controler !== 'push') return;
    var $content = $(response.ResponseText);
    $('body').append($content);
    historyPush.setPushAfterEvent($, response.CompactView);
    $content.ready(function() {
     var nodispFlg = $('#pushSplitData').attr('data-splitnodisp') === "1";
     if (!nodispFlg) pushEffect.init($, response.CompactView);
    });
   }, false);
  },
  setPushOnclickCatalystEvent: function($) {
   $('.onclickPushFunc').click(function() {
    var funcName = $(this).attr('data-onclickfunc');
    onclickcatalyst_pushfunction(funcName);
    return true;
   });
  },
  setPushAfterEvent: function($, compactView) {
   historyPush.setPushOnclickCatalystEvent($);
   var splitpattern = $('#pushSplitData').attr('data-splitpattern');
   if (!compactView) {
    if (splitpattern === "A") {
     onclickcatalyst_pushtest_A();
    } else if (splitpattern === "B") {
     onclickcatalyst_pushtest_B();
    }
   }
   $('div.pushCompareLink').click(function() {
    var param = {
     Controler: 'pushitemview',
     Product: $(this).attr('data-product'),
    };
    $historyfrm.contentWindow.postMessage(JSON.stringify(param), CstHistoryDomain)
    return true;
   });
   $('div.pushMallLink').click(function() {
    var param = {
     Controler: 'pushmallshop',
     Mallkey: $(this).attr('data-mallkey'),
     Price: $(this).attr('data-price'),
    };
    $historyfrm.contentWindow.postMessage(JSON.stringify(param), CstHistoryDomain)
    return true;
   });
   $('span.pushPriceDownClose').click(function() { 
    var param = { Controler: 'pushclose' };
    $historyfrm.contentWindow.postMessage(JSON.stringify(param), CstHistoryDomain)
    return true;
   });
  },
 }
}
// namespace
var pushEffect = window.pushEffect || {};
new function() {
 pushEffect = {
  init: function($, compactView) {
   if($('.is-jack')[0]) return;
   
   //通知外枠
   var pushPriceDownWrp = $('.pushPriceDownWrp');
   
   //通知枠初期表示のサイズ取得・高さ設定
   var pushPriceDownInnr = pushPriceDownWrp.find('.pushPriceDownInnr');
   var pushPriceBigW = pushPriceDownInnr.width();
   var pushPriceBigH = pushPriceDownInnr.height();
   pushPriceDownInnr.css('height', pushPriceBigH + 'px');
   
   //通知枠縮小時のサイズ取得
   var pushPriceDownS = pushPriceDownWrp.find('.pushPriceDownS');
   var pushPriceSmallW = pushPriceDownS.outerWidth() + 13;
   var pushPriceSmallH = pushPriceDownS.outerHeight() + 1;
   
   //通知枠初期表示
   if (compactView) {
    $('.pushPriceDownL').hide();
    pushPriceDownInnr.css({width: pushPriceSmallW, height: pushPriceSmallH});
    pushPriceDownS.show();
    pushPriceDownWrp.addClass('typeBig');
    pushPriceDownWrp.css({'left': '10px'});
   } else {
    pushPriceDownWrp.animate({
     'left': '10px'
    }, 300, 'swing', function () {
     toPushSmall();
    });
   }

   //通知枠縮小時押下で元のサイズへ戻す
   pushPriceDownS.click(function(){
    pushPriceDownS.hide();
    pushPriceDownInnr.animate({ 
     width: pushPriceBigW + 'px',
     height: pushPriceBigH + 'px'
    }, 300, function(){
     $('.pushPriceDownL').show();
     pushPriceDownWrp.removeClass('typeBig');
     toPushSmall();
    } )
   });
   
   //閉じるボタン押下
   $('.pushPriceDownClose').click(function(){
    pushPriceDownWrp.animate({
     'left': '-400px'
    }, 300, 'swing');
   });
   
   //通知枠内ビガーリンク
   $('.pushPriceDownLink1, .pushPriceDownLink2').hover(
    function(){
     $(this).addClass('hov');
    },function(){
     $(this).removeClass('hov');
    }
   ).click(function(){
    var url = $(this).find('a').attr('href');
    if($(this).find('a').attr('target') === '_blank'){
     window.open(url, '_blank');
    } else {
     window.location.href = url;
    }
    return false;
   });
   
   //通知枠15秒後に縮小
   function toPushSmall(){
    setTimeout(function() {
     $('.pushPriceDownL').hide();
     pushPriceDownInnr.animate({ 
      width: pushPriceSmallW,
      height: pushPriceSmallH
     }, 300, function(){
      pushPriceDownS.show();
      pushPriceDownWrp.addClass('typeBig');
     })
    }, 15000);
   }
  }
 }
}