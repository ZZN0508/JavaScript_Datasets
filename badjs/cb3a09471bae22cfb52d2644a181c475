let Jet = new JetManager();Jet.bind([]);Jet.init({authType: 4, egs: 0, egsAccessed: 0});Jet.bind(["a", "button"]) 

           	document.addEventListener('DOMContentLoaded', function(){
				let items = document.querySelectorAll('.itmHldr_fkcwe90kf2g .item');
				for (item of items) {
					item.onmouseover = function(e) {
						let el = e.target.closest('.itmHldr_fkcwe90kf2g .item');
						el.classList.add('hover');
					}
					item.onmouseout = function(e) {
						let el = e.target.closest('.itmHldr_fkcwe90kf2g .item');
						el.classList.remove('hover');
					}
				}
				document.onclick = function(e) {
					let el = document.getElementById('tooltip');
					if(el.style.display != "block" && e.target.closest('#showTooltip') == document.getElementById('showTooltip')) {
						el.style.display = "block";
						el.classList.remove('fadeOut');
						el.classList.add('fadeTo');
					} else {
						el.classList.remove('fadeTo');
						el.classList.add('fadeOut');
						setTimeout(() => { el.style.display = "none" }, 200);
					}
				}

				let items2 = document.querySelectorAll('#mobileTrigger');
				for (item2 of items2) {
					item2.onclick = function(e) {
						document.getElementById('offInMobileClick').style.display = "none";
						document.getElementById('showThisOnMobileClick').style.display = "block";
						

					}
				}
				
			});
        