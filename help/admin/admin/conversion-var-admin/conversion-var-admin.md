---
description: Die benutzerspezifische Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Webseiten Ihrer Site in den Adobe-Code aufgenommen. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen dem Benutzer für einen bestimmten Zeitraum.
keywords: eVar
title: Konversionsvariablen (eVar)
feature: Admin Tools
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
source-git-commit: 2b5c7702d31d451ca4d42dc256c338567b17b8de
workflow-type: tm+mt
source-wordcount: '1579'
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
>Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [Listenvariablen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html?lang=de).

## Konversionsvariablen – Beschreibungen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschreibungen der Felder, die beim [Bearbeiten von Konversionsvariablen](/help/admin/admin/conversion-var-admin/t-conversion-variables-admin.md) verwendet werden.

| Element | Beschreibung |
| --- | --- |
| [!UICONTROL Name] | Der benutzerfreundliche Name der Konversionsvariablen. Dieser Name der eVar wird im allgemeinen Reporting und als Bericht-/Dimensionsname im Menü links genutzt. |
| [!UICONTROL Typ] (nur eVar) | Der Typ des Variablenwerts:<ul><li>**[!UICONTROL Textzeichenfolge]**: Erfasst die auf Ihrer Site verwendeten Textwerte. Dies ist der gängigste eVar-Typ und die Standardeinstellung. Diese eVar verhält sich ähnlich wie andere Variablen, bei denen der zugrundeliegende Wert eine statische Textzeichenfolge ist. Wenn Sie beispielsweise interne Kampagnen oder interne Suchkeywords nachverfolgen, ist dies die empfohlene Einstellung.</li><li>**[!UICONTROL Zähler]**: Zählt, wie oft eine Aktion stattfindet, bevor sie zum Erfolg führt. Wenn Sie z. B. eine eVar verwenden, um interne Suchvorgänge auf Ihrer Seite zu verfolgen, bewirkt die Werteinstellung auf [!UICONTROL Textzeichenfolge], dass Suchbegriffe verfolgt werden. Stellen Sie diesen Wert auf [!UICONTROL Zähler] ein, um die Zahl der durchgeführten Suchen unabhängig von den verwendeten Suchbegriffen zu zählen. Sie können z. B. eine Zähler-eVar nutzen, um die Anzahl der Male, die jemand vor Tätigen eines Kaufs Ihre interne Suche genutzt hat, zu zählen.</li></ul> |
| [!UICONTROL Zuordnung] | Legt fest, wie in Analytics Gutschriften für ein Erfolgsereignis zugewiesen werden, wenn eine Variable mehrere Werte vor dem Ereignis erhält. Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Zuletzt verwendet]**: Der letzte eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft.</li><li>**[!UICONTROL Ausgangswert]**: Der erste eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft.</li><li>**[!UICONTROL Linear]**: Weist Erfolgsereignisse gleichmäßig allen eVar-Werten zu. Da bei der linearen Zuweisung Werte nur innerhalb eines Besuchs genau verteilt werden, sollten Sie die lineare Zuweisung bei einem eVar-Ablauf von „Besuch“ verwenden.</li></ul> **Hinweis**: Beim Wechsel zu oder von linearen Werten wird unterbunden, dass historische Daten angezeigt werden. Das Mischen von Zuweisungstypen in der Berichterstellungsoberfläche kann zu falsch angegebenen Daten in Berichten führen. Bei einer linearen Zuweisung etwa könnte der Umsatz auf eine Reihe unterschiedlicher eVar-Werte aufgeschlüsselt werden. Nach dem Zurücksetzen auf die „Zuletzt“-Zuweisung würden 100 % des Umsatzes dem aktuellsten Einzelwert zugewiesen. Diese Zuweisung kann dazu führen, dass Benutzer die falschen Schlüsse ziehen.<br><br>Um die Wahrscheinlichkeit von Missverständnissen beim Reporting zu verringern, macht Adobe Analytics die historischen Daten für die Oberfläche nicht verfügbar. Wenn Sie sich entscheiden, die gegebene eVar wieder auf die ursprüngliche Zuweisungseinstellung zurückzusetzen, können diese angesehen werden – allerdings sollten Sie die eVar-Zuweisungseinstellungen nicht ändern, bloß um auf historische Daten zugreifen zu können. Adobe empfiehlt, eine neue eVar zu nutzen, wenn neue Zuweisungseinstellungen für bereits aufgezeichnete Daten gewünscht werden, statt die Zuweisungseinstellung einer eVar zu verändern, die bereits eine erhebliche Menge historischer Daten aufgebaut hat. |
| [!UICONTROL Läuft ab nach] | Hier wird ein Zeitraum bzw. ein Ereignis angegeben, nach dem der eVar-Wert abläuft (d. h. keine Gutschrift für Erfolgsereignisse mehr erhält). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ zugeschrieben.  Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Tritt das Ereignis nicht ein, läuft die Variable auch nicht ab.  Die verfügbaren Ablaufoptionen können in vier Hauptkategorien eingeteilt werden.<ul><li>**Auf Ebene einer Seitenansicht oder eines Besuchs.** Konversionsereignisse, die über die Seitenansicht oder Besuche hinausgehen, werden nicht mit eVar in Verbindung gebracht.</li><li>**Auf Grundlage eines Zeitraums, z. B. Tag, Woche, Monat oder Jahr.** Konversionsereignisse, die über den festgelegten Zeitraum hinausgehen, werden nicht mit eVar in Verbindung gebracht. Der Ablaufzeitraum beginnt mit der Einstellung der Variablen. eVars laufen, ausgehend von dem Zeitpunkt, zu dem sie festgelegt wurden, bei Erreichen der entsprechenden Sekunde (Minute, Stunde, Tag, Monat usw.) ab: <ul><li>MINUTE = 60 Sekunden</li><li>STUNDE = 3.600 Sekunden (60 Minuten)</li><li>TAG = 86.400 Sekunden (24 Stunden)</li><li>WOCHE = 604.800 Sekunden (7 Tage)</li><li>MONAT = 2.678.400 Sekunden (31 Tage)</li><li>QUARTAL = 8.035.200 Sekunden (93 Tage – 3 Monate mit 31 Tagen)</li><li>JAHR = 31.536.000 Sekunden (365 Tage)</li><br>Wenn ein Besuch am Montag um 7:00 Uhr beginnt und bei diesem Besuch um 7:15 Uhr eVar festgelegt wird, läuft diese wie folgt ab:<li>Ablauf nach einem Tag: eVar läuft am Dienstag um 7:15 Uhr ab.</li><li>Ablauf nach einer Woche: eVar läuft am folgenden Montag um 7:15 Uhr ab.</li><li>Ablauf nach einem Monat: eVar läuft 31 Tage nach diesem Montag um 7:15 Uhr ab.</li></ul><li>**Spezifische Konversionsereignisse.** Alle sonstigen Konversionsereignisse, die ausgelöst werden, nachdem das spezifische Ereignis, das eVar zugeordnet ist, eintritt.</li><li>**Nie.** Solange das Cookie  visitorID intakt ist, kann ein beliebiger Zeitraum zwischen eVar und Ereignis verstreichen.</li></ul> |
| [!UICONTROL Status] (nur eVar) | Hiermit wird der [!UICONTROL eVar]-Status definiert:<ul><li>**Deaktiviert**: Deaktiviert die [!UICONTROL eVar]. Entfernt die [!UICONTROL  eVar] aus der Liste der Konversionsvariablen.</li><li>**Keine untergeordneten Beziehungen**: Verhindert, dass die [!UICONTROL eVar] anhand einer Dimension unterteilt wird.</li><li>**Grundlegende untergeordnete Beziehungen**: Ermöglicht die Unterteilung einer eVar anhand einer vollständigen Dimension (z. B. „Produkte“ oder „Kampagnen“).</li></ul> |
| [!UICONTROL Zurücksetzen] | Hiermit werden alle Werte in der eVar zurückgesetzt. Mit dieser Einstellung können Sie verhindern, dass bei einer Neuverwendung einer eVar alte Werte in neuen Berichten verwendet werden. Durch das Zurücksetzen werden historische Daten nicht gelöscht. |
| [!UICONTROL Merchandising]  (nur eVar) | Merchandisingvariablen können einer oder zwei Syntaxen folgen:<ul><li>**[!UICONTROL Produktsyntax]**: Hiermit wird einem Produkt der eVar-Wert zugewiesen. **Hinweis**: Wenn die [!UICONTROL Produktsyntax] ausgewählt ist, ist der Bereich [!UICONTROL „Merchandising-Binding-Ereignis“] deaktiviert und kann nicht für die Bearbeitung ausgewählt werden. Für diese Syntax können keine [!UICONTROL Binding-Ereignisse] angewendet werden.</li><li>**[!UICONTROL Syntax der Konversionsvariablen]**: Hierbei wird einem Produkt nur dann die eVar zugewiesen, wenn ein [!UICONTROL Binding-Ereignis] auftritt. In diesem Fall legen Sie fest, welche Ereignisse als [!UICONTROL Binding-Ereignisse] gelten.  Wenn Sie diese Einstellung ändern, ohne den JavaScript-Code zu aktualisieren, gehen Daten verloren. Siehe [Merchandising-Variablen](/help/components/dimensions/evar-merchandising.md).</li></ul> |
| [!UICONTROL Merchandising-Binding-Ereignis] (nur eVar) | Wenn „Merchandising“ auf [!UICONTROL Konversionsvariablensyntax] eingestellt ist, wird der aktuelle eVar-Wert durch die ausgewählten Ereignisse mit einem Produkt verbunden. Um ein [!UICONTROL Binding-Ereignis] zu verwenden, setzen Sie [!UICONTROL Zuordnung] auf [!UICONTROL Zuletzt verwendet]. Wenn [!UICONTROL Zuordnung] auf [!UICONTROL Ausgangswert] eingestellt ist, bleibt die erste eVar-Produktverbindung erhalten, bis die eVar abläuft. Sie können mehrere Ereignisse auswählen, indem Sie die Strg-Taste (Windows) oder die Cmd-Taste (Mac) gedrückt halten und auf mehrere Elemente in der Liste klicken. Sie können nur dann ein Ereignis auswählen, wenn [!UICONTROL Konversionsvariablensyntax] ausgewählt ist. |

