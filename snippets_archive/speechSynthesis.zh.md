### speechsynthesis

执行语音合成(实验). 

使用`speechsynthesisutterance.voice`和`window.speechsynthesis.getvoices()`将消息转换为speech.use`window.speechsynthesis.speak()`发挥消息. 

了解更多[语音API的speechsynthesisutterance界面](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance). 

```js
const speechSynthesis = message => {
  const msg = new SpeechSynthesisUtterance(message);
  msg.voice = window.speechSynthesis.getVoices()[0];
  window.speechSynthesis.speak(msg);
};
```

```js
speechSynthesis('Hello, World'); // // plays the message
```