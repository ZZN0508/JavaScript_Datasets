var rootSysName = "jsp";
//鎵╁睍瀛楃涓茬殑endwith鏂规硶
String.prototype.endWith=function(oString)
{  
 var   reg=new   RegExp(oString+"$");  
 return   reg.test(this);  
}
String.prototype.ReplaceAll = function(AFindText,ARepText)
{
 var raRegExp = new RegExp(AFindText,"g")
 try{
 var res = this.replace(raRegExp,ARepText);
 return res;
 }catch(e){return "";}
}
//XML瑙ｆ瀽鍑芥暟锛屽res涓殑XML瀛楃涓茶繘琛岃В鏋�
function xmljx(res)
{
 var xmlDoc = null;
 try{
  xmlDoc = new ActiveXObject("Microsoft.XMLDOM"); 
  xmlDoc.async = "false";
  xmlDoc.loadXML(res);
 }catch(e){
  var parser = new DOMParser();
  xmlDoc = parser.parseFromString(res,"text/xml");
 }
 
 return xmlDoc;
}
function setHTMLValue(id,type,value)
{
 try{
  if(type == "value")
   document.getElementById(id).value = value;
  else if(type == "innerHTML")
   document.getElementById(id).innerHTML = value;
  else
  {
   var excuteStr = "document.getElementById('"+id+"')."+type+"='"+value+"'";
   eval(excuteStr);
  }
 }catch(e){}
}
function getHTMLValue(id,type)
{
 var value = "";
 if(type == "value")
  value = document.getElementById(id).value;
 else if(type == "innerHTML")
  value = document.getElementById(id).innerHTML;
 else
 {
  var excuteStr = "document.getElementById('"+id+"')."+type;
  value = eval(excuteStr);
 }
 if(typeof(value) == "undefined")
  return "";
 else
  return value;
}
function $value(fieldName,webType)
{
 var value = "";
 try{
  if(webType == "澶氶€夋寜閽�")
  {
   value = ";";
   var elements = document.getElementsByName(fieldName);
   for(var i=0;i<elements.length;i++)
   {
    if(elements[i].checked)
     value += elements[i].value+";";
   }
   if(value == ";")
    value = "";
  }
  else if( webType == "鍗曢€夋寜閽�")
  {
   var elements = document.getElementsByName(fieldName);
   for(var i=0;i<elements.length;i++)
   {
    if(elements[i].checked)
    {
     value += elements[i].value;
     break;
    }
   }
  }
  else if(webType == "缂栬緫鍣�" )
  {
   var editorFrame = window.frames[fieldName];
   var editorValue = editorFrame.getHtmlContent();
   if(editorValue)
    editorValue = editorValue.ReplaceAll("&nbsp;","OA_YHNBSP");
   return editorValue;
  }
  else
   value = document.getElementById(fieldName).value;
  //濡傛灉value涓洪潪娉曟暟鍊硷紝鍒欒礋鍊间负绌�
  if(!value)
   value = "";
 }catch(e){value = "";}
 return value;
}
function $setvalue(fieldName,webType,fieldValue)
{
 try{
  if(webType == "鍗曢€夋寜閽�")
  {
   var RadioGroup = document.getElementsByName(fieldName);
   for(var i=0;i<RadioGroup.length;i++)
   {
    if (RadioGroup[i].value == fieldValue)
    {
     RadioGroup[i].checked = true;
     return;
    }
   }
  }
  else if(webType == "澶氶€夋寜閽�")
  {
   var CheckedGroup = document.getElementsByName(fieldName);
   for(var i=0;i<CheckedGroup.length;i++)
   {
    if (fieldValue.indexOf(";"+CheckedGroup[i].value+";") != -1)
     CheckedGroup[i].checked = true;
   }
  }
  else if(webType == "涓嬫媺妗�")
  {
   var currOptions = document.getElementById(fieldName);
   for(var i=0;i<currOptions.length;i++)
   {
    if(currOptions[i].value == fieldValue)
    {
     currOptions[i].selected = true;
     return;
    }
   }
   //濡傛灉娌℃湁鐨勮瘽锛屽垯鍦⊿elected鐨勬渶鍚庢坊鍔犱笂涓€椤癸紝骞朵笖閫変腑
   var newOption = document.createElement("option");
   newOption.text = fieldValue;
   newOption.value = fieldValue;
   currOptions.add(newOption);
   newOption.selected = true;
  }
  else if(webType == "缂栬緫鍣�" )
  {
   setHTMLValue(fieldName+"HTMLDIV","innerHTML",fieldValue);
  }
  else
   setHTMLValue(fieldName,"value",fieldValue);
 }catch(e){}
}
function addWhere(where,str)
{
 if(where == "")
  return str;
 else
  return where+" "+str;
}
function addDBWhere(where,str)
{
 if(!where)
 {
  if(!str)
   return "";
  else
   return str;
 }
 else
 {
  if(!str)
   return where;
  else
   return "("+where+") and ("+str+")";
 }
}
function createXMLNode(key,value)
{
 var sResult = "";
 sResult += "<"+key+">";
 sResult += "<![CDATA["+value+"]]>";
 sResult += "</"+key+">";
 return sResult;
}
//娓呴櫎鏌愪竴涓粍浠剁殑鎵€鏈夊瓙缁勪欢
function clear(ele)
{
 var index = ele.childNodes.length;
 for(var i=index-1;i>=0;i--)
  ele.removeChild(ele.childNodes[i]);
}
//寰楀埌鏌愪竴涓璞＄殑鍊�
function $F(id)
{
 var ele = document.getElementById(id);
 if(ele)
  return ele.value;
 else
  return "";

}
//閫変腑鏌愪竴涓€�
function setRadioValue(id,value)
{
 var elements = document.getElementsByName(id);
 for(var i=0;i<elements.length;i++)
 {
  if(elements[i].value == value)
  {
   elements[i].checked = true;
   return;
  }
 }
}
//寰楀埌鐖剁獥鍙ｇ殑淇℃伅
function getOpener()
{
 if(window.opener)
  return window.opener;
 else
  return window.dialogArguments;
}
//鍘绘帀瀛楃涓插乏杈圭殑绌烘牸
function Ltrim(str)
{
   return str.replace(/ +/,"")
}

