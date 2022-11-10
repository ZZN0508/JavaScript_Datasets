var SfdcWwwBase=SfdcWwwBase||{};
var oneTrustComponent=(function(){var b,e=0;
var a={TAB:9,ESCAPE:27,ENTER:13,SPACE:32,LEFT:37,RIGHT:39};
function d(){var p=((b&&b.querySelectorAll(".category-menu-switch-handler"))?b.querySelectorAll(".category-menu-switch-handler"):false);
var n=((b&&b.querySelector(".save-preference-btn-handler"))?b.querySelector(".save-preference-btn-handler"):false);
var j=((b&&b.querySelector("#accept-recommended-btn-handler"))?b.querySelector("#accept-recommended-btn-handler"):false);
var k=((b&&b.querySelector("#ot-tab-desc"))?b.querySelector("#ot-tab-desc"):false);
var l=((b&&b.querySelector("#ot-pc-lst"))?b.querySelector("#ot-pc-lst"):false);
var g=((l&&l.querySelector("#ot-lst-title"))?l.querySelector("#ot-lst-title"):false);
var q=((g&&g.querySelector(".back-btn-handler"))?g.querySelector(".back-btn-handler"):false);
var h=((g&&g.getElementsByTagName("span"))?g.getElementsByTagName("span"):false);
if(q&&h){q.appendChild(h[0])
}function o(r){if(n&&j){if(typeof r.parentElement.dataset.optanongroupid==="undefined"){if(n.classList.contains("visible")){n.classList.remove("visible")
}if(j.classList.contains("optanon-ghost-button")){j.classList.remove("optanon-ghost-button")
}}else{n.classList.add("visible");
j.classList.add("optanon-ghost-button")
}}}for(let i=0;
i<p.length;
i++){p[i].addEventListener("click",function(r){o(r.currentTarget)
});
p[i].addEventListener("keydown",function(r){if(r.keyCode===a.LEFT||r.keyCode===a.RIGHT){m()
}})
}if(k&&n&&j&&p.length){for(let i=0;
i<p.length;
i++){if(i===0){p[0].addEventListener("keydown",function(r){if(r.shiftKey===true&&r.keyCode===a.TAB){setTimeout(function(){j.focus()
},100)
}if(r.shiftKey===false&&r.keyCode===a.TAB){setTimeout(function(){k.focus()
},100)
}})
}else{p[i].addEventListener("keydown",function(r){if(r.shiftKey===true&&r.keyCode===a.TAB){setTimeout(function(){j.focus()
},100)
}})
}}}function m(){for(let i=0;
i<p.length;
i++){if(p[i].classList.contains("ot-active-menu")){o(p[i])
}}}}function c(){var g=setInterval(function(){b=document.querySelector("#onetrust-pc-sdk");
if(b!==undefined&&b!==null&&b){d();
clearInterval(g)
}if(e++>10){clearInterval(g)
}},500)
}function f(){c()
}return{init:f,oneTrustComponent:oneTrustComponent}
}());
function runOneTrustComponent(){oneTrustComponent.init()
}if(document.readyState!="loading"){runOneTrustComponent()
}else{if(document.addEventListener){document.addEventListener("DOMContentLoaded",runOneTrustComponent)
}else{document.attachEvent("onreadystatechange",function(){if(document.readyState=="complete"){runOneTrustComponent()
}})
}};