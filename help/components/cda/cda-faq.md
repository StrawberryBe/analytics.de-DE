---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen für geräteübergreifende Analysen
translation-type: tm+mt
source-git-commit: 40d8ecae1ac7e0a1df4a2df17f5104bee6ecf336

---


# Häufig gestellte Fragen

> [!NOTE] Die geräteübergreifende Analytics-Dokumentation kann sich ändern, wenn die Funktion weiter entwickelt wurde. Überprüfen Sie regelmäßig nach Updates.

**Wie kann ich CDA verwenden, um zu erfahren, wie die Menschen von einem Gerätetyp zu einem anderen wechseln?**

Sie können eine Flussvisualisierung mit der Dimension "Mobilgerätetyp" verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Arbeitsflächenprojekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte Visualisierungen und ziehen Sie eine Flussvisualisierung auf die Arbeitsfläche rechts.
3. Klicken Sie auf der linken Seite auf die Registerkarte "Komponenten" und ziehen Sie die Dimension" Mobilgerätetyp" auf den mittleren Speicherort mit der Bezeichnung "Dimension oder Element" .
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um die Flüsse auf die nachfolgenden oder vorherigen Seiten zu erweitern. Verwenden Sie das Rechtsklick-Menü, um Spalten zu erweitern oder zu minimieren. Innerhalb desselben Flussberichts können auch unterschiedliche Dimensionen verwendet werden.

**Kann ich sehen, wie Menschen zwischen verschiedenen Benutzererfahrungen wechseln (z. B. Desktop-Browser und Mobilbrowser oder Mobilgeräte-App)?**

Mit dem oben aufgeführten Mobilgerätetyp können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktopgerätetypen wechseln. Möglicherweise möchten Sie jedoch auch Desktop-Browser von mobilen Browsern unterscheiden. Eine Möglichkeit hierfür besteht darin, eine evar zu erstellen, die aufzeichnet, ob das Erlebnis in einem Desktop-Browser, mobilen Browser oder mobilen App aufgetreten ist. Erstellen Sie dann ein Flussdiagramm, wie oben beschrieben, mithilfe Ihrer "Erlebnis" -evar statt der Dimension" Mobilgerätetyp" . Dies bietet eine etwas andere Ansicht für geräteübergreifende Verhaltensweisen.

**Wie weit werden die Besucher durch CDA geneigt?**

* Adobe hält Gerätestitching-Daten ungefähr 30 Tage lang. Wenn ein Gerät intitial ist, das nicht durch das Co-Op-Diagramm oder das Private Diagramm identifiziert wird, sondern später innerhalb von 30 Tagen identifiziert wird, wechselt CDA zurück und erinnert sich an die angegebene Person bis zu 30 Tage in der Vergangenheit. Wenn ein nicht identifizierbarer Verhalten eines Benutzers außerhalb des 30-Tage-Lookback-Fensters fällt, wird dieser Teil der Benutzerreise nicht gestipft.
* Adobe hält Gerätezuordnungen im Co-op-Diagramm und im privaten Diagramm für ca. 6 Monate bereit. Eine ECID, die über keine Aktivität für mehr als sechs Monate verfügt, wird aus dem Diagramm entfernt. Bereits in CDA angezeigte Daten sind nicht betroffen, aber folgende Treffer für diese ECID werden als neue Person behandelt.

**Wie verarbeitet CDA Treffer mit Zeitstempel?**

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels empfangen worden, nicht als Adobe den Treffer erhielten. Hits mit Zeitstempel, die älter als 1 Monat sind, können nicht gestipft werden, da sie außerhalb des Bereichs angesehen werden, der für die Stitching-Speicherung verwendet wird.
