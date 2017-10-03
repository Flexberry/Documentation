---
title: Перехват событий ObjectListView (создание, удаление, изменение объекта), выполнение действий
sidebar: flexberry-winforms_sidebar
keywords: Windows UI (Контролы)
toc: true
permalink: ru/fw_interception-events-objectlistview.html
folder: products/flexberry-winforms/
lang: ru
---

На самом деле, `ObjectListView` не содержит никакой функциональности по действиям (создание, сохранение и т.д.) с объектами данных, отображаемыми в списке. Программист должен написать код, «ловящий» события, происходящие в `ObjectListView`, и отрабатывающий соответствующую реакцию. Наоборот, если в программе произошло некоторое действие, необходимо сообщить о нём `ObjectListView` для адекватного отображения объектов.
Для перехвата событий, необходимо:
* Повесить обработчик на событие `CreateObject` при реализации действий по созданию объекта данных, событие происходит, когда пользователь нажимает в панели инструментов кнопку создания объекта;
* Повесить обработчик на событие `EditObject` при реализации действий по редактированию объекта данных, событие происходит, когда пользователь нажимает в панели инструментов кнопку редактирования объекта;
* Повесить обработчик на событие `DeleteObject` при реализации действий по созданию объекта данных, событие происходит, когда пользователь нажимает в панели инструментов кнопку удаления объекта;

Для информирования `ObjectListView` о произошедших действиях, необходимо:

* Вызвать метод `AddObject`, если объект данных был добавлен, он отобразится в `ObjectListView` (Важно! Не вызывайте данный метод до обработки объекта данных сервисом данных, поскольку это может вызвать ошибку, т.к. `ObjectListView` попытается прочитать объект данных из хранилища, где его ещё нет);
* Вызвать метод `UpdateObject`, если объект данных был изменён, тогда поля в `ObjectListView` поменяют значения на соответствующие в объекте данных;
* Вызвать метод `DeleteObject`, если объект данных был удалён, тогда он исчезнет из `ObjectListView`.

## Другие важные события
`OnChangeCurrentObject` — происходит, когда пользователь выбирает объект (перемещает курсор) в списке.
`ObjectDblClick` — Происходит, когда на текущем объекте выполнен `DblClick`.

## Другие важные свойства и методы
`ObjectCount` — получить количество объектов в списке.
`GetObject` — получение объекта данных непосредственно из списка по различным критериям.
`FillData` — заполнение списка данными (обновление).
`HideToolBar` — показать/спрятать тулбар.
`UseToolBar` — использовать нестандартный тулбар, какой-то другой, снаружи, на него автоматически «намазываются» кнопки от `ObjectListView`.
`ClearCache` — очистка внутреннего кеша.

