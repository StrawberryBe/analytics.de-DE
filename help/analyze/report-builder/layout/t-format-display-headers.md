---
description: Sie können Ihrem Bericht einen Namen geben und konfigurieren, wie die Zeilen- und Spaltenüberschriften angezeigt werden. Der Link „Formatoptionen“ ist für die Layouttypen „Pivot“ und „Benutzerdefiniert“ verfügbar.
title: Anzeigeüberschriften formatieren
topic: Report builder
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Anzeigeüberschriften formatieren

Sie können Ihrem Bericht einen Namen geben und konfigurieren, wie die Zeilen- und Spaltenüberschriften angezeigt werden. Der Link „Formatoptionen“ ist für die Layouttypen „Pivot“ und „Benutzerdefiniert“ verfügbar.

1. Erstellen Sie eine Anforderung auf der [!UICONTROL Request Wizard: Step 1].
1. Klicken Sie auf **[!UICONTROL Next]**.
1. On the [!UICONTROL Request Wizard: Step 2] form, add dimensions and metrics data to the request, as desired.
1. Klicken Sie auf **[!UICONTROL Format Options]**.
1. Configure the [!UICONTROL Display] options:

   | Element | Beschreibung |
   |--- |--- |
   | Berichtsname | Zeigt entweder den Namen des Berichtstyps an, der über den Baum in Schritt 1 des Berichtsassistenten ausgewählt wurde (z. B. [!DNL Traffic Report]), oder den im Feld [!DNL Name this Request] eingegebenen Namen. |
   | Filtert Parameter | Zeigt die Dimensionsfilter wie beispielsweise Suchfilter an |
   | Segment | Zeigt die Segmentparameter an |
   | Datenaktualität | Zeigt die Parameter für Datenaktualität an Beispiel:    Datenaktualität: Seitenansichten (vor 1,5 Stunden), Ausstiege (vor 30 Minuten); weitere Informationen zur aktuellen Datenverarbeitung finden Sie unter [Optionen](/help/analyze/report-builder/options.md). |

   Regarding display order, if the [!UICONTROL Row Label] grid (on Step 2) contains an item, it is displayed first in the request. If not, the system uses the first item present in the [!UICONTROL Column Label] grid. If no row or column items exist, the first item in the [!UICONTROL Metrics] grid is displayed.

   **Zeilen- und Spaltenüberschriften anzeigen:** Fügt eine Zeile und Spalte zur Anzeige dieser Elemente hinzu.

   In Version 3.11 konnte man eine Überschrift für jedes einzelne Element anzeigen. In Version 4 werden diese Elemente entweder alle oder gar nicht angezeigt. Wenn Sie eine Anforderung in Version 3.11 erstellt haben und sie in Version 4.x öffnen, werden Sie von ReportBuilder in Schritt 2 aufgefordert, den Zellenbereich für Elemente, die in einer Überschrift fehlen, um eine Zelle zu erweitern.

   **Überschriften in automatische Filterung von Excel ändern:** Nur verfügbar, wenn Zeilen- und Spaltenüberschriften angezeigt werden. Durch diese Einstellung wird in Excel ein automatischer Filter erstellt und an die Daten angehängt, die von Report Builder für die jeweilige Anforderung zurückgegeben werden.

   >[!NOTE]
   >
   >Excel unterstützt nur einen einzigen automatischen Filter pro Arbeitsblatt. Wenn Sie einen neuen automatischen Filter in einem Arbeitsblatt erstellen, das bereits einen automatischen Filter enthält, gibt Excel keine Warnung aus, dass der vorhandene automatische Filter ersetzt wird.

   **Automatische Gliederung durchführen:** Wandelt die von Report Builder ausgegebenen Daten von einer Listen- in eine Baumansicht um.

   **Diese Anforderung benennen:** Hier können Sie einen benutzerdefinierten Namen für die Anforderung eingeben oder den in Schritt 1 ausgewählten Standardnamen verwenden. Dieser Name wird als [!UICONTROL Report] Name in der [!UICONTROL Request Manager]. See [Name a Request](/help/analyze/report-builder/layout/name-a-request.md).

1. Klicken Sie auf **[!UICONTROL OK]**.
