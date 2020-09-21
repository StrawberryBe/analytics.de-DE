---
description: Mit Verarbeitungsregeln können Sie Änderungen an den Daten auf der Grundlage definierter Bedingungen vornehmen. Wenn Attribute oder Werte definierten Bedingungen entsprechen, können Werte festgelegt und gelöscht sowie Ereignisse festgelegt werden.
subtopic: Processing rules
title: Funktionsweise von Verarbeitungsregeln
topic: Admin tools
uuid: 19c31f94-c8d8-47b1-97fa-29ed98c94e87
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '690'
ht-degree: 100%

---


# Funktionsweise von Verarbeitungsregeln

Mit Verarbeitungsregeln können Sie Änderungen an den Daten auf der Grundlage definierter Bedingungen vornehmen. Wenn Attribute oder Werte definierten Bedingungen entsprechen, können Werte festgelegt und gelöscht sowie Ereignisse festgelegt werden.

Verarbeitungsregeln werden auf Daten während der Erfassung angewandt, und Regeln werden auf alle Daten angewandt, die über die AppMeasurement-Bibliotheken und durch die Dateneinfüge-API eingehen. Außerdem gelten die Verarbeitungsregeln für vollständige Data Sources und Protokolldatenquellen. Diese Quellen enthalten Daten, die für einen  *`hit`* oder für eine Aktion, die ein Benutzer ausführt, stehen. Für andere Datenquellen gelten die Verarbeitungsregeln nicht.

## Wichtige Konzepte {#section_EB138775E7C64C74B0D1D3213F7A823C}

In der folgenden Tabelle sind zentrale und grundlegende Konzepte für die Verwendung von Verarbeitungsregeln aufgeführt:

