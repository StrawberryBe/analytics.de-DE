---
description: Erstellen Sie benutzerdefinierte Datumsbereiche in Analysis Workspace und speichern Sie sie als Zeitkomponenten.
keywords: Analysis Workspace
seo-description: Erstellen Sie benutzerdefinierte Datumsbereiche in Analysis Workspace und speichern Sie sie als Zeitkomponenten.
seo-title: Erstellen Sie benutzerdefinierte Datumsbereiche
solution: Analytics
title: Erstellen Sie benutzerdefinierte Datumsbereiche
topic: Reports and Analytics
uuid: c 8873 d 41-454 d -4 f 22-ad 1 f -38 cacec 5 a 3 bc
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Erstellen Sie benutzerdefinierte Datumsbereiche

Erstellen Sie benutzerdefinierte Datumsbereiche in Analysis Workspace und speichern Sie sie als Zeitkomponenten.

**[!UICONTROL Komponenten]** &gt; **[!UICONTROL Neuer Datumsbereich]**

Ein Datumsbereich wird auf der Bereichsebene angewendet. To add a date range to your project, click **Panels** &gt; *`<select panel>`*, and specify a new date range.

## Date range for "two months ago" {#section_C4109C57CB444BB2A79CC8082BD67294}

Der folgende benutzerdefinierte Datumsbereich zeigt den Bereich vor zwei Monaten mit einer Visualisierung der Sammeländerung, die eine Trendentwicklung anzeigt.

![](assets/date-range-two-months-ago.png)

Der benutzerdefinierte Datumsbereich wird in Ihrem Projekt oben auf dem Komponentenbereich für den [!UICONTROL Datumsbereich] angezeigt:

![](assets/date-range-panel-two-months-ago.png)

Sie können diesen benutzerdefinierten Datumsbereich auf eine Spalte neben einem benutzerdefinierten, monatlichen rollierenden Datumsbereich ziehen und die Voreinstellung für den letzten Monat für den Vergleich nutzen. Fügen Sie eine Visualisierung der Sammeländerung hinzu und wählen Sie die Gesamtsummen der einzelnen Spalten aus, um eine Trendentwicklung zu zeigen:

![](assets/date-range-two-months-table.png)

## Use a 7-day rolling date range {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

Ein Datumsbereich wird auf der Bereichsebene angewendet. Klicken Sie, um einen Datumsbereich zu Ihrem Projekt hinzuzufügen, auf **Aktionen** &gt; **Bereich hinzufügen** und geben Sie einen neuen Datumsbereich an.

Im Datumsbereich-Builder können Sie einen benutzerdefinierten Datumsbereich erstellen, der zusammen mit anderen Datumsbereichen im Komponentenbereich angezeigt wird.

Sie können z. B. einen Datumsbereich erstellen, der ein rollierendes Zeitfenster von 7 Tagen anzeigt, das vor einer Woche endet:

![](assets/create_date_range.png)

Verwenden Sie *`rolling daily`* zu trennen.

* Die Starteinstellung lautet *`current day minus 14 days`*.

* Die Endeinstellung lautet *`current day minus 7 days`*.

Dieser Datumsbereich kann eine Komponente sein, die Sie auf eine beliebige Freiform-Tabelle ziehen können.
