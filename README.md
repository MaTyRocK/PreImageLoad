> **Note: I made this plugin when I was still learning jQuery and JavaScript in general. You should NOT use this! There are lots of good libraries that do the same but 1000x better.**

-----

# PreImageLoad
Ultralight weight jQuery plugin for load small (like thumbs, or nothing) images and fully image when is needed.

The js file size is only **424 bytes**!

# Features
- Small filesize (Only 424bytes!)
- Cross-browser (Tested in IE8 but teorically it works in IE6+)
- Easy customization and configuration
- Fast Page load
- SEO Optimized! (It don't hide images like another plugins)

# Starting
Loading files:

``` html
<script src="jquery-1.11.3.min.js"></script>
<script src="preimageload.min.js"></script>
```

You can put the script in the bottom (before `</body>`), but you could see 'ghost' if you insert alternate content in video container.

# Example

``` html
<!DOCTYPE html>
<html>
<head>
<script src="jquery-1.11.3.min.js"></script>
<script src="preimageload.min.js"></script>
</head>
<body>
<div style="height:500px"></div>
<p>With default config</p>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Googlelogo.png/320px-Googlelogo.png" data-pil-src="https://upload.wikimedia.org/wikipedia/commons/3/30/Googlelogo.png">
<div style="height:500px"></div>
<p>Configured offset</p>
<img data-pil-offset="-500" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Googlelogo.png/320px-Googlelogo.png" data-pil-src="https://upload.wikimedia.org/wikipedia/commons/3/30/Googlelogo.png">
<div style="height:500px"></div>
<script>
$(function(){
	$(window).scroll(function(){
		$.PreImageLoad();
	});
});
</script>
</body>
</html>
```

# Options
- @int `offset` (default `-50`): when to load the fully image
- @bool `allowOverride` (default `true`): read `<img>` `data-pil-offset` attribute and use it as a configuration

# Setting options
``` javascript
var options = {
	offset: 20,
	allowOverride: false
};
$.PreImageLoad(options);
```
