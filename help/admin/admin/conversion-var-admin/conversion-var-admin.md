---
description: Die Custom Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site im Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. An eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.
keywords: eVar
title: Konversionsvariablen (eVar)
topic: Admin tools
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Konversionsvariablen (eVars)

Die Custom Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site im Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. An eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.

Wenn eine eVar auf einen Wert für einen Besucher gesetzt wird, speichert Adobe automatisch diesen Wert, bis er abläuft. Alle Erfolgsereignisse, auf die ein Besucher stößt, während der eVar-Ereignis aktiv ist, werden in den eVar-Wert einbezogen.

eVars eignen sich am besten zur Messung von Ursache und Wirkung, z. B.:

* Welche internen Kampagnen beeinflussten den Umsatz
* Welche Banneranzeigen führten letztendlich zu einer Registrierung?
* Die Häufigkeit, mit der eine interne Suche verwendet wurde, bevor eine Bestellung aufgegeben wurde

Wenn Traffic-Messungen oder Pfade gewünscht werden, wird die Verwendung von Traffic-Variablen empfohlen.

>[!NOTE] Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [Listenvariablen](https://marketing.adobe.com/resources/help/de_DE/sc/implement/listN.html).

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
   <td colname="col2"> <p>Der Anzeigename der Konversionsvariablen. Auf diese Weise wird die eVar im Berichte referenziert und der Berichtname im Menü links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Typ</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Der Typ des Variablenwerts: </p> <p> <b>Textzeichenfolge</b>:</span> Erfasst die auf Ihrer Site verwendeten Textwerte. Dies ist der am häufigsten verwendete eVar-Typ und die Standardeinstellung. Es funktioniert ähnlich wie andere Variablen, bei denen der Wert darin eine statische Textzeichenfolge ist. Wenn Sie Dinge wie interne Kampagnen oder interne Suchbegriffe verfolgen, ist dies die empfohlene Einstellung. </p> <p> <b>Zähler</b>:</span> Zählt, wie oft eine Aktion stattfindet, bevor sie zum Erfolg führt. Wenn Sie z. B. eine eVar verwenden, um interne Suchvorgänge auf Ihrer Seite zu verfolgen, bewirkt die Werteinstellung auf <span class="uicontrol">Textzeichenfolge</span>, dass Suchbegriffe verfolgt werden. Stellen Sie diesen Wert auf <span class="uicontrol">Zähler</span> ein, um die Zahl der durchgeführten Suchen unabhängig von den verwendeten Suchbegriffen zu zählen. Beispielsweise können Sie mit einer Zähler-eVar verfolgen, wie oft jemand Ihre interne Suche verwendet hat, bevor er einen Kauf tätigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Zuordnung </span> </p> </td> 
   <td colname="col2"> <p>Legt fest, wie Analytics Gutschriften für ein Erfolgsereignis zuweist, wenn eine Variable mehrere Ereignis vor dem Ereignis erhält. Zu den unterstützten Werten gehören: </p> <p> <b>Zuletzt verwendet</b>: Der letzte eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft. </p> <p> <b>Ausgangswert</b>: Der erste eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft. </p> <p> <b>Linear</b>: Weist Erfolgsereignisse gleichmäßig allen eVar-Werten zu. Da bei der linearen Zuweisung Werte nur innerhalb eines Besuchs genau verteilt werden, sollten Sie die lineare Zuweisung bei einem eVar-Ablauf von „Besuch“ verwenden. </p> <p>Hinweis: Beim Wechsel zu oder von linearen Werten wird unterbunden, dass historische Daten angezeigt werden. Das Mischen von Zuordnungstypen in der Benutzeroberfläche des Berichte kann zu falsch angegebenen Daten in Berichten führen. Beispielsweise könnte die lineare Zuordnung den Umsatz auf eine Reihe unterschiedlicher eVar-Werte aufteilen. Nach dem Wechsel zurück zur Zuordnung "Zuletzt verwendet"werden 100 % dieses Umsatzes mit dem neuesten Einzelwert verknüpft. Dieser Zusammenhang kann zu falschen Schlussfolgerungen der Nutzer führen. </p> <p>Um Verwechslungsgefahr in Berichte zu vermeiden, macht Analytics die Verlaufsdaten für die Benutzeroberfläche nicht verfügbar. Sie kann angezeigt werden, wenn Sie die gegebene eVar wieder zur ursprünglichen Zuordnungseinstellung zurücksetzen möchten. Sie sollten jedoch die eVar-Zuordnungseinstellungen nicht ändern, um auf die Verlaufsdaten zuzugreifen. Adobe empfiehlt die Verwendung einer neuen eVar, wenn neue Zuordnungseinstellungen für bereits aufgezeichnete Daten gewünscht werden, anstatt die Zuordnungseinstellungen für eine eVar zu ändern, für die bereits eine erhebliche Menge historischer Daten erstellt wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Läuft ab nach</span> </p> </td> 
   <td colname="col2"> <p>Gibt einen Zeitraum oder ein Ereignis an, nach dem der eVar-Wert abläuft (d. h. keine Gutschrift mehr für Erfolgsereignisse mehr erhält). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. </p> <p>Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Wenn das Ereignis nicht eintritt, läuft die Variable nie ab. </p> <p>Die verfügbaren Ablaufoptionen lassen sich in vier Kategorien klassifizieren: </p> 
    <ul id="ul_810A37C9B6624F429F2FB45C18F7B43F"> 
     <li id="li_654D9D9044EC4E61AA7ABA372DBF8A93"><b>Auf Ansichten- oder Besuchsebene.</b> Umrechnungselemente, die über die Ansicht oder den Besuch hinausgehen, sind nicht mit der eVar verknüpft. </li> 
     <li id="li_689FBC8B4DAC41B3B0166E6586DD1990"><b>Basierend auf einem Zeitraum, z. B. Tag, Woche, Monat oder Jahr.</b> Konvertierungszeiträume überschreitende Ereignis werden nicht mit der eVar verknüpft. Der Ablaufzeitraum, der Beginn ist, wenn die Variable festgelegt wird. eVars laufen ab, je nachdem, wann sie festgelegt wurden, auf die zweite (Minute, Stunde, Tag, Monat usw.): 
      <ul id="ul_80C7E3182B6B4356B8A3CA920B81C6D5"> 
       <li id="li_F16F60319CCE406D9EDEFEC0A200BC4D">MINUTE = 60 Sekunden </li> 
       <li id="li_45F47F3F5691415B84052B235DF3BB54">STUNDE = 3600 Sekunden (60 Minuten) </li> 
       <li id="li_5288CE7D168E4C85B3D9BB67A44D32EC">TAG = 86.400 Sekunden (24 Stunden) </li> 
       <li id="li_60FC8BCD657745EE87B4E458CBA69583">WOCHE = 604800 Sekunden (7 Tage) </li> 
       <li id="li_7A05A66613C84F929F030310B9567CF5">MONAT = 2678400 Sekunden (31 Tage) </li> 
       <li id="li_DCD3CABF59E34D5999B03E606B08AD85">QUARTER = 8035200 Sekunden (93 Tage - 3 Monate mit 31 Tagen) </li> 
       <li id="li_54351D2899454D39A8BA205910D2CCB1">JAHR = 31536000 Sekunden (365 Tage) </li> 
      </ul> <p> </p> <p>Wenn ein Besuch am Montag um 7:00 Uhr und bei diesem Besuch um 7:15 Uhr eine eVar festgelegt wird, läuft dies wie folgt ab: </p> 
      <ul id="ul_72B311006BE6428698313D251C0940DB"> 
       <li id="li_50925D4A40AD4ACA88704A523138C5B9">Ablauf des Tages: eVar läuft am Dienstag um 7:15 Uhr ab. </li> 
       <li id="li_25846328766D4B4BAF407236C65C956C">Ablauf der Woche: eVar läuft am folgenden Montag um 7:15 Uhr ab. </li> 
       <li id="li_82DB2D7F53304623A5E1241D75C7DF94">Monatsablauf: eVar läuft 31 Tage ab Montag um 7:15 Uhr ab. </li> 
      </ul> </li> 
     <li id="li_C132C5C5A5344B91BDF5EB6A1C717C37"><b>Spezifische Ereignis zur Konversion.</b> Alle anderen Konvertierungs-Ereignis, die ausgelöst werden, nachdem das spezifische Ereignis, das mit der eVar verknüpft ist, ausgelöst wurde. </li> 
     <li id="li_5A782D743FB940649E6CB3E4BEA9B8B6"><b>Nie.</b> Solange das Cookie <span class="varname"> visitorID</span> intakt ist, kann ein beliebiger Zeitraum zwischen eVar und Ereignis verstreichen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Status</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Definiert den eVar-Status: </p> <p><b>Deaktiviert</b>:</span> Deaktiviert die eVar. Entfernt die eVar aus der Liste der Konversionsvariablen. </p> <p> <b>Keine untergeordneten Beziehungen</b>:</span> Verhindert, dass die eVar durch eine Subrelation unterteilt wird. </p> <p> <b>Grundlegende untergeordnete Beziehungen</b>: </span>Ermöglicht die Aufschlüsselung einer eVar anhand eines Berichts mit vollständigen Subrelationen (z. B. „Produkte“ oder „Kampagnen“). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Zurücksetzen</span> </p> </td> 
   <td colname="col2"> <p>Setzt alle vorhandenen Werte in der eVar zurück. </p> <p>Verwenden Sie diese Einstellung, wenn Sie eine eVar umwidmen, damit Sie einen alten Wert in einen neuen Bericht mischen. Beim Zurücksetzen werden historische Daten nicht gelöscht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Merchandising-Variablen können einer von zwei Syntaxen folgen: </p> <p> <b>Produktsyntax</b>:</span> Hiermit wird einem Produkt der eVar-Wert zugewiesen. Hinweis: Wenn die Produktsyntax ausgewählt ist, ist der Bereich „Merchandising-Binding-Ereignis“ deaktiviert und kann nicht für die Bearbeitung ausgewählt werden. Für diese Syntax können keine Binding-Ereignisse angewendet werden. </p> </p> <p> <b>Syntax der Konversionsvariablen</b>:</span> Hierbei wird einem Produkt nur dann die eVar zugewiesen, wenn ein Binding-Ereignis auftritt. In diesem Fall legen Sie fest, welche Ereignisse als Binding-Ereignisse gelten. </p> <p>Wenn Sie diese Einstellung ändern, ohne den JavaScript-Code zu aktualisieren, gehen Daten verloren. Siehe <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/var_merchandising.html">Merchandising-Variablen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising-Binding-Ereignis</span> </p> <p>(nur eVar) </p> </td> 
   <td colname="col2"> <p>Wenn „Merchandising“ auf <span class="uicontrol">Konversionsvariablensyntax</span> eingestellt ist, wird der aktuelle eVar-Wert durch die ausgewählten Ereignisse mit einem Produkt verbunden. </p> <p>Um ein Binding-Ereignis zu verwenden, setzen Sie <span class="uicontrol">„Zuordnung“ auf „Zuletzt verwendet“</span>. Wenn <span class="uicontrol">„Zuordnung“ auf „Ausgangswert“</span> eingestellt ist, bleibt die erste eVar-Produktverbindung erhalten, bis die eVar abläuft. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ablauf**

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Wenn Sie beispielsweise eine interne Promotion haben, die am Ende eines Besuchs abläuft, erhält die interne Promotion nur eine Gutschrift für Käufe oder Registrierungen, die während des Besuchs erfolgen, in dem sie aktiviert wurden.

Es gibt zwei Möglichkeiten, eine eVar ablaufen zu lassen:

* Sie können festlegen, dass die eVar nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können den Ablauf einer eVar erzwingen, indem Sie sie zurücksetzen. Dies ist nützlich, wenn Sie eine Variable erneut verwenden möchten.

Wenn Sie beispielsweise den Ablauf einer eVar von 30 auf 90 Tage ändern, bleiben die erfassten eVar-Werte für die Dauer des neuen Ablaufsatzes (in diesem Fall 90 Tage) erhalten. Das System prüft lediglich die aktuelle Ablaufeinstellung und den letzten festgelegten Zeitstempel des erfassten eVar-Werts, um den Ablauf zu bestimmen. Nur die **[!UICONTROL Reset]** Option läuft Werte ab und tut dies sofort.

Ein weiteres Beispiel: Wenn eine eVar im Mai zur Darstellung interner Promotions verwendet wird und nach 21 Tagen abläuft und im Juni zur Erfassung interner Suchbegriffe verwendet wird, sollten Sie am 1. Juni den Ablauf der Variablen erzwingen oder sie zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

**Groß-/Kleinschreibung**

Bei eVars wird zwischen Groß- und Kleinschreibung unterschieden, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Wenn beispielsweise die erste Instanz von eVar1 auf &quot;Angemeldet&quot;festgelegt ist, aber alle nachfolgenden Instanzen als &quot;angemeldet&quot;weitergeleitet werden, wird in Berichten immer &quot;Angemeldet&quot;als Wert der eVar angezeigt.

**Zähler**

Während eVars meist zum Speichern von Zeichenfolgenwerten verwendet werden, können sie auch so konfiguriert werden, dass sie als Zähler fungieren. eVars sind nützlich als Zähler, wenn Sie die Anzahl der Aktionen zählen möchten, die ein Benutzer vor einem Ereignis unternimmt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Bei jeder Suche eines Besuchers sollte die eVar den Wert &quot;+1&quot;enthalten. Wenn ein Besucher vier Mal vor einem Kauf sucht, wird eine Instanz für jede Gesamtanzahl angezeigt: 1.00, 2.00, 3.00 und 4.00. Jedoch wird nur der Wert 4.00 für das Ereignis purchase (Bestellungen und Umsatzmetriken) gutgeschrieben. Als Werte eines eVar-Zählers sind nur positive Zahlen zulässig.