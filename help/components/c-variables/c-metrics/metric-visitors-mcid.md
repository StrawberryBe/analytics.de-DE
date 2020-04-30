---
description: Verfügbar in Analysis Workspace und in Segment Builder.
title: Besucher mit Experience Cloud ID
uuid: 47ebd3d6-a921-4e51-ac7a-b8d5fb9565e0
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Besucher mit Experience Cloud ID

Verfügbar in Analysis Workspace und in Segment Builder.

Zeigt die Anzahl der Benutzer, die über eine Experience Cloud ID verfügen. Sie ermöglicht Ihnen, zu verstehen, auf welchen Seiten der Identity Service bereitgestellt ist und wie viele Besucher mit anderen Experience Cloud-Lösungen geteilt werden können. Sie können diese Metrik auch in Segmenten verwenden, die für die Experience Cloud freigegeben sind.

>[!IMPORTANT]
>
>Der [Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) muss für die Report Suite ausgeführt werden, damit diese Metrik angezeigt wird.

## Debugging Ihres Experience Cloud ID-Setups {#section_679E62142A3E46548FF8FBDA46568005}

Die [!UICONTROL Visitors with Experience Cloud ID] Metrik ist eine nützliche Metrik in Adobe Analytics, mit der Sie Ihre [!UICONTROL Identity Service]Einrichtung finden und debuggen können. Bei der Metrik handelt es sich um eine Zählung der Anzahl an Besuchern in einer Report Suite, die vom Identity Service eine Experience Cloud ID zugewiesen bekommen haben. Diese Metrik kann sehr hilfreich sein, wenn Sie herausfinden möchten, warum bestimmte Experience Cloud-Integrationen möglicherweise nicht so viele Besucher wie erwartet freigeben. Zudem können Sie damit Bereiche Ihrer Site identifizieren, für die die MCID möglicherweise noch nicht bereitgestellt wurde.

To use the Visitors with Experience Cloud ID metric, simply drag it in to any report as a metric, such as this [!UICONTROL Pages] report:

![](assets/metric-mcvid1.png)

Beachten Sie Folgendes: In diesem Beispiel weist jede Seite eine identische Anzahl an Unique Visitors und Besuchern mit Experience Cloud ID auf. Die Gesamtanzahl an Unique Visitors ist dabei größer als die Gesamtanzahl an Besuchern mit Experience Cloud ID. Um die Seiten zu finden, für die die MCID nicht für alle Besucher festgelegt ist, [erstellen Sie eine berechnete Metrik](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) anhand dieser Definition:

![](assets/metric-mcvid2.png)

Wenn Sie die berechnete Metrik zum Bericht hinzufügen, können Sie den Seiten-Bericht so sortieren, dass die Seiten mit der größten Anzahl an Besuchern ohne MCID oben angezeigt werden:

![](assets/metric-mcvid3.png)

Nun sehen Sie auf einen Blick, dass die Seiten zu Produktschnellansichten nicht ordnungsgemäß in den Identity Service implementiert wurden und so bald wie möglich aktualisiert werden sollten. Ein ähnlicher Bericht kann für beliebige Dimensionstypen wie beispielsweise den Browsertyp, den Sitebereich oder Content-Typen erstellt werden.

Sobald Sie Seiten mit Besuchern ohne MCID identifiziert haben, sollten Sie diese Ihrem Implementierungsteam melden, damit das Team die entsprechenden Seiten korrigieren kann.

In manchen Fällen stellen Sie möglicherweise fest, dass eine geringe Anzahl an MCIDs für einige Besucher nicht festgelegt wurde, obwohl der MCID-Dienst auf der Seite implementiert wurde. Dies liegt meist an einer häufigen Fehlkonfiguration der JavaScript- oder DTM-Konfiguration von Analytics, bei der die AppMeasurement-Funktion vor dem Bereitstellen einer Report Suite aufgerufen wird. Stellen Sie sicher, dass der [Core-AppMeasurement-Code ordnungsgemäß eingefügt wird](https://docs.adobe.com/content/help/en/analytics/implementation/other/dtm/analytics-tool/t-appmeasurement-code.html), um dies zu vermeiden.

Beachten Sie, dass alle Segmente auf Basis der Seite zu Produktschnellansichten (wie oben gezeigt), die Sie in der Experience Cloud freigeben, wahrscheinlich einen sehr geringen Übereinstimmungswert mit anderen Experience Cloud-Lösungen haben werden. Um die MCID-Abdeckung für ein beliebiges Segment zu überprüfen, können Sie einen Bericht erstellen, indem Sie wie folgt vorgehen:

![](assets/metric-mcvid4.png)

Aus dieser Tabelle, in der die Anzahl an Unique Visitors mit der Anzahl an Besuchern mit Experience Cloud ID verglichen wird, können Sie leicht ablesen, dass das Segment 1 keine 100-prozentige MCID-Abdeckung aufweist, wohingegen das Segment 2 dies tut. Dies bedeutet Folgendes: Wenn Sie Segment 1 in der Experience Cloud freigeben, wären nur 2.186 der insgesamt 3.859 Besucher für die Freigabe qualifiziert.
