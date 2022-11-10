var TRACKING_PK = 'people'; //浜у搧鍞竴鏍囪瘑锛堝叆椹诲悗骞冲彴鎻愪緵锛�
var TRACKING_UK = 'people_home';    //绔欎笟鍔★紙鑷畾涔変笟鍔℃爣璇嗭級
var TRACKING_APP_VERSION = 'V1.0.0';    //褰撳墠搴旂敤鐗堟湰鍙�
var TRACKING_CLICK_HEAT_PC_EID = 'clickheat';    //PC鐐瑰嚮鐑姏鍥撅紙鍏ラ┗鍚庡钩鍙版彁渚涳級
var TRACKING_CH_PC_JQSELECTER = '.layout'; 

// 椤甸潰鏇濆厜渚� 璇︽儏椤佃嚜鍔ㄥ姞杞�
$(document).ready(function (){
  //鑾峰彇鍩熷悕
  // host = window.location.host;
  // var indx=host.indexOf(".people.");
  // if(indx>=0){
  //  TRACKING_UK="people_"+host.substring(0,indx);
  // }
  var originalId = getCookieId();
  var userId = getSysUserId();
  var page_category=2;
  var content_id = getMetaContentByName('contentid');
  if(content_id==null || content_id<=0){
   page_category=1;
  }
  var node_id = getMetaContentByName('catalogs');
  if(content_id==null&&node_id!=null){
   content_id=node_id;
  }
  //console.log(TRACKING_UK);
        // 璋冪敤js-sdk
        view_tracking(TRACKING_PK, TRACKING_UK, originalId, userId, content_id, TRACKING_APP_VERSION, page_category);
        return
});
/**
 * 鑾峰彇鐢ㄦ埛sessionId 渚�
*/
function getCookieId(){
    var strcookie = document.cookie;//鑾峰彇cookie瀛楃涓�
    var arrcookie = strcookie.split("; ");//鍒嗗壊
    //閬嶅巻鍖归厤
    for ( var i = 0; i < arrcookie.length; i++) {
        var arr = arrcookie[i].split("=");
        if (arr[0] == 'wdcid'){
            return arr[1];
        }
    }
    return "";
}
/**
 * 鑾峰彇绯荤粺鐢ㄦ埛ID  渚�
 */
function getSysUserId(){
    // 鍚勭郴缁熻嚜琛屽皝瑁�
    return "sysuserid";
}
function getMetaContentByName(name,content1){
 var content = (content1==null)?'content':content1;
 try{
  var result = document.querySelector("meta[name='"+name+"']").getAttribute(content);
 }catch(err){
  return null;
    }
 return result;
}
/**
 * 鑾峰彇褰撳墠浜嬩欢瀵硅薄ID  渚�
 */
function getContentId(){
    // 鑾峰彇褰撳墠浜嬩欢瀵硅薄ID, url = http://xxxx.com.cn/xxxx/xxx?xxx=8415450
    var url = window.location.href;
    var content_id ="";

    if(url.lastIndexOf('=')>-1) {
        content_id = url.substring(url.lastIndexOf('=')+1);
    }

    return content_id;
}
function getMetaContentByName(name,content1){
 var content = (content1==null)?'content':content1;
 try{
  var result = document.querySelector("meta[name='"+name+"']").getAttribute(content);
 }catch(err){
  return null;
    }
 return result;
}