//鍘绘帀瀛楃涓插彸杈圭殑绌烘牸
function Rtrim(str)
{
   return str.replace(/ +$/,"")
}
//trim鍑芥暟
function trim(str) 
{
 if (!str || str=="") 
  return "";
 while ((str.charAt(0)==' ') || (str.charAt(0)=='\n') || (str.charAt(0,1)=='\r')) 
  str=str.substring(1,str.length);
 while ((str.charAt(str.length-1)==' ') || (str.charAt(str.length-1)=='\n') || (str.charAt(str.length-1)=='\r')) 
  str=str.substring(0,str.length-1);
 return str;
}

//19. 鐢ㄦ埛ID锛屽彲浠ヤ负鏁板瓧銆佸瓧姣嶃€佷笅鍒掔嚎鐨勭粍鍚堬紝 绗竴涓瓧绗︿笉鑳戒负鏁板瓧,涓旀€婚暱搴︿笉鑳借秴杩�20
function f_check_userID(obj,startLength,endLength)
{
 var userID = obj.value;
 if(userID.length < startLength || userID.length > endLength)
 {
  return "闀垮害蹇呴』鍦╗"+startLength+","+endLength+"]涔嬮棿";
 }

 if(!isNaN(userID.charAt(0)))
 {
  return "ID绗竴涓瓧绗︿笉鑳戒负鏁板瓧";
 }
 if(!/^\w{1,20}$/.test(userID))
 {
  return "ID鍙兘鐢辨暟瀛椼€佸瓧姣嶃€佷笅鍒掔嚎缁勫悎鑰屾垚";
 }
 return "OK";
}
//妫€鏌ュ瓧绗︿覆鏄惁涓烘眽瀛楋紝闀垮害鏄惁鍦ㄨ瀹氱殑闀垮害涔嬮棿
function f_check_china(obj,startLength,endLength)
{
 if (/^[\u4e00-\u9fa5]+$/.test(obj.value))
 {
  if(obj.value.length >= startLength && obj.value.length<= endLength)
   return "OK";
  else
  {
   return "闀垮害蹇呴』鍦╗"+startLength+","+endLength+"]涔嬮棿";
  }
 }
 else
 {
  return "璇疯緭鍏ユ眽瀛�";
 }
}
//鍒ゆ柇瀛楃涓茬殑闀垮害鏄惁鍦ㄦ煇涓€涓寖鍥村唴
function f_check_length(obj,startLength,endLength)
{
 if(obj.value.length >= startLength && obj.value.length<= endLength)
  return "OK";
 else
 {
  return "闀垮害蹇呴』鍦╗"+startLength+","+endLength+"]涔嬮棿";
 }
}
//瀵规暣褰㈡暟鎹繘琛屽垎鏋�
function f_check_integer(value)
{
 if (/^(\+|-)?\d+$/.test(value))
 {
    return true;
 }
 else
 {
  return false;
 }
}
//鍒ゆ柇鏄惁涓哄疄鏁�
function f_check_float(objvalue)
{
 if (/^(\+|-)?\d+($|\.\d+$)/.test(objvalue))
 {
    return true;
 }
 else
 {
    return false;
 }
}
//寰楀埌涓€涓棩鏈燂紝鏍煎紡涓� yyyy-MM-dd
function getDateTime()
{
 var date = new Date();
 var year = date.getFullYear();
 var month = date.getMonth();
 var day = date.getDate();
 month = (month < 10)?"0"+month:month;
 day = (day < 10)?"0"+day:day;
 return year+"-"+month+"-"+day;
}
// ================================================================
// 鏈嚱鏁扮敤浜庤嚜鍔ㄥ皢杈撳叆鏂囨湰妗嗕腑鐨勫唴瀹硅浆鎹㈡垚澶у啓瀛楃 
// ================================================================ 
function JHshToUpperCase(obj) 
{
 obj.value = obj.value.toUpperCase();
} 
//灏嗘煇涓€涓猄elect鐨勯€夐」璁剧疆涓洪€夋嫨 value
function chooseSelect(selectID,value)
{
 var selectOptions = document.getElementById(selectID).options;
 var length = selectOptions.length;
 var option = null;
 for(var i=0;i<length;i++)
 { 
  option = selectOptions[i];
  if(option.value == value)
   option.selected = true;
  break;
 }
}
//鏍规嵁涓€涓粷瀵硅矾寰勶紝寰楀埌鏌愪竴涓枃浠剁殑鐪熷疄鍚嶇О锛屼繚瀛樼殑瀹屾暣鍚嶇О鍜屾墿灞曞悕绉�-------淇濆瓨鍚嶇О鐨勮矾寰勬牸寮�=琛ㄥ崟鑻辨枃+瀛楁鍚嶇О+褰撳墠鐧诲綍浜哄憳鐨勪俊鎭�+褰撳墠鐨勬绉掓暟
function getPath(filePath,absolutePath,eformEnglish,eformFieldName,username)
{
 //alert("OKOK");
 var pathes = new Array();
 //寰楀埌鏈€鍚庝竴涓矾寰勭殑鏈€鍚庝竴涓猏绗﹀彿鐨勪綅缃�
 var index = filePath.lastIndexOf("\\");
 if(index == -1)
 {
  alert("璇疯緭鍏ュ悎娉曠殑鏂囨。璺緞");
  return false;
 }
 var subpath = filePath.substring(index+1);
 var index1 = subpath.lastIndexOf(".");
 if(index1 == -1)
 {
  alert("绯荤粺涓嶆敮鎸佹病鏈夋墿灞曞悕鐨勬枃浠朵笂浼�");
  return false;
 }
 var extendpath = subpath.substring(index1+1);
 var chinapath = subpath.substring(0,index1);
 var englishpath = absolutePath+"//"+eformEnglish+"_"+eformFieldName+"_"+username+"_"+(new Date()).getTime()+"_"+getRandomNum(999999)+"."+extendpath;
 pathes[0] = chinapath;pathes[1] = englishpath;pathes[2] = extendpath;
 return pathes;
}
//寰楀埌涓€涓皬浜嶮AX鐨勯殢鏈烘暟
function getRandomNum(Max){
 var Range = Max - 0;
 var Rand = Math.random();
 return(Math.round(Rand * Range));
}
function downLoad(filePath,fileName,appendixEXTENSIONValue)
{
 var formele = document.DOWNLOADFORM;
 formele.CHINAVALUE.value = fileName;
 formele.ENLISHVALUE.value = filePath;
 formele.EXTENSIONVALUE.value = appendixEXTENSIONValue;
 formele.submit();
}
/*
 * 鎵撳紑澶栭敭鐨勫熀鏈俊鎭�
 */
