var len = $(".scrollBanner > ul >li").length;
 if( len > 1){ //杞挱
  jQuery(".scrollBanner").slide({mainCell:"ul",autoPage:true,effect:"topLoop",autoPlay:true});
 }else{ //鍗曞紶banner
  jQuery(".scrollBanner").slide({mainCell:"ul",autoPage:true,effect:"topLoop",autoPlay:false});
 }
 //骞垮憡瑙掓爣
 $.each($(".adTips"), function(){ 
  var adtip = $(this).text();
  if(adtip.indexOf("骞垮憡") >= 0){
   $(this).show();
  }else{
   $(this).hide();
  }
 });
 