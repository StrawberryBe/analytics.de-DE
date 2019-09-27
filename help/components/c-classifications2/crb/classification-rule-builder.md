---
description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
seo-description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
seo-title: Classification Rule Builder-Workflow
solution: Analytics
subtopic: Classifications
title: Classification Rule Builder-Workflow
topic: Admin Tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Classification Rule Builder-Workflow

Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.

## Important Notice before you get started

Keep this in mind before you start using classification rules:

* Our current classification system can only export up to 10 million rows at a time.
* Wenn Classification Rule Builder (CRB) einen Export anfordert, zieht es sowohl klassifizierte als auch nicht klassifizierte Werte, wobei nicht klassifizierte Werte am Ende des Exports durchlaufen werden. Das bedeutet, dass man im Laufe der Zeit 10 Millionen klassifizierte Werte füllen könnte - ohne jemals zu den nicht klassifizierten Werten zu gelangen.
* Da die Architektur so eingerichtet ist, dass CRB von der Anzahl der Server mit "n"zurückgreifen kann, kann dies zu Inkonsistenzen darüber führen, welche Server aufgenommen werden und in welcher Reihenfolge. Aus diesem Grund ist es sehr schwierig, nicht klassifizierte Werte zu bekommen.

Dies ist die **Lösung** für diejenigen, die mehr als 10 Millionen klassifizierte Werte für eine Dimension haben: Sie müssen nicht klassifizierte Werte per FTP in 10 Millionen Stapel exportieren und manuell klassifizieren.

## Erste Schritte mit Classification-Regeln {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Rule Builder]**

Hier sind die Schritte auf hoher Ebene, die Sie zur Implementierung von Classification-Regeln unternehmen:

| Schritt | Wo | Beschreibung |
|--- |--- |--- |
| Step 1 (Prerequisite): [Set up your classification schema](https://marketing.adobe.com/resources/help/en_US/reference/c_classifications.html). | [!UICONTROL Admin] &gt; [!UICONTROL Report Suites] &gt; Einstellungen [!UICONTROL bearbeiten] &gt; &lt;Traffic-Klassifizierungen oder Umrechnungsklassifizierungen&gt; | Wählen Sie eine Variable aus und definieren Sie die für die Variable zu verwendenden Classifications. <br>Für Variablen muss mindestens eine Classification-Spalte erstellt werden, bevor sie in Regeln genutzt werden können.<br>Sobald Classifications aktiviert sind, können Sie den Importeur und den Rule Builder verwenden, um bestimmte Werte zu klassifizieren. |
| Step 2: [Create a rule set](../../../components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL Admin] &gt; [!UICONTROL Classification Rule Builder] &gt; [!UICONTROL Regelsatz hinzufügen] | Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. |
| Schritt 3: Report Suites und Variablen konfigurieren. | [!UICONTROL Classification Rule Builder] &gt; &lt;Ihr Regelsatz&gt; | Wenden Sie den Regelsatz auf Report Suites und Variablen an. |
| Step 4: [Add classification rules to the set](../../../components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] &gt; &lt;Ihr Regelsatz&gt; | Ordnen Sie einer Classification eine Bedingung zu, und legen Sie die Aktion fest, die für die Regel ausgeführt werden soll.  Machen Sie sich mit den Informationen in der [Verarbeitung](../../../components/c-classifications2/crb/classification-quickstart-rules.md)von Regeln vertraut. |
| Step 5: [Test a Classification Rule Set](../../../components/c-classifications2/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | Zum Testen der Regeln im Rahmen der Validierung bearbeiten Sie die Regeln im Entwurfsmodus. Im Entwurfsmodus können keine Regeln ausgeführt werden.<br>Dieser Schritt ist bei der Verwendung [regulärer Ausdrücke](../../../components/c-classifications2/crb/classification-quickstart-rules.md)wichtig. |
| Schritt 6: Gültige Regeln [aktivieren](../../../components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Sobald die Regeln gültig sind, aktivieren Sie den Regelsatz.  Bei Bedarf können Sie vorhandene Schlüssel überschreiben. Siehe [Verarbeitung der Regeln](../../../components/c-classifications2/crb/classification-quickstart-rules.md). |
| Step 7 (Optional): [Delete unwanted rules](../../../components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Löschen Sie die unerwünschten Regeln aus dem Satz.<br>Hinweis: Beim Löschen von Regeln werden die hochgeladenen klassifizierten Daten nicht gelöscht.  See  [Delete classification data](../../../components/c-classifications2/c-classifications-importer/t-delete-classification-data.md) if you need to delete classified data. |

>[!NOTE]
>
>Gruppen mit der Berechtigung zum Verwenden des Classification-Import-Tools können Classification-Regeln verwenden. See [How Rules Are Processed](../../../components/c-classifications2/crb/classification-quickstart-rules.md) for important processing information.

**Zusätzliche Ressourcen**

**Blog**: Weitere Informationen zu dieser Funktion finden Sie im Digital Marketing Blog: [Regelbasierte Klassifizierungen](https://blogs.adobe.com/digitalmarketing/analytics/rule-based-classifications-part-1-making-classifications-easier/?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+AdobeDigitalMarketing+%28Adobe+Digital+Marketing+Blog%29).

**Video**: Besuchen Sie [YouTube](https://www.youtube.com/watch?v=6laI5SBXY-I) , um das Video mit der Übersicht über [!UICONTROL Klassifizierungen] anzuzeigen.
