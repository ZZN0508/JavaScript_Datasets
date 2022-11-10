var clip, spinner, $shrinkLink, $shrinkButton, $copyButton, $spinner,$shrinkButton;

$(document).ready(function() {
 clip = null;
 if (AdFly.awesomeBrowser() && ZeroClipboard.detectFlashSupport()) {
  clip = new ZeroClipboard();
        clip.setHandCursor(true);
        clip.glue([$('#shrink_copy')[0]]);
        clip.on('complete', function(client, args) {
            onCopy(client, args);
        });
        $('#shrink_copy_wrapper').remove();
 }

 spinner = AdFly.createSpinner('loading_spinner');
 $shrinkLink = $('#shrink_link');
 $shrinkButton = $('#shrink_submit');
 $copyButton = $('#shrink_copy');
    /*$shrinkAnother = $('#shrink_another');*/
 $spinner = $('#loading_spinner');
 
    if ('#bmlLogin' == window.location.hash && typeof(bmlUrl) != 'undefined' && bmlUrl) {
     var bmlLoc = '/login?bmlUrl=' + encodeURIComponent(bmlUrl);
     if (typeof(bmlType) != 'undefined' && bmlType) {
      bmlLoc +=  '&bmlType=' + encodeURIComponent(bmlType);
     }
     if (typeof(bmlDomain) != 'undefined' && bmlDomain) {
      bmlLoc += '&bmlDomain=' + encodeURIComponent(bmlDomain);
     }
     if (typeof(bmlFolder) != 'undefined' && bmlFolder) {
      bmlLoc += '&bmlFolder=' + encodeURIComponent(bmlFolder);
     }
     window.location = bmlLoc;
    }
    $('#shrink_link').placeholder();
    $('#shrink_submit').click(doShrink);
    $('#shrink_another').click(resetShrinker);
});

function onCopy(client, text) {
    resetShrinker();
};

function resetShrinker(){
    $shrinkLink.val('');
    $shrinkLink.removeAttr('disabled');
    $copyButton.fadeOut(500, function() { $shrinkButton.fadeIn(500); });
    /*$shrinkAnother.fadeOut(500);*/
}

function doShrink() {
 function errorOccured() {
  alert('There was an error while processing your URL. Please make sure the URL you entered is valid and not an adf.ly link.');
 }
 
    $.ajax({
        type: 'post',
        url: '/shortener/shorten',
        data: {
         _user_id: AdFly.API_ANONYMOUS.USER_ID, 
         _api_key: AdFly.API_ANONYMOUS.API_KEY, 
         url: $.trim($shrinkLink.val()),
         csrfToken: $('#shortenIndexCsrfToken').val()
        },
        beforeSend: function(jqXHR, settings) { 
         $shrinkLink.val(' '); // Hide placeholder.
         //$shrinkLink.attr('disabled', 'disabled');
         $shrinkButton.hide();
         $spinner.show();
        },
        error: function(jqXHR, textStatus, errorThrown) {
         errorOccured();
        },
        success: function(data, textStatus, jqXHR) {
         if (typeof(data) != 'object' || data.errors.length != 0 || data.shorts.length != 1) {
                var error = [];
                if (data.errors.length != 0) {
                    for (var i = 0; i < data.errors.length; i++) {
                        error.push(data.errors[i].message);
                    }
                    alert(error.join('\n'));
                } else {
                    errorOccured();
                }
          $shrinkLink.val('');
          $shrinkLink.removeAttr('disabled');
             $shrinkButton.show();
         } else {
          $shrinkLink.val(data.shorts[0].short_url);
          if (AdFly.awesomeBrowser() && ZeroClipboard.detectFlashSupport()) {
           $copyButton.show();
                    /*$shrinkAnother.show();*/
           clip.setText(data.shorts[0].short_url);
           clip.setHandCursor(true);
          } else {
           $copyButton.hide();
                    /*$shrinkAnother.hide();*/
           $shrinkButton.show();
           $shrinkLink.removeAttr('disabled');
          }
         }
         $spinner.hide();
        }
    });
    return false;
};

/*
$(document).ready(function() {
    var divider, earnings, earnings_sel, getStats, links, links_sel, oldStat, parseStat, time_delay, updateStat;
    
    time_delay = 5000;
    divider = '<li class="divider">,</li>';
    earnings = "";
    earnings_sel = $('#earned').find('ul');
    links = "";
    links_sel = $('#clicked').find('ul');
    oldStat = function(sel) {
      var old_stat, selector;
      old_stat = "";
      selector = $(sel).find('.digit');
      $.each(selector, function(key, val) {
        return old_stat += $(val).text();
      });
      return old_stat;
    };
    updateStat = function(selector, value) {
      return $(selector).find('li').fadeOut(500, function() {
        $(selector).html('').append(value);
        return $(selector).find('li').fadeIn(1000);
      });
    };
    parseStat = function(stat) {
      var k, output, output_array, stat_array, v, _ref;
      output = '';
      output_array = [];
      stat_array = stat.split('');
      _ref = stat_array.reverse();
      for (k in _ref) {
        v = _ref[k];
        if (((parseInt(k, 10)) % 3 === 0) && k > 0) {
          output_array.unshift(divider);
          output_array.unshift('<li class="digit">' + v + '</li>');
        } else {
          output_array.unshift('<li class="digit">' + v + '</li>');
        }
      }
      for (k in output_array) {
        v = output_array[k];
        output += v;
      }
      return output;
    };
    getStats = function() {
      var new_earnings, new_links, old_earnings, old_links;
      old_earnings = parseInt(oldStat(earnings_sel), 10);
      old_links = parseInt(oldStat(links_sel), 10);
      new_earnings = '';
      new_links = '';
      return $.ajax({
        url: 'data/home-stats.json',
        dataType: 'json',
        success: function(result) {
          new_earnings = result.data.stats.earned;
          return new_links = result.data.stats.links;
        },
        error: function(request, textStatus, errorThrown) {},
        complete: function(request, textStatus) {
          if (old_earnings !== parseInt(new_earnings, 10)) {
            updateStat(earnings_sel, parseStat(new_earnings, 10));
          }
          if (old_links !== parseInt(new_links)) {
            return updateStat(links_sel, parseStat(new_links));
          }
        }
      });
    };
    //setInterval(getStats, time_delay);
  });
*/