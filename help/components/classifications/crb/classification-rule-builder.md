---
description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
subtopic: Classifications
title: Classification Rule Builder-Workflow
feature: Admin Tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
exl-id: cdb20dcc-0635-4d5e-9c54-f102d17a0a3d
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 97%

---

# Classification Rule Builder-Workflow

Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.

## Wichtiger Hinweis vor Beginn

Beachten Sie Folgendes, bevor Sie mit der Verwendung von Classification-Regeln beginnen:

* Classification Rule Builder (CRB) unterstützt keine Unterklassifizierungen.
* Unser aktuelles Classification-System kann bis zu 10 Millionen Zeilen gleichzeitig exportieren.
* Wenn CRB einen Export anfordert, ruft er sowohl klassifizierte als auch nicht klassifizierte Werte ab, wobei nicht klassifizierte Werte am Ende des Exports stehen. Das bedeutet, dass man im Laufe der Zeit 10 Millionen klassifizierte Werte auflisten könnte, ohne jemals zu den nicht klassifizierten Werten zu gelangen.
* Da die Architektur so eingerichtet ist, dass der CRB Werte von Servern mit der Anzahl „n“ abrufen kann, kann dies zu Inkonsistenzen dahingehend führen, welche Server aufgenommen werden und in welcher Reihenfolge. Aus diesem Grund ist es sehr schwierig, nicht klassifizierte Werte zu erhalten.

Hier finden Sie die **Lösung** für diejenigen, die mehr als 10 Millionen klassifizierte Werte für eine Dimension haben: Sie müssen nicht klassifizierte Werte per FTP in 10 Millionen Stapel exportieren und manuell klassifizieren.

## Erste Schritte mit Classification-Regeln {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Für die Implementierung von Classification-Regeln gelten die nachfolgenden allgemeinen Schritte:

| Schritt | Wo | Beschreibung |
|--- |--- |--- |
| Schritt 1 (Voraussetzung): [Classification-Schema einrichten](https://docs.adobe.com/content/help/de-DE/analytics/components/classifications/c-classifications.html). | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Einstellungen bearbeiten] > &lt;Traffic-Klassifizierungen oder Konversionsklassifizierungen> | Wählen Sie eine Variable aus und definieren Sie die für die Variable zu verwendenden Classifications. <br>Für Variablen muss mindestens eine Classification-Spalte erstellt werden, bevor sie in Regeln genutzt werden können.<br>Sobald Classifications aktiviert sind, können Sie den Importeur und den Rule Builder verwenden, um bestimmte Werte zu klassifizieren. |
| Schritt 2: [Regelsatz erstellen](/help/components/classifications/crb/classification-rule-set.md). | [!UICONTROL Admin] > [!UICONTROL Classification Rule Builder] > [!UICONTROL Regelsatz hinzufügen] | Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. |
| Schritt 3: Report Suites und Variablen konfigurieren. | [!UICONTROL Classification Rule Builder] >  &lt;Ihr Regelsatz> | Wenden Sie den Regelsatz auf Report Suites und Variablen an. |
| Schritt 4: [Classification-Regeln zum Satz hinzufügen](/help/components/classifications/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] >  &lt;Ihr Regelsatz> | Ordnen Sie einer Classification eine Bedingung zu, und legen Sie die Aktion fest, die für die Regel ausgeführt werden soll.  Machen Sie sich mit den Informationen unter [Verarbeitung der Regeln](/help/components/classifications/crb/classification-quickstart-rules.md) vertraut. |
| Schritt 5: [Testen eines Klassifizierungsregelsatzes](/help/components/classifications/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | Zum Testen der Regeln im Rahmen der Validierung bearbeiten Sie die Regeln im Entwurfsmodus. Im Entwurfsmodus können keine Regeln ausgeführt werden.<br>Dieser Schritt ist bei der Verwendung [regulärer Ausdrücke](/help/components/classifications/crb/classification-quickstart-rules.md) wichtig. |
| Schritt 6: [Gültige Regeln aktivieren](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Sobald die Regeln gültig sind, aktivieren Sie den Regelsatz.  Bei Bedarf können Sie vorhandene Schlüssel überschreiben. Siehe [Verarbeitung der Regeln](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Schritt 7 (Optional): [Unerwünschte Regeln löschen](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Löschen Sie die unerwünschten Regeln aus dem Satz.<br>Hinweis: Beim Löschen von Regeln werden die hochgeladenen klassifizierten Daten nicht gelöscht.  Informationen zum Löschen klassifizierter Daten finden Sie unter [Löschen von Classification-Daten](/help/components/classifications/importer/t-delete-classification-data.md). |

>[!NOTE]
>
>Gruppen mit der Berechtigung zum Nutzen des Classification-Importtools können Classification-Regeln verwenden. Wichtige Verarbeitungsinformationen finden Sie unter [Verarbeitung der Regeln](/help/components/classifications/crb/classification-quickstart-rules.md).

**Zusätzliche Ressourcen**

**Blog**: Weitere Informationen zu dieser Funktion finden Sie im Digital Marketing Blog: [Regelbasierte Klassifizierungen](https://theblog.adobe.com/rule-based-classifications-part-1-making-classifications-easier/).

**Video**: Ansicht des Videos  [&quot;](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/components/classifications/overview-of-classifications.html) Übersicht über Klassifizierungen&quot;.
