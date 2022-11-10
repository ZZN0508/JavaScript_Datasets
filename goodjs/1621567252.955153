 var ue_t0=window.ue_t0||+new Date();
 

        if (window.Mobvious === undefined) {
          window.Mobvious = {};
        }
        window.Mobvious.device_type = 'desktop';
        

//<![CDATA[

  WebFont.load({
    classes: false,
    custom: {
      families: ["Lato:n4,n7,i4", "Merriweather:n4,n7,i4"],
      urls: ["https://s.gr-assets.com/assets/gr/fonts-e256f84093cc13b27f5b82343398031a.css"]
    }
  });

//]]>


  //<![CDATA[
    var gptAdSlots = gptAdSlots || [];
    var googletag = googletag || {};
    googletag.cmd = googletag.cmd || [];
    (function() {
      var gads = document.createElement("script");
      gads.async = true;
      gads.type = "text/javascript";
      var useSSL = "https:" == document.location.protocol;
      gads.src = (useSSL ? "https:" : "http:") +
      "//securepubads.g.doubleclick.net/tag/js/gpt.js";
      var node = document.getElementsByTagName("script")[0];
      node.parentNode.insertBefore(gads, node);
    })();
    // page settings
  //]]>


  //<![CDATA[
    googletag.cmd.push(function() {
      googletag.pubads().setTargeting("sid", "osid.d74df58b4798a81bcec724764bb5a2f5");
    googletag.pubads().setTargeting("grsession", "osid.d74df58b4798a81bcec724764bb5a2f5");
    googletag.pubads().setTargeting("surface", "desktop");
    googletag.pubads().setTargeting("signedin", "false");
    googletag.pubads().setTargeting("gr_author", "false");
    googletag.pubads().setTargeting("author", []);
      googletag.pubads().enableAsyncRendering();
      googletag.pubads().enableSingleRequest();
      googletag.pubads().collapseEmptyDivs(true);
      googletag.pubads().disableInitialLoad();
      googletag.enableServices();
    });
  //]]>


  //<![CDATA[
    ! function(a9, a, p, s, t, A, g) {
      if (a[a9]) return;
    
      function q(c, r) {
        a[a9]._Q.push([c, r])
      }
      a[a9] = {
      init: function() {
        q("i", arguments)
      },
      fetchBids: function() {
        q("f", arguments)
      },
      setDisplayBids: function() {},
        _Q: []
      };
      A = p.createElement(s);
      A.async = !0;
      A.src = t;
      g = p.getElementsByTagName(s)[0];
      g.parentNode.insertBefore(A, g)
    }("apstag", window, document, "script", "//c.amazon-adsystem.com/aax2/apstag.js");
    
    apstag.init({
      pubID: '3211', adServer: 'googletag', bidTimeout: 4e3, params: { aps_privacy: '1YN' }
    });
  //]]>


  //<![CDATA[
    var initializeGrfb = function() {
      $grfb.initialize({
        appId: "2415071772"
      });
    };
    if (typeof $grfb !== "undefined") {
      initializeGrfb();
    } else {
      window.addEventListener("DOMContentLoaded", function() {
        if (typeof $grfb !== "undefined") {
          initializeGrfb();
        }
      });
    }
  //]]>


  //<![CDATA[
    function loadScript(url, callback) {
      var script = document.createElement("script");
      script.type = "text/javascript";
    
      if (script.readyState) {  //Internet Explorer
          script.onreadystatechange = function() {
            if (script.readyState == "loaded" ||
                    script.readyState == "complete") {
              script.onreadystatechange = null;
              callback();
            }
          };
      } else {  //Other browsers
        script.onload = function() {
          callback();
        };
      }
    
      script.src = url;
      document.getElementsByTagName("head")[0].appendChild(script);
    }
    
    function initAppleId() {
      AppleID.auth.init({
        clientId : 'com.goodreads.app', 
        scope : 'name email',
        redirectURI: 'https://www.goodreads.com/apple_users/sign_in_with_apple_web',
        state: 'apple_oauth_state_e939b675-b32e-4758-9ed3-55c106b7049b'
      });
    }
    
    var initializeSiwa = function() {
      var APPLE_SIGN_IN_JS_URL =  "https://appleid.cdn-apple.com/appleauth/static/jsapi/appleid/1/en_US/appleid.auth.js"
      loadScript(APPLE_SIGN_IN_JS_URL, initAppleId);
    };
    if (typeof AppleID !== "undefined") {
      initAppleId();
    } else {
      initializeSiwa();
    }
  //]]>


