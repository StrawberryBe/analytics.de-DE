---
description: Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden jetzt in Schritt 1 des Anforderungs-Assistenten als Dimensionen aufgelistet und können als Report Builder-Anforderungen importiert werden.
title: Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren
feature: Report Builder
role: User, Admin
exl-id: 19813950-2495-4a75-aacb-587b59bf2484
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 65%

---

# Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren

Alle mit Lesezeichen markierten Berichte und Dashboard-Berichte werden jetzt in Schritt 1 des Anforderungs-Assistenten als Dimensionen aufgelistet und können als Report Builder-Anforderungen importiert werden.

Wenn Sie einen mit Lesezeichen markierten Bericht auswählen, belegt der Anforderungs-Assistent alle Dimensionen und Metriken, die diesen mit Lesezeichen markierten Bericht definieren. Der Datumsbereich, die Granularität und das ausgewählte Segment werden ebenfalls basierend auf dem ausgewählten Lesezeichen aktualisiert.

So werden in Schritt 1 des Anforderungs-Assistenten ein Dashboard und die zugehörigen Kurzberichte angezeigt:

![Screenshot mit dem Anforderungs-Assistenten Schritt 1 von 2, in dem die Option Dashboards abrufen und Lesezeichen abrufen hervorgehoben wird.](assets/import_dashboard_reportlet.png)

Wenn Sie auf **[!UICONTROL Ihre Dashboards abrufen]** oder auf **[!UICONTROL Ihre Lesezeichen abrufen]** klicken, werden Ihre vorhandenen Dashboard- und/oder Lesezeichendaten abgerufen und in das Arbeitsblatt eingefügt.

>[!NOTE]
>
>Es werden ausschließlich Daten importiert. Wenn das Lesezeichen ein Diagramm enthält oder der Dashboard-Kurzbericht nur aus einem Diagramm besteht, werden nur die Daten importiert, auf denen das Diagramm basiert.

Sobald Sie eine Anforderung durch Importieren eines Dashboard-Kurzberichts (bzw. eines Lesezeichens) erstellt haben, wird die Anforderung mit der primären Dimension des Kurzberichts (bzw. des Lesezeichens) verknüpft. Das führt dazu, dass in der Baumansicht nicht mehr der Knoten des Dashboard-Kurzberichts (bzw. des Lesezeichens) ausgewählt wird, wenn Sie eine Anforderung bearbeiten, sondern die primäre Dimension.

