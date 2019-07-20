---
description: In diesem Abschnitt werden die Dateien beschrieben, die in einer Datenfeed-Auslieferung enthalten sind.
keywords: Datenfeed; job; Inhalt; manifest; Datei; Suche; Trefferdaten; Bereitstellungsinhalte
seo-description: In diesem Abschnitt werden die Dateien beschrieben, die in einer Datenfeed-Auslieferung enthalten sind.
seo-title: Datenfeed-Inhalt - Übersicht
solution: Analytics
subtopic: Datenfeeds
title: Datenfeed-Inhalt - Übersicht
topic: Reports and Analytics
uuid: 82 a 86314-4841-4133-a 0 dc -4 e 7 c 6 cd 14 fc 1
translation-type: tm+mt
source-git-commit: 7fe23291d8ee9675181065025692108aee3ea9a5

---


# Datenfeed-Inhalt - Übersicht

In diesem Abschnitt werden die Dateien beschrieben, die in einer Datenfeed-Auslieferung enthalten sind.

## Manifestdatei {#section_044BBDE2906D49518F8264CD4832D429}

Die Manifestdatei enthält folgende Details zu den einzelnen Dateien, die Bestandteil des hochgeladenen Datensatzes sind:

* Dateiname
* Dateigröße
* MD5-Hash
* Anzahl der in der Datei enthaltenen Datensätze

Die Manifestdatei folgt demselben Format wie eine Java-JAR-Manifestdatei.

The manifest file is always delivered last as a separate `.txt` file, so that its existence indicates that the complete data set for that request period has already been delivered. Manifestdateien werden nach folgendem Muster benannt:

```
<report_suite_id>_YYYY_MM_DD.txt
```

Eine typische Manifestdatei enthält Daten, die folgendem Schema entsprechen:

