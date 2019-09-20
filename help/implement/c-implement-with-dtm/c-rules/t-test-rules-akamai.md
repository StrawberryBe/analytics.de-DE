---
description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
keywords: Dynamisches Tag-Management;Regel;Umschalter-Plugin;Akamai;Test-Akamai;unveröffentlichte Regeln;Nicht veröffentlichte Regeln testen;Debug-Regel
seo-description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
seo-title: Testen unveröffentlichter Regeln für Akamai-Hosting
solution: Experience Cloud, Analytics, Target, Dynamisches Tag-Management
title: Testen unveröffentlichter Regeln für Akamai-Hosting
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Testen unveröffentlichter Regeln für Akamai-Hosting

Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.

Mit dem Switch-Plugin sind die Tests meist am einfachsten durchzuführen. Weitere Informationen finden Sie unter [Search Discovery-Plugins](https://marketing.adobe.com/resources/help/en_US/dtm/search_discovery_plugins.html) in der Produktdokumentation für das Dynamic Tag Management.

Führen Sie die folgenden Schritte zum Testen ohne Switch-Plug-in aus:

1. Greifen Sie auf die Webkonsole auf Ihrer Website zu und geben Sie `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. Press **[!UICONTROL Enter]**.
1. Geben Sie `_satellite.setDebug(true)`ein und drücken Sie dann die **[!UICONTROL Eingabetaste]**.
1. Aktualisieren Sie die Seite.

   Mit dieser Aktion wird Ihre Staging-Bibliothek geladen und der Debugger festgelegt, sodass Sie Details aller verfügbaren (veröffentlichten/nicht veröffentlichten) Regeln sehen können, die auf der Seite ausgelöst werden.
1. Führen Sie abschließend `localStorage.setItem('sdsat_stagingLibrary', false)`die **[!UICONTROL Eingabetaste]** aus.

   Schritt Ergebnis