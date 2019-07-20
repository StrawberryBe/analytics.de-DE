---
description: Methoden zur Optimierung der ReportBuilder-Bereitstellung und eine Liste mit Fehlermeldungen, die möglicherweise auftreten könnten.
seo-description: Methoden zur Optimierung der ReportBuilder-Bereitstellung und eine Liste mit Fehlermeldungen, die möglicherweise auftreten könnten.
seo-title: Fehlerbehebung und Best Practices für Reportbuilder
solution: Analytics
title: Fehlerbehebung und Best Practices für Reportbuilder
topic: ReportBuilder
uuid: 36 a 08143-dc 78-40 f 5-9 ce 9-7 d 16980 aa 27 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Fehlerbehebung und Best Practices für Reportbuilder

Methoden zur Optimierung der ReportBuilder-Bereitstellung und eine Liste mit Fehlermeldungen, die möglicherweise auftreten könnten.

## Report Builder 5.0 users and opening 5.1 workbooks {#section_C29898775999453FABB5FB0E098415C8}

Adobe hat das Trennzeichen zwischen Dimensionen und Classifications von einem Unterstrich (_) in || geändert. Diese Änderung wirkt sich auf die Kompatibilität für Benutzer von ReportBuilder Version 5.0 aus, die eine ReportBuilder 5.1-Arbeitsmappe mit Classification-Anforderungen öffnen. Sobald eine Arbeitsmappe, die mit Version 5.1 oder älter erstellt wurde, geöffnet wird, werden alle serialisierten Classification-Anforderungen in dieses Format umgewandelt.

Dies bringt ein Kompatibilitätsproblem beim Weiterleiten mit sich: Sobald eine Arbeitsmappe, die in Version 5.1 konvertiert wurde, an einen Benutzer mit ReportBuilder Version 5.0 weitergegeben wird, kann dieser Benutzer die Classification-Anforderung nicht mehr erkennen (es wird nach „_“ gesucht, aber Version 5.1 hat „||“ serialisiert).

Außerdem führt das Öffnen einer ARB Version 5.1-Arbeitsmappe mit Classification-Anforderung zu folgender Nebenwirkung:

* Wenn Sie die Arbeitsmappe öffnen, erhalten Sie folgende Warnmeldung: „Diese Arbeitsmappe wurde zuletzt mit ReportBuilder Version 5.1 gespeichert. Diese Version hat einige Funktionen eingefügt, die mit der ReportBuilder-Version, die auf diesem Computer installiert ist, nicht kompatibel sind. Es wird dringend empfohlen, ein Upgrade auf die neueste Version von ReportBuilder durchzuführen, bevor diese Arbeitsmappe aktualisiert wird.“
* Wenn Sie einen Rechtsklick auf eine ARB-Anfrage mit Classification ausführen, werden die ReportBuilder-Kontextmenüs („Anforderung bearbeiten“, „Abhängige Anforderung hinzufügen“ ...) nicht angezeigt.
* Wenn Sie die Option „Alle aktualisieren“ ausführen, indem Sie auf die dritte Schaltfläche klicken oder indem Sie einen Satz Anforderungen aus dem Anforderungs-Manager aktualisieren, wird die Classification-Anforderung ohne Fehler ausgeführt. Die Classification-Werte werden jedoch nicht ausgeschrieben.
* Sie können die Anforderung weiterhin bearbeiten, indem Sie den Anforderungs-Manager öffnen und dann von Zeile zu Zeile navigieren, bis Sie bei der richtigen Anforderung angelangt sind.
* Wenn Sie die Anforderung bearbeiten, alle Parameter beibehalten und dann auf „Abschließen“ klicken, wird die Antwort ordnungsgemäß ausgeschrieben. Das Bearbeiten der Anforderung löst also das Problem, da die Antwortlayoutparameter neu serialisiert werden. Abhilfe ist also möglich, wenn auch zeitaufwendig.

## Authentication issues in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

Zur Erstellung von Datenanforderungen aus Report Suites durch ReportBuilder ist eine Authentifizierung erforderlich. Manchmal kann es bei der Anmeldung bei ReportBuilder abhängig von Ihren persönlichen Einstellungen in [!DNL Analytics] oder Ihrem Netzwerk zu Schwierigkeiten kommen.

**Firmen-Anmeldung ungültig**

Dieser Fehler tritt normalerweise auf, wenn bei der Anmeldung der Firmenname falsch eingegeben wird oder Probleme mit der Netzwerk-Aktivität bestehen. Gehen Sie folgendermaßen vor:

* Überprüfen Sie Ihre Eingabe auf Tippfehler oder überflüssige Leerzeichen.
* Melden Sie sich mit demselben Firmennamen bei Analytics an, um sicherzustellen, dass die Angaben korrekt sind. Wenn Sie sich mit diesen Benutzerdaten nicht anmelden können, wenden Sie sich an einen Administrator in Ihrem Unternehmen und fordern Sie die korrekten Daten an.

