---
description: In diesem Thema erhalten Sie Antworten auf die am häufigsten gestellten Fragen.
subtopic: Data sources
title: Häufig gestellte Fragen zu Data Sources
topic: Developer and implementation
uuid: 394a627f-093c-400a-bfb3-c2aa24568deb
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '1496'
ht-degree: 95%

---


# Häufig gestellte Fragen zu Data Sources

In diesem Thema erhalten Sie Antworten auf die am häufigsten gestellten Fragen.

## Wie können Offline-Daten mit Online-Ereignissen verknüpft werden? {#section_F48A9474A70D4CB8B449DE305F199AD6}

Damit Transaktions-ID-Datenquellen Offline-Daten mit Online-Events verbinden können, müssen Sie die Aufzeichnung der Transaktions-ID aktivieren. Weitere Informationen erhalten Sie unter [Transaktions-ID-Aufzeichnung](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C).

## Wie viel kostet die Nutzung der Datenquelle-Funktion? {#section_0B84E3E8891B45E8970EA9D8AAD1ADEC}

Für die Nutzung der Data Sources-Applikation fallen keine weiteren Gebühren außer dem Standard-Server-Aufruf an. Server-Aufruf-gebühren gelten nur für Datenquellen-Typen mit vollständiger Verarbeitung, bei denen einzelne Treffer als Datenzeilen gesendet werden. Traffic- und Datenquellen auf aggregierter Ebene führen nicht zu zusätzlichen Kosten.

## Wie kann ich in Data Sources-Dateien Kommentare einfügen? {#section_AA42152C7B30425EA541A7BA274E78ED}

