# audio-IE8
Use HTML5 Audio Elements in Internet Explorer 8

## Usage
If RequireJS is involved, the following is recommended.

```html
<audio src="xxx.mp3" autoplay></audio>
<scrpit>
requirejs(['jquery','audioIE8'], function ($,audioIE8) {
        audioIE8.ready(function () {
        /**** do someting, for example:
            $('audio').on('ended',function(){
              this.play()
            })
        ******/
        });
});
</script>
```

If no using RequireJS, the following should be adopted.

```html
<script src="audio_ie8.js" />
<audio src="xxx.mp3" autoplay></audio>
<scrpit>
audioIE8.ready(function () {
/**** do someting, for example:
    $('audio').on('ended',function(){
        this.play()
    })
*******/
});
</script>
```

Call audioIE8.ready method to initialize all of audio elements, thereafter the function, the only argument, will be called when the initialization finishes. If all elements are already initialized before audioIE8.ready, the callback function will be executed immediately. The method, audioIE8.ready, can be repetitiously applied, by which multiple callback function can be added, and the initialization will start only when the first time calling audioIE8.ready.

Note: jquery.jplayer.min.js and jquery.jplayer.swf must be put in the same folder. If you don't use requirejs or seajs, you have to put audio_ie8.js in the same folder as the jplayer files.
