---
title: account
description: Verwenden Sie die Kontovariable, um die Report Suite zu bestimmen, an die Daten gesendet werden.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# account

> [!IMPORTANT] Diese Variable wird eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md) Funktion, wenn Sie bei Ihrer Implementierung das Ziel der Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account` Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie Adobe Experience Platform Launch verwenden, befinden sich Report Suites beim Konfigurieren der Adobe Analytics-Erweiterung unter dem [!UICONTROL Library Management] Akkordeon.
* Wenn Sie die [`s_gi()`](../functions/s-gi.md) Funktion zum Instanziieren eines Analytics-Verfolgungsobjekts verwenden, existieren die Report Suite-IDs bereits als erforderliches Argument in der Funktion.