<table id="table_287C606AE26E47AA8F737411990ACEB2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Konzept </p> </th> 
   <th colname="col2" class="entry"> <p>Details </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Regeln gelten für eine einzelne Report Suite. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md"> Kopieren von Verarbeitungsregeln in eine andere Report Suite </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitungsregeln werden in der aufgeführten Reihenfolge angewendet. </p> </td> 
   <td colname="col2"> <p>Wenn sich durch eine Aktion ein Wert ändert, wird dieser Wert bei späteren Bedingungen verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitungsregeln werden sofort nach ihrer Speicherung auf die Report Suite angewendet. </p> </td> 
   <td colname="col2"> <p>Änderungen der Verarbeitungsregeln sollten in Ihrer Report Suite wenige Minuten nach dem Speichern sichtbar werden. Beim Test von Verarbeitungsregeln empfehlen wird die Konfiguration von  <a href="/help/admin/admin/realtime/t-realtime-admin.md"> Echtzeitberichten</a> in Ihrer Test-Report Suite, so dass Sie die Ergebnisse der Verarbeitungsregel schnell sehen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitungsregeln sind die einzige Möglichkeit für den Zugriff auf Kontextdatenvariablen. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md"> Eine Kontextdatenvariable in eine eVar kopieren </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitungsregeln werden vor VISTA-Regeln und Marketingkanalregeln angewendet. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md"> Verarbeitungsreihenfolge </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Treffer können nicht ausgeschlossen werden. </p> </td> 
   <td colname="col2"> <p>Zum Ausschließen von Treffern müssen Sie VISTA-Regeln festlegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Die Produktzeichenfolge, der Referrer und der Benutzeragent können nicht geändert werden. </p> </td> 
   <td colname="col2"> <p>Der Referrer und der Benutzeragent sind schreibgeschützt. Die Produktzeichenfolge ist nicht verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Die Attribute und Classifications von mobilen Geräten sind nicht verfügbar. </p> </td> 
   <td colname="col2"> <p>Die Suche nach mobilen Geräten findet vor der Ausführung der Verarbeitungsregeln statt, aber in den Verarbeitungsregeln sind keine Attribute verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn Sie mit JavaScript AppMeasurement H.25.2 oder früher arbeiten, können die Abfragezeichenfolgenparameter nur bis zu den ersten 255 Zeichen der URL gelesen werden. JavaScript AppMeasurement H.25.3 (oder höher) liefert den Verarbeitungsregeln die vollständige URL sowie alle Abfragezeichenfolgenparameter. </p> </td> 
   <td colname="col2"> <p>Aktualisieren Sie auf Version H.25.3 oder höher, oder lesen Sie die Abfragezeichenfolgenparameter aus langen URLs clientseitig ein, und speichern Sie die Werte in Kontextdatenvariablen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Für die Nutzung in Verarbeitungsregeln müssen die Werte für die Abfragezeichenfolge in Unicode oder UTF-8 kodiert sein. </p> </td> 
   <td colname="col2"> <p>Hiervon sind unter Umständen Multibyte-Zeichen betroffen, die per Abfragezeichenfolge übertragen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Es gilt für alle Report Suites eine Grenze von 150 Regeln mit 30 Bedingungen. </p> </td> 
   <td colname="col2"> <p>Die Verarbeitungsregelgrenzen gelten pro Report Suite, nicht pro Unternehmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitungsregeln müssen so eingerichtet sein, dass Kontextdatenvariablen vor dem Versenden von Daten abgerufen werden. </p> </td> 
   <td colname="col2"> <p>Verarbeitungsregeln werden angewandt, während Server-Aufrufe versendet werden. In Kontextdatenvariablen gespeicherte Werte werden verworfen, wenn sie nicht mithilfe von Verarbeitungsregeln kopiert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bei Wertvergleichen in der Benutzeroberfläche wird zwischen Groß- und Kleinschreibung unterschieden. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md"> Bereinigen von Werten in einem Bericht</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Der Name der Kontextdatenvariablen darf nur alphanumerische Zeichen, Unterstriche und Punkte enthalten. Alle anderen Zeichen werden entfernt. </p> </td> 
   <td colname="col2"> <p>Beispiel: Die Kontextdatenvariable <code> login_page-home</code> wird automatisch in <code> login_pagehome</code> geändert. Alle an die <code> login_page-home</code>-Variable gesendeten Daten werden unter <code> login_pagehome</code> zugeordnet. </p> <p>Kontextdatenvariablen mit ungültigen Zeichen im Namen können nicht in die Verarbeitungsregel-Oberfläche aufgenommen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Das Caret (^) ist ein im Verarbeitungsregelsystem verwendetes Sonderzeichen. </p> </td> 
   <td colname="col2"> <p>Um nach einem einzelnen Caret-Zeichen zu suchen, geben Sie zwei Caret-Zeichen (^^) ein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Bedingungen für Verarbeitungsregeln  {#section_387390EEE9BA4DA98698522A84326DB4}

Mit Bedingungen werden Seitenvariablen darauf überprüft, ob ein Wert vorhanden ist oder übereinstimmt. Sie können mehrere Bedingungen hinzufügen, und es kann festgelegt werden, ob sämtliche Bedingungen erfüllt werden müssen.

Sie können eine Regel ohne Bedingungen erstellen, wenn bestimmte Aktionen immer ausgeführt werden sollen.

Variablen werden nicht automatisch auf bestimmte Werte überprüft, bevor Aktionen durchgeführt werden. So enthält „Prop1“ einen beliebigen Wert, und „eVar1“ ist leer. Wenn Sie festlegen, dass „Prop1“ den Wert von „eVar1“ annimmt, sind beide Werte leer. Wenn dies verhindert werden soll, müssen Sie mit einer Bedingung testen, ob ein Wert vorhanden ist.

## Aktionen für Verarbeitungsregeln  {#section_E2285C9D008442C7BF136E52A9A4CC06}

Mit Aktionen werden Seitenvariablen festgelegt oder gelöscht und Ereignisse ausgelöst. Mit Aktionen können auch Werte für eine Berichtanzeige miteinander verkettet werden.

So können Sie beispielsweise durch Verkettung zweier Variablen `category:product` anzeigen.
