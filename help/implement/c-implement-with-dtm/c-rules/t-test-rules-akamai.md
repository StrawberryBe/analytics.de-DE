---
description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
keywords: Dynamisches Tag-Management; rule; switcher plugin; akamai; test akamai; unveröffentlichte Regeln; Test unveröffentlichte Regeln; Debug-Regel
seo-description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
seo-title: Testen unveröffentlichter Regeln für Akamai-Hosting
solution: Marketing Cloud, Analytics, Target, Dynamisches Tag-Management
title: Testen unveröffentlichter Regeln für Akamai-Hosting
uuid: 979 e 3 d 74-8 d 96-47 d 0-b 581-cf 5371248434
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Testen unveröffentlichter Regeln für Akamai-Hosting

Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.

Mit dem Switch-Plugin sind die Tests meist am einfachsten durchzuführen. Weitere Informationen finden Sie unter [Search Discovery-Plugins](https://marketing.adobe.com/resources/help/en_US/dtm/search_discovery_plugins.html) in der Produktdokumentation für das Dynamic Tag Management.

Führen Sie die folgenden Schritte zum Testen ohne Switch-Plug-in aus:

1. Greifen Sie auf die Webkonsole auf Ihrer Website zu und geben Sie `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. Press **[!UICONTROL Enter]**.
1. Type `_satellite.setDebug(true)`, then press **[!UICONTROL Enter]**.
1. Aktualisieren Sie die Seite.

   Mit dieser Aktion wird Ihre Staging-Bibliothek geladen und der Debugger festgelegt, sodass Sie Details aller verfügbaren (veröffentlichten/nicht veröffentlichten) Regeln sehen können, die auf der Seite ausgelöst werden.
1. When finished, run `localStorage.setItem('sdsat_stagingLibrary', false)`, then press **[!UICONTROL Enter]**.

   Schritt Ergebnis