---
description: Konfigurieren Sie die globalen Verhaltenseinstellungen. Sie können beispielsweise die Einstellungen zum automatischen Speichern sowie für Diagramme und Tabellen konfigurieren und die Schriftart und das Gebietsschema einstellen.
title: Einstellungen
uuid: 34444052-479b-4923-b379-a03ca614bf3e
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 98%

---


# Einstellungen

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 in den Status als lebensbedrohlich. [Weitere Infos...](https://adobe.ly/discoverworkspace).

Konfigurieren Sie die globalen Verhaltenseinstellungen. Sie können beispielsweise die Einstellungen zum automatischen Speichern sowie für Diagramme und Tabellen konfigurieren und die Schriftart und das Gebietsschema einstellen.

## Einstellungen {#concept_D21E3D6F13EA4F97913F60C243B72173}

Konfigurieren Sie die globalen Verhaltenseinstellungen. Sie können beispielsweise die Einstellungen zum automatischen Speichern sowie für Diagramme und Tabellen konfigurieren und die Schriftart und das Gebietsschema einstellen.

Klicken Sie auf **[!UICONTROL Tools]** > **[!UICONTROL Einstellungen]**, um die [!UICONTROL Globalen Einstellungen] aufzurufen.

## Registerkarte „Allgemeine Einstellungen“ – Definitionen {#reference_EADAF83466994F89BCC6B0F49A9A53DB}

Konfigurieren Sie die Verhaltenseinstellungen für Datenquellen, das Speichern von Projekten, Diagramme und Tabellen.

<!-- 

r_dsc_general_settings.xml

 -->

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Feld </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Dateneinstellungen </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Wiederholte Instanzen zählen</span>: Gibt an, ob Instanzen in Berichten gezählt werden. Wenn mehrere sequentielle Werte für dieselbe Variable vorhanden sind, können Sie sie entweder als eine oder mehrere Instanzen der Variable zählen. </p> <p>Beispiel: Sie können wiederholte Seitenneuladungen anzeigen. Hierbei handelt es sich um die Anzahl an Neuladungen oder Aktualisierungen von Seiten während eines Besuchs. Mit dieser Option können Sie angeben, ob mehrere Treffer auf derselben Seite als ein Treffer oder mehrere Seitenansichten gezählt werden. </p> <p> <span class="uicontrol"> <span class="keyword"> Ad Hoc</span> </span>: Hiermit legen Sie <span class="keyword">Ad Hoc</span> als einzige Datenquelle zur Berichterstellung fest. Diese Daten stammen aus Bildanfragen, die von Webseiten erzeugt wurden. </p> <p> <span class="uicontrol"> <span class="keyword">Data Sources</span></span>: Hiermit legen Sie fest, ob Daten, die aus anderen Adobe-Quellen oder benutzerspezifischen Datenquellen hochgeladen wurden, verwendet werden sollen. Diese Daten sind für Produkte in <span class="keyword">Experience Cloud</span> verfügbar. Weitere Informationen finden Sie unter <a href="https://docs.adobe.com/content/help/de-DE/analytics/import/data-sources/datasrc-home.html"  >Data Sources</a>. </p> <p> <span class="uicontrol"> Beides</span>: (Standard) Verwendet Daten von <span class="keyword">Ad Hoc Analysis</span> und anderen Datenquellen. </p> <p>Hinweis: Eine Änderung dieser Optionen kann zu Abweichungen in den Berichten zwischen den Daten von <span class="keyword">Ad Hoc Analysis</span> und den Daten von <span class="keyword">Marketing Reports and Analytics</span> führen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Einstellungen für automatisches Speichern </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Automatisches Speichern aktiviert</span>: Die Funktion zum automatischen Speichern wird aktiviert. </p> <p> <span class="uicontrol"> Häufigkeit des automatischen Speichervorgangs für das Projekt</span>: Hier können Sie die Zeitabstände zwischen automatischen Speichervorgängen einstellen. Projekte werden nur bei Ad-hoc-Abstürzen automatisch gespeichert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Diagrammeinstellungen </p> </td> 
   <td colname="col2"> <p><b>Diagramme standardmäßig ausblenden</b>: Klicken Sie auf diese Schaltfläche, um Berichte ohne Diagramm im oberen Teil anzuzeigen. Mit dieser Option können Sie einen angezeigten Bericht manuell erweitern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Tabelleneinstellungen </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Zeilennummern anzeigen</span>: Schaltet die Zeilennummerierung in der Berichtstabelle ein bzw. aus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Registerkarte „Rangansicht“ – Definitionen {#reference_FB9BADD7E3DA42C1BB2A02A6E9D5C1CF}

Konfigurieren Sie, wie Daten in Spalten angezeigt werden, und wählen Sie Standardmetriken für Traffic- und Konversionsberichte aus.

<!-- 

r_dsc_ranked_tab.xml

 -->

| Feld | Definition |
|--- |--- |
| Spalteneinstellungen | Konfigurieren Sie, wie Sie Zellendaten in Tabellen und Balkendiagrammen in Diagrammen anzeigen möchten. |
| Standardmetriken auswählen | Geben Sie zusätzlich zu den für alle Berichte verfügbaren Metriken Standardmetriken für Traffic- und Konversionsberichte an.    Berichtspezifischen Standard einbeziehen: Gibt an, ob Standardmetriken beim Anpassen der Ansicht einbezogen werden sollen. |

## Registerkarte „Site-Analyse“ – Definitionen {#reference_9DD37C8EF718409E990E149596282FF8}

Konfigurieren Sie die Metriken und andere Grafikeinstellungen für den Site-Analysebericht.

<!-- 

r_dsc_site_analysis_tab.xml

 -->

| Feld | Definition |
|--- |--- |
| Metriken | Wählen Sie die durch Säulenbreite und -höhe dargestellten Metriken aus. Bestimmen Sie, welche Metrik farbig dargestellt werden soll. Sie können die Farben zur Darstellung hoher bzw. niedriger Metrikwerte festlegen. Sie können die Metriken für die X- und Y-Achsen bestimmen sowie weitere Metriken hinzufügen, die im Popup-Text des Berichts angezeigt werden sollen. Sie können die einzelnen Metriken zu Ansichtszwecken auch invertieren. |
| Allgemein und Warnhinweise | Hier können Sie bestimmte grafische Elemente des Berichts aktivieren und deaktivieren. Sie können außerdem Warnhinweise konfigurieren, die im Bericht erscheinen, wenn Metriken zu den als Säulen dargestellten Seiten einen bestimmten Wert unter- bzw. überschreiten. |

## Registerkarte „Schriftart und Gebietsschema“ – Definitionen {#reference_5F2129B67CC44E5BA9EA7E30A35BFB49}

Legen Sie die regionalen Spracheinstellungen sowie die Standardschrift fest. Um die Änderungen an der Schriftart und dem Gebietsschema zu übernehmen, müssen Sie neu starten.

<!-- 

r_dsc_font_locale.xml

 -->

| Feld | Definition |
|--- |--- |
| Ausgangsort auswählen | Legen Sie die Sprache fest, in der die Benutzeroberfläche angezeigt wird. |
| Schriftart auswählen | Hier können Sie die Schriftart der Darstellung auswählen. |