Jede Zeile in einer Data Sources-Datei, die mit einem Nummernzeichen (#) beginnt, wird als Kommentar interpretiert.

## Muss ich in meine Tabellendaten eine Datumsspalte einfügen? {#section_EA37F5FFB13446C497B3C64943F7084E}

Ja. Da viele Marketingberichte auf der Datumsspalte basieren, benötigt Data Sources eine Datumsspalte.

## Kann ich Daten in bestehenden und bereits verwendeten Variablen speichern? {#section_AB557C2997D04EAFBDC61398B13D13C6}

Adobe empfiehlt, dass Sie neue, noch nicht verwendete Variablen auswählen, um Daten mit Data Sources zu importieren. Wenn Sie sich bei der Konfiguration der Datendatei unsicher sind oder die Risiken einer erneuten Nutzung von Variablen besser verstehen möchten, setzen Sie sich mit der Kundenunterstützung in Verbindung.

## Kann ich Daten löschen, die mit Data Sources importiert wurden? {#section_DB73BC06BD774738BF019B347D9DED96}

Nein. Daten, die mit Data Sources in Berichte hochgeladen wurden, können nach dem Import nicht entfernt werden, auch nicht von Adobe-Mitarbeitern. Sie werden dauerhaft in die bestehenden Daten eingefügt und lassen sich nicht von den mit herkömmlichen Datenerfassungsmaßnahmen (z. B. JavaScript, ActionSource, Data Insertion API) eingegebenen Daten unterscheiden. Daher empfiehlt Adobe dringend, dass Sie Data Sources-Daten in eine Report Suite zum Testen laden, bevor Sie sie in eine Produktionssuite hochladen.

## Wie viele Daten kann ich gleichzeitig importieren? {#section_7A76D59E2C5B434D9BDBD2ABD2873168}

Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Um Verzögerungen beim Generieren von Berichten auf ein Minimum zu reduzieren, laden Sie pro Tag nicht mehr als die Daten von 90 Tagen hoch.

## Werden bestehende Daten überschrieben, wenn ich Daten über Data Sources importiere? {#section_BDBD16D0AFD54D55AFDB8AC77D35FE77}

Daten aus Data Sources überschreiben nie bestehende Berichtsdaten. Stattdessen werden die mit Data Sources hochgeladenen Daten den bestehenden Daten hinzugefügt.

## Warum werden nicht auch meine Metriken angezeigt, wenn ich Daten über Data Sources hochladen? {#section_33176B39744F4F5A861E69AD87B99B78}

Wenn Sie Daten aus Data Sources hochladen, laden Sie die Metriken hoch, die in der Berichtsoberfläche zur Verfügung stehen werden.

Wenn Sie beispielsweise den Call-Center-Umsatz für Produkte hochladen, die Sie über Ihre Site vertreiben, kann der Call-Center-Umsatz im gleichen Bericht wie der Online-Umsatz angezeigt werden. Sie können sie jedoch nicht zusammen mit Besuchen verwenden, da Sie damit nicht die Anzahl der Besuche hochgeladen haben. Adobe kann nur Berichte für die Metriken und Elemente erstellen, die Sie über Data Sources hochgeladen haben (neben den normalen Marketingberichtsmetriken).

## Was passiert, wenn ich über Data Sources negative Werte in Berichte einfüge? {#section_77E5F37F3CFB4407BA32A91E6F3132B2}

Der Wert wird entsprechend verringert.

## Worin besteht der Unterschied zwischen einer Traffic- und einer (generischen) Konversion-Datenquelle? {#section_A34C952490814D4FB802F22D9FB3E9F8}

Die Traffic-Datenquelle wird sehr viel schneller hochgeladen, da sie nur die zusammenfassenden Werte in den entsprechenden Tabellen aktualisiert. Die generische Datenquelle mit Konversion-Daten (Ereignisse usw.) erstellt für jeden Wert in der Spalte, die verarbeitet werden soll, einen Hit.

Beispieldatei:

<table id="table_D5408E0BDB984229B4C60A66BB53CEBB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code> Date </code> </p> </td> 
   <td colname="col2"> <p> <code> Event15 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code> 01/01/2013 </code> </p> </td> 
   <td colname="col2"> <p> <code> 553 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

Im oben aufgeführten Beispiel werden 553 Hits erzeugt, die im Cache-System verarbeitet werden sollen.

## Berücksichtigt Data Sources untergeordnete Beziehungen, Korrelationen und Pfade? {#section_7ABAE2F3C4DD48E18FB8CB20AE8AFD14}

Da der Datenquelle-Prozess („für generische DS, nicht Datenverkehr“) einzelne Hits erstellt, die vom Cache verarbeitet werden, wird der Prozess für untergeordnete Beziehungen und nicht der Korrelationsprozess verwendet. Pfade können potenziell verarbeitet werden, aber jeder Hit würde für einen eigenen Besuch stehen, sodass keine Pfade generiert werden. Pfaddaten werden für Webprotokoll-Importe generiert.

## Muss bei der Dateierweiterung die Groß- und Kleinschreibung für eine Datenquelle-Upload- oder Classification-Datei beachtet werden? {#section_710787BA4D8C403D8326D666807832B8}

Wenn die Erweiterungen einer Datenquelle-Upload-Datei oder einer Classification-Datei großgeschrieben sind, werden die Dateien nicht verarbeitet. Erweiterungen einer Datenquelle-Upload-Datei müssen kleingeschrieben werden. So werden beispielsweise [!DNL file.TXT] und [!DNL file.FIN] nicht verarbeitet. Auch [!DNL .TAB] und [!DNL .FIN] werden nicht verarbeitet. [!DNL .txt] und [!DNL .fin] werden jedoch verarbeitet.

## Kann ich weitere Ereignisse zur generierten Vorlage hinzufügen oder liegt das Maximum bei drei? {#section_F184913926DD43B1872956CED308ADB5}

Sie können beliebig viele Ereignisse hinzufügen. Der Assistent erlaubt jedoch nur drei Ereignisse. Sobald die Vorlagendatei erstellt wurde, können Sie bei Bedarf weitere Ereignisse hinzufügen.

## Was geschieht mit einer Datenquelle-Datei, in der mindestens einer der Datensätze nicht die gleiche Anzahl Spalten wie der Header-Datensatz hat? {#section_2666949CB11B49768774C904C93A16D4}

Bei einer Datenquelle-Datei, in der mindestens einer der Datensätze nicht die gleiche Anzahl Spalten wie der Header-Datensatz hat, passiert Folgendes.

* Der Ersteller der Datenquelle erhält eine E-Mail, in der er auf den Fehler hingewiesen wird.
* Die Datei wird aufgrund der ungleichen Spaltenanzahl nicht verarbeitet.

## Wird mit Data Sources-Informationen eine Datenaggregation durchgeführt? {#section_E0E44C55A84245918E7CF5A4232F5C88}

Mit Data Sources-Informationen kann eine Datenaggregation durchgeführt werden. Die Adobe-Kundenunterstützung muss die Datenaggregation jedoch ab den historischen Daten erneut verarbeiten, um die historischen Daten einzuschließen. Wenn das aktuelle Datum z. B. der 31. Oktober 2015 ist und Sie Daten für den 1. bis 15. August 2015 mit Data Sources hochladen, muss die Datenaggregation so eingerichtet sein, dass eine neue Verarbeitung ab dem 1. August 2015 durchgeführt wird, damit die neu importierten Daten eingeschlossen werden.

Beachten Sie zudem, dass Daten niemals direkt über Data Sources in eine Datenaggregations-Report-Suite hochgeladen werden sollten. Wenn diese Daten in einer Datenaggregation eingeschlossen werden sollen, müssen Sie in eine standardmäßige Report Suite importiert werden, die auch als *`child suite`* der Datenaggregation bezeichnet wird. Wenden Sie sich an die Adobe-Kundenunterstützung, um weitere Informationen zu erhalten.

## Warum enthält der Seitenansichtsbericht keine Data Sources-Daten für einen einzelnen Tag, sondern die korrekten Daten für eine Woche? {#section_E361A93AFDE1487989B4B0C4438EEDF7}

Data Sources erfasst keine Daten auf Stundenbasis. Wenn Sie einen Bericht für einen bestimmten Tag ausführen möchten, können die Daten nur stundenweise unterteilt werden, sodass nichts im Bericht angezeigt wird. Sie können nur Daten sehen, wenn die Unterteilung auf Tagesbasis oder in einem größeren Zeitraum erfolgt, indem Sie einen Wochen- oder Monatsbericht ausführen.

## Wie werden „Unique Visitors“ in einem Webserver-Protokoll Datenquelle-Upload berechnet? {#section_477FEDFD1DBE45278E7D09AFBD59CDAC}

Die Anzahl an einmaligen Besuchern in einem Webserver-Protokoll wird als spezifische Kombination aus *`IP Address`* und *`User Agent`* im Webprotokoll berechnet. Jede einzigartige Kombination dieser beiden Elemente wird als Unique Visitor berechnet. Wenn die Spalte [!UICONTROL Benutzeragent] leer ist (oder nicht im Webprotokoll eingeschlossen ist), können wir nicht die Anzahl an Unique Visitors ermitteln, sodass der gesamte Upload als ein Unique Visitor zählt (selbst wenn mehrere IP-Adressen vorliegen).

## Wie kann ich in Data Sources herausfinden, welche Anmeldeinformationen zu welcher Report Suite gehören? {#section_8EF9D22D5BE14C218724B06E78EF7DF4}

Die Report Suite-ID ist in Data Sources der erste Teil der Anmeldeinformationen, an den eine zufällige Nummer angehängt wird, die die jeweilige Datenquelle kennzeichnet, die eingerichtet wurde. Beispiel: `RSID-drmossdev5 Login-drmossdev5_0001343430`.

## Wie wirken sich die Version 15 und die Segmentierung auf Datenquellen aus? {#section_7E9E541DB73C49CDAADC031B678F8678}

In Version 15 weist Data Sources je nach Quelltyp ein unterschiedliches Verhalten auf:

* Datenquellen mit vollständiger Verarbeitung, Webprotokollen und Transaktions-ID werden normal angezeigt. Wenn Segmente angewendet werden, werden die Daten entsprechend den Segmentregeln gefiltert.
* Standard- oder Konversionsdatenquellen (Werbekampagnen, CRM, Kundenzufriedenheit, Siteperformance, allgemeine Zusammenfassungsdaten, Onlinekäufe, Interessenten und Angebote sowie Offlinekanaldaten) werden in Version 15 angezeigt. Da diese Datenquellen jedoch nicht an Besuche oder Besucher gebunden sind, werden sie beim Anwenden von Segmenten herausgefiltert.

## Sind Metriken, die mit einer Transaktions-ID importiert werden, in Clickstream Data Feeds und Data Warehouse verfügbar? {#section_01CD14CA3E11490CB2CBA433C649029E}

Der Data Feed enthält alle Metriken mit Transaktions-IDs, die empfangen wurden. Wenn Sie jedoch Transaktions-ID-Daten für ein Datum in der Vergangenheit hochladen, können diese Daten nur abgerufen werden, indem Sie den Data Feed erneut für diesen Tag herunterladen.

## Sind eVars, die aktuell im Besucherprofil bestehen, Metriken zugeordnet, die mithilfe von Datenquellen hochgeladen wurden? {#section_1748BD5C6A12467F8082E07D6A9CD595}

Im Falle einer vollen Verarbeitung ist dies nicht der Fall, im Falle von Transaktions-IDs trifft dies zu. Datenquellen mit vollständiger Verarbeitung werden mit getrennten Besucherprofilen verarbeitet. Das heißt, selbst wenn die Besucher-IDs übereinstimmen, werden sie aus der Sicht einer eVar-Zuordnung nicht aneinander gebunden. Transaktions-ID-Datenquellen werden an das Hauptbesucherprofil gebunden, sodass bestehende eVars Ereignissen zugeordnet werden, die mit einer Transaktions-ID hochgeladen wurden.

## Beeinflussen die mit Datenquellen hochgeladenen eVars das spätere Online-Verhalten? {#section_0B490CEAAB604826AFD3E8B2531C8F2D}

Nein. Die mit Transaktions-ID-Datenquellen hochgeladenen eVars führen in den gespeicherten Profilinformationen lediglich Lesevorgänge aus, das Profil wird nicht aktualisiert.
Nein. eVars sind die einzigen Variablen, die im Schnappschuss des Besucherprofils gespeichert werden.

## Wie funktionieren numerische und Währungs-Ereignis mit Datenquellen?

Die Vollverarbeitung unterstützt nur Legacy-Ereignis-Listen, wobei der numerische/Währungs-/Zählerwert (mehr als 1) direkt in der Ereignis-Liste, das heißt `"eventNN,eventKK"` nicht `"eventNN=#.##"`, ausgeschlossen wird. Dies bedeutet, dass es nur ein Zähler-Ereignis unterstützt, wenn es in der Datenquellendatei in der Spalte &quot;Ereignis&quot;übergeben wird und um 1 inkrementiert wird.

Wenn numerische, Währungs- oder Zählerwerte (mehr als 1) erforderlich sind, verwenden Sie die Liste des Produkts:

```js
s.products="Footwear;Running Shoes;1;99.99;event1=4.50";
s.products="Footwear;Running Shoes;1;99.99;event1=4.50|event4=1.99";
```
