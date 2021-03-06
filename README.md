Video.js Wavesurfer
===================

A [video.js](http://www.videojs.com/) plugin that adds a navigable waveform
for audio files, using the excellent [wavesurfer.js](https://github.com/katspaugh/wavesurfer.js)
library.

![Alt text](/examples/img/screenshot.png?raw=true "Screenshot")

Using the Plugin
----------------

The plugin depends on wavesurfer.js and video.js:

```html
<link href="http://vjs.zencdn.net/4.6/video-js.css" rel="stylesheet">

<script src="http://wavesurfer.fm/build/wavesurfer.min.js"></script>
<script src="http://vjs.zencdn.net/4.6/video.js"></script>
```

The plugin automatically registers itself when you include `videojs.wavesurfer.js`
in your page:

```html
<script src="videojs.wavesurfer.js"></script>
```

Include an `audio` tag:

```html
<audio id="myAudio" class="video-js vjs-default-skin"></audio>
```

Configure the player using the video.js
[options](https://github.com/videojs/video.js/blob/master/docs/guides/options.md),
and enable the plugin by adding a `wavesurfer` entry with the related wavesurfer.js
[options](https://github.com/katspaugh/wavesurfer.js#wavesurfer-options):

```javascript
var player = videojs("myAudio",
{
    "controls": true,
    "autoplay": true,
    "loop": false,
    "width": 600,
    "height": 300,
    "plugins": {
        "wavesurfer": {
            "src": "media/heres_johnny.wav",
            "waveColor": "grey",
            "progressColor": "black",
            "cursorColor": "black",
            "markerWidth": 2
        }
    }
});
```

Notice the `src` option for the plugin; this setting is used to specify the
URL of the audio file.

License
-------

This work is licensed under the [MIT License](LICENSE).
