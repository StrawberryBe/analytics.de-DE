---
description: 'null '
keywords: DFA
seo-description: 'null '
seo-title: Aktualisierung Ihres DFA-Abfragestringparameters
solution: Analytics
title: Aktualisierung Ihres DFA-Abfragestringparameters
topic: Data Connectors
uuid: adf 585 ac -84 ff -44 c 1-a 48 d-b 072726 c 8494
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Aktualisierung Ihres DFA-Abfragestringparameters{#update-your-dfa-query-string-parameter}

Wenn Sie vor der DFA-Integration Werbekampagnen mit Adobe Analytics getrackt haben, kann es sein, dass für alle Kampagnen (E-Mail, Suche, Banner) derselbe Abfragestringparameter zur Identifizierung der jeweiligen Kampagnen-ID auf der Landingpage verwendet wird.

Zur Erkennung des richtigen Zeitpunkts für Durchsichts- und Clickthrough-Datenabfragen von DFA-Daten für Ihre DFA-Werbekampagnen muss Data Connectors identifizieren können, wann Besucher auf eine DFA-Kampagnenbanneranzeige geklickt haben. Dazu müssen Sie einen differenzierten Abfragestringparameter zur Landingpage-URL der DFA-Anzeigenkampagne hinzufügen, sodass Data Connectors zwischen DFA-Anzeigenkampagnenseiten und anderen Anzeigenkampagnenseiten unterscheiden kann, die sich gegebenenfalls auf Ihrer Website befinden. Die `dfa_overrideParam` im javascript-Plug-in (siehe [Aktualisierung des Datenerfassungscodes Ihrer Website](../../../dfa-data-connector-analytics/dfa-integration/dfa-web-site-updates/dfa-update-data-collection-code.md#concept-8c108723ea0b4cc9a8c5cdc2d05894e3)) für DFA.

>[!CAUTION]
>
>Obwohl die Kampagnenvariable für andere Kampagnen verwendet werden kann, verwenden Sie sie nicht für DFA-Kampagnen. Wenn Sie eine DFA-Kampagnenlandingpage für die Kampagnenvariable festlegen, können Impressionen und Klicks nicht von Adobe zu DFA-Kampagnen-Clickthroughs zugeordnet werden. Pro Besuch überprüfen die Adobe-Erfassungsserver die DFA-Server auf vorhandene Clickthrough- oder Durchsichtsaktionen. Verwenden Sie den DFA-Plug-in-Code (weitere Informationen finden Sie unter [Aktualisierung des Datenerfassungscodes Ihrer Website](../../../dfa-data-connector-analytics/dfa-integration/dfa-web-site-updates/dfa-update-data-collection-code.md#concept-8c108723ea0b4cc9a8c5cdc2d05894e3)) daher nur auf herkömmlichen Landingpages, um so unnötige Weiterleitungen zu verhindern, durch die die Seitenladezeit beeinträchtigt werden kann, vor allem für Benutzer mit langsamer Internetverbindung.

