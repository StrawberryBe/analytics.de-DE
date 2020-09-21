---
title: Legacy Adobe Experience Cloud-Debugger
description: Installieren Sie den Legacy Adobe Experience Cloud-Debugger. Dieser Debugger überprüft Tags für Analytics, Target, Advertising Cloud, den Identitätsdienst, DTM und Launch.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '690'
ht-degree: 100%

---


# Legacy Adobe Experience Cloud-Debugger

>[!IMPORTANT]
>
>Dieses Debugging-Tool wird nicht mehr unterstützt. Adobe empfiehlt stattdessen die Chrome-Erweiterung [Adobe Experience Cloud-Debugger](https://docs.adobe.com/content/help/de-DE/debugger/using/experience-cloud-debugger.html).

Der [!UICONTROL Legacy-Debugger] prüft Tags für die meisten Adobe Experience Cloud-Dienste. Mithilfe des Debuggers können Sie sehen, welche Daten auf einer bestimmten Seite Ihrer Site an Adobe gesendet werden. Anhand dieser Informationen können Sie die Implementierung Ihrer Organisation reparieren oder validieren.

## Installieren des Legacy-Debuggers

Erstellen Sie ein JavaScript-Lesezeichen, um den Debugger zu installieren.

### Schritt 1: Lesezeichen-Code kopieren

Kopieren Sie den folgenden Code in die Zwischenablage:

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### Schritt 2: Lesezeichen-Code in ein Lesezeichen einfügen

Jeder Browser hat verschiedene Möglichkeiten, Lesezeichen zu bearbeiten, aber das Konzept ist dasselbe. Ein Lesezeichen wird mit dem gewünschten Namen und dem Lesezeichen-Code als URL erstellt.

#### Chrome

Wenn Sie darauf bestehen, die [Chrome-Erweiterung](https://docs.adobe.com/content/help/de-DE/debugger/using/experience-cloud-debugger.html) nicht zu verwenden, kann stattdessen das Legacy-Debugger-Lesezeichen verwendet werden.

1. Klicken Sie auf die drei Punkte oben rechts und gehen Sie dann zu „Lesezeichen“ > „Lesezeichen-Manager“. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `O` (Windows) oder `Cmd` + `Shift` + `O` (Mac) drücken.
2. Klicken Sie oben rechts im Lesezeichen-Manager auf die drei Punkte und dann auf „Neues Lesezeichen hinzufügen“.
3. Geben Sie im Feld „Name“ die Bezeichnung „Adobe Experience Cloud-Debugger“ ein und fügen Sie den Codeausschnitt in das Feld „URL“ ein.
4. Verwenden Sie den Lesezeichen-Manager, um Ihr neues Lesezeichen an der gewünschten Stelle zu platzieren.

#### Firefox

1. Klicken Sie auf die drei Zeilen oben rechts und gehen Sie dann zu „Bibliothek“ > „Lesezeichen“ > „Alle Lesezeichen anzeigen“. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `B` (Windows) oder `Cmd` + `Shift` + `B` (Mac) drücken.
2. Klicken Sie auf „Organisieren“ > „Neues Lesezeichen“.
3. Geben Sie im Feld „Name“ die Bezeichnung „Adobe Experience Cloud-Debugger“ ein und fügen Sie den Codeausschnitt in das Feld „Speicherort“ ein. Die Felder „Tags“ und „Keyword“ sind nicht erforderlich.
4. Verwenden Sie das Bibliotheksfenster, um Ihr neues Lesezeichen an der gewünschten Stelle zu platzieren.

#### Edge

In Edge können Sie Lesezeichen nicht manuell erstellen, jedoch können Sie eine Lesezeichen-URL in ein Lesezeichen umwandeln.

1. Klicken Sie auf das Sternsymbol rechts neben dem Feld „URL“, um die aktuelle Seite mit einem Lesezeichen zu versehen.
2. Nennen Sie das Lesezeichen „Adobe Experience Cloud-Debugger“ und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf das Sternsymbol mit Linien, um die Favoritenleiste zu öffnen.
4. Klicken Sie mit der rechten Maustaste auf das neu erstellte Lesezeichen und wählen Sie „URL bearbeiten“.
5. Fügen Sie den Codeausschnitt in das Textfeld ein und drücken Sie die Eingabetaste.

#### Safari

In Safari können Sie Lesezeichen nicht manuell erstellen, jedoch können Sie eine Lesezeichen-URL in ein Lesezeichen umwandeln.

1. Klicken Sie oben rechts auf das Symbol „Freigeben“, um ein modales Lesezeichen-Fenster zu öffnen.
2. Nennen Sie das Lesezeichen „Adobe Experience Cloud-Debugger“ und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf „Lesezeichen“ > „Lesezeichen bearbeiten“ und suchen Sie das neu erstellte Lesezeichen.
4. Klicken Sie mit der rechten Maustaste, wählen Sie „Adresse bearbeiten“ und fügen Sie dann den Codeausschnitt in das Textfeld ein.

## Verwenden des Legacy-Debuggers

Navigieren Sie zur gewünschten Seite auf Ihrer Website und klicken Sie dann auf das Lesezeichen. Es wird ein Popupfenster mit an Adobe gesendeten Daten angezeigt.

>[!NOTE]
>
>Bestimmte werbeblockierende Plug-ins und Popupblocker können das Laden des Debugger-Fensters beeinträchtigen. Überprüfen Sie, ob Popups im Browser blockiert sind, und lassen Sie sie zu, damit der Debugger ordnungsgemäß funktioniert.

Für den Debugger stehen verschiedene Optionen zur Verfügung, mit denen die Anzeige der Daten angepasst wird. Keine dieser Optionen wirkt sich auf die Datenerfassung aus.

* **Angezeigte Experience Cloud-Produkte:** Blendet Bildanforderungen für die einzelnen Experience Cloud-Produkte ein oder aus.
* **URL-Dekodierung:** Die URL dekodiert die Bildanforderung entsprechend der Anzeige im Reporting. Adobe empfiehlt, dieses Kontrollkästchen zu aktivieren.
* **Automatisch aktualisieren:** Aktualisiert das Popup alle paar Sekunden automatisch, um nach weiteren Bildanforderungen auf der Seite zu suchen. Wenn Sie Inhalte im Debugger kopieren/einfügen müssen, deaktivieren Sie die automatische Aktualisierung, damit die Auswahl erhalten bleibt.
* **Benutzerfreundliches Format:** Schaltet das Anzeigeformat zwischen hilfreichen Beschriftungen und Rohabfragezeichenfolgen in einer Bildanforderung um. Weitere Informationen finden Sie unter [Datenerfassungs-Abfrageparameter](query-parameters.md).

Um standardmäßige Anzeigeoptionen für den Debugger zu speichern, klicken Sie mit der rechten Maustaste auf den Link „Adobe Debugger“ in der oberen rechten Ecke und kopieren Sie dann die Linkadresse. Bearbeiten Sie das aktuelle Debugger-Lesezeichen und fügen Sie den aktualisierten Codeausschnitt in das Feld „URL“ ein.