```
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: bugzilla_2012-09-09-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-bugzilla_2012-09-09.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

Jede Manifestdatei enthält eine Kopfzeile, in der die Gesamtanzahl der Lookup-Dateien, Datendateien sowie die Gesamtanzahl der Datensätze in allen Datendateien angegeben sind. Nach dieser Kopfzeile folgen verschiedene Abschnitte mit Informationen zu den einzelnen Dateien, die in der Datenfeedauslieferung enthalten sind.

Some feeds are configured to receive a `rsid_YYYY-MM-DD.fin` file instead of a `.txt` manifest. The `.fin` indicates that the upload is complete, but it contains no metadata about the upload.

## Lookup-Dateien {#section_B5863537A48D47D78D0F7274838923C1}

Lookup-Dateien enthalten keine Trefferdaten. Es handelt sich vielmehr um ergänzende Dateien, die die Spaltenkopfzeilen für die Trefferdaten bereitstellen, und die Lookup-Dateien übersetzen die im Datenfeed ermittelten IDs in tatsächliche Werte. Beispiel: Der Wert „497“ in der Browserspalte gibt an, dass der Treffer aus „Microsoft Internet Explorer 8“ stammt.

Note that the `column_headers.tsv` and `event_list.tsv` are specific to the data feed and report suite. Andere Dateien, z. B. `browser.tsv`, sind hingegen generisch.

Lookup-Dateien werden in einer komprimierten ZIP-Datei bereitgestellt, die nach folgendem Muster benannt ist:

```
<report_suite_id>_<YYYY-mm-dd>-<HHMMSS>-lookup_data.<compression_suffix>
```

* [!DNL column_headers.tsv] (angepasst für diesen Datenfeed)
* [!DNL browser.tsv]
* [!DNL browser_type.tsv]
* [!DNL color_depth.tsv]
* [!DNL connection_type.tsv]
* [!DNL country.tsv]
* [!DNL javascript_version.tsv]
* [!DNL languages.tsv]
* [!DNL operating_systems.tsv]
* [!DNL plugins.tsv]
* [!DNL resolution.tsv]
* [!DNL referrer_type.tsv]
* [!DNL search_engines.tsv]
* [!DNL event_lookup.tsv] (angepasst für diesen Datenfeed)

## Trefferdatendateien {#section_B0745236104E41F2BA625D24AB442636}

Hit data is provided in a [!DNL hit_data.tsv] file. Die Menge an Daten in dieser Datei richtet sich nach dem Auslieferungsformat (stündlich oder täglich sowie danach, ob die Auslieferung in einer oder in mehreren Dateien erfolgt). Diese Datei enthält nur die Trefferdaten. Die Spaltenkopfzeilen werden separat mit den Lookup-Dateien geliefert. Jede Zeile in dieser Datei entspricht einem einzelnen Server-Aufruf.

## Auslieferungsinhalte {#section_994B43D1E71A4EFDB2E4183C0929A397}

>[!NOTE]
>
>Die Dateien werden mit ISO -8859-1 kodiert.

Die tatsächlich von Adobe bereitgestellten Dateien variieren je nach Art des konfigurierten Datenfeeds. Finden Sie anhand der folgenden Tabelle die Konfiguration, die zu Ihrem Datenfeed passt sowie eine Beschreibung zu den bereitgestellten Dateien.

Die Uhrzeit im Dateinamen (HHMMSS) gibt jeweils den Beginn des Datumsbereichs für die Daten in der Datei an, unabhängig davon, wann die Datei erzeugt oder hochgeladen wurde.

<table id="table_DBF34F39D29D4DA2B2689029CDA24B92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Auslieferungsformat </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Täglich; einzelne Datei </td> 
   <td colname="col2"> <p>Nachdem die Daten für einen Tag erfasst wurden, erhalten Sie eine Auslieferung, die Folgendes enthält: </p> 
    <ul id="ul_D630D73D0DBA440FA704CF31856243C7"> 
     <li id="li_717873DBBF264422A39217E1A8829742">eine einzelne komprimierte Datendatei </li> 
     <li id="li_9F75D42FD56E4CC89C4683D32E59337B">Eine Manifestdatei </li> 
    </ul> <p>Die Datendatei wird mit dem folgenden Namen bereitgestellt: </p> 
    <code>&lt; report_ suite &gt;_ &lt; JJJJ-mm-tt &gt;.&lt;compression_suffix&gt;
    </code> <p> Das <code>&lt;compression_suffix&gt;</code> ist entweder <code>tar.gz</code> oder <code>zip</code>. </p> <p>Wenn Sie diese Datei extrahieren, enthält sie eine einzelne Datei <span class="filepath">hit_data.tsv</span> mit allen Daten für diesen Tag sowie die komprimierten Lookup-Dateien, die zuvor beschrieben wurden. </p> <p>Die Größe der Trefferdatei kann in Abhängigkeit von der Anzahl der aktiv genutzten Variablen und dem Traffic in der Report Suite stark variieren. Eine Datenzeile ist durchschnittlich 500 B (komprimiert) oder 2 KB (unkomprimiert) groß. Dieser Wert multipliziert mit der Anzahl der Server-Aufrufe gibt einen ungefähren Schätzwert zur Größe einer Datenfeeddatei an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Täglich; mehrere Dateien </td> 
   <td colname="col2"> <p>Nachdem die Daten für einen Tag erfasst wurden, erhalten Sie eine Auslieferung, die Folgendes enthält: </p> 
    <ul id="ul_4B873D3F6F18467890C36AE8E86F49DA"> 
     <li id="li_227315384B954A5784FA370D9B30E2AF">Eine oder mehrere komprimierte Datendateien, die in Segmente von etwa 2 GB aufgeteilt sind </li> 
     <li id="li_4169D889CEA3446CB5FAA08FD60AA0D0">Eine Manifestdatei </li> 
    </ul> <p>Jede Datendatei wird mit dem folgenden Namen bereitgestellt: </p> 
    <code>&lt; index &gt;-&lt; report_ suite &gt;_ &lt; YYYY-mm-dd &gt;.&lt;compression_suffix&gt;
    </code> <p> Dabei ist <code>&lt;index&gt;</code> ein inkrementierter Dateiindex von <i>1</i> bis <i>n</i>, bei insgesamt <i>n</i> Dateien, und das <code>&lt;compression_suffix&gt;</code> lautet <code>tar.gz</code> oder <code>zip</code>. </p> <p>Wenn Sie diese Datei extrahieren, enthält jede Datendatei eine einzelne Datei <span class="filepath">hit_data.tsv</span> mit ca. 2 GB nicht komprimierten Daten sowie die komprimierten Lookup-Dateien, die zuvor beschrieben wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stündlich; einzelne Datei </td> 
   <td colname="col2"> <p>Nachdem die Daten für eine Stunde erfasst wurden, erhalten Sie eine Auslieferung, die Folgendes enthält: </p> 
    <ul id="ul_29B06981A4F74D2AA1171D733C5FB1F4"> 
     <li id="li_072BBC4BA9B84C61B4E8EFA35F54707B">Eine einzelne Datendatei </li> 
     <li id="li_E2D05E9DAE814309B6BC91798BB29FBB">Eine Manifestdatei </li> 
    </ul> <p>Die Datendatei wird mit dem folgenden Namen bereitgestellt: </p> 
    <code>&lt; report_ suite &gt;_ &lt; JHMMSS &gt; &lt; HHMMSS &gt;.&lt;compression_suffix&gt;
    </code> <p> Das <code>&lt;compression_suffix&gt;</code> ist entweder <code>tar.gz</code> oder <code>zip</code>. </p> <p>Wenn Sie diese Datei extrahieren, enthält sie eine einzelne Datei <span class="filepath">hit_data.tsv</span> mit allen Daten für diese Stunde. Die zuvor beschriebenen Lookup-Dateien werden nur für die Daten der ersten Stunde des jeweiligen Tages bereitgestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stündlich; mehrere Dateien </td> 
   <td colname="col2"> <p>Nachdem die Daten für eine Stunde erfasst wurden, erhalten Sie eine Auslieferung, die Folgendes enthält: </p> 
    <ul id="ul_A739BA12B66547A28BA45E0B9B747B16"> 
     <li id="li_C0DF059D1E6843C8A38E24CA1B59D99C">Eine oder mehrere komprimierte Datendateien, die in Segmente von etwa 2 GB aufgeteilt sind </li> 
     <li id="li_604266DA9B8A4000905C44C95DA65D14">Eine Manifestdatei </li> 
    </ul> <p>Jede Datendatei wird mit dem folgenden Namen bereitgestellt: </p> 
    <code>&lt; index &gt;-&lt; report_ suite &gt;_ &lt; JJJJ-mm-tt &gt;-&lt; HHMMSS &gt;. tsv.&lt;compression_suffix&gt;
    </code> <p>Dabei ist <code>&lt;index&gt;</code> ein inkrementierter Dateiindex von <i>1</i> bis <i>n</i>, bei insgesamt <i>n</i> Dateien, und das <code>&lt;compression_suffix&gt;</code> lautet entweder <code>gz</code> oder <code>zip</code>. </p> <p>Wenn Sie diese Datei extrahieren, enthält jede Datendatei eine einzelne Datei <span class="filepath">hit_data.tsv</span> mit ca. 2 GB nicht komprimierten Daten. Die zuvor beschriebenen Lookup-Dateien werden nur für die Daten der ersten Stunde des jeweiligen Tages bereitgestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

