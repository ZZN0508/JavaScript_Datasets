try { top.location.toString(); if (top != self) { throw new Error(''); } } catch (e) { top.location = location; }
if(navigator.sendBeacon){ var data = "a=" +JSON.stringify({ startupData: { headBeacon:1 } }); var headers = { type: 'application/x-www-form-urlencoded' }; var blob = new Blob([data], headers); navigator.sendBeacon('/gwtlog', blob); }
var swPath = "/app.js";
if ('serviceWorker' in navigator) { window.addEventListener('load', function(){ navigator.serviceWorker.register(swPath); }); }
var OK = OK || {}; OK.startupData = OK.startupData || {}; OK.startupData['okHeadStart'] = window.performance.now();
OK.startupData['odklCssGo'] = window.performance.now() - OK.startupData['okHeadStart'];
var pageCtx={0:0,regJsSrc:"res/js/scriptReg_42f2c12f.js",giftsJsSrc:"res/js/scriptGifts_8533b4fc.js",nativeHooksSrc:"res/js/nativeHooks_3c1fb4ed.js",textareaJsSrc:"res/js/textarea/textarea_2db7e046.js",photoUploaderJsSrc:"res/js/photoUploader_2dbe3c54.js",bottomJsSrc:"res/js/scriptBottom_7bedfc2c.js",photoLayerJsSrc:"res/js/photoLayer_5c8ef47e.js",promoAppJsSrc:"res/js/scriptPromoApp_fa4d97b9.js",appEditJsSrc:"res/js/scriptAppEditForm_eb6eeac3.js",cdnNodeSrc:"//st.mycdn.me/static/cdn/cdn.js?timestamp=1621566615113",gwtHash:"42107589T1621432801681",isAnonym:true,path:"/",state:"st.cmd=anonymMain",staticResourceUrl:"/",youlaApps:"youla,youla_test,sport2018,youla_stage,pandao,masters,get-ok-back-in-games"};
window.inline_resources = {};
window.inline_resources.pms={};
window.inline_resources.pts={};

