function getDfd() {let yFn,nFn;const p=new Promise((y, n)=>{yFn=y;nFn=n;});p.resolve=yFn;p.reject=nFn;return p;}window.lazyloader = getDfd();window.tracking = getDfd();window.impressionTracking = getDfd();window.pemTracking = getDfd();window.ingraphTracking = getDfd();window.appDetection = getDfd();

            function getDaidostupCookie(name) {
                var cookie = " " + document.cookie;
                var search = " " + name + "=";
                var setStr = null;
                var offset = 0;
                var end = 0;
                if (cookie.length > 0) {
                    offset = cookie.indexOf(search);
                    if (offset != -1) {
                        offset += search.length;
                        end = cookie.indexOf(";", offset)
                        if (end == -1) {
                            end = cookie.length;
                        }
                        setStr = unescape(cookie.substring(offset, end));
                    }
                }
                return(setStr);
            }

            function setDaidostupCookie(name, value, expires, path, domain, secure) {
                document.cookie = name + "=" + escape(value) +
                        ((expires) ? "; expires=" + expires : "") +
                        ((path) ? "; path=" + path : "") +
                        ((domain) ? "; domain=" + domain : "") +
                        ((secure) ? "; secure" : "");
            }

            function hideDaidostupBar() {
                var daidostupBarDiv = document.getElementById("dd_x2x_bar");
                if (daidostupBarDiv != null) {
                    daidostupBarDiv.parentNode.removeChild(daidostupBarDiv);
                }

                setDaidostupCookie("hidedaidostupbar", "true");

                return false;
            }

            function selectDaidostupAll(id)
            {
                document.getElementById(id).focus();
                document.getElementById(id).select();
            }
        

            var hideDaidostupBarCookieValue = getDaidostupCookie("hidedaidostupbar");
            if (hideDaidostupBarCookieValue == "true") {
                hideDaidostupBar();
            }

            if (typeof _gaq != "undefined") {
                document.getElementById("dd_x2x_form_cont").id = "dd_x2x_form_cont_ie9";
            }
        