---
title: Post
layout: page
permalink: /post.html

---


![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png) | Pick your capture tool| ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)
:-----------: | :-----------: | :-----------:  
 ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)|[![Menulogo](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/photo.png)](post_photo.html)| ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)
 ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)|[![Menulogo](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/audio.png)](post_audio.html)| ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)
  ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)|[![Menulogo](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/video.png)](post_video.html)| ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)
   ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)|[![Menulogo](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/library.png)](post_library.html)| ![pixel](https://raw.githubusercontent.com/Stuartbriner/portland/gh-pages/images/apixel.png)

<input type="file" accept="image/*" capture="camera">

<input type="file" accept="audio/*;capture=microphone">

<input type="file" accept="video/*;capture=camcorder">

<video autoplay id="vid" style="display:none;"></video>
<canvas id="canvas" width="400" height="400" style="border:1px solid #d3d3d3;"></canvas><br>
<button onclick="snapshot()">Take Picture</button>

<script type="text/javascript">
    var video = document.querySelector("#vid");
    var canvas = document.querySelector('#canvas');
    var ctx = canvas.getContext('2d');
    var localMediaStream = null;

    var onCameraFail = function (e) {
        console.log('Camera did not work.', e);
    };

    function snapshot() {
        if (localMediaStream) {
            ctx.drawImage(video, 0, 0);
        }
    }

    navigator.getUserMedia = navigator.getUserMedia || navigator.webkitGetUserMedia || navigator.mozGetUserMedia || navigator.msGetUserMedia;
    window.URL = window.URL || window.webkitURL;
    navigator.getUserMedia({video:true}, function (stream) {
        video.src = window.URL.createObjectURL(stream);
        localMediaStream = stream;
    }, onCameraFail);

</script>
***

[back](G1_A1_pathway2.html)


[Get Piano Practice Partner](https://itunes.apple.com/gb/app/abrsm-piano-practice-partner/id891238739?mt=8)
