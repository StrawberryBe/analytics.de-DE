---
description: Data Warehouse bezieht sich auf die Kopie der Analytics-Daten für Datenspeicherung- und benutzerspezifische Berichte, die Sie durch Filtern der Daten ausführen können. Sie können Berichte anfordern, um erweiterte Datenbeziehungen aus Rohdaten auf Basis Ihrer individuellen Fragen anzuzeigen. Data Warehouse-Berichte werden per E-Mail oder FTP gesendet und können bis zu 72 Stunden Verarbeitungszeit in Anspruch nehmen. Die Verarbeitungszeit hängt von der Komplexität der Abfrage und der Menge der angeforderten Daten ab.
title: Data Warehouse-Übersicht
topic: Data warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Data Warehouse-Übersicht

Data Warehouse bezieht sich auf die Kopie der Analytics-Daten für Datenspeicherung- und benutzerspezifische Berichte, die Sie durch Filtern der Daten ausführen können. Sie können Berichte anfordern, um erweiterte Datenbeziehungen aus Rohdaten auf Basis Ihrer individuellen Fragen anzuzeigen. Data Warehouse-Berichte werden per E-Mail oder FTP gesendet und können bis zu 72 Stunden Verarbeitungszeit in Anspruch nehmen. Die Verarbeitungszeit hängt von der Komplexität der Abfrage und der Menge der angeforderten Daten ab.

Adobe aktiviert Data Warehouse nur für Benutzer auf Administratorebene und nur für bestimmte Report Suites. (Sie kann für globale und untergeordnete Report Suites, jedoch nicht für Datenaggregations-Report Suites aktiviert werden.) Der Administrator kann eine Gruppe erstellen, die Zugriff auf Data Warehouse hat, und anschließend Benutzer, die sich nicht auf Administratorebene befinden, dieser Gruppe zuweisen.

Data Warehouse komprimiert automatisch alle Dateien, die größer als 1 MB sind. Die maximale Größe des E-Mail-Anhangs beträgt 10 MB.

Data Warehouse kann eine unbegrenzte Anzahl von Zeilen in einer einzigen Anforderung für einzelne terminierte und heruntergeladene Berichte verarbeiten.

>[!NOTE] Data Warehouse gibt in Berichten den ersten aufgefundenen Wert innerhalb des Berichtszeitraums aus.

>[!IMPORTANT]
>
>Bei der Segmentierung nach klassifizierten Werten behandeln Analysis Workspace und Data Warehouse „nicht spezifizierte“ Werte unterschiedlich. „Nicht spezifiziert“ in Workspace bezieht sich auf Werte, die nicht klassifiziert sind, während „nicht spezifiziert“ in Data Warehouse auf Werte verweist, die Sie als „nicht spezifiziert“ klassifiziert haben.

## Data Warehouse-Anforderungen – Beschreibungen {#section_F21C78ED36884C389C852E876AF5CDE8}

In dieser Tabelle werden die Felder und Optionen auf der [!UICONTROL Data Warehouse Request] Registerkarte beschrieben.

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
    </ul> <p>Data Warehouse Berichte für Virtual Report Suites unterstützt die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Verfügbare Segmente</span> </td> 
   <td colname="col2"> <p>Ermöglicht die Auswahl des Teils der Besucher-Population, den Sie untersuchen und komplexe Segmente generieren möchten. Sie können vorkonfigurierte Segmente laden, neue Segmente erstellen und Segmentkomponenten in einer Bibliothek speichern, um sie beim Erstellen zusätzlicher Segmente zu verwenden. </p> <p>Sie können Segmente jetzt stapeln. Wenn Sie mehrere Vorschauen auswählen, wird im Bereich "", im Anforderungs-Manager und im Popup "Anforderungsdetails"eine kommagetrennte Liste von Namen angezeigt (z. B. Segment1, Segment2). </p> <p>Weitere Informationen finden Sie im <a href="/help/components/c-segmentation/seg-home.md">Segmentierungsleitfaden</a>. </p> <p>Hinweis: Sie können in einem Data Warehouse-Bericht auf demselben Segment weder einen Segmentfilter noch eine Aufschlüsselung anwenden. Dies führt zu einem Fehler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Aufschlüsselung</span> </td> 
   <td colname="col2"> <p>Ermöglicht die Kategorisierung von Daten mithilfe von Aufschlüsselungen. Segmente und Aufschlüsselungen unterscheiden sich dadurch, dass ein Segment Daten aus einem Datensatz Filter, während eine Aufschlüsselung Daten über alle für die Aufschlüsselung gültigen Werte verteilt. </p> Sie können einen Bericht auch nach einem oder mehreren Segmenten unterteilen. Sie können jedoch nicht sowohl einen Segmentfilter als auch eine Aufschlüsselung für dasselbe Segment in denselben Data Warehouse-Bericht aufnehmen. Dies führt zu einem Fehler. <p> Verwenden Sie zum Beispiel Segmente, um ein Geschlecht aus dem Datensatz zu entfernen, und verwenden Sie eine Aufschlüsselung, um die Daten nach Geschlecht getrennt anzuzeigen. </p> <p>Wenn eine Data Warehouse-Anforderung mit mehreren Dimensionen mit mehreren Werten gesendet wird (z. B. mehrere Mobilberichte), kann aus einem einzelnen Treffer eine exponentielle Anzahl Zeilen generiert werden. Die Anzahl der Zeilen, die von einem einzelnen Treffer ausgegeben werden können, wird auf 100 begrenzt (zuvor 1.000). </p> </td> 
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
   <td colname="col2"> <p>Ermöglicht die Planung von Anforderungen für automatische Versand in bestimmten Zeitabständen oder als einmalige Berichte. Wenn Sie das Standardformat verwenden, wird der Bericht als .csv-Datei per E-Mail gesendet. </p> <p>Soll auch der Datumsbereich angegeben werden, ergänzen Sie den Dateinamen durch <span class="filepath">%R</span>. Dieser Wert stellt die Datumswerte dar, die vom Bericht angefordert werden. Wenn Sie zum Beispiel Daten vom 1. Mai 2013 bis zum 7. Mai 2013 anfordern, zeigt <span class="filepath">%R</span> einen Dateinamen einschließlich des Datumsbereichs 20130501-20130507 an. </p> </td> 
  </tr> 
 </tbody> 
</table>

