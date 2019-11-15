---
description: Installieren Sie den älteren Adobe Experience Cloud-Debugger. Dieser Debugger überprüft Tags für Analytics, Target, Advertising Cloud, Identitätsdienst, DTM und Launch.
title: Veralteter Adobe Experience Cloud-Debugger
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Veralteter Adobe Experience Cloud-Debugger

> [!IMPORTANT] Dieses Debugging-Tool wird nicht mehr unterstützt. Adobe empfiehlt stattdessen die Chrome-Erweiterung [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html).

Der [!UICONTROL Legacy-Debugger] prüft Tags für die meisten Adobe Experience Cloud-Dienste. Mithilfe des Debuggers können Sie sehen, welche Daten auf einer bestimmten Seite Ihrer Site an Adobe gesendet werden. Mit diesen Informationen können Sie die Implementierung Ihres Unternehmens überprüfen oder überprüfen.

## Installieren des Legacy-Debuggers

Erstellen Sie ein JavaScript-Lesezeichen, um den Debugger zu installieren.

### Schritt 1: Lesezeichen-Code kopieren

Kopieren Sie den folgenden Code in die Zwischenablage:

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### Schritt 2: Lesezeichen-Code in ein Lesezeichen einfügen

Jeder Browser hat verschiedene Möglichkeiten, Lesezeichen zu bearbeiten, aber das Konzept ist dasselbe. Ein Lesezeichen wird mit dem gewünschten Namen und dem Lesezeichen-Code als URL erstellt.

#### Chrome

Wenn Sie darauf bestehen, die [Chrome-Erweiterung](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html)nicht zu verwenden, kann stattdessen das Legacy-Debugger-Bookmarklet verwendet werden.

1. Klicken Sie auf die drei Punkte oben rechts und gehen Sie dann zu Lesezeichen &gt; Lesezeichen-Manager. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `O` (Windows) oder `Cmd` + `Shift` + `O` (Mac) drücken.
2. Klicken Sie oben rechts im Lesezeichen-Manager auf die drei Punkte und dann auf "Neues Lesezeichen hinzufügen".
3. Geben Sie im Feld Name die Bezeichnung "Adobe Experience Cloud-Debugger"ein und fügen Sie das Codefragment in das Feld URL ein.
4. Verwenden Sie den Lesezeichen-Manager, um Ihr neues Lesezeichen an der gewünschten Stelle zu platzieren.

#### Firefox

1. Klicken Sie auf die drei Zeilen oben rechts und gehen Sie dann zu Bibliothek &gt; Lesezeichen &gt; Alle Lesezeichen anzeigen. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `B` (Windows) oder `Cmd` + `Shift` + `B` (Mac) drücken.
2. Klicken Sie auf Organisieren &gt; Neues Lesezeichen.
3. Geben Sie im Feld Name die Bezeichnung "Adobe Experience Cloud-Debugger"ein und fügen Sie das Codefragment in das Feld Speicherort ein. Die Felder "Tags"und "Suchbegriff"sind nicht erforderlich.
4. Verwenden Sie das Bibliotheksfenster, um das neue Lesezeichen an der gewünschten Position zu platzieren.

#### Edge

Edge kann kein Lesezeichen manuell erstellen, aber eine Lesezeichen-URL kann bearbeitet werden.

1. Klicken Sie auf das Sternsymbol rechts neben dem Feld "URL", um die aktuelle Seite mit einem Lesezeichen zu versehen.
2. Benennen Sie das Lesezeichen "Adobe Experience Cloud-Debugger"und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf das Sternsymbol mit Linien, um die Favoritenleiste zu öffnen.
4. Klicken Sie mit der rechten Maustaste auf das neu erstellte Lesezeichen und wählen Sie "URL bearbeiten".
5. Fügen Sie das Codefragment in das Textfeld ein und drücken Sie die Eingabetaste.

#### Safari

Safari kann kein Lesezeichen manuell erstellen, aber eine Lesezeichen-URL kann bearbeitet werden.

1. Klicken Sie oben rechts auf das Symbol Freigeben, um ein modales Lesezeichen-Fenster zu öffnen.
2. Benennen Sie das Lesezeichen "Adobe Experience Cloud-Debugger"und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf Lesezeichen &gt; Lesezeichen bearbeiten und suchen Sie das neu erstellte Lesezeichen.
4. Klicken Sie mit der rechten Maustaste auf &gt; Adresse bearbeiten und fügen Sie dann das Codefragment in das Textfeld ein.

## Verwenden des alten Debuggers

Um den Debugger zu verwenden, navigieren Sie zur gewünschten Seite auf Ihrer Site und klicken Sie dann auf das Lesezeichen. Es wird ein Popupfenster mit an Adobe gesendeten Daten angezeigt.

> [!NOTE] Bestimmte werbeblockierende Plug-Ins und Popup-Blocker können das Laden des Debug-Fensters beeinträchtigen. Überprüfen Sie, ob Popups im Browser blockiert sind, und lassen Sie sie zu, damit der Debugger ordnungsgemäß funktioniert.

Für den Debugger stehen verschiedene Optionen zur Verfügung, mit denen die Anzeige der Daten angepasst wird. Keine dieser Optionen wirkt sich auf die Datenerfassung aus.

* **** Angezeigte Experience Cloud-Produkte: Blendet Bildanforderungen für die einzelnen Experience Cloud-Produkte ein oder aus.
* **** URL-Dekode: Die URL dekodiert die Bildanforderung entsprechend der Anzeige in der Berichterstellung. Adobe empfiehlt, dieses Kontrollkästchen zu aktivieren.
* **** Automatisch aktualisieren: Aktualisiert das Popup alle paar Sekunden automatisch, um nach weiteren Bildanforderungen auf der Seite zu suchen. Wenn Sie Inhalte im Debugger kopieren/einfügen müssen, deaktivieren Sie die automatische Aktualisierung, damit die Auswahl erhalten bleibt.
* **** Benutzerfreundliches Format: Schaltet das Anzeigeformat zwischen hilfreichen Beschriftungen und unbearbeiteten Abfragezeichenfolgen in einer Bildanforderung um. Weitere Informationen finden Sie unter Abfrageparameter[ zur ](../js-implementation/data-collection/query-parameters.md)Datenerfassung.

Um die standardmäßigen Anzeigeoptionen für den Debugger zu speichern, klicken Sie mit der rechten Maustaste auf den Link "Adobe Debugger"in der oberen rechten Ecke und kopieren Sie dann die Link-Adresse. Bearbeiten Sie das aktuelle Debugger-Bookmarklet und fügen Sie das aktualisierte Codefragment in das Feld URL ein.
