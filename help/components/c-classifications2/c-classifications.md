---
description: Eine Klassifizierung ist eine Möglichkeit, Analytics-Variablendaten zu kategorisieren und die Daten auf unterschiedliche Weise anzuzeigen, wenn Sie Berichte erzeugen.
seo-description: Eine Klassifizierung ist eine Möglichkeit, Analytics-Variablendaten zu kategorisieren und die Daten auf unterschiedliche Weise anzuzeigen, wenn Sie Berichte erzeugen.
seo-title: Informationen zu Classifications
solution: Analytics
subtopic: Classifications
title: Informationen zu Classifications
topic: Admin Tools
uuid: abc 1 a 1 be -8 e 37-4 b 7 e -81 fd -3 e 99 ac 27 fc 6 a
translation-type: tm+mt
source-git-commit: 2d01f9edb976a57c18641fea03e01ad029893eea

---


# Informationen zu Classifications

Eine Klassifizierung ist eine Möglichkeit, Analytics-Variablendaten zu kategorisieren und die Daten auf unterschiedliche Weise anzuzeigen, wenn Sie Berichte erzeugen.

Videoüberblick über [Analytics-Classifications](https://video.tv.adobe.com/v/16853/?captions=ger).

**[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Einstellungen bearbeiten]** &gt; *`<Traffic or Conversion>`*

Beim Klassifizieren bilden Sie eine Beziehung zwischen der Variablen und den Metadaten, die mit dieser Variable zusammenhängen. Classifications kommen am häufigsten in Kampagnen zum Einsatz. Die mit Variablen (eVars, Props und Ereignisse) erfassten Daten lassen sich durch Anwenden von Metadaten zusammenfassen.

![Schritt-Info](assets/sub_class_create.png)

Nach der Classification kann jeder Bericht, den Sie mithilfe der Schlüsselvariable erstellen können, auch mithilfe der zugeordneten Attribute erstellt werden. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Durch die Erweiterung der Reports &amp; Analysen-Daten um zusätzliche Attribute werden tiefergehende und komplexere Berichte möglich.

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juni 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

>[!NOTE]
>
>In der Analytics Maintenance Release vom 10. Mai 2018 wurde Adobe gestartet, um die Funktionalität von datumsaktivierten und numerischen Klassifizierungen zu beschränken. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und Numerisch-Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

Nach dem Erstellen der Klassifizierungen können Sie die neuen Datenattribute in Adobe Analytics nutzen.

**Beispiel zu Trackingcodes**

Angenommen, Sie möchten die Kampagnen nicht nur nach dem Trackingcode betrachten, sondern die Kampagnenergebnisse sollen nach Suchmaschinen, Keywords und Kampagnenkanälen angezeigt werden. In diesem Fall muss nicht jeweils eine Konversionsvariable festgelegt werden. Stattdessen können Sie drei Classifications der Kampagnenvariable für Suchmaschine, Keyword und Kampagnenkanal anlegen. Mit dieser Strategie werden die Erfolgsereignisse der Website ohne zusätzliches Tagging nach allen vier Variablen dargestellt.

Die Reports &amp; Analysen Funktion beinhaltet vordefinierte Classifications für die Trackingcode-Variable, mit der Classification-Basierte Berichte namens „Kreative Elemente“ und „Kampagnen“ erstellt werden können. Für alle anderen Konversion- und Traffic-Variablen müssen Sie die Classifications manuell konfigurieren.

Weitere Informationen finden Sie unter [Traffic-Classifications](/help/admin/admin/c-traffic-variables/traffic-classifications.md) und [Konversion-Classifications](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=conversion_classifications).

In der folgenden Tabelle werden die verschiedenen verfügbaren Classification-Typen und die Variablentypen, die sie unterstützen, beschrieben. Beachten Sie die Informationen unter [Allgemeine Dateistruktur](../../components/c-classifications2/c-classifications-importer/c-saint-data-files.md#concept_9EFF968DF5D244A887DE94075431C1BE) vor dem Hochladen von Datendateien.

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
   <td colname="col2"> <p>Konversion- und Traffic-Variablen </p> </td> 
   <td colname="col3"> <p>Text-Classifications definieren eine Kategorie, mit der Sie unterschiedliche Daten zu Berichtzwecken gruppieren können. </p> <p>Wenn Sie beispielsweise Hemden verkaufen, möchten Sie möglicherweise den Hemdenverkauf (Konversionen) nach Farbe, Größe und Stil kategorisieren, um Berichte zu erstellen, in denen die Hemdenverkäufe nach diesen Kategorien organisiert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Datumsaktivierter Text</span> </p> <p>Hinweis: In der Analytics Maintenance Release vom 10. Mai 2018 wurde Adobe gestartet, um die Funktionalität von datumsaktivierten Classifications zu beschränken. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung. </p> </td> 
   <td colname="col2"> <p>Konversionsvariablen </p> </td> 
   <td colname="col3"> <p>Mit einer datumsaktivierten Text-Classification können Sie einer Text-Classification Datumsbereiche zuweisen. Dies wird üblicherweise bei Kampagnen-Classifications gemacht, damit Sie die Vorteile der Gantt-Diagrammansicht im <span class="wintitle">Kampagnen</span>bericht nutzen können. </p> <p>Sie können die Datumsangaben der Kampagne in die Datendatei aufnehmen, mit der die Classification-Daten bestückt werden. </p> <p>Reports &amp; Analysen sammelt Kampagnen-Trackingcodes auch dann, wenn das Enddatum der Kampagne bereits erreicht ist. Die nach dem Enddatum der Kampagne gesammelten Daten sind jedoch nicht mit der Kampagne verknüpft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Nummerisch</span> <p>Hinweis: In der Analytics Maintenance Release vom 10. Mai 2018 hat Adobe begonnen, die Funktionalität numerischer Klassifizierungen einzuschränken. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen numerischen Klassifizierungen hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung. </p> </p> </td> 
   <td colname="col2"> <p>Konversionsvariablen </p> </td> 
   <td colname="col3"> <p>Mit nummerischen Classifications können Sie feste nummerische Werte auf <span class="wintitle">Konversions</span>berichte anwenden. Diese Classifications werden als Metriken in Berichten angezeigt. </p> <p>Bei der Erwägung, ob eine <span class="wintitle">nummerische</span> Classification hinzugefügt werden soll, muss der nummerische Wert fest eingestellt sein und darf sich im Laufe der Zeit nicht verändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

