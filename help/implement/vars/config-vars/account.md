---
title: account
description: Verwenden Sie Variable „account“, um die Report Suite zu bestimmen, an die Daten gesendet werden.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 47%

---

# account

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Funktion, wenn Sie bei Ihrer Implementierung die Ziel-Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account`-Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie das Web SDK verwenden, befinden sich die Report Suites in den Einstellungen des Adobe Analytics-Dienstes innerhalb des Datastreams, an den das Web SDK Daten sendet.
* Wenn Sie die Adobe Analytics-Erweiterung verwenden, befinden sich Report Suites unter der [!UICONTROL Bibliotheksverwaltung] Akkordeon beim Konfigurieren der Adobe Analytics-Erweiterung.
* Wenn Sie [`s_gi()`](../functions/s-gi.md) -Funktion ein Analytics-Tracking-Objekt instanziieren, sind die Report Suite-ID(s) bereits als erforderliches Argument in der Funktion vorhanden.
