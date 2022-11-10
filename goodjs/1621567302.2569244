var CstHistoryCookieDomain  = "history.kakaku.com";
var CstKeepDomain  = "kakaku.com";
var TargetProtocol = document.location.protocol;

//**********************************************************************
// ShowHistory()
// 履歴枠表示
//**********************************************************************
function ShowHistory(type)
{
 if (document.getElementById("ShowHistoryBox")) {
  document.getElementById("ShowHistoryBox").innerHTML = '<iframe src="https://' + CstHistoryCookieDomain + '/history/parts.aspx?type=' + encodeURIComponent(type) + '" frameborder="0" noresize="noresize" scrolling="no" width="720" height="230"></iframe>';
 }
}

// 履歴枠表示(カテトップ用)
function ShowHistoryCategoryTop(type, categoryName) {
 if (document.getElementById("ShowHistoryBox")) {
  document.getElementById("ShowHistoryBox").innerHTML = '<iframe src="https://' + CstHistoryCookieDomain + '/history/parts.aspx?type=' + encodeURIComponent(type) + '&category=' + encodeURIComponent(categoryName) + '&version=v2" name="cth" frameborder="0" noresize="noresize" scrolling="no" width="720" height="285"></iframe>';
 }
}

// 履歴枠表示(プライスメニュー用)
function ShowHistoryPriceMenu(type, categoryCD) {
 if (document.getElementById("ShowHistoryBox")) {
  document.getElementById("ShowHistoryBox").innerHTML = '<iframe src="https://' + CstHistoryCookieDomain + '/history/parts.aspx?type=' + encodeURIComponent(type) + '&categorycd=' + encodeURIComponent(categoryCD) + '&version=v2" name="pmh" frameborder="0" noresize="noresize" scrolling="no" width="720" height="295"></iframe>';
 }
}

// 履歴枠表示(カテトップ用)
function ShowHistoryCategoryTopV3(type, categoryName) {
 if (document.getElementById("ShowHistoryBox")) {
  document.getElementById("ShowHistoryBox").innerHTML = '<iframe src="https://' + CstHistoryCookieDomain + '/history/parts.aspx?type=' + encodeURIComponent(type) + '&category=' + encodeURIComponent(categoryName) + '&version=v3" name="cth" frameborder="0" noresize="noresize" scrolling="no" width="780" height="265"></iframe>';
 }
}

//**********************************************************************
// ShowShortcut()
// ショートカット枠表示
//**********************************************************************
// ショートカット枠表示(価格トップ用)
function ShowShortcut(type) {
 hideHistoryContainer();
 if (document.getElementById("ShowShortcutBox")) {
  document.getElementById("ShowShortcutBox").innerHTML = '<div id="historyFrame" class="hf_v2" style="width: 88px; padding:0 4px; margin: 0px; position: relative; background: url(\'https://img1.kakaku.k-img.com/images/history/bg_historyframe_v2.png\') no-repeat scroll 0px 0px transparent;"><iframe  id="f_keep" src="'+ TargetProtocol + '//' + CstKeepDomain +'/keep/shortcutparts.aspx" frameborder="0" noresize="noresize" allowtransparency="true" scrolling="no" width="96" height="49" allowtransparency="true"></iframe><iframe id="f_history" src="https://' + CstHistoryCookieDomain + '/history/shortcutpartsforkeep.aspx?type=' + encodeURIComponent(type) + '" frameborder="0" noresize="noresize" scrolling="no" width="96" allowtransparency="true"></iframe></div>';
 }
}

// ショートカット枠表示(カテトップ用)
function ShowShortcutCategoryTop(type, categoryName) {
 hideHistoryContainer();
 if (document.getElementById("ShowShortcutBox")) {
  document.getElementById("ShowShortcutBox").innerHTML = '<div id="historyFrame" class="hf_v2" style="width: 88px; padding:0 4px; margin: 0px; position: relative; background: url(\'https://img1.kakaku.k-img.com/images/history/bg_historyframe_v2.png\') no-repeat scroll 0px 0px transparent;"><iframe  id="f_keep" src="'+ TargetProtocol + '//' + CstKeepDomain +'/keep/shortcutparts.aspx" frameborder="0" noresize="noresize" allowtransparency="true" scrolling="no" width="96" height="49" allowtransparency="true"></iframe><iframe id="f_history" src="https://' + CstHistoryCookieDomain + '/history/shortcutpartsforkeep.aspx?type=' + encodeURIComponent(type) + '&category=' + encodeURIComponent(categoryName) + '" name="cts" frameborder="0" noresize="noresize" scrolling="no" width="96" allowtransparency="true"></iframe></div>';
 }
}

// ショートカット枠表示(プライスメニュー用)
function ShowShortcutPriceMenu(type, categoryCD) {
 hideHistoryContainer();
 if (document.getElementById("ShowShortcutBox")) {
  document.getElementById("ShowShortcutBox").innerHTML = '<div id="historyFrame" class="hf_v2" style="width: 88px; padding:0 4px; margin: 0px; position: relative; background: url(\'https://img1.kakaku.k-img.com/images/history/bg_historyframe_v2.png\') no-repeat scroll 0px 0px transparent;"><iframe  id="f_keep" src="'+ TargetProtocol + '//' + CstKeepDomain +'/keep/shortcutparts.aspx?categorycd=' + encodeURIComponent(categoryCD) + '" frameborder="0" noresize="noresize" allowtransparency="true" scrolling="no" width="96" height="49" allowtransparency="true"></iframe><iframe id="f_history" src="https://' + CstHistoryCookieDomain + '/history/shortcutpartsforkeep.aspx?type=' + encodeURIComponent(type) + '&categorycd=' + encodeURIComponent(categoryCD) + '" name="pms" frameborder="0" noresize="noresize" scrolling="no" width="96" allowtransparency="true"></iframe></div>';
 }
}

function hideHistoryContainer() {
 if (document.getElementById("historyContainer")) {
  document.getElementById("historyContainer").style.display = 'none';
 }
}