---
description: Data Warehouse bezieht sich auf die Kopie der Analytics-Daten für Speicherberichte und benutzerspezifische Berichte, die Sie durch Filtern der Daten ausführen können. Sie können Berichte anfordern, die auf Ihre individuellen Fragen erweiterte Datenbeziehungen aus Rohdaten anzeigen. Data Warehouse-Berichte werden per E-Mail oder über FTP versendet. Die Verarbeitung von Data Warehouse-Berichten kann bis zu 72 Stunden dauern. Die Verarbeitungsdauer ist abhängig von der Komplexität der Abfrage und der Menge der zu verarbeitenden Daten.
title: Data Warehouse-Übersicht
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 100%

---

# Data Warehouse-Übersicht

Data Warehouse bezieht sich auf die Kopie der Analytics-Daten für Speicherberichte und benutzerspezifische Berichte, die Sie durch Filtern der Daten ausführen können. Sie können Berichte anfordern, die auf Ihre individuellen Fragen erweiterte Datenbeziehungen aus Rohdaten anzeigen. Data Warehouse-Berichte werden per E-Mail oder über FTP versendet. Die Verarbeitung von Data Warehouse-Berichten kann bis zu 72 Stunden dauern. Die Verarbeitungsdauer ist abhängig von der Komplexität der Abfrage und der Menge der zu verarbeitenden Daten.

Adobe aktiviert Data Warehouse nur für Benutzer auf Administratorebene und nur für bestimmte Report Suites. (Die Funktion kann für globale und untergeordnete Report Suites, jedoch nicht für Datenaggregations-Report Suites aktiviert werden.) Der Administrator kann eine Gruppe erstellen, die Zugriff auf Data Warehouse hat, und anschließend Benutzer, die sich nicht auf Administrator-Ebene befinden, dieser Gruppe zuweisen.

Data Warehouse ZIP-komprimiert automatisch Dateien, die größer als 1 MB sind. Die Maximalgröße für E-Mail-Anhänge beträgt 10 MB.

Data Warehouse kann eine unbegrenzte Anzahl an Zeilen in einer einzigen Anforderung für einzelne terminierte und heruntergeladene Berichte verarbeiten.

>[!NOTE]
>
>Data Warehouse gibt in Berichten den ersten aufgefundenen Wert innerhalb des Berichtszeitraums aus.

>[!IMPORTANT]
>
>Bei der Segmentierung nach klassifizierten Werten behandeln Analysis Workspace und Data Warehouse „nicht spezifizierte“ Werte unterschiedlich. „Nicht spezifiziert“ in Workspace bezieht sich auf Werte, die nicht klassifiziert sind, während „nicht spezifiziert“ in Data Warehouse auf Werte verweist, die Sie als „nicht spezifiziert“ klassifiziert haben.

## Data Warehouse-Anforderungen – Beschreibungen {#section_F21C78ED36884C389C852E876AF5CDE8}

In dieser Tabelle werden die Felder und Optionen in dem Register [!UICONTROL Data Warehouse-Anforderung] beschrieben.

