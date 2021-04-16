---
description: Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.
keywords: eVar
title: Konversionsvariablen (eVar)
feature: Admin Tools
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 100%

---

# Konversionsvariablen (eVars)

Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.

Wenn eine eVar auf einen Wert für einen Besucher gesetzt wird, merkt Adobe sich automatisch diesen Wert, bis er abläuft. Jedes Erfolgsereignis, das beim Besucher während der eVar-Aktivität eintritt, wird für den eVar-Wert gezählt.

eVars eignen sich am besten zur Messung von Ursache und Wirkung, z. B.:

* Welche internen Kampagnen haben den Umsatz beeinflusst?
* Welche Banneranzeigen haben letztlich zu einer Registrierung geführt?
* Wie viele interne Suchläufe wurden durchgeführt, bevor eine Bestellung aufgegeben wurde?

Wenn eine Trafficmessung oder -pfaderstellung gewünscht wird, wird empfohlen, Traffic-Variablen zu nutzen.

>[!NOTE]
>
>Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [Listenvariablen](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/page-variables.html).

## Konversionsvariablen – Beschreibungen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschreibungen der Felder, die beim [Bearbeiten von Konversionsvariablen](/help/admin/admin/conversion-var-admin/t-conversion-variables-admin.md) verwendet werden.

<table id="table_E48D50926E6B492183300CA58A886927"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Name </span> </p> </td> 
   <td colname="col2"> <p>Der benutzerfreundliche Name der Konversionsvariablen. Dieser Name der eVar wird in der allgemeinen Berichterstattung und als Berichtname im Menü links genutzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Typ</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Der Typ des Variablenwerts: </p> <p> <b>Textzeichenfolge</b>:</span> Erfasst die auf Ihrer Site verwendeten Textwerte. Dies ist der gängigste eVar-Typ und die Standardeinstellung. Diese eVar verhält sich ähnlich wie andere Variablen, bei denen der zugrundeliegende Wert eine statische Textzeichenfolge ist. Wenn Sie beispielsweise interne Kampagnen oder interne Suchkeywords nachverfolgen, ist dies die empfohlene Einstellung. </p> <p> <b>Zähler</b>:</span> Zählt, wie oft eine Aktion stattfindet, bevor sie zum Erfolg führt. Wenn Sie z. B. eine eVar verwenden, um interne Suchvorgänge auf Ihrer Seite zu verfolgen, bewirkt die Werteinstellung auf <span class="uicontrol">Textzeichenfolge</span>, dass Suchbegriffe verfolgt werden. Stellen Sie diesen Wert auf <span class="uicontrol">Zähler</span> ein, um die Zahl der durchgeführten Suchen unabhängig von den verwendeten Suchbegriffen zu zählen. Sie können z. B. eine Zähler-eVar nutzen, um die Anzahl der Male, die jemand vor Tätigen eines Kaufs Ihre interne Suche genutzt hat, zu zählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol">Zuordnung</span> </p> </td> 
   <td colname="col2"> <p>Legt fest, wie in Analytics Gutschriften für ein Erfolgsereignis zugewiesen werden, wenn eine Variable mehrere Werte vor dem Ereignis erhält. Folgende Werte werden unterstützt: </p> <p> <b>Zuletzt verwendet</b>: Der letzte eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft. </p> <p> <b>Ausgangswert</b>: Der erste eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft. </p> <p> <b>Linear</b>: Weist Erfolgsereignisse gleichmäßig allen eVar-Werten zu. Da bei der linearen Zuweisung Werte nur innerhalb eines Besuchs genau verteilt werden, sollten Sie die lineare Zuweisung bei einem eVar-Ablauf von „Besuch“ verwenden. </p> <p>Hinweis: Beim Wechsel zu oder von linearen Werten wird unterbunden, dass historische Daten angezeigt werden. Das Mischen von Zuweisungstypen in der Berichterstellungsoberfläche kann zu falsch angegebenen Daten in Berichten führen. Bei einer linearen Zuweisung etwa könnte der Umsatz auf eine Reihe unterschiedlicher eVar-Werte aufgeschlüsselt werden. Nach dem Zurücksetzen auf die „Zuletzt“-Zuweisung würden 100 % des Umsatzes dem aktuellsten Einzelwert zugewiesen. Diese Zuweisung kann dazu führen, dass Benutzer die falschen Schlüsse ziehen. </p> <p>Um die Wahrscheinlichkeit von Missverständnissen bei der Berichterstellung zu verringern, macht Analytics die historischen Daten für die Oberfläche nicht verfügbar. Wenn Sie sich entscheiden, die gegebene eVar wieder auf die ursprüngliche Zuweisungseinstellung zurückzusetzen, können diese angesehen werden – allerdings sollten Sie die eVar-Zuweisungseinstellungen nicht ändern, bloß um auf historische Daten zugreifen zu können. Adobe empfiehlt, eine neue eVar zu nutzen, wenn neue Zuweisungseinstellungen für bereits aufgezeichnete Daten gewünscht werden, statt die Zuweisungseinstellung einer eVar zu verändern, die bereits eine erhebliche Menge historischer Daten aufgebaut hat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Läuft ab nach</span> </p> </td> 
   <td colname="col2"> <p>Hier wird ein Zeitraum bzw. ein Ereignis angegeben, nach dem der eVar-Wert abläuft (d. h. keine Gutschrift für Erfolgsereignisse mehr erhält). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. </p> <p>Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Tritt das Ereignis nicht ein, läuft die Variable auch nicht ab. </p> <p>Die verfügbaren Ablaufoptionen können in vier Hauptkategorien eingeteilt werden. </p> 
    <ul id="ul_810A37C9B6624F429F2FB45C18F7B43F"> 
     <li id="li_654D9D9044EC4E61AA7ABA372DBF8A93"><b>Auf Ebene einer Seitenansicht oder eines Besuchs.</b> Konversionsereignisse, die über die Seitenansicht oder Besuche hinausgehen, werden nicht mit eVar in Verbindung gebracht. </li> 
     <li id="li_689FBC8B4DAC41B3B0166E6586DD1990"><b>Auf Grundlage eines Zeitraums, z. B. Tag, Woche, Monat oder Jahr.</b> Konversionsereignisse, die über den festgelegten Zeitraum hinausgehen, werden nicht mit eVar in Verbindung gebracht. Der Ablaufzeitraum beginnt mit der Einstellung der Variablen. eVars laufen, ausgehend von dem Zeitpunkt, zu dem sie festgelegt wurden, bei Erreichen der entsprechenden Sekunde (Minute, Stunde, Tag, Monat usw.) ab: 
      <ul id="ul_80C7E3182B6B4356B8A3CA920B81C6D5"> 
       <li id="li_F16F60319CCE406D9EDEFEC0A200BC4D">MINUTE = 60 Sekunden </li> 
       <li id="li_45F47F3F5691415B84052B235DF3BB54">STUNDE = 3.600 Sekunden (60 Minuten) </li> 
       <li id="li_5288CE7D168E4C85B3D9BB67A44D32EC">TAG = 86.400 Sekunden (24 Stunden) </li> 
       <li id="li_60FC8BCD657745EE87B4E458CBA69583">WOCHE = 604.800 Sekunden (7 Tage) </li> 
       <li id="li_7A05A66613C84F929F030310B9567CF5">MONAT = 2.678.400 Sekunden (31 Tage) </li> 
       <li id="li_DCD3CABF59E34D5999B03E606B08AD85">QUARTAL = 8.035.200 Sekunden (93 Tage – 3 Monate mit 31 Tagen) </li> 
       <li id="li_54351D2899454D39A8BA205910D2CCB1">JAHR = 31.536.000 Sekunden (365 Tage) </li> 
      </ul> <p> </p> <p>Wenn ein Besuch am Montag um 7:00 Uhr beginnt und bei diesem Besuch um 7:15 Uhr eVar festgelegt wird, läuft diese wie folgt ab: </p> 
      <ul id="ul_72B311006BE6428698313D251C0940DB"> 
       <li id="li_50925D4A40AD4ACA88704A523138C5B9">Ablauf nach einem Tag: eVar läuft am Dienstag um 7:15 Uhr ab. </li> 
       <li id="li_25846328766D4B4BAF407236C65C956C">Ablauf nach einer Woche: eVar läuft am folgenden Montag um 7:15 Uhr ab. </li> 
       <li id="li_82DB2D7F53304623A5E1241D75C7DF94">Ablauf nach einem Monat: eVar läuft 31 Tage nach diesem Montag um 7:15 Uhr ab. </li> 
      </ul> </li> 
     <li id="li_C132C5C5A5344B91BDF5EB6A1C717C37"><b>Spezifische Konversionsereignisse.</b> Alle sonstigen Konversionsereignisse, die ausgelöst werden, nachdem das spezifische Ereignis, das eVar zugeordnet ist, eintritt. </li> 
     <li id="li_5A782D743FB940649E6CB3E4BEA9B8B6"><b>Nie.</b> Solange das Cookie  <span class="varname"> visitorID</span> intakt ist, kann ein beliebiger Zeitraum zwischen eVar und Ereignis verstreichen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Status</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Hiermit wird der eVar-Status definiert: </p> <p><b>Deaktiviert</b>:</span> Deaktiviert die eVar. Entfernt die eVar aus der Liste der Konversionsvariablen. </p> <p> <b>Keine untergeordneten Beziehungen</b>:</span> Verhindert, dass die eVar durch eine Subrelation unterteilt wird. </p> <p> <b>Grundlegende untergeordnete Beziehungen</b>: </span>Ermöglicht die Aufschlüsselung einer eVar anhand eines Berichts mit vollständigen Subrelationen (z. B. „Produkte“ oder „Kampagnen“). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Zurücksetzen</span> </p> </td> 
   <td colname="col2"> <p>Hiermit werden alle Werte in der eVar zurückgesetzt. </p> <p>Mit dieser Einstellung können Sie verhindern, dass bei einer Neuverwendung einer eVar alte Werte in neuen Berichten verwendet werden. Durch das Zurücksetzen werden historische Daten nicht gelöscht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Merchandisingvariablen können einer oder zwei Syntaxen folgen: </p> <p> <b>Produktsyntax</b>:</span> Hiermit wird einem Produkt der eVar-Wert zugewiesen. Hinweis: Wenn die Produktsyntax ausgewählt ist, ist der Bereich „Merchandising-Binding-Ereignis“ deaktiviert und kann nicht für die Bearbeitung ausgewählt werden. Für diese Syntax können keine Binding-Ereignisse angewendet werden. </p> </p> <p> <b>Syntax der Konversionsvariablen</b>:</span> Hierbei wird einem Produkt nur dann die eVar zugewiesen, wenn ein Binding-Ereignis auftritt. In diesem Fall legen Sie fest, welche Ereignisse als Binding-Ereignisse gelten. </p> <p>Wenn Sie diese Einstellung ändern, ohne den JavaScript-Code zu aktualisieren, gehen Daten verloren. Siehe <a href="https://docs.adobe.com/content/help/de-DE/analytics/components/variables/merchandising-variables/var-merchandising.html">Merchandising-Variablen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising-Binding-Ereignis</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Wenn „Merchandising“ auf <span class="uicontrol">Konversionsvariablensyntax</span> eingestellt ist, wird der aktuelle eVar-Wert durch die ausgewählten Ereignisse mit einem Produkt verbunden. </p> <p>Um ein Binding-Ereignis zu verwenden, setzen Sie <span class="uicontrol">„Zuordnung“ auf „Zuletzt verwendet“</span>. Wenn <span class="uicontrol">„Zuordnung“ auf „Ausgangswert“</span> eingestellt ist, bleibt die erste eVar-Produktverbindung erhalten, bis die eVar abläuft. Sie können mehrere Ereignisse auswählen, indem Sie die <code>ctrl</code>-Taste (Windows) oder die <code>cmd</code>-Taste (Mac) gedrückt halten und auf mehrere Elemente in der Liste klicken. Sie können nur ein Ereignis auswählen, wenn „Konversionsvariablensyntax“ ausgewählt wurde.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Ablauf**

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Beispiel: Wenn Sie eine interne Werbeaktion haben, die am Ende eines Besuchs abläuft, werden für diese interne Werbeaktionen nur Einkäufe oder Registrierungen gezählt, die während des Besuchs erfolgten, in der sie aktiviert wurde.

