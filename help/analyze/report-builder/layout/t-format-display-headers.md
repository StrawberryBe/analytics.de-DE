---
description: Sie können Ihrem Bericht einen Namen geben und konfigurieren, wie die Zeilen- und Spaltenüberschriften angezeigt werden. Der Link „Formatoptionen“ ist für die Layouttypen „Pivot“ und „Benutzerdefiniert“ verfügbar.
title: Anzeigeüberschriften formatieren
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 99%

---


# Anzeigeüberschriften formatieren

Sie können Ihrem Bericht einen Namen geben und konfigurieren, wie die Zeilen- und Spaltenüberschriften angezeigt werden. Der Link „Formatoptionen“ ist für die Layouttypen „Pivot“ und „Benutzerdefiniert“ verfügbar.

1. Erstellen Sie im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 1] eine Anforderung.
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. Fügen Sie der Anforderung im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] Dimensionen und Metriken entsprechend Ihren Bedürfnissen hinzu.
1. Klicken Sie auf **[!UICONTROL Formatoptionen]**.
1. Konfigurieren Sie [!UICONTROL die Anzeigeoptionen]:

   | Element | Beschreibung |
   |--- |--- |
   | Berichtsname | Zeigt entweder den Namen des Berichtstyps an, der über den Baum in Schritt 1 des Berichtsassistenten ausgewählt wurde (z. B. [!DNL Traffic Report]), oder den im Feld [!DNL Name this Request] eingegebenen Namen. |
   | Filtert Parameter | Zeigt die Dimensionsfilter wie beispielsweise Suchfilter an |
   | Segment | Zeigt die Segmentparameter an |
   | Datenaktualität | Zeigt die Parameter für Datenaktualität an Beispiel:    Datenaktualität: Seitenansichten (vor 1,5 Stunden), Ausstiege (vor 30 Minuten); weitere Informationen zur aktuellen Datenverarbeitung finden Sie unter [Optionen](/help/analyze/report-builder/options.md). |

   Anzeigereihefolge: Wenn im [!UICONTROL Zeilentitel] (Schritt 2) ein Element enthalten ist, wird dies in der Anforderung zuerst angezeigt. Falls nicht, verwendet das System das erste vorhandene Element im Raster [!UICONTROL Spaltenbezeichnung]. Falls weder Zeilen- oder Spaltenelemente vorhanden sind, wird das erste Element im Raster [!UICONTROL Metriken] angezeigt.

   **Zeilen- und Spaltenüberschriften anzeigen:** Fügt eine Zeile und Spalte zur Anzeige dieser Elemente hinzu.

   In Version 3.11 konnte man eine Überschrift für jedes einzelne Element anzeigen. In Version 4 werden diese Elemente entweder alle oder gar nicht angezeigt. Wenn Sie eine Anforderung in Version 3.11 erstellt haben und sie in Version 4.x öffnen, werden Sie von ReportBuilder in Schritt 2 aufgefordert, den Zellenbereich für Elemente, die in einer Überschrift fehlen, um eine Zelle zu erweitern.

   **Überschriften in automatische Filterung von Excel ändern:** Nur verfügbar, wenn Zeilen- und Spaltenüberschriften angezeigt werden. Durch diese Einstellung wird in Excel ein automatischer Filter erstellt und an die Daten angehängt, die von Report Builder für die jeweilige Anforderung zurückgegeben werden.

   >[!NOTE]
   >
   >Excel unterstützt nur einen einzigen automatischen Filter pro Arbeitsblatt. Wenn Sie einen neuen automatischen Filter in einem Arbeitsblatt erstellen, das bereits einen automatischen Filter enthält, gibt Excel keine Warnung aus, dass der vorhandene automatische Filter ersetzt wird.

   **Automatische Gliederung durchführen:** Wandelt die von Report Builder ausgegebenen Daten von einer Listen- in eine Baumansicht um.

   **Diese Anforderung benennen:** Hier können Sie einen benutzerdefinierten Namen für die Anforderung eingeben oder den in Schritt 1 ausgewählten Standardnamen verwenden. Dieser Name wird als [!UICONTROL Berichtname] im [!UICONTROL Anforderungs-Manager] angezeigt. Siehe [Eine Anforderung benennen](/help/analyze/report-builder/layout/name-a-request.md).

1. Klicken Sie auf **[!UICONTROL OK]**.
