---
title: Пользовательские формы (классы со стереотипом userform) 
sidebar: flexberry-designer_sidebar
keywords: Flexberry Designer
toc: true
permalink: ru/fd_userform.html
folder: products/flexberry-designer/class-diagram/
lang: ru
---

Пользовательская форма предназначена для определения пустой формы, размещение элементов управления на которой и программирование визуальной логики выполняется "вручную".

Для описания пользовательской формы необходимо нанести на диаграмму UML-класс со стереотипом `userform`, например:

![](/images/pages/products/flexberry-designer/class-diagram/userform.png)

## Что генерируется

1. Класс UI-независимой формы. 
2. .Net-интерфейс для зависимой формы. 
3. UI-зависимая форма, как просто форма (пустая). 
4. Атрибуты формы генерируются следующим образом: 
    * Генерируется .Net-интерфейс UI-зависимой формы с определением свойства, но только, если этот атрибут публичный. 
    * В код UI-зависимой формы генерируется реализующее вышеуказанное интерфейсное определение виртуального свойства, а также приватный член и в обоих аксессорах код по установке/получению значения приватного члена, сопровождаемый скобками программиста. 
    * В код UI-независимой формы генерируется определение виртуального свойства с указанным модификатором, с вызовом того же свойства UI-зависимой формы через интерфейс. 
5. Методы формы генерируются следующим образом: 
    * Генерируется .Net-интерфейс UI-зависимой формы с определением метода, но только, если этот метод публичный. 
    * В код UI-зависимой формы генерируется реализующий вышеуказанное интерфейсное определение виртуальный метод и в нём скобка программиста (подобно тому, как описано здесь). 
    * В код UI-независимой формы генерируется определение виртуального метода с указанным модификатором. с вызовом того же метода UI-зависимой формы через интерфейс.

## Дополнительно редактируемые свойства и что как генерируется

### Свойства формы

![](/images/pages/products/flexberry-designer/class-diagram/userformprops.png)

Свойство | Описание | Генерация в .Net-язык
:-------------------|:-----------------------------|:---------------------------------------------
`Name` | имя UML-класса | Имя .Net-класса независимой формы и производное от него для зависимой (например, `winformXXXXXX`).
`Description` | некоторое описание класса | `DocComment` перед определением класса независимой формы
`PBCustomAttributes` | позволяет указать, необходима ли скобка программиста непосредственно перед описанием класса для "ручного" внесения атрибутов | Если галочка указана - генерируется скобка программиста для "ручного" внесения .Net атрибутов перед классом независимой формы.
`PBMembers` | | Если галочка указана - генерируется скобка программиста для "ручного" внесения членов класса независимой формы.
`Packet, NamespacePostfix` | позволяют настроить сборку и пространство имен | см. [Расположение сборок после генерации кода](fo_location-assembly-after-code-generation.html).
`ScriptName` | имя сценария, который должен использоваться этой формой. Соответствует имени EBSD-диаграммы, использующейся для описания сценария | Метод `GetScript` в классе независимой формы перегружается таким образом, что возвращает из провайдера сценариев сценарий с указанным именем. 
`PublishToEBSD` | | Если галочка указана - перед классом независимой формы генерируется указание атрибута `PublishToEBSDAttribute`, который указывает доступность данного класса для использования в редакторе диаграмм сценариев.

### Свойства атрибутов

Свойства атрибутов аналогичны указанным [в статье Атрибуты классов данных](fo_attributes-class-data.html), с учётом вышеуказанных (в п.4 "Что генерируется") замечаний.

### Свойства методов

Свойства методов аналогичны указанным [в статье Методы классов и параметры методов](fd_methods-parameters.html), с учётом вышеуказанных (в п.5 "Что генерируется") замечаний.