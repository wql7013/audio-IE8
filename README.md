# audio-IE8
Use HTML5 Audio Elements in Internet Explorer 8

##Usage
```html
<audio src="xxx.mp3" autoplay></audio>
requirejs(['jquery','audioIE8'], function ($,audioIE8) {
        audioIE8.ready(function () {
            $('audio')[0].on('ended',function(){
              this.play()
            })
        });
});

Call audioIE8.ready method to initialize all of audio elements, then the callback function will be called. In the callback function, most of the methods and properties of audio object can be used.
