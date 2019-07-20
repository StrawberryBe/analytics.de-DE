---
description: Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden ab sofort in Schritt 1 des Anforderungs-Assistenten als Dimensionen gelistet und können als ReportBuilder-Anforderungen importiert werden.
seo-description: Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden ab sofort in Schritt 1 des Anforderungs-Assistenten als Dimensionen gelistet und können als ReportBuilder-Anforderungen importiert werden.
seo-title: Mit Lesezeichen markierte Berichte und Dashboard-Reportlets importieren
solution: Analytics
title: Mit Lesezeichen markierte Berichte und Dashboard-Reportlets importieren
topic: ReportBuilder
uuid: 0 fdbdb 2 e -5 db 7-4 f 64-b 771-23482 ba 3606 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Mit Lesezeichen markierte Berichte und Dashboard-Reportlets importieren

Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden ab sofort in Schritt 1 des Anforderungs-Assistenten als Dimensionen gelistet und können als ReportBuilder-Anforderungen importiert werden.

Wenn Sie einen mit Lesezeichen markierten Bericht auswählen, belegt der Anforderungs-Assistent alle Dimensionen und Metriken, die diesen mit Lesezeichen markierten Bericht definieren. Der Datumsbereich, die Granularität und das ausgewählte Segment werden ebenfalls auf Basis des ausgewählten Lesezeichens aktualisiert.

So werden in Schritt 1 des Anforderungs-Assistenten ein Dashboard und die zugehörigen Kurzberichte angezeigt:

![](assets/import_dashboard_reportlet.png)

When you click **[!UICONTROL Retrieve your Dashboards]** or **[!UICONTROL Retrieve your Bookmarks]**, your existing dashboard and/or bookmark data is retrieved and pasted in the worksheet.

>[!NOTE]
>
>In Reportbuilder ist die Liste der verfügbaren Dashboards und Lesezeichen auf den Benutzer beschränkt, aber auch auf diejenigen, die für die Report Suite gelten, die Sie in Schritt 1 des Assistenten ausgewählt haben. In Marketing Reports &amp; Analysen hingegen haben Sie Zugriff auf alle Lesezeichen und Dashboards, auf die Sie zugreifen können, unabhängig davon, welche Report Suites diese Dashboards und Lesezeichen verwenden.

>[!NOTE]
>
>Es werden nur Daten importiert. Wenn das Lesezeichen ein Diagramm enthält oder das Dashboard-Reportlet aus einem Diagramm besteht, werden nur die Daten importiert, die zum Ausfüllen des Diagramms verwendet werden.

Sobald Sie eine Anforderung durch Importieren eines Dashboard-Kurzberichts (bzw. eines Lesezeichens) erstellt haben, wird die Anforderung mit der primären Dimension des Kurzberichts (bzw. des Lesezeichens) verknüpft. Das führt dazu, dass in der Baumansicht nicht mehr der Knoten des Dashboard-Kurzberichts (bzw. des Lesezeichens) ausgewählt wird, wenn Sie eine Anforderung bearbeiten, sondern die primäre Dimension.

Mithilfe des importierten Bookmarklet werden die Report Suite, das ausgewählte Segment, die Dimension und die ausgewählten Metriken korrekt festgelegt, und zwar entsprechend derselben Parameter, die für das Lesezeichen zu Reports &amp; Analysen gelten.

>[!IMPORTANT]
>
>Der Datumsbereich wird auf denselben Datumsbereich festgelegt, aber als statischer Datumsbereich - auch wenn dieser Datumsbereich im Lesezeichen Reports &amp; Analysen ein rollierender Datumsbereich war.

