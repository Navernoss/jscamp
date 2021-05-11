---
id: javascript28
title: Async Await
sidebar_label: Async Await
---

import YouTube from 'react-youtube'

![@serverSerrverlesskiy](/img/javascript/headers/29.jpg)

Существует специальный синтаксис 📖 для работы с промисами, который называется `async/await`.

## Создание асинхронной функции

![creature](https://media.giphy.com/media/4T7e4DmcrP9du/giphy.gif)

Асинхронная функция⚙️ определяется выражением асинхронной функции⚙️. Базовая функция⚙️ выглядит так:

```javascript
async function foo() {
  const value = await somePromise()
  return value
}
```

Мы определяем функцию⚙️ как асинхронную с помощью `async`. Это ключевое🗝️ слово может использоваться с любым синтаксисом📖 объявления🗣️ функции⚙️:

```javascript
// Function Declaration
async function foo() { ... }

// Function Expression
const foo = async function () { ... }

// Arrow function
const foo = async () => { ... }

// Class methods
class Bar {
    async foo() { ... }
}
```

![Stops](https://media.giphy.com/media/WrgAGkGrh0MD1Z2gkO/giphy.gif)

Как только мы определили функцию⚙️ как асинхронную, мы можем использовать ключевое🗝️ слово `await`.
Это ключевое🗝️ слово помещается перед вызовом промиса, оно приостанавливает выполнение функции⚙️ до тех пор, пока промис не будет выполнен или отклонён.

## Видео

<YouTube videoId="I0t9dwZ4ST8" />

<!-- ## Async

![run](https://media.giphy.com/media/3N0fFF5xxcZrO/giphy.gif)

У нас есть ключевое🗝️ слово `async`, которое мы помещаем перед объявлением🗣️ функции⚙️, чтобы сделать ее асинхронной. Асинхронная функция⚙️ — это функция⚙️, которая предвосхищает возможность использования ключевого🗝️ слова `await` для запуска асинхронного кода📟 .

Попробуйте набрать в консоли браузера следующее:

```javascript
function hello() {
  return 'Hello'
}
hello()
```

Функция⚙️ вернет 'Hello'. Ничего необычного.

Но что если мы превратим ее в асинхронную функцию⚙️? Попробуйте сделать следующее:

```javascript
async function hello() {
  return 'Hello'
}
hello()
```

![Promise](https://media.giphy.com/media/GFtJhEvG3681y/giphy.gif)

Теперь вызов функции⚙️ возвращает🔄 обещание. Это одна из особенностей асинхронных функций⚙️ — они возвращают🔄 значения, которые гарантировано преобразуются в обещания.

Вы также можете создать🏗️ асинхронное функциональное⚙️ выражение, например, так:

```javascript
// Function Expression
let hello = async function () {
  return hello()
}
hello()
```

Также можно использовать стрелочные функции⚙️:

```javascript
let hello = async () => {
  return 'Hello'
}
```

Все эти функции⚙️ делают одно и тоже.

Для того, чтобы получить значение завершенного обещания, мы можем использовать блок `.then()`:

```javascript
hello().then(value => console.log(value))
```

… или даже так:

```javascript
hello().then(console.log)
```

Таким образом, добавление ключевого🗝️ слова `async` заставляет функцию⚙️ возвращать🔄 обещание вместо значения. Кроме того, это позволяет синхронным функциям избегать любых накладных расходов, связанных с запуском и поддержкой использования `await`. Простое добавление `async` перед функцией⚙️ обеспечивает автоматическую оптимизацию кода📟 движком JS.

## Await

![Wait](https://media.giphy.com/media/myPdoRAlad0J2/giphy.gif)

Преимущества асинхронных функций⚙️ становятся еще более очевидными, когда вы комбинируете их с ключевым🗝️ словом `await`. Оно может быть добавлено перед любой основанной на обещаниях функцией⚙️, чтобы заставить ее дожидаться завершения обещания, а затем вернуть результат. После этого выполняется следующий блок кода📟 .

Вы можете использовать `await` при вызове любой функции⚙️, возвращающей🔄 обещание, включая функции⚙️ `Web API`.

Синтаксис📖:

```javascript
let response = await fetch('https://jsonplaceholder.typicode.com/users')
let data = await response.json()
console.log(data[0].name + ' and ' + data[2].name)
```

## Обработка ошибок с `try...catch`

![code rewriting](https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif)

Если вы хотите добавить обработку ошибок, у вас есть несколько вариантов.

Вы можете использовать синхронную структуру `try...catch` вместе с `async/await`:

```javascript
async function myFetch() {
  try {
    let response = await fetch('https://jsonplaceholder.typicode.com/users')
    let data = await response.json()
    console.log(data[0].name + ' and ' + data[2].name)
  } catch (e) {
    console.log(e)
  }
}

myFetch()
```

Блок `catch(){}` принимает объект ошибки🙅‍♂️, который мы назвали `e`. Теперь мы можем вывести его в консоль, это позволит нам получить сообщение💬 о том, в каком месте кода📟 произошла ошибка🙅‍♂️.

Целенаправленно создадим ошибку в `url` и посмотрим на вывод ошибки.

```javascript
async function myFetch() {
  try {
    let response = await fetch('https://jsonplaceholder.typicode.com/sers')
    let data = await response.json()
    console.log(data[0].name + ' and ' + data[2].name)
  } catch (e) {
    console.log(e)
  }
}

myFetch()
```

![fetch error](/img/javascript/17.jpg)

## Итого

![Conclusion](https://media.giphy.com/media/3o6ZsVl2hv8ZnhSXug/giphy.gif)

`Async/await` позволяет писать 🖊️ асинхронный код, который легко читать и поддерживать. Шесть причин почему его лучше использовать вместо промисов читайте [здесь](https://habr.com/ru/company/ruvds/blog/326074/).

## Проблемы?

![Problem](https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif)

Пишите в [Discord](https://discord.gg/6GDAfXn) или телеграмм [чат](https://t.me/jscampapp), а также подписывайтесь на наши [новости](https://t.me/javascriptapp)

![JavaScript Camp](/img/bandlink.png)


## Вопросы:

![Question](https://media.giphy.com/media/l0HlRnAWXxn0MhKLK/giphy.gif)

Где помещается ключевое слово `async`?

1. Перед объявлением функции
2. После объявления функции
3. В теле функции

В каких функциях работает `await`?

1. Только в синхронных функциях
2. Только в асинхронных функциях
3. В любых функциях

Асинхронная функция - это:

1. Это функция, которая определяется ключевым словом `async`
2. Это функция, которая предвосхищает возможность использования ключевого слова `await`
3. Оба варианта верны

Преимуществом `async/await` является:

1. Собственный код является заблокированным
2. Лаконичный и чистый код

Для того чтобы понять, на сколько вы усвоили этот урок, пройдите тест в [мобильном приложении](http://onelink.to/njhc95) нашей школы по этой теме или в нашем [телеграм боте](https://t.me/javascriptcamp_bot).

![Sumerian school](/img/app.jpg)

## Ссылки:

1. [Async-await](https://learn.javascript.ru/async-await)
2. [Как освоить Async / Await в JavaScript на реальных примерах](https://webformyself.com/async-await-v-javascript-na-primerax)
3. [Асинхронное программирование с async/await](https://habr.com/ru/post/491012/) -->

## Оплата

Сейчас ты находишся на урезанной версии сайта, после оформления подписки на [Patreon](https://www.patreon.com/javascriptcamp), ты получишь полный доступ к обучающему курсу, а также доступ к серетным каналам нашего сервера в [Discord](https://discord.gg/6GDAfXn).  

Качай наше [мобильное приложение](http://onelink.to/njhc95) или пройди тестирование в нашем [JavaScript телеграм боте](https://t.me/javascriptcamp_bot), а также подпишитесь на [наши новости](https://t.me/javascriptapp).

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
    <td align="center"><a href="https://github.com/AlisaNasibullina"><img src="https://avatars3.githubusercontent.com/u/74646904?s=460&v=4" width="200px;" alt=""/><br /><sub><b>AlisaNasibullina</b></sub></a><br /><a href="#mentoring-KoDim-React" title="Mentoring">📖</a></td>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /><a href="#financial-gHashTag" title="Financial">💵</a></td>
    <td align="center"><a href="https://github.com/Resoner2005"><img src="https://avatars1.githubusercontent.com/u/75675814?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Resoner2005</b></sub></a><br /><a href="https://github.com/gHashTag/react-native-village/issues?q=author%3AResoner2005" title="Bug reports">🐛 🎨 </a></td>
  </tr>
</table>

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)
