var site_search_url = "http://search.cnnic.cn/cnnic_search/showResult.jsp";
var channel_search_url = "http://search.cnnic.cn/cnnic_search/search_channel.jsp";
//寰楀埌涓€涓皬浜嶮AX鐨勯殢鏈烘暟
function getRandomNum(Max){
 var Range = Max - 0;
 var Rand = Math.random();
 return(Math.round(Rand * Range));
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
   return where+"CNNICDNA"+str;
 }
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
function handler_date_query(field,value,query){
 var array = value.split("-");
 if(array.length != 3)
  return query;
 value = array[0]+"CNNICHG"+array[1]+"CNNICHG"+array[2];

 query = addDBWhere(query,field+"CNNICDYDYCNNICTODATES"+value+"CNNICTODATEE1");
 query = addDBWhere(query,field+"CNNICXYDYCNNICTODATES"+value+"CNNICTODATEE2");

 return query;
}
function pl_search_bz_btn_1(){
 var bzmc = $("#PL_BZMC_1").val();
 var bzh = $("#PL_BZH_1").val();
 var dyqcr = $("#PL_DYQCR_1").val();
 var fbsj = $("#PL_FBSJ_1").val();
 var sqjg = $("#PL_SQJG_1 option:selected").val();
 var docchannel = $("#PL_DOCCHANNEL_1").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!bzmc && !bzh && !dyqcr && !fbsj && !sqjg){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(bzmc){
  bzmc = encode(bzmc);
  query = addDBWhere(query,"DOCTITLECNNICEKILCNNICHYDCNNICHFB"+bzmc+"CNNICHFBCNNICHYD");
 }
 if(bzh){
  bzh = encode(bzh);
  query = addDBWhere(query,"STANDARDNUMBERCNNICEKILCNNICHYDCNNICHFB"+bzh+"CNNICHFBCNNICHYD");
 }
 if(dyqcr){
  dyqcr = encode(dyqcr);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+dyqcr+"CNNICHFBCNNICHYD");
 }
 if(fbsj)
  query = handler_date_query("DOCRELTIME",fbsj,query);
 if(sqjg){
  sqjg = encode(sqjg);
  query = addDBWhere(query,"COMPANYCNNICEKILCNNICHYDCNNICHFB"+sqjg+"CNNICHFBCNNICHYD");
 }
 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='1'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}
function pl_search_hqjk_btn_2(){
 var hjmc = $("#PL_HJMC_2").val();
 var hjsj = $("#PL_HJSJ_2").val();
 var wcr = $("#PL_WCR_2").val();
 var sjbm = $("#PL_SJBM_2").val();
 var sjlb = $("#PL_HJLB_2 option:selected").val();
 var docchannel = $("#PL_DOCCHANNEL_2").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!hjmc && !hjsj && !wcr && !sjbm && !sjlb){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(hjmc){
  hjmc = encode(hjmc);
  query = addDBWhere(query,"DOCTITLECNNICEKILCNNICHYDCNNICHFB"+hjmc+"CNNICHFBCNNICHYD");
 }

 if(hjsj)
  query = handler_date_query("DOCRELTIME",hjsj,query);

 if(wcr){
  wcr = encode(wcr);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+wcr+"CNNICHFBCNNICHYD");
 }
 if(sjbm){
  sjbm = encode(sjbm);
  query = addDBWhere(query,"DEPTCNNICEKILCNNICHYDCNNICHFB"+sjbm+"CNNICHFBCNNICHYD");
 }
 
 if(sjlb){
  sjlb = encode(sjlb);
  query = addDBWhere(query,"AWARDCATALOGCNNICEKILCNNICHYDCNNICHFB"+sjlb+"CNNICHFBCNNICHYD");
 }
 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='2'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}
