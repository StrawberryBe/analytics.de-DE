---
description: Beim Einrichten eines Feeds wird anhand einiger Einstellungen bestimmt, wie oft Aufträge verarbeitet werden.
keywords: Datenfeed; job; settings; täglich; stündlich; Datenaufstockungen für stündliche Datenfeeds; Aufstockung
seo-description: Beim Einrichten eines Feeds wird anhand einiger Einstellungen bestimmt, wie oft Aufträge verarbeitet werden.
seo-title: Auftragseinstellungen
solution: Analytics
title: Auftragseinstellungen
uuid: e 124 b 4 f 1-0168-4 eaa -8657-19207 b 2 f 263 f
translation-type: tm+mt
source-git-commit: b6169d2febded32d772f82d5917b1132695ab442

---


# Auftragseinstellungen

Wenn Sie einen Feed einrichten, bestimmen einige Einstellungen, wie oft Aufträge verarbeitet werden.

Verwenden Sie zum Konfigurieren der Auftragsverarbeitungszeiten die folgenden Einstellungen. Diese Einstellungen werden nicht auf Auftrags-, sondern auf Feed-Ebene festgelegt.

<table id="table_2070F73212F245E98DADC6B5DFDB1C72"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Täglich </td> 
   <td colname="col2"> <p>Daten für einzelne Tage werden in einer einzelnen komprimierten Datei bereitgestellt. Die Größe dieser Datei ist auf 2 GB beschränkt. Wenn die Datei mehr als 2 GB unkomprimierte Daten enthält, werden zusätzliche Dateien erstellt. Sie erhalten für jeden Tag eine einzelne Lieferung aller Dateien. </p> <p>Jede Datei wird im folgenden Format benannt: </p> <p> <span class="filepath"><span class="varname"> reportsuite</span>-<span class="varname"> date</span>.tar</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stündlich (Standardeinstellung) </td> 
   <td colname="col2"> <p>Daten für einzelne Stunden werden in einer einzelnen komprimierten Datei bereitgestellt, die alle Daten umfasst, die innerhalb dieser Stunde empfangen wurden. Sie erhalten pro Tag 24 separate Dateibereitstellungen. Jede Datei wird dabei bereitgestellt, nachdem die Daten für diese Stunde verarbeitet wurden. </p> <p>Der Begriff „Stündlich“ beschreibt den Zeitrahmen der Daten, die in den einzelnen Datenexporten gesendet werden, und nicht den Zeitrahmen, in dem die Bereitstellung erfolgt. Stündliche Datenfeeds werden nach besten Möglichkeiten verarbeitet und bereitgestellt. </p> <p>Bei stündlichen Datenfeeds wird erwartet, dass der Datenfeed innerhalb von 12 Stunden zu 95 % der Zeit die Daten liefert, die dem Abschluss dieser Stunde entsprechen. Die Verarbeitung und Bereitstellung von Datenfeeds für Report Suites mit hohem Datenverkehrsvolumen kann mehr Zeit in Anspruch nehmen. </p> <p>Der Empfang stündlicher Datenfeeds unterscheidet sich vom Empfang täglicher Feeds mit mehreren Dateibereitstellungen. Beim Empfang stündlicher Datenfeeds werden die Daten für einen einzelnen Tag auf 24 Dateien aufgeteilt, basierend auf den Daten, die innerhalb dieser Stunde erfasst werden, und jede Datei wird bereitgestellt, sobald sie verfügbar ist. Ein täglicher Feed, der mehrere Dateien umfasst, wird einmalig pro Tag geliefert, nachdem die Daten des vorherigen Tages verarbeitet sind. Diese Daten werden dabei in Einzeldateien zu jeweils 2 GB an erfassten Daten aufgeteilt. </p> <p>Jede Datei wird im folgenden Format benannt: </p> <p> <span class="filepath"><span class="varname"> reportsuite</span>-<span class="varname"> date</span>-<span class="varname"> hour</span>.tar</span> </p> <p>Weitere Informationen zu den Faktoren, die stündliche Feeds beeinflussen können, finden Sie unter <a href="../../../export/analytics-data-feed/c-df-contents/jobs-faq.md#concept_7C67A012CCF64B0C8DA33E5A6CF7FD9E" format="dita" scope="local">Häufig gestellte Fragen zu Aufträgen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Datenaufstockungen für stündliche Datenfeeds </td> 
   <td colname="col2"> <p>Wenn Sie bei der Einrichtung eines neuen Datenfeeds Daten für frühere Zeitpunkte anfordern, werden Daten für Zeitpunkte, die über 60 Tage zurückliegen, möglicherweise im täglichen und nicht im stündlichen Format ausgeliefert. </p> <p>In diesem Fall erhalten Sie für diese Tage nicht 24 separate Auslieferungen, sondern nur eine Auslieferung mit einem auf Mitternacht gesetzten Zeitstempel, die alle Daten für den jeweiligen Tag enthält. Wenn Sie diese Art Aufstockung anfordern, sollten Sie sicherstellen, dass Ihr ETL für die Verarbeitung von täglichen Auslieferungen konfiguriert ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

