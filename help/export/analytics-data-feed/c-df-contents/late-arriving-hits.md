---
title: Verspätete Treffer
description: Erfahren Sie, wie Datenfeeds verspätete Zugriffe behandeln.
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Verspätete Treffer

Historische Daten können nach Abschluss der Verarbeitung eines Datenfeed-Auftrags für eine bestimmte Stunde oder einen bestimmten Tag eingehen, z. B. durch Treffer mit Zeitstempel oder Datenquellen. Bei verspäteten Zugriffen handelt es sich um eine Einstellung zur Backend-Anpassung, die von Adobe bereitgestellt wird, um diese Daten in Datenfeeds einzubeziehen.

## Wie lange die Treffer noch nicht erreicht haben

Wenn ein Datenfeed normalerweise Daten verarbeitet, werden nur Daten innerhalb des Berichtsfensters (in der Regel die letzte Stunde oder der letzte Tag) betrachtet. Wenn Daten nach der Verarbeitung dieses Berichtsfensters durch einen Feed eingehen, werden diese Daten nie in einen Datenfeed aufgenommen.

Bei aktivierten Treffern mit verspäteter Eingabe ändert sich die Verarbeitungsmethode, um diese Daten einzuschließen. Jedes Mal, wenn ein Data Feed Daten verarbeitet, werden alle verspäteten Treffer geprüft, die eingetroffen sind, und diese in der nächsten an Ihre FTP-Site gesendeten Datenfeed-Datei stapelt.

## Aktivieren verspäteter Treffer

Verspätete Zugriffe können von Adobe für einzelne Datenfeeds manuell aktiviert werden. Berücksichtigen Sie zunächst Folgendes:

* Daten für verschiedene Tage werden häufig in Datenfeeds angezeigt, wenn Treffer mit verspäteter Eingabe aktiviert sind. Stellen Sie sicher, dass die Plattform, die Sie zum Erfassen von Datenfeeds verwenden, Daten aus verschiedenen Tagen in derselben Datei aufnehmen kann.
* Bei verspäteten Zugriffen verlängert sich die Verarbeitungszeit. In der Regel beträgt diese Verzögerung weniger als eine Stunde, kann aber mehrere Stunden betragen, wenn Ihre Report Suite eine große Anzahl verspäteter Treffer erhält. Adobe empfiehlt, diese Einstellung nicht zu aktivieren, wenn eine rechtzeitige Ankunft für Data Feeds für den Arbeitsablauf in Ihrem Unternehmen unbedingt erforderlich ist.
* Wenn eine Datenfeed-Datei erneut verarbeitet wird, werden die verspäteten Treffer, die in der Originaldatei enthalten waren, nicht in die erneut verarbeitete Datei aufgenommen.

Wenn Sie für einen vorhandenen wiederkehrenden Datenfeed verspätete Treffer aktivieren möchten, bitten Sie einen unterstützten Benutzer, sich an die Kundenunterstützung zu wenden und Folgendes einzuschließen:

* Hinweis, dass Sie für einen bestimmten Data Feed Treffer mit verspätetem Zugriff aktivieren möchten
* Report Suite-ID
* Data Feed-Name
