---
description: Auf der Seite Rechnungsstellung können Sie auf die Rechnungsinfomationen zugreifen, einschließlich der Traffic-Details der einzelnen Report Suites. Nur autorisierte Administratoren haben Zugriff auf diese Seite.
solution: Analytics
title: Rechnungsstellung
topic: Admin tools
uuid: ad6ee1c4-d317-4320-a36e-ee966c8f145e
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Rechnungsstellung

Auf der Seite Rechnungsstellung können Sie auf die Rechnungsinfomationen zugreifen, einschließlich der Traffic-Details der einzelnen Report Suites. Nur autorisierte Administratoren haben Zugriff auf diese Seite.

> [!NOTE] Wenn der Zugriff auf die Registerkarte "Rechnungsstellung"für Ihr Unternehmen deaktiviert ist, wenden Sie sich an Ihren Kundenbetreuer.

Mit Hilfe der Übersichtsdaten zum Traffic auf der Seite „Rechnungsstellung“ können Sie die Seitenansichtsdaten aus Berichten mit den abrechnungsfähigen Server-Aufrufen aus der Rechnung in Verbindung setzen. Auf der Seite [!UICONTROL Rechnungsstellung] haben Sie folgende Möglichkeiten:

* Prüfen der Rechnung
* Aufschlüsseln der Kosten pro Report Suite für interne Buchungszuweisungen
* Anzeigen der Verteilung primärer und sekundärer Server-Aufrufe

Auf der Seite [!UICONTROL Rechnungsstellung] werden die Informationen monatsweise aufgeführt.

Wenn Sie die Übersichtsdaten zum monatlichen Traffic-Daten anzeigen möchten, klicken Sie auf den Monat, für den die Daten angezeigt werden sollen, auf **[!UICONTROL Ansicht]**.

Der [!UICONTROL Monatsrechnungs]-Bericht enthält die folgenden Informationen:

| Spalte | Beschreibung |
|--- |--- |
| Report Suite | Die bei der Datenerfassung verwendete Report Suite. |
| Position | Das Rechencenter, das die Report Suite-Daten speichert: San Jose (Kalifornien), Dallas (Texas), Pacific Northwest (US), London (UK) oder Singapur. In den meisten Fällen sind sämtliche Report Suites eines Unternehmens im gleichen Rechenzentrum untergebracht. |
| Primäre Server-Aufrufe | Anforderungen, die direkt von den Browsern der Website-Besucher oder von der Dateneinfüge-API empfangen werden. Umfasst Primärtreffer (Seitenansichten), primäre benutzerspezifische Ereignisse, primäre Download-Ereignisse sowie primäre Ausstiegsereignisse. |
| Sekundäre Server-Aufrufe | Kopien der primären Server-Aufrufe, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden.  Falls ein sekundärer Serveraufruf mittels VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, wird der Transfer mit einer negativen Zahl auf der Seite „Rechnungsstellung“ aufgeführt. In diesem Fall werden die angesammelten sekundären Aufrufe von den primären Server-Aufrufen abgezogen. |
| Server-Aufrufe insgesamt | Die Gesamtanzahl an primären und sekundären Server-Aufrufen für diese Report Suite an einem vorgegebenen Standort. |
| Seitenansichten | Die Gesamtanzahl an Seitenansichten für die einzelnen Report Suites. Die Seitenansichts-Werte können unter Site-Metriken &gt; Seitenansichten bestätigt werden. |
| Downloads | Die Download-Summen für die einzelnen Report Suites. Die Download-Werte können unter Site-Content &gt; Links &gt; Datei-Downloads bestätigt werden. |
| Benutzerspezifische Links | Die Summen der benutzerspezifischen Links für die einzelnen Report Suites. Die Werte für benutzerspezifische Links können unter Site-Content &gt; Links &gt; Benutzerspezifische Links bestätigt werden. |
| Exitlinks | Die Summen der Exitlinks für die einzelnen Report Suites. Die Werte für Exitlinks können unter Site-Content &gt; Links &gt; Exitlinks bestätigt werden. |

> [!NOTE] Um eine Arbeitskopie des Berichts " [!UICONTROL Monatliche Rechnung] "zu erhalten, kopieren Sie ihn in die Zwischenablage und fügen Sie ihn dann in ein Tabellenkalkulationsprogramm wie Microsoft Excel* ein.

## Berichtsdatum vs. Verarbeitungsdatum {#section_51A48C2F223F4904BE1407C13333C457}

In der Reporting-Benutzerschnittstelle werden die präsentierten Daten immer dem **Berichtsdatum** zugeordnet, das dem Zeitstempel entspricht, der dem Ereignis zugeordnet wurde.

Nutzung/Abrechnung verwendet hingegen immer das **Verarbeitungsdatum** bzw. den Zeitpunkt, zu dem die Daten tatsächlich im System verarbeitet wurden. Wegen grundlegender Wartezeiten, Datenimporten oder Zeitzonenunterschieden bei der Ereigniszeit (die Verarbeitung erfolgt immer in Pazifischer Zeit), entsprechen Berichts- und Verarbeitungsdatum einander in der Regel nicht vollständig.