function openForeignWindow(foreignName,showFieldName,hideFieldName)
{
 //window.open("go_to_page.do?path=eformdatachooselist&basename="+foreignName+"&showFieldName="+showFieldName+"&hideFieldName="+hideFieldName);
 window.showModalDialog("go_to_page.do?path=eformdatachooselist&basename="+foreignName+"&showFieldName="+showFieldName+"&hideFieldName="+hideFieldName, window, "dialogWidth:800px; dialogHeight:600px; center:yes; help:no; resizable:yes; status:no"); 
}
/*
 *缂栫爜瑙ｇ爜鍑芥暟
 */
 function encode(str,u) 
{
 if (typeof(encodeURIComponent) == 'function') 
 {
  if (u) 
   return encodeURI(str);
  else 
   return encodeURIComponent(str);
 }
 else 
 {
  return escape(str);
 }
}



function decode(str) 
{
 if (typeof(decodeURIComponent) == 'function') 
 {
  try{
  str = decodeURIComponent(str);}catch(Exception){str = unescape(str);}
 } 
 else 
 {
  str = unescape(str);
 }
 return str;
}



 //璁剧疆Cookie鐨勬柟娉�
function setCookie(name,value,path,expires) 
{
 document.cookie = name + "=" + encode(value)    + ";path="+path+" ;" + expires;
}
//寰楀埌Cookie鐨勬柟娉�
function getCookie(name) {  
 var mycookie = document.cookie.split("; ");
 for(var i=0; i<mycookie.length; i++)
 {
  var cookieUser = mycookie[i].split("=");
  if(cookieUser[0] == name)
  {
   return decode(cookieUser[1]);
  }
 }
 return "";
}
/*
 * 鏄剧ず瀹炰綋鐨勮缁嗕俊鎭�
 *ID:鑷畾涔夎〃鍗曠殑锛╋激
 *eformDataID :鑷畾涔夎〃鍗曠殑鏁版嵁鐨処D
 *isMark锛氭槸鍚︽煡鐪嬬暀鐥�
 */
 function showDetail(ID,eformDataID,isMark)
 {
 //window.open("go_to_page.do?path=downloadframe&isMark="+isMark+"&ID="+ID+"&eformDataID="+eformDataID);
 window.showModalDialog("go_to_page.do?path=downloadframe&isMark="+isMark+"&ID="+ID+"&eformDataID="+eformDataID, window, "dialogWidth:800px; dialogHeight:600px; center:yes; help:no; resizable:yes; status:no");
 }
 function showDetailDoc(ID,eformDataID)
 {
  if(ID == "509"){
   window.open("../document/eformDataDetail.jsp?ID="+ID+"&eformDataId="+eformDataID+"&type=onlyContent");
  }else{
   window.open("../document/eformDataDetail.jsp?ID="+ID+"&eformDataId="+eformDataID);
  }
 }
function showDispense(docid,scrollTop,scrollLeft){
 document.getElementById('docid').value=docid;

 document.getElementById('dispense').style.display='block';

 document.getElementById("dispense").style.top=(scrollTop+document.body.clientHeight-document.getElementById("dispense").offsetHeight)/2+"px";
 document.getElementById("dispense").style.left=(scrollLeft+document.body.clientWidth-document.getElementById("dispense").offsetWidth)/2+"px"; 
}

 //鎵撳紑涓€涓枃鏈
 function openWindow(url)
 {
 window.open(url);
 }
 //鎵撳紑涓€涓爣鍑嗙殑鏂囨湰妗�
 function openNoWindow(url)
 {
  window.open(url,'', '','')
 }
function openMorePersonWindow(showField,hideField)
{
 window.open('../main/choose_more_person.jsp?showField='+showField+"&hideField="+hideField,'userwidow','','');
}
function openOnePersonWindow(showField,hideField)
{
 window.open('../main/choose_one_person.jsp?showField='+showField+"&hideField="+hideField,'userwidow','','');
}