require.config({"baseUrl":"/","enforceDefine":"false","paths":{"OK/LinkOnCommand":"res/js/app/LinkOnCommand_4dabb51f","OK/PaymentApi":"res/js/app/PaymentApi_e42fbef8","OK/UserClientCache":"res/js/app/UserClientCache_e06fd1a5","OK/NumberSequence":"res/js/app/NumberSequence_2d7fbcff","OK/iframeResize":"res/js/app/iframeResize_ca52aa0e","OK/InputCard":"res/js/app/InputCard_21aa5c4","jquery.ui.resizable":"res/js/lib/jquery.ui.resizable_9ec24770","OK/Captcha":"res/js/app/Captcha_95538bf8","OK/GroupInfoPanel":"res/js/app/GroupInfoPanel_33411206","music":"//st.mycdn.me/static/music/0-3-15","OK/privacy":"res/js/app/privacy_c247502c","b/postingDecoration":"res/js/b/postingDecoration_ae6d4353","OK/SettingsSaveButton":"res/js/app/SettingsSaveButton_9f3b650c","OK/BannerRefreshLogger":"//st.mycdn.me/static/hf/2020-12-10brl2/BannerRefreshLogger","OK/ProfileCoverSettings":"res/js/app/ProfileCoverSettings_b4f3929b","OK/FriendshipRelationsSelector":"res/js/app/FriendshipRelationsSelector_95b8bbca","OK/MotivatorGame":"res/js/app/MotivatorGame_d5b1ba29","OK/WidgetVideoAdv":"res/js/app/WidgetVideoAdv_6d086c33","OK/textCounter":"res/js/app/textCounter_6bb93a89","OK/AmPromoCodeDialog":"//st.mycdn.me/static/hf/2020-04-03am3/AmPromoCodeDialog","OK/EventFactory.d":"res/js/app/EventFactory.d_6556f0cd","OK/GroupJournalPageItem":"res/js/app/GroupJournalPageItem_1e02221","b/discussions-feed":"res/js/b/discussions-feed_60bdd105","superappkit":"res/js/lib/superappkit/superappkit_f5073d9e","OK/MediaTopicTrack":"res/js/app/MediaTopicTrack_0","OK/RemoveHideGroupLink":"res/js/app/RemoveHideGroupLink_66c5ca60","jquery.ui.widget":"res/js/lib/jquery.ui.widget_a4321f6","OK/Discussion":"res/js/app/Discussion_3ff78f2","OK/MallProductsFeedPortlet":"res/js/app/MallProductsFeedPortlet_fa2fd2f","OK/WidgetRescuerFriendsMob":"res/js/app/WidgetRescuerFriendsMob_d70c7afc","OK/GroupPaidAccessSettings":"res/js/app/GroupPaidAccessSettings_f9420432","OK/PostingFormVideoPickerInput":"res/js/app/PostingFormVideoPickerInput_2c9fed78","OK/FeedDiscussion":"res/js/app/FeedDiscussion_fcc7a7ef","OK/StickerPreview":"//st.mycdn.me/static/messages/2021-04-13ls10/StickerPreview","OK/StubTimeout":"res/js/app/StubTimeout_a7dc69e9","OK/GroupTopicPublishOriginator":"res/js/app/GroupTopicPublishOriginator_1731e2e9","OK/Interests":"res/js/app/Interests_3ab7a4b","OK/WidgetSharePreviewResponsive":"res/js/app/WidgetSharePreviewResponsive_8922ddd2","OK/PaymentVideoAdvRedLink":"res/js/app/PaymentVideoAdvRedLink_3ed67e73","OK/PresentSlider":"res/js/app/PresentSlider_40c2a4d0","OK/MovieEventLogger":"res/js/app/MovieEventLogger_d92f987c","quasi-state":"//st.mycdn.me/static/dailyphoto/1-5-3/quasi-state/quasi-state","OK/AppsShowcaseVideo":"res/js/app/AppsShowcaseVideo_edb19468","OK/photoUploadFacade":"res/js/app/photoUploadFacade_6d8b1962","OK/SearchInput":"res/js/app/SearchInput_141848fe","OK/PopLayerPhoto":"res/js/app/PopLayerPhoto_f28ec7ed","OK/GroupBroadcast":"res/js/app/GroupBroadcast_2d1c3884","OK/GroupTargetAdWrapper":"res/js/app/GroupTargetAdWrapper_f6eae07a","OK/FormManager":"res/js/app/FormManager_9eb26348","OK/ExpressReactionsPopup":"res/js/app/ExpressReactionsPopup_dea4baea","L10n/datepicker-en":"res/js/L10n/datepicker-en_501d2439","OK/HelpFeedbackForm":"res/js/app/HelpFeedbackForm_775a420a","OK/PopLayerHelpFeedback":"res/js/app/PopLayerHelpFeedback_83942a86","OK/WidgetVideoAdvMob":"res/js/app/WidgetVideoAdvMob_6d086c33","OK/webapi.d":"res/js/app/webapi.d_6556f0cd","OK/UserProfileAddFriend":"res/js/app/UserProfileAddFriend_146c0fe2","b/videochat":"//st.mycdn.me/static/messages/2020-05-12join41/videochat.min","OK/call2":"res/js/app/call2_8b5ed1f4","OK/pms":"res/js/app/pms_9d2a6c36","OK/WidgetInviteMob":"res/js/app/WidgetInviteMob_611d6ce0","OK/GroupDescriptionInSearch":"res/js/app/GroupDescriptionInSearch_ed97aaa6","OK/MallCheckoutAddressFieldsObserver":"res/js/app/MallCheckoutAddressFieldsObserver_ee5aff3c","OK/NavigationGoBack":"res/js/app/NavigationGoBack_d14bd51f","OK/GroupMessagesBubbleEventBus":"res/js/app/GroupMessagesBubbleEventBus_3a2417f8","OK/cookie":"res/js/app/cookie_a43a2903","OK/AppAdBlockCheck":"res/js/app/AppAdBlockCheck_f88fa8ff","OK/utils/md5":"//st.mycdn.me/res/js/app/utils/md5","OK/GiftChainlet":"res/js/app/GiftChainlet_9e032dc8","b/autophotopins":"res/js/b/autophotopins_14412b68","OK/GameStreams":"res/js/app/GameStreams_a69c8ef4","OK/GroupInvitationsEntityList":"res/js/app/GroupInvitationsEntityList_13be2754","OK/GroupSubscriptionEventSender":"res/js/app/GroupSubscriptionEventSender_6a057045","OK/RightColumn":"res/js/app/RightColumn_2d73161e","OK/RegexpToken":"res/js/app/RegexpToken_2f62b8dc","OK/ScrollerTopPanel":"res/js/app/ScrollerTopPanel_423d03ca","OK/LazyIconNative":"res/js/app/LazyIconNative_617485b8","OK/MallProductInfo":"res/js/app/MallProductInfo_c0d2aa89","OK/ChatBotPortlet":"res/js/app/ChatBotPortlet_181f6872","webrtc/sdp-interop":"res/js/lib/webrtc/sdp-interop_8114582f","OK/OkLiveMap":"res/js/app/OkLiveMap_648a4681","jquery.okTags":"res/js/lib/jquery.okTags_a07ce1da","OK/SelectedDiscussion":"res/js/app/SelectedDiscussion_5940bd6f","OK/PhotoLayer":"res/js/app/PhotoLayer_4aa52c23","OK/GroupDmrCardFrame":"res/js/app/GroupDmrCardFrame_8a4ceb0","OK/NewsFetchCoordinator":"res/js/app/NewsFetchCoordinator_85ed620d","OK/viewport":"res/js/app/viewport_23a3c380","b/externalWidget":"res/js/b/externalWidget_af431545","dailyphoto-archive":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-archive/dailyphoto-archive","OK/FindFriendByPhoto":"res/js/app/FindFriendByPhoto_6a57bd08","OK/PrevAlbum":"res/js/app/PrevAlbum_ad9a3487","OK/MallProductReviews":"res/js/app/MallProductReviews_22e1b9ef","colorPickerSpectrum":"res/js/lib/color-picker-spectrum.min_4901b4f1","OK/DndOverlay":"res/js/app/DndOverlay_e3edbfec","OK/DelayedBlocksUpdater":"res/js/app/DelayedBlocksUpdater_bff418ba","OK/PhotoPickerEventBuses":"res/js/app/PhotoPickerEventBuses_7dd769c6","b/nonBlockingTip":"res/js/b/nonBlockingTip_502675f9","OK/EventsCalendarOptions":"res/js/app/EventsCalendarOptions_78f9cc89","OK/FaviconManager":"res/js/app/FaviconManager_99e18e79","OK/GroupDonateSettings":"res/js/app/GroupDonateSettings_32938d0d","OK/audioPlayer":"res/js/app/audioPlayer_c9420947","b/primary":"res/js/b/primary_69afb2e2","OK/Art":"res/js/app/Art_5a1a1451","OK/FeelingBackgrounds":"res/js/app/FeelingBackgrounds_70c3b04c","OK/MotivatorConstructorQuestionDialog":"res/js/app/MotivatorConstructorQuestionDialog_a1ce12","OK/NativeHookJs":"res/js/app/NativeHookJs_21c8ee8c","OK/StartupTimingLogger":"res/js/app/StartupTimingLogger_88a23034","OK/FeedNavigationComponentSlider":"res/js/app/FeedNavigationComponentSlider_af4af0cc","OK/ClipboardText":"res/js/app/ClipboardText_e20c752f","OK/ChangeAvatarSuggest":"res/js/app/ChangeAvatarSuggest_2c38710f","OK/WebPushPortlet":"res/js/app/WebPushPortlet_5b29696f","OK/SettingsPage":"res/js/app/SettingsPage_752c6d53","highcharts-fill":"res/js/lib/highcharts-fill_39441973","OK/SearchTrack":"res/js/app/SearchTrack_b478c010","OK/ProfileCoverSettingsButtonMenu":"res/js/app/ProfileCoverSettingsButtonMenu_a7daf37f","mrg-smokescreen/StyleSheets":"res/js/lib/mrg-smokescreen/StyleSheets_daf016a0","OK/utils/viewport":"//st.mycdn.me/static/hf/2020-10-01viewport1/viewport","OK/VideoAddByLink":"res/js/app/VideoAddByLink_4b0dfef5","OK/ListPhotos":"res/js/app/ListPhotos_9720dab9","OK/PhoneMaskHook":"res/js/app/PhoneMaskHook_944ef00d","OK/dailyphoto-slider":"res/js/app/dailyphoto-slider_2af749ae","b/postingBundle":"res/js/b/postingBundle_df798f41","OK/confirmUserCity":"res/js/app/confirmUserCity_abfb6721","OK/NotificationRemoved":"res/js/app/NotificationRemoved_54eef555","OK/ToolbarManager":"res/js/app/ToolbarManager_1b2c57f0","b/groupDatePicker":"res/js/b/groupDatePicker_23c253d7","OK/GwtConfig":"res/js/app/GwtConfig_6483459d","onepagescroll":"res/js/lib/onepagescroll_5cb4f9b4","OK/StickyDiscoveryMenu":"res/js/app/StickyDiscoveryMenu_5c75dd56","OK/ShortcutMenuAdapter":"res/js/app/ShortcutMenuAdapter_a11ea568","OK/WidgetInvite":"res/js/app/WidgetInvite_611d6ce0","OK/uslider":"res/js/app/uslider_5dfc0fd1","OK/MusicBanner":"res/js/app/MusicBanner_3634b8af","OK/PhotoItemsMarks":"res/js/app/PhotoItemsMarks_c03ca95d","OK/AbstractShortcutMenu":"res/js/app/AbstractShortcutMenu_fbb7890d","OK/MotivatorGameWheel":"res/js/app/MotivatorGameWheel_d22f038d","OK/PhotoDescriptionWrapper":"res/js/app/PhotoDescriptionWrapper_c7721b0f","L10n/datepicker-az":"res/js/L10n/datepicker-az_44d28dad","OK/slider":"res/js/app/slider_b2b3dc45","OK/AttachPhotoUpload":"res/js/app/AttachPhotoUpload_42eb2019","OK/Community":"res/js/app/Community_5df247","OK/MallDeliveryFillZipcode":"res/js/app/MallDeliveryFillZipcode_7b6ed0bf","OK/MediaLayer":"res/js/app/MediaLayer_d0f51f1e","OK/PhotoUploadWithParams":"res/js/app/PhotoUploadWithParams_c5d67aa9","OK/WideRightColumn":"res/js/app/WideRightColumn_6d83dcd5","OK/CommentWidgets":"res/js/app/CommentWidgets_5d2ae1de","OK/FormManagerValidator":"res/js/app/FormManagerValidator_94ca371c","OK/PhoneForm":"res/js/app/PhoneForm_8ed0b5ee","OK/Uploader":"res/js/app/Uploader_3897a88c","OK/ViewportTracker":"res/js/app/ViewportTracker_e58c0aae","OK/StreamDonate":"res/js/app/StreamDonate_fda04545","REACT/vendors":"res/react/vendors_fa1ac5f1","OK/SuggestProfileCover":"res/js/app/SuggestProfileCover_3ec640c4","OK/css-loader":"res/js/app/css-loader_9b0bd807","OK/has":"res/js/app/has_d42e7b6f","OK/NotificationsMarkAsRead":"res/js/app/NotificationsMarkAsRead_77267aea","OK/AuthLoginPopup":"res/js/app/AuthLoginPopup_1cb829e4","OK/MallBasket":"res/js/app/MallBasket_7b6f99df","OK/MemoriesEventBuses":"res/js/app/MemoriesEventBuses_2ff72612","webrtc/adapter":"res/js/lib/webrtc/adapter-7.1.1_3f2fe827","OK/PortletReactLazy":"res/js/app/PortletReactLazy_b1eb912d","OK/MallDMROuterCallback":"res/js/app/MallDMROuterCallback_dfc04e4d","OK/GoSearch":"res/js/app/GoSearch_d3f507fa","OK/ProfileCover":"res/js/app/ProfileCover_aadeaa58","OK/AmPromo":"res/js/app/AmPromo_82be2c27","OK/BoostPostStatsDialog":"res/js/app/BoostPostStatsDialog_81d5058e","OK/LiveReaction":"res/js/app/LiveReaction_514c04e1","OK/Html5interactive":"res/js/app/Html5interactive_6c5af5ff","OK/PostingFormLinkImageSelect":"res/js/app/PostingFormLinkImageSelect_33d3c317","OK/react-tag-loader.d":"res/js/app/react-tag-loader.d_6556f0cd","OK/WidgetSuggest":"res/js/app/WidgetSuggest_611d6ce0","OK/AutopinSettingsPopup":"res/js/app/AutopinSettingsPopup_46d09f7d","OK/ProfileCoverDialogPhotoList":"res/js/app/ProfileCoverDialogPhotoList_a152bc81","OK/Carousel":"res/js/app/Carousel_b1e9b051","OK/CircleBoostInfo":"res/js/app/CircleBoostInfo_9227dcf3","jquery.ui.droppable":"res/js/lib/jquery.ui.droppable_4f3c16ab","lottie":"res/js/lib/lottie.min.5.7.6_1d877156","OK/NavigationProgressBar":"res/js/app/NavigationProgressBar_1add416","OK/AdvertsPicker":"res/js/app/AdvertsPicker_3cc8e82c","b/videostream":"res/js/b/videostream_f3df1d43","OK/MallDeliveryFieldsAutosave":"res/js/app/MallDeliveryFieldsAutosave_d5ce9fbe","OK/WidgetAdCanvasCreate":"res/js/app/WidgetAdCanvasCreate_6d565dd","OK/FeedVirtualList":"res/js/app/FeedVirtualList_910a15f2","OK/TwoFactorAuth":"res/js/app/TwoFactorAuth_2cc95c7b","OK/SuggestProfileCoverPortlet":"res/js/app/SuggestProfileCoverPortlet_ec7ab598","OK/FavPhotos":"res/js/app/FavPhotos_3a2eb32f","OK/LazyIconsCache":"res/js/app/LazyIconsCache_2f677c5f","OK/BirthdayNotifAction":"res/js/app/BirthdayNotifAction_88de55f9","OK/EventFactory":"res/js/app/EventFactory_9faf0430","OK/MotivatorGameCarousel":"res/js/app/MotivatorGameCarousel_7e36c039","OK/Surprise":"res/js/app/Surprise_452e9ae5","b/discussions":"res/js/b/discussions_7e810658","OK/GiftToFriendWithSections":"res/js/app/GiftToFriendWithSections_d63166b3","text":"res/js/lib/text_aedac35d","OK/PinnedTopicSort":"res/js/app/PinnedTopicSort_b3a74c7e","b/adsManager":"res/js/b/adsManager_248714d8","OK/InlineDropdown":"res/js/app/InlineDropdown_523f7700","OK/JoinCallLanding":"res/js/app/JoinCallLanding_e2bc950b","OK/ProAvatarAnimation":"res/js/app/ProAvatarAnimation_2e808a78","OK/AttachLink":"res/js/app/AttachLink_74a81712","OK/RandomCongratsCard":"res/js/app/RandomCongratsCard_9ce82baf","OK/StickyNavside":"res/js/app/StickyNavside_b321b08a","doT":"res/js/lib/doT_6d67910d","OK/GroupPayment":"res/js/app/GroupPayment_27d53177","OK/VideoCallStream":"res/js/app/VideoCallStream_b9d62f2","OK/withFriendsEditor":"res/js/app/withFriendsEditor_1b4e1733","OK/VideoCardMenu":"res/js/app/VideoCardMenu_e3aaddf7","OK/ViewportWidthObserver":"res/js/app/ViewportWidthObserver_2d867618","OK/MemoryImage":"res/js/app/MemoryImage_9e4f51ea","OK/SimplePopup":"res/js/app/SimplePopup_b8a7e432","OK/GroupCallWidgetSettings":"res/js/app/GroupCallWidgetSettings_bfa1288","OK/MallProductPurchase":"res/js/app/MallProductPurchase_20c1c5a8","OK/AdvertNavigation":"res/js/app/AdvertNavigation_b2087411","b/messagesLayer":"//st.mycdn.me/static/music/2020-05-07/messagesLayer_3ac8bdb7","b/registration":"res/js/b/registration_4813865e","OK/WidgetAdCanvasPreview":"res/js/app/WidgetAdCanvasPreview_d9a7888b","b/contentWidget":"res/js/b/contentWidget_5bd3fa0f","OK/gdprCmp":"res/js/app/gdprCmp_b9bfbd47","OK/WebRTCUtils":"res/js/app/WebRTCUtils_fbe4dbb","OK/GroupModeratorRole":"res/js/app/GroupModeratorRole_30eaf0f3","OK/GeoSelect":"res/js/app/GeoSelect_68deb313","OK/InteractiveArt":"res/js/app/InteractiveArt_708f72ba","OK/AdvertSort":"res/js/app/AdvertSort_e939cda6","OK/Footer":"res/js/app/Footer_6614fee7","OK/InviteFriendsToGroup":"//st.mycdn.me/static/messages/2020-03-19invite/InviteFriendsToGroup","OK/MistakeHelper":"res/js/app/MistakeHelper_f4488bf3","OK/MallDeliveryAddress":"res/js/app/MallDeliveryAddress_3d412657","OK/SortStickers":"res/js/app/SortStickers_427a7d5e","mrg-smokescreen/StyleSheets.NativeParser":"res/js/lib/mrg-smokescreen/StyleSheets.NativeParser_6c970de5","OK/RbTopCounter":"res/js/app/RbTopCounter_c8aecbcc","OK/tmr":"res/js/app/tmr_faac3caf","OK/FriendshipFeedPortlet":"res/js/app/FriendshipFeedPortlet_39dbfc0f","OK/HideSetPro":"res/js/app/HideSetPro_5b9d4ba0","OK/MemoriesFeedPortlet":"res/js/app/MemoriesFeedPortlet_64cc37d3","OK/MrgCounterDot":"res/js/app/MrgCounterDot_550e8ec1","OK/PhotoLayerShortLink":"res/js/app/PhotoLayerShortLink_baaf9848","OK/ProfileCoverSettingsButtonDialog":"res/js/app/ProfileCoverSettingsButtonDialog_1d704c28","OK/adLinkInput":"res/js/app/adLinkInput_df1ab89c","OK/AdvSlider":"res/js/app/AdvSlider_b165b30a","OK/ProgressCircleSimple":"res/js/app/ProgressCircleSimple_7f7aebf0","OK/PresentPlay":"res/js/app/PresentPlay_b83ced35","OK/EventBus":"res/js/app/EventBus_987bdeb8","OK/LogAggregator":"res/js/app/LogAggregator_1b3ca113","OK/search":"res/js/app/search_fe6c9a57","mrg-smokescreen/Welter":"res/js/lib/mrg-smokescreen/Welter_1d89b7bd","OK/endorphin-loader":"res/js/app/endorphin-loader_c908210c","OK/DiscoveryEventBuses":"res/js/app/DiscoveryEventBuses_4bab74a9","OK/EventBus.d":"res/js/app/EventBus.d_6556f0cd","OK/BookmarkCardDecorator":"res/js/app/BookmarkCardDecorator_d188b0aa","OK/MusicTrack":"res/js/app/MusicTrack_37a77dd9","OK/GroupPassAdminRights":"res/js/app/GroupPassAdminRights_d019e4c2","highstock":"res/js/lib/highstock_d85a437f","OK/MotivatorShowcase":"res/js/app/MotivatorShowcase_6558c5fa","Clipboard":"res/js/lib/clipboard_d4fbc119","OK/Pushes":"res/js/app/Pushes_c6ff0004","OK/MainFeedsNewFeedPush":"res/js/app/MainFeedsNewFeedPush_9437e675","OK/VideoChatPush":"res/js/app/VideoChatPush_8074f511","jquery.ui.sortable":"res/js/lib/jquery.ui.sortable_4fe47671","OK/AjaxLinkHook":"res/js/app/AjaxLinkHook_d1111201","OK/SearchInputReact":"res/js/app/SearchInputReact_ab8310b0","OK/DiscoveryEventBusesModule":"res/js/app/DiscoveryEventBusesModule_8e7a37cd","OK/MallBasketAddress":"res/js/app/MallBasketAddress_15b6a555","OK/StickyPanel":"res/js/app/StickyPanel_30b3bb49","OK/VideoLayerPins":"res/js/app/VideoLayerPins_a7e67919","OK/PhotoUploadStarter":"res/js/app/PhotoUploadStarter_3b32f8a6","OK/CountdownTextarea":"res/js/app/CountdownTextarea_6117fe3d","OK/GroupCallPush":"res/js/app/GroupCallPush_ef238a2c","OK/ScrollSlider":"res/js/app/ScrollSlider_bf18f145","OK/Map":"res/js/app/Map_c07ab40","OK/StartLiveForm":"res/js/app/StartLiveForm_a968d79a","OK/ToolbarGrowl":"res/js/app/ToolbarGrowl_9adf4b51","OK/immortalRegimentCounter":"res/js/app/immortalRegimentCounter_b686f54e","OK/GoShare":"res/js/app/GoShare_b64421ce","OK/WSConnectionCheck":"res/js/app/WSConnectionCheck_e2b34cd7","OK/Loader":"res/js/app/Loader_d1ddff1","OK/WidgetAdCanvasConstructor":"res/js/app/WidgetAdCanvasConstructor_6d565dd","dailyphoto-layer":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-layer/dailyphoto-layer","OK/Toggler":"res/js/app/Toggler_b91672f2","OK/YoulaAdvertsFeedPortlet":"res/js/app/YoulaAdvertsFeedPortlet_a454ae4a","mrg-smokescreen/Honeypot":"res/js/lib/mrg-smokescreen/Honeypot_13d52ec8","OK/cropRect":"res/js/app/cropRect_432894ed","OK/FAPIClient":"res/js/app/FAPIClient_4fdfd32b","OK/MemoryEditor":"res/js/app/MemoryEditor_4b4036c0","OK/ToolbarReact":"res/js/app/ToolbarReact_5c701af2","OK/ClipboardUrl":"res/js/app/ClipboardUrl_1d030b1","b/mall":"res/js/b/mall_881bb13d","OK/scrollToTop":"res/js/app/scrollToTop_f98ea938","OK/HelpFeedbackAttachmentForm":"res/js/app/HelpFeedbackAttachmentForm_5283503f","OK/AddHolidayPopup":"res/js/app/AddHolidayPopup_ca59cae4","OK/Survey":"res/js/app/Survey_48eff3e3","OK/UserAlbumSettings":"res/js/app/UserAlbumSettings_5d3a145f","OK/EventsCalendarScroll":"res/js/app/EventsCalendarScroll_7cbb3ffc","OK/Link":"res/js/app/Link_d7e9018b","OK/StickerOnSmileSuggester":"res/js/app/StickerOnSmileSuggester_680533e9","OK/PromoAvatarRecommendLink":"res/js/app/PromoAvatarRecommendLink_d7592494","OK/AcceptGifts":"res/js/app/AcceptGifts_6bb0a0c6","OK/AttachVideoUploader":"res/js/app/AttachVideoUploader_b88a4547","OK/emojiarea":"//st.mycdn.me/static/messages/2021-04-13ls10/emojiarea","OK/StickyPlayer":"res/js/app/StickyPlayer_6cef6a","OK/VideoHistoryHelper":"res/js/app/VideoHistoryHelper_dc45cd03","OK/ProfileCoverSlider":"res/js/app/ProfileCoverSlider_cc3806f1","candy":"//hls.goodgame.ru/candy/candy.min","OK/GroupDonate":"res/js/app/GroupDonate_6d78327c","OK/AmHideBoostBtn":"res/js/app/AmHideBoostBtn_e0919a65","b/messages2":"//st.mycdn.me/static/messages/1-5-16/messages/bootstrap","jquery":"res/js/lib/jquery-1.8.3_20a32fe5","OK/Payment":"res/js/app/Payment_6b6851d7","OK/dailyphoto-archive":"res/js/app/dailyphoto-archive_2af749ae","jquery.ui.datepicker":"res/js/lib/jquery.ui.datepicker-1.8.16_d896cf3f","OK/UnconfirmedAutoPinsPortlet":"res/js/app/UnconfirmedAutoPinsPortlet_3dd8ff08","OK/FriendshipCardCounters":"res/js/app/FriendshipCardCounters_1168a084","OK/ActiveTopics":"res/js/app/ActiveTopics_9210ef6f","OK/GameVideoAdv":"res/js/app/GameVideoAdv_a6cc61ea","OK/RecommendedGroupsFeedPortlet":"res/js/app/RecommendedGroupsFeedPortlet_ddb02303","OK/FeedDeleteStub":"res/js/app/FeedDeleteStub_6d39f095","OK/uuid":"res/js/app/uuid_5299e130","OK/CultureMotivatorContent":"res/js/app/CultureMotivatorContent_eb71d8ce","OK/FriendsStream":"res/js/app/FriendsStream_c911dd6f","OK/ImagesLoadCallback":"res/js/app/ImagesLoadCallback_84516a71","OK/ReactIconsWithCounter":"res/js/app/ReactIconsWithCounter_4862493","jquery.ui.core":"res/js/lib/jquery.ui.core_42ff0b7c","OK/GroupStatAdvancedPage":"res/js/app/GroupStatAdvancedPage_ffe5806f","OK/SharedAlbumSettings":"res/js/app/SharedAlbumSettings_dcbd25b7","OK/NonBlockingTip.d":"res/js/app/NonBlockingTip.d_6556f0cd","OK/MediaTopicAdvertLayerBody":"res/js/app/MediaTopicAdvertLayerBody_857a5aad","OK/withFriends":"res/js/app/withFriends_f8cc38d5","OK/alf":"res/js/app/alf_c73ef106","OK/FeedFirstKlassComponent":"res/js/app/FeedFirstKlassComponent_435a0566","OK/RegisterSpamLRBlock":"res/js/app/RegisterSpamLRBlock_93894bad","OK/AppModerationLayer":"res/js/app/AppModerationLayer_7ac303b8","OK/LogGridSeen":"res/js/app/LogGridSeen_e76af69f","OK/CallsPromo":"res/js/app/CallsPromo_1d6a17f8","OK/GroupSettingsFormToggler":"res/js/app/GroupSettingsFormToggler_6c84d3d3","OK/Poll":"res/js/app/Poll_3d4c7993","OK/ProcessMoreInfo":"res/js/app/ProcessMoreInfo_b35b56ed","OK/FAPI":"res/js/app/FAPI_510f80cc","OK/immortalRegiment":"res/js/app/immortalRegiment_af998c32","OK/Thumbnails":"res/js/app/Thumbnails_3e705b43","OK/TransitionAndTransform":"res/js/app/TransitionAndTransform_4e2309b6","OK/react-loader":"res/js/app/react-loader_e998fef2","OK/FriendStream":"res/js/app/FriendStream_b6374cf1","OK/OkLivePromoMap":"res/js/app/OkLivePromoMap_9683a4b8","OK/saveText":"res/js/app/saveText_3b9ce54f","OK/MagicAlbumPhotos":"res/js/app/MagicAlbumPhotos_d3b8eaa0","OK/tabs":"res/js/app/tabs_a99dd809","jquery.jcrop":"res/js/lib/jquery.jcrop-0.9.9.ok_16e650c1","OK/RandomCongratsSplash":"res/js/app/RandomCongratsSplash_8c0ca7ef","b/postingTimerBundle":"res/js/b/postingTimerBundle_128f181b","OK/SuggestedProfileCover":"res/js/app/SuggestedProfileCover_45386fec","OK/PaymentVideoAdv":"res/js/app/PaymentVideoAdv_4f578290","OK/AttachUploader":"res/js/app/AttachUploader_449fa487","OK/WebPush":"res/js/app/WebPush_8e2ab839","OK/MoviesRecommendationsController":"res/js/app/MoviesRecommendationsController_b7ee6d77","OK/RemoveFromRecentPhoto":"res/js/app/RemoveFromRecentPhoto_15a99193","b/multiSelect":"res/js/b/multiSelect_5d7d51e0","OK/DropdownMenu":"res/js/app/DropdownMenu_d90fa4a","OK/locations":"res/js/app/locations_b7cce423","OK/postingFormFilter":"res/js/app/postingFormFilter_15392bb0","OK/VideoAutoplayLayer":"res/js/app/VideoAutoplayLayer_1ab3f19d","OK/Accordion":"res/js/app/Accordion_183bb0d8","OK/scroll":"res/js/app/scroll_934ab4dd","OK/ToolbarBack":"res/js/app/ToolbarBack_bef3b5bb","OK/MediaTopicSettingsForm":"res/js/app/MediaTopicSettingsForm_ab02bdbc","OK/PopLayer":"res/js/app/PopLayer_9cac636e","OK/WidgetRescuerFriends":"res/js/app/WidgetRescuerFriends_d70c7afc","OK/PostAfterUpload":"res/js/app/PostAfterUpload_18c04171","OK/StickerSuggester":"res/js/app/StickerSuggester_9b9d9b8b","OK/PhotoSeenLogger":"res/js/app/PhotoSeenLogger_3ae61c7d","OK/UploadProgressBar":"res/js/app/UploadProgressBar_a6638352","OK/LogSeen":"res/js/app/LogSeen_c4c3b385","OK/Relations":"res/js/app/Relations_141c4266","OK/StickerSender":"res/js/app/StickerSender_c28ae61e","OK/AdVideoPicker":"res/js/app/AdVideoPicker_34295950","OK/SupportChatReactOpener":"res/js/app/SupportChatReactOpener_fd7fbbb4","mrg-smokescreen/StyleSheets.Item":"res/js/lib/mrg-smokescreen/StyleSheets.Item_c9757bf2","OK/ChangeUserAvatar":"res/js/app/ChangeUserAvatar_5ec9795","OK/HookModel":"res/js/app/HookModel_8044813f","OK/YandexMapsApi":"res/js/app/YandexMapsApi_74902487","iframe-resizer":"res/js/lib/iframe-resizer_d2acdd06","OK/SimilarPhotos":"res/js/app/SimilarPhotos_8b40da4b","OK/MassSendPostcard":"res/js/app/MassSendPostcard_494ffe94","OK/PopLayerLogin":"res/js/app/PopLayerLogin_f44b5164","OK/LikeComponent":"res/js/app/LikeComponent_dcb3ef8","OK/SettingsNotificationsPopup":"res/js/app/SettingsNotificationsPopup_137e8931","OK/query":"res/js/app/query_177d85a","b/fancyGifts":"res/js/b/fancyGifts_e6869ad3","OK/endorphin":"res/js/app/endorphin_68125a02","OK/NonBlockingTip":"res/js/app/NonBlockingTip_37fb36ee","OK/FilterTags":"res/js/app/FilterTags_f596a0ea","OK/ShortcutMenuReact":"//st.mycdn.me/static/hf/2020-09-03sc/ShortcutMenuReact","mrg-smokescreen/Utils":"res/js/lib/mrg-smokescreen/Utils_fe15bae3","OK/OkLivePromoEditor":"res/js/app/OkLivePromoEditor_7d982954","OK/SendActionCongratsFriends":"res/js/app/SendActionCongratsFriends_d982fcbe","OK/AltGroupSettingsApp":"res/js/app/AltGroupSettingsApp_3c3f726c","OK/MotivatorGameSlot":"res/js/app/MotivatorGameSlot_3c41fd43","OK/FirstInteractiveLogger":"res/js/app/FirstInteractiveLogger_692654d8","OK/VideoCopyrightAdmin":"res/js/app/VideoCopyrightAdmin_42949e54","OK/dailyphoto-autoplay":"res/js/app/dailyphoto-autoplay_2af749ae","OK/installAltGroupApp":"res/js/app/installAltGroupApp_59fbfafe","OK/number":"res/js/app/number_d399d029","L10n/datepicker-uk":"res/js/L10n/datepicker-uk_c854d288","OK/FriendsSearch":"res/js/app/FriendsSearch_dd4cd8b9","OK/PaymentContext":"res/js/app/PaymentContext_7f83df89","detect-zoom":"res/js/lib/detect-zoom_670ab469","OK/MusicPlayButton":"res/js/app/MusicPlayButton_5c4ea930","OK/cookieBanner":"res/js/app/cookieBanner_1f07b0b","OK/GroupMainLayer":"res/js/app/GroupMainLayer_73bc60af","OK/PostingFormVideoPicker":"res/js/app/PostingFormVideoPicker_dfb22785","b/banners":"res/js/b/banners_27d62e07","L10n/datepicker-tr":"res/js/L10n/datepicker-tr_7471f4d0","OK/PrivateProfileTumbler":"res/js/app/PrivateProfileTumbler_eef373b4","OK/DiscoveryGrid":"res/js/app/DiscoveryGrid_a0f3efa1","OK/SimpleSendPresent":"res/js/app/SimpleSendPresent_58532b50","OK/GroupAllMessagesBubble":"res/js/app/GroupAllMessagesBubble_efe8ae88","OK/Toolbar":"res/js/app/Toolbar_a415f7d8","b/shortcutMenuBundle":"res/js/b/shortcutMenuBundle_680a54f5","okVideoPlayerUtils":"//st.mycdn.me/static/MegaPlayer/10-11-3/okVideoPlayerUtils.min","OK/PhoneMask":"res/js/app/PhoneMask_16deaf9c","noext":"res/js/lib/noext_7935a4d9","OK/WebPushSettings":"res/js/app/WebPushSettings_240f68cd","jquery.ui.mouse":"res/js/lib/jquery.ui.mouse_a7cd149d","OK/SeenGroupLogger":"res/js/app/SeenGroupLogger_45cc56d3","b/ddMenu":"res/js/b/ddMenu_c725e80a","OK/MemoryPreview":"res/js/app/MemoryPreview_3d9599da","OK/emojiScroll":"res/js/app/emojiScroll_57fc4765","dailyphoto-reactions":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-reactions/dailyphoto-reactions","OK/LinkDetector":"res/js/app/LinkDetector_ec173922","OK/mainAvatarUpdater":"res/js/app/mainAvatarUpdater_ac1cd3af","OK/AmPromoRedirect":"//st.mycdn.me/static/hf/2020-04-03am3/AmPromoRedirect","OK/MemoryText":"res/js/app/MemoryText_ad10167","FileAPI":"res/js/lib/FileAPI_6706a68a","OK/Charts":"res/js/app/Charts_f15fd2cd","OK/ReshareLayer":"res/js/app/ReshareLayer_c26e769","OK/VideoAutoplayFlow":"res/js/app/VideoAutoplayFlow_5358f447","OK/ToolbarBubble":"res/js/app/ToolbarBubble_b0fdfa2c","OK/FeedExperiments":"res/js/app/FeedExperiments_6292c52a","OK/GroupMessagesBubble":"res/js/app/GroupMessagesBubble_5851302d","OK/Smokescreen":"res/js/app/Smokescreen_80c92de8","OK/ProgressCircle":"res/js/app/ProgressCircle_4197c6d4","OK/OptionsEditor":"res/js/app/OptionsEditor_b5252c27","OK/CollageSlider":"res/js/app/CollageSlider_5fe609c2","L10n/datepicker-ro":"res/js/L10n/datepicker-ro_6d380e19","chromecast":"//www.gstatic.com/cv/js/sender/v1/cast_sender","OK/PhotoLayerDeleteRestore":"res/js/app/PhotoLayerDeleteRestore_bcaa9281","OK/Loader.d":"res/js/app/Loader.d_6556f0cd","OK/BlockHider":"res/js/app/BlockHider_c3b9359","OK/TopicViews":"res/js/app/TopicViews_803ad398","OK/PhotoUploadController":"//st.mycdn.me/static/hf/2020-12-14PhotoUploadController/PhotoUploadController","OK/RemoveGroupToGroup":"res/js/app/RemoveGroupToGroup_b42b90cd","b/p2p":"res/js/b/p2p_bab12e0b","b/videoEditor":"res/js/b/videoEditor_6c0b2a23","OK/PhotoLotteryPortlet":"res/js/app/PhotoLotteryPortlet_cb3b531e","OK/SendActionCongratsCard":"res/js/app/SendActionCongratsCard_d0ce5174","OK/ReactComponent":"res/js/app/ReactComponent_174b5002","OK/LottieSticker":"res/js/app/LottieSticker_9522073e","OK/RandomCongratsReset":"res/js/app/RandomCongratsReset_ce51f0bd","OK/react-tag-loader":"res/js/app/react-tag-loader_c4d82cc7","REACT/core":"res/react/core-client_e566932f","OK/NotificationPermissionPopup":"res/js/app/NotificationPermissionPopup_70483e4","OK/Pixel":"res/js/app/Pixel_ad9eaa7f","OK/Surveys":"res/js/app/Surveys_a092f1c8","mrg/ads":"//r.mradx.net/img/2D/6DC085","OK/JsonCustomHook":"res/js/app/JsonCustomHook_4a923cd0","OK/textarea":"res/js/app/textarea_2c74a18d","OK/dailyphoto-model":"res/js/app/dailyphoto-model_2af749ae","OK/ReactionsFeedback":"res/js/app/ReactionsFeedback_b522f284","OK/editableLabel":"res/js/app/editableLabel_9a14a95b","OK/GroupPurchaseBoosts":"res/js/app/GroupPurchaseBoosts_1ce1b80d","OK/AttachPreview":"res/js/app/AttachPreview_c5f2345c","OK/PhotoUploadInput":"res/js/app/PhotoUploadInput_a3d971ec","OK/GroupMemberBlocking":"res/js/app/GroupMemberBlocking_ce94876a","OK/MallSearchFilter":"res/js/app/MallSearchFilter_115b1d2a","mrg-smokescreen/StyleSheets.Parser":"res/js/lib/mrg-smokescreen/StyleSheets.Parser_579e18f6","OK/OhManager":"res/js/app/OhManager_c0a37d56","OK/ExpandLeftColumn":"res/js/app/ExpandLeftColumn_5373c72f","OK/ToolbarLogoGrowl":"res/js/app/ToolbarLogoGrowl_756cdd61","OK/PostingFormQuitConfirmation":"res/js/app/PostingFormQuitConfirmation_72043c10","OK/https":"res/js/app/https_5cd97298","OK/RecommendedPhotos":"res/js/app/RecommendedPhotos_9bb1be5c","OK/dailyphoto-avatar":"res/js/app/dailyphoto-avatar_59dd0e35","OK/webapi":"res/js/app/webapi_181fd38e","OK/GroupJoinRequestsEntityList":"res/js/app/GroupJoinRequestsEntityList_d6e516ab","OK/VideoPreviewAutoplay":"res/js/app/VideoPreviewAutoplay_65836305","leaflet":"res/js/lib/leaflet_17d6ca39","OK/DiscoverySearch":"res/js/app/DiscoverySearch_aaef81d3","OK/PresentVoiceMsg":"res/js/app/PresentVoiceMsg_b7a17fa9","mrg-nano-xhr":"res/js/lib/mrg-nano-xhr_113e42e","OK/phoneMaskingUtils":"res/js/app/phoneMaskingUtils_f0c5b8ad","b/photowall":"res/js/b/photowall_3fa7be14","OK/Suggest":"res/js/app/Suggest_2dae816f","OK/CitymobilQuestions":"res/js/app/CitymobilQuestions_9ff95431","OK/VideoUploader":"res/js/app/VideoUploader_eccd8bf0","OK/BehaviorLogger":"res/js/app/BehaviorLogger_2c33296c","OK/VideoMiniPlayer":"res/js/app/VideoMiniPlayer_a88dd072","OK/AjaxNavigationLog":"res/js/app/AjaxNavigationLog_20c9cb21","OK/GiftToFriend":"res/js/app/GiftToFriend_2d659448","OK/AttachPhotoUploader":"res/js/app/AttachPhotoUploader_cfc53505","OK/YoulaPostAdvert":"res/js/app/YoulaPostAdvert_54687a38","b/messages2helper":"res/js/b/messages2helper_97e1622b","OK/PhotoAlbumsSM":"res/js/app/PhotoAlbumsSM_f394c1c4","OK/PickerToMessagesBridge":"res/js/app/PickerToMessagesBridge_3ba725e5","OK/SetAvatarFromFeed":"res/js/app/SetAvatarFromFeed_17f4a61f","OK/GroupSettingsRights":"res/js/app/GroupSettingsRights_9ff182d4","OK/WidgetAdCanvasStandalonePreview":"res/js/app/WidgetAdCanvasStandalonePreview_66330882","OK/MotivatorGameGrid":"res/js/app/MotivatorGameGrid_8e840e24","OK/Skrepochka":"res/js/app/Skrepochka_84114891","OK/EventsCalendar":"res/js/app/EventsCalendar_badfef5","OK/capture.d":"res/js/app/capture.d_6556f0cd","jquery.autoGrowInput":"res/js/lib/jquery.autoGrowInput_7dfb8ab6","OK/GroupJournalPage":"res/js/app/GroupJournalPage_c68be55a","OK/MallDeliveryYandexSuggestField":"res/js/app/MallDeliveryYandexSuggestField_78733896","OK/SocialSearch":"res/js/app/SocialSearch_42c82f38","b/entitySuggest":"res/js/b/entitySuggest_a181cec8","OK/ProgressText":"res/js/app/ProgressText_cc3e0d62","OK/ShortcutMenuReplaceItem":"res/js/app/ShortcutMenuReplaceItem_3369bace","b/suggestBundle":"res/js/b/suggestBundle_80c4c34c","OK/FavoritePhotos":"res/js/app/FavoritePhotos_7bb94f4f","OK/AmBoostBtn":"res/js/app/AmBoostBtn_6cbb3800","OK/AppGroupInvite":"res/js/app/AppGroupInvite_112dc903","OK/MTLayerOpen":"res/js/app/MTLayerOpen_a75232f9","OK/crop":"res/js/app/crop_3aac0eb5","OK/CreateJoinLink":"res/js/app/CreateJoinLink_8554c0ca","OK/StickerOverlays":"res/js/app/StickerOverlays_9cc1cc21","OK/KlassOverProduct":"res/js/app/KlassOverProduct_3fd3c84e","OK/Datepicker":"res/js/app/Datepicker_44fdc7f3","OK/DiscussionManager":"res/js/app/DiscussionManager_d6ec484f","OK/UploadVideoQuestion":"res/js/app/UploadVideoQuestion_b06c296b","OK/VideoEmbed":"res/js/app/VideoEmbed_412fdba8","OK/SubmitOnChange":"res/js/app/SubmitOnChange_77d09a0a","OK/EventBusesForPhoto":"res/js/app/EventBusesForPhoto_4479e59f","OK/pts":"res/js/app/pts_45483173","OK/AdCanvasConstructorIframe":"res/js/app/AdCanvasConstructorIframe_1dfa1af1","jquery.ui.draggable":"res/js/lib/jquery.ui.draggable_d327c8b5","OK/MallSearchFilterTags":"res/js/app/MallSearchFilterTags_c5b1013b","OK/PhotoUploadDnd":"res/js/app/PhotoUploadDnd_b0b765fd","OK/MallPayMethodSelector":"res/js/app/MallPayMethodSelector_14025bf9","OK/FeelingPostLayer":"res/js/app/FeelingPostLayer_11e49f90","OK/Faq":"res/js/app/Faq_17f5f20b","OK/SpriteAnimation":"res/js/app/SpriteAnimation_2c10e623","OK/FriendsOnline4thColumn":"res/js/app/FriendsOnline4thColumn_77515a67","OK/CityMatchSuggestionsProxy":"res/js/app/CityMatchSuggestionsProxy_203b7673","OK/KlassOverPhoto":"res/js/app/KlassOverPhoto_e2fbfccc","OK/ImageRotation":"res/js/app/ImageRotation_53783ca5","OK/MainContentHeader":"res/js/app/MainContentHeader_8de41798","OK/PostingFormAdLink":"res/js/app/PostingFormAdLink_3dcfe6b0","MSG/bootstrap":"//st.mycdn.me/static/messages/res/bootstrap-1-5-16","OK/OfferPromo":"res/js/app/OfferPromo_dee08a39","OK/ShortcutMenuAdapter.d":"res/js/app/ShortcutMenuAdapter.d_6556f0cd","OK/GroupCategorySelect":"res/js/app/GroupCategorySelect_e47d601d","OK/MallBuyWait":"res/js/app/MallBuyWait_f0d18713","mrg-smokescreen/Locator":"res/js/lib/mrg-smokescreen/Locator_74ddbeca","OK/OKVideo.d":"res/js/app/OKVideo.d_6556f0cd","OK/VideoChatPermissionsHint":"res/js/app/VideoChatPermissionsHint_31b5717a","b/messagesButton":"res/js/b/messagesButton_a2f2b8d1","OK/photowall":"//st.mycdn.me/static/hf/2018-04-28/photowall","OK/BlockUpdater":"res/js/app/BlockUpdater_1cdd7e14","OK/VideoHelper":"res/js/app/VideoHelper_43ff4232","MSG":"//st.mycdn.me/static/messages/res","dailyphoto-slider":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-slider/dailyphoto-slider","OK/AttachPicker":"res/js/app/AttachPicker_178aaf16","swfobject":"res/js/lib/swfobject-2.3_d45181da","OK/WidgetLeadAdsConstructor":"res/js/app/WidgetLeadAdsConstructor_8d68a1d3","b/gifts":"res/js/b/gifts_8bd16321","OK/GroupJoinRequests":"res/js/app/GroupJoinRequests_f4aa3cd8","OK/PostingFormPicker":"res/js/app/PostingFormPicker_aea3dff3","OK/GroupPhotoUploader":"res/js/app/GroupPhotoUploader_961fabb0","mrg-smokescreen/Cid":"res/js/lib/mrg-smokescreen/Cid_3e81426c","OK/WidgetSuggestMob":"res/js/app/WidgetSuggestMob_611d6ce0","OK/JavascriptHook":"res/js/app/JavascriptHook_230abd60","OK/EventsCalendarMarks":"res/js/app/EventsCalendarMarks_fb81b94f","OK/GiftCardPixel":"res/js/app/GiftCardPixel_292bfeb8","OK/ProfileCoverSettingsButtonRemove":"res/js/app/ProfileCoverSettingsButtonRemove_8f30de41","OK/VideoChatSound":"res/js/app/VideoChatSound_bb143db7","OK/PostingFormLink":"res/js/app/PostingFormLink_d7d4bdee","OK/autosize":"res/js/app/autosize_5c2747af","OK/SendActionCongratsMenu":"res/js/app/SendActionCongratsMenu_d5d51c92","OK/LazyIconsCache.d":"res/js/app/LazyIconsCache.d_6556f0cd","OK/LinkedHooksStore":"res/js/app/LinkedHooksStore_cfbf2a31","OK/alf2":"//st.mycdn.me/static/hf/2021-03-30alf/alf2.min","OK/SendSocialFriendshipRequest":"res/js/app/SendSocialFriendshipRequest_d4275ab3","OK/Tiler":"res/js/app/Tiler_d75ff8ba","OK/MediaTopicWidget":"res/js/app/MediaTopicWidget_c944106","b/search":"res/js/b/search_dd13611d","OK/LoginVisual":"res/js/app/LoginVisual_59e72d0e","OK/PopupTipContainer":"res/js/app/PopupTipContainer_28340b66","OK/ProfileCoverButton":"res/js/app/ProfileCoverButton_2d98eb99","OK/BusinessProfileSettings":"res/js/app/BusinessProfileSettings_41dca19a","OK/react-loader.d":"res/js/app/react-loader.d_6556f0cd","OK/ExpandLink":"res/js/app/ExpandLink_5ce0d5ab","L10n/datepicker-kk":"res/js/L10n/datepicker-kk_9524185f","OK/MallWaitingProcessing":"res/js/app/MallWaitingProcessing_f558dac9","OK/PostingFormOffer":"res/js/app/PostingFormOffer_24069a4d","OK/SystemTextPopup":"res/js/app/SystemTextPopup_766f91b6","OK/EasterEgg":"res/js/app/EasterEgg_c271347c","OK/BanDataCfgJs":"res/js/app/BanDataCfgJs_fcc34e4c","OK/MediaTopicAdvertTemplate":"res/js/app/MediaTopicAdvertTemplate_66898d00","OK/GroupAppOpen":"res/js/app/GroupAppOpen_a341245c","dailyphoto-autoplay":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-autoplay/dailyphoto-autoplay","OK/MallProductReviewsWait":"res/js/app/MallProductReviewsWait_f2a95e24","OK/ProfileButtonSelector":"res/js/app/ProfileButtonSelector_3a914b53","OK/GroupReportBadRecommendation":"res/js/app/GroupReportBadRecommendation_30ef0fbd","OK/GroupVideoPortlet":"res/js/app/GroupVideoPortlet_5e6170f2","OK/autofocus":"res/js/app/autofocus_d6083eca","L10n/datepicker-ka":"res/js/L10n/datepicker-ka_38539bb3","dailyphoto-model":"//st.mycdn.me/static/dailyphoto/1-5-3/dailyphoto-model/dailyphoto-model","OK/Notifications":"res/js/app/Notifications_ed312ef0","OK/WidgetAdCanvasStandalonePreviewMob":"res/js/app/WidgetAdCanvasStandalonePreviewMob_66330882","OK/animations":"res/js/app/animations_166c7448","OK/Feed":"res/js/app/Feed_db3cd187","b/recovery":"res/js/b/recovery_b5bf569d","OK/FrameRateLogger":"res/js/app/FrameRateLogger_4a62c3ae","OK/MixedGiftsGrid":"res/js/app/MixedGiftsGrid_d1449402","OK/SortedLinkedList":"res/js/app/SortedLinkedList_a495c73f","OK/giftAcceptance":"res/js/app/giftAcceptance_2ea0fda8","OK/VideoAutoplayFlowAlt":"res/js/app/VideoAutoplayFlowAlt_adf14f14","OK/FootballSportMail":"res/js/app/FootballSportMail_a21d0eaa","OK/UserInlineSearch":"res/js/app/UserInlineSearch_dde4d0e0","OK/AbstractNativeHook":"res/js/app/AbstractNativeHook_ee010155","OK/pts.d":"res/js/app/pts.d_6556f0cd","OK/ToolbarGrowl.d":"res/js/app/ToolbarGrowl.d_6556f0cd","OK/TextField":"res/js/app/TextField_4d4006c8","OK/ColorPickerCatalogBtn":"res/js/app/ColorPickerCatalogBtn_457ec3f9","OK/PaymentVideoAdvSlotChecker":"res/js/app/PaymentVideoAdvSlotChecker_2df60ca0","OK/SelectPromoAvatar":"res/js/app/SelectPromoAvatar_5c2aea0c","OK/LiveSticker":"//st.mycdn.me/static/messages/2021-04-13ls10/LiveSticker","OK/MarketSelectionPhotoLoader":"res/js/app/MarketSelectionPhotoLoader_30c51478","OK/CurrentUserCfg":"res/js/app/CurrentUserCfg_4dc1c5c","OK/MallDeliveryYandexSuggest":"res/js/app/MallDeliveryYandexSuggest_d43b4ac2","youtube":"https://www.youtube.com/iframe_api?noext","OK/OnlineIcon":"res/js/app/OnlineIcon_c8d6b892","OK/ProgressButton":"res/js/app/ProgressButton_99cff88b","OK/Timer":"res/js/app/Timer_66cc85e4","OK/SendActionTabs":"res/js/app/SendActionTabs_e10e3db8","OK/MallCheckout":"res/js/app/MallCheckout_6b329291","OK/BannerLogger":"res/js/app/BannerLogger_b62ec0a","OK/MediaTopicPlace":"res/js/app/MediaTopicPlace_576b6992","OK/OKVideo":"res/js/app/OKVideo_b46ff39","OK/PhotoCollageRunner":"res/js/app/PhotoCollageRunner_b1305aeb","OK/uploaderDialog":"res/js/app/uploaderDialog_93633cd7","OK/Calendar":"res/js/app/Calendar_fab14b49","b/feedback":"res/js/b/feedback_c27453d1","adman":"//ad.mail.ru/static/admanhtml/rbadman-html5.min","OK/GroupContentDeleteAuxActionsV2":"res/js/app/GroupContentDeleteAuxActionsV2_229dab0a","b/messages2notifier":"//st.mycdn.me/static/messages/1-5-16/messages/notifier","OK/VideoLiveChat":"res/js/app/VideoLiveChat_b2349990","OK/StickyBlock":"res/js/app/StickyBlock_855958e4","OK/MotivatorViralLayer":"res/js/app/MotivatorViralLayer_d463694d","OK/ToolbarProgressBar":"res/js/app/ToolbarProgressBar_aa36e300","OK/DispatcherJs":"res/js/app/DispatcherJs_c67c193f","b/music2":"res/js/b/music2_2c8a56ce","OK/FaqModern":"res/js/app/FaqModern_77247f3a","L10n/datepicker-hy":"res/js/L10n/datepicker-hy_f6bfad95","b/reactions":"res/js/b/reactions_56d810b","OK/GameCampaign":"res/js/app/GameCampaign_5b5d9e5d","OK/LogClicks":"res/js/app/LogClicks_3bc0dd2f","OK/PhotoEdit":"res/js/app/PhotoEdit_b588d01d","OK/ShortcutMenu":"res/js/app/ShortcutMenu_44e437d5","OK/DetectUsageGoogleTranslate":"res/js/app/DetectUsageGoogleTranslate_e701de77","OK/GroupPhotoPicker":"res/js/app/GroupPhotoPicker_5133a328","OK/VideoVitrina":"res/js/app/VideoVitrina_7e5d872d","b/charts":"res/js/b/charts_6baa3cc8","OK/PostingFormVideoUpload":"res/js/app/PostingFormVideoUpload_7e9e93f3","OK/capture":"res/js/app/capture_35dd3684","OK/InputRange":"res/js/app/InputRange_68fc8341","OK/ChallengeLayer":"res/js/app/ChallengeLayer_5fd6121d","OK/Gif":"res/js/app/Gif_d0202f7e","OK/ReplyList":"res/js/app/ReplyList_8169c37e","OK/dailyphoto-reactions":"res/js/app/dailyphoto-reactions_2af749ae","OK/VideoGroupUploader":"res/js/app/VideoGroupUploader_e7aaa680","OK/FriendProfileCover":"res/js/app/FriendProfileCover_82d0a7bb"},"bundles":{"b/photowall":["OK/photowall/SuperAnimation","OK/photowall/TimerCountdown","OK/photowall/VoteComponent","OK/photowall/PhotoWallProgress","OK/photowall/ResultsDrawer","OK/photowall/ResultsSaver","OK/photowall/ViewsSnitch","OK/photowall/VoteOverPhoto","OK/photowall/PushController","OK/photowall/Lottery"],"b/videostream":["OK/videostream/Streamer","OK/videostream/FlashStreamer","OK/videostream/WebRTCStreamer","OK/videostream/SoundController","OK/videostream/Layer"],"b/contentWidget":["OK/widget/shareContent/linkManager","OK/widget/shareContent"],"b/search":["OK/search/GlobalSearch","OK/search/PortalSearchFilters"],"b/postingTimerBundle":["OK/postingForm/postingTimer","OK/postingForm/postingTimer/postingTimerCalendar","OK/postingForm/postingTimer/postingTimerTimeLine"],"b/messages2":["OK/messages2/toolbar-button","OK/messages2/timing","OK/messages2/layer","OK/messages2/loader","OK/messages2/app","OK/messages2/history","OK/messages2/push"],"b/fancyGifts":["OK/fancyGifts/FancyGifts","OK/fancyGifts/FancyGiftsFormController"],"b/ddMenu":["OK/menu/dropdown/PositionManager","OK/menu/dropdown/triggerEventWorker/Click","OK/menu/dropdown/triggerEventWorker/MouseEnter","OK/menu/dropdown/DropDownTemplate","OK/menu/DropdownMenu","OK/menu/main/MoreBtn","OK/menu/NavMenu"],"b/nonBlockingTip":["OK/NonBlockingTip"],"b/feedback":["OK/feedback/FeedbackButton","OK/feedback/FeedbackDiscussion","OK/feedback/FeedbackItem","OK/feedback/FeedbackLayer","OK/feedback/FeedbackLayerController","OK/feedback/ListController","OK/feedback/Settings","OK/feedback/TotalLink","OK/feedback/FeedbackActions","OK/feedback/RestoreLink"],"b/primary":["OK/utils/utils","OK/utils/vanilla","OK/utils/throttle","OK/utils/debounce","OK/utils/requireBlock","OK/utils/dom","OK/utils/delegate","OK/cookie","OK/utils/environment","OK/LogClicks","OK/NewsFetchCoordinator","OK/HookModel","OK/CommentWidgets","OK/scrollToTop","OK/mrg/projects","OK/mrg/counters","OK/mrg/wamba","OK/banners/StickyBannerContainer","OK/banners/SmokescreenImgStyle","OK/banners/moneySave","OK/banners/BannerClickLog","mrg-smokescreen/Locator","mrg-smokescreen/StyleSheets","mrg-smokescreen/StyleSheets.Item","mrg-smokescreen/StyleSheets.NativeParses","mrg-smokescreen/StyleSheets.Parser","mrg-smokescreen/Welter","mrg-smokescreen/Utils","mrg-smokescreen/Cid","mrg-nano-xhr","mrg-smokescreen/Honeypot","OK/ToolbarBubble","OK/ToolbarGrowl","OK/css-loader","OK/Pushes"],"b/messages2helper":["OK/messages2/ads","OK/messages2/bind-events","OK/messages2/alert","OK/messages2/helper"],"b/discussions":["OK/Discussion","OK/DiscussionManager","OK/discussions/ScrollController","OK/discussions/Comment","OK/discussions/CommentEntry","OK/discussions/CommentsList","OK/discussions/CommentForm","OK/discussions/CommentFormAuthorMenu","OK/discussions/LinkAttachController","OK/discussions/TypingStatus","OK/utils/textchange","OK/discussions/Reveal","OK/discussions/Mentions"],"b/messages2notifier":["OK/messages2/push"],"b/multiSelect":["OK/multi-select/model/MultiSelectNode","OK/multi-select/model/MultiSelectTreeNode","OK/multi-select/model/MultiSelectVisibleNode","OK/multi-select/store/MultiSelectStore","OK/multi-select/store/MultiSelectTreeStore","OK/multi-select/transport/MultiSelectTransportAbstract","OK/multi-select/model/MultiSelectModel","OK/multi-select/transport/MultiSelectLocalTransport","OK/multi-select/transport/MultiSelectRemoteTransport","OK/multi-select/proxy/MultiSelectProxy","OK/multi-select/view/tag","OK/multi-select/view/listItem","OK/multi-select/view/treeListItem","OK/multi-select/view/hint/hints","OK/multi-select/MultiSelectSuggest","OK/multi-select/AbstractMultiSelect","OK/multi-select/MultiSelect"],"b/messagesButton":["OK/messages/BrowserNotifications","OK/messages/Helper","OK/messages/MessagesAlert","OK/messages/MessageDelivery","OK/messages/MessagesConfig","OK/messages/MessagesPushController","OK/messages/MessagesToggleButton","OK/messages/MessagesToolbarButton","OK/messages/UnsentMessages","OK/messages/WindowTitleChanger","OK/messages/WindowVisibility","OK/messages/SoundPlayer","OK/messages/Timing"],"b/adsManager":["OK/adsManager/t/filterWithCheckboxTree","OK/adsManager/CampaignActiveEditDialog","OK/adsManager/CampaignCreatedDialogCall","OK/adsManager/CampaignSettings","OK/adsManager/PaymentLayer","OK/adsManager/SberPaymentLayer","OK/adsManager/AdPaymentTypeForm","OK/adsManager/AdLegalPaymentForm","OK/adsManager/AdLegalPaymentInvoiceForm","OK/adsManager/SearchTopicDropdown","OK/adsManager/SelectedDropdown","OK/adsManager/SelectPublicationSource","OK/adsManager/multiSelect/CitiesMultiSelect","OK/adsManager/multiSelect/IncomesMultiSelect","OK/adsManager/multiSelect/InterestsMultiSelect","OK/adsManager/multiSelect/ContextPhrasesMultiSelect","OK/adsManager/Switch","OK/adsManager/BudgetTargetingSettings","OK/adsManager/RestartCampaign","OK/adsManager/scheduler/Scheduler","OK/adsManager/dateTime","OK/adsManager/superGeo/SuperGeo","OK/adsManager/apps/AppBlock","OK/adsManager/InputRangeMultiple","OK/adsManager/PromoCodeDialog","OK/adsManager/AdsProgress","OK/adsManager/AdsPhoneMask","OK/adsManager/FormattedInputRange"],"b/postingDecoration":["OK/postingForm/decoration/utils/ColorPickerUtils","OK/postingForm/decoration/model/bg/BgDecoratorSimple","OK/postingForm/decoration/model/bg/BgDecoratorLinearGradient","OK/postingForm/decoration/model/bg/BgDecoratorSimpleImage","OK/postingForm/decoration/model/bg/BgDecorator","OK/postingForm/decoration/model/bg/BgDecoratorCover","OK/postingForm/decoration/model/Decorator","OK/postingForm/decoration/model/DecoratorStorage","OK/postingForm/decoration/TextSizeControl","OK/postingForm/decoration/ColorPickerCatalog","OK/postingForm/decoration/ColorPickerList","OK/postingForm/decoration/ColorPicker","OK/postingForm/decoration/PollColorPicker"],"b/entitySuggest":["OK/entitySuggest/AbstractEntitySuggest","OK/entitySuggest/PYMKCard","OK/entitySuggest/PYMKRelationsCard","OK/entitySuggest/FriendshipCard","OK/entitySuggest/EntitySuggestSeenLogger","OK/entitySuggest/SetSuccessCardStatus"],"b/videochat":["OK/videochat/flash/VideoChat","OK/videochat/flash/FlashDriver","OK/videochat/flash/VideoChatIntegration","OK/videochat/transport/DirectTransport","OK/videochat/transport/ServerTransport","OK/videochat/transport/Transport","OK/videochat/EventEmitter","OK/videochat/Capturer","OK/videochat/Chat","OK/videochat/EmbedChat","OK/videochat/Conversation","OK/videochat/Enums","OK/videochat/Logger","OK/videochat/Tracer","OK/videochat/UIRemoteVideo","OK/videochat/UIStreaming","OK/videochat/VolumeDetector","OK/videochat/MediaSource","OK/videochat/Signaling","OK/videochat/UI","OK/videochat/CallerBlockConfirm","OK/videochat/Utils","OK/videochat/Debug"],"b/music2":["OK/music2/app","OK/music2/bind-events","OK/music2/layer","OK/music2/toolbar-button","OK/music2/play-button","OK/music2/push","OK/music2/preloader","OK/music2/theme","OK/music2/last-played-growl","OK/music2/growl-close"],"b/mall":["OK/mall/Reviews","OK/mall/ReviewForm","OK/mall/DropdownCloseHandler","OK/mall/PromoCodeBanner","OK/mall/MallAddressSelector"],"b/gifts":["OK/gifts/BookmarkToggleButton","OK/gifts/FixPriceTimerCountdown","OK/gifts/GiftBookmark","OK/gifts/GiftCardBookmark","OK/gifts/GiftDeletedLayer"],"b/reactions":["OK/reactions/Reaction","OK/reactions/ReactionOld","OK/reactions/ReactionAnimatable","OK/reactions/ReactionAnimationItem","OK/reactions/ReactionAnimationUtils","OK/reactions/ReactionController","OK/reactions/ReactionModel","OK/reactions/ReactionResourcesLoader","OK/reactions/ReactionPerformance","OK/reactions/ReactionLogger","OK/reactions/canvas/ReactionsCanvas","OK/reactions/canvas/ReactionsCanvasCss","OK/reactions/canvas/ReactionsCanvasHtml5","OK/reactions/canvas/ReactionsCanvasHtml5V2","OK/reactions/canvas/ReactionsCanvasWebGL","OK/reactions/ReactionCanvasFactory"],"b/suggestBundle":["OK/suggest/suggestImpl","OK/suggest/searchEngines","OK/suggest/renderers","OK/suggest/inputChecker"],"b/charts":["OK/chart/ChartLegend","OK/chart/Chart","OK/chart/LineChart"],"b/recovery":["OK/recovery/clearFormErrors"],"b/banners":["OK/banners/BannerController","OK/banners/BannerLoader","OK/banners/bannerNew/hooks/BaseBannerHookJs","OK/banners/bannerNew/hooks/AppsRecommendBannerHookJs","OK/banners/bannerNew/hooks/BannerAppsHookJs","OK/banners/bannerNew/hooks/BannerHookJs","OK/banners/bannerNew/hooks/ForthColumnBannerHookJs","OK/banners/bannerNew/hooks/ViewportHeightAwareBannersHookJs","OK/banners/bannerNew/hooks/BannerNavigationDataProviderHookJs","OK/banners/bannerNew/discussions/DiscussionsBannerJs"],"b/discussions-feed":["OK/discussions-feed/item","OK/discussions-feed/tutor","OK/discussions-feed/scroll-arrow"],"b/autophotopins":["OK/autophotopins/PhotoPins","OK/autophotopins/PhotoPins2","OK/autophotopins/PhotoFeed","OK/autophotopins/PhotoLayer","OK/autophotopins/PhotoPreview"],"b/shortcutMenuBundle":["OK/AbstractShortcutMenu","OK/ShortcutMenu"],"b/postingBundle":["OK/postingForm/clipboard","OK/postingForm/globalVariablesContainer","OK/postingForm/mediaCarousel","OK/postingForm/mediaCarouselCard","OK/postingForm/mediaCarouselStub","OK/postingForm/mediaGifts","OK/postingForm/mediaGiftsAddButton","OK/postingForm/mediaLinkLoader","OK/postingForm/mediaMusicAddButton","OK/postingForm/mediaMusicFacade","OK/postingForm/mediaMusic","OK/postingForm/mediaPhotosAddButton","OK/postingForm/mediaPhotos","OK/postingForm/mediaPoll","OK/postingForm/mediaStatic","OK/postingForm/mediaText","OK/postingForm/mediaVideoAddButton","OK/postingForm/postingCommon","OK/postingForm/postingModal","OK/postingForm/posting","OK/postingForm/postingSmiles","OK/postingForm/preview","OK/postingForm/templates","OK/postingForm/postingPhotoBattleMotivator","OK/postingForm/postingQuestionConstructorMotivator","OK/postingForm/motivatorUploadArea"],"b/p2p":["OK/p2p/dropdown","OK/p2p/formchange","OK/p2p/formchange","OK/p2p/transferDetail"],"b/videoEditor":["OK/videoEditor/VideoEditorEnums","OK/videoEditor/VideoEditorUtils","OK/videoEditor/VideoEditorObsSettings","OK/videoEditor/VideoEditorAnnotation","OK/videoEditor/VideoEditorAnnotationList","OK/videoEditor/VideoEditorTimelineController","OK/videoEditor/VideoEditorAddLink","OK/videoEditor/VideoEditorAddPoll","OK/videoEditor/VideoEditorAddText","OK/videoEditor/VideoEditorStreamInterrupt","OK/videoEditor/VideoEditorLive","OK/videoEditor/VideoEditorMain"],"b/groupDatePicker":["OK/groupDatePicker/model/GroupDatePickerMonthModel","OK/groupDatePicker/model/GroupDatePickerYearModel","OK/groupDatePicker/model/GroupDatePickerModel","OK/groupDatePicker/GroupDatePicker"],"b/registration":["OK/registration/Registration","OK/registration/Utils","OK/registration/enterCode","OK/registration/backhandler","OK/registration/vkconnect","OK/registration/enterPhoneNew","OK/registration/enterCodeNew","OK/registration/chooseUser","OK/registration/authorize","OK/registration/socialSignIn","OK/registration/socialAuthHandler","OK/registration/acceptPP","OK/registration/StatesManager","OK/registration/countryDropdown","OK/registration/translit","OK/registration/ChangedFieldValidator"],"b/messagesLayer":["OK/messages/Chatname","OK/messages/Chatname2","OK/messages/Column","OK/messages/ColumnManager","OK/messages/Conversation","OK/messages/ConversationHook","OK/messages/ConversationsList","OK/messages/ConversationsListItem","OK/messages/ConversationsManager","OK/messages/CreateConversationButton","OK/messages/HistoryHelper","OK/messages/HelloStickers","OK/messages/HelloStickersClose","OK/messages/ThanksPresentsClose","OK/messages/InfoPanel","OK/messages/InfoPanelState","OK/messages/InfoPanelClose","OK/messages/UserActionConfirm","OK/messages/LastMsgUpdater","OK/messages/MenuConfirm","OK/messages/MessageForm","OK/messages/MessagesLayer","OK/messages/MessagesList","OK/messages/ParticipantsAddMenu","OK/messages/ParticipantsListMenu","OK/messages/ChatPresets","OK/messages/promobubble","OK/messages/ReadMarks","OK/messages/RedLink","OK/messages/StickerSetPro","OK/messages/Search","OK/messages/SearchPanel","OK/messages/MessagesSettings","OK/messages/MessagesSettingsButton","OK/messages/TypingStatus","OK/messages/TypingUtil","OK/messages/AvatarCropForm","OK/audioPlayer","OK/messages/ScrollArrow","OK/messages/DateBar","OK/messages/MsgReplies","OK/messages/MessageAjaxController","OK/messages/CopyMsgText","OK/messages/ConvOnlineStatusTextUpdater"]},"waitSeconds":0,"shim":{"youtube":{"exports":"YT"},"jquery.ui.droppable":{"exports":"jQuery.fn.droppable","deps":["jquery.ui.mouse"]},"jquery.ui.sortable":{"exports":"jQuery.fn.sortable","deps":["jquery.ui.mouse"]},"swfobject":{"exports":"swfobject"},"candy":{"exports":"Candy"},"jquery.ui.mouse":{"exports":"jQuery.fn.mouse","deps":["jquery.ui.widget"]},"REACT/core":{"exports":"OK_REACT_core"},"jquery.ui.resizable":{"exports":"jQuery.fn.resizable","deps":["jquery.ui.mouse"]},"chromecast":{"exports":"navigator"},"mrg/ads":{"exports":"MRGtag"},"jquery.ui.widget":{"exports":"jQuery.widget","deps":["jquery.ui.core"]},"jquery.ui.datepicker":{"exports":"jQuery.fn.datepicker","deps":["jquery.ui.core"]},"jquery.ui.draggable":{"exports":"jQuery.fn.draggable","deps":["jquery.ui.mouse"]},"leaflet":{"exports":"L"},"REACT/vendors":{"exports":"OK_REACT_vendors"},"FileAPI":{"deps":["jquery","OK/logger"]},"jquery.ui.core":{"exports":"jQuery.ui","deps":["jquery"]}},"map":{"*":{"OK/dailyphoto-autoplay":"dailyphoto-autoplay","OK/adsManager/InputRange":"OK/InputRange","OK/MusicPicker":"music/picker","OK/messages2/app":"MSG/bootstrap","PTS":"noext!//ok.ru/web-api/pts","OK/alf":"OK/alf2","OK/messages2/toolbar-button":"MSG/bootstrap","OK/dailyphoto-archive":"dailyphoto-archive","OK/dailyphoto-model":"dailyphoto-model","OK/messages2/layer":"MSG/bootstrap","OK/MSG/bootstrap":"MSG/bootstrap","OK/dailyphoto-slider":"dailyphoto-slider","OK/dailyphoto-reactions":"dailyphoto-reactions","OK/adsManager/PromoCodeDialog":"OK/AmPromoCodeDialog"}},"config":{"OK/messages/MessagesToolbarButton":{"url":"wss://testproxy2.tamtam.chat/websocket"},"OK/messages/MessagesLayer":{"tns":"//www.tns-counter.ru/V13a****odnoklassniki_ru/ru/UTF-8/tmsec=odnoklassniki_site/"},"OK/music/collections":{"bubble":0},"OK/music/flash":{"limit":5000,"force":-1,"pts":1},"OK/cookieBanner":{"expireDate":"Tue, 19 Jan 2038 03:14:07 UTC"},"OK/music/upload":{"max":157286400,"host":"//musicupload.ok.ru"},"OK/music/wmf":{"host":"//wmf.ok.ru","hd":true},"okVideoPlayerUtils":{"noComscore":true},"FileAPI":{"imageOrientation":true,"staticPath":"//st.mycdn.me/static/fileapi/2-0-3n18/"}}}); require.config({"config":{"OK/react-loader":{"retryRequireLoad":3,"alwaysUndefOnError":true}}});require.config({"paths":{"OK/ProcessMoreInfo":"//st.mycdn.me/static/hf/2020-12-23more/ProcessMoreInfo"}});
requirejs.onError = function handleRequireError(eo) { 'use strict'; if (OK.fn.isDebug()) { console.error(eo); } /** * @param {Error} err */ function parse(err) { var /** @type {string} */ s = '\n', /** @type {RegExp} */ re = /(^|@)\S+\:\d+/, /* FIREFOX/SAFARI */ /** @type {RegExp} */ alt = /\s+at .*(\S+\:\d+|\(native\))/, /* CHROME/IE */ /** @type {string} */ res; if (err.stack.match(alt)) { /* Use alt */ re = alt; } res = err.stack .split(s) .filter(function (line) { return !!line.match(re); }) .join(s); return err + s + res; } var /** @type {Object} */ err = eo.originalError || eo, /** @type {Object} */ r = requirejs.s.contexts._, /** @type {string} */ clob = '', /** @type {string} */ info = '', /** @type {object} */ context = '', /** @type {string[]} */ deps = []; if (eo.requireMap) { context = r.registry[eo.requireMap.id]; deps = context.depMaps.map(function (item) { return item.id; }); info = (context.factory.name || 'anonymous') + ',[' + deps + ']'; /* Function code */ clob = 'Executing ' + context.factory + '\n'; } else { info = eo.requireType + ',[' + eo.requireModules + ']'; } if (err.stack) { clob += parse(err); } else { clob += err + '\n@' + info; } OK.logger.clob('rjs', clob, info, err.name); if (Array.isArray(eo.requireModules)) { eo.requireModules.forEach(function (path) { if (path.indexOf('/res/react') === 0) { sendReactError(path); } }); } function sendReactError(reactPath) { var clob = 'message=' + err.message + '\n' + 'requireType=' + eo.requireType + '\n' + 'requireModules=' + eo.requireModules.toString() + '\n' + 'stack=' + err.stack; var tagName = reactPath.split('.')[0].split('_')[1]; if (!tagName) { tagName = reactPath; } OK.logger.clob('react-error', clob, tagName, 'react-module-error'); } };
function scriptsReload() { var xhttp = new XMLHttpRequest(); xhttp.open("POST", "/gwtlog", true); xhttp.setRequestHeader("Content-Type", "application/x-www-form-urlencoded"); xhttp.send('a=' + JSON.stringify({ oldscripts: { reload:1 } })); xhttp.onload = function() { window.location.reload(); }; }

  try{
    (function (w, d, prefix) {
    w.RB = w.RB && w.RB.v && w.RB.v === 1 ? w.RB : (function () {
      var // main flag,
        enabled = !1,
        servingType = serveType(),
        useObserver = !!window.IntersectionObserver,
        useGeom = !useObserver && servingType !== "XD_FRAME",
        // old opera focus flag
        focused = !0,
        // counted flag
        counted = "mailru-visibility-counted",
        // banners to inspect
        banners = {},
        // shortcuts
        e = d.documentElement,
        VE = d.mozVisibilityState ? "mozvisibilitychange" : d.webkitVisibilityState ? "webkitvisibilitychange" : d.visibilityState ? "visibilitychange" : "",
        HP = "hidden" in d ? "hidden" : "webkitHidden" in d ? "webkitHidden" : "mozHidden" in d ? "mozHidden" : "",
        // lastTimeStamp = 0,

        // timing
        tm,
        // interstion observer instance
        observer;

      // handlers
      function onFocusIn() {
        focused = !0;
        C(!0);
      }

      function onFocusOut() {
        focused = !1;
      }

      function onUnload() {
        Clear();
        off();
      }

      // using visibility could have profits when tab is not

      function onVisibilityChange() {
        if (!d[HP]) onFocusIn();
        else onFocusOut();
      }

      function onWindowScroll() {
        C();
      }

      function onWindowResize() {
        C();
      }

      // I &ndash; inspect

      function I(bannerObject, id) {
        if (Object.prototype.toString.call(bannerObject) === "[object Array]") {
          Clear(bannerObject);
          var k = bannerObject.length - 1;
          for (; k >= 0; k--) {
            if (!s(bannerObject[k].el, counted)) {
              I(bannerObject[k]);
            }
          }
          return;
        }

        if (!useObserver && !useGeom) {
          tr(bannerObject.pixels_undetermined);
          bannerObject.el[counted] = true;
          return;
        }
        // bannerObject contains bannerObject.el and bannerObject.pixels
        if (!bannerObject.el.id) {
          id =
            prefix +
            new Date().getTime() +
            Math.round(Math.random() * 1e6);
          bannerObject.el.id = id;
        }

        id = bannerObject.el.id;

        // lastTimeStamp = new Date().getTime();
        // adding the banner container to storage
        if (!banners[id]) {
          banners[id] = {
            c: bannerObject.el,
            px: bannerObject.pixels,
            px_un: bannerObject.pixels_undetermined,
            px_nv: bannerObject.pixels_nonviewable,
            cb: bannerObject.callback,
            io: useObserver
          };
        }

        // enabling anyway
        on();
        if (useObserver) {
          o(bannerObject.el);
        }
        C(!0);
      }

      // C &ndash; check viewability of banner with t, timeout after loading

      function C(t) {
        for (var id in banners) {
          if (banners[id] && !G(id)) {
            CL(id);
          } else if (
            banners[id] &&
            getVA(banners[id].c) >= 50 &&
            hasFocus() &&
            !banners[id].t
          ) {
            (function (_id) {
              banners[_id].t = setTimeout(function () {
                try {
                  P(_id);
                } catch (e) {}
              }, 1E3);
            })(id);
          } else if (
            banners[id] &&
            getVA(banners[id].c) < 50
          ) {
            if (banners[id].t) {
              clearTimeout(banners[id].t);
              delete banners[id].t;
            }
          } else if (banners[id] && !hasFocus()) {
            if (banners[id].t) {
              clearTimeout(banners[id].t);
              delete banners[id].t;
              clearTimeout(tm);
              t = false;
            }
          } else if (!banners[id]) {
            CL(id);
          }
        }

        if (t) {
          clearTimeout(tm);
          tm = setTimeout(
            function () {
              C(!0);
            },
            useGeom ? 3e2 : 10e3
          );
        }
      }

      // CL &ndash; Clear timers and stop listeners

      function CL(id, onlyTM, noCount) {
        if (id && banners[id]) {
          clearTimeout(banners[id].t);
          banners[id].t = null;
          if (!onlyTM) {
            if (banners[id].io && observer) {
              observer.unobserve(banners[id].c);
            }

            if (!noCount && !s(banners[id].c, counted)) {
              tr(banners[id].px_nv);
              banners[id].c[counted] = true;
            }
            banners[id].c = null;
            delete banners[id];
          }
          return;
        }
        clearTimeout(tm);
        tm = null;
        for (var id in banners) {
          if (banners[id].t) {
            CL(id, !0);
          }
        }
      }

      function Clear(bannersArray) {
        if (bannersArray && bannersArray.length >= 0) {
          //clear banners from array
          var k = bannersArray.length - 1;
          var id;
          for (; k >= 0; k--) {
            id = bannersArray[k].el.id;
            if (id && banners[id]) {
              // clear but don't count nonviewable
              CL(id, !1, !0);
            }
          }
        } else {
          for (var id in banners) {
            //clear all
            CL(id);
          }
        }
      }

      // P &ndash; pixel to send
      function P(id, obj, cnt) {
        if (!G(id)) {
          CL(id);
          // banner removed
          return;
        }

        if (banners[id]) {
          obj = banners[id].c;
        } else {
          return;
        }

        if (!hasFocus()) {
          CL(id, !0);
          return;
        } else if (getVA(obj) < 50) {
          CL(id, !0);
          return;
        }

        for (cnt = banners[id].px.length - 1; cnt >= 0; cnt--) {
          new Image().src = banners[id].px[cnt];
        }
        // set counted flag - skip in next collect loops
        obj[counted] = true;
        //try fire callback
        var cb = banners[id].cb;
        if (cb && typeof cb === "function") {
          try {
            cb();
          } catch (e) {}
        }
        // remove banner from storage of inspectable items
        CL(id);
        // turn listeners off if banners are not present
        if (!l(banners)) off();
      }

      function hasFocus() {
        if (HP) focused = !d[HP];
        else if (!VE && typeof d.hasFocus === "function")
          focused = d.hasFocus();
        return focused;
      }

      function getVA(obj, source) {
        if (obj.id && banners[obj.id] && banners[obj.id].io) {
          return banners[obj.id].v || 0;
        }

        var percent = getGeometryViewableArea(obj).percent;

        return percent;
      }

      /** LISTENERS SWITCHERS **/
      function on() {
        if (enabled) return;
        if (useGeom) {
          ev(w, "resize", onWindowResize);
          ev(w, "scroll", onWindowScroll);
        }
        if (useObserver) {
          observer = new IntersectionObserver(h, {
            threshold: [0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
          });
        }
        if (VE) ev(d, VE, onVisibilityChange);
        else {
          ev(w, "blur", onFocusOut);
          ev(w, "focus", onFocusIn);
        }
        ev(w, "unload", onUnload);
        enabled = true;
      }

      function off() {
        rm(w, "unload", onUnload);
        rm(w, "resize", onWindowResize);
        rm(w, "scroll", onWindowScroll);
        if (VE) rm(d, VE, onVisibilityChange);
        rm(w, "focus", onFocusIn);
        rm(w, "blur", onFocusOut);
        if (observer) {
          observer.disconnect();
          observer = null;
        }
        clearTimeout(tm);
        enabled = false;
      }

      /** INTERSECTION OBSERVER UTILS **/
      function o(e) {
        observer && observer.observe(e);
      }

      function h(changes) {
        changes.forEach(function (changeRecord) {
          var element = changeRecord.target;
          var id = element.id;

          if (id && banners[id]) {
            banners[id].v = Math.round(
              changeRecord.intersectionRatio * 100
            );
          }
        });
        C();
      }

      /** UTILS **/
      // G - get element by ID;
      function G(E) {
        return d.getElementById(E);
      }
      // ev - EVent to handle
      function ev(elem, eventName, callback) {
        elem.addEventListener
          ? elem.addEventListener(eventName, callback, !1)
          : elem.attachEvent &&
            elem.attachEvent("on" + eventName, callback);
      }

      function rm(elem, eventName, callback) {
        elem.removeEventListener
          ? elem.removeEventListener(eventName, callback, !1)
          : elem.detachEvent &&
            elem.detachEvent("on" + eventName, callback);
      }
      // obj length
      function l(obj) {
        var s = 0,
          key;
        for (key in obj) {
          if (obj.hasOwnProperty(key)) s++;
        }
        return s;
      }
      //elem state
      function s(elem, state) {
        return !(typeof elem[state] == undefined || elem[state] !== true);
      }
      //track
      function tr(pixels) {
        if (pixels && pixels.length) {
          for (cnt = pixels.length - 1; cnt >= 0; cnt--) {
            new Image().src = pixels[cnt];
          }
        }
      }
      function serveType() {
        try {
          if (window === window.top) {
            return "ON_PAGE";
          }

          var currentWindow = window;

          while (currentWindow !== currentWindow.parent) {
            if (
              currentWindow.document.domain !==
              currentWindow.parent.document.domain
            ) {
              return "XD_FRAME";
            }
            currentWindow = currentWindow.parent;
          }

          return "S_FRAME";
        } catch (e) {}

        return "XD_FRAME";
      }

      // geometry viewability
      function getGeometryViewableArea(element, contextWindow) {
        try {
          var rect = element.getBoundingClientRect();
          var area = getArea(rect);
          var currentWindow = window;

          contextWindow = contextWindow || window.top;

          while (currentWindow !== contextWindow) {
            // 1) get current frame coordinates inside its parent
            // 2) get element coordinates relative to parent
            // 3) get visible element coordinates relative to parent
            var currentRect = currentWindow.frameElement.getBoundingClientRect();

            rect = getRR(rect, currentRect);
            rect.left = Math.max(currentRect.left, rect.left);
            rect.right = Math.min(currentRect.right, rect.right);
            rect.top = Math.max(currentRect.top, rect.top);
            rect.bottom = Math.min(currentRect.bottom, rect.bottom);

            if (rect.right < rect.left) {
              rect.right = rect.left;
            }
            if (rect.bottom < rect.top) {
              rect.bottom = rect.top;
            }

            currentWindow = currentWindow.parent;
          }
          rect = getRVA(rect, contextWindow);

          var viewableArea = getArea(rect);

          rect.percent = (viewableArea / area) * 100;

          return rect;
        } catch (e) {
          return { left: 0, right: 0, top: 0, bottom: 0, percent: 0 };
        }
      }

      function getArea(rect) {
        return (rect.right - rect.left) * (rect.bottom - rect.top);
      }
      // relative rect
      function getRR(rect, contextRect) {
        return {
          left: rect.left + contextRect.left,
          right: rect.right + contextRect.left,
          top: rect.top + contextRect.top,
          bottom: rect.bottom + contextRect.top,
        };
      }
      // relative viewable area
      function getRVA(rect, contextWindow) {
        var result = {};
        var contextSize = getVS(contextWindow);

        result.left = Math.max(0, rect.left);
        result.right = Math.min(contextSize.width, rect.right);
        result.top = Math.max(0, rect.top);
        result.bottom = Math.min(contextSize.height, rect.bottom);

        return result;
      }
      // viewport size
      function getVS(w) {
        var viewPortSize = {
          width: Infinity,
          height: Infinity,
        };
        var d = w.document;

        if (!isNaN(d.body.clientWidth) && d.body.clientWidth > 0) {
          viewPortSize.width = d.body.clientWidth;
        }
        if (!isNaN(d.body.clientHeight) && d.body.clientHeight > 0) {
          viewPortSize.height = d.body.clientHeight;
        }
        if (
          !!d.documentElement &&
          !!d.documentElement.clientWidth &&
          !isNaN(d.documentElement.clientWidth)
        ) {
          viewPortSize.width = d.documentElement.clientWidth;
        }
        if (
          !!d.documentElement &&
          !!d.documentElement.clientHeight &&
          !isNaN(d.documentElement.clientHeight)
        ) {
          viewPortSize.height = d.documentElement.clientHeight;
        }
        if (!!w.innerWidth && !isNaN(w.innerWidth)) {
          viewPortSize.width = Math.min(viewPortSize.width, w.innerWidth);
        }
        if (!!w.innerHeight && !isNaN(w.innerHeight)) {
          viewPortSize.height = Math.min(
            viewPortSize.height,
            w.innerHeight
          );
        }

        return viewPortSize;
      }

      /** PUBLIC INTERFACE **/

      return {
        I: I,
        // debug
        // , banners: banners
        v: 1,
      };
    })();
  })(window, document, 'mailru')
  }catch (e) {}


  (function(prefix){
    try{
      
      function getAdsContainers() {
  			var ADS_CLASS = prefix + '-visibility-check',
  				ADS_COUNTER_CLASS = ADS_CLASS + '-counter',
  				ADS_CALLBACK_CLASS = ADS_CLASS + '-callback',
  				COUNTER_ATTR = 'data-counter',
  				COUNTER_ATTR_UNDETERMINED = COUNTER_ATTR + '-un',
  				COUNTER_ATTR_NONVIEWABLE = COUNTER_ATTR + '-nv',
  				CALLBACK_ATTR = 'data-callback',
  				OBSERVER_ATTR = 'data-observer',
  				containers = [],
  				countables = [],
  				i, k, counters, _counter, _observer;
   
  			containers = getByClass(document, ADS_CLASS);
  			for (i = containers.length - 1; i >= 0; i--) {
  				var counters = getByClass(containers[i], ADS_COUNTER_CLASS, 'span');
  				_counter = containers[i].getAttribute(COUNTER_ATTR);
  				_observer = containers[i].hasAttribute(OBSERVER_ATTR);
  				countables[i] = {
  					el: containers[i],
  					pixels: [],
  					pixels_undetermined: [],
  					pixels_nonviewable: [],
  					observer: _observer
  				};
  				if (_counter) countables[i].pixels.push(_counter);
  				for (k = counters.length - 1; k >= 0; k--) {
  					if (counters[k].parentNode === countables[i].el) {
              _counter = counters[k].getAttribute(COUNTER_ATTR);
              if (_counter) {
                countables[i].pixels.push(_counter);
              }
              _counter = counters[k].getAttribute(COUNTER_ATTR_UNDETERMINED);
              if (_counter) {
                countables[i].pixels_undetermined.push(_counter);
              }
              _counter = counters[k].getAttribute(COUNTER_ATTR_NONVIEWABLE);
              if (_counter) {
                countables[i].pixels_nonviewable.push(_counter);
              }
            }
  				}
  				var callback = getByClass(containers[i], ADS_CALLBACK_CLASS, 'span');
  				if (callback[0]) {
  				  var _callback = callback[0].getAttribute(CALLBACK_ATTR);
  				  if (_callback && window.RB_CALLBACKS && window.RB_CALLBACKS[_callback]) {
  				    countables[i].callback = window.RB_CALLBACKS[_callback];
  				  }
  				}
  				if (!countables[i].pixels.length) countables.splice(i, 1);
  			}
   
  			return countables;
  		}
   
  		function getByClass(parent, childClassName, tagName) {
  			if (parent.getElementsByClassName) {
  				return parent.getElementsByClassName(childClassName);
  			} else if (parent.querySelectorAll) {
   
  				return parent.querySelectorAll('.' + childClassName);
  			} else {
  				var els = [];
  				var tmp = parent.getElementsByTagName(tagName ? tagName : "*");
  				var regex = new RegExp("(^|\s)" + childClassName + "(\s|$)");
  				for (var i = 0; i < tmp.length; i++) {
  					if (regex.test(tmp[i].className)) {
  						els.push(tmp[i]);
  					}
  				}
  				return els;
  			}
  		}
   
  		RB.I(getAdsContainers());
      
    }catch(e){}
  }('mailru'))

OK.scrollBar();
function refresh() { var img = document.getElementById("captcha"); img.src = img.src+'&'+(new Date().getTime()); document.getElementById('field_ccode').focus(); }
OK.afterWindowOnloadAttach(function(){(function (w, d) {
     var ref = '=',
            enc = encodeURIComponent;
        w.OK = w.OK || {};
        if (!w.OK.dref_li) {
            ref = enc(d.referrer);
            w.OK.dref_li = true;
        }
        new Image().src = '//counter.yadro.ru/hit?r' + ref + ((typeof (screen) == 'undefined') ? '' : ';s' + screen.width + '*' + screen.height + '*' + (screen.colorDepth ? screen.colorDepth : screen.pixelDepth)) + ';u' + enc(document.URL) + ';' + Math.random();
}(window, document));});
(function(){document.cookie="viewport="+window.screen.availHeight+";path=/";})();
(function(w){w.OK && w.OK.util && w.OK.util.setHighDensityCookie('_hd');})(window);
OK.photoLayer.close();
OK.loader.use(['jQuery', 'OKCustomJs'], function () { OK.Layers.setMaxSize(2); });
OK.loader.use(["OKCustomJs"], function() {OK.Layers.remove("video_player");});
OK.loader.execRequire('OK/MediaLayer', function(mtLayer) { mtLayer.closeLayer(); });
require(['OK/capture'],function(c){c.activateDocument(['PopLayerPhoto','PopLayerHelpFeedback','VideoSearchBlock:AjaxLinkHook'],null)});
(function(w){w.caches && w.caches.delete('okMessenger')})(window)
var supported = typeof performance.setResourceTimingBufferSize == "function";
if (supported) {
  performance.setResourceTimingBufferSize(500);
}

/* Metelev */
// fix payment window
window.addEventListener("message", function (e) {
var paymentWrapper = document.getElementById('pmntWzrdCtr');
if (paymentWrapper) {
 paymentWrapper.style.width="99%";
}
}, false);

/* Sevastyanov: fix of banner visibility */
(function() {
    var THRESHOLD = 1000 * 40;
    var userActive = Date.now();
    function userAction() {
        userActive = Date.now();
    }
    document.scrollingElement.addEventListener('scroll', userAction);
    document.body.addEventListener('mousemove', userAction);
    function isUserActive() {
        return (Date.now() - userActive) < THRESHOLD;
    }
    window.__bannerCheckViewportFix = function (el, checkLayers, threshold) {
        if (document.visibilityState === 'hidden') {
            return false;
        }
        if (checkLayers && window.OK.Layers.isAnyLayerOpened()) {
            return false;
        }
        if ((Date.now() - userActive) > THRESHOLD) {
            return false;
        }
        var screenTop = window.pageYOffset;
        var screenHeight = window.innerHeight;
        var rect = el.getBoundingClientRect();
        var elPart = rect.height * threshold;
        var elTop = rect.top + screenTop;
        var elBottom = rect.bottom + screenTop;
        if (screenHeight < elPart) {
            return false;
        }
        var lowerBound = screenTop;
        var upperBound = screenHeight + screenTop;
        return ((elTop + elPart) < upperBound && elTop > lowerBound) ||
            ((elBottom - elPart) > lowerBound && elBottom < upperBound) ||
            (elTop < lowerBound && elBottom > upperBound);
    };
})();
/* /Sevastyanov: fix of banner visibility */