function pl_search_jgxm_btn_3(){
 var gjz = $("#PL_GJZ_3").val();
 var jgnf = $("#PL_JGNF_3").val();
 var xmfzr = $("#PL_XMFZR_3").val();
 var ly = $("#PL_LY_3 option:selected").val();
 var docchannel = $("#PL_DOCCHANNEL_3").val();
 //鍒嗘瀽绔ｅ伐骞翠唤
 if(jgnf && !isNumber(jgnf)){
  alert("绔ｅ伐骞翠唤蹇呴』鏄暟瀛楋紝璇烽噸鏂拌緭鍏�");
  $("#PL_JGNF_3").focus();
  return false;
 }
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!gjz && !jgnf && !xmfzr && !ly){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(gjz){
  gjz = encode(gjz);
  query = addDBWhere(query,"DOCKEYWORDSCNNICEKILCNNICHYDCNNICHFB"+gjz+"CNNICHFBCNNICHYD");
 }

 if(jgnf)
  query = addDBWhere(query,"CNNICYEARCNNICDY"+jgnf);

 if(xmfzr){
  xmfzr = encode(xmfzr);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+xmfzr+"CNNICHFBCNNICHYD");
 }
 if(ly){
  ly = encode(ly);
  query = addDBWhere(query,"DOCSOURCECNNICEKILCNNICHYDCNNICHFB"+ly+"CNNICHFBCNNICHYD");
 }
 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='3'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}

function pl_search_lunwen_btn_4(){
 var lwtm = $("#PL_LWTM_4").val();
 var dyzz = $("#PL_DYZZ_4").val();
 var lxzz = $("#PL_LXZZ_4").val();

 var kwmc = $("#PL_KWMC_4").val();
 var hymc = $("#PL_HYMC_4").val();
 var fbnd = $("#PL_FBND_4").val();
 var docchannel = $("#PL_DOCCHANNEL_4").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;

 //鍒嗘瀽绔ｅ伐骞翠唤
 if(fbnd && !isNumber(fbnd)){
  alert("鍙戣〃骞村害蹇呴』鏄暟瀛楋紝璇烽噸鏂拌緭鍏�");
  $("#PL_FBND_4").focus();
  return false;
 }
 if(!lwtm && !dyzz && !lxzz && !kwmc && !hymc && !fbnd){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(lwtm){
  lwtm = encode(lwtm);
  query = addDBWhere(query,"DOCTITLECNNICEKILCNNICHYDCNNICHFB"+lwtm+"CNNICHFBCNNICHYD");
 }

 if(dyzz){
  dyzz = encode(dyzz);
  query = addDBWhere(query,"FIRSTAUTHORCNNICEKILCNNICHYDCNNICHFB"+dyzz+"CNNICHFBCNNICHYD");
 }

 if(lxzz){
  lxzz = encode(lxzz);
  query = addDBWhere(query,"CALLAUTHORCNNICEKILCNNICHYDCNNICHFB"+lxzz+"CNNICHFBCNNICHYD");
 }
 
 if(kwmc){
  kwmc = encode(kwmc);
  query = addDBWhere(query,"KWNAMECNNICEKILCNNICHYDCNNICHFB"+kwmc+"CNNICHFBCNNICHYD");
 }
 

 if(hymc){
  hymc = encode(hymc);
  query = addDBWhere(query,"HYNAMECNNICEKILCNNICHYDCNNICHFB"+hymc+"CNNICHFBCNNICHYD");
 }
 

 if(fbnd){
  query = addDBWhere(query,"CNNICYEARCNNICDY"+fbnd);
 }
 
 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='4'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}

function pl_search_zjxm_btn_5(){
 var gjz = $("#PL_GJZ_5").val();
 var ly = $("#PL_LY_5").val();
 var ksnf = $("#PL_KSNF_5").val();
 var xmfzr = $("#PL_XMFZR_5").val();
 var docchannel = $("#PL_DOCCHANNEL_5").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!gjz && !ly && !ksnf && !xmfzr){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //鍒嗘瀽绔ｅ伐骞翠唤
 if(ksnf && !isNumber(ksnf)){
  alert("寮€濮嬪勾浠藉繀椤绘槸鏁板瓧锛岃閲嶆柊杈撳叆");
  $("#PL_KSNF_5").focus();
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(gjz){
  gjz = encode(gjz);
  query = addDBWhere(query,"DOCKEYWORDSCNNICEKILCNNICHYDCNNICHFB"+gjz+"CNNICHFBCNNICHYD");
 }

 if(ly){
  ly = encode(ly);
  query = addDBWhere(query,"DOCSOURCECNNICEKILCNNICHYDCNNICHFB"+ly+"CNNICHFBCNNICHYD");
 }

 if(ksnf){
  ksnf = encode(ksnf);
  query = addDBWhere(query,"CNNICYEARCNNICDY"+ksnf);
 }
 
 if(xmfzr){
  xmfzr = encode(xmfzr);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+xmfzr+"CNNICHFBCNNICHYD");
 }
 

 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='5'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}
function pl_search_zljs_btn_6(){
 var zlmc = $("#PL_ZLMC_6").val();
 var zllb = $("#PL_ZLLB_6 option:selected").val();
 var sqh = $("#PL_SQH_6").val();
 var zlh = $("#PL_ZLH_6").val();
 var sqrq = $("#PL_SQRQ_6").val();
 var dyfmr = $("#PL_DYFMR_6").val();

 var docchannel = $("#PL_DOCCHANNEL_6").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!zlmc && !zllb && !sqh && !zlh && !sqrq && !dyfmr){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(zlmc){
  zlmc = encode(zlmc);
  query = addDBWhere(query,"DOCTITLECNNICEKILCNNICHYDCNNICHFB"+zlmc+"CNNICHFBCNNICHYD");
 }

 if(zllb){
  zllb = encode(zllb);
  query = addDBWhere(query,"CATEGORYCNNICEKILCNNICHYDCNNICHFB"+zllb+"CNNICHFBCNNICHYD");
 }

 if(sqh){
  sqh = encode(sqh);
  query = addDBWhere(query,"APPLYNUMBERCNNICEKILCNNICHYDCNNICHFB"+sqh+"CNNICHFBCNNICHYD");
 }
 
 if(zlh){
  zlh = encode(zlh);
  query = addDBWhere(query,"PATENTNUMBERCNNICEKILCNNICHYDCNNICHFB"+zlh+"CNNICHFBCNNICHYD");
 }
 
 if(sqrq){
  query = handler_date_query("APPLYTIME",sqrq,query);
 }
 
 if(dyfmr){
  dyfmr = encode(dyfmr);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+dyfmr+"CNNICHFBCNNICHYD");
 }
 


 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='6'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}

