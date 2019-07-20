---
description: Classifications werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie „Popmusikbegriffe“ kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.
seo-description: Classifications werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie „Popmusikbegriffe“ kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.
seo-title: Umrechnungsklassifizierungen
solution: Analytics
subtopic: Classifications
title: Umrechnungsklassifizierungen
topic: Admin Tools
uuid: 4 c 8726 c 9-f 527-44 e 1-be 01-8 c 7 b 3 b 5 c 20 f 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Umrechnungsklassifizierungen

Classifications werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie „Popmusikbegriffe“ kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.

## Conversion classifications {#concept_B4B1478A8CB540599AC9D4A58CA4B6FE}

Classifications werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie *Popmusikbegriffe* kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.

Mit Konversion-Classifications können Sie Konversionsvariablen klassifizieren. Nach der Classification kann jeder Bericht, den Sie mithilfe der wichtigen Daten erstellen können, auch mithilfe der verbundenen Dateneigenschaften erstellt werden.

Nach der Aktivierung der Classifications verwenden Sie den [Classification Importer](../../components/c-classifications2/c-classifications-importer/c-working-with-saint.md#concept_08ED8C7A86C64E7DA5DE3044BB94B2EA), um bestimmte Werte der entsprechenden Classification zuzuweisen.

## Konversion-Classifications – Beschreibungen {#section_4A98DD5F5C314B9DAEE710AEE4EE51D4}

<table id="table_0B72C485467348E2A34BF913441F4AF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Name</span> </td> 
   <td colname="col2"> Der Name der Classification. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Datum aktiviert (nur Text)</span> </td> 
   <td colname="col2"> <p>Gibt an, ob die Text-Classification ein Datumsbereich für die Kampagnenvariablen ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Optionen (nur Text)</span> </td> 
   <td colname="col2">Erstellt eine Liste mit für diese Classification verfügbaren Werten. <span class="wintitle">„Optionen“</span> kann zusammen mit Kampagnenvariablen verwendet werden, um den Benutzern eine Liste mit unterstützten Werten für die Classification im <span class="wintitle">„Kampagnen-Manager“</span> bereitzustellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Zahlentyp (nur nummerisch)</span> </td> 
   <td colname="col2">Gibt den Typ der Zahl in der nummerischen Classification an. Zu den Optionen gehören <span class="wintitle">Nummerisch</span>, <span class="wintitle">Prozent</span> und <span class="wintitle">Währung</span>. </td> 
  </tr> 
 </tbody> 
</table>

## Konversion-Classifications hinzufügen {#task_D535D09E3EAF4CD1A15A6B93C0BB1BB5}

<!-- 

t_classification_conversion.xml

 -->

Schritte, die beschreiben, wie Konversion-Classifications in der Admin-Konsole hinzugefügt werden.

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL Conversion Classifications]**.
1. Wählen Sie in der Dropdownliste **„Einen Klassifizierungstyp auswählen“** die Variable aus, der Sie eine Klassifizierung hinzufügen möchten.

   ![Schritt-Info](assets/sub_class_create.png)

1. Mouse over the **[!UICONTROL Edit Classification]** icon, then select **[!UICONTROL Add Classification]**.
1.  Wählen Sie im Feld **Typ auswählen** den Klassifizierungstyp aus, den Sie der Variablen hinzufügen möchten.

   Options include **[!UICONTROL Text]** and **[!UICONTROL Numeric]**. For more information on classification types, see [About Classifications](../../components/c-classifications2/c-classifications.md#concept_4CEC7FF1A9E24204A7DA6B9AC70709DE).
1. In the **[!UICONTROL Text Classifications]** dialog box, configure the classification as desired.

   Weitere Informationen zu diesen Elementen finden Sie unter [Konversion-Classifications – Beschreibungen](../../components/c-classifications2/conversion-classifications.md#section_4A98DD5F5C314B9DAEE710AEE4EE51D4).

1. In the **[!UICONTROL Dropdown List]** dialog box, add or remove options.

   Durch Hinzufügen von Optionen wird eine Liste mit für diese Classification verfügbaren Classification-Werten erstellt. Diese Option kann zusammen mit Kampagnenvariablen verwendet werden, um den Benutzern eine Liste mit unterstützten Werten für die Classification im Kampagnen-Manager bereitzustellen. Verwenden Sie dies für Classification-Dimensionen, bei denen eine kleine Zahl erlaubter Werte vorliegt, die sich selten oder nie ändern. Sie können zum Beispiel verschiedene Kampagnen durchführen, die auf verschiedene Stufen der Kundenbindung ausgerichtet sind: Silber, Gold und Platin. Sie können dann Dropdown-Listen verwenden, um sicherzustellen, dass nur solche Werte akzeptiert werden, die Ihren drei Stufen entsprechen. Der Versuch, einen anderen Wert zu verwenden, wird verworfen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Löschen von Konversions-Classifications {#task_566651BC245944618A6A833E58211FDE}

<!-- 

t_classification_delete_conversion.xml

 -->

Löschen Sie nicht mehr benötigte Konversion-Classifications

1. Open the Report Suite Manager by clicking **[!UICONTROL Admin]**&gt; **[!UICONTROL Report Suites]** in the Suite header.
1. Wählen Sie eine Report Suite aus.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL Conversion Classifications]**.
1. Wählen Sie in der Dropdownliste **„Einen Klassifizierungstyp auswählen“** die Variable aus, in der Sie eine Klassifizierung löschen möchten.
1. Mouse over the **[!UICONTROL Edit Classification]** icon, then select **[!UICONTROL Delete Classification]**.
1. In the Delete Classification dialog box, click **[!UICONTROL Delete]**.
