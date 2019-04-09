# Speech Recognition Example

You need Google Chrome (2019-04-09).

- [Live demo  
https://ginpei.github.io/speech-recognition-example/](https://ginpei.github.io/speech-recognition-example/)
- [Spec](https://w3c.github.io/speech-api/)
- [MDN](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition)
- [Can I use](https://caniuse.com/#feat=speech-recognition)

## Basic code

You can try this code in console.

```js
// initialize
const sr = new webkitSpeechRecognition();
 
// show result
sr.addEventListener('result', (event) => {
  const text = event.results[0][0].transcript;
  console.log(text);
});
 
// start listening
sr.start();
```

The recognition seems to stop automatically when you finish speaking.
