---
description: 'null'
subtopic: Alerts
title: Warnhinweise
topic: Reports and analytics
uuid: e1333a9b-eba0-45b7-b7e6-46e06190db64
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 100%

---


# Warnhinweise

## Warnhinweise {#concept_8AB25AF6FB52478DB98C1BA4577A2E16}

Intelligente Warnhinweise, das neue Warnhinweissystem für sämtliche Bereiche von Adobe Analytics, erlauben das Erstellen und Verwalten von Warnhinweisen, inklusive Warnhinweis-Vorschau und Regelbeiträgen. Sie können

* Warnhinweise erstellen, die auf Anomalien basieren (90 %, 95 % oder 99 % Schwellen, Änderungen in %, darüber/darunter).
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird.
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken.
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Über **[!UICONTROL Mehr]** > **[!UICONTROL Warnhinweise]** können Sie in allen Berichten in Reports &amp; Analytics auf das neue Warnhinweissystem zugreifen.

Weitere Informationen finden Sie in der Analysis Workspace-Dokumentation unter [Intelligente Warnhinweise](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html).

## Warnhinweis hinzufügen {#task_51187E8BF19544DDA9EF2057E6F11D35}

In diesen Schritten wird beschrieben, wie Sie Warnhinweise in Adobe Analytics hinzufügen.

<!-- 

t_add_an_alert.xml

 -->

Navigieren Sie zur neuen Warnhinweiserstellung im Menü **[!UICONTROL Analytics]** > **[!UICONTROL Komponenten]**. Sie können jedoch trotzdem aus Berichten in Reports &amp; Analytics darauf zugreifen:

1. Öffnen Sie in Reports &amp; Analytics den Bericht, für den Sie einen Warnhinweis einrichten möchten.
1. Klicken Sie auf **[!UICONTROL Mehr]** > **[!UICONTROL Warnhinweis hinzufügen]**.
1. Dadurch werden Sie zur [neuen Warnhinweiserstellung](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/alert-builder.html) geleitet.

## Bestehende Warnhinweise anzeigen oder bearbeiten {#task_2ADF2A05EB784B8BBAFE293AC8243C46}

Aufgabenkontext

1. Gehen Sie zu **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]**. Dadurch werden Sie zum neuen [Warnhinweis-Manager](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/alert-manager.html) geleitet.

## Migration veralteter Warnhinweise {#concept_7E8179F5EF6E4913B0CE5CF4FF186911}

Einige Funktionen von vorhandenen Analytics-Warnhinweisen sind im neuen Warnhinweis-Manager, der als Bestandteil des Analysis Workspace im Herbst 2016 veröffentlicht wird, nicht enthalten. In der folgenden Tabelle sind veraltete Warnhinweisfunktionen sowie einige Funktionen aufgeführt, die in anderer Form in den neuen Warnhinweis-Manager migriert werden.

<!-- 

deprecated_alerts.xml

 -->

