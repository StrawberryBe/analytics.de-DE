---
description: Für einen Massenimport von Bot-Regeln können Sie eine CSV-Datei hochladen, in der die Regeln definiert sind.
seo-description: Für einen Massenimport von Bot-Regeln können Sie eine CSV-Datei hochladen, in der die Regeln definiert sind.
seo-title: Hochladen von Bot-Regeln
solution: Analytics
subtopic: Bot Rules
title: Hochladen von Bot-Regeln
topic: Admin Tools
uuid: bd 70 c 199-5817-437 e -980 d -6 d 8 f 95 d 82 f 2 c
translation-type: tm+mt
source-git-commit: 319eba8896e629214000c56ad6ef6b5774e89e1e

---


# Hochladen von Bot-Regeln

Für einen Massenimport von Bot-Regeln können Sie eine CSV-Datei hochladen, in der die Regeln definiert sind.

Erstellen Sie eine CSV-Datei mit den folgenden Spalten in der angezeigten Reihenfolge:

| Spalte 1 | Spalte 2 | Spalte 3 | Spalte 4 | Spalte 5 |
|---|---|---|---|---|
| Bot-Name | IP-Start | IP-Ende | Agent-Übereinstimmungsregel<br>(`contains` oder `starts with`) | Agent Exclude<br>(255 char limit) |

Sie können drei Arten von Bot-Regeln definieren:

* Benutzeragent enthält oder beginnt mit
* Einzelne IP-Adresse oder Wildcard-Übereinstimmung
* IP-Bereichsübereinstimmung

Jede Zeile in der Importdatei kann nur eine der folgenden Bot-Definitionen enthalten:

* **Benutzeragent enthält oder beginnt mit:** Geben Sie eine einzige Benutzeragent-Zeichenfolge zur Übereinstimmung in der Spalte „Agent einschließlich“ ein. Legen Sie den gewünschten Übereinstimmungstyp fest, indem Sie im Feld zur Agent-Übereinstimmungsregel den Vermerk *enthält* oder *beginnt mit* platzieren. An optional value can be included in the Agent Exclude column that defines one or more pipe-delimited ( `|` ) strings that the Agent does not contain. Bei Zeichenfolgen-Übereinstimmungen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Sowohl die Spalte „IP-Start“ als auch „IP-Ende“ müssen leer sein.

* **Einzelne IP-Adresse oder Wildcard-Übereinstimmung**: Um eine einzelne IP-Adresse ( `10.10.10.1`) oder Wildcard-IP-Adresse ( `10.10.*.*`) zuzuordnen, müssen Sie denselben Wert sowohl in der Spalte IP-Start als auch in IP-Ende einfügen. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

* **IP-Bereichs-Übereinstimmung**: Definieren Sie einen Bereich von IP-Adressen mithilfe der Spalten „IP-Start“ und „IP-Ende“. Wildcards can be used to match IP ranges, for example `10.10.10.*` to `10.10.20.*`. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

## Mehrere mit ODER kombinierte Regeln

Um eine Übereinstimmung für einen Bot mithilfe einer ODER-Kombination aus Regeln zu finden (z. B. Benutzeragent ODER IP-Adresse), geben Sie einen identischen Namen für alle Regeln an, die Sie in dem Bot-Namensfeld kombinieren möchten. UND-Übereinstimmungen werden nicht unterstützt.

## Alle Regeln mit einer Upload-Datei überschreiben

Wählen Sie das Kontrollkästchen **[!UICONTROL Bestehende Regeln überschreiben]an, um alle bestehenden Regeln zu löschen und sie durch die in der Upload-Datei definierten Regeln zu ersetzen.**

## Exportregeln

Über die Schaltfläche **[!UICONTROL Hochgeladene Bot-Datei]werden alle in der Benutzeroberfläche definierten Regeln in einem CSV-Format exportiert.**