function openSqlTool(eformID,parentFieldName,basename)
{
 window.showModalDialog("go_to_page.do?path=sqltool&eformID="+eformID+"&basename="+basename+"&parentFieldName="+parentFieldName, window, "dialogWidth:700px; dialogHeight:500px; center:yes; help:no; resizable:yes; status:no") ;
}
//鍒犻櫎涓€涓〃鍗曟暟鎹殑鏂规硶
function delete_eform_data(ID,eformDataIdList)
{
 var url = "delete_eformdata.do";
 var pars = 'ID='+ID+'&eformDataIdList='+eformDataIdList+'&random='+Math.random();
 //var myAjax = new Ajax.Request(url,{method:'post',parameters:pars,onComplete:});
 $.ajax({
  type: "POST",
  url: url,
  data: pars,
  success: function(msg){
   var initText = msg;
   if(initText.indexOf("FAIL")!=-1)
   {
    //alert("鍒犻櫎[ "+eformDataIdList+" ]鏁版嵁澶辫触");
    alert("鍒犻櫎鏁版嵁澶辫触");
   }else
   {
    //alert("鎴愬姛鍒犻櫎[ "+eformDataIdList+" ]鏁版嵁");
    alert("鎴愬姛鍒犻櫎鏁版嵁");
   }
   init();
  }
 });
}
//褰掓。琛ㄥ崟鏁版嵁鐨勬柟娉�
function gd_eform_data(ID,eformDataIdList)
{
 var url = "gd_eformdata.do";
 var pars = 'ID='+ID+'&eformDataIdList='+eformDataIdList+'&random='+Math.random();
 $.ajax({
  type: "POST",
  url: url,
  data: pars,
  success: function(msg){
   var initText = msg;
   if(initText.indexOf("FAIL")!=-1)
   {
    alert("褰掓。[ "+eformDataIdList+" ]鏁版嵁澶辫触");
   }else
   {
    alert("鎴愬姛瀵筟 "+eformDataIdList+" ]鏁版嵁杩涜浜嗗綊妗�");
   }
   init();
  }
 });
}
//鍒犻櫎琛ㄥ崟鐨勫瓧娈电殑淇℃伅
function deleteTEformField(eformFieldID)
{
 var url = "deleteeformfield.do";
 var pars = 'eformFieldID='+eformFieldID+'&random='+Math.random();
 $.ajax({
  type: "POST",
  url: url,
  data: pars,
  success: function(msg){
   var initText = msg;
   if(initText.indexOf("$FAIL$")!=-1)
   {
    alert("鍒犻櫎[ "+eformFieldID+" ]鏁版嵁澶辫触");
   }else
   {
    alert("鎴愬姛鍒犻櫎[ "+eformFieldID+" ]鏁版嵁");
    init();
   }
  }
 });

}
//寰楀埌杩涜楂樼骇妫€绱㈢殑椤甸潰淇℃伅
function heightSearch(ID)
{
 window.showModalDialog("go_to_page.do?ID="+ID+"&path=eformdatasearch", window, "dialogWidth:900px; dialogHeight:550px; center:yes; help:no; resizable:yes; status:no");
}
//瀵煎嚭鏁版嵁妯℃澘
function downLoadTemplate(ID,fileName)
{
 var url = "geteformdatatemplate.do";
 var pars = 'eformID='+ID+'&random='+Math.random();
 $.ajax({
  type: "POST",
  url: url,
  data: pars,cache: false,
  success: function(msg){
   var text = msg;
   if(text.indexOf("$FAIL$")!=-1)
   {
    alert("鏈嶅姟鍣ㄥ嚭鐜板紓甯�");

   }
   else
   {
    text = trim(text);
    window.location.href = "download/download.jsp?file="+text+"&name="+fileName+".xls";
   }   
  }
 });

}
//閫夋嫨琛ㄥ崟鐨勬柟娉�
function chooseEformID(showFieldName,hideFieldName)
{
 window.showModalDialog("go_to_page.do?showFieldName="+showFieldName+"&hideFieldName="+hideFieldName+"&path=alerteformchooseid", window, "dialogWidth:600px; dialogHeight:700px; center:yes; help:no; resizable:yes; status:no");
}
/*--------------------------------鏍规嵁鍏冪礌鐨� ID 鎴栬€� Name 寰楀埌鏈€鍚庡厓绱犵殑鍊�-----------*/
function $text(fieldId)
{
 var value = ";";
 var element = document.getElementById(fieldId);
 var subOptions = element.options;
 var subOption = null;
 for(var i=0;i<subOptions.length;i++)
 {
  subOption = subOptions[i];
  if(subOption.selected)
   value += subOption.text+";";
 }
 if(value == ";")
  value = "";
 return value;
}
//寰楀埌鏌愪竴涓瓧娈电殑鎵€鍦ㄧ殑TD鐨勫璞�
function searchObjByTagName(obj,tag1,tag2)   
{   
 var index = 0;
 while(obj!=null && typeof(obj.tagName) != "undefind" && index <=5)   
 {   
  if(obj.tagName.toUpperCase()  == tag1.toUpperCase()) 
   return(obj);
  else if(obj.tagName.toUpperCase()  == tag2.toUpperCase()) 
   return(obj);
  obj = obj.parentElement;   
  index ++;
 }   
 return   null;
}   
//鐪佷唤 甯傚尯鐨勪笅鎷夋鍙樺寲鎻愮ず
function province_city_union(cityID,provinceName,cityName)
{
 $("#"+provinceName).change(function(){
  var province = $value(provinceName);
  var url = "getcityaction.do";
  var pars = 'provinceName='+province+'&cityID='+cityID+'&random='+Math.random();
  $.ajax({
   type: "POST",
   url: url,
   data: pars,
   cache: false,
   success: function(msg){
    msg = xmljx(msg);
    var value = XML.getValue(msg,"VALUELIST");
    var text = XML.getValue(msg,"TEXTLIST");
    THSelect.initOne(cityName,text,value,"");
   }
  });
 });
}
//鎵撳紑涓婁紶鐨勭獥鍙ｇ殑淇℃伅
function openAppendix(eformFieldID,eformFieldName)
{
 window.showModalDialog("go_to_page.do?path=upload_frame&eformFieldID="+eformFieldID+"&eformFieldName="+eformFieldName, window, "dialogWidth:800px; dialogHeight:300px; center:yes; help:no; resizable:yes; status:no");
}
//涓嬭浇涓€涓枃浠剁殑鏂规硶
function download(saveFilePath,uploadFileName)
{
 window.location.href = "download/download.jsp?file="+saveFilePath+"&name="+uploadFileName;
}
//缁欎竴涓枃浠剁暀鐥曠殑鏂规硶
function leaveMarks(saveFilePath,uploadFileName,fileExt,type)
{
 if(fileExt == ".doc" || fileExt == ".DOC")
  //window.open("leave_marks.do?file="+saveFilePath+"&type="+type); 
  window.showModalDialog("leave_marks.do?file="+saveFilePath+"&type="+type, window, "dialogWidth:1000px; dialogHeight:600px; center:yes; help:no; resizable:yes; status:no"); 
 else
  download(saveFilePath,uploadFileName);
}
//鍒犻櫎涓€涓檮浠剁殑淇℃伅
function deleteAppendix(eformFieldName,appendixId)
{
 var url = "delete_appendix.do";
 var pars = 'appendixId='+appendixId+'&random='+Math.random();
 //var myAjax = new Ajax.Request(url,{method:'post',parameters:pars,onComplete:});
 $.ajax({
  type: "POST",
  url: url,
  data: pars,
  success: function(msg){
   var initText = msg;
   if(initText.indexOf("$FAIL$")!=-1)
   {
    alert("鍒犻櫎闄勪欢淇℃伅澶辫触");
   }else
   {
    alert("鎴愬姛鍒犻櫎浜嗛檮浠剁殑淇℃伅");
    //寰楀埌褰撳墠鐨勯檮浠剁殑 Hidden 鍩熷悕
    var appendixele = document.getElementById(eformFieldName);
    //寰楀埌褰撳墠鐨勯檮浠剁殑 TD 鐨勪俊鎭�
    var tdele = searchObjByTagName(appendixele,"span","td");
    //寰楀埌褰撳墠鐨勯檮浠舵墍鍦ㄧ殑 SPAN 鐨勪俊鎭�
    var appendixSpan = document.getElementById("appendix_span_"+appendixId);
    //浠嶵D涓垹闄ゆ帀 褰撳墠鐨勯檮浠朵腑鐨� SPAN 鐨勪俊鎭�
    tdele.removeChild(appendixSpan);
    //淇敼闄勪欢涓暟瀵瑰簲鐨勪俊鎭�
    var appendixNum = document.getElementById(eformFieldName).value;
    appendixNum = parseInt(appendixNum)-1;
    document.getElementById(eformFieldName).value = appendixNum;
   }
  }
 });
}
function deleteKmsAppendix(type,appendixId)
{
 var url = "deleteKmsAppendix.do";
 var data = "appendixId="+appendixId+"&type="+type;
 $.ajax({
  type: "POST",
  url: url,
  data:data,
  cache: false,
  success: function(date){
   //鍒嗘瀽闄勪欢鍒犻櫎鏄惁鎴愬姛
   if(date.indexOf("SUCCESS") != -1)
   {
    alert("闄勪欢鍒犻櫎鎴愬姛");
    //寰楀埌褰撳墠鐨勯檮浠剁殑 TD 鐨勪俊鎭�
    var comName = "";
    if(type == "0")
     comName = "PICAPPENDIXELE";
    else if(type == "1")
     comName = "FILEAPPENDIXELE";
    var tdele = document.getElementById(comName);
    //寰楀埌褰撳墠鐨勯檮浠舵墍鍦ㄧ殑 SPAN 鐨勪俊鎭�
    var appendixSpan = document.getElementById("appendix_span_"+appendixId);
    //浠嶵D涓垹闄ゆ帀 褰撳墠鐨勯檮浠朵腑鐨� SPAN 鐨勪俊鎭�
    tdele.removeChild(appendixSpan);
    //淇敼闄勪欢涓暟瀵瑰簲鐨勪俊鎭�
    var appendixNum = document.getElementById(docAppendix).value;
    appendixNum = parseInt(appendixNum)-1;
    document.getElementById(docAppendix).value = appendixNum;
   }
   else if(date.indexOf("$FAIL$") != -1)
    alert("闄勪欢鍒犻櫎澶辫触");
  }
 });
}
function doubleclick(eformName)
{
 if(confirm("纭畾鎵嬪姩杈撳叆锛�"))
 {
  var curSelectNode = document.getElementById(eformName);
  var replaceInputStr = "<input type='text' name="+curSelectNode.name+" id="+curSelectNode.id+" style='width:100px'>";
  var parentEle = searchObjByTagName(curSelectNode,"span","p");
  parentEle.innerHTML = replaceInputStr;
 }
}
//澶勭悊鏌愪竴涓猆RL鍦板潃鐨勫弬鏁颁俊鎭�
function handler(url,param)
{
 var param = param+"=";
 var sindex = url.indexOf(param);
 if(sindex == -1)
  return "";
 var eindex = url.indexOf("&",sindex);
 if(eindex == -1)
  return url.substring(sindex+param.length);
 else
  return url.substring(sindex+param.length,eindex);
}
//鏄剧ず杩涘害鏉�
function showprogress()
{
 //$("#processdiv").attr("className","show");
 
}
//鍏抽棴杩涘害鏉�
function closeprogress()
{
 //$("#processdiv").attr("className","hide");
 //$(document).attr("background","white");
}
function showEditEformData(eformID,eformDataId)
{
 window.showModalDialog("go_to_page.do?path=eformdataedit&ID="+eformID+"&eformDataID="+eformDataId+"&isclosed=true", window, "dialogWidth:800px; dialogHeight:300px; center:yes; help:no; resizable:yes; status:no");
}
function showAddEformData(eformID)
{
 window.showModalDialog("go_to_page.do?path=eformdatainsert&ID="+eformID+"&isclosed=true", window, "dialogWidth:800px; dialogHeight:300px; center:yes; help:no; resizable:yes; status:no");
}
//璁剧疆涓€涓椂闂存鐨勯粯璁ゆ椂闂�
function getDefaultTime(timeDefault)
{
 var date = new Date();
 var year = date.getYear();
 var month = date.getMonth()+1;
 var day = date.getDate();
 var hours = date.getHours();
 var minutes = date.getMinutes();
 month = (month < 10)?"0"+month:month;
 day = (day < 10)?"0"+day:month;
 hours = (hours < 10)?"0"+hours:hours;
 minutes = (minutes < 10)?"0"+minutes:minutes;
 if(timeDefault == "TH_CURDATETIME")
 {
  
  var nowtime = year+"-"+month+"-"+day+" "+hours+":"+minutes;
  return nowtime;
 }
 else if(timeDefault == "TH_CURDATE")
 {
  var nowtime = year+"-"+month+"-"+day;
  return nowtime;
 }
 else
  return "";
}
//寰楀埌褰撳墠鐨勪汉鍛樼殑淇℃伅
function chooseUser(comFieldID,comFieldName)
{
 window.showModalDialog("chooseidname.do?path=chooseuser&comFieldID="+comFieldID+"&comFieldName="+comFieldName, window, "dialogWidth:500px; dialogHeight:600px; center:yes; help:no; resizable:yes; status:no") ;
}
//寰楀埌褰撳墠鐨勮鑹茬殑淇℃伅
function chooseRole(comFieldID,comFieldName)
{
 window.showModalDialog("chooseidname.do?path=chooserole&comFieldID="+comFieldID+"&comFieldName="+comFieldName, window, "dialogWidth:500px; dialogHeight:600px; center:yes; help:no; resizable:yes; status:no") ;
}
function ForDight(Dight,How)  
{  
 Dight = Math.round(Dight*Math.pow(10,How))/Math.pow(10,How);  
 return Dight;  
} 
//鎵撳紑鑱婂ぉ绐楀彛鐨勪俊鎭�
function openChat(loginName)
{
 var s_width = 0;
 var s_height = 0;
 if (self.screen) 
 {
  s_width=screen.width;
  s_height=screen.height;
 } 
 else
 {
  s_width=1024;
  s_height=768;  
 }
 var left = s_width-240;
 window.open("chatTreeIndex.do",loginName+"chatUserTreeWindow","left="+left+",top=0,height=500,width=240,menubar=no,toolbar=no,location =no,status=no,scrollbars=yes,resizable=yes,alwaysRaised=yes,depended=yes,hotkeys=yes,resizable=no");

}
//鏄剧ず婊氬姩鏉�
function showprocessbar(){
 try{
  $("#right").scrollTop(0);
  var jiazai = document.getElementById('jiazai');
  if(!jiazai){
   jiazai = document.createElement('div');
   jiazai.id="jiazai";
   document.body.appendChild(jiazai);

  }
  jiazai.className="add_block_process";
  jiazai.innerHTML = '<div class="border_5"><table width="100%" height="100%" border="0" cellpadding="0" cellspacing="0" class="b0rder_0">     <tr>      <td width="25%" align="right"><img src="'+rootSysName+'/images/loading_2.gif"></td>      <td width="75%" style="padding-left:8px;font-size: 11pt;">姝ｅ湪鏌ヨ锛岃绋嶅悗...</td>     </tr>    </table> </div>';
 }catch(e){
 }
}
//鍏抽棴婊氬姩鏉�
function closeprocessbar(){
 try{
  var jiazai = document.getElementById('jiazai');
  if(jiazai){
   jiazai.innerHTML ="";
   jiazai.className="";
  }
 
 }catch(e){
  alert("error");
 }
}
function getScroll()
{
 if (document.documentElement && document.documentElement.scrollTop)       
  document.documentElement.scrollTop = 0;
 else if (document.body)      
  document.body.scrollTop = 0;
}
function Utf8ToUnicode(strUtf8)
{
 var bstr = "";
 var nTotalChars = strUtf8.length; // total chars to be processed.
 var nOffset = 0; // processing point on strUtf8
 var nRemainingBytes = nTotalChars; // how many bytes left to be converted
 var nOutputPosition = 0;
 var iCode, iCode1, iCode2; // the value of the unicode.

 while (nOffset < nTotalChars)
 {
 iCode = strUtf8.charCodeAt(nOffset);
 if ((iCode & 0x80) == 0) // 1 byte.
 {
 if ( nRemainingBytes < 1 ) // not enough data
 break;

 bstr += String.fromCharCode(iCode & 0x7F);
 nOffset ++;
 nRemainingBytes -= 1;
 }
 else if ((iCode & 0xE0) == 0xC0) // 2 bytes
 {
 iCode1 =   strUtf8.charCodeAt(nOffset + 1);
 if ( nRemainingBytes < 2 || // not enough data
  (iCode1 & 0xC0) != 0x80 ) // invalid pattern
 {
 break;
 }

 bstr += String.fromCharCode(((iCode & 0x3F) << 6) | (     iCode1 & 0x3F));
 nOffset += 2;
 nRemainingBytes -= 2;
 }
 else if ((iCode & 0xF0) == 0xE0) // 3 bytes
 {
 iCode1 =   strUtf8.charCodeAt(nOffset + 1);
 iCode2 =   strUtf8.charCodeAt(nOffset + 2);
 if ( nRemainingBytes < 3 || // not enough data
  (iCode1 & 0xC0) != 0x80 || // invalid pattern
  (iCode2 & 0xC0) != 0x80 )
 {
 break;
 }

 bstr += String.fromCharCode(((iCode & 0x0F) << 12) |
 ((iCode1 & 0x3F) <<   6) |
 (iCode2 & 0x3F));
 nOffset += 3;
 nRemainingBytes -= 3;
 }
 else // 4 or more bytes -- unsupported
 break;
 }

 if (nRemainingBytes != 0)
 {
 // bad UTF8 string.
 return "";
 }

 return bstr;
}
function SetHome(obj){
 var url= window.location.href;
 try{
  obj.style.behavior='url(#default#homepage)';
  obj.setHomePage(url);
 }
 catch(e){
  if(window.netscape) {
   try {
    netscape.security.PrivilegeManager.enablePrivilege("UniversalXPConnect");
   }
   catch (e) {
    alert("姝ゆ搷浣滆娴忚鍣ㄦ嫆缁濓紒\n璇峰湪娴忚鍣ㄥ湴鍧€鏍忚緭鍏モ€渁bout:config鈥濆苟鍥炶溅\n鐒跺悗灏� [signed.applets.codebase_principal_support]鐨勫€艰缃负'true',鍙屽嚮鍗冲彲銆�");
   }
   var prefs = Components.classes['@mozilla.org/preferences-service;1'].getService(Components.interfaces.nsIPrefBranch);
   prefs.setCharPref('browser.startup.homepage',url);
  }
 }
}
//娣诲姞鍒版敹钘忓す
function AddFavorite(title)
{
 var url=window.location.href;
 try
 {
  window.external.addFavorite(url, title);
 }
 catch (e)
 {
  try
  {
   window.sidebar.addPanel(title, url, "");
  }
  catch (e)
  {
   alert("鍔犲叆鏀惰棌澶辫触锛岃浣跨敤Ctrl+D杩涜娣诲姞");
  }
 }
}

