rolling-buttons jQuery plugin
-------------------------
This plugin creates the selected hyperlinks as rolling hyperlinks 

```html
<script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
<script src="http://cdn.rawgit.com/pankajpatel/rolling-buttons/master/jquery.rollingButtons.js"></script>
<script type="text/javascript">
  $(document).ready(function(e){
    $('a').rollingButtons({ background: '#5F85B0', color: '#fff'});
  });
</script>
<a href="time2hack.com">Time to Hack</a>
```
-----------------------------------------------------------------------------

It does not require any explicit CSS or html. Though if you wanna add the css added by plugin to your regular CSS/LESS/SCSS files; you can add the following code block:

```css
.rollers {
  display: inline-block;
  overflow: hidden;
  vertical-align: top;
  -webkit-perspective: 600px;
  -moz-perspective: 600px;
  -ms-perspective: 600px;
  perspective: 600px;
  -webkit-perspective-origin: 50% 50%;
  -moz-perspective-origin: 50% 50%;
  -ms-perspective-origin: 50% 50%;
  perspective-origin: 50% 50%;
}
.rollers:hover {
  text-decoration:none;
}
.rollers span {
  display: block;
  position: relative;
  padding: 0 2px;
  -webkit-transition: all 400ms ease;
  -moz-transition: all 400ms ease;
  -ms-transition: all 400ms ease;
  transition: all 400ms ease;
  -webkit-transform-origin: 50% 0%;
  -moz-transform-origin: 50% 0%;
  -ms-transform-origin: 50% 0%;
  transform-origin: 50% 0%;
  -webkit-transform-style: preserve-3d;
  -moz-transform-style: preserve-3d;
  -ms-transform-style: preserve-3d;
  transform-style: preserve-3d;
}
.rollers:hover span {
  background:'+ options.background +';
  -webkit-transform: translate3d(0px, 0px, -30px) rotateX(90deg);
  -moz-transform: translate3d(0px, 0px, -30px) rotateX(90deg);
  -ms-transform: translate3d(0px, 0px, -30px) rotateX(90deg);
  transform: translate3d(0px, 0px, -30px) rotateX(90deg);
}
.rollers span:after {
  content: attr(data-title);
  display: block;
  position: absolute;
  left: 0;
  top: 0;
  padding: 0 2px;
  color:'+options.color+';
  background:'+ options.background +';
  -webkit-transform-origin: 50% 0%;
  -moz-transform-origin: 50% 0%;
  -ms-transform-origin: 50% 0%;
  transform-origin: 50% 0%;
  -webkit-transform: translate3d(0px, 105%, 0px) rotateX(-90deg);
  -moz-transform: translate3d(0px, 105%, 0px) rotateX(-90deg);
  -ms-transform: translate3d(0px, 105%, 0px) rotateX(-90deg);
  transform: translate3d(0px, 105%, 0px) rotateX(-90deg);
}
```

And if you have added above css in your CSS files, you can initiate the plugi as following code:

```javascript
$(document).ready(function(e){
  $('a').rollingButtons({ background: '#5F85B0', color: '#fff', style: false, className: 'rollers' });
});
```

Just try and play with it

