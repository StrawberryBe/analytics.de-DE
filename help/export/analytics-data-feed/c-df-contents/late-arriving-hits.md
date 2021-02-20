---
title: Verspätete Treffer
description: Erfahren Sie, wie Daten-Feeds verspätete Treffer handhaben.
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 100%

---


# Verspätete Treffer

Historische Daten können eingehen, nachdem die Verarbeitung eines Daten-Feed-Vorgangs für eine bestimmte Stunde oder einen bestimmten Tag beendet wurde, z. B. über Treffer mit Zeitstempeln oder Datenquellen. Bei verspäteten Treffern handelt es sich um eine Backend-Einstellung durch Adobe, damit diese Daten in Daten-Feeds einbezogen werden können.

## Funktionsweise verspäteter Treffer

Normalerweise werden bei der Datenverarbeitung eines Daten-Feeds nur Daten innerhalb des Berichtsfensters (in der Regel die letzte Stunde oder der letzte Tag) beachtet. Wenn Daten nach der Verarbeitung innerhalb dieses Berichtsfensters durch einen Feed eingehen, werden diese Daten in keinen Daten-Feed mehr aufgenommen.

Sind aber verspätete Treffer aktiviert, wird die Verarbeitungsmethode so geändert, dass diese Daten einbezogen werden. Jedes Mal, wenn ein Daten-Feed Daten verarbeitet, werden alle verspäteten Treffer geprüft und in die nächste an Ihre FTP-Site gesendete Daten-Feed-Datei eingefügt.

## Aktivieren verspäteter Treffer

Verspätete Treffer können von Adobe für einzelne Daten-Feeds manuell aktiviert werden. Achten Sie dabei auf Folgendes:

* Daten für verschiedene Tage werden häufig dann in Daten-Feeds angezeigt, wenn verspätete Treffer aktiviert sind. Stellen Sie sicher, dass die Plattform, die Sie zum Erfassen von Daten-Feeds verwenden, Daten aus verschiedenen Tagen in derselben Datei aufnehmen kann.
* Bei verspäteten Treffern verlängert sich die Verarbeitungszeit. In der Regel beträgt diese Verzögerung weniger als eine Stunde, kann aber mehrere Stunden betragen, wenn Ihre Report Suite eine große Anzahl verspäteter Treffer erhält. Adobe empfiehlt, diese Einstellung nicht zu aktivieren, wenn der zeitgerechte Empfang von Daten-Feeds für den Arbeitsablauf in Ihrem Unternehmen wichtig ist.
* Wenn eine Daten-Feed-Datei erneut verarbeitet wird, sind die verspäteten Treffer, die in der Originaldatei enthalten waren, nicht Teil der erneut verarbeiteten Datei.

Wenn Sie für einen vorhandenen wiederkehrenden Daten-Feed verspätete Treffer aktivieren möchten, bitten Sie einen unterstützten Benutzer, sich an die Kundenunterstützung zu wenden und folgende Angaben zu machen:

* Eine Mitteilung, dass Sie für einen bestimmten Daten-Feed verspätete Treffer aktivieren möchten
* Die Report Suite-ID
* Den Namen des Daten-Feeds
