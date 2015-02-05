# Atlas.js [![Build Status](https://travis-ci.org/uupaa/Atlas.js.png)](http://travis-ci.org/uupaa/Atlas.js)

[![npm](https://nodei.co/npm/uupaa.atlas.js.png?downloads=true&stars=true)](https://nodei.co/npm/uupaa.atlas.js/)

Create texture atlas

## Document

- [Atlas.js wiki](https://github.com/uupaa/Atlas.js/wiki/Atlas)
- [WebModule](https://github.com/uupaa/WebModule)
    - [Slide](http://uupaa.github.io/Slide/slide/WebModule/index.html)
    - [Development](https://github.com/uupaa/WebModule/wiki/Development)

## Run on

### Browser

```js
<script src="lib/Atlas.js"></script>
<script>
var imageList = ["http://.../a.png", ...];
var sprite = new Atlas();

Atlas.imageLoader(imageList, function(images) {
    var canvas = document.createElement("canvas");
    var ctx = canvas.getContext("2d");

    for (var i = 0, iz = images.length; i < iz; ++i) {
        sprite.draw(images[i].src, ctx, i * 32, i * 32);
    }
}, function(error) {
    throw error;
}, function(image) {
    sprite.add(image.src, image);
});
</script>
```

### node-webkit

```js
<script src="lib/Atlas.js"></script>
<script>
</script>
```

