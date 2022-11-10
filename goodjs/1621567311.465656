var targetWin = 'https://www.ndtv.com/sites/newsalert/share.aspx?ch=' + Date.now();
function submitFormInPopUp() {
    window.open('', 'Prvwindow', 'top=150,left=350,height=350,width=650,directories=no,titlebar=no,toolbar=no,location=no,status=no,menubar=no,scrollbars=no,resizable=no,addressbar=no');
    var Mainform = document.getElementById('Mainform');
    Mainform.action = targetWin;
    Mainform.target = "Prvwindow";
    Mainform.submit();
    return false;
}

function closeNewsflash() {
    document.getElementById("breakingnews2015").style.display = "none";
    
}
(function jqIsReady() {
    if (typeof $ === "undefined") {
        setTimeout(jqIsReady, 10);
        return;
    }



    var _breakinghtml = "";
    var agentType = String($('.breaking_alert').attr('data-type')).toLowerCase();
    if (agentType === "desktop") {
        $("<link/>", {
            rel: "stylesheet",
            type: "text/css",
            href: "https://drop.ndtv.com/homepage/css/homecss/realtimenewsalert.css"
        }).appendTo("head");
    }

    _breakinghtml = '<div class="breakingnews_new bnews_extra"  id="breakingnews2015">';
    _breakinghtml += '<div class="balert1"><span class="alertType"></span></div>';
    _breakinghtml += '<div class="btext btext1"><a id="alertNews" href=""></a></div>';
    _breakinghtml += '<a class="closebutton closebutton1" href="javascript:void(0);"  onclick="closeNewsflash();"> </a>';
    _breakinghtml += '<div class="bsharetool bsharetool1">';
    _breakinghtml += '<a class="break_fb" href="javascript:void(0);"  onclick="window.open(\'https://www.facebook.com/dialog/feed?app_id=213741912058651&display=popup&title={~title~}&link=https://www.ndtv.com\', \'fshare\', \'width=500, height=350\'); return false;" ></a>';
    _breakinghtml += '<a  class="break_tw" href="javascript:void(0);"  onclick="twittershare(\'{~titletweet~}\');"></a>';
    _breakinghtml += '<a class="break_mail" href="javascript:void(0);" onclick="submitFormInPopUp();"></a>';
    _breakinghtml += '</div>';
    _breakinghtml += '</div>';

    _breakinghtml += '<form action="" id="Mainform" name="Mainform" method="post"> ';
    _breakinghtml += '<input id="MainContent_hdnTitle" type="hidden" value="" name="ctl00$MainContent$hdnTitle">';
    _breakinghtml += '<input id="MainContent_hdnUrl" type="hidden" value="" name="ctl00$MainContent$hdnUrl">';
    _breakinghtml += '<input id="MainContent_hdnnewsType" type="hidden" value="" name="ctl00$MainContent$hdnnewsType">';
    _breakinghtml += '<input type="hidden" name="ctl00$MainContent$hdnRealTitle" id="MainContent_hdnRealTitle" value="{~titleshare~}" />';
    _breakinghtml += '<input type="hidden" name="ctl00$MainContent$hdnRealUrl" id="MainContent_hdnRealUrl" value="Shared via http://www.ndtv.com" />';
    _breakinghtml += '<input type="hidden" name="ctl00$MainContent$hdnRealType" id="MainContent_hdnRealType" value="News Flash" />';
    _breakinghtml += '</form>';


    $(document).ready(function () {
        var proRandom = getRandomNumber(1, 4);
        
        var brkconfig = {

            projectId: "fir-breaking-bucket-" + proRandom
        };

        var canUrl = $("link[rel='canonical']").attr("href");
        var brkApp = firebase.initializeApp(brkconfig, "secondary");
        var dbCollection = 'elections.ndtv.com';
        var db1 = brkApp.firestore();
        var alertType = String($('.breaking_alert').attr('data-alert')).toLowerCase();

        
        // var alertDoc = "ndtv-breakingnews-stage";


        var alertDoc = alertType + "-breakingnews";

        db1.collection(dbCollection).doc(alertDoc).onSnapshot(function (doc) {
            if ($('.breaking_alert').html() !== '') {
                $('.breaking_alert').html('');

            }

            var breakingNewsData = doc.data().data;
          
          


            if (breakingNewsData !== null && breakingNewsData.alerttext !== "") {

                var newsalerttext = breakingNewsData.alerttext.replace(/'/g, "\'");
                var tweetEncode_newsalerttext = encodeURI(breakingNewsData.alerttext).replace(/'/g, "\\'");
                var shareEncode_newsalerttext = encodeURI(breakingNewsData.alerttext.replace(/'/g, "\'"));
                var encode_newsalerttext = encodeURI(breakingNewsData.alerttext.replace(/'/g, ""));


                var new_breakinghtml = _breakinghtml.replace(/{~title~}/g, encode_newsalerttext).replace(/{~titleshare~}/g, shareEncode_newsalerttext).replace(/{~titletweet~}/g, tweetEncode_newsalerttext);


                $('.breaking_alert').html(new_breakinghtml);

                var unixTimestamp = breakingNewsData.updatedtime;
                

                var storyUrl = breakingNewsData.storylink == '' ? "" : breakingNewsData.storylink + (breakingNewsData.storylink.indexOf('?') > 0 ? "&pfrom=web-homepagerealtime"  : "?pfrom=web-homepagerealtime");
                $('.alertType').html(breakingNewsData.alerttype);
                $('#alertNews').html(newsalerttext).attr('href', storyUrl);

                if (storyUrl === '') {
                    $('#alertNews').removeAttr('href');

                }

            }

        });


    });
})();
function getRandomNumber(low, high) {
    var r = Math.floor(Math.random() * (high - low + 1)) + low;
    return r;
}


function twittershare(text) {
    window.open('https://www.twitter.com/share?text=' + text + 's&url=https://www.ndtv.com', 'Tweet', 'width=500, height=400');
}