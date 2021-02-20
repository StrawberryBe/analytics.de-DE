---
description: In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.
title: VRS-Unterstützung in Mobile Services
uuid: 1b11279e-d0d8-48c5-a5b5-8020d5ed39da
translation-type: tm+mt
source-git-commit: 9193a520b13a0717a3383a32b39936f278c49d49
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 100%

---


# VRS-Unterstützung in Mobile Services

In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.

## VRS-Unterstützung in Mobile Services {#topic_1D0BABFA64EF42DE9C09B7AA37CACEC5}

In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.

Adobe Mobile Services unterstützt Virtual Report Suites. Wenn Sie jedoch eine Virtual Report Suite mit mehreren Apps erstellen möchten und eine Messaging-Aktivität planen, müssen Sie die jeweilige App-ID als Parameter angeben. Beim Erstellen einer Push-Nachricht muss die App-ID einer der Parameter des verwendeten Segments sein. Beim Erstellen einer In-App-Nachricht muss die App-ID einer der Parameter der für die Nachricht festgelegten Eigenschaften sein. Ist dies nicht der Fall, wird die Nachricht auf allen Apps ausgelöst/allen Benutzern gesendet, die den Segment-/Auslöserkriterien entsprechen.

Weitere Informationen finden Sie unter [Virtual Report Suites](https://docs.adobe.com/content/help/de-DE/mobile-services/using/manage-apps-ug/c-mob-vrs.html) in der Dokumentation zu Adobe Mobile Services.
