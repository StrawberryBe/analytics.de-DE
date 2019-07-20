---
description: 'null '
seo-description: 'null '
seo-title: Einschränkungen und Spezifikationen
title: Einschränkungen und Spezifikationen
uuid: 6717 b 6 ea -7 e 01-49 b 8-8 f 6 e-fb 733 a 03 b 687
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Einschränkungen und Spezifikationen

## Power BI publishing restrictions {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE]
>
>Diese Einschränkungen gelten nur für die Option "Reportbuilder-Anforderungen als Power BI Datensatz-Tabellen veröffentlichen" .

* Maximal 100 ReportBuilder-Anforderungen pro Arbeitsmappe können nach Power BI exportiert werden.
* Dieser Planungsvorgang beendet den Export, sobald die 101. Anforderung erreicht ist.
* Pro ReportBuilder-Anforderung werden nur die Analytics-Daten in den ersten 10.000 Zeilen an Power BI gesendet. Die restlichen Zeilen werden ignoriert.

## Edit a Report Builder request after publishing to Power BI {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE]
>
>Diese Spezifikation gilt für die Optionen "Alle Reportbuilder-Anforderungen als Power BI Datensatz-Tabellen veröffentlichen" und" Alle formatierten Tabellen in den Arbeitsmappen als Power BI Datensatz-Tabellen veröffentlichen" .

Bearbeiten einer ReportBuilder-Anforderung nach der Veröffentlichung in Power BI kann zu Problemen führen.

* **Fall 1**: Sie veröffentlichen eine Arbeitsmappe in Power BI und erstellen eine Visualisierung basierend auf den darin enthaltenen Daten. Als Nächstes ändern Sie die Arbeitsmappe, indem Sie eine der Spalten aus dem referenzierten Datensatz ausblenden. Dann veröffentlichen Sie sie erneut. Dadurch wird die Visualisierung in Power BI beschädigt.

   **Beispiel für eine Bearbeitung MIT Beschädigung der Visualisierung:**

   1. Erstellen Sie in ReportBuilder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   1. [Planen](../../../analyze/report-builder/whats-new-arb.md#section_0C26057C7DBB4068A643FDD688F6E463) Sie die Veröffentlichung dieser Anforderung in Power BI.
   1. Erstellen Sie in Power BI eine Visualisierung für „Seite“ und „Seitenansichten“.
   1. Bearbeiten Sie die Arbeitsmappe, indem Sie „Seitenansichten“ aus der Anforderung entfernen.
   1. Bearbeiten Sie den Plan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung für Power BI erneut.
   1. Nachdem die neue Arbeitsmappe an Power BI gesendet wurde, gehen Sie wie folgt vor:

      1. Vergewissern Sie sich, dass der bei Ihrer ersten Veröffentlichung erstellte Datensatz überschrieben wurde.
      1. Stellen Sie sicher, dass die Tabelle für Seite 1 ordnungsgemäß mit den Spalten „Seite“ und „Besuche“ aktualisiert wurde.
      1. Prüfen Sie, ob die Visualisierung beschädigt ist, da sie die Spalte „Seitenansichten“ referenziert, die nicht mehr in der Tabelle für Seite 1 enthalten ist.
   **Beispiel für eine Bearbeitung OHNE Beschädigung der Visualisierung:**

   1. Erstellen Sie in ReportBuilder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   1. [Planen](../../../analyze/report-builder/whats-new-arb.md#section_0C26057C7DBB4068A643FDD688F6E463) Sie die Veröffentlichung dieser Anforderung in Power BI.
   1. Erstellen Sie in Power BI eine Visualisierung für „Seite“ und „Seitenansichten“.
   1. Bearbeiten Sie die Arbeitsmappe in ReportBuilder, indem Sie die Metrik für Besuche hinzufügen und „Seite“ sowie „Seitenansichten“ beibehalten.
   1. Bearbeiten Sie den Plan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung für Power BI erneut.
   1. Nachdem die neue Arbeitsmappe an Power BI gesendet wurde, gehen Sie wie folgt vor:

      1. Vergewissern Sie sich, dass der bei Ihrer ersten Veröffentlichung erstellte Datensatz überschrieben wurde.
      1. Stellen Sie sicher, dass die Tabelle für Seite 1 ordnungsgemäß mit den Spalten „Seite“, „Seitenansichten“ und „Besuche“ aktualisiert wurde.
      1. Prüfen Sie, ob Ihre Visualisierung weiterhin korrekt funktioniert, da sie zwei Spalten referenziert, die sich noch immer in der Tabelle für Seite 1 befinden.


* **Fall 2**: Heften Sie einen Abschnitt Ihrer Arbeitsmappe an ein Dashboard in Power BI an und entfernen Sie diesen angehefteten Abschnitt (beispielsweise ein Diagramm oder eine Tabelle) später aus der Arbeitsmappe. Dadurch wird die Visualisierung beschädigt.

## Change the name of a Power BI report {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Standardmäßig wird der Name aus dem Dateinamen der Arbeitsmappe abgeleitet (ohne die Erweiterung „.xlsx“), wobei Leerzeichen durch Unterstriche ersetzt werden.

Bedenken Sie Folgendes:

* Die Bezeichnung darf keine Kombination aus Buchstaben und Zahlen sein, die mit einer Zeilen- und Spaltenadresse verwechselt werden kann. Beispielsweise darf die Bezeichnung nicht A100 lauten, da dies die Adresse einer Zelle in einem Arbeitsblatt ist.
* Die folgenden Zeichen sind für eine Bezeichnung nicht gültig: '#', '@', '!', '$', '^', '&amp;', '*', '`', '~', ' ' . Sie werden durch einen Unterstrich ersetzt.
* Wenn Sie einen ungültigen Namen eingeben, wird eine Warnmeldung angezeigt, in der ein automatisch generierter Name vorgeschlagen wird. If you click **[!UICONTROL Yes]**, this name will be used. If you click **[!UICONTROL No]**, the Advanced Wizard UI will let you enter the new name.

