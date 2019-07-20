---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
seo-description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
seo-title: Intelligente Warnhinweise Überblick
title: Übersicht über intelligente Warnhinweise
uuid: b 9 bf 75 ad-bb 6 f -49 fe -8 c 55-355 ea 3 c 50 a 71
translation-type: tm+mt
source-git-commit: 2f06b402486d4162a968764b398e13893b4a7a75

---


# Übersicht über intelligente Warnhinweise

>[!Important]
>Die Verwendung von Daten mit Zeitstempel zum Erstellen von Warnungen kann dazu führen, dass Warnhinweise nicht korrekt ausgelöst werden. Es empfiehlt sich daher, intelligente Warnhinweise zu nutzen &gt; Daten ohne Zeitstempel.

Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.

[Intelligente Warnhinweise auf youtube](https://www.youtube.com/watch?v=UVH9xr_2REA&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&index=65) (5:34)

## Überblick {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

Die neuen Funktionen „Warnhinweiserstellung“ und „Warnhinweis-Manager“ in Analysis Workspace ersetzen die bisherigen Funktionen in Reports &amp; Analytics. Mithilfe intelligenter Warnhinweise können Sie

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter).
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird.
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken.
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Das neue Warnhinweissystem enthält die folgenden Komponenten: Warnhinweiserstellung, Alert-Manager, Warnhinweisvorschau und einen besseren kontextbezogenen Zugriff für das Erstellen von Warnhinweisen. Die Benutzeroberfläche für das alte Warnhinweissystem wird nicht mehr zur Verfügung stehen, die Warnhinweise werden jedoch migriert. Einige alte Warnhinweisfunktionen [werden nicht mehr zur Verfügung stehen](https://marketing.adobe.com/resources/help/en_US/sc/user/deprecated_alerts.html).

Es gibt vier Möglichkeiten, in die Warnhinweiserstellung zu gelangen:

* Mithilfe der folgenden Tastenkombination in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* By going directly to the Alert Builder:  **[!UICONTROL Workspace]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL New Alert]** .
* Indem Sie ein oder mehrere Freiform-Tabellenzeilenelemente auswählen, mit der rechten Maustaste klicken und **[!UICONTROL Warnhinweis aus Auswahl erstellen auswählen]**. Dadurch wird die Warnhinweiserstellung geöffnet, und die entsprechenden Metriken und angewendeten Filter aus der Tabelle werden automatisch eingetragen sein. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten.

   ![](assets/create-alert-from-selection.png)

* From within a Reports &amp; Analytics report, by going to  **[!UICONTROL More]** &gt; **[!UICONTROL Add Alert]** . Dadurch wird die neue Warnhinweiserstellung geöffnet, und die entsprechenden Metriken und angewendeten Filter aus dem Bericht werden automatisch eingetragen sein. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten.

   ![](assets/add-alert.png)

## FAQ: How alerts are calculated and triggered {#section_1F3B1DAF21784306953B49AAD4C3DCAB}

Bei den prozentualen Schwellenwerten handelt es sich um Standardabweichungen. Beispiel: 95 % = 2 Standardabweichungen und 99 % = 3 Standardabweichungen. Je nach der von Ihnen ausgewählten Zeitgranularität [werden verschiedene Modelle](../../../analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md#concept_0705DC91F0F44951AC2226EC846E824C) verwendet, um zu berechnen, wie weit jeder Punkt von der Norm entfernt ist (Anzahl der Standardabweichungen). Wenn Sie einen niedrigeren Schwellenwert festlegen (z. B. 90 %), erhalten Sie mehr Anomalien als bei einem höheren Schwellenwert (99 %). Die Schwellenwerte 99,75 % und 99,99 % wurden speziell für die Granularität „Stündlich“ eingeführt, damit nicht allzu viele Anomalien ausgelöst werden.

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
   <td colname="col2"> <p>Der Trainingszeitraum hängt von der ausgewählten Granularität ab. (Weitere Informationen finden Sie unter <a href="../../../analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md#concept_0705DC91F0F44951AC2226EC846E824C" format="dita" scope="local"> Statistische Verfahren, die in der Anomalieerkennung </a> für weitere Details verwendet werden.) Zusammenfassung: </p> 
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
   <td colname="col2"> <p>Nicht in Workspace, aber Sie können dazu Report Builder nutzen (siehe Video zum Thema <a href="https://www.youtube.com/watch?v=-a-8W6GQZnU" format="https" scope="external">Anomalieerkennung in Report Builder </a>). </p> <p>Beachten Sie, dass in Report Builder weniger ausgefeilte Methoden zur Anomalieerkennung angewandt werden. Es wird ein nicht konfigurierbarer Trainingszeitraum von 30 Tagen mit einem festgelegten 95-%-Intervall Training angewandt. Der Vorgang ist vergleichbar mit der <a href="https://marketing.adobe.com/resources/help/en_US/reference/anomaly.html" format="html" scope="external">Anomalieerkennung in Reports &amp; Analytics </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

