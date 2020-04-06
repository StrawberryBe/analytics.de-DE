---
description: 'null'
title: Einschränkungen und Spezifikationen
uuid: 6717b6ea-7e01-49b8-8f6e-fb733a03b687
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Einschränkungen und Spezifikationen

## Einschränkungen für Power BI-Veröffentlichungen {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE] Diese Einschränkungen gelten nur für die Option „Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“.

* Maximal 100 Report Builder-Anforderungen pro Arbeitsmappe können nach Power BI exportiert werden.
* Der Planungsprozess beendet den Export von Anforderungen, wenn die 101. Anforderung erreicht wird.
* Pro Report Builder-Anforderung werden nur die Analytics-Daten in den ersten 10.000 Zeilen an Power BI gesendet. Die verbleibenden Zeilen werden ignoriert.

## Report Builder-Anforderung nach der Veröffentlichung in Power BI bearbeiten {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE] Diese Angaben gelten für die Optionen „Alle Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“ und „Alle formatierten Tabellen der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen“.

Bearbeiten einer Report Builder-Anforderung nach der Veröffentlichung in Power BI kann zu Problemen führen.

* **Fall 1**: Sie veröffentlichen eine Arbeitsmappe in Power BI und erstellen eine Visualisierung basierend auf den Daten. Als Nächstes nehmen Sie Änderungen an der Arbeitsmappe vor, wodurch eine der Spalten des Datensatzes, auf die sie verweist, ausgeblendet wird. Anschließend veröffentlichen Sie erneut. Dies wird die Visualisierung in Power BI unterbrechen.

   **Hier ein Beispiel, wie die Visualisierung umbrechen wird:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   1. [Planen Sie die Veröffentlichung dieser Anforderung](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section) in Power BI.
   1. Erstellen Sie in Power BI eine Visualisierung für Seiten- und Seiten-Ansichten.
   1. Bearbeiten Sie die Arbeitsmappe jetzt, indem Sie die Ansichten der Seite aus der Anforderung entfernen.
   1. Bearbeiten Sie den Zeitplan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung erneut auf Power BI.
   1. Sobald die neue Arbeitsmappe an Power BI gesendet wurde

      1. Vergewissern Sie sich, dass der beim ersten Veröffentlichen erstellte Datensatz überschrieben wurde.
      1. Überprüfen Sie, ob die Tabelle &quot;page_1&quot;ordnungsgemäß mit den Spalten &quot;Seite&quot;und &quot;Besuche&quot;aktualisiert wurde.
      1. Überprüfen Sie, ob Ihre Visualisierung beschädigt ist, da sie auf die Spalte &quot;Seiten-Ansichten&quot;verweist, die nicht mehr in der Tabelle &quot;page_1&quot;vorhanden ist.
   **Hier ein Beispiel, wie die Visualisierung NICHT umbrechen wird:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   1. [Planen Sie die Veröffentlichung dieser Anforderung](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section) in Power BI.
   1. Erstellen Sie in Power BI eine Visualisierung für Seiten- und Seiten-Ansichten.
   1. Bearbeiten Sie die Arbeitsmappe in Report Builder, indem Sie die Metrik für Besuche hinzufügen und „Seite“ sowie „Seitenansichten“ beibehalten.
   1. Bearbeiten Sie den Zeitplan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung erneut auf Power BI.
   1. Sobald die neue Arbeitsmappe an Power BI gesendet wurde

      1. Vergewissern Sie sich, dass der beim ersten Veröffentlichen erstellte Datensatz überschrieben wurde.
      1. Vergewissern Sie sich, dass die Tabelle &quot;page_1&quot;ordnungsgemäß mit den Spalten &quot;Seite&quot;, &quot;Ansichten&quot;und &quot;Besuche&quot;aktualisiert wurde.
      1. Überprüfen Sie, ob Ihre Visualisierung weiterhin ordnungsgemäß funktioniert, da sie auf zwei Spalten verweist, die noch in der Tabelle &quot;page_1&quot;vorhanden sind.


* **Fall 2**: Sie veröffentlichen einen Abschnitt Ihrer Arbeitsmappe in Power BI in ein Dashboard und entfernen ihn später aus der Arbeitsmappe (z. B. ein Diagramm oder eine Tabelle). Dadurch wird die Visualisierung unterbrochen.

## Power BI-Berichtnamen ändern {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Standardmäßig wird der Name aus dem Arbeitsmappendateinamen (ohne die Erweiterung .xlsx) gefüllt, wobei Leerzeichen jedoch durch Unterstrichzeichen ersetzt werden.

Bedenken Sie Folgendes

* Die Beschriftung darf keine Kombination aus Buchstaben und Zahlen sein, die mit einer Zeilen- und Spaltenadresse verwechselt werden könnten. Beispielsweise kann A100 keine Beschriftung sein, da es die Adresse einer Zelle in einem Arbeitsblatt ist.
* Die folgenden Zeichen sind keine gültigen Beschriftungszeichen: &#39;#&#39;, &#39;@&#39;, &#39;!&#39;, &#39;$&#39;, &#39;^&#39;, &#39;&amp;&#39;, &#39;*&#39;, &#39;`, &#39;~&#39;, &#39; &#39;. Sie werden durch einen Unterstrich ersetzt.
* Wenn Sie einen ungültigen Namen eingeben, wird eine Warnmeldung angezeigt, die einen automatisch generierten Namen anzeigt. Wenn Sie auf klicken **[!UICONTROL Yes]**, wird dieser Name verwendet. Wenn Sie auf **[!UICONTROL No]** klicken, können Sie in der Benutzeroberfläche des erweiterten Assistenten den neuen Namen eingeben.

