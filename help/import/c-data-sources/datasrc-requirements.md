---
description: Informationen zu den Anforderungen an Ihre Report Suite vor der Nutzung von Data Sources.
seo-description: Informationen zu den Anforderungen an Ihre Report Suite vor der Nutzung von Data Sources.
seo-title: Anforderungen und Upload-Beschränkungen
solution: Analytics
subtopic: Datenquellen
title: Anforderungen und Upload-Beschränkungen
topic: Entwickler und Implementierung
uuid: d 79 fca 77-fa 0 e -4171-b 978-cdee 5 c 67 d 9 df
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Anforderungen und Upload-Beschränkungen

Informationen zu den Anforderungen an Ihre Report Suite vor der Nutzung von Data Sources.

In den folgenden Abschnitten werden Beschränkungen aufgeführt, die für Data Sources und für in Marketing Reports &amp; Analysen importierte Daten gelten.

* [Größenbeschränkungen](../../import/c-data-sources/datasrc-requirements.md#section_77B06D82CB374FFABD39F7D9A49D8E18)
* [Datum](../../import/c-data-sources/datasrc-requirements.md#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2)
* [Allgemein](../../import/c-data-sources/datasrc-requirements.md#section_1CD337F660484ABDB7D8CAE96FF46ACF)
* [Multibyte-Unterstützung](../../import/c-data-sources/datasrc-requirements.md#section_96C8D26B21184C3E839865DB6F23EA22)
* [Hochladen von Webprotokolldateien](../../import/c-data-sources/datasrc-requirements.md#section_DD736FC971FE45C89AB310BEDC1FE707)

## Größenbeschränkungen {#section_77B06D82CB374FFABD39F7D9A49D8E18}

* Jedes FTP-Konto kann maximal Daten in Höhe von 50 MB umfassen. Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt.

## Daten {#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2}

* Sie können an jedem Kalendertag Daten für 90 individuelle Daten hochladen. Wenn Sie diesen Grenzwert überschreiten, schlägt der Upload fehl und Sie erhalten eine Fehlermeldung, die darauf hinweist, dass Sie das Maximum für eindeutige Tage überschritten haben.
* Nur Daten aktuellen Datums oder vergangener Daten können importiert werden. Versuchen Sie nicht, zukünftige Daten in Ihren Data Sources-Daten zu verwenden.
* In allen Zeilen muss ein Datum angegeben sein, um die Diagrammfunktionen für Berichte zu aktivieren. Wenn eine Zeile kein Datum umfasst, generiert Data Sources einen Fehler und lehnt die Datei ab. Das Datum-/Zeit-Format variiert je nach Datenquellentyp:

   * **Volle Verarbeitung der Datenquellen**: Verwenden Sie das ISO 8601-Datumsformat ( `YYYY-MM-DDThh:mm:ss±UTC_offset` z `2013-09-01T12:00:00-07:00`. B.) oder das Unix Time Format (die Anzahl der seit dem 1. Januar 1970 verstrichenen Sekunden).

   * **Standard- und Integration-Datenquellen**: Verwenden Sie das folgende Datumsformat: `MM/DD/YYYY/HH/mm/SS` (zum Beispiel `01/01/2013/06/00/00`)

## Allgemein {#section_1CD337F660484ABDB7D8CAE96FF46ACF}

* Wenn Sie eine Data Sources-Datei hochladen, führt Data Sources eine grundlegende Datenvalidierung durch, um sicherzustellen, dass die Datei keine Formatierungsfehler enthält. Wenn in einer Datei ein Fehler erkannt wird, wird eine E-Mail-Benachrichtigung gesendet und die Verarbeitung wird gestoppt.
* Datenfelder dürfen keine Semikolons enthalten. Data Sources überspringt Datensätze, die ein Semikolon enthalten.
* Daten aus Webprotokollen, Traffic- und einige generische Data Sources-Gruppen stehen nicht in Data Warehouse oder Discover zur Verfügung. Weitere Informationen finden Sie unter [Datentypen und -kategorien](../../import/c-data-sources/c-datasrc-types/datasrc-categories.md#concept_42D1534F48324F20B4F9297FC4022105).
* Data Sources unterstützt keine serialisierten Ereignisse.

## Multibyte-Unterstützung {#section_96C8D26B21184C3E839865DB6F23EA22}

Data Sources unterstützt Multibyte-Codierung. Data Sources versucht, das Format der eingehenden Data Sources-Datei zu erkennen und ggf. in ein unterstütztes Format zu konvertieren. Die folgende Tabelle enthält gängige Zeichenformate und den jeweiligen Unterstützungsstatus.

<table id="table_F9E685D7EEAB49A9ABAD622AE630EC21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Zeichenformat </th> 
   <th colname="col2" class="entry"> Unterstützung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> UTF-8 </td> 
   <td colname="col2"> <p>Unterstützt. Für die mit Data Sources verwendete Report Suite muss die Unterstützung für Multibyte-Zeichen aktiviert werden. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=new_report_suite" format="https" scope="external">Neue Report Suite</a> in der Hilfe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-8 mit Byte Order Mark (EF BB BF) </td> 
   <td colname="col2"> <p>Unterstützt. Dieses Format ist nicht der Standard, auch wenn viele Windows-Anwendungen in diesem Format speichern. </p> <p>Zum Beispiel wird in WordPad unter diesem Format gespeichert, wenn Sie „UTF-8“ wählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ISO-8859-1 (auch bezeichnet als Latein-1 oder Windows-1252) </td> 
   <td colname="col2"> Unterstützt. Microsoft Excel speichert in diesem Format, wenn Sie einen tabulatorgetrennten Export wählen. Die Report Suite muss das Gebietsschema ISO-8859-1 verwenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 Little-Endian mit Byte Order Mark (FF FE) </td> 
   <td colname="col2"> Konvertiert in ISO-8859-1 oder UTF-8, je nach Bericht-Suite-Konfiguration. Microsoft Excel speichert in diesem Format, wenn Sie einen Unicode-Export wählen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 Big-Endian mit Byte Order Mark (EF FF) </td> 
   <td colname="col2"> Konvertiert in ISO-8859-1 oder UTF-8, je nach Bericht-Suite-Konfiguration. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 ohne Byte Order Mark </td> 
   <td colname="col2"> Nicht unterstützt. </td> 
  </tr> 
 </tbody> 
</table>

Wenn Sie eine UTF-8- oder ISO-8859-1-Datei einreichen und Ihre Bericht-Suite dies nicht unterstützt, tritt eine der folgenden Situationen ein:

* Wenn der Fehler während der Konversion erkannt wird, erhalten Sie eine Meldung wie die folgende: „Fehlerhaftes Zeichen in Datei an Position 18 beim Konvertieren von UTF-8 nach ISO-8859-1“.
* Die Datei wird ohne Fehler verarbeitet, aber es werden unleserliche Daten im Bericht ausgegeben.

## Hochladen von Webprotokolldateien {#section_DD736FC971FE45C89AB310BEDC1FE707}

* Die nützlichsten Berichte zum Anzeigen von Webprotokolldaten sind Traffic-Berichte wie Seitenansichten.
* Seitennamen werden als gesamte URL angezeigt, darunter auch die Abfragezeichenfolge.
* Jede Dateianforderung wird als eigenständige Seitenansicht angezeigt, darunter Style Sheets und Grafikdatein.
* Wenn Sie Informationen an die URL anhängen, können Dateien als eigenständige Seiten aufgezeichnet werden. Marketingberichte zeichnen beispielsweise die folgenden URLs als zwei eigenständige Seiten auf:

[!DNL /jokes/misc/snail_joke.html?userid=12345]

[!DNL /jokes/misc/snail_joke.html?userid=98765]
