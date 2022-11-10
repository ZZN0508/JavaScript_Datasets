var __px = window.__px || {};
__px.campaigns = __px.campaigns || [];
__px.campaigns.push({
    "nest": {
        "conditions": [{
            "nest": {
                "conditions": [{
                    "patternName": "target__target_card_scv__bnk_1000",
                    "patternId": "target__34446__125203",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201111_kobo/pitari_bank_1000.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "cu_bankscv": 0
                    }
                }, {
                    "patternName": "target__target_card_scv__rmb_mno_2009",
                    "patternId": "target__34446__125204",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20200911_kobo/pitari_rmb_mno_2009.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "cu_mnoscv": 0
                    }
                }, {
                    "patternName": "target__target_card_scv__keiba_1000",
                    "patternId": "target__34446__125205",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201111_kobo/pitari_keiba_1000.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "cu_keibascv": 0
                    }
                }, {
                    "patternName": "target__target_card_scv__travel_goto_b",
                    "patternId": "target__34446__125206",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_travel_goto_b.html",
                            "target": "right_upper_banner"
                        }]
                    }
                }],
                "type": "Target"
            },
            "match": {
                "cu_cardscv": 1
            }
        }, {
            "patternName": "target__root__rtc_regular_visa",
            "patternId": "target__34445__125208",
            "actions": {
                "replace": [{
                    "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_rtc_nonholder_regular.html",
                    "target": "right_upper_banner"
                }]
            },
            "match": {
                "__pitari_non_login": 0
            }
        }, {
            "nest": {
                "conditions": [{
                    "patternName": "target__target_else__rmb_mno_2009",
                    "patternId": "target__34447__125209",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20200911_kobo/pitari_rmb_mno_2009.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "co_user_rank": 7
                    }
                }, {
                    "patternName": "target__target_else__rtc_platinum_visa",
                    "patternId": "target__34447__125210",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_rtc_nonholder_platinum.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "co_user_rank": 6
                    }
                }, {
                    "patternName": "target__target_else__rtc_gold_visa",
                    "patternId": "target__34447__125211",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_rtc_nonholder_gold.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "co_user_rank": 5
                    }
                }, {
                    "patternName": "target__target_else__rtc_silver_visa",
                    "patternId": "target__34447__125212",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_rtc_nonholder_silver.html",
                            "target": "right_upper_banner"
                        }]
                    },
                    "match": {
                        "co_user_rank": 4
                    }
                }, {
                    "patternName": "target__target_else__rtc_regular_visa",
                    "patternId": "target__34447__125213",
                    "actions": {
                        "replace": [{
                            "source": "/ichibatop/com/inc/home/20080930/beta/tz/opt/right_upper_banner/20201027_kobo/pitari_rtc_nonholder_regular.html",
                            "target": "right_upper_banner"
                        }]
                    }
                }],
                "type": "Target"
            }
        }],
        "type": "Target"
    },
    "enableIframe": true,
    "experimentId": 6781,
    "cookieName": "Rp",
    "ratConfig": {
        "acc": 486,
        "aid": 1,
        "endPoint": "//rat.rakuten.co.jp/?cpkg_none=",
        "ckp": "Rz",
        "cks": "Rp"
    },
    "scvParams": {
        "acc": "1",
        "aid": "43",
        "attr": "111"
    },
    "campaignName": "ichiba_top_page_right_banner_pc",
    "webViewEnabled": true,
    "apiType": "CCMP",
    "apiUrl": "https://user-attributes.api.rakuten.co.jp/capi/v1/ecosys/user.json"
});
(function() {
    if (document.addEventListener) {
        document.addEventListener('ph-CampaignEvent', function(event) {
            if (event.detail && event.detail.data) {
                var data = event.detail.data;
                data['phxpatternname'] = gP(data.phxpattern);
                if (6781 === data.phxexperiment) {
                    /**
                     * This function will be executed after your experiment processed
                     *
                     * Parameter references
                     * data.phxexperiment {string} Experiment ID
                     * data.phxpatternname {string} Matched pattern name
                     * data.phxsegments {array} Matched segment names
                     * data.phxabtestvalue {number} AB Test value
                     */

                }
            }
        });
    }

    function gP(p) {
        var t = '__';
        var s = p.split(t);
        return s[s.length - 1];
    }
})();