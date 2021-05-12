---
id: javascript05
title: Errors
sidebar_label: Errors
---

import YouTube from 'react-youtube'

![@serverSerrverlesskiy](/img/javascript/headers/05.jpg)

You will definitely, like the rest of us, make mistakes🙅‍♂️ in the code📟. Software bugs🙅‍♂️ are called bugs. Bug - means an error🙅‍♂️ in the program💾 or in the system, due to which the program produces unexpected behavior and, as a result, the result. Most software errors🙅‍♂️ arise from errors🙅‍♂️ made by program developers in its source code📟 or in its design.

![error](https://media.giphy.com/media/1VT3UNeWdijUSMpRL4/giphy.gif)

In the meaning of "elusive technical error", the word "bug" was used long before the advent of computers by the staff of telegraph and telephone companies in relation to problems with electrical equipment and radio equipment. In 1878, Thomas Edison wrote:

> “This was the case with all my inventions. 1️⃣ The first step is intuition, which comes like a flash, then difficulties arise - the device refuses to work, and that's when the bugs appear - as these small mistakes and difficulties are called - and it takes months of close observation, research and effort before it comes to commercial success or failure. "

Debugging is the process of finding and fixing errors🙅‍♂️ in a script.

[Wikipedia](https://ru.wikipedia.org/wiki/Программная_ошибка🙅‍♂️)

<!-- ## Video

<YouTube videoId="xJtVop2fAxg" /> -->

## The most common mistakes

![Teacher](https://media.giphy.com/media/27c3zdaY6eeIAwp7Qi/giphy.gif)

I hope you have already encountered your first mistakes🙅‍♂️ in the process of writing code. Why hope? Because mistakes🙅‍♂️ are our teachers who show us what we do wrong in our code📟 and a computer🖥️, or rather a code interpreter📟, simply cannot understand us. Mistakes🙅‍♂️ when writing code📟 happen almost every day. The trick is to be able to read the error message💬 that the machine will give you in order to quickly find and fix a defect in the written code📟. The more you learn JavaScript, the more you appreciate the error messages💬 - they often show very accurately where you went wrong.

A couple of the most common error types🙅‍♂️ in code код:

## SyntaxError

![Error](https://media.giphy.com/media/TqiwHbFBaZ4ti/giphy.gif)

`Syntax Error` - violation of language rules правил. For example, enter nine plus a semicolon `9 +;` 👇:

```jsx live
function learnJavaScript() {
  var error = 9

  return error
}
```

Reply: `SyntaxError: Unexpected token;`

A syntax error🙅‍♂️ simply means that there is an error in the body of your sentence🙅‍♂️. In other words, what you wrote is not correct in terms of JavaScript. The interpreter cannot read your sentence and does not know what to do with it. `Unexpected token;` means that the interpreter has read something that it did not expect to read at all: in our case, a semicolon `;`.

Let's make a mistake again🙅‍♂️!
Let's enter five plus three in the console and a parenthesis at the end of `5 + 3)`.

```jsx live
function learnJavaScript() {
  var error = 5

  return error
}
```

You have a closing parenthesis `)`, but there is no opening parenthesis `(`! But the parentheses always go in pairs - it cannot be that there is a closing, but there is no opening parenthesis, and vice versa.

## Payment

Now you are on a stripped-down version of the site, after subscribing to [Patreon](https://www.patreon.com/javascriptcamp), you will get full access to the training course, as well as access to our server's private channels in [Discord](https://discord.gg/6GDAfXn).

Download our [mobile application](http://onelink.to/njhc95) or get tested in our [JavaScript telegram bot](https://t.me/javascriptcamp_bot), and also subscribe to [our news](https://t.me/javascriptapp).

[![Become a Patron!](/Img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)


[![Sumerian school](/img/app.jpg)](http://onelink.to/njhc95)

![JavaScript Camp](/img/bandlink.png)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<table>
  <tr>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /> <a href="https://github.com/gHashTag/react-native-village/commits?author=gHashTag" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/Resoner2005"><img src="https://avatars1.githubusercontent.com/u/75675814?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Resoner2005</b></sub></a><br /><a href="https://github.com/gHashTag/react-native-village/issues?q=author%3AResoner2005" title="Bug reports">🐛 🎨 🖋</a></td>
  </tr>
  
</table>

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)