//<![CDATA[  

  function submitShelfLink(unique_id, book_id, shelf_id, shelf_name, submit_form, exclusive) {
    var checkbox_id = 'shelf_name_' + unique_id + '_' + shelf_id;
    var element = document.getElementById(checkbox_id)

    var checked = element.checked
    if (checked && exclusive) {
      // can't uncheck a radio by clicking it!
      return
    }
    if(document.getElementById("savingMessage")){
      Element.show('savingMessage')
    }
    var element_id = 'shelfInDropdownName_' + unique_id + '_' + shelf_id;
    Element.update(element_id, "saving...");
    if (submit_form) {
      Element.hide('shelfDropdown_' + unique_id)
      var form = document.getElementById('addBookForm' + book_id)
      if (form) {
        form.shelf.value = shelf_name
        form.onsubmit()
      }
    }
    else {
      var action = checked ? 'remove' : ''
      element.checked = !element.checked
      new Ajax.Request('/shelf/add_to_shelf', {asynchronous:true, evalScripts:true, onSuccess:function(request){shelfSubmitted(request, book_id, checkbox_id, element_id, unique_id, shelf_name)}, parameters:'book_id=' + book_id + '&name=' + shelf_name + '&a=' + action + '&authenticity_token=' + encodeURIComponent('pHhXgq17jEFngtK0eUDxb7AYL+7wf9VzFG87SkSloZcGJadHVOAiKshyPEWegmOrkGNZywHTxMj+3ywo6HfBNw==')})
    }
  }

  function shelfSubmitted(request, book_id, checkbox_id, element_id, unique_id, shelf_name) {
    Element.update('shelfListfalse_' + book_id, request.responseText)
    afterShelfSave(checkbox_id, element_id, unique_id, shelf_name.escapeHTML())
  }

  function refreshGroupBox(group_id, book_id) {
    new Ajax.Updater('addGroupBooks' + book_id + '', '/group/add_book_box', {asynchronous:true, evalScripts:true, onSuccess:function(request){refreshGroupBoxComplete(request, book_id);}, parameters:'id=' + group_id + '&book_id=' + book_id + '&refresh=true' + '&authenticity_token=' + encodeURIComponent('/ye1krOcGa9G5d1PNNS9lKCgNt8vCX3smFiRL5zteexdekVXSge3xOkVM77TFi9QgNtA+t6lbFdy6IZNMD8ZTA==')})
  }
//]]>


