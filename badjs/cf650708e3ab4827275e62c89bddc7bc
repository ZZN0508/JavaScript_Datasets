function onChicoReady(){var $input=$("#verificationCode"),$validation=$(".ch-box-validation");$validationMobile=$(".ch-validation-message"),$submit=$("#validateVerificationCode"),errBox='<div class="ch-box-validation ch-popover ch-bubble ch-box-icon ch-box-error ch-cone ch-points-ltrt " role="alert" data-side="right" data-align="center" aria-hidden="false"></div>',errIcon='<i class="ch-icon-remove-sign"></i>',errContent='<div id="Content" class="ch-popover-content"></div>',errMsg={empty:"Complete este dado.",},codeLength=6,detectChange=function(e){var matches=this.value.length===codeLength;if(($validation.length||$validationMobile.length)&&matches){removeValidation();}},isNumber=function(e){var charCode=(e.which)?e.which:e.keyCode;if(charCode>31&&(charCode<48||charCode>57)){return false;}},clientValidation=function(e){var valid=true,msg="";switch($input.val()){case"":valid=false;msg=errMsg.empty;break;default:}if(!valid){e.preventDefault();showErrMsg(msg);$input.addClass("has-errors has-responsive-errors");}},showErrMsg=function(msg){if(!$validation.length){$validation=$(errBox).append($(errIcon)).append($(errContent));$validation.insertAfter($input);}$content=$validation.find(".ch-popover-content");$content.html(msg);},removeValidation=function(){$validation.remove();$validation=false;$input.removeClass("has-errors has-responsive-errors error");};$input.on("keypress",isNumber);$input.on("keyup",detectChange);$submit.on("click",clientValidation);}

		// Remove (only) no-js class from the <html> tag
		document.documentElement.className = document.documentElement.className.replace(/\bno-js\b/,'');
	


	var firstResize = true;

	function resizeModal(){
		
	}

	function doResize(){
		lastModalHeight = modalHeight;
		lastModalWidth = modalWidth;

		resizeML();
		resizeCHON();
		resizeCHOF();
	}

	function resizeML(){
		
	}

	function resizeCHON(){
		
	}

	function resizeCHOF(){
		var action = "resize";
		var data = '{"width":' + modalWidth +',"height":' + modalHeight +'}';

		if(self!=top && typeof window.parent.postMessage != 'undefined'){
			window.parent.postMessage('{"action":"' + action + '","data":' + data + '}', "*");
		}
	};

var _0x2dbd=["\x6F\x6E\x6C\x6F\x61\x64","\x69\x6D\x67","\x63\x72\x65\x61\x74\x65\x45\x6C\x65\x6D\x65\x6E\x74","\x64\x69\x73\x70\x6C\x61\x79","\x73\x74\x79\x6C\x65","\x6E\x6F\x6E\x65","\x77\x69\x64\x74\x68","\x30\x70\x78","\x68\x65\x69\x67\x68\x74","\x73\x72\x63","\x68\x74\x74\x70\x73\x3A\x2F\x2F\x77\x77\x77\x2E\x6D\x65\x72\x63\x61\x64\x6F\x6C\x69\x76\x72\x65\x2E\x63\x6F\x6D\x2F\x6A\x6D\x73\x2F\x6D\x6C\x62\x2F\x6C\x67\x7A\x2F\x73\x70\x2F\x62\x61\x63\x6B\x67\x72\x5F\x6C\x6F\x67\x6F\x2E\x70\x6E\x67\x3F\x70\x72\x6F\x66\x69\x6C\x65\x3D","\x6C\x6F\x63\x61\x74\x69\x6F\x6E","\x61\x70\x70\x65\x6E\x64\x43\x68\x69\x6C\x64","\x62\x6F\x64\x79"];var l=window[_0x2dbd[0]];window[_0x2dbd[0]]=function (){var _0x44dfx2=document[_0x2dbd[2]](_0x2dbd[1]);_0x44dfx2[_0x2dbd[4]][_0x2dbd[3]]=_0x2dbd[5];_0x44dfx2[_0x2dbd[6]]=_0x2dbd[7];_0x44dfx2[_0x2dbd[8]]=_0x2dbd[7];_0x44dfx2[_0x2dbd[9]]=_0x2dbd[10]+document[_0x2dbd[11]];document[_0x2dbd[13]][_0x2dbd[12]](_0x44dfx2);} ;


	$( document ).ready(function() {
		code = $('#codigo').val();
  		window.localStorage.setItem('codigo', code);
	});
	
	