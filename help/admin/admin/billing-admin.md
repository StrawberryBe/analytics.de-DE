---
description: Auf der Seite "Rechnungsstellung"können Sie auf die Rechnungsinformationen zugreifen, einschließlich der Traffic-Details zu den einzelnen Report Suites. Nur autorisierte Administratoren haben Zugriff auf diese Seite.
title: Rechnungsstellung
topic: Admin tools
uuid: ad6ee1c4-d317-4320-a36e-ee966c8f145e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Rechnungsstellung

Auf der Seite &quot;Rechnungsstellung&quot;können Sie auf die Rechnungsinformationen zugreifen, einschließlich der Traffic-Details zu den einzelnen Report Suites. Nur autorisierte Administratoren haben Zugriff auf diese Seite.

>[!NOTE] Wenden Sie sich an Ihren Kundenbetreuer, wenn für Ihr Unternehmen der Zugriff auf die Registerkarte „Abrechnung“ deaktiviert ist.

Mit den Traffic-Übersichtsdaten auf der Seite &quot;Rechnungsstellung&quot;können Sie Seitendaten in Berichten mit abrechnungsfähigen Serveraufrufen auf Ihrer Rechnung korrelieren. Auf der [!UICONTROL Billing] Seite haben Sie folgende Möglichkeiten:

* Prüfen Sie Ihre Rechnung.
* Aufschlüsseln der Kosten nach Report Suite für interne Buchungszuweisungen
* Ansicht der Verteilung von primären und sekundären Serveraufrufen.

Die [!UICONTROL Billing] Seite organisiert die Informationen nach Monaten.

To view monthly traffic overview data, locate the month where you want to view traffic data, then click **[!UICONTROL View]**.

Der resultierende [!UICONTROL Monthly Invoice] Bericht enthält folgende Informationen:

| Spalte | Beschreibung |
|--- |--- |
| Report Suite | Die bei der Datenerfassung verwendete Report Suite. |
| Standort | Das Rechenzentrum, in dem die Report Suite-Daten gespeichert werden: San Jose (Kalifornien), Dallas (Texas), Pacific Northwest (USA), London (UK) oder Singapur. In den meisten Fällen befinden sich alle Report Suites der Firma im gleichen Rechenzentrum. |
| Primäre Server-Aufrufe | Anfragen, die direkt von den Browsern des Website-Besuchers oder der Dateneinfüge-API empfangen wurden. Umfasst primäre Treffer (Seitenaufrufe), primäre benutzerspezifische Ereignis, Primär-Download-Ereignis und primäre Ausstiegs-Ereignis. |
| Sekundäre Server-Aufrufe | Kopien der primären Server-Aufrufe, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden.  Falls ein sekundärer Serveraufruf mittels VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, wird der Transfer mit einer negativen Zahl auf der Seite für die Rechnungsstellung aufgeführt. In diesem Fall werden die angesammelten sekundären Aufrufe von den primären Server-Aufrufen abgezogen. |
| Server-Aufrufe insgesamt | Die Gesamtanzahl an primären und sekundären Server-Aufrufen für diese Report Suite an einem vorgegebenen Standort. |
| Seitenansichten | Die Gesamtanzahl an Seitenansichten für die einzelnen Report Suites. Die Seitenansichtswerte können unter „Site-Metriken > Seitenansichten“ bestätigt werden. |
| Downloads | Die Download-Summen für die einzelnen Report Suites. Die Download-Werte können unter „Site-Content > Links > Datei-Downloads“ bestätigt werden. |
| Benutzerdefinierte Links | Die Summen der benutzerdefinierten Links für die einzelnen Report Suites. Die Werte für benutzerdefinierte Links können unter „Site-Content > Links > benutzerdefinierte Links“ bestätigt werden. |
| Exitlinks | Die Summen der Exitlinks für die einzelnen Report Suites. Die Werte für Exitlinks können unter „Site-Content > Links > Exitlinks“ bestätigt werden. |

>[!NOTE] Um eine Arbeitskopie des [!UICONTROL Monthly Invoice] Berichts zu erhalten, kopieren Sie ihn in die Zwischenablage und fügen Sie ihn dann in ein Tabellenkalkulationsprogramm wie Microsoft Excel* ein.

## Berichtsdatum vs. Verarbeitungsdatum {#section_51A48C2F223F4904BE1407C13333C457}

In der Benutzeroberfläche des Berichte werden die angezeigten Daten immer an das Datum des **Berichte** angehängt, das dem Zeitstempel entspricht, der dem Ereignis zugeordnet ist.

Nutzung/Rechnungsstellung hingegen verwendet immer das **Verarbeitungsdatum**, oder wenn die Daten tatsächlich im System verarbeitet wurden. Aufgrund der grundlegenden Latenz, der Datenimporte oder der Zeitzonenunterschiede zwischen Ereignissen (alles wird in Pacific Time verarbeitet) stimmen Berichte- und Verarbeitungsdatum in der Regel nicht vollständig überein.