//<![CDATA[
      var newTip = new Tip($('quote_book_link_30633'), "\n\n  <h2><a class=\"readable bookTitle\" href=\"https://www.goodreads.com/book/show/30633.The_Four_Loves?from_choice=false&amp;from_home_module=false\">The Four Loves<\/a><\/h2>\n\n      <div>\n        by <a class=\"authorName\" href=\"/author/show/1069006.C_S_Lewis\">C.S. Lewis<\/a>\n      <\/div>\n\n          <div class=\"smallText uitext darkGreyText\">\n            <span class=\"minirating\"><span class=\"stars staticStars notranslate\"><span size=\"12x12\" class=\"staticStar p10\"><\/span><span size=\"12x12\" class=\"staticStar p10\"><\/span><span size=\"12x12\" class=\"staticStar p10\"><\/span><span size=\"12x12\" class=\"staticStar p10\"><\/span><span size=\"12x12\" class=\"staticStar p3\"><\/span><\/span> 4.14 avg rating &mdash; 47,040 ratings<\/span>            &mdash; published 1960\n          <\/div>\n\n    <div class=\"addBookTipDescription\">\n      \n<span id=\"freeTextContainer9378433305417889905\">The Four Loves summarizes four kinds of human love--affection, friendship, erotic love, and the love of God. Masterful without being magisterial, this book&apos;s wise, gentle, candid reflections on the virtues and dangers of love draw on sources from Jan<\/span>\n  <span id=\"freeText9378433305417889905\" style=\"display:none\">The Four Loves summarizes four kinds of human love--affection, friendship, erotic love, and the love of God. Masterful without being magisterial, this book\'s wise, gentle, candid reflections on the virtues and dangers of love draw on sources from Jane Austen to St. Augustine. The chapter on charity (love of God) may be the best thing Lewis ever wrote about Christianity. Consider his reflection on Augustine\'s teaching that one must love only God, because only God is eternal, and all earthly love will someday pass away:  Who could conceivably begin to love God on such a prudential ground--because the security (so to speak) is better? Who could even include it among the grounds for loving? Would you choose a wife or a Friend--if it comes to that, would you choose a dog--in this spirit? One must be outside the world of love, of all loves, before one thus calculates.  His description of Christianity here is no less forceful and opinionated than in Mere Christianity or The Problem of Pain, but it is far less anxious about its reader\'s response--and therefore more persuasive than any of his apologetics. When he begins to describe the nature of faith, Lewis writes: &quot;Take it as one man\'s reverie, almost one man\'s myth. If anything in it is useful to you, use it; if anything is not, never give it a second thought.&quot; --Michael Joseph Gross<\/span>\n  <a data-text-id=\"9378433305417889905\" href=\"#\" onclick=\"swapContent(\$(this));; return false;\">...more<\/a>\n\n    <\/div>\n\n      <div class=\'wtrButtonContainer wtrSignedOut\' id=\'2_book_30633\'>\n<div class=\'wtrUp wtrLeft\'>\n<form action=\"/shelf/add_to_shelf\" accept-charset=\"UTF-8\" method=\"post\"><input name=\"utf8\" type=\"hidden\" value=\"&#x2713;\" /><input type=\"hidden\" name=\"authenticity_token\" value=\"oz4fAznNGOOk4MGD36uaxhZ/tjdRjpHa7qz8fwk3aDwBY+/GwFa2iAsQL3I4aQgCNgTAEqAigGEEHOsdpeUInA==\" />\n<input type=\"hidden\" name=\"book_id\" id=\"book_id\" value=\"30633\" />\n<input type=\"hidden\" name=\"name\" id=\"name\" value=\"to-read\" />\n<input type=\"hidden\" name=\"unique_id\" id=\"unique_id\" value=\"2_book_30633\" />\n<input type=\"hidden\" name=\"wtr_new\" id=\"wtr_new\" value=\"true\" />\n<input type=\"hidden\" name=\"from_choice\" id=\"from_choice\" value=\"false\" />\n<input type=\"hidden\" name=\"from_home_module\" id=\"from_home_module\" value=\"false\" />\n<input type=\"hidden\" name=\"ref\" id=\"ref\" value=\"\" class=\"wtrLeftUpRef\" />\n<input type=\"hidden\" name=\"existing_review\" id=\"existing_review\" value=\"false\" class=\"wtrExisting\" />\n<input type=\"hidden\" name=\"page_referrer\" id=\"page_referrer\" value=\"https://www.goodreads.com/\" />\n<input type=\"hidden\" name=\"page_url\" id=\"page_url\" value=\"/\" />\n<button class=\'wtrToRead\' type=\'submit\'>\n<span class=\'progressTrigger\'>Want to Read<\/span>\n<span class=\'progressIndicator\'>saving…<\/span>\n<\/button>\n<\/form>\n\n<\/div>\n\n<div class=\'wtrRight wtrUp\'>\n<form class=\"hiddenShelfForm\" action=\"/shelf/add_to_shelf\" accept-charset=\"UTF-8\" method=\"post\"><input name=\"utf8\" type=\"hidden\" value=\"&#x2713;\" /><input type=\"hidden\" name=\"authenticity_token\" value=\"h1gKr2+zfYa6WHoG/SORHTsU9/RvDsewjijIDriivPUlBfpqlijT7RWolPca4QPZG2+B0Z6i1gtkmN9sFHDcVQ==\" />\n<input type=\"hidden\" name=\"unique_id\" id=\"unique_id\" value=\"2_book_30633\" />\n<input type=\"hidden\" name=\"book_id\" id=\"book_id\" value=\"30633\" />\n<input type=\"hidden\" name=\"a\" id=\"a\" />\n<input type=\"hidden\" name=\"name\" id=\"name\" />\n<input type=\"hidden\" name=\"from_choice\" id=\"from_choice\" value=\"false\" />\n<input type=\"hidden\" name=\"from_home_module\" id=\"from_home_module\" value=\"false\" />\n<input type=\"hidden\" name=\"page_referrer\" id=\"page_referrer\" value=\"https://www.goodreads.com/\" />\n<input type=\"hidden\" name=\"page_url\" id=\"page_url\" value=\"/\" />\n<\/form>\n\n<button class=\'wtrShelfButton\'><\/button>\n<\/div>\n\n<div class=\'ratingStars wtrRating\'>\n<div class=\'starsErrorTooltip hidden\'>\nError rating book. Refresh and try again.\n<\/div>\n<div class=\'myRating uitext greyText\'>Rate this book<\/div>\n<div class=\'clearRating uitext\'>Clear rating<\/div>\n<div class=\"stars\" data-resource-id=\"30633\" data-user-id=\"0\" data-submit-url=\"/review/rate/30633?page_referrer=https%3A%2F%2Fwww.goodreads.com%2F&page_url=%2F&rate_books_page=false&stars_click=false&wtr_button_id=2_book_30633\" data-rating=\"0\"><a class=\"star off\" title=\"did not like it\" href=\"#\" ref=\"\">1 of 5 stars<\/a><a class=\"star off\" title=\"it was ok\" href=\"#\" ref=\"\">2 of 5 stars<\/a><a class=\"star off\" title=\"liked it\" href=\"#\" ref=\"\">3 of 5 stars<\/a><a class=\"star off\" title=\"really liked it\" href=\"#\" ref=\"\">4 of 5 stars<\/a><a class=\"star off\" title=\"it was amazing\" href=\"#\" ref=\"\">5 of 5 stars<\/a><\/div>\n<\/div>\n\n<\/div>\n\n\n\n\n", { style: 'addbook', stem: 'leftMiddle', hook: { tip: 'leftMiddle', target: 'rightMiddle' }, offset: { x: 5, y: 0 }, hideOn: false, width: 400, hideAfter: 0.05, delay: 0.35 });
      $('quote_book_link_30633').observe('prototip:shown', function() {
        if (this.up('#box')) {
          $$('div.prototip').each(function(i){i.setStyle({zIndex: $('box').getStyle('z-index')})});
        } else {
          $$('div.prototip').each(function(i){i.setStyle({zIndex: 6000})});
        }
      });

      newTip['wrapper'].addClassName('prototipAllowOverflow');

        $('quote_book_link_30633').observe('prototip:shown', function () {
          $$('div.prototip').each(function (e) {
            if ($('quote_book_link_30633').hasClassName('ignored')) {
              e.setStyle({'display': 'none'});
              return;
            }
            e.setStyle({'overflow': 'visible'});
          });
        });
      $('quote_book_link_30633').observe('prototip:hidden', function () {
        $$('span.elementTwo').each(function (e) {
          if (e.getStyle('display') !== 'none') {
            var lessLink = e.next();
            swapContent(lessLink);
          }
        });
      });

