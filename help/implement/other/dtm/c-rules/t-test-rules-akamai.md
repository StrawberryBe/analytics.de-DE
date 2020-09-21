---
description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
keywords: Dynamic Tag Management;rule;switcher plug-in;akamai;test akamai;unpublished rules;test unpublished rules;debug rule
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Testen unveröffentlichter Regeln für Akamai-Hosting
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: ht
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16
workflow-type: ht
source-wordcount: '132'
ht-degree: 100%

---


# Testen unveröffentlichter Regeln für Akamai-Hosting

Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.

Mit dem Switcher-Plug-in sind die Tests meist am einfachsten durchzuführen. Weitere Informationen finden Sie unter [Search Discovery-Plug-ins](https://docs.adobe.com/content/help/de-DE/dtm/using/resources/plugins/search-discovery-plugins.html) in der Produktdokumentation für das Dynamic Tag Management.

Führen Sie die folgenden Schritte zum Testen ohne Switcher-Plug-in aus:

1. Greifen Sie auf die Webkonsole auf Ihrer Website zu und geben Sie `localStorage.setItem('sdsat_stagingLibrary', true)` ein.
1. Drücken Sie die **[!UICONTROL Eingabetaste]**.
1. Geben Sie `_satellite.setDebug(true)` ein und drücken Sie dann die **[!UICONTROL Eingabetaste]**.
1. Aktualisieren Sie die Seite.

   Mit dieser Aktion wird Ihre Staging-Bibliothek geladen und der Debugger festgelegt, sodass Sie Details aller verfügbaren (veröffentlichten/nicht veröffentlichten) Regeln sehen können, die auf der Seite ausgelöst werden.
1. Führen Sie abschließend `localStorage.setItem('sdsat_stagingLibrary', false)` aus und drücken Sie die **[!UICONTROL Eingabetaste]**.

   Schrittergebnis
