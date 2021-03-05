---
description: Einschränkungen bei der Verwendung von Report Builder und Microsoft Power BI.
title: Einschränkungen und Spezifikationen
uuid: 6717b6ea-7e01-49b8-8f6e-fb733a03b687
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 97%

---


# Einschränkungen und Spezifikationen

## Einschränkungen für Power BI-Veröffentlichungen {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE]
>
> Diese Einschränkungen gelten nur für die Option „Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“.

* Maximal 100 Report Builder-Anforderungen pro Arbeitsmappe können nach Power BI exportiert werden.
* Dieser Planungsvorgang beendet den Export, sobald die 101. Anforderung erreicht ist.
* Pro Report Builder-Anforderung werden nur die Analytics-Daten in den ersten 10.000 Zeilen an Power BI gesendet. Die restlichen Zeilen werden ignoriert.

## Report Builder-Anforderung nach der Veröffentlichung in Power BI bearbeiten {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE]
>
> Diese Angaben gelten für die Optionen „Alle Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“ und „Alle formatierten Tabellen der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen“.

Bearbeiten einer Report Builder-Anforderung nach der Veröffentlichung in Power BI kann zu Problemen führen.

* **Fall 1**: Sie veröffentlichen eine Arbeitsmappe in Power BI und erstellen eine Visualisierung basierend auf den darin enthaltenen Daten. Als Nächstes ändern Sie die Arbeitsmappe, indem Sie eine der Spalten aus dem referenzierten Datensatz ausblenden. Dann veröffentlichen Sie sie erneut. Dadurch wird die Visualisierung in Power BI beschädigt.

   **Beispiel für eine Bearbeitung MIT Beschädigung der Visualisierung:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   2. Planen Sie die Veröffentlichung dieses Antrags bei Power BI.
   3. Erstellen Sie in Power BI eine Visualisierung für „Seite“ und „Seitenansichten“.
   4. Bearbeiten Sie die Arbeitsmappe, indem Sie „Seitenansichten“ aus der Anforderung entfernen.
   5. Bearbeiten Sie den Plan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung für Power BI erneut.
   6. Nachdem die neue Arbeitsmappe an Power BI gesendet wurde, gehen Sie wie folgt vor:

      1. Vergewissern Sie sich, dass der bei Ihrer ersten Veröffentlichung erstellte Datensatz überschrieben wurde.
      2. Stellen Sie sicher, dass die Tabelle für Seite 1 ordnungsgemäß mit den Spalten „Seite“ und „Besuche“ aktualisiert wurde.
      3. Prüfen Sie, ob die Visualisierung beschädigt ist, da sie die Spalte „Seitenansichten“ referenziert, die nicht mehr in der Tabelle für Seite 1 enthalten ist.

   **Beispiel für eine Bearbeitung OHNE Beschädigung der Visualisierung:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   2. Planen Sie die Veröffentlichung dieser Anforderung in Power BI.
   3. Erstellen Sie in Power BI eine Visualisierung für „Seite“ und „Seitenansichten“.
   4. Bearbeiten Sie die Arbeitsmappe in Report Builder, indem Sie die Metrik für Besuche hinzufügen und „Seite“ sowie „Seitenansichten“ beibehalten.
   5. Bearbeiten Sie den Plan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anforderung für Power BI erneut.
   6. Nachdem die neue Arbeitsmappe an Power BI gesendet wurde, gehen Sie wie folgt vor:

      1. Vergewissern Sie sich, dass der bei Ihrer ersten Veröffentlichung erstellte Datensatz überschrieben wurde.
      2. Stellen Sie sicher, dass die Tabelle für Seite 1 ordnungsgemäß mit den Spalten „Seite“, „Seitenansichten“ und „Besuche“ aktualisiert wurde.
      3. Prüfen Sie, ob Ihre Visualisierung weiterhin korrekt funktioniert, da sie zwei Spalten referenziert, die sich noch immer in der Tabelle für Seite 1 befinden.


* **Fall 2**: Heften Sie einen Abschnitt Ihrer Arbeitsmappe an ein Dashboard in Power BI an und entfernen Sie diesen angehefteten Abschnitt (beispielsweise ein Diagramm oder eine Tabelle) später aus der Arbeitsmappe. Dadurch wird die Visualisierung beschädigt.

## Power BI-Berichtnamen ändern {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Standardmäßig wird der Name aus dem Dateinamen der Arbeitsmappe abgeleitet (ohne die Erweiterung „.xlsx“), wobei Leerzeichen durch Unterstriche ersetzt werden.

Bedenken Sie Folgendes

* Die Bezeichnung darf keine Kombination aus Buchstaben und Zahlen sein, die mit einer Zeilen- und Spaltenadresse verwechselt werden kann. Beispielsweise darf die Bezeichnung nicht A100 lauten, da dies die Adresse einer Zelle in einem Arbeitsblatt ist.
* Die folgenden Zeichen sind für eine Bezeichnung nicht gültig: &#39;#&#39;, &#39;@&#39;, &#39;!&#39;, &#39;$&#39;, &#39;^&#39;, &#39;&amp;&#39;, &#39;*&#39;, &#39;`&#39;, &#39;~&#39;, &#39; &#39; . Sie werden durch einen Unterstrich ersetzt.
* Wenn Sie einen ungültigen Namen eingeben, wird eine Warnmeldung angezeigt, in der ein automatisch generierter Name vorgeschlagen wird. Wenn Sie auf **[!UICONTROL Ja]** klicken, wird dieser Name verwendet. Wenn Sie auf **[!UICONTROL Nein]** klicken, können Sie im erweiterten Assistenten einen neuen Namen eingeben.

