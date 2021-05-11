---
id: typescript09
title: Декларации
sidebar_label: Декларации
---

Декларации это очень важная часть TypeScript благодаря которой статическая типизация проецируется на динамический JavaScript.

![Space](https://media.giphy.com/media/RkHrSGDmPCb7QSwDYz/giphy.gif)

## Declaration

Поскольку при разработке программ на TypeScript используются библиотеки написанные на JavaScript, компилятор `tsc`, чьей главной задачей является проверка типов, чувствует себя будто у него завязаны глаза. Несмотря на то, что с каждой новой версией вывод типов все лучше и лучше учится разбирать JavaScript, но до идеала ещё далеко. Кроме того, разбор JavaScript кода добавляет нагрузку на процессор, драгоценного время которого при разработке современных приложений, порой и так не достаточно.

TypeScript решил эту проблему за счет подключения к проекту заранее сгенерированных им или создаваемых вручную разработчиками деклараций. Декларации размещаются в файлах с расширением `.d.ts` и состоят только из объявлений типов полностью повторяющих программу до момента компиляции при которой она была лишена всех признаков типизации. Их действие во многом похоже на работу файлов с расширением `.h` в языках C/C++.

```ts
// Файл Animal.ts
export default class Animal {
  public name: string = 'animal'
  public voice(): void {}
}

// Файл Animal.d.ts
declare module 'Animal' {
  export default class Animal {
    name: string
    voice(): void
  }
}
```



## Оплата

Сейчас ты находишся на урезанной версии сайта, после оформления подписки на [Patreon](https://www.patreon.com/javascriptcamp), ты получишь полный доступ к обучающему курсу, а также доступ к серетным каналам нашего сервера в [Discord](https://discord.gg/6GDAfXn).  

Качай наше [мобильное приложение](http://onelink.to/njhc95) или пройди тестирование в нашем [JavaScript телеграм боте](https://t.me/javascriptcamp_bot), а также подпишитесь на [наши новости](https://t.me/javascriptapp).


[![Sumerian school](/img/app.jpg)](http://onelink.to/njhc95)

![JavaScript Camp](/img/bandlink.png)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<table>
  <tr> 
    <td align="center"><a href="https://github.com/IIo3iTiv"><img src="https://avatars1.githubusercontent.com/u/72025062?v=4?s=200" width="200px;" alt=""/><br /><sub><b>IIo3iTiv</b></sub></a><br /><a href="https://github.com/gHashTag/react-native-village/commits?author=IIo3iTiv" title="Documentation">📖</a></td>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /><a href="#financial-gHashTag" title="Financial">💵</a></td>
  </tr>
</table>

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)
