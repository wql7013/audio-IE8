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

调用audioIE8.ready函数初始化所有audio标签，初始化结束后调用回调函数，回调函数中可以使用大多数audio对象的方法和属性
