$(function() { UniversalAuth.performAuth(); });

        $('.hero-box .close').click(function () {
            $.cookie("hero", "closed", { path: "/", expires: 365 });
            var $hero = $(".hero-box");
            $hero.slideUp('fast', function () { $hero.remove(); });
            StackExchange.helpers.gps('hero.closed');
            return false;
        });
    

            var _gaq = _gaq || [];
            _gaq.push(['_setAccount', 'UA-5620270-24']);
            _gaq.push(['_setDomainName', '.stackexchange.com']);
            _gaq.push(['_trackPageview']);

            (function () {
                var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
                ga.src = 'https://ssl.google-analytics.com/ga.js';
                var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
            })();

            _qoptions = { qacct: "p-c1rF4kxgLUzNc" };
        

            var $trigger = $('.js-footer-category-trigger'), $footer = $('.js-footer'), $back = $('.js-footer-back'), $cols = $('.js-footer-col');

            function setCategory(target) {
                var $picked = $cols.filter('[data-name="' + target + '"]');
                $cols.removeClass('site-footer--col__visible');
                $picked.addClass('site-footer--col__visible');
            }

            $trigger.on('click', function (e) {
                e.preventDefault();

                var target = $(this).data('target');

                $trigger.removeClass('_active');
                $(this).addClass('_active');

                $footer.addClass('site-footer__open');
                setCategory(target);
            });

            $back.on('click', function (e) {
                e.preventDefault();

                $trigger.removeClass('_active');
                $footer.removeClass('site-footer__open');

                setCategory('default');
            });
        

        var settings = {
            fkey: 'fb0d641afb6ba49158eb5bf49110e5b7bb66ed3df9d19970a173a2fef5f6dfce',
            contentPath: "https://cdn.sstatic.net/stackexchange"
        };
        $(function() {
            StackExchange.init({"serverTime":1621566797});
            StackExchange.topbar.init();
        });
    