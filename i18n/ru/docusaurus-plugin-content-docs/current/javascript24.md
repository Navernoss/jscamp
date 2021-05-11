---
id: javascript24
title: Запрет на "this"
sidebar_label: Запрет на "this"
---

import YouTube from 'react-youtube'

![@serverSerrverlesskiy](/img/javascript/headers/24.jpg)

Удаление ключевого🗝️ слова `this` из JavaScript делает язык👅 лучше!

Причина в том, что `this` зависит от того, как была вызвана функция⚙️, а не от того, где она была определена. Поэтому `this` в JavaScript является источником большой путаницы в языке👅.

Использование `this` гарантирует, что функция работает именно с тем объектом, в контексте которого вызвана.
Через `this` метод можно не только обратиться к любому свойству объекта, но и передать куда-то ссылку на сам объект целиком (снижая безопасность приложения).

Значение `this` называется контекстом вызова и будет определено в момент вызова функции. Например, такая функция, объявленная без объекта, вполне допустима:

```javascript
functionsay Hi() {
  console.log(this.firstName)
}
```

Эта функция ещё не знает, каким будет `this`. Это выяснится при выполнении программы.

Если одну и ту же функцию запускать в контексте разных объектов, она будет получать разный `this`:

```javascript
var user = { firstName: 'Джони' }
var admin = { firstName: 'Админ' }

function funcName() {
  console.log(this.firstName)
}
user.f = funcName
admin.g = funcName

//this равен объекту перед точкой:
user.f() //Джони
admin.g() //Админ
admin['g']() //Админ (доступ к объект реализован через квадратные скобки)
```

Итак, значение `this` не зависит от того, как функция была создана, оно определяется исключительно в момент вызова.

## Видео

<YouTube videoId="4GR2KQwqa98" /> 

<!-- ## `this` и его недостатки

Методы — это функции⚙️, которые хранятся в объектах. Для того, чтобы функция⚙️ знала, над каким объектом работать, используется `this.`

![Poor](https://media.giphy.com/media/fQJbwrRJdHyMOP7RPH/giphy.gif)

Но `this` теряет контекст во многих ситуациях (неизвестно возвращаемое🔄 значение):

- теряет контекст внутри вложенных функций
- теряет контекст в обратных вызовах (callback)
- `this` теряет контекст, когда метод используется в качестве обработчика события.


## Лучший язык

![The_best](https://media.giphy.com/media/ZBn3ZRvCbWz2PS3Rbg/giphy.gif)

JavaScript — это и функциональный язык программирования, и язык на основе прототипов. Если мы избавимся от `this`, у нас останется JavaScript как функциональный⚙️ язык👅 программирования. Это даже лучше!

В то же время, без `this` JavaScript предлагает 🆕 новый, уникальный способ выполнения объектно-ориентированного программирования без классов и наследования.


## Отказ от this

![remember](https://media.giphy.com/media/S52I9r5QfB4fIBS6WV/giphy.gif)

Лучший способ избежать связанных с `this` проблем — вообще не использовать `this`!

:::note JavaScript
JavaScript без this выглядит как лучший функциональный⚙️ язык👅 программирования!
:::

Мы можем создавать🏗️ инкапсулированные объекты без использования `this` в качестве коллекций закрытий. С помощью [React Hooks](https://ru.reactjs.org/docs/hooks-intro.html) мы можем создавать🏗️ без `this` компоненты с сохранением состояния.

Ключевое слово `this` не может быть удалено из JavaScript, без разрушения всех существующих приложений. Однако что можно сделать? Мы можем написать 🖊️ собственный код без `this` и позволить его использовать только в библиотеках. Тем временем вводятся [новые правила](https://ru.reactjs.org/docs/hooks-rules.html#eslint-plugin) `ESLint,` запрещающие использование `this`.

Так как в прошлом уроке мы отказались от [классов](https://react-native-village.github.io/docs/javascript25#отказ-от-классов), то и вместе с ними прощаемся и с `this`.

## Проблемы?

![Problem](https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif)

Пишите в [Discord](https://discord.gg/6GDAfXn) или телеграмм [чат](https://t.me/jscampapp), а также подписывайтесь на наши [новости](https://t.me/javascriptapp)

![JavaScript Camp](/img/bandlink.png)

## Вопросы

![Question](https://media.giphy.com/media/l0HlRnAWXxn0MhKLK/giphy.gif)

Можно ли обойтись без `this`:

1. Можно, и лучше вообще не использовать
2. Можно, но не целесообразно
3. Нельзя, т.к. `this` не может быть удален из JavaScript

JavaScript без `this` выглядит как лучший:

1. Функциональный язык программирования
2. Процедурный язык программирования
3. Логический язык программирования

Для того чтобы понять, на сколько вы усвоили этот урок, пройдите тест в [мобильном приложении](http://onelink.to/njhc95) нашей школы по этой теме или в нашем [телеграм боте](https://t.me/javascriptcamp_bot).

![Sumerian school](/img/app.jpg)

## Ссылки

1. [Статья "Удаление ключевого слова «this» из JavaScript делает язык лучше"](https://webformyself.com/udalenie-klyuchevogo-slova-this-iz-javascript/)
2. [Статья "Ключевое слово this в JavaScript"](https://habr.com/ru/post/464163/)
3. [MDN web doc. Статья "this"](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/this) -->

## Оплата

Сейчас ты находишся на урезанной версии сайта, после оформления подписки на [Patreon](https://www.patreon.com/javascriptcamp), ты получишь полный доступ к обучающему курсу, а также доступ к серетным каналам нашего сервера в [Discord](https://discord.gg/6GDAfXn).  

Качай наше [мобильное приложение](http://onelink.to/njhc95) или пройди тестирование в нашем [JavaScript телеграм боте](https://t.me/javascriptcamp_bot), а также подпишись на [наши новости](https://t.me/javascriptapp).

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)


[![Sumerian school](/img/app.jpg)](http://onelink.to/njhc95)

![JavaScript Camp](/img/bandlink.png)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/KoDim-React"><img src="https://avatars1.githubusercontent.com/u/72087863?v=4?s=200" width="200px " alt=""/><br /><sub><b>Dmitriy K.</b></sub></a><br /><a href="#mentoring-KoDim-React" title="Mentoring">📖</a></td>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px " alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /><a href="#financial-gHashTag" title="Financial">💵</a></td>
    <td align="center"><a href="https://github.com/Resoner2005"><img src="https://avatars1.githubusercontent.com/u/75675814?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Resoner2005</b></sub></a><br /><a href="https://github.com/gHashTag/react-native-village/issues?q=author%3AResoner2005" title="Bug reports">🐛 🎨 🖋</a></td>
    <td align="center"><a href="https://github.com/Navernoss"><img src="https://avatars0.githubusercontent.com/u/75784137?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Navernoss</b></sub></a><br /><a href="#content-Navernoss" title="Content">🖋 🐛 🎨 </a></td>
  </tr>
  
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)
