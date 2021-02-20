---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
title: Intelligente Warnhinweise
uuid: ac8c9710-d245-46e9-b906-32d3bb0013c0
translation-type: tm+mt
source-git-commit: 56ca9fa36db9d7dd126808280ba17f29f4b787d9
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 96%

---


# Intelligente Warnhinweise

Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.

## Überblick {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>Intelligente Warnhinweise sind nur für Kunden von Adobe [!DNL Analytics] Prime und Adobe [!DNL Analytics] Ultimate verfügbar.

Die neuen Funktionen „Warnhinweiserstellung“ und „Warnhinweis-Manager“ ersetzen die bisherigen Funktionen in Adobe [!DNL Analytics]. Mithilfe intelligenter Warnhinweise können Sie

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter).
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird.
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken.
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Das neue Warnhinweissystem enthält die folgenden Komponenten: Warnhinweiserstellung, Alert-Manager, Warnhinweisvorschau und einen besseren kontextbezogenen Zugriff für das Erstellen von Warnhinweisen. Die Benutzeroberfläche für das alte Warnhinweissystem wird nicht mehr zur Verfügung stehen, die Warnhinweise werden jedoch migriert. Einige alte Warnhinweisfunktionen [werden nicht mehr zur Verfügung stehen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/alerts.html).

Es gibt vier Möglichkeiten, in die Warnhinweiserstellung zu gelangen:

* Mithilfe des folgenden Tastaturbefehls in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* Indem Sie direkt zur Warnhinweiserstellung wechseln: **[!UICONTROL Workspace]** > **[!UICONTROL Komponenten]** > **[!UICONTROL neuer Warnhinweis]** .
* Indem Sie ein oder mehrere Freiform-Tabellenzeilenelemente auswählen, mit der rechten Maustaste klicken und **[!UICONTROL Warnhinweis aus Auswahl erstellen auswählen]**. Dadurch wird die Warnhinweiserstellung geöffnet, und die entsprechenden Metriken und angewendeten Filter aus der Tabelle werden automatisch eingetragen sein. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten.

   ![](assets/create-alert-from-selection.png)

* Indem Sie von einem [!UICONTROL Reports &amp; Analytics]-Bericht aus zu **[!UICONTROL Mehr]** > **[!UICONTROL Warnhinweis hinzufügen]** navigieren. Dadurch wird die neue Warnhinweiserstellung geöffnet, und die entsprechenden Metriken und angewendeten Filter aus dem Bericht werden automatisch eingetragen sein. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten.

   ![](assets/add-alert.png)

## FAQ: Wie werden Warnhinweise berechnet und ausgelöst?    {#section_1F3B1DAF21784306953B49AAD4C3DCAB}

Bei den prozentualen Schwellenwerten handelt es sich um Standardabweichungen. Beispiel: 95 % = 2 Standardabweichungen und 99 % = 3 Standardabweichungen. Je nach der von Ihnen ausgewählten Zeitgranularität  [werden verschiedene Modelle](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) verwendet, um zu berechnen, wie weit jeder Punkt von der Norm entfernt ist (Anzahl der Standardabweichungen). Wenn Sie einen niedrigeren Schwellenwert festlegen (z. B. 90 %), erhalten Sie mehr Anomalien als bei einem höheren Schwellenwert (99 %). Die Schwellenwerte 99,75 % und 99,99 % wurden speziell für die Granularität „Stündlich“ eingeführt, damit nicht allzu viele Anomalien ausgelöst werden.

<table id="table_B3AA85E1DE3543DCA34966A52E3CE4AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Frage: Wie weit reicht die Anomalieerkennung des Warnhinweises zur Ermittlung von Datenanomalien zurück?</b> </p> </td> 
   <td colname="col2"> <p>Der Trainingszeitraum hängt von der ausgewählten Granularität ab. Weitere Informationen finden Sie unter den statistischen Verfahren für die <a href="/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md">Anomalieerkennung</a>. Zusammenfassung: </p> 
    <ul id="ul_4F8C2A41F06C498DBF5E7AE5DE803773"> 
     <li id="li_E246091A3F1E484C8444AF4052FCA784">Monatlich = 15 Monate + derselbe Bereich im letzten Jahr </li> 
     <li id="li_CC014FB38AE1492B9647E990C29BFB3C">Wöchentlich = 15 Wochen + derselbe Bereich im letzten Jahr </li> 
     <li id="li_2517EE2097534324BE9C1B54CD181A62">Täglich = 35 Tage + derselbe Bereich im letzten Jahr </li> 
     <li id="li_710BC8B009354542AA4962A59A646099">Stündlich = 336 Stunden </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Frage: Wenn ich nur bei einem Rückgang bzw. nur bei einem Anstieg des Verhaltens einen Warnhinweis erhalten möchte, kann ich die Anomalieerkennung nutzen oder muss ich den Absolutwert verwenden?</b> </p> </td> 
   <td colname="col2"> <p>Bei Verwendung des Absolutwerts werden Warnhinweise sowohl bei einem Rückgang als auch bei einem Anstieg ausgelöst. Sie können keine gesonderten Warnhinweise nur für Rückgänge oder nur für Anstiege einrichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Frage: Kann ich Warnhinweise so konfigurieren, dass sie nur während bestimmten Uhrzeiten ausgelöst werden (z. B. zu Geschäftszeiten und Nicht-Geschäftszeiten)? </b> </p> </td> 
   <td colname="col2"> <p>Derzeit ist dies leider nicht möglich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Frage: Kann ich eine Tabelle der „erwarteten Werte“, die die gepunktete Linie ausmachen, oder eine andere Art von Darstellung dieser Werte erhalten? </b> </p> </td> 
   <td colname="col2"> <p>Nicht in Workspace, aber Sie können dazu Report Builder nutzen (siehe Video zum Thema <a href="https://docs.adobe.com/content/help/en/analytics-learn/tutorials/exporting/report-builder/anomaly-detection-in-report-builder.html"  >Anomalieerkennung in Report Builder </a>). </p> <p>Beachten Sie, dass in Report Builder weniger ausgefeilte Methoden zur Anomalieerkennung angewandt werden. Es verwendet eine feste 30-Tage-Schulungszeit, die ein 95%-Intervall festlegt. </p> </td> 
  </tr> 
 </tbody> 
</table>

