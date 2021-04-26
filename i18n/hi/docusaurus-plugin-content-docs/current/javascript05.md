---
id: javascript05
title: त्रुटियाँ
sidebar_label: त्रुटियाँ
---

import YouTube from 'react-youtube'

![@serverSerrverlesskiy](/img/javascript/headers/05.jpg)

आप निश्चित रूप से, हम में से बाकी लोगों की तरह, गलतियाँ करेंगे🙅‍♂️ कोड में📟. सॉफ्टवेयर कीड़े🙅‍♂️ कीड़े कहलाते हैं। बग का अर्थ है त्रुटि🙅‍♂️ अपकृत्य💾 या एक ऐसी प्रणाली पर जो अप्रत्याशित व्यवहार और एक परिणाम के रूप में एक कार्यक्रम का कारण बनती है। अधिकांश प्रोग्रामिंग त्रुटियाँ🙅‍♂️ त्रुटियों के कारण उत्पन्न होते हैं🙅‍♂️, कार्यक्रम के डेवलपर्स द्वारा इसके स्रोत कोड में अनुमति दी गई है📟, या इसके डिजाइन में।

![error](https://media.giphy.com/media/1VT3UNeWdijUSMpRL4/giphy.gif)

"मायावी तकनीकी त्रुटि के अर्थ में🙅‍♂️» शब्द "बग" (अंग्रेज़ी. bug) कंप्यूटर के आगमन से बहुत पहले इस्तेमाल किया🖥️ बिजली के उपकरणों और रेडियो उपकरणों के साथ समस्याओं के बारे में टेलीग्राफ और टेलीफोन कंपनियों के कर्मियों। 1878 में थॉमस एडिसन ने लिखा:

> «मेरे सभी आविष्कारों का यही हाल था। 1️⃣ पहला कदम अंतर्ज्ञान है, जो एक फ्लैश की तरह आता है, फिर कठिनाइयां पैदा होती हैं - डिवाइस काम करने से इनकार करता है, और जब बग दिखाई देते हैं - जैसा कि इन छोटी गलतियों और कठिनाइयों को कहा जाता है - और इससे पहले अवलोकन, अनुसंधान और प्रयास में महीनों लगते हैं। यह व्यावसायिक सफलता या विफलता की बात आती है। ”

डिबगिंग त्रुटियों को खोजने और ठीक करने की प्रक्रिया है🙅‍♂️ स्क्रिप्ट में।

[Wikipedia](https://ru.wikipedia.org/wiki/Программная_ошибка🙅‍♂️)

## वीडियो

<YouTube videoId="xJtVop2fAxg" />

## सबसे आम गलतियाँ

![Teacher](https://media.giphy.com/media/27c3zdaY6eeIAwp7Qi/giphy.gif)

मुझे आशा है कि आप अपनी पहली गलतियों को पूरा कर चुके हैं।🙅‍♂️ कोड लिखने की प्रक्रिया में। मुझे उम्मीद क्यों है? क्योंकि गलतियाँ🙅‍♂️ - ये हमारे शिक्षक हैं जो हमें दिखाते हैं कि हम अपने कोड में क्या गलत कर रहे हैं📟 और कंप्यूटर🖥️, अधिक सटीक एक कोड दुभाषिया📟, हम बस समझ नहीं सकते। त्रुटियाँ🙅‍♂️ कोड लिखते समय📟 लगभग हर दिन होता है। संदेश पढ़ने के लिए ट्रिक सक्षम होना चाहिए।💬 त्रुटि के बारे में🙅‍♂️, जो मशीन आपको देगी🚗, लिखित कोड में दोष खोजने और ठीक करने के लिए📟. जितना अधिक आप अध्ययन करेंगे JavaScript, जितना अधिक आप संदेशों की सराहना करते हैं💬 गलतियों के बारे में🙅‍♂️ - वे अक्सर बहुत सटीक दिखाते हैं कि आप कहां गलत थे।

सबसे सामान्य प्रकार की त्रुटियों की एक जोड़ी🙅‍♂️ कोड में📟:

## SyntaxError

![Error](https://media.giphy.com/media/TqiwHbFBaZ4ti/giphy.gif)

`Syntax Error` - भाषा के नियमों का उल्लंघन👅. उदाहरण के लिए, नौ प्लस एक अर्धविराम दर्ज करें `9 + ;`👇:

```jsx live
function learnJavaScript() {
  var error = 9

  return error
}
```

उत्तर: `SyntaxError: Unexpected token ;`

वक्य रचना त्रुटि🙅‍♂️, बस इसका मतलब है कि आपके वाक्य के शरीर में कोई त्रुटि है🙅‍♂️. दूसरे शब्दों में, आपने जो लिखा है वह भाषा के संदर्भ में सही नहीं है।👅 JavaScript. दुभाषिया आपके वाक्य को नहीं पढ़ सकता है और यह नहीं जानता है कि इसके साथ क्या करना है। `Unexpected token ;` इसका मतलब है कि दुभाषिया ने कुछ ऐसा पढ़ा है कि वह बिल्कुल भी पढ़ने की उम्मीद नहीं करता था: हमारे मामले में, अर्धविराम `;`.

हम फिर से गलत होंगे🙅‍♂️!
आइए सांत्वना पाँच प्लस तीन और अंत में एक कोष्ठक में दर्ज करें `5+3)`.

```jsx live
function learnJavaScript() {
  var error = 5

  return error
}
```

आपके पास एक समापन कोष्ठक है `)`, लेकिन कोई ओपनिंग कोष्ठक नहीं है `(`! लेकिन कोष्ठक हमेशा जोड़े में जाते हैं - ऐसा नहीं हो सकता है कि एक समापन है, लेकिन कोई उद्घाटन कोष्ठक नहीं है, और इसके विपरीत।

## ReferenceError

![Error](https://media.giphy.com/media/8L0Pky6C83SzkzU55a/giphy.gif)

`ReferenceError` - गलत नाम! एक वस्तु `ReferenceError` एक त्रुटि प्रस्तुत करता है🙅‍♂️, जिक्र करते समय उठता है अस्तित्वहीन चर। उदाहरण के लिए, पांच प्लस बारी बारी से दर्ज करें `5 + परिवर्तनशील`:

```jsx live
function learnJavaScript() {
  var error = 5

  return error
}
```

अब हमसे गलती हो गई `ReferenceError`. शायद आपने पहले ही ध्यान दिया हो कि यहाँ क्या मामला है? संदेश को ध्यान से पढ़ें।💬 एक त्रुटि के बारे में (आखिरकार, इसके लिए, अंत में, यह जारी किया जाता है!)। यह कहता है: `चर 🔔 is not defined` — चर सेट नहीं है, यह वह जगह है जहाँ हमारी समस्या है! हमें पहले घोषणा करनी चाहिए🗣️ किसी तरह से एक चर, इस तरह से कहें:

```jsx live
function learnJavaScript() {
  var परिवर्तनशील = 5
  var error = 5 + परिवर्तनशील

  return error
}
```

## TypeError

एक वस्तु TypeError एक त्रुटि का प्रतिनिधित्व करता है जब एक मान अपेक्षित प्रकार का नहीं होता है। हम विधि लागू करते हैं `toUpperCase`, जिसे हम बाद में विस्तार से जानने के लिए टाइप करेंगे undefined, लेकिन यह मान्य नहीं है क्योंकि यह विधि स्ट्रिंग को अपरकेस में परिवर्तित करती है। ब्राउज़र कंसोल में इस त्रुटि की जाँच करें, इसलिए `LIVE EDITOR` वह काम नहीं करती।

```javascript
var foo = undefined
foo.toUpperCase()
```

![TypeError](/img/javascript/25.jpg)

## मदद

हम गलतियाँ भी कर सकते हैं, इसलिए यदि आप साइट पर कोई त्रुटि पाते हैं या गलत अनुवाद करते हैं, तो आप आसानी से साइट पर त्रुटि को ठीक करने में मदद कर सकते हैं। ऐसा करने के लिए, आपको बटन पर क्लिक करने की आवश्यकता है `Edit this page` हर पृष्ठ के बहुत नीचे।

## समस्या?

![Problem](https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif)

को लिखना [Discord](https://discord.gg/6GDAfXn) या टेलीग्राम [चैट](https://t.me/jscampapp), और हमारी सदस्यता भी लें [समाचार](https://t.me/javascriptapp)

## प्रशन:

![Question](https://media.giphy.com/media/l0HlRnAWXxn0MhKLK/giphy.gif)

क्या करता है `Syntax Error`?

1. संकेतों का गलत क्रम
2. भाषा के नियमों का उल्लंघन
3. अनुचित कोष्ठक

क्या करता है `Reference Error`?

1. अघोषित चर
2. सिंटैक्स त्रुटि
3. गलत नाम
यह समझने के लिए कि आपने इस पाठ को कितना सीखा है, परीक्षा को अंदर लें [जिस स्थिति में ऑपरेटर रिटर्न नहीं के बराबर देता है](http://onelink.to/njhc95) इस विषय पर हमारा स्कूल।

![Sumerian school](/img/app.jpg)

## लिंक:

1. [MDN web docs](https://developer.mozilla.org/ru/docs/Web/JavaScript/Data_structures)
2. [किशोर के लिए कोड: प्रोग्रामिंग के लिए एकदम सही शुरुआत की गाइड, वॉल्यूम 1: Javascript - Jeremy Moritz ](https://www.amazon.com/Code-Teens-Beginners-Programming-Javascript-ebook/dp/B07FCTLVPC)
3. [JavaScript.ru](https://learn.javascript.ru/types)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<table>
  <tr>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /> <a href="https://github.com/gHashTag/react-native-village/commits?author=gHashTag" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/Resoner2005"><img src="https://avatars1.githubusercontent.com/u/75675814?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Resoner2005</b></sub></a><br /><a href="https://github.com/gHashTag/react-native-village/issues?q=author%3AResoner2005" title="Bug reports">🐛 🎨 🖋</a></td>
  </tr>
  
</table>

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)