//绯荤粺鍚庨€€
function backOrForward(type,obj){
 try{
  $.ajax({
   type:"post",
   url:"go.do",
   data:"type="+type,
   cache:false,
   beforeSend:function(){
    $(obj).unbind("click");
    showprocessbar();
   },
   success:function(date){
    
    if(trim(date).length==0){
     alert("鏈€鍚庝竴椤碉紝鏃犳硶鍚庨€€锛�");
     closeprocessbar();
     return;
    }
    var attr = date.split("?");
    $.post(attr[0],attr[1]+"&backOrforward=0",function(data2){
     closeprocessbar();
     $("#right").html(data2);
     $(obj).bind("click",function(){
      backOrForward(type,obj);
     });
    });
   }
  });
 
 }catch(e){
 }
}
function goToDocDetail(title,url,docid,groupid,content,publishtime,sitename,author,classify,siteaddr,happenprovince,emotion,polarity,keywords,keywordhash,personname,addressname,departname,gathertime,txtfile,txtoffset,txtlength,ip,keyword,channelId)
{ 
 var tag = true;
 try{
  var length = $("input[type=checkbox][name=changeDocId][checked]").length;
  if(length>0){
   tag = window.confirm("纭畾瑕佽闂鏂囩珷鍚�?");
  }
 }catch(e){
 }
 if(tag){
  var param = "title="+title;
  param += "&url="+url;
  param += "&siteName="+sitename;
  param += "&author="+author;
  param += "&classInfo="+classify;
  param += "&siteAddr="+siteaddr;
  param += "&happenProvice="+happenprovince;
  param += "&keywords="+keywords;
  param += "&persionName="+personname;
  param += "&addressName="+addressname;
  param += "&departName="+departname;
  param += "&keywordHash="+keywordhash;
  param += "&ip="+ip;
  param += "&txtfile="+txtfile;
  param += "&txtoffset="+txtoffset;
  param += "&txtlength="+txtlength;
  param += "&docId="+docid;
  param += "&emotion="+emotion;
  param += "&polarity="+polarity;
  param += "&keyword="+keyword;
  param += "&searchChannel="+channelId;
  var url = "document_page_detail.do?menuType=detail&"+param;
  window.open(url);
 }
} 
function goToSkyDocDetail(title,url,docid,groupid,content,publishtime,sitename,author,classify,siteaddr,happenprovince,emotion,polarity,keywords,keywordhash,personname,addressname,departname,gathertime,txtfile,txtoffset,txtlength,ip,keyword,channelId)
{ 
 var tag = true;
 if(tag){
  var param = "title="+title;
  param += "&url="+url;
  param += "&siteName="+sitename;
  param += "&author="+author;
  param += "&classInfo="+classify;
  param += "&siteAddr="+siteaddr;
  param += "&happenProvice="+happenprovince;
  param += "&keywords="+keywords;
  param += "&persionName="+personname;
  param += "&addressName="+addressname;
  param += "&departName="+departname;
  param += "&keywordHash="+keywordhash;
  param += "&ip="+ip;
  param += "&txtfile="+txtfile;
  param += "&txtoffset="+txtoffset;
  param += "&txtlength="+txtlength;
  param += "&docId="+docid;
  param += "&emotion="+emotion;
  param += "&polarity="+polarity;
  param += "&keyword="+keyword;
  param += "&searchChannel="+channelId;
  var url = "document_page_detail_sky.do?menuType=detail&"+param;
  window.open(url);
 }
} 
 
