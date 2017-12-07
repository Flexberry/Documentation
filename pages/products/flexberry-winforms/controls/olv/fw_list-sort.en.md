---
title: Сортировка списков
sidebar: flexberry-winforms_sidebar
keywords: Windows UI (Контролы)
toc: true
permalink: en/fw_list-sort.html
lang: en
---

Списки позволяют сортировать содержащиеся в них объекты по определенным столбцам. Пользователь может сам настроить необходимую ему сортировку.
Также сортировку списка можно настроить из кода.

Настройка сортировки столбцов [ObjectListView](fw_objectlistview.html) осуществляется путем указания типа сортировки у объекта
`ICSSoft.STORMNET.Windows.Forms.ColumnInfo` свойства `.Columns`.

Пример:

```csharp
this.objectListView1.Columns = new ICSSoft.STORMNET.Windows.Forms.ColumnInfo[] {
    new ICSSoft.STORMNET.Windows.Forms.ColumnInfo("ФИО", -1, true, ICSSoft.STORMNET.Business.SortOrder.Asc, ((byte)(0)), "ФИО"),
    new ICSSoft.STORMNET.Windows.Forms.ColumnInfo("Прописка", -1, true, ICSSoft.STORMNET.Business.SortOrder.Asc, ((byte)(1)), "Прописка")
}
```

Здесь конструктор `ColumnInfo` принимает третьим и четвертым параметрами способ сортировки типа `ICSSoft.STORMNET.Business.SortOrder` (Asc, Desc, None) и приоритет сортировки типа `byte`.