function pl_search_zzq_btn_7(){
 var mc = $("#PL_MC_7").val();
 var bbh = $("#PL_BBH_7").val();
 var djh = $("#PL_DJH_7").val();
 var djsj = $("#PL_DJSJ_7").val();
 var zz = $("#PL_ZZ_7").val();
 var scfbr = $("#PL_SCFBR_7").val();

 var docchannel = $("#PL_DOCCHANNEL_7").val();
 //寮€濮嬫瀯閫犳绱�
 var query = "DOCCHANNELCNNICDY"+docchannel;
 if(!mc && !bbh && !djh && !djsj && !zz && !scfbr){
  alert("璇疯緭鍏ユ绱㈡潯浠讹紝鐒跺悗妫€绱�");
  return false;
 }
 //寮€濮嬫瀯閫犺鍒�
 if(mc){
  mc = encode(mc);
  query = addDBWhere(query,"DOCTITLECNNICEKILCNNICHYDCNNICHFB"+mc+"CNNICHFBCNNICHYD");
 }

 if(bbh){
  bbh = encode(bbh);
  query = addDBWhere(query,"ISBNCNNICEKILCNNICHYDCNNICHFB"+bbh+"CNNICHFBCNNICHYD");
 }

 if(djh){
  djh = encode(djh);
  query = addDBWhere(query,"REGISTIDCNNICEKILCNNICHYDCNNICHFB"+djh+"CNNICHFBCNNICHYD");
 }
 
 if(djsj){
  query = handler_date_query("REGISTTIME",djsj,query);
 }
 
 if(zz){
  zz = encode(zz);
  query = addDBWhere(query,"DOCAUTHORCNNICEKILCNNICHYDCNNICHFB"+zz+"CNNICHFBCNNICHYD");
 }
 
 if(scfbr){
  query = handler_date_query("FIRSTTIME",scfbr,query);
 }
 


 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+channel_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='query' id='query' value='"+query+"'/><input type='hidden' name='channelid' id='channelid' value='7'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
 return false;
}

function pl_search_site_btn_0(){
 var pl_search_keyword = $("#PL_SEARCH_KEYWORD_0").val();
 pl_search_keyword = encode(pl_search_keyword);
 //寰楀埌涓€涓殢鏈烘暟
 var randomNumber = getRandomNum(99999);
 $(document.body).append("<form action='"+site_search_url+"' method='post' target='_blank' name='pl_new_search_form"+randomNumber+"' id='pl_new_search_form"+randomNumber+"' target='_blank'><input type='hidden' name='sChar' id='sChar' value='"+pl_search_keyword+"'/></form>");
 $("#pl_new_search_form"+randomNumber).submit();
}