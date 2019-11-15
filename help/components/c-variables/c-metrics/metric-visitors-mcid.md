---
description: Verfügbar in Analysis Workspace und in Segment Builder.
title: Besucher mit Experience Cloud ID
uuid: 47ebd3d6-a921-4e51-ac7a-b8d5fb9565e0
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Besucher mit Experience Cloud ID

Verfügbar in Analysis Workspace und in Segment Builder.

Zeigt die Anzahl der Benutzer, die über eine Experience Cloud ID verfügen. Sie können verstehen, auf welchen Seiten der Identitätsdienst bereitgestellt ist und wie viele Besucher mit anderen Experience Cloud-Lösungen geteilt werden können. Sie können diese Metrik auch in Segmenten verwenden, die für die Experience Cloud freigegeben sind.

>[!IMPORTANT]
>
>For this metric to appear, you have to have the [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/) running for the report suite.

## Debugging Ihres Experience Cloud ID-Setups {#section_679E62142A3E46548FF8FBDA46568005}

The [!UICONTROL Visitors with Experience Cloud ID] metric is a useful metric in Adobe Analytics intended to help you find and debug your [!UICONTROL Identity Service]setup. Die Metrik ist ein Zähler der Besucher in einer Report Suite, denen vom Identitätsdienst eine Experience Cloud ID zugewiesen wurde. Diese Metrik kann sehr hilfreich sein, wenn Sie herausfinden möchten, warum bestimmte Experience Cloud-Integrationen möglicherweise nicht so viele Besucher wie erwartet freigeben. Zudem können Sie damit Bereiche Ihrer Site identifizieren, für die die MCID möglicherweise noch nicht bereitgestellt wurde.

Wenn Sie die Metrik „Besucher mit Experience Cloud ID“ nutzen möchten, ziehen Sie sie einfach als Metrik in einen beliebigen Bericht, beispielsweise in diesen [!UICONTROL Seiten]-Bericht:

![](assets/metric-mcvid1.png)

Beachten Sie Folgendes: In diesem Beispiel weist jede Seite eine identische Anzahl an Unique Visitors und Besuchern mit Experience Cloud ID auf. Die Gesamtanzahl an Unique Visitors ist dabei größer als die Gesamtanzahl an Besuchern mit Experience Cloud ID. Um die Seiten zu finden, für die die MCID nicht für alle Besucher festgelegt ist, [erstellen Sie eine berechnete Metrik](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_build_metrics.html) anhand dieser Definition:

![](assets/metric-mcvid2.png)

Wenn Sie die berechnete Metrik zum Bericht hinzufügen, können Sie den Seiten-Bericht so sortieren, dass die Seiten mit der größten Anzahl an Besuchern ohne MCID oben angezeigt werden:

![](assets/metric-mcvid3.png)

Jetzt können Sie schnell erkennen, dass die Seiten "Produktsymbole"nicht ordnungsgemäß mit dem Identitätsdienst implementiert sind und so schnell wie möglich aktualisiert werden sollten. Ein ähnlicher Bericht kann für beliebige Dimensionstypen wie beispielsweise den Browsertyp, den Sitebereich oder Content-Typen erstellt werden.

Sobald Sie Seiten identifiziert haben, die Besucher ohne MCID haben, sollten Sie in der Lage sein, dies an Ihr Implementierungsteam zurückzunehmen, damit diese Seiten repariert werden können.

In manchen Fällen stellen Sie möglicherweise fest, dass eine geringe Anzahl an MCIDs für einige Besucher nicht festgelegt wurde, obwohl der MCID-Dienst auf der Seite implementiert wurde. Dies liegt meist an einer häufigen Fehlkonfiguration der JavaScript- oder DTM-Konfiguration von Analytics, bei der die AppMeasurement-Funktion vor dem Bereitstellen einer Report Suite aufgerufen wird. Stellen Sie sicher, dass der [Core-AppMeasurement-Code ordnungsgemäß eingefügt wird](https://marketing.adobe.com/resources/help/en_US/sc/implement/dtm/t_appmeasurement-code.html), um dies zu vermeiden.

Beachten Sie, dass alle Segmente, die auf der Seite "Produkt-Schnellansichten"(wie oben gezeigt) basieren und die Sie mit der Experience Cloud freigeben, wahrscheinlich eine sehr niedrige Übereinstimmungsrate mit anderen Experience Cloud-Lösungen aufweisen. Um die MCID-Abdeckung für ein beliebiges Segment zu überprüfen, können Sie einen Bericht erstellen, indem Sie wie folgt vorgehen:

![](assets/metric-mcvid4.png)

In dieser Tabelle, in der die Anzahl der individuellen Besucher mit der Anzahl der Besucher mit einer Experience Cloud ID verglichen wird, ist leicht zu erkennen, dass "Segment 1"keine 100%ige MCID-Abdeckung aufweist, während dies bei "Segment 2"der Fall ist. Dies bedeutet Folgendes: Wenn Sie Segment 1 in der Experience Cloud freigeben, wären nur 2.186 der insgesamt 3.859 Besucher für die Freigabe qualifiziert.