//]]>


//<![CDATA[
if (typeof window.uet == 'function') { window.uet('be'); }
//]]>


  //<![CDATA[
    qcdata = {} || qcdata;
      (function(){
        var elem = document.createElement('script');
        elem.src = (document.location.protocol == "https:" ? "https://secure" : "http://pixel") + ".quantserve.com/aquant.js?a=p-0dUe_kJAjvkoY";
        elem.async = true;
        elem.type = "text/javascript";
        var scpt = document.getElementsByTagName('script')[0];
        scpt.parentNode.insertBefore(elem,scpt);
      }());
    var qcdata = {qacct: 'p-0dUe_kJAjvkoY', uid: ''};
  //]]>


  //<![CDATA[
    var _comscore = _comscore || [];
    _comscore.push({ c1: "2", c2: "6035830", c3: "", c4: "", c5: "", c6: "", c15: ""});
    (function() {
    var s = document.createElement("script"), el = document.getElementsByTagName("script")[0]; s.async = true;
    s.src = (document.location.protocol == "https:" ? "https://sb" : "http://b") + ".scorecardresearch.com/beacon.js";
    el.parentNode.insertBefore(s, el);
    })();
  //]]>


  //<![CDATA[
    window.addEventListener("DOMContentLoaded", function() {
      ReactStores.GoogleAdsStore.initializeWith({"targeting":{"sid":"osid.d74df58b4798a81bcec724764bb5a2f5","grsession":"osid.d74df58b4798a81bcec724764bb5a2f5","surface":"desktop","signedin":"false","gr_author":"false","author":[]},"ads":{"div-gpt-ad-goodr-home-top-300x250":{"isNativeAd":false,"hasCreative":false,"hasRequestedCreative":false,"path":"/4215/goodr.home.top.300x250","dimensions":"300x250","adSizeMapping":null,"adDeviceType":"desktop","pmetImpressionTrackUrl":"https://www.goodreads.com/dfp/impression","pmetClickTrackUrl":"https://www.goodreads.com/dfp/click","creativeSelector":"div#google_image_div","isLazyLoaded":false},"div-gpt-ad-goodr-home-cb-300x250":{"isNativeAd":false,"hasCreative":false,"hasRequestedCreative":false,"path":"/4215/goodr.home.cb.300x250","dimensions":"300x250","adSizeMapping":null,"adDeviceType":"desktop","pmetImpressionTrackUrl":"https://www.goodreads.com/dfp/impression","pmetClickTrackUrl":"https://www.goodreads.com/dfp/click","creativeSelector":"div#google_image_div","isLazyLoaded":false}},"nativeAds":{}});
    });
  //]]>
