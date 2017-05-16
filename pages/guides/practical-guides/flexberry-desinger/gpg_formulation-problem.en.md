---
title: Постановка задачи
sidebar: guide-practical-guides_sidebar
keywords: guide
toc: true
permalink: en/gpg_formulation-problem.html
lang: en
---

## Характеристики объекта автоматизации

_Описание процесса работы будет произведено на примере приложения «АСУ Склад»._

Предприятие производит оптовую реализацию промышленной продукции широкого ассортимента. Поставщиками компании выступают заводы и фабрики, находящиеся на территории РФ. Клиенты предприятия – предприниматели, фирмы и др. организации, осуществляющие розничную и мелкооптовую продажу.

## Постановка задачи на проектирование информационной системы

Проектируемая система обязана производить учет и контроль движения продуктов на складе. Автоматизировать процесс выписки накладных, счётов и других документов.

## Описание бизнес-процесса «Реализация продукции со склада»

Клиент, решивший оформить заказ на поставку продукции, обращается в офис предприятия. Менеджер согласовывает с клиентом все условия по оформлению заказа. При этом менеджер обязан проверить наличие на складе каждого из заявленных продуктов.  
В случае если все затребованные клиентом позиции продуктов есть в наличии, либо клиентом приняты альтернативные варианты, заказ передается в бухгалтерию, и клиенту предлагается его оплатить.
Если клиент оплачивает заказ по наличному расчету, то после оплаты бухгалтер сразу выписывает две товарно-транспортные накладные, которые передаются клиенту.  
После получения накладной клиент прибывает на склад за своим товаром. Кладовщик выдает необходимые продукты и делает отметку в обоих экземплярах накладной о том, что груз выдан. Далее, клиент расписывается в двух экземплярах накладной и отбывает с полученным товаром и одним экземпляром накладной. Второй экземпляр накладной остается у кладовщика.

## Перейти

* <i class="fa fa-arrow-left" aria-hidden="true"></i> [Практическое руководство по созданию UML-диаграмм](gpg_practical-guides-uml.html)
* [Построение диаграммы вариантов использования](gpg_use-case-diagram.html) <i class="fa fa-arrow-right" aria-hidden="true"></i>