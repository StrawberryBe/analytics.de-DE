---
description: Methoden zur Optimierung der Report Builder-Bereitstellung und eine Liste mit Fehlermeldungen, die auftreten könnten.
title: Fehlerbehebung und Best Practices für Report Builder
topic: Report builder
uuid: 36a08143-dc78-40f5-9ce9-7d16980aa27b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Fehlerbehebung und Best Practices für Report Builder

Methoden zur Optimierung der Report Builder-Bereitstellung und eine Liste mit Fehlermeldungen, die auftreten könnten.

## Benutzer von Report Builder 5.0 und Öffnen von 5.1-Arbeitsmappen {#section_C29898775999453FABB5FB0E098415C8}

Adobe hat das Trennzeichen zwischen Dimensionen und Classifications von einem Unterstrich (_) in||. Diese Änderung wirkt sich auf die Kompatibilität für Benutzer von Report Builder Version 5.0 aus, die eine Report Builder 5.1-Arbeitsmappe mit Classification-Anforderungen öffnen. Jedes Mal, wenn eine Arbeitsmappe aus einer älteren Version als v5.1 geöffnet wird, werden alle serialisierten Classification-Anforderungen in dieses Format konvertiert.

Dies bringt ein Kompatibilitätsproblem beim Weiterleiten mit sich: Sobald eine Arbeitsmappe, die in Version 5.1 konvertiert wurde, an einen Benutzer mit Report Builder Version 5.0 weitergegeben wird, kann dieser Benutzer die Classification-Anforderung nicht mehr erkennen (es wird nach „_“ gesucht, aber Version 5.1 hat „||“ serialisiert).

Außerdem bewirkt das Öffnen einer ARB Version 5.1-Arbeitsmappe mit Classification-Anforderung Folgendes:

* Wenn Sie die Arbeitsmappe öffnen, erhalten Sie folgende Warnmeldung: „Diese Arbeitsmappe wurde zuletzt mit Report Builder Version 5.1 gespeichert. Diese Version hat einige Funktionen eingefügt, die mit der Report Builder-Version, die auf diesem Computer installiert ist, nicht kompatibel sind. Es wird dringend empfohlen, ein Upgrade auf die neueste Version von Report Builder durchzuführen, bevor diese Arbeitsmappe aktualisiert wird.“
* Wenn Sie einen Rechtsklick auf eine ARB-Anfrage mit Classification ausführen, werden die Report Builder-Kontextmenüs („Anforderung bearbeiten“, „Abhängige Anforderung hinzufügen“ ...) nicht angezeigt.
* Wenn Sie eine Aktualisierung für alle durchführen, indem Sie auf die dritte Schaltfläche klicken oder indem Sie eine Reihe von Anforderungen aus dem Anforderungs-Manager aktualisieren, wird die Classification-Anforderung fehlerfrei ausgeführt. Die Classification-Werte werden jedoch nicht ausgeschrieben.
* Sie können die Anforderung weiterhin bearbeiten, indem Sie den Anforderungs-Manager öffnen und dann von Zeile zu Zeile wechseln, bis die richtige Anforderung erreicht ist.
* Wenn Sie die Anforderung bearbeiten und alle Parameter unverändert lassen und dann auf &quot;Fertig stellen&quot;klicken, wird die Antwort ordnungsgemäß ausgeschrieben. Das Bearbeiten der Anforderung löst das Problem, da die Parameter des Antwortlayouts neu serialisiert werden. Es gibt also eine Lösung, obwohl sie zeitaufwendig ist.

## Authentifizierungsprobleme in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

Zur Erstellung von Datenanforderungen aus Report Suites durch Report Builder ist eine Authentifizierung erforderlich. Manchmal kann es bei der Anmeldung bei Report Builder abhängig von Ihren persönlichen Einstellungen in [!DNL Analytics] oder Ihrem Netzwerk zu Problemen kommen.

**Firmen-Anmeldung ungültig**

Dieser Fehler tritt am häufigsten auf, wenn entweder die Firma für die Anmeldung falsch eingegeben wurde oder Probleme mit der Aktivität des Netzwerks aufgetreten sind. Führen Sie folgende Schritte aus:

* Überprüfen Sie die Rechtschreibung der Firma für die Anmeldung, um sicherzustellen, dass kein Tippfehler oder ein fehlerhafter Leerzeichen vorhanden ist.
* Melden Sie sich mit demselben Firmennamen bei Analytics an, um sicherzustellen, dass die Angaben korrekt sind. Wenn Sie sich mit diesen Benutzerdaten nicht anmelden können, wenden Sie sich an einen Administrator in Ihrem Unternehmen und fordern Sie die korrekten Daten an.

