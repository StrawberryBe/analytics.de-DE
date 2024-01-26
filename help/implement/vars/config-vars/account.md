---
title: account
description: Verwenden Sie Variable „account“, um die Report Suite zu bestimmen, an die Daten gesendet werden.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
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
* Wenn Sie die [`s_gi()`](../functions/s-gi.md) -Funktion ein Analytics-Tracking-Objekt instanziieren, sind die Report Suite-ID(s) bereits als erforderliches Argument in der Funktion vorhanden.
