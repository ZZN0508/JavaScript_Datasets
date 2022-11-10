window.ikeaStartpage = {};
window.config = {"rootPath":"https://www.ikea.com"};

  function interIkeaCookieConsent(domainName) {
  const otSettings = {
    alertBoxCookieName: 'OptanonAlertBoxClosed',
    currentDomain: domainName,
    ikeaCookieName: 'interIkeaConsent',
    ikeaCookieVersion: 'v0.9', //Bump version if every user should see cookie message again
  };
  function _getCookie(cname) {
    var name = cname + '=';
    var decodedCookie = decodeURIComponent(document.cookie);
    var ca = decodedCookie.split(';');
    for (var i = 0; i < ca.length; i++) {
      var c = ca[i];
      while (c.charAt(0) == ' ') {
        c = c.substring(1);
      }
      if (c.indexOf(name) == 0) {
        return c.substring(name.length, c.length);
      }
    }
    return '';
  }

  function _setCookie(cname, cvalue, exdays, domain) {
    var d = new Date();
    d.setTime(d.getTime() + exdays * 24 * 60 * 60 * 1000);
    var expires = 'expires=' + d.toUTCString();
    var setDomain = domain ? 'domain=' + domain + ';' : '';
    document.cookie =
      cname + '=' + cvalue + ';' + setDomain + expires + ';path=/';
  }
  if (
    _getCookie(otSettings.alertBoxCookieName) ||
    _getCookie(otSettings.ikeaCookieName) == otSettings.ikeaCookieVersion
  ) {
    // Create interIkeaConsent cookie
    _setCookie(
      otSettings.ikeaCookieName,
      otSettings.ikeaCookieVersion,
      365,
      false
    );
    // Invalidate OptanonAlertBoxClosed cookie
    _setCookie(otSettings.alertBoxCookieName, '', -1, otSettings.currentDomain);

    // Hide banner
    document.head.insertAdjacentHTML(
      'beforeend',
      '<style>#onetrust-banner-sdk,.onetrust-pc-dark-filter{display:none;}</style>'
    );
  }
}

  function OptanonWrapper() {
        interIkeaCookieConsent(".www.ikea.com");
      }
    

      (function initGA() {
  window.dataLayer = window.dataLayer || [];
  function gtag() {
    dataLayer.push(arguments);
  }
  window.gtag = gtag;
  gtag('js', new Date());
  gtag('config', 'UA-172012033-1', { transport_type: 'beacon' });
})();
    

        window.Sentry.init({
            dsn: "https://75f51570d7fc47bc92a5565007146415@o437184.ingest.sentry.io/5399384",
            environment: "production",
            beforeSend: function beforeSend(event, hint) {
  var err = hint && hint.originalException;

  if (err && err.message) {
    var ignorePatterns = [
      /Preflight response is not successful/,
      /NotAllowedError: The request is not allowed by the user agent/,
      /Network request failed/,
      /NetworkError when attempting to fetch resource/,
      /cancelled/,
      /Abgebrochen/,
      /geannuleerd/,
      /avbruten/,
      /annullato/,
      /cancelado/,
      /annulé/,
      /annulleret/,
      /anulowane/,
      /avbrutt/,
    ];

    for (var i = 0; i < ignorePatterns.length; i++) {
      if (err.message.match(ignorePatterns[i])) {
        return null;
      }
    }
  }

  return event;
},
            release: window.config.releaseId,
            sampleRate: 0.1
        });
    
bazadebezolkohpepadr="522362729"
var _cf = _cf || [];  _cf.push(['_setFsp', true]);  _cf.push(['_setBm', true]);  _cf.push(['_setAu', '/resources/4f8dc19470rn18824071acaf63b5de73']); 