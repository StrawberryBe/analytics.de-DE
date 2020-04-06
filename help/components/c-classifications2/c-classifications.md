---
description: Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, sobald Sie einen Bericht erzeugen.
subtopic: Classifications
title: Informationen über Klassifizierungen
topic: Admin tools
uuid: abc1a1be-8e37-4b7e-81fd-3e99ac27fc6a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Informationen über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, sobald Sie einen Bericht erzeugen.

Videoüberblick über [Analytics-Classifications](https://video.tv.adobe.com/v/16853/?captions=ger).

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > *`<Traffic or Conversion>`*

Beim Klassifizieren erstellen Sie eine Beziehung zwischen der Variablen und den Metadaten, die sich auf diese Variable beziehen. Classifications werden am häufigsten in Kampagnen verwendet. Daten, die mithilfe von Variablen (eVars, Props und Ereignisse) erfasst werden, können aggregiert werden, indem Metadaten auf die in den Variablen erfassten Werte angewendet werden.

![Schritt-Info](assets/sub_class_create.png)

Nach der Klassifizierung kann jeder Bericht, den Sie mit der Schlüsselvariablen erstellen können, auch mit den zugehörigen Attributen erstellt werden. Sie können beispielsweise [!UICONTROL Product IDs] mit weiteren Produktattributen klassifizieren, wie Produktname, Farbe, Größe, Beschreibung und SKU. Die Erweiterung von Berichte- und Analysedaten um zusätzliche Attribute bietet tiefere und komplexere Berichte.

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juni 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert, und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

>[!NOTE] Nach der Analytics-Wartungsversion vom 10. Mai 2018 schränkte Adobe die Funktion für datumsaktivierte und numerische Classifications ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und numerischen Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

Nach dem Erstellen der Klassifizierungen können Sie die neuen Datenattribute im gesamten Adobe Analytics nutzen.

**Beispiel zu Trackingcodes**

Angenommen, Sie möchten die Kampagnen nicht nur nach dem Rückverfolgungscode, sondern nach Suchmaschine, Suchbegriff und Kampagne Kanal anzeigen. Anstatt Konversionsvariablen für jede dieser Variablen zu verwenden, können Sie drei Klassifizierungen der Variablen &quot;Kampagne&quot;erstellen, um die Kanal &quot;Suchmaschine&quot;, &quot;Suchbegriff&quot;und &quot;Kampagne&quot;zu repräsentieren. Mit dieser Strategie können Sie die Site-Erfolgsvariablen ohne zusätzliches Tagging nach allen vier Ereignissen anzeigen.

Berichte and Analytics umfasst vordefinierte Classifications für die Trackingcode-Variable, die Angebot Classification-basierte Berichte mit den Namen Kreative Elemente und Kampagnen enthält. Sie müssen Classifications für alle anderen Konversions- und Traffic-Variablen manuell konfigurieren.

Siehe [Traffic-Klassifizierungen](/help/admin/admin/c-traffic-variables/traffic-classifications.md) und [Umrechnungsklassifizierungen](https://marketing.adobe.com/resources/help/de_DE/reference/conversion_classifications.html).

In der folgenden Tabelle werden die verschiedenen verfügbaren Classification-Typen und die Variablentypen, die sie unterstützen, beschrieben. Beachten Sie die Informationen unter  [Allgemeine Dateistruktur](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) vor dem Hochladen von Datendateien.

<table id="table_279728C28D9C40EE832ACC9F211B5F17"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>TYP </p> </th> 
   <th colname="col2" class="entry"> <p>VERFÜGBARKEIT </p> </th> 
   <th colname="col3" class="entry"> <p>BESCHREIBUNG </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Text</span> </p> </td> 
   <td colname="col2"> <p>Konversions- und Traffic-Variablen </p> </td> 
   <td colname="col3"> <p>Textklassifizierungen definieren eine Kategorie, mit der Sie Variablendaten zu Berichten gruppieren können. </p> <p>Wenn Sie z. B. Hemden verkaufen, sollten Sie den Hemdverkauf (Konversionen) nach Farbe, Größe und Stil kategorisieren, um Berichte zu erstellen, die Ihnen die von diesen Kategorien organisierten Hemdverkäufe anzeigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Datumsaktivierter Text</span> </p> <p>Hinweis: Seit der Analytics-Wartungsversion vom 10. Mai 2018 schränkt Adobe die Funktion für datumsaktivierte Klassifizierungen ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten Klassifizierungen hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung. </p> </td> 
   <td colname="col2"> <p>Konversionsvariablen </p> </td> 
   <td colname="col3"> <p>Mit einer datumsaktivierten Textklassifizierung können Sie einer Textklassifizierung Datumsbereiche zuweisen. Dies wird üblicherweise bei Kampagnen-Classifications gemacht, damit Sie die Vorteile der Gantt-Diagrammansicht im <span class="wintitle">Kampagnen</span> bericht nutzen können. </p> <p>Sie können die Datumsangaben der Kampagne in die Datendatei aufnehmen, mit der die Classification-Daten bestückt werden. </p> <p>Reports &amp; Analytics sammelt Kampagnen-Trackingcodes selbst dann, wenn das Enddatum der Kampagne bereits erreicht wurde. Die nach Ende der Kampagne gesammelten Daten werden jedoch nicht der Kampagne zugeordnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Numerisch</span> <p>Hinweis: Seit der Analytics-Wartungsversion vom 10. Mai 2018 schränkt Adobe die Funktion für numerische Klassifizierungen ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen numerischen Klassifizierungen hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung. </p> </p> </td> 
   <td colname="col2"> <p>Konversionsvariablen </p> </td> 
   <td colname="col3"> <p>Mit numerischen Classifications können Sie feste numerische Werte auf <span class="wintitle">Konversions</span> berichte anwenden. Diese Classifications werden als Metriken in Berichten angezeigt. </p> <p>Bei der Erwägung, ob eine <span class="wintitle">numerische</span> Classification hinzugefügt werden soll, muss der numerische Wert fest eingestellt sein und darf sich im Laufe der Zeit nicht verändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