<table id="table_9307013B16AC4AC7BFC6F4C440FCFDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veraltete Warnhinweisfunktion </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> Veraltet oder migriert? </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gesamt (Alle Elemente) </p> </td> 
   <td colname="col2"> <p>Warnhinweise für alle Elemente eines Dimensionsberichts erstellen. </p> </td> 
   <td colname="col3"> <p>Bei der Erstellung eines Warnhinweises für alle Elemente eines Dimensionsberichts ist das Ergebnis in manchen Fällen dasselbe wie bei einem Warnhinweis, der nur für die aggregierte Metrik (nicht auf eine Dimension angewendet) erstellt wird. Ein Beispiel: Sie erstellen einen monatlichen Warnhinweis für alle Elemente in der Metrik „Umsatz“. Sie würden dasselbe Ergebnis erhalten, wenn Sie nur den Umsatzbericht ausführen und dafür einen monatlichen Warnhinweis erstellen. </p> <p>Für solche Fälle ist der veraltete Warnhinweis „Gesamt (Alle Elemente)“ nicht länger verfügbar und wird in die letztgenannte, einfachere Möglichkeit migriert. </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Oberste 1000 Elemente </p> <p> </p> </td> 
   <td colname="col2"> <p>Warnhinweise für die obersten 1000 Elemente in einem Bericht erstellen. </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht mehr verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zeitbasierte Unique Visitors-Warnhinweise (tägliche, wöchentliche, monatliche etc. Unique Visitors) </p> <p> </p> </td> 
   <td colname="col2"> <p>Warnhinweise für stündliche, tägliche, wöchentliche und monatliche Unique Visitor-Berichte erstellen. </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager werden bestimmte zeitbasierte Unique Visitor-Warnhinweise nicht mehr unterstützt. Anstatt wie zuvor beispielsweise einen wöchentlichen Warnhinweis für Unique Visitors pro Tag zu erstellen, können Sie jetzt einen täglichen, wöchentlichen etc. fortlaufenden Warnhinweis für die Metrik „Unique Visitors“ erstellen. (Analysis Workspace unterstützt die Metrik „Unique Visitors“, jedoch keine täglichen/wöchentlichen/monatlichen/etc. Unique Visitors-Metriken.) </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durchsuchen </p> </td> 
   <td colname="col2"> <p>Warnhinweise für einen Dimensionsbericht mit angewendeter Suche erstellen. Gilt nur für „Gesamt“ („Alle Elemente“) oder „Oberste 1000 Elemente“. </p> <p> </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht mehr verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spezifische Berichte für Reports &amp; Analytics </p> </td> 
   <td colname="col2"> <p>Warnhinweise für diverse Berichte erstellen, die in Reports &amp; Analytics existieren und keinem Bericht in Analysis Workspace entsprechen, wie zum Beispiel 
     <ul id="ul_9A690970A5AE4ED39E664DF23EF3164F"> 
      <li id="li_E2F44EDBA1D945CEBAC4802ED714E7A1">JavaScript </li> 
      <li id="li_B847C6A988854F76824F099681705EC9">Path Length </li> 
      <li id="li_4AF656460BC748E8802FAF258D01842F">Bots </li> 
      <li id="li_A300D2803B244774839BEC23D3EB533A">Zeitzonen </li> 
      <li id="li_7A0B4CF92F4D47238B7B329EEC213322">Domänen auf oberster Ebene </li> 
     </ul> </p> <p> </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht mehr verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Warnhinweise mit ASI-Slot als Report Suite </p> </td> 
   <td colname="col2"> <p>Das Erstellen oder Bearbeiten von ASI-Slots ist nicht länger möglich und sie sind auch nicht in Analysis Workspace verfügbar. Daher werden sie von den neuen Warnhinweisen nicht unterstützt. </p> <p> </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Warnhinweise mit Teilnahmemetriken </p> </td> 
   <td colname="col2"> <p> <a href="https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/attribution/overview.html"  > Teilnahmemetriken</a> sind in Reports &amp; Analytics verfügbar, jedoch zur Zeit nicht im neuen Warnhinweissystem in Analysis Workspace. </p> <p> </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Monatliche Warnhinweise für benutzerdefinierte Kalender-Report Suites </p> </td> 
   <td colname="col2"> <p>Dies betrifft nur Kunden, die Warnhinweise für Report Suites mit <a href="https://docs.adobe.com/content/help/de-DE/analytics/analyze/report-builder/data-requests/date-ranges/custom-calendar.html"  >benutzerdefinierten Monatsanfängen</a> nutzen (National Retail Federation/NRF und benutzerdefinierte Kalendertypen). </p> <p>Es betrifft keine Warnhinweise für Report Suites mit gregorianischem oder modifiziertem gregorianischem Kalender. Bisher wurden diese Warnhinweise am ersten Tag des gregorianischen Monats gesendet (zum Beispiel am 1. Januar, am 1. Februar usw.). Dies ist mit der neuen Anomalieerkennungsfunktion für Warnhinweise nicht mehr möglich. Diese Funktion bezieht die Daten des vorangegangenen Monats in die Suche nach Anomalien ein. Zukünftig werden in unserer Terminplanung auch benutzerdefinierte Kalender unterstützt, damit für Warnhinweise und für geplante Projekte festgelegt werden kann, dass sie am ersten Tag des benutzerdefinierten Kalendermonats ausgelöst werden, und nicht nur am ersten Tag des gregorianischen Monats. </p> <p> </p> </td> 
   <td colname="col3"> <p>Im neuen Warnhinweis-Manager nicht verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Warnhinweise, die seit September 2015 nicht mehr ausgeführt wurden. </p> </td> 
   <td colname="col2"> <p>Wenn Warnhinweise seit September 2015 nicht mehr ausgeführt worden sind, kann es verschiedene Gründe geben, darunter: </p> 
    <ul id="ul_15812938A2454537AF6ADDB039DE16BC"> 
     <li id="li_D079A819CEE04F609AF18C09EEE83F0D">Sie haben im Warnhinweismanager für diesen Warnhinweis auf „Deaktivieren“ geklickt. </li> 
     <li id="li_E23D01FA0B1341AD8BC1DDD16FB1366F">Beim Warnhinweis treten Fehler auf und er wird nicht erfolgreich beendet. </li> 
    </ul> <p> </p> </td> 
   <td colname="col3"> Diese Warnhinweise werden nicht ins neue System migriert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Als „deaktiviert“ markierte Warnhinweise </td> 
   <td colname="col2"> Derzeit gibt es in der neuen Benutzeroberfläche keine Möglichkeit, Warnhinweise zu deaktivieren/erneut zu aktivieren, diese Funktion ist jedoch für die Zukunft vorgesehen. <p> </p> </td> 
   <td colname="col3"> Diese Warnhinweise werden nicht ins neue System migriert. </td> 
  </tr> 
 </tbody> 
</table>

