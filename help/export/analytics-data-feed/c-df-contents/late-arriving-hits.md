---
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042
translation-type: tm+mt

---
# Verspätete Treffer mit Treffern

Historische Daten können eingehen, nachdem ein Datenfeed-Auftrag für eine bestimmte Stunde oder einen bestimmten Tag verarbeitet wurde, z. B. durch Treffer mit Zeitstempel oder Datenquellen. Verspätete Treffer sind eine Backend-Anpassung, die von Adobe bereitgestellt wird, um diese Daten in Datenfeeds einzubinden.

## Funktionsweise der verspäteten Treffer

Wenn ein Datenfeed normalerweise Daten verarbeitet, wird er nur Daten innerhalb des Berichtsfensters (gewöhnlich die letzte Stunde oder Tag) betrachtet. Wenn Daten eingehen, nachdem ein Feed die Verarbeitung des Berichtsfensters abgeschlossen hat, werden diese Daten in keinem Datenfeed enthalten.

Wenn verspätete Treffer aktiviert sind, ändert sich die Verarbeitungsmethode, um diese Daten aufzunehmen. Jedes Mal, wenn ein Datenfeed Daten verarbeitet, werden alle verspäteten Treffer betrachtet, die eingetroffen sind und in der nächsten Datenfeed-Datei, die an Ihre FTP-Site gesendet wird, gefüllt sind.

## Aktivieren von spät eintreffenden Treffern

Verspätete Treffer können von Adobe für einzelne Datenfeeds manuell aktiviert werden. Beachten Sie zuvor Folgendes:

* Daten für verschiedene Tage werden häufig in Datenfeeds angezeigt, wenn verspätete Treffer aktiviert sind. Stellen Sie sicher, dass die Plattform, die Sie zum Erfassen von Datenfeeds verwenden, Daten aus unterschiedlichen Tagen derselben Datei aufnehmen kann.
* Verspätete Treffer erhöhen die Verarbeitungszeit. Normalerweise liegt diese Verzögerung unter der Stunde, kann aber mehrere Stunden oder mehr betragen, wenn Ihre Report Suite eine große Anzahl verspäteter Treffer erhält. Adobe empfiehlt, diese Einstellung zu aktivieren, wenn die rechtzeitige Ankunft von Datenfeeds für den Arbeitsablauf Ihres Unternehmens unabdingbar ist.
* Wenn eine Datenfeed-Datei erneut verarbeitet wird, sind die verspäteten Treffer, die in der Originaldatei enthalten waren, nicht in der erneut verarbeiteten Datei enthalten.

Wenn Sie verspätet eintreffende Treffer für einen vorhandenen wiederkehrenden Datenfeed aktivieren möchten, bitten Sie einen unterstützten Benutzer, sich an den Kundendienst zu wenden und Folgendes zu berücksichtigen:

* Hinweis, dass Sie verspätet eintreffende Treffer für einen bestimmten Datenfeed aktivieren möchten
* Report Suite-ID
* Datenfeed-Name