**Firewall**

Report Builder verwendet die Ports 80 und 443. Stellen Sie sicher, dass diese Anschlüsse über die Firewall Ihres Unternehmens zulässig sind. Weitere Firewall-Ausnahmen finden Sie unter Interne IP-Adressen von Adobe.

## Recommendations zur Anforderungsoptimierung {#section_33EF919255BF46CD97105D8ACB43573F}

Durch die folgenden Faktoren kann die Anfragekomplexität erhöht und damit die Verarbeitungsgeschwindigkeit verringert werden:

**Mögliche Gründe für Bereitstellungsverzögerungen**

* Es wurden zu viele Lesezeichen, Dashboards und Report Builder-Arbeitsmappen innerhalb weniger Stunden geplant.
* Es wurden zu viele Report Builder-Arbeitsmappen für die gleiche Uhrzeit geplant. In diesem Fall tritt in der Berichts-API-Warteschlange ein Rückstand ein.

**Mögliche Gründe für Verzögerungen bei der Ausführung von Arbeitsmappen**

* Deutliche Zunahme der Klassifizierungen.
* Erhöhen des Anforderungsdatumsbereichs im Zeitverlauf.

   **Beispiel**: Angenommen, Sie haben eine Trendanforderung mit der Einstellung „Aktuelles Jahr“ erstellt und diese mit der Granularität „Tag“ aufgegliedert. Am Ende des Jahres werden mit der Anforderung mehr Zeiträume als der eine zu Beginn des Jahres erstellte Zeitraum zurückgegeben.

   `(January 1 - January 30 versus January 1 - December 31.)`

**Mögliche Gründe für einen Arbeitsmappen-Bereitstellungsfehler**

Komplexe Excel-Formeln in einer Arbeitsmappe, insbesondere wenn die Arbeitsmappe Datums- und Uhrzeitwerte enthält.

**Zellen, die 0 zurückgeben (keine Werte)**

Ein Apostroph oder ein einfaches Anführungszeichen im Excel-Blattnamen führt dazu, dass ReportBuilder keine Werte zurückgibt. (Dies ist eine Microsoft Excel-Beschränkung.)

**Individuelle Anforderungsleistung**

Die Verarbeitungsgeschwindigkeit kann durch die folgenden Einstellungen beeinflusst werden:

| Einstellung | Schnellere Leistung | Langsamere Leistung |
|--- |--- |--- |
| Aufschlüsselungen und Aufschlüsselungsreihenfolge | Wenig | many |
|  | Beispiel: Bei einer Aufteilung von A bis Z sollte die Anzahl der Elemente für A immer niedriger sein als die Anzahl der Elemente für Z. Andernfalls kann sich die Anforderungszeit deutlich erhöhen. |
| Datumsbereich | Kleiner Bereich | Breiter Bereich |
| Filtern | Spezifische Filter | Bevorzugte Filterung |
| Granularität | Aggregiert | Stündlich<ul><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Quartalsweise</li><li>Jährlich</li></ul> |
| Anzahl der Einträge | Kleiner Datensatz | Großer Datensatz |


**Zeitplanung**

Staffeln Sie die Zeitplanung über einen Zeitraum von 24 Stunden (siehe Tabelle unten). Durch vorhandene Lesezeichen, Dashboards und Report Builder-Arbeitsmappen, die zeitlich kurz aufeinander folgen, können Verzögerungen verursacht werden.

Planen Sie größere, komplexere Anforderungen am frühen Morgen, um manuelle Abrufe und Aktualisierungen während des Geschäftstages zu ermöglichen.

| Planungszeit | 01:00 Uhr - 2.00 Uhr | 2.00 Uhr - 07.00 Uhr | 07:00 Uhr - 18.00 Uhr | 18.00 Uhr - Mitternacht |
|--- |--- |--- |--- |--- |
| Report Builder – Nutzung | Ruhe | Sehr beschäftigt | clientseitige Nutzung.<br>Höhere Anzahl an Nutzern, die eine lokale Aktualisierung vornehmen und ein „Sofortiges Senden“ anfordern.<br>Überprüfen Sie außerdem, ob die API-Warteschlange gelöscht wird, wenn bei geplanten Arbeitsmappen ein Timeout auftritt. | Nicht besetzt |

**Timeouts**

Ein terminierter Bericht wird nach vier Stunden beendet. Das System versucht dreimal zu planen, was möglicherweise zu einem Fehler führt. (Im Allgemeinen gilt: Je größer der Datensatz, desto länger dauert die Ausführung.) Dies wird in der [!DNL Analytics]-Berichterstellung und in Report Builder angezeigt:

