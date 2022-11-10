var domain = window.location.hostname;

if(Notification.permission == "granted"  && document.cookie.indexOf('KgnotifDuplicateSwSuccess=') == -1){

    if(document.cookie.indexOf('KgnotifDuplicateSw=') != -1)
    {
        cookie_value = getCookieNotifDpt('KgnotifDuplicateSw');

        if(cookie_value != domain)
        {
            // get all service workers registered
            navigator.serviceWorker.getRegistrations().then(function(registrations){

                // loop all service workers
                for(let registration of registrations) {

                    // find service worker selected
                    if(registration.scope == 'https://'+domain+'/firebase-cloud-messaging-push-scope');
                    {
                        console.log('unregister selected service worker by scope / url / domain')
                        registration.unregister();
                        setCookieNotifDpt("KgnotifDuplicateSwSuccess", 1, 3650, domain);
                    }
                }
            })
        }
    }
    else
    {
        setCookieNotifDpt("KgnotifDuplicateSw", domain, 3650);
    }
}

function setCookieNotifDpt(cname, cvalue, exdays, domain='.kompas.com') {
    var d = new Date();
    d.setTime(d.getTime() + exdays * 24 * 60 * 60 * 1000);
    var expires = "expires=" + d.toUTCString();
    document.cookie = cname + "=" + cvalue + ";" + expires + ";domain="+domain+";path=/";
}

function getCookieNotifDpt(cname) {
    var name = cname + "=";
    var ca = document.cookie.split(";");
    for (var i = 0; i < ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0) == " ") {
            c = c.substring(1);
        }
        if (c.indexOf(name) == 0) {
            return c.substring(name.length, c.length);
        }
    }
    return null;
}