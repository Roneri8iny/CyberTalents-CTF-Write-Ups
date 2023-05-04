# Cool Name Effect Write-Up:

After we view page source, we find this piece of code:

```JavaScript
eval(function(p,a,c,k,e,d){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--){d[e(c)]=k[c]||e(c)}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('(6($,12){$.1b.N=6(25,5){7 T={\'1L\':1W.2b,\'1K\':1W.2a};d 4.p(6(){7 $4=$(4);7 1T=25||1;b(5){$.1H(T,5)}7 1m=6(){$4.W(\'2c-2d\',n.2f(n.29($4.2e()/(1T*10),22(T.1K)),22(T.1L)))};1m();$(X).1u(1m)})};6 Y(t,23,1Q,1P){7 a=t.2A().2u(23),1g=\'\',S;b(a.2t){$(a).p(6(i,V){S=\'\';b(V===\' \'){S=\' 1O\';V=\'&2s;\'}1g+=\'<1k 2h="\'+1Q+(i+1)+S+\'">\'+V+\'</1k>\'+1P});t.1O().2y(1g)}}7 O={1n:6(){d 4.p(6(){Y($(4),\'\',\'2x\',\'\')})},2r:6(){d 4.p(6(){Y($(4),\' \',\'2q\',\' \')})},2k:6(){d 4.p(6(){7 r="2j";Y($(4).2i("2l").2p(r).2n(),r,\'2v\',\'\')})}};$.1b.1h=6(q){b(q&&O[q]){d O[q].1j(4,[].1d.K(1e,1))}1R b(q===\'F\'||!q){d O.1n.1j(4,[].1d.K(1e,0))}$.1Y(\'2o \'+q+\' 2m 2z 2w 18 1f.1h\');d 4};$.L=6(5,1x){4.$E=$(1x);4.1y(5)};$.L.1E={9:0,C:1,D:R,N:J};$.L.21={1y:6(5){4.5=$.1H(R,{},$.L.1E,5);4.1w();4.$E.k(\'c\',R);4.Z();4.P();4.1q()},1w:6(){4.$E.1h();b(4.5.N)4.$E.N();4.$F=4.$E.26(\'1k\').W(\'27\',\'28-2g\')},Z:6(){b(4.5.9===-1)d J;4.1B();4.1p()},1B:6(){4.B=0;7 8=4;4.$F.p(6(i){7 $e=$(4),14=$e.1o(R);8.B+=14;$e.k(\'1l\',8.B-14/2)});7 1c=4.B/2;b(4.5.9<1c)4.5.9=1c;4.1X=4.B;7 M=2*n.1I(4.1X/(2*4.5.9));4.1t=4.5.9*M},1p:6(){7 8=4,G=0;4.$F.p(6(i){7 $e=$(4),1v=($e.1o(R)/8.B)*8.1t,19=1v/8.5.9,h=8.5.9*(n.1F(19/2)),1s=n.2F((8.B/2-G)/8.5.9),17=1s+19/2,x=n.1F(17)*h,y=n.38(17)*h,15=G+n.34(8.B/2-x-G),1r=0|15-$e.k(\'1l\'),1i=0|8.5.9-y,M=(8.5.D)?0|-n.1I(x/8.5.9)*(2Z/n.32):0;G=2*15-G;$e.k({x:1r,y:(8.5.C===1)?1i:-1i,a:(8.5.C===1)?M:-M})})},P:6(Q){b(!4.$E.k(\'c\'))d J;7 8=4;4.$F.p(6(i){7 $e=$(4),H=(8.5.9===-1)?\'1A\':\'2X(\'+$e.k(\'x\')+\'1G) 2Y(\'+$e.k(\'y\')+\'1G) D(\'+$e.k(\'a\')+\'37)\',m=(Q)?\'2B \'+(Q.39||0)+\'13 \'+(Q.3d||\'3b\'):\'1A\';$e.W({\'-1C-m\':m,\'-1D-m\':m,\'-o-m\':m,\'-13-m\':m,\'m\':m}).W({\'-1C-I\':H,\'-1D-I\':H,\'-o-I\':H,\'-13-I\':H,\'I\':H})})},1q:6(){b(4.5.N){7 8=4;$(X).18(\'1u.c\',6(){8.Z();8.P()})}},1z:6(v){b(!v.9&&!v.C&&v.D===\'12\'){d J}4.5.9=v.9||4.5.9;4.5.C=v.C||4.5.C;b(v.D!==12){4.5.D=v.D}4.Z();4.P(v.Q)},3a:6(){4.5.9=-1;4.P();4.$F.20(\'x y a 1l\');4.$E.20(\'c\');$(X).2V(\'.c\')}};7 16=6(1J){b(4.1Z){1Z.1Y(1J)}};$.1b.c=6(5){b(2I 5===\'2J\'){7 1S=2K.21.1d.K(1e,1);4.p(6(){7 A=$.k(4,\'c\');b(!A){16("2H K O 18 c 2G 11 2C; "+"2D 11 K q \'"+5+"\'");d}b(!$.2E(A[5])||5.2W(0)==="2L"){16("2M 2S q \'"+5+"\' 2T c A");d}A[5].1j(A,1S)})}1R{4.p(6(){7 A=$.k(4,\'c\');b(!A){$.k(4,\'c\',2Q $.L(5,4))}})}d 4}})(1f);(6(j,w){7 24=1U;7 U=6(){7 z=[\'y\',\'o\',\'u\',\'r\',\' \',\'f\',\'l\',\'a\',\'g\',\' \',\'i\',\'s\',\':\'];7 f=([]["2N"]+"")[3];f+=([J]+12)[10];f+=(1N+[1V])[10];f+=(1N+[1V])[10];f+=(+(2O))["11"+1M["1a"]](31)[1];f+=([]["2P"]()+"")[3];f+=(+(35))["11"+1M["1a"]](36);24(z.2R(\'\')+f)};w.1U=U;w.2U=U;w.33=U;j(6(){$x=j(\'#1a\');$x.c({9:3c});$x.c(\'1z\',{9:30,C:1})})})(1f,X);',62,200,'||||this|options|function|var|_self|radius||if|arctext|return|letter||||||data||transition|Math||each|method|||||opts|||||instance|dtWord|dir|rotate|el|letters|iteratorX|transformation|transform|false|call|Arctext|angle|fitText|methods|_rotateWord|animation|true|emptyclass|settings|newAlert|item|css|window|injector|_calc||to|undefined|ms|letterWidth|xpos|logError|theta|on|beta|name|fn|centerWord|slice|arguments|jQuery|inject|lettering|yval|apply|span|center|resizer|init|outerWidth|_calcLetters|_loadEvents|xval|alpha|dtArc|resize|dtArcLetter|_applyLettering|element|_init|set|none|_calcBase|webkit|moz|defaults|cos|px|extend|asin|message|maxFontSize|minFontSize|String|NaN|empty|after|klass|else|args|compressor|alert|Infinity|Number|dtArcBase|error|console|removeData|prototype|parseFloat|splitter|legacyAlert|kompressor|find|display|inline|min|POSITIVE_INFINITY|NEGATIVE_INFINITY|font|size|width|max|block|class|children|eefec303079ad17405c889e092e105b0|lines|br|does|end|Method|replaceWith|word|words|nbsp|length|split|line|exist|char|append|not|text|all|initialization|attempted|isFunction|acos|prior|cannot|typeof|string|Array|_|no|fill|211|entries|new|join|such|for|prompt|off|charAt|translateX|translateY|180|140||PI|confirm|abs|||deg|sin|speed|destroy|linear|400|easing'.split('|'),0,{}));
```

