var sessionIdentifier = '20201008123300-000.TCbs6a';

        setTimeout(function() {
          if (displayMode === 'bookmarkinfo') {
            var bookmarkInfoBox = document.getElementById('bookmark-info-box');
            if (typeof(bookmarkInfoBox) != 'undefined' && bookmarkInfoBox != null) {
              bookmarkInfoBox.style.display = 'block';
            }
          }
        }, 1000);
      
var shopLoginLink = 'https://www.1und1.de/shoplogin'

            var displayMode = 'unblocked';
          

            var shopLoginEnabled = true;
          

        window.addEventListener('message', ngCookieCheckMessage, false);
        var ngCookieCheck = false;
        var visitId = '20201008123300-000.TCbs6a';
        function ngCookieCheckMessage(event) {
          if (displayMode === 'unblocked' && event && event.data && event.data.ngCookieCheck) {
            var OAO = window.OAO || {};
            OAO.q = OAO.q || {};
            OAO.q.tour = OAO.q.tour || [];
            if (shopLoginEnabled) {
              OAO.q.tour.push(['setLoginInfoLink', shopLoginLink + '?v=' + visitId]);
            }
            OAO.q.tour.push(['setTour', 'login']);
            OAO.q.tour.push(['openWelcomeTour']);
          }
        }
        if (displayMode === 'manual') {
          var OAO = OAO || {};
          OAO.q = OAO.q || {};
          OAO.q.tour = OAO.q.tour || [];
          if (shopLoginEnabled) {
            OAO.q.tour.push(['setLoginInfoLink', shopLoginLink + '?v=' + visitId]);
          }
          OAO.q.tour.push(['setTour', 'login']);
          OAO.q.tour.push(['openWelcomeTour']);
        }
      