window.scriptsLoaded++;
(function() {
    try {
        var getCookie = function getCookie(name) {
            var parts, returnValue, value;
            value = ";" + document.cookie;
            parts = value.split("; " + name + "=");
            returnValue = "";

            if (parts.length === 2) {
                returnValue = parts.pop().split(";").shift();
            }

            return returnValue;
        };

        var insertScript = function insertScript(w, d, t, r, u) {
            var f, n, i;
            w[u] = w[u] || [];

            f = function f() {
                var o = {
                    ti: "5224622"
                };
                o.q = w[u];
                w[u] = new UET(o);
                w[u].push("pageLoad");
            };

            n = d.createElement(t);
            n.src = r;
            n.async = 1;

            n.onload = n.onreadystatechange = function () {
                var s = this.readyState;
                s && s !== "loaded" && s !== "complete" || (f(), n.onload = n.onreadystatechange = null);
            };

            i = d.getElementsByTagName(t)[0];
            i.parentNode.insertBefore(n, i);
        };

        var filterVideoGames = function filterVideoGames(subCategory) {
            var categoryName, webSubCategory;
            categoryName = "video games";
            webSubCategory = "";

            if (subCategory !== undefined && subCategory !== null) {
                webSubCategory = subCategory.toString();
            }

            switch (webSubCategory) {
                case "02":
                case "2":
                    categoryName = categoryName + ": nintendo 3ds";
                    break;

                case "13":
                    categoryName = "electronics: computer & office";
                    break;

                case "22":
                    categoryName = categoryName + ": xbox 360";
                    break;

                case "24":
                    categoryName = categoryName + ": playstation 3";
                    break;

                case "26":
                    categoryName = categoryName + ": nintendo wii";
                    break;

                case "28":
                    categoryName = categoryName + ": pc games";
                    break;

                case "29":
                    categoryName = categoryName + ": retro consoles";
                    break;

                case "30":
                    categoryName = categoryName + ": nintendo switch/wii u";
                    break;

                case "32":
                    categoryName = categoryName + ": xbox one";
                    break;

                case "34":
                    categoryName = categoryName + ": playstation 4";
                    break;

                case "35":
                    break;

                default:
                    categoryName = "";
                    break;
            }

            return categoryName;
        };

        var filterMovies = function filterMovies(subCategory) {
            var categoryName, webSubCategory;
            categoryName = "movies";
            webSubCategory = "";

            if (subCategory !== undefined && subCategory !== null) {
                webSubCategory = subCategory.toString();
            }

            switch (webSubCategory) {
                case "01":
                case "1":
                case "02":
                case "2":
                case "03":
                case "3":
                    categoryName = categoryName + ": dvd: miscellaneous";
                    break;

                case "10":
                case "21":
                    categoryName = categoryName + ": kids & family";
                    break;

                case "11":
                    categoryName = categoryName + ": dvd: fitness";
                    break;

                case "12":
                    categoryName = categoryName + ": dvd: drama";
                    break;

                case "13":
                    categoryName = categoryName + ": dvd: musical";
                    break;

                case "14":
                    categoryName = categoryName + ": dvd: comedy";
                    break;

                case "15":
                    categoryName = categoryName + ": dvd: special interest";
                    break;

                case "16":
                    categoryName = categoryName + ": dvd: horror & sci-fi";
                    break;

                case "17":
                    categoryName = categoryName + ": dvd: action & adeventure";
                    break;

                case "18":
                    categoryName = categoryName + ": dvd: western";
                    break;

                case "19":
                    categoryName = categoryName + ": dvd: holiday";
                    break;

                case "22":
                    categoryName = categoryName + ": dvd: tv";
                    break;

                case "23":
                case "24":
                    categoryName = categoryName + ": dvd: bundles";
                    break;

                case "27":
                    categoryName = categoryName + ": blu ray";
                    break;

                case "28":
                    categoryName = categoryName + ": dvd: spanish";
                    break;

                case "30":
                case "31":
                    categoryName = categoryName + ": blu ray: kids & family";
                    break;

                case "32":
                    categoryName = categoryName + ": blu ray: drama";
                    break;

                case "33":
                    categoryName = categoryName + ": blu ray: musical";
                    break;

                case "34":
                    categoryName = categoryName + ": blu ray: comedy";
                    break;

                case "35":
                    categoryName = categoryName + ": blu ray: special interest";
                    break;

                case "36":
                    categoryName = categoryName + ": blu ray: horror & sci-fi";
                    break;

                case "37":
                    categoryName = categoryName + ": blu ray: holiday";
                    break;

                case "39":
                    categoryName = categoryName + ": blu ray: tv";
                    break;

                case "40":
                case "41":
                    categoryName = categoryName + ": blu ray: bundles";
                    break;

                case "50":
                case "51":
                case "52":
                    categoryName = categoryName + ": disney";
                    break;

                default:
                    categoryName = "";
                    break;
            }

            return categoryName;
        };

        var filterMusic = function filterMusic(subCategory) {
            var webSubCategory, categoryName;
            categoryName = "music";
            webSubCategory = "";

            if (subCategory !== undefined && subCategory !== null) {
                webSubCategory = subCategory.toString();
            }

            switch (webSubCategory) {
                case "00":
                    categoryName = categoryName + ": kids";
                    break;

                case "01":
                    categoryName = categoryName + ": budget";
                    break;

                case "02":
                case "2":
                case "17":
                    categoryName = categoryName + ": target exclusive";
                    break;

                case "03":
                case "3":
                    categoryName = categoryName + ": r&b/rap";
                    break;

                case "04":
                case "4":
                    categoryName = categoryName + ": pop";
                    break;

                case "05":
                case "5":
                    categoryName = categoryName + ": country";
                    break;

                case "06":
                case "6":
                    categoryName = categoryName + ": rock";
                    break;

                case "07":
                case "7":
                    categoryName = categoryName + ": various artists";
                    break;

                case "09":
                case "9":
                    categoryName = categoryName + ": latin";
                    break;

                case "11":
                    categoryName = categoryName + ": dvd music video";
                    break;

                case "12":
                    categoryName = categoryName + ": holiday";
                    break;

                case "13":
                    categoryName = categoryName + ": soundtracks & compilations";
                    break;

                case "14":
                    categoryName = categoryName + ": christian/gospel";
                    break;

                default:
                    categoryName = "";
                    break;
            }

            return categoryName;
        };

        var filterWebSubClassArray = function filterWebSubClassArray(products) {
            return products.map(function (item) {
                var webClass, webSubClass, obj;
                webClass = "";

                if (item.webClass !== undefined && item.webClass !== null) {
                    webClass = item.webClass.toString();
                }

                switch (webClass) {
                    case "012":
                    case "12":
                        webSubClass = filterMusic(item.webSubClass);
                        break;

                    case "058":
                    case "58":
                        webSubClass = filterMovies(item.webSubClass);
                        break;

                    case "207":
                        webSubClass = filterVideoGames(item.webSubClass);
                        break;

                    case "244":
                        webSubClass = "music: miscellaneous";
                        break;

                    case "246":
                        webSubClass = "movies: miscellaneous";
                        break;

                    default:
                        break;
                }

                if (webSubClass !== undefined) {
                    obj = {
                        tcin: item.tcin,
                        webSubClass: webSubClass
                    };
                }

                return obj;
            }).filter(function (item) {
                return item !== undefined;
            });
        };

        var checkIfFilterReq = function checkIfFilterReq(tcin, webSubClassArray) {
            var checkTcin = tcin;
            webSubClassArray.forEach(function (item) {
                if (item.tcin === tcin) {
                    checkTcin = item.webSubClass;
                }
            });
            return checkTcin;
        };

        var filterTcins = function filterTcins(bingdl) {
            var webSubClass, tcin;
            webSubClass = filterWebSubClassArray(bingdl.products);
            tcin = bingdl.products.map(function (product) {
                return checkIfFilterReq(product.tcin, webSubClass);
            });
            return tcin;
        };

        var buildAudience = function buildAudience(prodid, pagetype) {
            window.uetq.push({
                prodid: prodid,
                pagetype: pagetype
            });
        };

        var coreFunction = function coreFunction() {
            var bingdl, bing_order_revenue, ci_afid, id, pagetype, prodid;

            if (window.tgt !== undefined && window.tgt.dataLayer !== undefined) {
                id = document.querySelector('div[id^=\'batBeacon\']');
                bingdl = window.tgt.dataLayer;
                ci_afid = getCookie('ci_afid');
                prodid = '';
                pagetype = bingdl.appState.pageType;
                window.uetq = [];

                if (id !== null && id !== undefined) {
                    id.parentNode.removeChild(id);
                }

                if (bingdl.checkout.orderId !== "" && bingdl.checkout.purchase === true) {
                    bing_order_revenue = 0;

                    for (var i = 0, j = bingdl.products.length; i < j; i++) {
                        bing_order_revenue += Math.round(parseFloat(bingdl.products[i].price) * 100) / 100;
                    }

                    bing_order_revenue = Math.round(parseFloat(bing_order_revenue) * 100) / 100 || 0;

                    if (ci_afid !== undefined && /^(bing|msn)/i.test(ci_afid)) {
                        window.uetq.push({
                            'gv': bing_order_revenue
                        });
                    }

                    buildAudience(filterTcins(bingdl), "purchase");
                } else if (pagetype === "product details") {
                    prodid = filterTcins(bingdl);
                    buildAudience(prodid[0], "product");
                } else {
                    switch (pagetype) {
                        case "search: search results":
                            pagetype = "searchresults";
                            buildAudience(filterTcins(bingdl), pagetype);
                            break;

                        case "level 1":
                        case "level 2":
                        case "level 3":
                        case "level 4":
                        case "brand":
                            pagetype = "category";
                            buildAudience(filterTcins(bingdl), pagetype);
                            break;

                        case "home page":
                            pagetype = "home";
                            buildAudience("", pagetype);
                            break;

                        default:
                            pagetype = "other";
                            buildAudience("", pagetype);
                            break;
                    }
                }

                insertScript(window, document, "script", "//bat.bing.com/bat.js", "uetq");
            }
        };

        if (window.location.host !== "http://intl.target.com/") {
            coreFunction();
        }
    }
    catch(e) {
        console.log(e.message);
    }
})();