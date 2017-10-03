---
title: ComboLookup
sidebar: flexberry-winforms_sidebar
keywords: Windows UI (Контролы)
toc: true
permalink: ru/fw_combo-lookup.html
folder: products/flexberry-winforms/
lang: ru
---

# Описание
Элемент управления для выбора мастера из комбинированного списка ComboBox.

Основные свойства:
* '''DataObjectType''' – тип мастерового объекта.
* '''MasterPropertyName''' – свойство объекта данных, которое редактируется ComboLookup.
* '''ComboPropertyName''' – мастерового объекта, которое будет отображаться в списке.
* '''CachedData''' – данные читаются из базы при каждом открытии списка или кэшируются.
* '''Limit''' – ограничение на список мастеровых объектов. Следует заметить, что свойство имеет тип FunctionForControls (см. пример).

```csharp
comboLookup1.CachedData = true;
comboLookup1.ComboPropertyName = "Название";
comboLookup1.DataObjectType = typeof(IIS.КошкиСЛапами.Кошка);
comboLookup1.MasterPropertyName = "Порода";

SQLWhereLanguageDef langdef = SQLWhereLanguageDef.LanguageDef;  
Function lf = langdef.GetFunction(langdef.funcLike,   
new VariableDef(langdef.StringType, "Название"), "Перс%");
comboLookup1.Limit = new FunctionForControls("ПородаL", lf);
```

# Изменение типа лукапа с Default на Combo
Если форма уже существует, то при попытке изменения типа у существующего лукапа изменения '''не применятся'''. 

Чтобы изменения вступили в силу необходимо вручную удалить весь код, связанный с контролом, из кода страницы и запустить перегенерацию.