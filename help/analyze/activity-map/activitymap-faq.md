---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.
title: Activity Map – Häufig gestellte Fragen
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
source-git-commit: a283ba5d5678498cde9d0065a4f9f6b8a98558dd
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 77%

---

# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.

## Haben alle Analytics-Kunden Zugriff auf die Seite „Activity Map – Aktivierung“ in den Admin Tools?

Organisationen mit Verträgen für Adobe Analytics Standard, Premium und Ultimate haben Zugang zu Activity Map.

## Wie unterstützt Activity Map Einzelseiten-Apps (SPA)?

Alle paar Sekunden scannt Activity Map die Webseite und sucht nach Änderungen an der Seite. ActivityMap findet neuen Inhalt auf der Seite, ohne dass eine neue Seite geladen werden muss. Dieser neue Inhalt wird jedoch immer dem ersten pageName zugeordnet, der beim Laden der Seite gefunden wurde.

* Activity Map prüft, ob sich die Sichtbarkeit von Links, von denen es weiß, geändert hat. Wenn eine Änderung der Sichtbarkeit festgestellt wird, wird die Spalte &quot;Links auf Seite&quot;der Tabelle &quot;Präsenz&quot;für diesen Link mit [!UICONTROL Angezeigt] oder [!UICONTROL Ausgeblendet] aktualisiert.

* Wenn durch die Benutzerinteraktion neue Inhalte erstellt werden, werden alle neuen Elemente, die von AppMeasurement als Link erkannt werden, zur Tabelle [!UICONTROL Links auf Seite] hinzugefügt. Activity Map sendet eine neue Datenanforderung, die diese neuen Links enthält. Die neuen Links sollten in der Tabelle [!UICONTROL Links auf Seite] angezeigt werden, wenn die Datenanforderung von der Benutzeroberfläche verarbeitet wird.


## Bietet Activity Map Daten zu „Ansichten“?

Nein, Adobe verfolgt keine Links, die angezeigt wurden.

## Welche Browser und Versionen werden von Activity Map unterstützt?

Activity Map unterstützt die aktuelle Version der gängigsten Browser.

## Führt Activity Map zu einer Zunahme von Server-Aufrufen?

Activity Map sendet keine Server-Aufrufe von sich aus. Stattdessen werden die Kontextdatenvariablen von Activity Map in die Seitenaufrufe der Analytics-Ansicht auf der nachfolgenden Seite einbezogen.

## Warum fehlen für einige Elemente, denen ein Rang zugewiesen wurde, die Überlagerungen?**

Einige Rang-Links, wie z. B. Untermenü-Links, werden auf der Seite ausgeblendet. Daher werden die entsprechenden Link-Überlagerungen nicht angezeigt. Der Rang wird für alle Links auf der Seite berechnet, einschließlich ausgeblendeter Links.

## Wie wird die Rangzuweisung für Links im Bericht „Alle Links“ bestimmt?**

* **In den Modi „Verlauf“ und „Blase“**: Die Rangzuweisung wird anhand der Metrikspalte bestimmt. Für Links mit dem gleichen Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* **Im Modus „Gewinner und Verlierer“** wird der Rang hauptsächlich anhand der Spalte „% Gewinn“ bestimmt. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

## Wie funktioniert Activity Map mit Seiten, die mehrere Report Suites verwenden?

Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag verbunden ist, das von der Seite gesendet wird. Sie können eine andere getaggte Report Suite auf der Registerkarte unter **[!UICONTROL Einstellungen für Activity Map]** > **[!UICONTROL Andere]** auswählen.

## Wie lange sucht Activity Map nach Adobe Analytics auf der Seite?

Activity Map sucht bis zu 20 Sekunden nach Adobe Analytics, nachdem ein „page complete“-Ereignis abgeschlossen ist.

## Wie behandelt Activity Map dynamischen Inhalte?

Activity Map sucht alle zwei Sekunden nach Statusänderungen der Web-Seite wie:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wird Inhalt verborgen oder angezeigt, so ändert da Programm automatisch den Status der betroffenen Links (und somit der Überlagerungen) von „verborgen“ in „angezeigt“ oder umgekehrt. Wird neuer Inhalt eingefügt, ruft das Programm die zugehörigen Links ab, generiert Analysedaten für sie und fügt Überlagerungen für diese Links hinzu.

## Auf welcher Metrik basiert der Seitenflussbericht?

Alle angezeigten Daten basieren auf Seitenansichten.

## Kann ich Kontextdatenvariablen aus Activity Map über Daten-Feeds exportieren?

Kontextdatenvariablen aus Activity Map sind in Daten-Feeds nicht verfügbar.

## Funktionieren Segmente im Live-Modus?

Nein, Segmente funktionieren nicht im Live-Modus. Die Funktionalität entspricht der von Echtzeit-Berichten in Reports &amp; Analytics, die keine Segmentierung unterstützen.

## Ist Activity Map mit Virtual Report Suites kompatibel?

Ja. Aufgrund der Einschränkungen von Virtual Report Suites ist jedoch der Live-Modus von Activity Map nicht mit Virtual Report Suites kompatibel.
