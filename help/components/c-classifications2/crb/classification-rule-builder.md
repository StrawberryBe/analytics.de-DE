---
description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
seo-description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
seo-title: Classification Rule Builder-Arbeitsablauf
solution: Analytics
subtopic: Classifications
title: Classification Rule Builder-Arbeitsablauf
topic: Admin Tools
uuid: edb 1 f 07 e-fa 66-4055-8 f 4 b-cce 2 d 370 edbb
translation-type: tm+mt
source-git-commit: e71c24fa4762d7f0bc80fc7133ca1cd79dfaf7c5

---


# Classification Rule Builder-Arbeitsablauf

Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.

## Wichtige Hinweise vor dem Einstieg

Beachten Sie dies, bevor Sie mit der Verwendung von Classification-Regeln beginnen:

* Unser aktuelles Klassifizierungssystem kann jeweils nur bis zu 10 Millionen Zeilen exportieren.
* Wenn der Classification Rule Builder (CRB) einen Export anfordert, ruft er sowohl klassifizierte als AUCH nicht klassifizierte Werte ab, wobei nicht klassifizierte Werte am Ende des Exports liegen. Das bedeutet, dass Sie im Laufe der Zeit 10 Millionen klassifizierte Werte ausfüllen können - ohne jemals die nicht klassifizierten Werte zu erhalten.
* Da die Architektur so eingerichtet ist, dass CRB von der Anzahl der Server abgerufen werden kann, kann dies zu Inkonsistenzen führen, an denen die Server abgerufen werden und in welcher Reihenfolge. Aus diesem Grund ist es sehr schwer, zu nicht klassifizierten Werten zu gelangen.

This is the **workaround** for those who have more than 10 million classified values for a dimension: You will need to export unclassified values via FTP, in 10-million batches, and manually classify them.

## Erste Schritte mit Classification-Regeln {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Rule Builder]**

Hier sind die allgemeinen Schritte, die Sie zur Implementierung von Classification-Regeln ergreifen:

| Schritt | Wo | Beschreibung |
|--- |--- |--- |
| Step 1 (Prerequisite): [Set up your classification schema](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_classifications). | [!UICONTROL Admin] &gt; [!UICONTROL Report Suites] &gt; [!UICONTROL Einstellungen bearbeiten] &gt; &lt; Traffic-Classifications oder Konversionsklassifizierungen &gt; | Wählen Sie eine Variable aus und definieren Sie die für die Variable zu verwendenden Classifications. <br>Für Variablen muss mindestens eine Classification-Spalte erstellt werden, bevor sie in Regeln genutzt werden können.<br>Sobald Classifications aktiviert sind, können Sie den Importeur und den Rule Builder verwenden, um bestimmte Werte zu klassifizieren. |
| Step 2: [Create a rule set](../../../components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL Admin] &gt; [!UICONTROL Classification Rule Builder] &gt; [!UICONTROL Regelsatz hinzufügen] | Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. |
| Schritt 3: Konfigurieren Sie Report Suites und Variablen. | [!UICONTROL Classification Rule Builder] &gt; &lt; Ihr Regelsatz &gt; | Wenden Sie den Regelsatz auf Report Suites und Variablen an. |
| Step 4: [Add classification rules to the set](../../../components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] &gt; &lt; Ihr Regelsatz &gt; | Ordnen Sie einer Classification eine Bedingung zu, und legen Sie die Aktion fest, die für die Regel ausgeführt werden soll.  Be familiar with the information in  [How Rules Are Processed](../../../components/c-classifications2/crb/classification-quickstart-rules.md). |
| Step 5: [Test a Classification Rule Set](../../../components/c-classifications2/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | Zum Testen der Regeln im Rahmen der Validierung bearbeiten Sie die Regeln im Entwurfsmodus. Im Entwurfsmodus können keine Regeln ausgeführt werden.<br>Dieser Schritt ist wichtig, wenn [reguläre Ausdrücke verwendet](../../../components/c-classifications2/crb/classification-quickstart-rules.md)werden. |
| Step 6: [Activate valid rules](../../../components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Sobald die Regeln gültig sind, aktivieren Sie den Regelsatz.  Bei Bedarf können Sie vorhandene Schlüssel überschreiben. Siehe [Verarbeitung der Regeln](../../../components/c-classifications2/crb/classification-quickstart-rules.md). |
| Step 7 (Optional): [Delete unwanted rules](../../../components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Löschen Sie die unerwünschten Regeln aus dem Satz.<br>Hinweis: Beim Löschen von Regeln werden die hochgeladenen klassifizierten Daten nicht gelöscht.  See  [Delete classification data](../../../components/c-classifications2/c-classifications-importer/t-delete-classification-data.md) if you need to delete classified data. |

>[!NOTE]
>
>Gruppen mit Berechtigungen zum Verwenden des Classification-Import-Tools können Classification-Regeln verwenden. See [How Rules Are Processed](../../../components/c-classifications2/crb/classification-quickstart-rules.md) for important processing information.

**Zusätzliche Ressourcen**

**Blog**: Weitere Informationen zu dieser Funktion finden Sie im Digital Marketing Blog: [Regelbasierte Klassifizierungen](https://blogs.adobe.com/digitalmarketing/analytics/rule-based-classifications-part-1-making-classifications-easier/?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+AdobeDigitalMarketing+%28Adobe+Digital+Marketing+Blog%29).

**Video**: Besuchen [Sie youtube](https://www.youtube.com/watch?v=6laI5SBXY-I) , um das [!UICONTROL Classifications-Übersichtsvideo] anzuzeigen.
