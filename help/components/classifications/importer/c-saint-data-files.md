---
description: Mit dem Importeur können Sie Classification-Daten in großen Mengen in Form einer Classification-Datendatei in die Analytics-Berichterstellung hochladen. Für den Import ist ein besonderes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden.
subtopic: Classifications
title: Klassifizierungsdatendateien
topic: Admin tools
uuid: f27bb812-56e0-472a-9993-d869f0fea700
translation-type: tm+mt
source-git-commit: af41b67c4fb1bb3cfe363be5619d382399cf5bca
workflow-type: tm+mt
source-wordcount: '1771'
ht-degree: 100%

---


# Klassifizierungsdatendateien

Mit dem Importeur können Sie Classification-Daten in großen Mengen in Form einer Classification-Datendatei in die Analytics-Berichterstellung hochladen. Für den Import ist ein besonderes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden.

Zum Erstellen gültiger Datendateien können Sie eine Vorlage herunterladen, die Ihnen eine Dateistruktur zur Verfügung stellt, in die Sie die Classification-Daten einfügen können. Weitere Informationen finden Sie unter [Klassifizierungsvorlage herunterladen](/help/components/classifications/importer/c-download-saint-data.md).

Weitere Informationen zu Zeichenbeschränkungen in Klassifizierungen finden Sie unter [Allgemeine Dateistruktur](/help/components/classifications/importer/c-saint-data-files.md).

## Allgemeine Dateistruktur

Die folgende Abbildung zeigt eine Beispieldatendatei:

![](assets/completed-saint-file.png)

Eine Datendatei muss den folgenden Strukturregeln entsprechen:

* Der Wert von Classifications darf nicht 0 (null) sein.
* Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.
* Hochgeladene Dateien sollten die Zeichenkodierung UTF-8 ohne BOM verwenden.
* Sonderzeichen wie Tabulatoren, Zeilenumbrüche und Anführungszeichen können in eine Zelle eingebettet werden, wenn das v2.1-Dateiformat angegeben und die Zelle ordnungsgemäß [maskiert wurde](/help/components/classifications/importer/t-classifications-escape-data.md). Sonderzeichen umfassen:

   ```
   \t     tab character 
   \r     form feed character 
   \n    newline character 
   "       double quote
   ```

   Das Komma ist kein Sonderzeichen.

