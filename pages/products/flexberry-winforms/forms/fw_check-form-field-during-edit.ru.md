---
title: Проверка данных на форме во время редактирования
sidebar: flexberry-winforms_sidebar
keywords: Windows UI (формы)
toc: true
permalink: ru/fw_check-form-field-during-edit.html
folder: products/flexberry-winforms/
lang: ru
---
Проверка данных на форме во время редактирования может осуществляться за счёт:
* [генерации исключения при неправильном вводе в методе `set` соответствующего поля объекта](fo_сheck-object-set.html);
* определения обязательных для заполнения полей на диаграмме классов через атрибут `[Атрибуты-классов-данных|NotNull]`;
* проверки через [`DataObjectErrorProvider`](fw_data-object-error-provider.html).

| Приём | Преимущества | Недостатки|
|--|--|--|
| [Генерация исключения при неправильном вводе в методе `set` соответствующего поля объекта](fo_сheck-object-set.html) | + позволяет организовать работу таким образом, что пользователь не выйдет из поля до тех пор, пока значение поля не будет введено корректно | - для начала проверки требуется, чтобы фокус попал на соответствующее поле
| Определение обязательных для заполнения полей на диаграмме классов через атрибут [`NotNull`](fo_attributes-class-data.html) | + позволяет в модели задать обязательные для заполнения поля <br> + ненавязчивое сигнализирование о незаполненности поля | - не позволяет определять поля, обязательные только в некоторых ситуациях
| Проверка через [`DataObjectErrorProvider`](fw_data-object-error-provider.html) | + позволяет быстро прописать в коде перечень обязательных полей и пользователи приложения не смогут его менять, <br> + ненавязчивое сигнализирование о незаполненности поля  | - не позволяет пользователям менять условия проверки данных на форме
|||

Другие методы проверки данных на форме описаны [здесь](fw_edit-form-validation.html).