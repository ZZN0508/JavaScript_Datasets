var adCindex = new Object();
adCindex.go = function (code) {
 switch (code) {
  case 1:
   {
    if (typeof (fcBox) != "undefined") {
     fcBox.go();
    }
    if (typeof (xtBox) != "undefined") {
     xtBox.go();
    }
    if (typeof (fcBox) == "undefined" && typeof (xtBox) == "undefined") {
     if (typeof $PMP_RICHMEDIA_SHOWID != "undefined"){
      importAd(["//static.mediav.com/js/mvf_g3.js"]);
     }else{
      adCindex.go(2);
     }
    }
    break;
   }
  case 2:
   {
    if (typeof (dlBox) != "undefined") {
     dlBox.go();
    }
    if (typeof (scBox) != "undefined") {
     scBox.go();
    }
    if (typeof (dwBox) != "undefined") {
     dwBox.createAD();
    }
    if (typeof (top_banner_big) != "undefined") {
     top_banner_big.createAD();
    }
    if (typeof (TfBox) != "undefined") {
     TfBox.createAD();
    }
    else {
     adCindex.go(3);
    }
    break;
   }
  case 3:
   {
    break;
   }
   break;
 }
}
adCindex.go(1);