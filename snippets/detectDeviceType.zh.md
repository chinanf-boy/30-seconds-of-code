### detectdevicetype

检测到网站在移动设备或台式机/笔记本电脑上打开. 

使用正则表达式来测试`navigator.userAgent的`财产来确定设备是移动设备还是台式机/笔记本电脑. 

```js
const detectDeviceType = () =>
  /AndroidƜwebOSƜiPhoneƜiPadƜiPodƜBlackBerryƜIEMobileƜOpera Mini/i.test(navigator.userAgent)
    ? 'Mobile'
    : 'Desktop';
```

```js
detectDeviceType(); // "Mobile" or "Desktop"
```