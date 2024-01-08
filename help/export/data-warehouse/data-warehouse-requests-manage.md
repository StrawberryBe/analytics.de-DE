---
description: Der Anforderungs-Manager ermöglicht es Ihnen, Anforderungen anzuzeigen, zu duplizieren und neu zu priorisieren.
title: Verwalten von Data Warehouse-Anforderungen
feature: Data Warehouse
uuid: cdeb764f-56f9-43ec-9228-8ed5a2b58909
exl-id: a399d366-8402-4f4f-9b9f-14b218cd074a
source-git-commit: abfc67abdba5e35b12a583fafe9a6e42192af631
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 5%

---

# Verwalten von Data Warehouse-Anforderungen

Sie können Data Warehouse-Anfragen, die Sie gestellt haben, anzeigen und verwalten. Nur Administratoren können Anforderungen anderer Benutzer in ihrer Organisation anzeigen und verwalten.

In den folgenden Abschnitten werden die Aktivitäten beschrieben, die Sie bei der Verwaltung von Anforderungen durchführen können.

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

* Administratoren, die die Anforderung eines anderen Benutzers bearbeiten, müssen ein neues Konto und einen neuen Speicherort auswählen, auf das sie zugreifen können.

So bearbeiten Sie eine geplante Anforderung:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, die Sie bearbeiten möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Bearbeiten**] aus.

1. Bearbeiten Sie die Anforderung wie gewünscht. Eingestellte Konfigurationsoptionen können nicht bearbeitet werden.

   Informationen zu den einzelnen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Auswählen [!UICONTROL **Änderungen speichern**].

## Verlauf einer Anforderung anzeigen

Sie können den Verlauf aller von Ihnen durchgeführten Data Warehouse-Anfragen anzeigen.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Instrumente**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anforderung aus, deren Verlauf Sie anzeigen möchten.

   ![Anforderung verwalten](assets/dw-manage-request.png)

1. Auswählen [!UICONTROL **Verlauf anzeigen**].

   Die [!UICONTROL **Data Warehouse-Anfrage anzeigen**] zeigt eine Liste der einzelnen Berichtbereitstellungen an, die mit der Anfrage verknüpft sind.

   Wählen Sie die **Spalte konfigurieren** icon ![Spaltensymbol konfigurieren](assets/configure-column-icon.png) um Spalten auszublenden oder Spalten anzuzeigen, die nicht standardmäßig angezeigt werden.

   ![Seite mit Anforderungsverlauf](assets/dw-request-history.png)

   Die folgenden Spalten sind verfügbar:

   | Spalte | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Erstellt am**] | Datum und Uhrzeit der Berichterstellung.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Startdatum**] | Datum und Uhrzeit des Berichtstarts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Datum abgeschlossen**] | Datum und Uhrzeit des Abschlusses des Berichts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Aktualisierungsdatum**] | Datum und Uhrzeit der letzten Aktualisierung des Berichts<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Status**] | Der Status des Berichtversands. Mögliche Status sind:<ul><li>[!UICONTROL **Erstellt**]: Der Bericht wurde erstellt, aber noch nicht verarbeitet.</li><li>[!UICONTROL **Ausstehend**]: Der Bericht wartet auf die Verarbeitung.</li><li>[!UICONTROL **Verarbeitung**]: Der Bericht wird derzeit verarbeitet.</li><li>[!UICONTROL **Abgeschlossen**]: Der Bericht ist abgeschlossen und ist jetzt verfügbar.</li><li>[!UICONTROL **Geplant**]: Der Bericht ist geplant, hat aber noch nicht begonnen.</li><li>[!UICONTROL **Abgebrochen**]: Der Bericht wurde vom Benutzer abgebrochen.</li><li>[!UICONTROL **Fehler - Verarbeitung**:] Der Bericht ist fehlerhaft und konnte nicht verarbeitet werden.</li><li>[!UICONTROL **Fehler - fehlgeschlagener Versand**]: Der Bericht wurde erfolgreich generiert, konnte jedoch nicht bereitgestellt werden. Überprüfen Sie die [Konfiguration Ihres Ziels](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)und senden Sie dann den Bericht erneut.</li></ul>. |
   | [!UICONTROL **Von**] | Das Startdatum des im Bericht enthaltenen Gesamtzeitrahmens.<p>Dies wird in der Zeitzone der Report Suite angezeigt.</p> |
   | [!UICONTROL **Bis**] | Das Enddatum des gesamten im Bericht enthaltenen Zeitrahmens. <p>Dies wird in der Zeitzone der Report Suite angezeigt.</p> |
   | [!UICONTROL **Legacy-Anfrage-ID**] | Die ID, mit der ein Bericht in der alten Data Warehouse-Oberfläche identifiziert wird. Diese ID kann bei der Kontaktaufnahme mit der Adobe-Kundenunterstützung erforderlich sein. |
   | [!UICONTROL **Bericht-ID**] | Die ID, mit der ein Bericht in der aktuellen Data Warehouse-Oberfläche identifiziert wird. Diese ID kann bei der Kontaktaufnahme mit der Adobe-Kundenunterstützung erforderlich sein. |


