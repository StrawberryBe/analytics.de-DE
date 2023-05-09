---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 5ce3684b44feb37f443046e93aa6d4b17aef8125
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 60%

---

# Aktuelle Adobe Analytics-Versionshinweise (Mai 2023)

**Letzte Aktualisierung:**: 8. Mai 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Aufstockung für Nicht-Produktions-Sandboxes** | Beim Erstellen eines Analytics Source Connector-Datenflusses in einer Nicht-Produktions-Sandbox ist die Aufstockung in Nicht-Produktions-Sandboxes auf 3 Monate beschränkt. Für Produktions-Sandboxes bleibt sie bei 13 Monaten. | Nicht angegeben | 26. April 2023 |
| **Link-Freigabe für Projekte (keine Anmeldung erforderlich)** | Sie können jetzt schreibgeschützte Links zu Analysis Workspace-Projekten für Personen freigeben, die keinen Zugriff auf Adobe Analytics haben. Dazu gehört die Freigabe für Personen außerhalb Ihres Unternehmens oder für Personen in Ihrem Unternehmen, die nicht für Adobe Analytics bereitgestellt werden. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=en#share-public-link)<p>Diese Funktion ist standardmäßig aktiviert und kann vom Systemadministrator deaktiviert werden. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/user-preferences.html?lang=en#company-preferences)</p> | 3. Mai 2023 | Juni 2023 |
| **Aktualisierter Startbildschirm für die Analytics-Dashboards-App (Mobile App)** | Mit dem neuen aktualisierten Startbildschirm können Sie alle Ihre Scorecards in einer konsolidierten Scorecard-Liste anzeigen.  Wenn Sie unter einer Anmeldung Zugriff auf mehr als eine Organisation haben, stehen alle Scorecards Ihrer Organisation in einer einzigen Liste zur Verfügung. | Nicht angegeben | 10. Mai 2023 |
| **Komponenten in Analysis Workspace sortieren** | Bei der Anzeige von Komponenten in der linken Leiste oder im Datenwörterbuch in Analysis Workspace ist jetzt eine neue Sortieroption verfügbar. Sie können Komponenten nach Empfohlen (am häufigsten verwendete), Alphabetisch oder Kategorisch (Typ) sortieren.<p>Zuvor war es nur möglich, Komponenten zu suchen oder zu filtern. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html?lang=en)</p> | Nicht angegeben | 10. Mai 2023 |
| **Löschen von Zeilen, die dynamische Dimensionen enthalten, aus einer Freiformtabelle** | In einer Freiformtabelle in Analysis Workspace können Sie jetzt mithilfe des x-Symbols schnell bestimmte Zeilen löschen, die dynamische Dimensionen enthalten. Dabei wird automatisch die Filterregel &quot;Ist nicht gleich&quot;angewendet.<p>Zuvor bestand die einzige Möglichkeit zum Löschen von Zeilen, die dynamische Dimensionen enthielten, darin, manuell eine Regel im Dialogfeld Filter zu erstellen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.html?lang=en)</p> | Nicht angegeben | 10. Mai 2023 |
| **Neue Schaltfläche zum Hinzufügen einer Visualisierung in einem Bedienfeld** | Unten in jedem Bedienfeld in Analysis Workspace ist jetzt eine neue Schaltfläche verfügbar, mit der Sie schnell eine Visualisierung hinzufügen können. <p>Zuvor bestand die einzige Methode zum Hinzufügen einer Visualisierung zu einem Bedienfeld darin, eine Visualisierung aus der linken Leiste zu ziehen, eine vorhandene Visualisierung zu duplizieren oder zu kopieren oder ein leeres Bedienfeld zu erstellen. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=en#quick-viz)</p> | Nicht angegeben | 17. Mai 2023 |
| **Deep-Linking (mobile App)** | Ermöglicht Benutzern das Senden von Links zu Scorecards, die sie direkt zum Scorecard-Projekt in der App führen. Dies erleichtert die Freigabe von Projekten und die Interaktion von weniger technischen Zielgruppen. | TBD | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

