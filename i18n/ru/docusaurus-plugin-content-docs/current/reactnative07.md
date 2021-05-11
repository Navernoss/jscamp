---
id: reactnative07
title: Элемент форм - TextInput
sidebar_label: Элемент форм - TextInput
---

import YouTube from 'react-youtube'

## TextInput

`TextInput` - это основной компонент, который позволяет пользователю вводить текст. Это базовый компонент для ввода текста в приложение с клавиатуры. Props предоставляет возможность настройки для нескольких функций, таких как автокоррекция, автоматический ввод заглавных букв, placeholder-текст и различные типы клавиатуры, например такие как цифровая клавиатура. У него есть свойство `onChangeText`, которое принимает функцию, вызываемую каждый раз при изменении текста, и свойство `onSubmitEditing`, которое принимает функцию, вызываемую при отправке текста. Пока не обращайте внимание на хук `useState`, он используется для изменения состояния приложения, с ним мы познакомимся ближе в следующих сериях.

```SnackPlayer name=index.js
import React, { useState } from 'react'
import { Text, TextInput, View } from 'react-native'

const PizzaTranslator = () => {
  const [text, setText] = useState('')
  return (
    <View style={{padding: 10}}>
      <TextInput
        style={{height: 40}}
        placeholder="Введите здесь, чтобы перевести!"
        onChangeText={text => setText(text)}
        defaultValue={text}
      />
    </View>
  )
}

export default PizzaTranslator
```

В этом примере мы сохраняем текст в состоянии, потому что он изменяется со временем.

Есть еще много вещей, которые вы можете сделать с вводом текста. Например, вы можете проверить текст внутри, пока пользователь печатает. Более подробные примеры смотри в справочной документации по [TextInput](https://reactnative.dev/docs/textinput).

Ввод текста - это один из способов взаимодействия пользователя с приложением. Затем давайте посмотрим на другой тип ввода и узнаем, как обрабатывать прикосновения.


<!-- ## Проблемы?

![Problem](https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif)

Пишите в [Discord](https://discord.gg/6GDAfXn) или телеграмм [чат](https://t.me/jscampapp), а также подписывайтесь на наши [новости](https://t.me/javascriptapp)

![JavaScript Camp](/img/bandlink.png)

## Вопросы

Основной компонент, который позволяет пользователю вводить текст?

1. Text
2. TextInput
3. Input

Как называется свойство у компонент TextInput, которое принимает функцию, вызываемую каждый раз при изменении текста?

1. `onSubmitEditing`
2. `onChange`
3. `onChangeText`

Как называется свойство у компонент TextInput, которое принимает функцию, вызываемую при отправке текста?

1. `onSubmitEditing`
2. `onChange`
3. `onChangeText`

## Done ✅

Чтобы узнать, насколько хорошо вы усвоили этот урок, пройдите тест в [мобильном приложении](http://onelink.to/njhc95) нашей школы по этой теме или в [боте Telegram](https://t.me/javascriptcamp_bot).

![Sumerian school](/img/app.jpg)

## Ссылки:

1. [React Native](https://reactnative.dev/docs/handling-text-input)

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291) -->

## Оплата

Сейчас ты находишся на урезанной версии сайта, после оформления подписки на [Patreon](https://www.patreon.com/javascriptcamp), ты получишь полный доступ к обучающему курсу, а также доступ к серетным каналам нашего сервера в [Discord](https://discord.gg/6GDAfXn).  

Качай наше [мобильное приложение](http://onelink.to/njhc95) или пройди тестирование в нашем [JavaScript телеграм боте](https://t.me/javascriptcamp_bot), а также подпишитесь на [наши новости](https://t.me/javascriptapp).

[![Become a Patron!](/img/logo/patreon.jpg)](https://www.patreon.com/bePatron?u=31769291)


[![Sumerian school](/img/app.jpg)](http://onelink.to/njhc95)

![JavaScript Camp](/img/bandlink.png)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):


<table>
  <tr>
    <td align="center"><a href="https://fullstackserverless.github.io/"><img src="https://avatars0.githubusercontent.com/u/6774813?v=4?s=200" width="200px;" alt=""/><br /><sub><b>Dmitriy Vasilev</b></sub></a><br /><a href="#financial-gHashTag" title="Financial">📖 💵</a></td>
  </tr>
</table>
