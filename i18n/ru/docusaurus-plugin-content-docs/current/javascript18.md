---
id: javascript18
title: Операторы Rest и Spread
sidebar_label: Операторы Rest и Spread
---

import YouTube from 'react-youtube'

![@serverSerrverlesskiy](/img/javascript/headers/19.jpg)

Многие встроенные функции⚙️ JavaScript поддерживают произвольное количество аргументов.

Например:

`Math.max(arg1, arg2, ..., argN)` – вычисляет максимальное число из переданных аргументов.

`Math.min(arg1, arg2, ..., argN)` - возвращает🔄 минимальное значение из переданных аргументов.

В этой статье мы узнаем, как сделать то же самое с нашими собственными функциями⚙️ и как передавать таким функциям⚙️ параметры в виде массива.

## Видео

<YouTube videoId="X4JepTP9zbk" />

## Остаточные параметры `(...rest)`

![Parametrs](https://media.giphy.com/media/3osxYoufeOGOA7xiX6/giphy.gif)

Вызывать функцию⚙️ можно с любым количеством аргументов независимо от того, как она была определена.

Например 👇 :

```jsx live
function learnJavaScript() {
  let summa = (a, b, c) => {
    return a + b + c
  } // Сумма 3-х чисел

  return summa(1, 2, 3, 4, 5, 6, 7)
}
```

Лишние аргументы не вызовут ошибку, но конечно посчитаются только первые три.

<!-- ### Концепция ES6

![Idea](https://media.giphy.com/media/3o6Mbj2w67HnPQKgcE/giphy.gif)

Начиная со стандарта ES6 появилась концепция, как `...rest` - остаточные параметры.

```jsx
let goFun = (...rest) => {
  // Алгоритм
}
```

Свободные параметры могут быть обозначены через три точки `...`. Буквально это значит: "собери оставшиеся параметры и положи их в массив".

Например, соберём все аргументы в массив `args`👇 :

```jsx live
function learnJavaScript() {
  let sumAll = (...args) => {
    // args — имя массива передаваемых аргументов
    let sum = 0
    for (let arg of args) if (typeof arg === 'number') sum += arg // sum - соберется сумма всех числовых аргументов
    return sum
  }
  return sumAll(1, 2, 3, 4, 5, 6, 7, 'React', 'Native')
}
```

Ответ уже 28 и без ошибок🙅‍♂️! Подробуйте изменить аргументы или размерность массива.

### Несколько параметров

Мы можем положить первые несколько параметров в переменные 🔔 , а остальные – собрать в массив.
Это означает то, что вы просто можете вставить `...rest`, но только вместо последнего параметра функции.

![paste](https://media.giphy.com/media/3o6ZtafpgSpvIaKhMI/giphy.gif)

```jsx
let goFun = (first, second, ...rest) => {
  // Алгоритм
}
```

В примере ниже первые два2️⃣ аргумента функции станут именем и фамилией, а третий и последующие превратятся в массив `titles[i]` 👇 :

```jsx live
function learnJavaScript() {
  let free = ''
  let showName = (firstName, lastName, ...titles) => {
    free = firstName + ' ' + lastName // Имя + Фамилия
    return titles[0] + ' ' + titles[1]
  }
  // Оставшиеся параметры пойдут в массив titles = ["React", "Native"]
  // titles[0]  // React
  // titles[1]  // Native

  let result = showName('Юлий', 'Цезарь', 'React', 'Native')

  return free + ' или ' + result
}
```

### Возможные ошибки

![error](https://media.giphy.com/media/xTiN0L7EW5trfOvEk0/giphy.gif)

Остаточные параметры должны располагаться в конце, поэтому нельзя писать 🖊️ что-либо после них.
Это вызовет `ошибку`:

```jsx
function f(arg1, ...rest, arg2) {   // arg2 после ...rest ?
  // Ошибка!
}
```

:::note Запомни
`...rest` должен всегда быть последним.
:::

<!-- ### Опасный "arguments"

![dangerous](https://media.giphy.com/media/xT5LMAvRY92qUXj7dC/giphy.gif)

Все аргументы функции⚙️ находятся в псевдомассиве `arguments` под своими порядковыми номерами.

Но доступ через массив `arguments[]` можно найти только в старом коде📟 . Не применяйте его!

:::note Внимание
Cтрелочные функции⚙️ не имеют `arguments[]` как и собственного `this.`
:::

Если мы обратимся к `arguments` из стрелочной функции⚙️, то получим аргументы внешней "классической" функции⚙️. Соответственно, для более удобной работы с аргументами лучше использовать только остаточные параметры `...rest`. -->



## Оплата

Сейчас ты находишся на урезанной версии сайта, после оформления подписки на [Patreon](https://www.patreon.com/javascriptcamp), ты получишь полный доступ к обучающему курсу, а также доступ к серетным каналам нашего сервера в [Discord](https://discord.gg/6GDAfXn).  

Качай наше [мобильное приложение](http://onelink.to/njhc95) или пройди тестирование в нашем [JavaScript телеграм боте](https://t.me/javascriptcamp_bot), а также подпишись на [наши новости](https://t.me/javascriptapp).

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)


[![Sumerian school](/img/app.jpg)](http://onelink.to/njhc95)

 

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

<!--
Например:
```jsx
function showName() {
  console.log( arguments.length )
  console.log( arguments[0] )
  console.log( arguments[1] )

  // Объект arguments можно перебирать
  // for (let arg of arguments) console.log(arg)
}

// Вывод: 2, Юлий, Цезарь
showName("Юлий", "Цезарь")

// Вывод: 1, Илья, undefined (второго аргумента нет)
showName("Илья")
```
Раньше в языке не было остаточных параметров, и получить все аргументы функции можно было только с помощью arguments. Этот способ всё ещё работает, мы можем найти его в старом коде.
Но у него есть один недостаток. Хотя arguments похож на массив, и его тоже можно перебирать, это всё же не массив. Он не поддерживает методы массивов, поэтому мы не можем, например, вызвать arguments.map(...).
К тому же, arguments всегда содержит все аргументы функции — мы не можем получить их часть. А остаточные параметры позволяют это сделать.
Соответственно, для более удобной работы с аргументами лучше использовать остаточные параметры.
-->

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)