**Firewall**

ReportBuilder verwendet die Ports 80 und 443. Stellen Sie sicher, dass diese Ports von der Firewall in Ihrem Unternehmen freigegeben sind. Überprüfen Sie auch die interne IP-Adresse von Adobe auf weitere Firewall-Ausnahmen.

## Recommendations for optimizing requests {#section_33EF919255BF46CD97105D8ACB43573F}

Durch die folgenden Faktoren kann die Anfragekomplexität erhöht und damit die Verarbeitungsgeschwindigkeit verringert werden:

**Faktoren, die zu Lieferverzögerungen beitragen können**

* Es wurden zu viele Lesezeichen, Dashboards und ReportBuilder-Arbeitsmappen innerhalb weniger Stunden geplant.
* Es wurden zu viele ReportBuilder-Arbeitsmappen für die gleiche Uhrzeit geplant. In diesem Fall tritt für die Berichts-API-Warteschlange ein Rückstand ein.

**Faktoren, die zu Verzögerungen bei der Ausführung von Arbeitsmappen beitragen können**

* Deutliche Erhöhung der Classifications.
* Erweiterung des Anfragedatenbereichs im Laufe der Zeit.

   **Beispiel**: Angenommen, Sie haben eine Trendanforderung mit der Einstellung Aktuelles Jahr erstellt und diese mit der Granularität Tag aufgegliedert. Am Ende des Jahres werden mit der Anforderung mehr Zeiträume als der eine zu Beginn des Jahres erstellte Zeitraum zurückgegeben.

   `(January 1 - January 30 versus January 1 - December 31.)`

**Ursachen, die zu einem Arbeitsmappen-Bereitstellungsfehler beitragen**

Komplexe Excel-Formeln in einer Arbeitsmappe, insbesondere, wenn die Arbeitsmappe Datums- und Uhrzeitwerte enthält.

**Zellen, die 0 zurückgeben (keine Werte)**

Wenn im Namen des Excel-Arbeitsblatts ein Apostroph oder ein einfaches Anführungszeichen enthalten ist, wird ReportBuilder keine Werte zurückgeben. (Dies ist eine Microsoft Excel-Einschränkung.)

**Individuelle Anforderungsleistung**

Die Verarbeitungsgeschwindigkeit kann durch die folgenden Einstellungen beeinträchtigt werden:

| Einstellung | Schnellere Leistung | Langsamere Leistung |
|--- |--- |--- |
| Aufschlüsselung und Aufschlüsselungsreihenfolge | Wenig | Viele |
|  | Beispiel: Bei einer Aufteilung von A bis Z sollte die Anzahl der Elemente für A immer niedriger sein als die Anzahl der Elemente für Z. Andernfalls kann sich die Anforderungszeit deutlich erhöhen. |
| Datumsbereich | Kleiner Bereich | Großer Bereich |
| Filtern | Spezifische Filter | Am meisten bevorzugte Filter |
| Granularität | Aggregiert | Stündlich<ul><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Quartalsweise</li><li>Jährlich</li></ul> |
| Anzahl der Einträge | Kleiner Datensatz | Großer Datensatz |


**Zeitplanzeit**

Staffeln Sie die Zeitplanung über einen Zeitraum von 24 Stunden (siehe Tabelle unten). Durch vorhandene Lesezeichen, Dashboards und ReportBuilder-Arbeitsmappen, die zeitlich kurz aufeinander folgen, können Verzögerungen verursacht werden.

Planen Sie größere, komplexere Anforderungen in den frühen Morgenstunden, um manuelle Abrufe und Aktualisierungen im Laufe des Arbeitstages zuzulassen.

| Zeitplanung | 01:00 – 02:00 Uhr | 02:00 – 07:00 Uhr | 07:00 – 18:00 Uhr | 18:00 – 24:00 Uhr |
|--- |--- |--- |--- |--- |
| ReportBuilder – Nutzung | Ruhig | Hohe Auslastung | clientseitige Nutzung<br>Höhere Anzahl an Nutzern, die eine lokale Aktualisierung vornehmen und ein „Sofortiges Senden“ anfordern<br>Überprüfen Sie außerdem, ob die API-Warteschlange gelöscht wird, wenn bei geplanten Arbeitsmappen ein Timeout auftritt. | Geringe Auslastung |

**Timeouts**

Alle terminierten Berichte werden nach vier Stunden beendet. Das System versucht drei weitere Male eine Planung, die möglicherweise zu einem Fehler führen. (Im Allgemeinen gilt: Je größer der Datensatz, desto länger dauert die Ausführung.) Dies wird in der [!DNL Analytics]-Berichterstellung und ReportBuilder angezeigt:

