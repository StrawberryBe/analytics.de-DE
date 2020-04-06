---
description: Mit dem Importer können Sie Classification-Daten in großen Mengen in Analytics Berichte in einer Datei hochladen. Für den Import ist ein bestimmtes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden können.
subtopic: Classifications
title: Klassifizierungsdatendateien
topic: Admin tools
uuid: f27bb812-56e0-472a-9993-d869f0fea700
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Klassifizierungsdatendateien

Mit dem Importer können Sie Classification-Daten in großen Mengen in Analytics Berichte in einer Datei hochladen. Für den Import ist ein bestimmtes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden können.

Um Ihnen bei der Erstellung gültiger Datendateien zu helfen, können Sie eine Vorlagendatei herunterladen, die eine Dateistruktur bietet, in die Sie die Klassifizierungsdaten einfügen können. Weitere Informationen finden Sie unter [Klassifizierungsvorlage herunterladen](/help/components/c-classifications2/c-classifications-importer/c-download-saint-data.md).

Weitere Informationen zu Zeichenbeschränkungen in Klassifizierungen finden Sie unter [Allgemeine Dateistruktur](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md).

Unter [„Numerisch 2“-Klassifizierungen](/help/components/c-classifications2/c-numeric-2/c-numeric-2-classifications.md) finden Sie Informationen zum Hochladen von Daten mithilfe von „Numerisch 2“-Klassifizierungen.

## Allgemeine Dateistruktur

Die folgende Abbildung zeigt eine Beispieldatendatei:

![](assets/completed-saint-file.png)

Eine Datendatei muss den folgenden Strukturregeln entsprechen:

* Classifications können nicht den Wert 0 (Null) haben.
* Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.
* Hochgeladene Dateien sollten UTF-8 ohne BOM-Zeichenkodierung verwenden.
* Sonderzeichen wie Tabulatoren, Zeilenumbrüche und Anführungszeichen können in eine Zelle eingebettet werden, wenn das v2.1-Dateiformat angegeben und die Zelle ordnungsgemäß  [maskiert wurde](/help/components/c-classifications2/c-classifications-importer/t-classifications-escape-data.md). Zu den Sonderzeichen gehören:

   ```
   \t     tab character 
   \r     form feed character 
   \n    newline character 
   "       double quote
   ```

   Das Komma ist kein Sonderzeichen.

