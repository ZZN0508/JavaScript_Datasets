(function Xy(){var t={isLoggedIn:function(e){if("boolean"==typeof e)return e;var a=t.readCookie("amexsessioncookie"),_=t.readCookie("blueboxvalues"),l=t.readCookie("SMSESSION"),o=!1;if(null!==a&&""!==a){var r=(new Date).getTime(),d=/uts=([^|]+)/.exec(a);if(!d)return!1;(r-parseInt(d[1],10))/6e4<5&&(o=!0)}else(null!==_&&""!==_||null!==l&&"LOGGEDOFF"!==l)&&(o=!0);return o},readCookie:function(e){for(var a=document.cookie.split(";"),_="".concat(e,"="),l=null,o=0;o<a.length;o+=1){var r=a[o].trim();if(0===r.indexOf(_)){l=r.substring(_.length,r.length);break}}return l},appendQueriesToUrl:function(e){var t=e.url,a=e.queries,n=t;return a.forEach(function(e){var a=e.key,_=e.value;if(-1<n.indexOf("".concat(a,"="))){var l=new RegExp("[\\?&]".concat(a,"=([^&#]*)")),o=l.exec(t)[0].charAt(0),r=t.replace(l,"".concat(o).concat(a,"=").concat(_));return"undefined"===_&&(r=r.replace(new RegExp("[\\?&]".concat(a,"=").concat(_)),"")),void(n=r)}if("undefined"!==_){var d=-1<n.indexOf("?")?"&":"?";n="".concat(n).concat(d).concat(a,"=").concat(_)}}),n},appendDestPageQuery:function(e,a){return t.appendQueriesToUrl({url:e,queries:[{key:"DestPage",value:encodeURIComponent(a)}]})},updateAuthView:function(e){try{var a=document.getElementById("gnav_logout"),_=document.getElementById("gnav_login");t.isLoggedIn(e)?(a.style.display="inline-block",_.style.display="none"):(a.style.display="none",_.style.display="inline-block")}catch(e){}},setLoginDestPage:function(e){try{var a=document.getElementById("gnav_login");a.href=t.appendDestPageQuery(a.href,e)}catch(e){}},setLogoutDestPage:function(e){try{var a=document.getElementById("gnav_logout");a.href=t.appendDestPageQuery(a.href,e)}catch(e){}}};return t.updateAuthView(),window.AmexNavigation={updateAuthView:t.updateAuthView,setLoginDestPage:t.setLoginDestPage,setLogoutDestPage:t.setLogoutDestPage},t})();

    var browserType = navigator.userAgent;
    if(browserType.indexOf("MSIE")>=0){
        function getParentWithClass(ele, parentClass){
            var e = ele;
            while(e.className.indexOf(parentClass)<0){
                e = e.parentElement;
            }
            return e;
        }

        function showMessageHideAll() {
            document.querySelector('#amex-header').style.display='none';
            document.querySelector('#amex-footer').style.display='none';

            var condContainerElement = document.querySelector('.conditional-container');
            var containingParentGrid = getParentWithClass(condContainerElement, 'aem-GridColumn');
            if(!containingParentGrid) { return; }
            var absParentNode = containingParentGrid.parentNode;
            if(!containingParentGrid) { return; }
            var childElements = absParentNode.children;
            for (i = 0; i < childElements.length; i++) {
                if (!childElements[i]) { continue;}
                if (childElements[i].querySelectorAll(".conditional-container").length > 0) {
                    document.querySelector('.legacy-browser').style.display = "block";
                } else {
                    childElements[i].style.display = "none";
                }
            }
        };
        document.onreadystatechange = function () {
            console.debug("onreadystatechange");
            if (document.readyState === 'complete' || document.readyState === 'interactive') {
                showMessageHideAll();
            }
        }
    }



    var digitalData = {"page":{"pageInfo":{"pageName":"Homepage","country":"JP","language":"ja","currency":"","pageID":"JP|AMEX|Home|Homepage","reportSuite":""},"category":{"businessUnit":"AMEX","primaryCategory":"","subCategory1":"Home","subCategory2":"","subCategory3":""}},"event":[]};

 var excludeOmniture = true;
 if(!!window._satellite) { window._satellite.pageBottom(); } 