We see that this is an obfuscation, that means that we can use the website http://deobfuscatejavascript.com/ to deobfuscate this. After doing just that, we get the following code:

```JavaScript
(function($, undefined) {
    $.fn.fitText = function(kompressor, options) {
        var settings = {
            'minFontSize': Number.NEGATIVE_INFINITY,
            'maxFontSize': Number.POSITIVE_INFINITY
        };
        return this.each(function() {
            var $this = $(this);
            var compressor = kompressor || 1;
            if (options) {
                $.extend(settings, options)
            }
            var resizer = function() {
                    $this.css('font-size', Math.max(Math.min($this.width() / (compressor * 10), parseFloat(settings.maxFontSize)), parseFloat(settings.minFontSize)))
                };
            resizer();
            $(window).resize(resizer)
        })
    };

    function injector(t, splitter, klass, after) {
        var a = t.text().split(splitter),
            inject = '',
            emptyclass;
        if (a.length) {
            $(a).each(function(i, item) {
                emptyclass = '';
                if (item === ' ') {
                    emptyclass = ' empty';
                    item = '&nbsp;'
                }
                inject += '<span class="' + klass + (i + 1) + emptyclass + '">' + item + '</span>' + after
            });
            t.empty().append(inject)
        }
    }
    var methods = {
        init: function() {
            return this.each(function() {
                injector($(this), '', 'char', '')
            })
        },
        words: function() {
            return this.each(function() {
                injector($(this), ' ', 'word', ' ')
            })
        },
        lines: function() {
            return this.each(function() {
                var r = "eefec303079ad17405c889e092e105b0";
                injector($(this).children("br").replaceWith(r).end(), r, 'line', '')
            })
        }
    };
    $.fn.lettering = function(method) {
        if (method && methods[method]) {
            return methods[method].apply(this, [].slice.call(arguments, 1))
        } else if (method === 'letters' || !method) {
            return methods.init.apply(this, [].slice.call(arguments, 0))
        }
        $.error('Method ' + method + ' does not exist on jQuery.lettering');
        return this
    };
    $.Arctext = function(options, element) {
        this.$el = $(element);
        this._init(options)
    };
    $.Arctext.defaults = {
        radius: 0,
        dir: 1,
        rotate: true,
        fitText: false
    };
    $.Arctext.prototype = {
        _init: function(options) {
            this.options = $.extend(true, {}, $.Arctext.defaults, options);
            this._applyLettering();
            this.$el.data('arctext', true);
            this._calc();
            this._rotateWord();
            this._loadEvents()
        },
        _applyLettering: function() {
            this.$el.lettering();
            if (this.options.fitText) this.$el.fitText();
            this.$letters = this.$el.find('span').css('display', 'inline-block')
        },
        _calc: function() {
            if (this.options.radius === -1) return false;
            this._calcBase();
            this._calcLetters()
        },
        _calcBase: function() {
            this.dtWord = 0;
            var _self = this;
            this.$letters.each(function(i) {
                var $letter = $(this),
                    letterWidth = $letter.outerWidth(true);
                _self.dtWord += letterWidth;
                $letter.data('center', _self.dtWord - letterWidth / 2)
            });
            var centerWord = this.dtWord / 2;
            if (this.options.radius < centerWord) this.options.radius = centerWord;
            this.dtArcBase = this.dtWord;
            var angle = 2 * Math.asin(this.dtArcBase / (2 * this.options.radius));
            this.dtArc = this.options.radius * angle
        },
        _calcLetters: function() {
            var _self = this,
                iteratorX = 0;
            this.$letters.each(function(i) {
                var $letter = $(this),
                    dtArcLetter = ($letter.outerWidth(true) / _self.dtWord) * _self.dtArc,
                    beta = dtArcLetter / _self.options.radius,
                    h = _self.options.radius * (Math.cos(beta / 2)),
                    alpha = Math.acos((_self.dtWord / 2 - iteratorX) / _self.options.radius),
                    theta = alpha + beta / 2,
                    x = Math.cos(theta) * h,
                    y = Math.sin(theta) * h,
                    xpos = iteratorX + Math.abs(_self.dtWord / 2 - x - iteratorX),
                    xval = 0 | xpos - $letter.data('center'),
                    yval = 0 | _self.options.radius - y,
                    angle = (_self.options.rotate) ? 0 | -Math.asin(x / _self.options.radius) * (180 / Math.PI) : 0;
                iteratorX = 2 * xpos - iteratorX;
                $letter.data({
                    x: xval,
                    y: (_self.options.dir === 1) ? yval : -yval,
                    a: (_self.options.dir === 1) ? angle : -angle
                })
            })
        },
        _rotateWord: function(animation) {
            if (!this.$el.data('arctext')) return false;
            var _self = this;
            this.$letters.each(function(i) {
                var $letter = $(this),
                    transformation = (_self.options.radius === -1) ? 'none' : 'translateX(' + $letter.data('x') + 'px) translateY(' + $letter.data('y') + 'px) rotate(' + $letter.data('a') + 'deg)',
                    transition = (animation) ? 'all ' + (animation.speed || 0) + 'ms ' + (animation.easing || 'linear') : 'none';
                $letter.css({
                    '-webkit-transition': transition,
                    '-moz-transition': transition,
                    '-o-transition': transition,
                    '-ms-transition': transition,
                    'transition': transition
                }).css({
                    '-webkit-transform': transformation,
                    '-moz-transform': transformation,
                    '-o-transform': transformation,
                    '-ms-transform': transformation,
                    'transform': transformation
                })
            })
        },
        _loadEvents: function() {
            if (this.options.fitText) {
                var _self = this;
                $(window).on('resize.arctext', function() {
                    _self._calc();
                    _self._rotateWord()
                })
            }
        },
        set: function(opts) {
            if (!opts.radius && !opts.dir && opts.rotate === 'undefined') {
                return false
            }
            this.options.radius = opts.radius || this.options.radius;
            this.options.dir = opts.dir || this.options.dir;
            if (opts.rotate !== undefined) {
                this.options.rotate = opts.rotate
            }
            this._calc();
            this._rotateWord(opts.animation)
        },
        destroy: function() {
            this.options.radius = -1;
            this._rotateWord();
            this.$letters.removeData('x y a center');
            this.$el.removeData('arctext');
            $(window).off('.arctext')
        }
    };
    var logError = function(message) {
            if (this.console) {
                console.error(message)
            }
        };
    $.fn.arctext = function(options) {
        if (typeof options === 'string') {
            var args = Array.prototype.slice.call(arguments, 1);
            this.each(function() {
                var instance = $.data(this, 'arctext');
                if (!instance) {
                    logError("cannot call methods on arctext prior to initialization; " + "attempted to call method '" + options + "'");
                    return
                }
                if (!$.isFunction(instance[options]) || options.charAt(0) === "_") {
                    logError("no such method '" + options + "' for arctext instance");
                    return
                }
                instance[options].apply(instance, args)
            })
        } else {
            this.each(function() {
                var instance = $.data(this, 'arctext');
                if (!instance) {
                    $.data(this, 'arctext', new $.Arctext(options, this))
                }
            })
        }
        return this
    }
})(jQuery);
(function(j, w) {
    var legacyAlert = alert;
    var newAlert = function() {
            var z = ['y', 'o', 'u', 'r', ' ', 'f', 'l', 'a', 'g', ' ', 'i', 's', ':'];
            var f = ([]["fill"] + "")[3]; 
            f += ([false] + undefined)[10];   
            f += (NaN + [Infinity])[10];   
            f += (NaN + [Infinity])[10];   
            f += (+(211))["to" + String["name"]](31)[1];
            f += ([]["entries"]() + "")[3];
            f += (+(35))["to" + String["name"]](36);
            legacyAlert(z.join('') + f);
            console.log(f);
        };
    w.alert = newAlert;
					    w.prompt = newAlert;
    w.confirm = newAlert;
    j(function() {
        $x = j('#name');
        $x.arctext({
            radius: 400
        });
        $x.arctext('set', {
            radius: 140,
            dir: 1
        })
    })
})(jQuery, window);
```

We can conclude from focusing on the last function which creates  a new flag that we have to somehow force an alert box to appear in hope that the flag will appear in it.

We can do this via XSS , so I tried the first payload which is :

> <script>alert()</script>

And I noticed that the output seems to be buffled , so I figured that the input field filters the input and does not pass "script" word.

So, I tried changing the format of the word script in hopes that it will bypass the filteration and fortunately it did.
The script was:

> <ScRiPt>alert()</ScRiPt>

And that did the trick and an alert box appeared containing the flag.