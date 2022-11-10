var cookie_cleaner = cookie_cleaner || {};
(function (global) {
    var RCC_COINFIG = {
        targetDomains: { // The whole should match "document.domain". Regular expressions are available by starting the domain name with "^". The first matching setting is used.
            "point-g.rakuten.co.jp": {
                trigger: "basicTrigger",
                jobs: ["basic-job"]
            },
            "recipe.rakuten.co.jp": {
                trigger: "basicTrigger",
                jobs: ["recipe-job"]
            },
            "kobo-free.books.rakuten.co.jp": {
                trigger: "basicTrigger",
                jobs: ["chappy-job"]
            },
            "emagazine.rakuten.co.jp": {
                trigger: "basicTrigger",
                jobs: ["basic-job"]
            },
            "dm.rakuten.co.jp": {
                trigger: "basicTrigger",
                jobs: ["basic-job"]
            }
        },

        components: {
            triggers: { // Specify by regular expression.
                basicTrigger: {
                    triggerSize:   5000,  // Process if the total size of name+value is greater than or equal to the specified value
                    terminateSize: 4000   // The process ends when the total size of name+value is less than the specified value.
                }
            },
            jobs: {
                "basic-job": [{
                    domain: ".rakuten.co.jp",  // Cookie domain
                    cookiePath: "/",
                    sizeToBeRemoved: 800, // Cookies specified in checkCookies are deleted if value is less than or equal to the specified value.
                    protectCookies: ["rakutenProtect"],
                    deleteCookies: ["rakutenDelete"],
                    checkCookies: ["rakutenCheck"]
                }],
                "chappy-job": [{
                    domain: ".rakuten.co.jp",  // Cookie domain
                    cookiePath: "/",
                    sizeToBeRemoved: 800, // Cookies specified in checkCookies are deleted if value is less than or equal to the specified value.
                    protectCookies: ["rakutenProtect", "koboChappyProtect"],
                    deleteCookies: ["rakutenDelete"],
                    checkCookies: ["rakutenCheck"]
                }],
                "recipe-job": [{
                    domain: ".rakuten.co.jp",  // Cookie domain
                    cookiePath: "/",
                    sizeToBeRemoved: 800, // Cookies specified in checkCookies are deleted if value is less than or equal to the specified value.
                    protectCookies: ["rakutenProtect", "recipeProtect"],
                    deleteCookies: ["rakutenDelete"],
                    checkCookies: ["rakutenCheck"]
                }]
            },
            cookies: { // Case-sensitive. Regular expressions are available by starting the domain name with "^".
                koboChappyProtect: ["timeTravel", "csid", "chappy-session", "_ra", "Rp", "rat_v", "m", "s", "message", "bifocal:device-id", "bifocal:mode:spread", "Rz", "Ra", "Rq", "Ry", "Rb", "Rp"],
                recipeProtect: ["e_recipe", "u_recipe", "c_recipe", "h_recipe", "t_recipe", "g_recipe", "m_recipe", "f_recipe", "a_recipe"],
                rakutenProtect: ["Ra", "Rb", "Rq", "Ry", "Rz", "Rp", "OSSO", "ODID", "Im", "Ims"],
                rakutenDelete: ["^stc.*", "^amcv.*"],
                rakutenCheck: []
            }
        }
    };
    // Set public accessor
    cookie_cleaner.config = RCC_COINFIG;

}(this));