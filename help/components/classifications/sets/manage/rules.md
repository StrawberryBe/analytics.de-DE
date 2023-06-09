---
title: Classification-Set-Regeln
description: Anzeigen und Bearbeiten von Regeln für einen einzelnen Classification-Satz.
source-git-commit: 496b4891d447ed9dd091a6498a792146a2d5aceb
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Classification-Set-Regeln

Mit Classification-Satzregeln können Sie Werte automatisch basierend auf dem Wert klassifizieren, auf den die Variable gesetzt ist. Diese Regeln gelten für alle eingehenden Variablenwerte für alle Abonnements des Classification-Sets.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes > **[!UICONTROL Regeln]**

## Regeleinstellungen

Einstellungen, die für den gesamten Regelsatz gelten.

* **[!UICONTROL Überschreiben von Regeln]**: Bestimmt das Verhalten aller Regeln in Fällen, in denen ein Classification-Wert vorhanden ist.
   * **[!UICONTROL Auf alle Werte anwenden]**: Wenn eine Regel übereinstimmt, überschreiben Sie immer den Classification-Wert.
   * **[!UICONTROL Nur auf nicht festgelegte Werte anwenden]**: Wenn eine Regel mit übereinstimmt, schreiben Sie den Classification-Wert nur, wenn er leer ist. Wenn ein Classification-Wert vorhanden ist, führen Sie keine Schritte aus.
* **[!UICONTROL Lookback-Fenster]**: Wenn diese Regel aktiviert wird, werden alle Regeln für alle eindeutigen Werte ausgeführt, die im hier festgelegten Lookback-Fenster angezeigt werden.

## Regeln

Eine Liste von Regeln, die für jeden eindeutigen Wert ausgeführt werden.

* **[!UICONTROL Suche]**: Ein Suchfeld, mit dem Sie Regeln nach Übereinstimmungskriterien filtern können.
* **[!UICONTROL Regel hinzufügen]**: Fügt der Regeltabelle eine leere Zeile hinzu.
* **[!UICONTROL Testregelsatz]**: Öffnet eine Test-Benutzeroberfläche, über die Sie Ihre Regeln überprüfen können. Auf der linken Seite können Sie Schlüsselwerte manuell eingeben oder eine Classification-Datei per Drag-and-Drop verschieben, um viele Werte zu importieren, mit denen Sie testen können. Rechts befindet sich eine Tabelle, die vorläufige Ergebnisse zeigt, wie klassifizierte Werte aussehen würden, wenn der Regelsatz aktiviert würde. Da diese Schnittstelle nur zur Validierung dient, werden keine Werte klassifiziert.

Wählen Sie eine oder mehrere Regeln aus, indem Sie auf das Kontrollkästchen neben der gewünschten Regel klicken. Wenn Sie eine Regel auswählen, werden die folgenden Optionen angezeigt:

* **[!UICONTROL Löschen]**: Löscht die Zeile aus der Regeltabelle.
* **[!UICONTROL Duplizieren]**: Kopiert die ausgewählten Zeilen in neue Zeilen in der Regeltabelle.

## Regeltabelle

Die Regeltabelle ist vertikal in zwei Hauptteile unterteilt: übereinstimmende Bedingung und Classification-Aktion. Jede Zeile (eine einzelne Regel) enthält eine übereinstimmende Bedingung und eine Classification-Aktion.

* **Regelnummer**: Regeln werden in der gleichen Reihenfolge ausgeführt wie die Regeltabelle. Wenn [!UICONTROL Überschreiben von Regeln] auf [!UICONTROL Auf alle Werte anwenden]überschreibt die letzte übereinstimmende Regel alle vorherigen Regeln für dieselbe Classification-Dimension. Wenn [!UICONTROL Überschreiben von Regeln] auf [!UICONTROL Nur nicht festgelegte Werte anwenden]gilt die erste Regel, die einen Classification-Wert festlegt.
* **[!UICONTROL Regeltyp auswählen]**: Die Regelkriterien. Optionen umfassen [!UICONTROL Enthält], [!UICONTROL Endet in], [!UICONTROL Regulärer Ausdruck], [!UICONTROL Regulärer Ausdruck]und [!UICONTROL Beginnt mit].
* **[!UICONTROL Übereinstimmungskriterien eingeben]**: Die Textzeichenfolge, die abgeglichen werden soll. Wenn Sie [!UICONTROL Regulärer Ausdruck] als Regeltyp angezeigt wird, erscheint eine Überlagerung, mit der Sie den Wert eingeben, den regulären Ausdruck testen und eine Beispielsyntax bereitstellen können.
* **[!UICONTROL Classification auswählen]**: Eine Dropdown-Liste, die die Classification-Dimension festlegt, der Sie einen Wert zuweisen möchten. Gültige Optionen umfassen Elemente in Ihrer [schema](schema.md).
* **[!UICONTROL nach]**: Die Textzeichenfolge, auf die der klassifizierte Wert gesetzt werden soll. Wenn der Regeltyp [!UICONTROL Regulärer Ausdruck]können Sie eine Kombination aus Text und Übereinstimmungsgruppen einschließen.
