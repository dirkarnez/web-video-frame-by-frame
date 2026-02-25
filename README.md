[web-video-frame-by-frame](http://dirkarnez.github.io/web-video-frame-by-frame/index.html)
==========================================================================================
From [mosse/examples/filtertest_gum.html at master · auduno/mosse](https://github.com/auduno/mosse/blob/master/examples/filtertest_gum.html)


### TODOs
- [ ] Offscreen canvas (https://web.dev/articles/offscreen-canvas)
  - ```js
              function detectVideo(active) {
            if (active) {
              detect(el.video)
                .then(() => requestId = requestAnimationFrame(() => detectVideo(true)))
      
            } else {
              cancelAnimationFrame(requestId)
              requestId = null
            }
          }
      
      canvas,
      
      offCanvas.getContext('2d', { willReadFrequently: true })
         offCtx.drawImage(source, 0, 0)
       imageData = offCtx.getImageData(0, 0, canvas.width, canvas.height),
      
      zbarWasm
                .scanImageData(imageData).then(symbols => {
      draw on canvas
      })
    ```
- [ ] Emscripten
- [ ] Threejs integration
- [ ] Worker
  - ```js
    const offscreen = document.querySelector('canvas').transferControlToOffscreen();
    const worker = new Worker('myworkerurl.js');
    worker.postMessage({canvas: offscreen}, [offscreen]);
    ```
- [Manipulating video using canvas - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Manipulating_video_using_canvas)