* [!DNL Analytics]: **[!UICONTROL Favoriten]** &gt; **[!UICONTROL Geplante Berichte]**

* ReportBuilder: Klicken Sie auf der Registerkarte **[!UICONTROL Add-Ins]** in Excel auf [!UICONTROL Verwaltung].

## Error message descriptions {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Eine Liste der Fehlermeldungen, die gelegentlich bei der Verwendung von ReportBuilder auftreten können.

>[!NOTE]
>
>Dies ist nur eine Auswahl von Fehlermeldungen und keine umfassende Liste. Weitere Informationen zur Behebung von Fehlern erhalten Sie von Ihrem Administrator.

**Diese Funktion kann nur auf eine geöffnete Arbeitsmappe angewendet werden.**

Wenn in Excel keine Arbeitsmappen (Kalkulationstabellen) geöffnet sind und Sie auf eines der Symbole der ReportBuilder-Symbolleiste klicken, wird diese Meldung angezeigt. Darüber hinaus wird die Symbolleiste deaktiviert, bis Sie eine Arbeitsmappe öffnen. Sie können allerdings auf das Hilfesymbol klicken, solange die Symbolleiste noch aktiviert ist, ohne dass diese Fehlermeldung erfolgt.

**Sie müssen zunächst den[!UICONTROL Anforderungs-Assistenten]beenden, bevor Sie den[!UICONTROL Anforderungs-Manager aktivieren].**

Der [!UICONTROL Anforderungs-Assistent] und der [!UICONTROL Anforderungs-Manager] sind zwar funktional verbunden, aber es ist nicht möglich, den [!UICONTROL Anforderungs-Manager] zu verwenden, bevor Sie eine im [!UICONTROL Anforderungs-Assistenten] begonnene Arbeit abgebrochen oder abgeschlossen haben.

**Mit diesem Bereich ist keine Anforderung verbunden.**

Diese Fehlermeldung wird angezeigt, wenn Sie im [!UICONTROL Anforderungs-Manager] auf die Schaltfläche [!UICONTROL Aus Blatt] klicken, aber die entsprechende Zelle im Arbeitsblatt keine Anforderungen enthält.

Um zu prüfen, welche Zellen des Arbeitsblatts Anforderungen enthalten, klicken Sie auf die einzelnen Anforderungen in der Liste im [!UICONTROL Anforderungs-Manager]. Wenn eine Anforderung mit Zellen verknüpft ist, werden die Zellen bei Auswahl der Anforderung in der Liste markiert dargestellt.

**Der ausgewählte Bereich ist ungültig. Wählen Sie einen anderen Bereich aus.**

Diese Fehlermeldung wird angezeigt, wenn eine Zelle des Arbeitsblatts ausgewählt wird, der bereits eine Anforderung zugeordnet ist. Löschen Sie entweder die der Zelle zugeordnete Anforderung oder wählen Sie einen anderen Zellenbereich für die Verknüpfung aus.

Wenn Sie Zellen löschen möchten, müssen Sie unbedingt Zellen vorher ermitteln, welche Zellen Anforderungen enthalten und die Anforderung löschen, bevor Sie die Zellen löschen (indem Sie Zeilen oder Spalten entfernen).

**Verlassen Sie die Excel-Zelle, während diese ausgewählt ist, um diese Funktion zu verwenden.**

Wenn Sie sich im *Bearbeitungsmodus* in einer Excel-Zelle befinden und auf eines der ReportBuilder-Symbole klicken, wird diese Fehlermeldung angezeigt. Unter Bearbeitungsmodus für eine Excel-Zelle ist zu verstehen, dass die Zelle ausgewählt ist und der Cursor sich in der Zelle befindet. Sie befinden sich in Excel außerdem im Bearbeitungsmodus, wenn Sie Daten direkt in das [!UICONTROL Namensfeld] in der [!UICONTROL Formelleiste] eingeben.

**Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.**

Wenn Sie bereits eine Gruppe von Zellen mit dem Arbeitsblatt verknüpft haben, wird diese Fehlermeldung angezeigt.

Sie können vor dem Hinzufügen neuer Anforderungen ermitteln, welche Zellen Zuordnungen aufweisen, indem Sie den [!UICONTROL Anforderungs-Assistenten] schließen und den [!UICONTROL Anforderungs-Manager] öffnen. Wählen Sie dann nacheinander die Elemente in der Liste aus. Wenn Sie eine Anforderung in der Liste auswählen, werden die zugehörigen Zellen im Arbeitsblatt markiert dargestellt.

Aus diesem Grund sollten Sie unbedingt in Betracht ziehen, Zellen durch Formatierungen, Markierungen oder Zeilen- bzw. Spalteninformationen zu kennzeichnen, bevor Sie mehrere unterschiedliche Zellen mehreren unterschiedlichen Bereichen zuordnen.