function chooseAll(id,obj){
 var eles = document.getElementsByName(id);
 var ele = null;
 if(obj.checked){
  for(var i=0;i<eles.length;i++){
   ele = eles[i];
   ele.checked = true;
  }
 }
 else{
  for(var i=0;i<eles.length;i++){
   ele = eles[i];
   ele.checked = false;
  }
 }
}
function updateLocation(str){
 $("#location").html(str);
}
//鍏ㄩ€�
function taggleSelectAll(id,name){
 if($("#"+id).attr("checked")){
  $("input[type=checkbox][name="+name+"]").attr("checked","checked"); 
 }else{
  $("input[type=checkbox][name="+name+"]").removeAttr("checked");
 }
}

function getCheckValue(name){
 var ids = ",";
 $("input[type=checkbox][name="+name+"][checked]").each(function(){
  ids =ids+$(this).val()+",";
 });
 return ids;
}
function addLightColorToString(oldStr,keyword){
 if(keyword==null||keyword.length==0){
  return oldStr;
 }
 if(oldStr==null||oldStr.length==0){
  return oldStr;
 }
 var regex = new RegExp(keyword,"g");
 oldStr = oldStr.replace(regex,"<span style='color:#ff0000'>"+keyword+"</span>");
 return oldStr;
}
function handlerStr(str,len){
 if(str.length > len)
  str = str.substring(0,len);
 return str;
}
function isNumber(oNum) 
{ 
 if(!oNum) 
  return false; 
 var strP=/^\d+(\.\d+)?$/; 
 if(!strP.test(oNum)) 
  return false; 
 try{ 
  if(parseFloat(oNum)!=oNum) 
   return false; 
 } 
 catch(ex){ 
  return false; 
 } 
 return true; 
}
//楠岃瘉閭
function isEmail(email)
{
  myReg = /^([-_A-Za-z0-9\.]+)@([-_A-Za-z0-9]+\.)+[_A-Za-z0-9]{2,3}$/;
   if(myReg.test( email )) return true;
   return false;  
}
//楠岃瘉鎵嬫満
function isMobileNo(mobile1)
{
  myReg = /^([-_0-9]+)$/;
  if(myReg.test( mobile1 )) return true;
  return false;  
}
//@param dateLong锛氬綋鍓嶆椂闂寸殑闀挎暣褰�
//@param geshi:杩斿洖瀛楃涓茬殑绫诲瀷 $year$:骞翠唤 $MM$:鏈堜唤 $dd$:鏃ユ湡 $HH$:灏忔椂 $mm$:鍒嗛挓 $ss$:绉� $XSQ$:璺濈褰撳墠澶氬皯涓皬鏃�
function getTimeStringByLong(dateLong,geshi){
 //alert(dateLong);
 if(!isNumber(dateLong))
  return "";
 //dateLong = dateLong+"";
 //if(dateLong.length <=10)
  //dateLong = dateLong+"000";
 //dateLong = parseInt(dateLong);
 if(!geshi)
  geshi = "$yyyy$-$MM$-$dd$ $HH$:$mm$:$ss$";
 var date = new Date();
 var cha = date.getTime()-dateLong;
 date.setTime(dateLong);
 var year = parseInt(date.getYear());
 year = (year < 1900)?(year+1900):year;
 
 var month = parseInt(date.getMonth()+1);
 month = (month < 10)?("0"+month):month;
 
 var cur_date = parseInt(date.getDate());
 cur_date = (cur_date < 10)?("0"+cur_date):cur_date;

 var hour = parseInt(date.getHours());
 hour = (hour < 10)?("0"+hour):hour;

 var minutes = parseInt(date.getMinutes());
 minutes = (minutes < 10)?("0"+minutes):minutes;

 var seconds = parseInt(date.getSeconds());
 seconds = (seconds < 10)?("0"+seconds):seconds;
 geshi = geshi.ReplaceAll("\\$yyyy\\$",(year)).ReplaceAll("\\$MM\\$",(month)).ReplaceAll("\\$dd\\$",cur_date).ReplaceAll("\\$HH\\$",hour).ReplaceAll("\\$mm\\$",minutes).ReplaceAll("\\$ss\\$",seconds).ReplaceAll("\\$XSQ\\$",parseInt((cha/1000/60/60)));

 return geshi;
}
/**
 * @ 鎵惧埌鏌愪竴涓暟缁勪腑鏌愪竴涓€煎墠闈㈠拰鍚庨潰鐨勫€�
 * @ param array:鏁扮粍淇℃伅
 * @ param value:鍊�
 */
function findPreAndNext(array,value){
 var pre = 0;
 var next = 0;
 for(var i=0;i<array.length;i++){
  pre = i-1;
  next = i+1;
  if(array[i] == value)
   break;
 }
 if(pre < 0)
  pre = 0;
 if(next >= array.length)
  next = array.length - 1;
 var resArray = new Array();
 resArray[0] = array[pre];
 resArray[1] = array[next];
 return resArray;
}