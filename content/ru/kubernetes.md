---
title: Kubernetes
status: Completed
category: technology
tags: ["infrastructure", "fundamental", ""]
---

Kubernetes (часто сокращается до K8s) — это система для управления контейнерами (т. н. оркестратор) с открытым исходным кодом.
Kubernetes автоматизирует жизненный цикл контейнеризированных приложений в современных инфраструктурах, выступая в качестве «операционной системы для центров обработки данных», которая управляет приложениями в [распределенных системах](/distributed-systems/).

Kubernetes планирует (т. е. распределяет) [контейнеры](/ru/container/) по [узлам](/nodes/) [кластера](/cluster/), попутно обеспечивая их различными инфраструктурными ресурсами: например, балансировщиками нагрузки, постоянным хранилищем и т. д., которые необходимы для запуска контейнеризованных приложений.

Kubernetes также обеспечивает автоматизацию и расширяемость, позволяя пользователям использовать декларативность (см. ниже) и обеспечивать воспроизводимость в процессе развертывания приложений.
[API](/application-programming-interface/) Kubernetes позволяет опытным пользователям расширять и дополнять его возможности по автоматизации в соответствии со своими потребностями.

## Какую проблему решает

Автоматизация инфраструктуры и декларативное управление конфигурацией уже давно занимают важное место в IT, но с ростом популярности [облачных вычислений](/cloud-computing/) их актуальность возросла еще сильнее. 

Спрос на вычислительные ресурсы постоянно увеличивается, а компании стараются сделать труд инженеров максимально эффективным, чтобы оптимизировать ФОТ. Новые технологии и методы работы как раз призваны удовлетворить обе эти потребности.

## Как именно решает проблему

Как и традиционные инструменты или подходы, например, [инфраструктура как код (IaC)](/infrastructure-as-code/), Kubernetes помогает автоматизировать процессы, но у него есть и серьезное преимущество перед ними — использование контейнеров.

Контейнеры более устойчивы к накапливающимся со временем изменениям в конфигурации, нежели [виртуальные](/virtual-machine/) или физические машины.

Кроме того, Kubernetes работает декларативно, то есть пользователь не указывает компьютеру, что и как нужно сделать, а лишь описывает желаемое конечное состояние инфраструктуры (обычно в виде файлов-манифестов на языке YAML).
Все остальное Kubernetes берет на себя.
Таким образом, Kubernetes в высшей степени совместим с подходом «инфраструктура как код».

В Kubernetes также встроена функция [самовосстановления](/self-healing/).

Фактическое состояние кластера всегда стремится к тому состоянию, которое описал оператор.
Когда Kubernetes обнаруживает отклонение от файлов манифеста, в дело вступает контроллер Kubernetes, который устраняет это отклонение.
Инфраструктура, с которой работает Kubernetes, может в любой момент измениться, однако оркестратор постоянно и автоматически адаптируется к изменениям, следя за тем, чтобы фактическое состояние кластера всегда соответствовало желаемому состоянию.