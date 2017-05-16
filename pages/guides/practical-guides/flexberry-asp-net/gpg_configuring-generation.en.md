---
title: Настройка кодогенерации (CSharp)
sidebar: guide-practical-guides_sidebar
keywords: guide
toc: true
permalink: en/gpg_configuring-generation.html
lang: en
---

1.	Выбрать стадию (щелкнуть левой кнопкой мыши).
2.	Далее нажать на стадии правой кнопкой мыши. В появившемся меню выбрать пункт `ASP.NET` -> `C#` -> `Свойства модели`.
3.	В поле Product указать имя программного продукта (например, `АСУ_Склад`). По умолчанию название проекта будет иметь вид: `Product_****`, оно должно быть изменено. 
4.	Настроить путь до каталога, в который будут помещены сгенерированные проекты: в поле `Каталог для исходного кода` указать относительный путь для генерации веб-приложения, например, `CodeGen\АСУ_Склад`. Базовый путь для генерации приложений можно изменить, выбрав в главном меню пункт `Настройки` -> `Путь генерации…`

![](/images/pages/guides/flexberry-aspnet/generation-path.png) 
 
5.В окне `Стадия (редактирование)` нажать `Сохранить и закрыть`.

## Перейти

*  <i class="fa fa-arrow-left" aria-hidden="true"></i> [Настройка структуры приложения](gpg_connection-settings-db.html)
* [Генерация веб-приложения](gpg_generation-application.html) <i class="fa fa-arrow-right" aria-hidden="true"></i> 