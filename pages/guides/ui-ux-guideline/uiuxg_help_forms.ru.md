---
title: Формы со справочными материалами
keywords: UI, UX
sidebar: ui-ux-guideline_sidebar
toc: false
permalink: ru/.html
lang: ru
summary: Описание основных функций форм и страниц со справочными материалами.
---

# Использование справочных материалов в Системах

Справочные материалы - это информация, которая предоставляет ответы на вопросы Пользователей при работе с Системой. 

## Общие рекомендации

* Использовать язык разметки [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet);
* Максимально кратко и понятно описывать функции;
* При обращении к другому материалу обязательно добавлять ссылки на него;
* Добавлять скриншоты там, где это необходимо;
* Структурировать материал по функциям.

## Основные функции справки

* Пошаговое описание всех необходимых для работы процессов;
* Ответы на часто задаваемые вопросы;
* Примеры выполнения задач.

## Примеры реализации

### Справка в сайдпейдже

При нажатию на кнопку **Справка** открывается сайдпейдж, который содержит детальную информацию о данной функции.

![Прототип справки в сайдпейдже](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/5.png)

### Отдельный документ

> Необходимо использовать только если есть необходимость.

Во многих системах требуется «формальный» справочный документ. Для этого создаются PDF файлы, которые можно скачать нажав на кнопку в разделе **Руководство пользователя**.

Пример АИСОГД:

![Пример - АИСОГД](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/1.png)

### Кнопка перехода

Данная кнопка или индикатор может выглядеть по-разному. Вид определяется на основе информационной системы и экрана на котором находится.

Примеры:

![Пример - УИС МВ](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/2.png)

![Пример - Новый дизайн](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/6.png)

### Справка по кнопке в отдельных полях

> Для показа справки по отдельным полям лучше всего использовать элемент [сайдпейдж](uiuxg_sidepage.ru.md).

Для сложных полей с кодом или специальным синтаксисом нужны отдельные справочные страницы.

![УИС МВ - шаблон поля информации](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/3.png)

При нажатии на кнопку ![Пример УИС МВ](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/4.png) открывается отдельная страница, которая содержит справку со следующими элементами:

* Синтаксис;
* Вспомогательные функции;
* Модель данных;
* Пример шаблона.

## Тултип

При наведении курсора на неподписанный элемент или иконку нужно показывать тултип.

![УИС МВ - шаблон поля информации](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/7.png)

![УИС МВ - шаблон поля информации](../../../images/pages/guides/ui-ux-guideline/uiuxg_help_forms/8.png)