**Ablauf**

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Beispiel: Wenn Sie eine interne Werbeaktion haben, die am Ende eines Besuchs abläuft, werden für diese interne Werbeaktionen nur Einkäufe oder Registrierungen gezählt, die während des Besuchs erfolgten, in der sie aktiviert wurde.

Es gibt zwei Möglichkeiten für den Ablauf einer eVar:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können das Ablaufen einer eVar erzwingen, indem Sie sie zurücksetzen (z. B. wenn eine Variable für einen anderen Zweck eingesetzt werden soll).

Wenn Sie beispielsweise den Ablauf einer eVar von 30 auf 90 Tage ändern, bleiben die erfassten eVar-Werte für die Dauer des neu eingestellten Ablaufzeitraums (in diesem Fall 90 Tage) erhalten. Das System prüft lediglich die aktuelle Ablaufeinstellung und den letzten festgelegten Zeitstempel des erfassten eVar-Werts, um den Ablauf zu bestimmen. Nur die Option **[!UICONTROL Zurücksetzen]** bewirkt ein unmittelbares Ablaufen von Werten.

Ein weiteres Beispiel: Wenn eine eVar im Mai dazu dienen soll, interne Werbeaktionen widerzuspiegeln (wobei sie nach 21 Tagen ablaufen soll) und im Juni dann eingesetzt wird, um interne Keywords zu erfassen, müssen Sie am 1. Juni ihren Ablauf erzwingen oder die Variable zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

**Groß-/Kleinschreibung**

Bei eVars wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Groß- oder Kleinschreibung, die für das Reporting verwendet wird, basiert auf dem ersten Wert, den das Backend-System registriert. Dieser Wert kann entweder die erste jemals erkannte Instanz sein oder je nach Zeitraum (z. B. monatlich) variieren, je nach der Vielfalt und Menge der mit der Report Suite verknüpften Daten.

**Zähler**

Während eVars meist zur Speicherung von Zeichenfolgenwerten dienen, können sie auch so konfiguriert werden, dass sie als Zähler funktionieren. Als Zähler sind eVars dann nützlich, wenn Sie die Anzahl von Aktionen zählen möchten, die ein Benutzer vor einem Ereignis durchführt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Sobald ein Besucher eine Suche durchführt, wird der Wert der eVar um 1 erhöht. Wenn ein Besucher vier Suchen durchführt, bevor er einen Einkauf tätigt, wird Ihnen zu jeder Instanz eine Zählersumme angezeigt (1,00, 2,00, 3,00 und 4.00). Für das Kaufereignis wird jedoch nur die 4,00 gutgeschrieben (Bestellungen und Umsatz). Als Werte für eVar-Zähler sind nur positive Zahlen erlaubt.
