---
title: Using data types in the application structure
sidebar: flexberry-orm_sidebar
keywords: Flexberry ORM, data types, DataObject, data service
summary: Правила обработки TypeUsage и задания имен полей хранения ссылок
toc: true
permalink: en/fo_type-usage.html
lang: en
---

Если [мастер в ассоциации](fd_master-association.html) имеет [наследников](fd_inheritance.html), то на стороне мастера может быть объект любого типа из иерархии наследования. Однако бывают условия, при которых такие ситуации требуется исключить. Для этого во [Flexberry ORM] реализован `TypeUsage`-атрибут, ограничивающий список типов в иерархии наследования, на который распространяется данная связь.

## Обработка TypeUsage

Встроенные в `Flexberry Platform` [сервисы данных](fo_data-service.html) ([SQLDataService](fo_sql-data-service.html) и его наследники) обрабатывают `TypeUsage` следующим образом:

Если указан `TypeUsage` для [мастерового свойства](fd_master-association.html), этому свойству [в структуре данных соответствуют](fo_storing-data-objects.html) внешние ключи на таблицы, соответствующие указанным в `TypeUsage` классам.

Имена внешним ключам даются такие: `<ИмяРолиМастера>_M<ПорядкНомерВTypeUsage>.«ПорядкНомерВTypeUsage»` — начинается с 0.

Таким образом, вышеприведённому примеру соответствует таблица, у которой есть два внешних ключа с именами `M_m0` (соответствует M1) и `M_m1` (соответствует M2).

![](/images/pages/products/flexberry-orm/data-types/primer2.jpg)

## Задание имён для полей хранения ссылок

Если есть потребность задать вместо имён `M_m0` и `M_m1` некоторые мнемонические имена, то необходимо:

1. Отключить галочку [AutoGenerateTypeUsage](fd_master-association.html).
2. Правильно проставить атрибуты [TypeUsage](fo_type-usage-problem.html) и Storage.

Например, пусть имеется диаграмма вида:

![](/images/pages/products/flexberry-orm/data-types/type-usage-test.png)

Если ничего не менять в настройках элементов диаграммы, то, например, в таблице `ДниПосещения` будут внешние ключи с именами `Пользователь_m0`, `Пользователь_m1`, `Пользователь_m2`. 

Однако если у связи, соединяющей классы `Пользователь` и `ДниПосещения` проставить в `TypeUsage` и `Storage` строку вида `Пользователь,Врач,Пациент`, то в таблице `ДниПосещения` будут внешние ключи с именами `Пользователь`, `Врач`, `Пациент`. Аналогично можно настроить [детейловую связь](fo_detail-associations-properties.html).