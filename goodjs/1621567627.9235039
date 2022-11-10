 var nowTime = new Date();
    var current_year = nowTime.getFullYear();
    var current_month = nowTime.getMonth() + 1;
    var current_day = nowTime.getDate();
    var current = current_year + '-' + current_month + '-' + current_day;
    var start = current_year - 6;
    var end_year = current_year;
    var end_month = current_month+11;
    
    if(end_month>12){
        end_month = end_month-12;
        end_year = current_year+1;
    }
    var end_day = getDays(end_year, end_month);
    var timeline = {
        "start": start + "-1-1",
        "end": end_year + "-" + end_month + "-" + end_day,
        "current": current
    };
 
/* if(current_year == 2015 && (current_day <=3)){
  $(".category_search .l a").css("background-image","url(http://www.ci123.com/index/styles/images/new_year.gif)");
  $(".category_search .l a").css("width","250px");
  $(".category_search .l a").css("height","85px");
        $(".category_search .l a").css("margin-top","-9px");
  $(".category_search .l span").css("display","none");
 }*/
    var temp = timeline["start"].split("-");
    start_year = temp[0];
    start_month = temp[1];
    start_day = temp[2];

    $(".zyyear").html(addOption(start_year, end_year, current_year));
    selectMonth(current_year, $('.zyyear'));
    setTimeout(function(){
  $('.zymonth option[value="'+current_month+'"]').attr('selected', true);
 }, 1); 
    selectDay(current_year, current_month, $('.zymonth'));
    setTimeout(function(){
  $('.zyday option[value="'+current_day+'"]').attr('selected', 'selected');
 }, 1);
    $('.zyday option[value="'+current_day+'"]').attr('selected', 'selected');

    $(".zyyear").change(function() {
        var selected_year = $(this).find("option:selected").text();
        $(this).next().html("");
        $(this).next().next().html("<option>请选择</option>");

        selectMonth(selected_year, $(this));
    });

    $(".zyyear").next().change(function() {
        var selected_year = $(this).prev().find("option:selected").text();
        var selected_month = $(this).find("option:selected").text();
        $(this).next().html("");
        selectDay(selected_year, selected_month, $(this));
    });

    function selectMonth(selected_year, dom){
        if (selected_year == start_year) {
            dom.next().append(addOption(start_month, 12));
        } else if (selected_year == end_year) {
            dom.next().append(addOption(1, end_month));
        } else {
            dom.next().append(addOption(1, 12));
        }
    }

    function selectDay(selected_year, selected_month, dom){
        var days = getDays(selected_year, selected_month);
        if (selected_year == start_year & selected_month == start_month) {
            dom.next().append(addOption(start_day, days));
        } else if (selected_year == end_year & selected_month == end_month) {
            dom.next().append(addOption(1, end_day));
        } else {
            dom.next().append(addOption(1, days));
        }
    }

    function addOption(start, end, selected) {
        selected = arguments[2] ? arguments[2] : false;//参数列表的第三个
        var code="<option>"+"请选择"+"</option>";
        for (var i = start; i <= end; i++) {
            if (selected == i) {
                code = code + "<option value='"+i+"' selected='selected'>" + i + "</option>";
            }else{
                code = code + "<option value='"+i+"'>" + i + "</option>";
            }
        }
        return code;
    }

    function isRN(y) { //计算闺年
        return y % 4 == 0 || (y % 100 == 0 && y % 400 == 0);
    }

    function getDays(y, m) { //计算每月天数
        if (m == 2) {
            return isRN(y) ? 29 : 28;
        } else if (m < 8) {
            return m % 2 == 0 ? 30 : 31
        } else {
            return m % 2 == 0 ? 31 : 30
        }
    }

/*data.js*/


// 換一批 start
$(function() {
    $('#next1').click(function() {
        var lis = $('#lunhuan_content li');
        var lis_current = $('#lunhuan_content li:visible');
        lis_current.fadeOut();
        if (lis_current.last().index() == lis.last().index()) {
            $('#lunhuan_content li:lt(3)').fadeIn();
        } else {
            lis_current.last().next().fadeIn().next().fadeIn().next().fadeIn();
        }
    });
});
// 換一批 end


// function switch_ad(id_element, self_click) {

//     var ads = $('span', id_element);

//     if (self_click.hasClass("shift_left")) {
//         var last_ad = ads.last().clone();
//         id_element.prepend(last_ad);
//         ads.last().remove();
//     } else {
//         var first_ad = ads.first().clone();
//         id_element.append(first_ad);
//         ads.first().remove();
//     }

// }

/*
$(document).ready(function() {

    var ad_auto_switch = setInterval("fadeAd()",5000);
    $('.slide_li').mouseover(function(){
        window.clearInterval(ad_auto_switch);
    }).mouseout(function(){
        ad_auto_switch = setInterval("fadeAd()",5000);        
    })

})
*/  


function fadeAd(){
    var current = $('.slide_li:visible');
    $('.slide_li').hide();
    if(current.next().hasClass('slide_li')){
        current.hide().next().fadeIn();
    }else{
        $('.slide_li:first').fadeIn();
    }
}



// $(function(){
//     $('#slide_pic').zxSlider({
//         numeric:false,
//         showBtn:false,
//         ulClass: '.slide_pic',
//         liClass: '.slide_li'
//     });
    
// });
$(function(){
    if(!placeholderSupport()){   // 判断浏览器是否支持 placeholder
        $('[placeholder]').focus(function() {
            var input = $(this);
            if (input.val() == input.attr('placeholder')) {
                input.val('');
                input.removeClass('placeholder');
            }
        }).blur(function() {
                var input = $(this);
                if (input.val() == '' || input.val() == input.attr('placeholder')) {
                    input.addClass('placeholder');
                    input.val(input.attr('placeholder'));
                }
            }).blur();
    };
})
function placeholderSupport() {
    return 'placeholder' in document.createElement('input');
}

$(document).ready(function() {
 var center = $('ul.center_view');
 var li = center.find('li');
    li.last().addClass('current_view');
 var right = (li.length-1)*parseInt(li.css('width')) + 'px';
 center.css('right', right);
 $('.l_view').addClass("l_view_x");
 $('.l_view').click(function() {
        var current = center.find('li.current_view');
        if(current.prev().length != 0){
            $('.r_view').css("cursor","pointer");
            current.removeClass('current_view');
            current.prev().addClass('current_view');
            center.animate({
                right: '-='+current.css('width')
            })
        }else{
      $(".l_view").css("cursor","default");
            $('.l_view').removeClass("l_view_x");
        }
    });

    $('.r_view').click(function() {
        var current = center.find('li.current_view');
  $('.r_view').addClass("r_view_x");
        if(current.next().length != 0){
            $('.l_view').css("cursor","pointer");
            current.removeClass('current_view');
            current.next().addClass('current_view');
            center.animate({
                right: '+='+current.css('width')
            })
        }else{
      $(".r_view").css("cursor","default");
            $('.r_view').removeClass("r_view_x");
        }
    });
})

function goWeekly(){
 var select_time = $(".look").parent().prev();
 var year = select_time.find('.zyyear option:selected').val();
 var month = select_time.find('.zymonth option:selected').val();
 var day = select_time.find('.zyday option:selected').val();
 if(year=="请选择"||month=="请选择"|| day=="请选择"){
  return false;
 }else{
  window.open('http://www.ci123.com/weekly/?day='+year+'-'+month+'-'+day);
 }
}