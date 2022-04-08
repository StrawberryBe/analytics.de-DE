---
description: In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.
title: VRS-Unterstützung in Mobile Services
feature: VRS
exl-id: 3082333a-514d-45c6-9432-da32bd27a2eb
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: ht
source-wordcount: '219'
ht-degree: 100%

---

# VRS-Unterstützung in Mobile Services

In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.

## VRS-Unterstützung in Mobile Services {#topic_1D0BABFA64EF42DE9C09B7AA37CACEC5}

In der Oberfläche von Adobe Mobile Services werden Daten der mobilen Anwendungen über Ihre Adobe Analytics Report Suites zusammengefasst, und Sie können Push-Benachrichtigungen versenden und In-App-Benachrichtigungen erstellen.

Adobe Mobile Services unterstützt Virtual Report Suites. Wenn Sie jedoch eine Virtual Report Suite mit mehreren Apps erstellen möchten und eine Messaging-Aktivität planen, müssen Sie die jeweilige App-ID als Parameter angeben. Beim Erstellen einer Push-Nachricht muss die App-ID einer der Parameter des verwendeten Segments sein. Beim Erstellen einer In-App-Nachricht muss die App-ID einer der Parameter der für die Nachricht festgelegten Eigenschaften sein. Ist dies nicht der Fall, wird die Nachricht auf allen Apps ausgelöst/allen Benutzern gesendet, die den Segment-/Auslöserkriterien entsprechen.

Weitere Informationen finden Sie unter [Virtual Report Suites](https://experienceleague.adobe.com/docs/mobile-services/using/manage-apps-ug/c-mob-vrs.html?lang=de) in der Dokumentation zu Adobe Mobile Services.
