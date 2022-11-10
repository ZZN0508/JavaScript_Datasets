var jq = jQuery.noConflict(true);
jq(document).ready(function(){
    jq(".yinyingceng").click(function(){
      jq('#xialacaidan').collapse('hide');
      jq("html,body").addClass('ovfhidden');
      jq(".xiao-ul").animate({left:'0px'},"slow");
      jq(".xiao-ul").hide().css("display","block");
      jq(".zhezhao").show().css({height:$("html").height()});
    })
    jq(".zhezhao").click(function(){
        if((".xiao-ul:visible")){
          jq("html,body").removeClass('ovfhidden');
          jq(".xiao-ul").animate({left:'-500px'},"slow");
          jq(".zhezhao").hide().css("display","none");
        }
    })
  jq(window).scroll(function() {
    if(jq(window).scrollTop()>100 && jq("html").width()<600){
    jq(".gotop").fadeIn(100);
    }else{
    jq(".gotop").fadeOut(100);
    }
  })
    jq(".gotop").click(function(){
        jq("html,body").animate({ scrollTop:0},300);
    })
  jq('#identifier').carousel({
  interval: 5000
})

    var myTouch = util.toucher(document.getElementById('myCarousel'));

    myTouch.on('swipeLeft',function(e){
     jq('#carright').click();
      }).on('swipeRight',function(e){
      jq('#carleft').click();
      });
  });