* [!DNL Analytics]: **[!UICONTROL Favorites]** > **[!UICONTROL Scheduled Reports]**

* Report Builder: Click **[!UICONTROL Management]** in the [!UICONTROL Add-ins] tab in Excel.

## Beschreibung der Fehlermeldungen {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Eine Liste der Fehlermeldungen, die gelegentlich bei der Verwendung von Report Builder auftreten können.

>[!NOTE] Dies ist nur eine Auswahl der Fehlermeldungen, keine umfassende Auflistung. Weitere Informationen zur Behebung von Fehlern erhalten Sie von Ihrem Administrator.

**Diese Funktion kann nur auf eine geöffnete Arbeitsmappe angewendet werden.**

Wenn in Excel keine Arbeitsmappen (Kalkulationstabellen) geöffnet sind und Sie auf eines der Symbole in der ReportBuilder-Symbolleiste klicken, wird diese Meldung angezeigt. Darüber hinaus wird die Symbolleiste deaktiviert, bis Sie eine Arbeitsmappe öffnen. Sie können jedoch auf das Symbol für die Online-Hilfe klicken, während die Symbolleiste weiterhin aktiviert ist, ohne dass dieser Fehler verursacht wird.

**Sie müssen zuerst die Anwendung beenden,[!UICONTROL Request Wizard]bevor Sie die[!UICONTROL Request Manager]aktivieren.**

Während die [!UICONTROL Request Manager] und die [!UICONTROL Request Wizard] sind funktional verknüpft, ist es nicht möglich, mit dem Beginn zu arbeiten, [!UICONTROL Request Manager] bevor in der [!UICONTROL Request Wizard].

**Mit diesem Bereich ist keine Anforderung verbunden.**

Diese Fehlermeldung wird angezeigt, wenn Sie auf die [!UICONTROL From Sheet] Schaltfläche im Feld klicken, [!UICONTROL Request Manager] wenn eine Zelle des Arbeitsblatts keine Anforderungen enthält.

Um zu ermitteln, welche Zellen im Arbeitsblatt Anforderungen enthalten, klicken Sie auf die einzelnen Anforderungen in der Tabelle [!UICONTROL Request Manager]. Wenn eine Anforderung mit Zellen verknüpft ist, werden die Zellen hervorgehoben angezeigt, wenn die Anforderung in der Tabelle ausgewählt ist.

**Der ausgewählte Bereich ist ungültig. Wählen Sie einen anderen Bereich aus.**

Wenn eine Zelle des Arbeitsblatts ausgewählt ist und ihr bereits eine Anforderung zugeordnet ist, tritt dieser Fehler auf. Löschen Sie entweder die den Zellen zugeordnete Anforderung oder wählen Sie einen anderen Zellenbereich für die Zuordnung aus.

Wenn Sie Zellen löschen möchten, müssen Sie die Zellen, die Anforderungen enthalten, suchen und die Anforderung löschen, bevor Sie die Zellen löschen (Zeilen oder Spalten entfernen).

**Verlassen Sie die Excel-Zelle, während diese ausgewählt ist, um diese Funktion zu verwenden.**

Wenn Sie sich im *Bearbeitungsmodus* in einer Excel-Zelle befinden und auf eines der Report Builder-Symbole klicken, wird diese Fehlermeldung angezeigt. Unter Bearbeitungsmodus für eine Excel-Zelle ist zu verstehen, dass die Zelle ausgewählt ist und der Cursor sich in der Zelle befindet. Sie befinden sich auch im Bearbeitungsmodus in einer Excel-Zelle, wenn Sie direkt in die [!UICONTROL Formula] Leiste oder in den [!UICONTROL Name Box] oberen Bereich von Excel eingeben.

**Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.**

Wenn Sie dem Arbeitsblatt bereits eine Reihe von Zellen zugeordnet haben, wird dieser Fehler angezeigt.

Eine Möglichkeit, vor dem Hinzufügen neuer Anforderungen zu bestimmen, welche Zellen zugeordnet werden, besteht darin, die Zellen zu schließen [!UICONTROL Request Wizard] und zu öffnen [!UICONTROL Request Manager]. Wählen Sie dann nacheinander die Elemente in der Liste aus. Wenn Sie eine Anforderung in der Liste auswählen, werden die entsprechenden Zellen, die Anforderungszuordnungen im Arbeitsblatt enthalten, hervorgehoben.

Dies ist ein Grund, warum Sie erwägen sollten, Zellen mit Markierung, Zeilen- oder Spalteninformationen oder einem Formatierungsstil zu kennzeichnen, bevor Sie mehrere Zellen mehreren Bereichen zuordnen.
