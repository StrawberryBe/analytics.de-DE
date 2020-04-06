---
description: Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden ab sofort in Schritt 1 des Anforderungs-Assistenten als Dimensionen gelistet und können als Report Builder-Anforderungen importiert werden.
title: Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren
topic: Report builder
uuid: 0fdbdb2e-5db7-4f64-b571-23482ba3606d
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren

Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden ab sofort in Schritt 1 des Anforderungs-Assistenten als Dimensionen gelistet und können als Report Builder-Anforderungen importiert werden.

Wenn Sie einen mit Lesezeichen versehenen Bericht auswählen, füllt der Anforderungs-Assistent alle Dimensionen und Metriken, die diesen mit Lesezeichen versehenen Bericht definieren. Der Datumsbereich, die Granularität und das ausgewählte Segment werden ebenfalls anhand des ausgewählten Lesezeichens aktualisiert.

So zeigt der Anforderungs-Assistent Schritt 1 ein Dashboard und seine Reportlets an:

![](assets/import_dashboard_reportlet.png)

Wenn Sie auf **[!UICONTROL Retrieve your Dashboards]** oder **[!UICONTROL Retrieve your Bookmarks]** klicken, werden Ihre vorhandenen Dashboard- und/oder Lesezeichendaten abgerufen und in das Arbeitsblatt eingefügt.

>[!NOTE] In Report Builder ist die Liste der verfügbaren Dashboards und Lesezeichen auf den Benutzer und die Dashboards beschränkt, die für die Report Suite gelten, die Sie in Schritt 1 des Assistenten ausgewählt haben. In Marketing Reports &amp; Analysen hingegen haben Sie Zugriff auf alle Lesezeichen und Dashboards, auf die Sie zugreifen können, unabhängig davon, welche Report Suites diese Dashboards und Lesezeichen verwenden.

>[!NOTE] Es werden ausschließlich Daten importiert. Wenn das Lesezeichen ein Diagramm enthält oder der Dashboard-Kurzbericht nur aus einem Diagramm besteht, werden nur die Daten importiert, auf denen das Diagramm basiert.

Nachdem Sie eine Anforderung durch Importieren eines Dashboard-Reportlets (oder eines Lesezeichens) erstellt haben, wird die Anforderung dann der primären Dimension des Reportlets (oder Lesezeichens) zugeordnet. Wenn Sie daher die Anforderung bearbeiten, wählt die Tree-Ansicht nicht mehr den Dashboard-Reportlet-Baum-Ansicht-Knoten (oder Lesezeichenknoten) aus: sondern wählt stattdessen seine primäre Dimension aus.

Mithilfe des importierten Bookmarklet werden die Report Suite, das ausgewählte Segment, die Dimension und die ausgewählten Metriken korrekt festgelegt, und zwar entsprechend derselben Parameter, die für das Lesezeichen zu Reports &amp; Analytics gelten.

>[!IMPORTANT]
>
>Für den Datumsbereich wird derselbe Datumsbereich festgelegt, jedoch als statischer Datumsbereich – auch wenn es sich bei diesem Datumsbereich im Lesezeichen zu Reports &amp; Analytics um einen rollierenden Datumsbereich handelt.