<table id="table_7325A2466866460E8B0AF7D696152713"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Anforderungsname</span> </td> 
   <td colname="col2"> Bezeichnet die Anforderung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Berichtsdatum</span> </td> 
   <td colname="col2"> <p>Datum und Granularität der Anforderung. </p> 
    <ul id="ul_C00F4529BD9E4113B517A61751B1DD5C"> 
     <li id="li_4D7C26812DF94ED7B64F985309541F46"> <span class="wintitle"> Benutzerspezifisch</span>: Ein Datumsbereich, den Sie im Kalender konfigurieren. </li> 
     <li id="li_2B272087006847148A936350D1B2D523"> <span class="wintitle"> Voreingestellt</span>: Ein voreingestellter Bereich. Der voreingestellte Bereich steht im Verhältnis zum Berichtsdatum. </li> 
     <li id="li_745989965BB94D489FF7046587E13C42"> <span class="wintitle"> Granularität</span>: Die Zeitgranularität. Gültige Werte sind „Keine“, „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“ und „Jahr“. </li> 
    </ul> <p>Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Verfügbare Segmente</span> </td> 
   <td colname="col2"> <p>Hier können Sie den Teil der Besucher auswählen, den Sie untersuchen und weiter segmentieren möchten. Sie können vorkonfigurierte Segmente laden, neue Segmente erstellen und Segmentkomponenten in einer Bibliothek zur Verwendung beim Aufbau zusätzlicher Segmente speichern. </p> <p>Segmente können jetzt gestapelt werden. Wenn mehrere Segmente ausgewählt werden, wird im Vorschaubereich, im Anforderungs-Manager und im Popup mit den Anforderungsdetails eine durch Kommas getrennte Liste der Namen angezeigt (z. B. Segment1, Segment2). </p> <p>Weitere Informationen finden Sie im <a href="/help/components/segmentation/seg-home.md">Segmentierungsleitfaden</a>. </p> <p>Hinweis: Sie können in einem Data Warehouse-Bericht auf demselben Segment weder einen Segmentfilter noch eine Aufschlüsselung anwenden. Dies führt zu einem Fehler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Aufschlüsselung</span> </td> 
   <td colname="col2"> <p>Hier können Sie Daten mithilfe von Aufschlüsselungen kategorisieren. Segmente und Aufschlüsselungen unterscheiden sich insofern, als ein Segment Daten aus einem Datensatz filtert, während eine Aufschlüsselung Daten über alle für die Aufschlüsselung verfügbaren gültigen Werte unterteilt. </p> Sie können einen Bericht auch nach einem oder mehreren Segmenten aufschlüsseln. Sie können jedoch in einem Data Warehouse-Bericht auf demselben Segment weder einen Segmentfilter noch eine Aufschlüsselung anwenden. Dies führt zu einem Fehler. <p> Verwenden Sie z. B. Segmente zum Entfernen eines Geschlechts aus dem Datensatz und verwenden Sie eine Aufschlüsselung von Daten nach Geschlecht. </p> <p>Werden Data Warehouse-Anfragen mit mehreren Dimensionen und mehreren Werten (z. B. mehrere Mobilberichte) versendet, kann aus einem einzigen Treffer eine exponentielle Anzahl Zeilen generiert werden. Die Zeilenzahl, die aus einem einzigen Treffer generiert werden kann, wird auf 100 begrenzt (ehemals 1000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Metriken</span> </td> 
   <td colname="col2">Ermöglicht das Hinzufügen der Metriken, über die Sie einen Bericht erstellen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Sortieren von Metriken</span> </td> 
   <td colname="col2">Bietet nach Rang geordnet Detailberichte, die nach absteigendem Metrikwert sortiert sind und in etwa dem entsprechen, was in den Benutzeroberflächen von Reports &amp; Analytics, Data Workbench usw. angezeigt wird. <a href="/help/export/data-warehouse/sorting-by-metric.md"  > Mehr...</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Bereitstellung planen</span> </td> 
   <td colname="col2"> <p>Hier können Sie Anforderungen für eine automatische Bereitstellung in ausgewählten Intervallen oder als einmalige Berichtsanforderung planen. Wenn Sie das Standardformat verwenden, wird der Bericht als .csv-Datei per E-Mail gesendet. </p> <p>Soll auch der Datumsbereich angegeben werden, ergänzen Sie den Dateinamen durch <span class="filepath">%R</span>. Dieser Wert stellt die Datumswerte dar, die vom Bericht angefordert werden. Wenn Sie zum Beispiel Daten vom 1. Mai 2013 bis zum 7. Mai 2013 anfordern, zeigt <span class="filepath">%R</span> einen Dateinamen einschließlich des Datumsbereichs 20130501-20130507 an. </p> </td> 
  </tr> 
 </tbody> 
</table>