1. Wählen Sie einen Berichtversand und dann eine der folgenden Optionen aus:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Zieldetails**] | Zeigt die mit der Anfrage verknüpften Konto- und Standortdetails an. Dies ist das Konto und der Speicherort, die zuvor konfiguriert wurden, wie unter [Berichtsziel für eine Data Warehouse-Anforderung konfigurieren](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | [!UICONTROL **Bericht abbrechen**] | Bricht den Bericht ab. Berichte mit dem Status [!UICONTROL **Abgeschlossen**] oder [!UICONTROL **Abgebrochen**]. |
   | [!UICONTROL **Bericht erneut ausführen**] | Führt den Bericht erneut mit den Daten aus, die zum Zeitpunkt des ursprünglichen Versands vorlagen. Sie können einen Bericht mit einem der folgenden Status erneut ausführen: [!UICONTROL **Abgebrochen**], [!UICONTROL **Abgeschlossen**], [!UICONTROL **Fehler - Verarbeitung**] oder [!UICONTROL **Fehler - fehlgeschlagener Versand**]. |
   | [!UICONTROL **Bericht erneut senden**] | Sendet die zuvor generierte Berichtsdatei erneut. Sie können einen Bericht mit einem der folgenden Status erneut senden: [!UICONTROL **Abgeschlossen**] oder [!UICONTROL **Fehler - fehlgeschlagener Versand**]. |

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
   | Angefragt von | Der Benutzer, der die Anforderung erstellt hat. |
   | Datum der Anfrage | Das Datum, an dem die Anfrage gestellt wurde. |
   | Status | Die folgenden Status sind verfügbar:<ul><li><p>**Abgeschlossen**: Die Anfrage wurde erfolgreich ausgeführt.</p></li><li><p>**Abgebrochen**: Die Anfrage wurde vom Benutzer abgebrochen.</p></li><li><p>**Geplant**: Die Anforderung ist so konfiguriert, dass sie nach einem Zeitplan ausgeführt wird.</p></li><li><p>**Fehlgeschlagen**: Die Anfrage konnte nicht abgeschlossen werden. Wenn die Anfrage weiterhin fehlschlägt, wenden Sie sich an den Support.</p></li></ul> |

   {style="table-layout:auto"}

1. Stellen Sie sicher, dass alle Spalten ausgewählt sind, die angezeigt werden sollen. Ausgewählte Spalten werden auf der Data Warehouse-Seite angezeigt und zeigen die entsprechenden Informationen an.

## Anforderungen filtern und sortieren

1. Wählen Sie die **Filter** in der linken Leiste der Data Warehouse-Seite.

   ![Anforderungen filtern](assets/dw-filter.png)

1. Erweitern Sie die [!UICONTROL **Report Suites**], [!UICONTROL **Inhaber**] oder [!UICONTROL **Status**] und wählen Sie aus, wie Sie die Anforderungen filtern möchten.

## Suchen nach Anforderungen

1. Geben Sie im Suchfeld oben auf der Data Warehouse-Seite den Anforderungsnamen an, den Sie anzeigen möchten.

   Anforderungen werden bei der Eingabe gefiltert.