* Klassifizierungen dürfen kein Caret (^) enthalten, da dieses Zeichen zur Bezeichnung einer Unterklassifizierung verwendet wird.
* Seien Sie vorsichtig, wenn Sie einen Bindestrich verwenden. Wenn Sie beispielsweise einen Bindestrich (-) in einem sozialem Begriff verwenden, erkennt Social ihn als [!DNL Not]-Operator (Minuszeichen). Wenn Sie beispielsweise mit dem Import *`fragrance-free`* als Begriff angeben, interpretiert Social den Begriff folgendermaßen: Parfüm *`minus`* frei. Dadurch werden Wortlaute mit den Begriffen *`fragrance`*, jedoch nicht *`free`* erfasst.
* Zeichenbeschränkungen werden erzwungen, um Berichtdaten zu klassifizieren. Wenn Sie beispielsweise eine Klassifizierungstextdatei für Produkte (*`s.products`*) mit Produktnamen mit mehr als 100 Zeichen (Byte) hochladen, werden die Produkte nicht in den Berichten angezeigt. Für Trackingcodes und für alle benutzerdefinierten Konversionsvariablen (eVars) sind jeweils 255 Byte zulässig.
* Tabulatorgetrennte Datendatei (Sie können die Vorlagendatei mit jeder Tabellenkalkulationsanwendung oder einem Texteditor erstellen).
* Die Dateierweiterung muss entweder [!DNL .tab] oder [!DNL .txt] lauten.
* Ein Rautenzeichen (#) kennzeichnet die Zeile als Benutzerkommentar. Adobe ignoriert alle Zeilen, die mit # beginnen.
* Ein Dublette-Pfund-Zeichen gefolgt von SC (## SC) kennzeichnet die Zeile als Kopfzeilenkommentar vor der Verarbeitung, der von Berichte verwendet wird. Löschen Sie diese Zeilen nicht.
* Classification-Exporte können aufgrund von Zeilenumbruchzeichen im Schlüssel über Duplikat-Schlüssel verfügen. In einem FTP- oder Browser-Export kann dies durch Aktivieren der Anführungszeichen für das FTP-Konto behoben werden. Dadurch werden die einzelnen Schlüssel mit Zeilenumbruchzeichen in Anführungszeichen gesetzt.
* Die Zelle C1 in der ersten Zeile der Importdatei enthält eine Versionskennung, die bestimmt, wie Classifications die Verwendung von Anführungszeichen im Rest der Datei handhaben.

   * v2.0 ignoriert Anführungszeichen und geht davon aus, dass sie alle Teil der angegebenen Schlüssel und Werte sind. Betrachten Sie zum Beispiel den folgenden Wert: &quot;Dies ist ein &quot;beliebiger Wert&quot;&quot;. v2.0 würde dies wörtlich wie folgt interpretieren: &quot;Dies ist ein &quot;beliebiger Wert&quot;&quot;.
   * v2.1 weist Classifications an, davon auszugehen, dass Anführungszeichen Teil der in Excel-Dateien verwendeten Dateiformatierung sind. Daher würde v2.1 das obige Beispiel wie folgt formatieren: Dies ist &quot;irgendein Wert&quot;.
   * Probleme können auftreten, wenn v2.1 in der Datei angegeben ist, aber tatsächlich v2.0 gewünscht wird, d. h. wenn Anführungszeichen auf eine Weise verwendet werden, die unter Excel-Formatierung unzulässig ist. Wenn Sie beispielsweise einen Wert haben: &quot;VP NO REPS&quot; S/l Kleid mit Überlagerung. Bei Version 2.1 ist dies eine falsche Formatierung (der Wert sollte von öffnenden und schließenden Anführungszeichen umgeben sein, und Anführungszeichen, die Teil des tatsächlichen Werts sind, sollten mit Anführungszeichen versehen werden), und Klassifizierungen funktionieren über diesen Punkt hinaus nicht.
   * Führen Sie einen der folgenden Schritte aus: Ändern Sie das Dateiformat in v2.0, indem Sie die Kopfzeile (Zelle C1) der hochgeladenen Dateien ändern ODER Excel-Anführungszeichen ordnungsgemäß in alle Dateien implementieren.

* Die erste (Nicht-Kommentar)-Zeile der Datendatei enthält die Spaltenüberschriften, die die Classification-Daten in der Spalte bezeichnen. Der Importeur benötigt ein bestimmtes Format für Spaltenüberschriften. Weitere Informationen finden Sie unter [Format der Spaltenüberschrift](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md).
* Direkt nach der Kopfzeile in einer Datendatei sind die Datenzeilen. Jede Datenzeile sollte ein Datenfeld für jede Spaltenüberschrift enthalten.
* Die Datendatei unterstützt die folgenden Steuercodes, mit denen Adobe die Datei strukturiert und Klassifizierungsdaten korrekt importiert:

<table id="table_0548F2E58B6644208147434EB9B3C21B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> STEUERCODE </th> 
   <th colname="col2" class="entry"> BESCHREIBUNG </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>&lt;Neue Zeile&gt; </p> </td> 
   <td colname="col2"> <p>Ein neues Zeilenzeichen ist das einzige unterstützte Trennzeichen zwischen Datenzeilen/Datensätzen in der Datendatei. Normalerweise müssen Sie diese Zeichen nur spezifisch einfügen, wenn Sie ein Programm schreiben, um automatisch Datendateien zu generieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~autogen~ </p> </td> 
   <td colname="col2"> <p>Fordert an, dass Adobe automatisch eine eindeutige ID für dieses Element generiert. </p> <p>Im Kontext der Kampagne weist dieser Steuerelementwert Adobe an, jedem kreativen Element eine Kennung zuzuweisen. Weitere Informationen finden Sie unter <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  >Schlüssel</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~period~ </p> </td> 
   <td colname="col2"> <p>Gibt an, dass die Datenspalte den mit dem Element verbundenen Datumsbereich darstellt. Weitere Informationen finden Sie unter <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  >Datum</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeres Feld </p> </td> 
   <td colname="col2"> <p>Stellt einen NULL-Wert für das aktuelle Feld dar. Verwenden Sie dies, wenn eine bestimmte Datenspalte nicht auf den aktuellen Datensatz angewendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PRO-Modifikatoren </p> </td> 
   <td colname="col2"> <p>Zeigt an, dass die Datenspalte <span class="wintitle">PER-Modifizierer</span>-Felder repräsentiert. Weitere Informationen finden Sie unter <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  >PER-Modifizierer-Überschriften</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORELIKETHIS]
>
>* [Häufige Probleme beim Hochladen von](https://helpx.adobe.com/de/analytics/kb/common-saint-upload-issues.html)


## Format der Spaltenüberschrift

>[!NOTE] Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.

Classification-Datendateien unterstützen die folgenden Überschriften:

### Schlüssel

Jeder Wert muss innerhalb des Systems eindeutig sein. Der Wert in diesem Feld entspricht einem Wert, den Sie im [!DNL JavaScript]-Beacon für Ihre Website der [!DNL Analytics]-Variablen zugewiesen haben. Daten in dieser Spalte können ~autogen~ oder einen beliebigen anderen eindeutigen Trackingcode beinhalten.

### Überschrift einer Klassifizierungsspalte

In Reports &amp; Analysen werden beispielsweise automatisch zwei Klassifizierungen für [!UICONTROL Campaign] Variablen eingefügt: [!UICONTROL Campaigns] und [!UICONTROL Creative Elements]. Um Daten zur [!UICONTROL Campaigns] Klassifizierung hinzuzufügen, wird die Spaltenüberschrift in der Classification-Datendatei [!UICONTROL Campaigns]verwendet.

>[!NOTE] Die Werte in der [!UICONTROL Classifications] Spaltenüberschrift müssen exakt der Namenskonvention der Klassifizierung entsprechen, andernfalls schlägt der Import fehl. Wenn der Administrator beispielsweise [!UICONTROL Campaigns] in [!UICONTROL Internal Campaign Names] der Spalte &quot; [!UICONTROL Campaign Set-up Manager]Datei&quot;wechselt, muss die Spaltenüberschrift der Datei entsprechend geändert werden.

Darüber hinaus unterstützt die Datendatei die folgenden zusätzlichen Überschriftenkonventionen zur Identifizierung von Unterklassifizierungen und anderen spezialisierten Datenspalten:

### Überschrift einer Unterklassifizierung

Beispielsweise [!UICONTROL Campaigns^Owner] ist eine Spaltenüberschrift für die Spalte mit [!UICONTROL Campaign Owner] Werten vorhanden. Gleichermaßen [!UICONTROL Creative Elements^Size] ist eine Spaltenüberschrift für die Spalte, die die [!UICONTROL Size] Unterklassifizierung der [!UICONTROL Creative Elements] Klassifizierung enthält.

### Klassifizierungsmetrik-Überschriften

For example, [!UICONTROL Campaigns^~Cost] refers to the [!UICONTROL Cost] metric in the [!UICONTROL Campaigns] classification.

### PER-Modifizierer-Überschriften

*`Per Modifier`*-Überschriften werden durch Hinzufügen von *`~per`* zur Klassifizierungsmetrik-Überschrift gekennzeichnet. Wenn die *`Metric`*-Überschrift beispielsweise *`Campaigns^~Cost`* lautet, lautet die Überschrift des PER-Modifizierers *`Campaigns^~Cost~per`*. Adobe unterstützt die folgenden *`PER Modifier`*-Keywords:

Diese Zeichen haben in einer Datendatei eine besondere Bedeutung. Vermeiden Sie nach Möglichkeit die Verwendung dieser Wörter in Attributnamen und -daten.

**BEHOBEN:** Fester Wert. Keine Skalierung durchführen.

**TAG:** Multipliziert den Wert mit der Anzahl der Tage im Bericht.

**BESTELLUNG:** Multipliziert den Wert mit der Anzahl der Bestellungen für den Zeileneintrag im Bericht.

**CHECKOUT:** Multipliziert den Wert mit der Anzahl der Kassengänge für den Zeileneintrag im Bericht.

**EINHEIT:** Multipliziert den Wert mit der Anzahl der Einheiten für den Zeileneintrag im Bericht.

**UMSATZ:** Multipliziert den Wert mit dem Umsatzbetrag für den Zeileneintrag im Bericht.

**SCADD:** Multipliziert den Wert mit der Anzahl der Aufrufe des [!UICONTROL Shopping Cart Add] Ereignisses pro Zeileneintrag im Bericht.

**SCREMOVE:** Multipliziert den Wert mit der Anzahl der Aufrufe des [!UICONTROL Shopping Cart Remove] Ereignisses pro Zeileneintrag im Bericht.

**INSTANZ:** Multipliziert den Wert mit der Anzahl der Instanzen für den Zeileneintrag im Bericht.

**KLICKEN SIE AUF:** Multipliziert den Wert mit der Anzahl der Klicks für den Zeileneintrag im Bericht.

**EREIGNIS:** Multipliziert den Wert mit der Häufigkeit, mit der das angegebene benutzerspezifische Ereignis pro Zeileneintrag im Bericht aufgetreten ist.

**Beispiel:** Wenn Kampagne A 10.000 USD kostet, enthält die [!UICONTROL Campaigns^~Cost] Spalte den Wert 10.000 und die Spalte [!UICONTROL Campaigns^~~Kosten] enthält [!UICONTROL FIXED]. Beim Anzeigen der Kosten für Kampagne A in den Berichten sehen Sie den Betrag von 10.000 USD als Festkosten der Kampagne A für den Datumsbereich.

**Beispiel:** Wenn Kampagne B ca. 2 USD pro Klick kostet, enthält die [!UICONTROL Campaigns^~Cost] Spalte 2 und die Spalte **[!UICONTROL Campaigns^~~Kosten]** enthält [!UICONTROL CLICK]. Beim Anzeigen der Kosten für Kampagne B in den Berichten führt Adobe für den Datumsbereich des Berichts schnell die Kalkulation (2 * [Anzahl Klicks]) durch. Damit erhalten Sie eine Gesamtkostenkalkulation basierend auf im Zuge von Kampagne B erfolgten Klicks.

### Datum

Datumsangaben für Kampagnen sind in der Regel Bereiche (Beginns- und Enddaten), die mit einzelnen Kampagnen verknüpft sind. Datumsangaben sollten im Format JJJJ/MM/TT angezeigt werden. Beispiel: 2013/06/15-2013/06/30.

Weitere Informationen finden Sie unter [Umrechnungsklassifizierungen](https://marketing.adobe.com/resources/help/en_US/admin/index.html#Conversion%20Classifications).

>[!NOTE] Seit der [!DNL Analytics]-Wartungsversion vom 10. Mai 2018 schränkt Adobe die Funktion für datumsaktivierte und numerische Klassifizierungen ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und numerischen Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

## Using dates in conjunction with [!UICONTROL classifications] {#section_966A07B228CD4643B258E73FB8BA150A}

[!UICONTROL Classifications] können Datumsbereiche zu Kampagnen oder anderen Konvertierungen zugewiesen werden, [!UICONTROL classifications]was eine genauere Messung der Kampagne ermöglicht. Nach Angabe des Datumsbereichs eines Werts werden übereinstimmende Werte, die außerhalb des Datumsbereichs auftreten, nicht klassifiziert. Dies ist nützlich für die Messung der Kampagne, die genau die Daten nutzen möchte, zu denen eine Kampagne Live war, und nicht alle Treffer, die mit der Kampagne selbst übereinstimmen. Um einen Wert mit einem Datumsbereich erfolgreich zu klassifizieren, muss Folgendes erfüllt sein:

* The [!UICONTROL classification] must be based on a conversion variable.
* The [!UICONTROL classification] used must be set as Date-Enabled or Numeric 2.
* Der betreffende Datumsbereich muss ein Beginn und (optional) ein Enddatum enthalten.

So klassifizieren Sie Kampagnen anhand des Datumsbereichs:

1. Melden Sie sich bei [!DNL Analytics] an und gehen Sie zu „Admin“ > „Klassifizierungen“.
1. Click the **[!UICONTROL Browser Export]** tab, ensure the settings to your date-enabled classification are correct, then click Export File.
1. Öffnen Sie diese Datei in Microsoft Excel oder einem anderen Tabelleneditor, mit dem Sie vertraut sind.
1. Eine der Spalten endet auf

   ^~Punkt~.
Dies ist die Spalte, in der Sie den Datumsbereich eingeben müssen.
1. Geben Sie unter dieser Spalte den Datumsbereich der einzelnen Werte im folgenden Format ein:

   `YYYY/MM/DD - YYYY/MM/DD`. Bitte stellen Sie Folgendes sicher:

   * Lassen Sie Leerzeichen auf beiden Seiten des Bindestrichs.
   * Verwenden Sie einen Bindestrich (-), um Bereiche zu trennen, nicht einen Gedankenstrich oder einen Geviertstrich.
   * Wenn der Monat oder Tag eine einstellige Zahl ist, gibt es eine führende Null.
   * Der Datumsbereich muss ein Anfangsdatum aufweisen, das Enddatum ist optional.

1. Speichern Sie die Datei und laden Sie sie in [!DNL Analytics] hoch, indem Sie „Admin“ | „Klassifizierungen“ | „Datei importieren“ aufrufen.

>[!NOTE] Ein spezieller Schlüsselwert kann nicht mehrere Datumsbereiche aufweisen.

## Fehlerbehebung für Classifications

* [Häufige Probleme beim Hochladen von](https://helpx.adobe.com/de/analytics/kb/common-saint-upload-issues.html): Knowledge Base-Artikel, in dem Probleme aufgrund von falschen Dateiformaten und Dateiinhalten beschrieben werden.

