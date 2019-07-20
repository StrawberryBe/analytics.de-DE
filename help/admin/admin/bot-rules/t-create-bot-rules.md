---
description: Mit benutzerspezifischen Bot-Regeln können Sie Traffic auf Grundlage selbst definierter Bedingungen filtern.
seo-description: Mit benutzerspezifischen Bot-Regeln können Sie Traffic auf Grundlage selbst definierter Bedingungen filtern.
seo-title: Erstellen einer benutzerspezifischen Bot-Regel
solution: Analytics
subtopic: Bot Rules
title: Erstellen einer benutzerspezifischen Bot-Regel
topic: Admin Tools
uuid: abbc 5 c 7 e -912 f -4660-a 02 b -0431 a 740 ec 70
translation-type: tm+mt
source-git-commit: 93d6c7698216b3064f5417dbcfb33184efc2c132

---


# Erstellen einer benutzerspezifischen Bot-Regel

Mit benutzerspezifischen Bot-Regeln können Sie Traffic auf Grundlage selbst definierter Bedingungen filtern.

Benutzerspezifische Bot-Regeln werden mithilfe der folgenden Bedingungstypen definiert:

* Benutzeragent
* IP-Adresse
* IP-Bereich

Für eine einzige Regel können mehrere Bedingungen definiert werden. Mehrere Bedingungen werden mithilfe des „oder“-Befehls zugewiesen. Wenn Sie beispielsweise einen Wert für Benutzeragent und IP-Adresse bereitstellen, wird der Traffic als Bot-Traffic gewertet, wenn eine dieser beiden Bedingungen erfüllt ist.

## Benutzeragent

Eine Benutzeragent-Bedingung prüft den Benutzeragentenwert, um zu sehen, ob dieser mit der angegebenen Zeichenfolge **[!UICONTROL beginnt]** oder diese **enthält[!UICONTROL .]** Wenn **[!UICONTROL enthält]ausgewählt wurde, wird die Unter-Zeichenfolge zugewiesen, wenn sie an einer beliebigen Stelle im Benutzeragenten auftaucht.**

Optionale Werte können in die Liste **[!UICONTROL enthält nicht]aufgenommen werden, um Werte zu definieren, die der Benutzeragent für eine erfolgreiche Übereinstimmung nicht enthalten darf.** Sie können mehrere Werte spezifizieren, indem Sie einen Wert pro Zeile aufnehmen. Wenn der Benutzeragent die in der Übereinstimmungszeichenfolge spezifizierten Kriterien erfüllt, aber auch eine Zeichenfolge enthält, die auf der „enthält nicht“-Liste steht, wird er nicht als Übereinstimmung gewertet.

**[!UICONTROL Das „enthält“-Feld ist auf 100 Zeichen begrenzt.]** Die „enthält nicht“-Liste ist auf 255 Zeichen abzüglich eines Trennzeichens für jede neue Zeile begrenzt. (Dies entspricht der Anzahl der Zeichenfolgen – 1. Wenn Sie vier *enthält nicht*-Zeichenfolgen spezifizieren, werden drei Trennzeichen benötigt.) Bei allen Zeichenfolgen-Übereinstimmungen wird zwischen Groß- und Kleinschreibung unterschieden.

## IP-Adresse (inklusive Wildcard-Übereinstimmungen)

Weist eine oder mehrere IP-Adressen im selben Block mithilfe von Wildcards (*) zu. Geben Sie die numerischen Werte der IP-Adresse an, für die Sie eine Übereinstimmung suchen. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch ein Sternchen (*). Die folgende Liste enthält Beispiele der IP-Adressen-Übereinstimmungszeichenfolge:

```
10.10.10.1
10.10.10.*
```

## IP-Adressbereich

Geben Sie die Start- und Endbereiche der zuzuweisenden IP-Adressen an. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch ein Sternchen (*).

## Definieren einer benutzerspezifischen Bot-Regel

1. Go to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]**, select one or more report suites and click **[!UICONTROL General]** &gt; **[!UICONTROL Bot Rules]**.
1. Click **[!UICONTROL Add Rule]** and define one or more match conditions.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Die Änderung sollte binnen 30 Minuten in Kraft treten.

>[!Note]
>In der Benutzeroberfläche können 500 Regeln manuell definiert werden. Wenn diese Grenze erreicht wurde, müssen Regeln über die Optionen „Datei importieren“ und „Bot-Regeln exportieren“ stapelweise verwaltet werden.
