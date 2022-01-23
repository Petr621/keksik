# Keksik

[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]
[![Node.js Version][node-version-image]][node-version-url]
[![Build Status][travis-image]][travis-url]
[![Test Coverage][coveralls-image]][coveralls-url]

Библиотека для взаимодействия с кексиком (вк)

## Установка

Это модуль на [Node.js](https://nodejs.org/en/)
Устанавливается с помощью [`npm install` command](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)

```
$ npm install keksik
```

## Использование

<!-- eslint-disable no-unused-vars -->

```js
const KEKSIK = require('keksik');
```

### Параметры

```js
const keksik = new KEKSIK({
    "token": "user token", // Токен кексика
    "group": 209016879, // ID группы в Вк
    "key": "key" // Ключ для подтверждения сервера
});
```

token - Токен кексика (берется в приложении)  
group - Цифровой ID вашей группы вк (берется в настройках)  
key - Параметр нужный для колбека (не обязателен)  

### Key

Параметр нужный для использования колбека кексика  
Он берется в приложении в настройках сервера  
Нужен для подтверждения сервера (требование кексика)  
Этот параметр не обязателен при использовании онли запросов  

## Методы
Список методов API  
[donatesget](https://www.npmjs.com/package/keksik#donatesget) - Получение списка донатов  
[donatesgetlast](https://www.npmjs.com/package/keksik#donatesgetlast) - Получение списка последних донатов  
[donateschangestatus](https://www.npmjs.com/package/keksik#donateschangestatus) - Изменить статус доната  
[donatesanswer](https://www.npmjs.com/package/keksik#donatesanswer) - Добавить/изменить ответ сообщества на донат  
[donateschangerewardstatus](https://www.npmjs.com/package/keksik#donateschangerewardstatus) - Изменить выдачи вознаграждения  
[campaignsget](https://www.npmjs.com/package/keksik#campaignsget) - Получить список краудфандинговых кампаний (последние 20 кампаний)  
[campaignsgetactive](https://www.npmjs.com/package/keksik#campaignsgetactive) - Получить активную краудфандинговую кампанию  
[campaignsgetrewards](https://www.npmjs.com/package/keksik#campaignsgetrewards) - Получить список вознаграждений краудфандинговой кампании  
[campaignschange](https://www.npmjs.com/package/keksik#campaignschange) - Обновить информацию о краудфандинговой кампании  
[campaignschangereward](https://www.npmjs.com/package/keksik#campaignschangereward) - Обновить информацию о вознаграждении краудфандинговой кампании  
[paymentsget](https://www.npmjs.com/package/keksik#paymentsget) - Получить список заявок на выплату (последние 20 заявок)  
[paymentscreate](https://www.npmjs.com/package/keksik#paymentscreate) - Создать заявку на выплату  
[balance](https://www.npmjs.com/package/keksik#balance) - Получить баланс группы в приложении  

### donatesget

## Коды ошибок

1000 - Неизвестный метод.  
1001 - Не переданы обязательные параметры.  
1002 - Переданы некорректные значения для некоторых параметров.  
1004 - Ошибка авторизации. Проверьте правильность параметров \'group\' и \'token\'.  
1005 - Версия API устарела.  
1006 - API сервис временно не доступен.  
2000 - Превышен лимит обращений к API.  
3000 - В данный момент нет активной кампании.  
3001 - Кампания с таким ID не найдена.  
3002 - Заявка на вывод с таким ID не найдена.  
3003 - Донат с таким ID не найден.  
3004 - Запрашиваемая сумма выплаты превышает остаток средств на балансе.  
3005 - Запрашиваемая сумма выплаты ниже минимальной суммы выплаты для данной платежной системы.  
3006 - Ошибка списания средств. Повторите запрос.  
3007 - Создание выплат через API отключено в настройках приложения.  
3008 - Время окончания указано неправильно. Кампания не может оканчиваться менее чем через три часа от текущего момента.  
3009 - Запрашиваемая сумма выплаты выше максимальной суммы выплаты для данной платежной системы.  

## Помощь

[Zozick](https://vk.com/zozick_off) - Писать по любым вопросам  
[Mail](https://e.mail.ru/compose/?to=zozi@zozick.ru) - Мой майл  

## Лицензия

[MIT](https://github.com/Petr621/keksik/blob/main/LICENSE)