Es gibt zwei Möglichkeiten für den Ablauf einer eVar:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können das Ablaufen einer eVar erzwingen, indem Sie sie zurücksetzen (z. B. wenn eine Variable für einen anderen Zweck eingesetzt werden soll).

Wenn Sie beispielsweise den Ablauf einer eVar von 30 auf 90 Tage ändern, bleiben die erfassten eVar-Werte für die Dauer des neu eingestellten Ablaufzeitraums (in diesem Fall 90 Tage) erhalten. Das System prüft lediglich die aktuelle Ablaufeinstellung und den letzten festgelegten Zeitstempel des erfassten eVar-Werts, um den Ablauf zu bestimmen. Nur die Option **[!UICONTROL Zurücksetzen]** bewirkt ein unmittelbares Ablaufen von Werten.

Ein weiteres Beispiel: Wenn eine eVar im Mai dazu dienen soll, interne Werbeaktionen widerzuspiegeln (wobei sie nach 21 Tagen ablaufen soll) und im Juni dann eingesetzt wird, um interne Keywords zu erfassen, müssen Sie am 1. Juni ihren Ablauf erzwingen oder die Variable zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

**Groß-/Kleinschreibung**

eVars sind nicht von Schreibweise abhängig, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Beispiel: Wenn eVar1 bei der ersten Instanz den Wert „Angemeldet“ enthält, in den darauf folgenden Instanzen jedoch „angemeldet“ heißt, wird in Berichten immer „Angemeldet“ als Wert von eVar angezeigt.

**Zähler**

Während eVars meist zur Speicherung von Zeichenfolgenwerten dienen, können sie auch so konfiguriert werden, dass sie als Zähler funktionieren. Als Zähler sind eVars dann nützlich, wenn Sie die Anzahl von Aktionen zählen möchten, die ein Benutzer vor einem Ereignis durchführt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Sobald ein Besucher eine Suche durchführt, wird der Wert der eVar um 1 erhöht. Wenn ein Besucher vier Suchen durchführt, bevor er einen Einkauf tätigt, wird Ihnen zu jeder Instanz eine Zählersumme angezeigt (1,00, 2,00, 3,00 und 4.00). Für das Kaufereignis wird jedoch nur die 4,00 gutgeschrieben (Bestellungen und Umsatz). Als Werte für eVar-Zähler sind nur positive Zahlen erlaubt.