AN-312098; AN-318309; AN-316675; AN-318173; AN-310359; AN-317613; AN-318836; AN-315744; AN-311772; AN-318719; AN-314074; AN-316651<!--"Verified" status-->; AN-318602; AN-315961; AN-317534; AN-318607; AN-316498; AN-316648; AN-318244; AN-317747; AN-318432; AN-318231; AN-317590; AN-318415; AN-318154; AN-316647; N-314417; AN-317614; AN-317725; AN-318114; AN-317876; AN-318052; AN-317966; AN-316477; AN-318036; AN-317931; AN-318045; AN-316246; AN-317281; AN-317879; AN-308077; AN-317708; AN-316115; AN-315963

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Hinzugefügt oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Hinweis: Neue IPs, die von Adobe Analytics Data Feeds und der Data Warehouse Egress im London Data Center verwendet werden** | 27. April 2023 | Für Kunden im London Data Center, bei denen Daten-Feed-Anfragen und/oder Data Warehouse-Berichte an einen FTP-/SFTP-Dienst gesendet werden, sollten die folgenden IP-Adressbereiche zu Ihrer Firewall-Konfiguration hinzugefügt werden, um den Zugriff zu ermöglichen: <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |
| **Gerätesuchvorgänge verwenden jetzt einen Drittanbieter für alle Gerätesuchen.** | 3. März 2023 | Am 2. März 2023 haben wir im Rahmen des Support-Rollouts für Client-Hinweise unsere Gerätesuchvorgänge so aktualisiert, dass für alle Gerätesuchen ein Drittanbieter verwendet wird. Zuvor hatten wir den Drittanbieter nur für die Suche nach Mobilgeräten verwendet. Im Zuge dieses Rollouts wurden einige Desktop-Betriebssysteme fälschlicherweise mit dem Text „Mobile“ gekennzeichnet (z. B. „Mobile OS X 10.15.7“ anstelle von „OS X 10.15.7“).<p>Bei der Adobe-Aprilversion werden wir diese Namen korrigieren. Die Analytics- und CJA-Berichte werden rückwirkend aktualisiert, da die zugehörigen Berichtsfunktionen den Betriebssystemnamen basierend auf einer ID nachschlagen, die als Teil der Ereignisdaten aufgezeichnet wird. Sobald der Suchwert, der einer ID entspricht, aktualisiert wird, werden alle Berichte korrigiert, einschließlich historischer Daten. Für Kunden und -Kundinnen von [!UICONTROL Daten-Feeds] ist die Änderung rückwirkend, wenn zum Berichtszeitpunkt ein ähnlicher Suchvorgang verwendet wird. Wenn Sie den Betriebssystemwert jedoch in Ihren Ereignisdaten speichern, werden nur die Berichte in der Zukunft aktualisiert. Weitere Informationen dazu finden Sie unter [Betriebssystem](/help/components/dimensions/operating-systems.md). |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL des japanischen Feature Phone-Tracking-Dienstes** | 21. März 2023 | Nur für unsere japanischen Kundinnen und Kunden: **Ende Mai 2023** wird der japanische Tracking-Dienst „Feature Phone“ (mod_ktrack) eingestellt. Wir entschuldigen uns für die Unannehmlichkeiten, bitten jedoch darum, die auf Ihrem Apache-Server installierten Module zu deinstallieren oder zu deaktivieren. Siehe Seiten 27 und 28 in [diesem Dokument](/help/release-notes/mod_ktrackforSiteCatalyst_ver1.40.pdf). |
| **EOL für [!DNL Reports & Analytics]** | 7. März 2023 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert.<p>Am 31. Dezember 2023 werden wir viele der zugehörigen Reports &amp; Analytics-Funktionen einstellen, insbesondere: Terminierte Berichte, Datenextraktionen und DL-Berichte. Nach dem 31. Dezember 2023 werden terminierte Berichte nicht mehr gesendet. Im **April 2023** werden alle Berichte, die nach dem 31. Dezember 2023 ablaufen sollten, automatisch aktualisiert und auf den 31. Dezember 2023 zurückgesetzt. Darüber hinaus können Sie nach dem 31. Dezember 2023 keine zukünftigen Berichte mehr planen. |
| **Ende der Nutzungsdauer der [!UICONTROL Personen]-Metrik** | 9. März 2023 | Mit der Einstellung der [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html?lang=de) ist die Metrik „Personen“, die sich auf die Gerätekooperation bezieht, nicht mehr relevant. Am 8. Mai 2023 werden wir die Metrik [!UICONTROL Personen] entfernen. An diesem Punkt werden wir diese Daten an die [!UICONTROL Unique Visitor]-Metrik umleiten, um zu verhindern, dass Projekte, Segmente und berechnete Metriken beschädigt werden.<p>**Hinweis**: Die [[!UICONTROL Personen]-Metrik, die mit der geräteübergreifenden Analyse verknüpft ist](/help/components/metrics/people.md), ist von dieser Ankündigung nicht betroffen. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des Endes der Nutzungsdauer von Reports &amp; Analytics werden [!UICONTROL Veröffentlichungslisten] voraussichtlich im **Dezember 2023** das Ende der Nutzungsdauer erreichen. Sie werden keine neuen [!UICONTROL Veröffentlichungslisten] erstellen oder auf bestehende [!UICONTROL Analysis Workspace]-Projekte zugreifen können, um diese zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an den für Ihre Organisation zuständigen Adobe-Kundenbetreuer. |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
