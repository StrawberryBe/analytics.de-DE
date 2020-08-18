---
description: Klassifizierungen werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie „Popmusikbegriffe“ kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.
subtopic: Classifications
title: Konversionsklassifizierungen
topic: Admin tools
uuid: 4c8726c9-f527-44e1-be01-8c7b3b5c20f0
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---


# Konversionsklassifizierungen

Klassifizierungen werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie „Popmusikbegriffe“ kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.

## Konversionsklassifizierungen {#concept_B4B1478A8CB540599AC9D4A58CA4B6FE}

Klassifizierungen werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie *Popmusikbegriffe* kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthrough-Raten genannt) und Konversion in Erfolgsereignisse berichten.

Mit Konversion-Classifications können Sie Konversionsvariablen klassifizieren. Nach der Classification kann jeder Bericht, den Sie mithilfe der wichtigen Daten erstellen können, auch mithilfe der verbundenen Dateneigenschaften erstellt werden.

Nach der Aktivierung der Classifications verwenden Sie den [Classification Importer](/help/components/classifications/importer/c-working-with-saint.md), um bestimmte Werte der entsprechenden Classification zuzuweisen.

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

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**. 
1. Report Suite auswählen.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Konversion-Classifications]**. 
1. Wählen Sie in der Dropdownliste **[!UICONTROL Einen Klassifizierungstyp auswählen]** die Variable aus, der Sie eine Klassifizierung hinzufügen möchten.

   ![Schritt-Info](assets/sub_class_create.png)

1. Bewegen Sie den Mauszeiger über das Symbol **[!UICONTROL Klassifizierung bearbeiten]** und wählen Sie dann **[!UICONTROL Klassifizierung hinzufügen]**.
1. Wählen Sie im Feld **[!UICONTROL Typ auswählen]** den Klassifizierungstyp aus, den Sie der Variablen hinzufügen möchten.

   Zu den Optionen gehören **[!UICONTROL Text]** und **[!UICONTROL Numerisch]**. Weitere Informationen zu Klassifizierungstypen finden Sie unter [Informationen über Klassifizierungen](/help/components/classifications/c-classifications.md).
1. Konfigurieren Sie die Klassifizierung im Dialogfeld **[!UICONTROL Textklassifizierungen]** nach Bedarf.

   Weitere Informationen zu diesen Elementen finden Sie unter [Konversion-Classifications – Beschreibungen](/help/components/classifications/conversion-classifications.md#section_4A98DD5F5C314B9DAEE710AEE4EE51D4).

1. Fügen Sie im Dialogfeld **[!UICONTROL Dropdown-Liste]** Optionen hinzu oder entfernen Sie Optionen.

   Durch Hinzufügen von Optionen wird eine Liste mit für diese Classification verfügbaren Classification-Werten erstellt. Diese Option kann zusammen mit Kampagnenvariablen verwendet werden, um den Benutzern eine Liste mit unterstützten Werten für die Classification im Kampagnen-Manager bereitzustellen. Verwenden Sie dies für Classification-Dimensionen, bei denen eine kleine Zahl erlaubter Werte vorliegt, die sich selten oder nie ändern. Sie können zum Beispiel verschiedene Kampagnen durchführen, die auf verschiedene Stufen der Kundenbindung ausgerichtet sind: Silber, Gold und Platin. Sie können dann Dropdown-Listen verwenden, um sicherzustellen, dass nur solche Werte akzeptiert werden, die Ihren drei Stufen entsprechen. Der Versuch, einen anderen Wert zu verwenden, wird verworfen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Löschen von Konversions-Classifications {#task_566651BC245944618A6A833E58211FDE}

<!-- 

t_classification_delete_conversion.xml

 -->

Löschen Sie nicht mehr benötigte Konversion-Classifications.

1. Öffnen Sie den Report Suite Manager, indem Sie in der Suite-Kopfzeile auf **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** klicken.
1. Report Suite auswählen.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Konversion-Classifications]**. 
1. Wählen Sie in der Dropdownliste **[!UICONTROL Einen Klassifizierungstyp auswählen]** die Variable aus, in der Sie eine Klassifizierung löschen möchten.
1. Bewegen Sie den Mauszeiger über das Symbol **[!UICONTROL Klassifizierung bearbeiten]** und wählen Sie dann **[!UICONTROL Klassifizierung löschen]**.
1. Klicken Sie im Dialogfeld „Klassifizierung löschen“ auf **[!UICONTROL Löschen]**.