* Classifications können kein Caret (^) enthalten, da mit diesem Zeichen eine Unter-Classification gekennzeichnet wird.
* Vorsicht bei der Verwendung von Bindestrichen. Wenn Sie beispielsweise einen Bindestrich (-) in einem sozialem Begriff verwenden, erkennt Social ihn als [!DNL Not]-Operator (Minuszeichen). Wenn Sie beispielsweise mit dem Import *`fragrance-free`* als Begriff angeben, interpretiert Social den Begriff folgendermaßen: Parfüm *`minus`* frei. Dadurch werden Wortlaute mit den Begriffen *`fragrance`*, jedoch nicht *`free`* erfasst.
* Zeichenbeschränkungen werden erzwungen, um Berichtdaten zu klassifizieren. Wenn Sie beispielsweise eine Klassifizierungstextdatei für Produkte (*`s.products`*) mit Produktnamen mit mehr als 100 Zeichen (Byte) hochladen, werden die Produkte nicht in den Berichten angezeigt. Für Trackingcodes und für alle benutzerdefinierten Konversionsvariablen (eVars) sind jeweils 255 Byte zulässig.
* Tabulatorgetrennte Datendatei (Sie können die Vorlagendatei mit jeder Tabellenkalkulationsanwendung oder einem Texteditor erstellen).
* Die Dateierweiterung muss entweder [!DNL .tab] oder [!DNL .txt] lauten.
* Ein Rautenzeichen (#) kennzeichnet eine Zeile als Benutzerkommentar. Sämtliche mit # beginnenden Zeilen werden von Adobe ignoriert.
* Ein doppeltes Rautenzeichen, gefolgt von SC (## SC) kennzeichnet die Zeile als Kopfzeilenkommentar vor der Verarbeitung, der von der Berichterstellung genutzt wird. Löschen Sie diese Zeilen nicht.
* Classification-Exporte können aufgrund von Zeilenumbruchzeichen im Schlüssel doppelte Schlüssel aufweisen. Bei einem FTP- oder Browser-Export können Sie dies vermeiden, indem Sie Anführungszeichen für das FTP-Konto aktivieren. Dadurch wird jeder Schlüssel mit Zeilenumbruchzeichen in Anführungszeichen gesetzt.
* Die Zelle C1 in der ersten Zeile der Importdatei enthält eine Versionskennung, die festlegt, wie Classifications die Verwendung von Anführungszeichen im Rest der Datei handhaben.

   * v2.0 ignoriert Anführungszeichen und nimmt an, dass sie alle Bestandteil der angegebenen Schlüssel und Werte sind. Beachten Sie z. B. diesen Wert: &quot;Dies ist &quot;&quot;irgendein Wert&quot;&quot;&quot;. v2.0 würde dies wörtlich wie folgt interpretieren: &quot;Dies ist &quot;&quot;irgendein Wert&quot;&quot;&quot;.
   * v2.1 teilt Classifications mit, dass sie Anführungszeichen als Bestandteil der in Excel-Dateien verwendeten Dateiformatierungen betrachten sollen. Daher würde v2.1 das obenstehende Beispiel wie folgt umformatieren: Dies ist &quot;irgendein Wert&quot;.
   * Es kann zu Problemen kommen, wenn in der Datei v2.1 angegeben ist, jedoch tatsächlich v2.0 gewünscht wurde – und zwar, wenn Anführungszeichen auf eine Weise verwendet werden, die bei Excel-Formatierung nicht zulässig wäre. Z. B., wenn folgender Wert vorliegt: „VP NO REPS“ S/l Dress w/ Overlay. Im Fall von v2.1 ist diese Formatierung nicht korrekt (der Wert sollte von öffnenden und schließenden Anführungszeichen eingeschlossen sein, und Anführungszeichen, die Bestandteil des eigentlichen Werts sind, müssen von Anführungszeichen umgeben sein), und Classifications funktionieren über diesen Punkt hinaus nicht.
   * Vergewissern Sie sich, dass Sie eine der folgenden Aktionen durchführen: Ändern Sie das Dateiformat in v2.0, indem Sie die Kopfzeile (Zelle C1) in den Dateien ändern, die Sie hochladen, ODER setzen Sie die Anführungszeichen für Excel in allen Ihren Dateien korrekt um.

* Die erste (Nicht-Kommentar)-Zeile der Datendatei enthält die Spaltenüberschriften, die die Classification-Daten in der Spalte bezeichnen. Für Spaltenüberschriften ist im Importeur ein bestimmtes Format erforderlich. Weitere Informationen finden Sie unter [Format der Spaltenüberschrift](/help/components/classifications/importer/c-saint-data-files.md).
* Unmittelbar auf die Überschriftenzeile in einer Datendatei folgen die Datenzeilen. Jede Zeile mit Daten sollte ein Datenfeld für jede Spaltenüberschrift enthalten.
* Die Datendatei unterstützt die folgenden Steuercodes, die von Adobe genutzt werden, um die Datei zu strukturieren und Classification-Daten korrekt zu importieren:

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
   <td colname="col2"> <p>Ein Neue-Zeile-Zeichen ist das einzig unterstützte Trennzeichen zwischen Datenzeilen/Datensätzen in der Datendatei. In der Regel müssen Sie diese Zeichen nur spezifisch einfügen, wenn Sie ein Programm zur automatischen Erzeugung von Datendateien schreiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~autogen~ </p> </td> 
   <td colname="col2"> <p>Fordert an, dass Adobe automatisch eine eindeutige ID für dieses Element erzeugt. </p> <p>In Zusammenhang mit Kampagnen weist dieser Steuercode Adobe an, jedem kreativen Element eine Kennzeichnung zuzuweisen. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >Schlüssel</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~period~ </p> </td> 
   <td colname="col2"> <p>Zeigt an, dass die Datenspalte den dem Element zugeordneten Datenbereich widerspiegelt. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >Datum</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeres Feld </p> </td> 
   <td colname="col2"> <p>Repräsentiert einen NULL-Wert für das aktuelle Feld. Verwenden Sie dies, wenn eine bestimmte Datenspalte nicht für den aktuellen Datensatz einbezogen werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PRO-Modifizierer </p> </td> 
   <td colname="col2"> <p>Zeigt an, dass die Datenspalte <span class="wintitle">PER-Modifizierer</span>-Felder repräsentiert. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >PER-Modifizierer-Überschriften</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORELIKETHIS]
>
>* [Häufige Probleme beim Hochladen von](https://helpx.adobe.com/de/analytics/kb/common-saint-upload-issues.html)


## Format der Spaltenüberschrift

>[!NOTE]
>
>Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.

Classification-Datendateien unterstützen die folgenden Überschriften:

### Schlüssel

Jeder Wert muss innerhalb des Systems eindeutig sein. Der Wert in diesem Feld entspricht einem Wert, den Sie im [!DNL JavaScript]-Beacon für Ihre Website der [!DNL Analytics]-Variablen zugewiesen haben. Daten in dieser Spalte können ~autogen~ oder einen beliebigen anderen eindeutigen Trackingcode beinhalten.

### Überschrift einer Klassifizierungsspalte

Reports &amp; Analytics enthalten beispielsweise automatisch zwei Classifications für [!UICONTROL Kampagnen] variablen: [!UICONTROL Kampagnen] und [!UICONTROL Kreative Elemente]. Um Daten zur [!UICONTROL Kampagnen]-Classification hinzuzufügen, muss die Spaltenüberschrift in der Classification-Datendatei [!UICONTROL Campaigns] lauten.

>[!NOTE]
>
>Die Werte in der Überschrift der Spalte [!UICONTROL Klassifizierungen] müssen die Namenskonvention für Klassifizierungen exakt erfüllen, da sonst der Import fehlschlägt. Wenn der Administrator beispielsweise im [!UICONTROL Campaign Set-up Manager] [!UICONTROL Campaigns] in [!UICONTROL Internal Campaign Names] ändert, muss dies ebenfalls in die Spaltenüberschrift übernommen werden.

Darüber hinaus unterstützt die Datendatei weitere Überschriftenkonventionen zur Kennzeichnung von Unter-Classifications und anderen spezialisierten Datenspalten:

### Überschrift einer Unterklassifizierung

Beispielsweise ist [!UICONTROL Campaigns^Owner] eine Spaltenüberschrift für die Spalte, die Werte zum [!UICONTROL Kampagnenverantwortlichen] enthält. Vergleichbar ist [!UICONTROL Creative Elements^Size] eine Spaltenüberschrift für die Spalte, die die [!UICONTROL Größen]-Unter-Classification der [!UICONTROL Kreative-Elemente]-Classification enthält.

### Klassifizierungsmetrik-Überschriften

So bezieht sich beispielsweise [!UICONTROL Campaigns^~Cost] auf die [!UICONTROL Kosten] metrik in der [!UICONTROL Kampagnen]-Classification.

### PER-Modifizierer-Überschriften

*`Per Modifier`*-Überschriften werden durch Hinzufügen von *`~per`* zur Klassifizierungsmetrik-Überschrift gekennzeichnet. Wenn die *`Metric`*-Überschrift beispielsweise *`Campaigns^~Cost`* lautet, lautet die Überschrift des PER-Modifizierers *`Campaigns^~Cost~per`*. Adobe unterstützt die folgenden *`PER Modifier`*-Keywords:

Diese Zeichen haben in einer Datendatei eine spezielle Bedeutung. Vermeiden Sie nach Möglichkeit, diese Wörter in Attributnamen und -daten zu verwenden.

**FIXED:** Fester Wert. Es wird keine Skalierung durchgeführt.

**TAG:** Multipliziert den Wert mit der Anzahl der Tage im Bericht.

**BESTELLUNG:** Multipliziert den Wert mit der Anzahl der Bestellungen für den Zeileneintrag im Bericht.

**KASSE:** Multipliziert den Wert mit der Anzahl der Kassengänge für den Zeileneintrag im Bericht.

**EINHEIT:** Multipliziert den Wert mit der Anzahl der Einheiten für den Zeileneintrag im Bericht.

**UMSATZ:** Multipliziert den Wert mit dem Umsatz für den Zeileneintrag im Bericht.

**SCADD:** Multipliziert den Wert mit der Anzahl des auftretenden Ereignisses [!UICONTROL Zusatz zum Warenkorb] pro Zeileneintrag im Bericht.

**SCREMOVE:** Multipliziert den Wert mit der Anzahl des auftretenden Ereignisses [!UICONTROL Entnahme aus Warenkorb] pro Zeileneintrag im Bericht.

**INSTANZ:** Multipliziert den Wert mit der Anzahl der Instanzen für den Zeileneintrag im Bericht.

**KLICK:** Multipliziert den Wert mit der Anzahl der Klicks für den Zeileneintrag im Bericht.

**EREIGNIS:** Multipliziert den Wert mit der Anzahl der auftretenden, jeweils angegebenen benutzerspezifischen Ereignisse pro Zeileneintrag im Bericht.

**Beispiel:** Wenn Kampagne A 10.000 USD kostet, enthält die Spalte [!UICONTROL Campaigns^~Cost] den Wert 10000, und die Spalte [!UICONTROL Campaigns^~Cost~per] enthält die Angabe [!UICONTROL FIXED]. Beim Anzeigen der Kosten für Kampagne A in den Berichten sehen Sie den Betrag von 10.000 USD als Festkosten der Kampagne A für den Datumsbereich.

**Beispiel:** Wenn Kampagne B ca. 2 USD pro Klick kostet, enthält die Spalte [!UICONTROL Campaigns^~Cost] den Wert 2 und die Spalte **[!UICONTROL Campaigns^~Cost~per]** enthält die Angabe [!UICONTROL CLICK]. Beim Anzeigen der Kosten für Kampagne B in den Berichten führt Adobe für den Datumsbereich des Berichts schnell die Kalkulation (2 * [Anzahl Klicks]) durch. Damit erhalten Sie eine Gesamtkostenkalkulation basierend auf im Zuge von Kampagne B erfolgten Klicks.

### Datum

Kampagnendatumsangaben sind üblicherweise Datumsbereiche (Start- und Enddaten), die einzelnen Kampagnen zugewiesen wurden. Datumsangaben müssen das Format JJJJ/MM/TT aufweisen, zum Beispiel 2013/06/15-2013/06/30.

Weitere Informationen finden Sie unter [Konversion-Classifications](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/conversion-variables/conversion-classifications.html).

>[!NOTE]
>
>Seit der [!DNL Analytics]-Wartungsversion vom 10. Mai 2018 schränkt Adobe die Funktion für datumsaktivierte und numerische Klassifizierungen ein. Diese Classification-Typen wurden aus den Admin- und Classification Importer-Schnittstellen entfernt. Es können keine neuen datumsaktivierten und Numerisch-Classifications hinzugefügt werden. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf verwaltet (hochgeladen, gelöscht) werden und stehen auch noch für die Berichterstellung zur Verfügung.

## Verwendung von Datumsangaben zusammen mit [!UICONTROL Klassifizierungen ]{#section_966A07B228CD4643B258E73FB8BA150A}

Mit [!UICONTROL Klassifizierungen] können Sie Datumsbereiche zu Ihren Kampagnen oder anderen Konversions [!UICONTROL klassifizierungen] zuweisen, um eine genauere Kampagnenmessung zu erreichen. Nachdem Sie den Datumsbereich eines Wertes angegeben haben, werden übereinstimmende Werte, die außerhalb des Datumsbereichs auftreten, nicht klassifiziert. Dies ist für Kampagnenmessungen nützlich, bei denen die genauen Tage genutzt werden sollen, an denen die Kampagne aktiv war, und nicht alle Hits, die mit der Kampagne selbst übereinstimmen. Um einen Wert erfolgreich mit einem Datumsbereich zu klassifizieren, müssen die folgenden Voraussetzungen erfüllt werden:

* Die [!UICONTROL Klassifizierung] muss auf einer Konversionsvariable basieren.
* Die verwendete [!UICONTROL Klassifizierung] muss auf „Datumsaktiviert“ oder „Numerisch 2“ eingestellt sein.
* Der betreffende Datumsbereich muss ein Anfangsdatum und (optional) ein Enddatum enthalten.

So klassifizieren Sie Kampagnen basierend auf einem Datumsbereich:

1. Melden Sie sich bei [!DNL Analytics] an und gehen Sie zu „Admin“ > „Klassifizierungen“.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Browser-Export]**, stellen Sie sicher, dass die Einstellungen für die datumsaktivierte Classification richtig sind, und klicken Sie dann auf „Datei exportieren“.
1. Öffnen Sie diese Datei in Microsoft Excel oder einem anderen Tabelleneditor, mit dem Sie vertraut sind.
1. Eine der Spalten endet auf

   ^~Punkt~.
Dies ist die Spalte, in der Sie den Datumsbereich eingeben müssen.
1. Geben Sie unter dieser Spalte den Datumsbereich der einzelnen Werte im folgenden Format ein:

   `YYYY/MM/DD - YYYY/MM/DD`. Achten Sie dabei auf Folgendes:

   * Behalten Sie die Leerzeichen vor und nach dem Bindestrich bei.
   * Trennen Sie Bereiche mit einem Bindestrich (-) und nicht mit einem Gedankenstrich oder Geviertstrich.
   * Wenn der Monat oder Tag einstellig ist, muss eine Null vorangestellt werden.
   * Der Datumsbereich muss ein Anfangsdatum aufweisen, das Enddatum ist optional.

1. Speichern Sie die Datei und laden Sie sie in [!DNL Analytics] hoch, indem Sie „Admin“ | „Klassifizierungen“ | „Datei importieren“ aufrufen.

>[!NOTE]
>
>Ein spezieller Schlüsselwert kann nicht mehrere Datumsbereiche aufweisen.

## Fehlerbehebung für Classifications

* [Häufige Probleme beim Hochladen von](https://helpx.adobe.com/de/analytics/kb/common-saint-upload-issues.html): Knowledge Base-Artikel, in dem Probleme aufgrund von falschen Dateiformaten und Dateiinhalten beschrieben werden.

