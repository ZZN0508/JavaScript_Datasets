/*<![CDATA[*/if($(document).bind("mobileinit",function(){$.mobile.autoInitializePage=!1}),navigator.userAgent.match(/IEMobile\/10\.0/)){var msViewportStyle=document.createElement("style");msViewportStyle.appendChild(document.createTextNode("@-ms-viewport{width:auto!important}"));document.getElementsByTagName("head")[0].appendChild(msViewportStyle)}/*]]>*/
/*<![CDATA[*/function DecodeHTML(){$(".msame_Header_chev").length&&($(".msame_Header_chev").text()?$(".msame_Header_chev").html($(".msame_Header_chev").text()).show():$(".msame_Header_chev").hide())}function checkDecode(){DecodeHTML();$(".msame_Header_chev").unbind("DOMSubtreeModified",checkDecode)}$(document).ready(function(){var i=document.getElementById("cli_shellHeaderSearchInput"),t=$(i).attr("placeholder").match(/&#(\d+);/g),r=t&&t.length,n;if(r)for(n=0;n<r;n++)i.placeholder=i.placeholder.replace(t[n],String.fromCharCode(t[n].match(/\d+/)))});$(document).ready(DecodeHTML);$(window).load(DecodeHTML);$(window).resize(function(){$(".msame_Header_chev").bind("DOMSubtreeModified",checkDecode)})/*]]>*/

	try {
		if (window.top.location.href == window.location.href) {
			window.addEventListener("message", function (event) {
				if (event.data instanceof Array && event.data.length >= 2 && event.data[0] == "sf_block") {
					window.top.document.body.onbeforeunload = null;
					if (event.data.length == 3 && event.data[2] == "verification-mode") {
						window.top.location.href = event.origin + "/__sf_block/" + event.data[1] + "?url=" + window.top.location.href;
					}
					else {
						window.top.location.href = event.origin + "/__sf_block/" + event.data[1];
					}
				}
			}, false);
		}
	}
	catch (err) { }
