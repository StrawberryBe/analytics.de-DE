---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: ht
source-wordcount: '1077'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (Januar 2024)

**Letzte Aktualisierung:** 10. Januar 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum von Januar 2024 bis zum 13. Februar 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Data Warehouse-Aktualisierungen** | Die folgenden Data Warehouse-Verbesserungen sind jetzt verfügbar:<ul><li>Beim Erstellen einer Data Warehouse-Anforderung können Benutzende jetzt Anforderungen für alle Benutzenden in der Organisation verfügbar machen, indem sie den neuen Umschalter mit dem Namen [!UICONTROL **Bereitstellung für Benutzende in Ihrer Organisation**] aktivieren.<p>Weitere Informationen finden Sie unter [Allgemeine Einstellungen für Data Warehouse-Anfragen](/help/export/data-warehouse/create-request/dw-general-settings.md).</p></li><li>Bei der Erstellung oder Verwaltung von Data Warehouse-Berichtszielen können Systemadmins jetzt Konten und Orte anzeigen, die von Benutzenden in der Organisation erstellt wurden, indem sie den Umschalter [!UICONTROL **Alle Ziele anzeigen**] aktivieren.<p>Weitere Informationen finden Sie unter [Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-destinations.md).</p></li> | Nicht angegeben | 10. Januar 2024 |
| **Aktualisierungen zur Visualisierung der Schlüsselmetrikübersicht** | Bei der Visualisierung der Schlüsselmetrikübersicht kann der Vergleichs-Datumsbereich jetzt automatisch aktualisiert werden, je nachdem, ob der ausgewählte Vergleichs-Datumsbereich relativ zum primären Datumsbereich oder fest ist. [Weitere Informationen](/help/analyze/analysis-workspace/visualizations/key-metric.md). | Nicht angegeben | 17. Januar 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden die folgenden Klassifizierungsprobleme behoben: AN-314821; AN-326839; AN-332079; AN-332704; AN-332812; AN-332902; AN-332975; AN-333300; AN-333023; AN-333033; AN-333174; AN-333910; AN-334097; AN-334208; AN-334373; AN-334439; AN-334698; AN-334838; AN-334848; AN-334987; AN-335046; AN-335082; AN-335202; AN-335203; AN-335254; AN-335322; AN-335552; AN-335591; AN-335603; AN-335610; AN-335617; AN-335699; AN-335891; AN-335901; AN-336063; AN-336072; AN-336193; AN-336479; AN-336684; AN-336801; AN-337370; AN-337398
* Es wurden die folgenden Probleme mit dem Classification Rule Builder behoben: AN-332390; AN-332573; AN-332718; AN-332927; AN-333248; AN-333953; AN-334647; AN-334736; AN-334910; AN-335642; AN-335683; AN-335811; AN-336033; AN-336569; AN-336852; AN-336875; AN-336902; AN-337190;
* Die folgenden A4T-Probleme wurden behoben: AN-334564; AN-336178;
* Die folgenden Probleme bei der Nutzung von Server-Aufrufen wurden behoben: AN-332568; AN-333105; AN-333167; AN-333983; AN-334209; AN-334278
* Es wurden folgende Data Warehouse-Probleme behoben: AN-333010; AN-333076; AN-330227; AN-331580; AN-333350; AN-334291; AN-334283; AN-334287; AN-334301; AN-334385; AN-334453; AN-334977; AN-335079; AN-335171; AN-335245; AN-335426; AN-335680; AN-335818; AN-336087; AN-337308;
* Es wurden die folgenden Daten-Feeds-Probleme behoben: AN-332241; AN-332366; AN-332617; AN-332654; AN-332702; AN-332723; AN-333014; AN-333166; AN-334037; AN-334125; AN-334211; AN-334216; AN-334235; AN-334976; AN-335158; AN-335368; AN-335408; AN-335468; AN-335471; AN-335528; AN-335596; AN-335662; AN-335733; AN-335883; AN-335894; AN-335968; AN-336098; AN-336192; AN-336243; AN-336659; AN-336977; AN-337117; AN-337219; AN-337262; AN-337393; AN-337462; AN-337854
* Es wurden die folgenden Report Builder-Probleme behoben: AN-335246; AN-336311;
* Es wurden die folgenden Analysis Workspace-Probleme behoben: AN-323760; AN-324191; AN-324913; AN-330126; AN-332808; AN-333168; AN-333382; AN-334839; AN-336040; AN-337043;

### Weitere Fehlerbehebungen

AN-323975; AN-325383; AN-325809; AN-326787; AN-331611; AN-331818; AN-332124; AN-332272; AN-332911; AN-333070; AN-333302; AN-333377; AN-333904; AN-333928; AN-333968; AN-334056; AN-334099; AN-334191; AN-334207; AN-334776; AN-335206; AN-335294; AN-335320; AN-335394; AN-335443; AN-335967; AN-336099; AN-337452; AN-337463

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| Adobe-API-Objektmitgliederergänzungen | 17. Januar 2024 | Adobe kann ohne Ankündigung oder Versionsänderung optionale Anforderungs- und Antwortmitglieder (Name/Wert-Paare) zu bestehenden API-Objekten hinzufügen. Solche Ergänzungen sollten für Ihre Implementierung keine einschneidenden Änderungen darstellen. Adobe empfiehlt, in der API-Dokumentation jedes Drittanbieter-Tools, das Sie in unsere API integrieren, nachzuschlagen, damit solche Ergänzungen bei der Verarbeitung ignoriert werden, wenn sie nicht verstanden werden. Adobe entfernt keine Parameter und fügt keine erforderlichen Parameter hinzu, ohne zuvor durch Versionshinweise eine Standardbenachrichtigung bereitzustellen. |
| `getPageLoadTime`-Plug-in veraltet | 10. Januar 2024 | Dieses Plug-in wird nicht mehr unterstützt. Der Code verwendet die Methode „performance.timing“, die (laut MDN) [veraltet](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming) ist. Die Arbeit an einem aktualisierten Plug-in hat begonnen. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für [!DNL Reports & Analytics]** | 10. Januar 2024 | Ab dem **17. Januar 2024** hat Adobe [!DNL Reports & Analytics] und seine begleitenden Berichte und Funktionen eingestellt. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von [!DNL Reports & Analytics] entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 17. Januar 2024 haben wir viele der verknüpften Reports &amp; Analytics-Funktionen eingestellt, einschließlich, unter anderem, terminierter Berichte, Datenextraktionen und DL-Berichte. Nach dem 17. Januar 2024 wurden terminierte Berichte nicht mehr gesendet. Zusätzlich können Sie zukünftige Berichte seit dem 17. Januar 2024 nicht mehr terminieren. |
| **Einstellungszeitpunkt für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 10. Januar 2024 | Als Teil der Einstellung von Reports &amp; Analytics wurden [!UICONTROL Veröffentlichungslisten] am **17. Januar 2024** eingestellt. Sie können keine neuen [!UICONTROL Veröffentlichungslisten] mehr erstellen oder auf vorhandene zugreifen, um Projekte in [!UICONTROL Analysis Workspace] zu senden oder zu planen.  |
| **Einstellungszeitpunkt für Data Workbench** | 2. Januar 2024 | Adobe hat Data Workbench am **31. Dezember 2023** eingestellt. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://express.adobe.com/page/GSu6oKOD88GAj/). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.25.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2023](/help/release-notes/2023.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
