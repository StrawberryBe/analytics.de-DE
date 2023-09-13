---
description: Der Anforderungs-Manager ermöglicht es Ihnen, Anforderungen anzuzeigen, zu duplizieren und neu zu priorisieren.
title: Verwalten von Data Warehouse-Anforderungen
feature: Data Warehouse
uuid: cdeb764f-56f9-43ec-9228-8ed5a2b58909
exl-id: a399d366-8402-4f4f-9b9f-14b218cd074a
source-git-commit: 8507ce3f7e4d09956ad88c2be5335b68c8e3b8a0
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 18%

---

# Verwalten von Data Warehouse-Anforderungen

{{release-limited-testing}}

>[!NOTE]
>
>Wenn Ihr Unternehmen noch nicht über das neue Data Warehouse-Erlebnis verfügt, das bald für alle Kunden verfügbar sein wird, verwenden Sie die Informationen unter [Data Warehouse-Anforderungen verwalten (altes Erlebnis)](#manage-data-warehouse-requests-old-experience)


Sie können Data Warehouse-Anfragen verwalten, die Sie gestellt haben. In den folgenden Abschnitten werden die Aktivitäten beschrieben, die Sie bei der Verwaltung von Anforderungen durchführen können. <!-- just those you have made? I think you can see other people's requests (you can filter by them). What can you do with other people's requests? Just view them?-->

## Anforderungen anzeigen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

   Auf der Data Warehouse-Seite werden alle Anfragen angezeigt, die Sie gestellt haben. <!-- just those you have made? -->Daten werden in jeder Spalte angezeigt. Sie können [Konfigurieren der Spalten](#configure-columns) sichtbar sind.

   <!-- add screenshot of main page -->

<!-- describe columns? -->

1. (Optional) Klicken Sie auf den Anforderungsnamen, um ein Dialogfeld mit den folgenden Informationen anzuzeigen: <!-- Check this -->

   * Bei Beginn der Verarbeitung einer Anforderung

   * Rate Limited: Ihr Unternehmen führt zu viele Data Warehouse-Anfragen aus. Die Anfrage wird angehalten, bis andere Datenanforderungen abgeschlossen sind.

## Anforderungen bearbeiten

Beachten Sie beim Bearbeiten von Anforderungen Folgendes:

* Es können nur Anforderungen bearbeitet werden, die für die Ausführung nach einem Zeitplan konfiguriert sind.

* Es können nicht alle mit der Anfrage verknüpften Felder bearbeitet werden. Felder, die nicht bearbeitet werden können, sind abgeblendet.

So bearbeiten Sie eine geplante Anforderung:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, die Sie bearbeiten möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Bearbeiten**] aus.

1. Bearbeiten Sie die Anforderung wie gewünscht. Eingestellte Konfigurationsoptionen können nicht bearbeitet werden.

   Informationen zu den einzelnen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Auswählen [!UICONTROL **Änderungen speichern**].

## Verlauf einer Anforderung anzeigen

Sie können den Verlauf aller ausgeführten Berichte anzeigen.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, deren Verlauf Sie anzeigen möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Auswählen [!UICONTROL **Verlauf anzeigen**].

## Anforderungen kopieren

Beim Kopieren einer Anforderung werden alle Konfigurationsoptionen aus der ursprünglichen Anforderung kopiert.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, die Sie kopieren möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Auswählen [!UICONTROL **Kopieren**].

   Die Seite Data Warehouse-Anfrage kopieren wird angezeigt. Alle Konfigurationsoptionen werden aus der ursprünglichen Anforderung kopiert.

1. Aktualisieren Sie alle Konfigurationsoptionen, die mit der Anfrage verknüpft sind.

   Informationen zu den einzelnen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Auswählen [!UICONTROL **Änderungen speichern**].

## Anfragen abbrechen

Es können nur Anforderungen abgebrochen werden, die für die Ausführung nach einem Zeitplan konfiguriert sind.

So brechen Sie eine geplante Anforderung ab:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, die Sie bearbeiten möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Auswählen [!UICONTROL **Abbrechen**].

   Die Anfrage wird nicht mehr zur geplanten Zeit ausgeführt.

## Spalten konfigurieren

Sie können konfigurieren, welche Informationen für jede Anforderung angezeigt werden, indem Sie Spalten hinzufügen oder entfernen.

1. Wählen Sie die **Spalten konfigurieren** rechts oben auf der Data Warehouse-Seite.

   ![Spalten konfigurieren](assets/dw-configure-columns.png)

   Die folgenden Spalten sind verfügbar:

   | Spalte verfügbar | Beschreibung |
   |---------|----------|
   | Anfragename | Der Name der Person, die die Anfrage erstellt hat. |
   | Report Suite | Die mit der Anforderung verknüpfte Report Suite. |
   | Angefordert von | Der Benutzer, der die Anforderung erstellt hat. |
   | Datum der Anfrage | Das Datum, an dem die Anfrage gestellt wurde. |
   | Status | Die folgenden Status sind verfügbar:<ul><li><p>**Abgeschlossen**: Die Anfrage wurde erfolgreich ausgeführt.</p></li><li><p>**Abgebrochen**: Die Anfrage wurde vom Benutzer abgebrochen.</p></li><li><p>**Geplant**: Die Anforderung ist so konfiguriert, dass sie nach einem Zeitplan ausgeführt wird.</p></li><!-- Are there other statuses? Failed? --> |

   {style="table-layout:auto"}

1. Stellen Sie sicher, dass alle Spalten ausgewählt sind, die angezeigt werden sollen. Ausgewählte Spalten werden auf der Data Warehouse-Seite angezeigt und zeigen die entsprechenden Informationen an.

## Anforderungen filtern und sortieren

1. Wählen Sie die **Filter** in der linken Leiste der Data Warehouse-Seite.

   ![Anforderungen filtern](assets/dw-filter.png)

1. Erweitern Sie die [!UICONTROL **Report Suites**], [!UICONTROL **Inhaber**] oder [!UICONTROL **Status**] und wählen Sie aus, wie Sie die Anforderungen filtern möchten.

## Suchen nach Anforderungen

1. Geben Sie im Suchfeld oben auf der Data Warehouse-Seite den Anforderungsnamen an, den Sie anzeigen möchten.

   Anforderungen werden bei der Eingabe gefiltert.

## Data Warehouse-Anforderungen verwalten (altes Erlebnis)

>[!NOTE]
>
>Die folgenden Informationen gelten nur, wenn Ihr Unternehmen noch nicht über das neue Data Warehouse-Erlebnis verfügt, das demnächst für alle Analytics-Kunden verfügbar sein wird.


Der Anforderungs-Manager ermöglicht es Ihnen, Anforderungen anzuzeigen, zu duplizieren und neu zu priorisieren.

Wählen Sie in Data Warehouse die Registerkarte **[!UICONTROL Anforderungs-Manager]** aus.

Die Arbeit in dieser Registerkarte ermöglicht es Ihnen,

* aktuelle Berichtsanforderungen nach Berichtsnamen, angewendetem Segment, anfordernder Person, Anforderungsdatum und -status anzuzeigen.
* Anforderungen zu duplizieren. Klicken Sie neben der Anforderung auf **[!UICONTROL Duplizieren]**.

  >[!NOTE]
  >
  >Diese Aktion dupliziert lediglich die Anforderung, jedoch nicht den Zeitplan bzw. die Lieferdetails.

* Berichte nach Berichtsnamen oder Anmeldenamen der anfordernden Person zu suchen.
* Berichte durch Ziehen und Ablegen an einer neuen Position in der Warteschlange neu zu priorisieren.
* Möchten Sie es anzeigen, wenn eine Anfrage verarbeitet wird, klicken Sie auf die ID einer geplanten Anfrage und prüfen Sie das sich öffnende Popup.

Klicken Sie auf einen Auftrag, um einzelne Anforderungen für diesen Auftrag anzuzeigen.

* Rate Limited: Ihr Unternehmen führt zu viele Data Warehouse-Anfragen aus. Die Anfrage wird angehalten, bis andere Datenanforderungen abgeschlossen sind.