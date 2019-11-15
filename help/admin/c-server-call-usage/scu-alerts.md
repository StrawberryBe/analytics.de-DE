---
description: Fügen Sie Warnhinweise zur Nutzung von Server-Aufrufen hinzu oder verwalten Sie diese. Wenn Sie einen Warnhinweis einrichten, dann gilt dieser für alle Report Suites und Anmeldeunternehmen eines Abrechnungsunternehmens.
title: Warnungen zur Verwendung von Server-Aufrufen
uuid: 701fd542-5b24-42df-97a0-08e10929fa48
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Warnungen zur Verwendung von Server-Aufrufen

Wenn Sie einen Warnhinweis einrichten, dann gilt dieser für alle Report Suites und Anmeldeunternehmen eines Abrechnungsunternehmens.

## Überblick

A new alert category called **[!UICONTROL Server Calls Usage Alert]** is part of the existing [Alert Management](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/intellligent_alerts.html) user interface.

It is pre-populated with **1 default alert** that appears within any login company that has access to the Server Call Usage feature. Diese Warnhinweise löst eine Benachrichtigung aus, die an alle Administratoren des Anmeldeunternehmens gerichtet ist, wenn eines der folgenden Kriterien erfüllt ist:

* „Beliebige“ Nutzung der Server-Aufrufe, die bei „über oder gleich“ 100 % irgendeiner Art von Server-Aufrufen liegt, zu denen sie berechtigt sind, ODER
* „Beliebige“ Nutzung der Server-Aufrufe, die bei „über oder gleich“ 90 % irgendeiner Art von Server-Aufrufen liegt, zu denen sie berechtigt sind, ODER
* „Beliebige“ Nutzung der Server-Aufrufe, die bei „über oder gleich“ 75 % irgendeiner Art von Server-Aufrufen liegt, zu denen sie berechtigt sind, UND „Verbrauchte Nutzungsperiode“ liegt bei „unter oder gleich“ 75 % der Nutzungsperiode.

![](assets/alerts.png)

Sie können mithilfe von zwei Methoden auf die Warnhinweise zur Nutzung von Server-Aufrufen zugreifen:

* Klicken Sie auf **[!UICONTROL Warnhinweise verwalten]in der oberen rechten Ecke des Reiters „Aktuelle Nutzung“ oder des Reiters „Nutzung der Report Suite“; oder**
* Navigate to **[!UICONTROL Components]** &gt; **[!UICONTROL Alerts]** in Adobe Analytics.

## Warnhinweise zur Nutzung von Server-Aufrufen erstellen {#section_2A2882C6D48D47C1944D52FB7C766BEC}

Um zusätzliche Warnhinweise zu erstellen:

1. Click **[!UICONTROL + Add]** and select **[!UICONTROL Server Call Usage Alert]**.

   ![](assets/server_call_alert.png)

1. Definieren Sie den Warnhinweis.

   ![](assets/sc_alert.png)

   * **Titel**: Geben Sie einen beschreibenden Namen an. Sie können einen Warnhinweis nicht ohne Namen speichern.
   * **Zeitgranularität**: Gibt an, wie oft die Warnung überprüft wird. *Momentan unterstützen wir nur eine wöchentliche Granularität.* Das bedeutet, dass der Warnhinweis wöchentlich überprüft wird. Dabei werden die Daten der aktuellen Nutzungsperiode berücksichtigt.
   * **Empfänger**: Geben Sie Personen im Unternehmen an, die eine E-Mail erhalten sollen, wenn die Warnung den angegebenen Schwellenwert auslöst.
   * **Ablaufdatum**: Standardmäßig ist das Ablaufdatum ein Jahr nach dem Erstellungsdatum der Warnung.
   * **Warnhinweis senden, wenn**:

      * Beliebige dieser Metriken AuslöserFügen Sie den Typ des/der Server-Aufrufe/s als Metrik hinzu und geben Sie den Warnungsschwellenwert durch Auswahl des Modifikators und des Schwellenwerts an:
         * ist größer oder gleich
         * ist kleiner oder gleich
      * Mit Geben Sie den Schwellenwert und die Bedingung (über oder gleich oder unter oder gleich) für den Nutzungszeitraum an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Warnhinweise zur Nutzung von Server-Aufrufen verwalten {#section_8FF98170763C4B5CBEC6DD43F893177A}

![](assets/alert_mgmt.png)

Warnhinweise verwalten:

1. Wählen Sie das Kästchen neben einem oder mehreren Warnhinweisen aus. Oben werden die Verwaltungsoptionen für Warnhinweise angezeigt.
1. Führen Sie eine oder mehrere dieser Aktionen durch:

   | Aktion | Definition |
   |--- |--- |
   | + Fügen Sie | Die [Warnhinweiserstellung](/help/admin/c-server-call-usage/scu-alerts.md) per Klick auf [!UICONTROL + Hinzufügen] öffnen. |
   | Markieren | Markieren Sie Warnhinweise, um sie leichter zu verwenden. |
   | Löschen | Sie können alle Warnhinweise mit Ausnahme des standardmäßigen Warnhinweises löschen. |
   | Umbenennen | Sie können alle Warnhinweise mit Ausnahme des standardmäßigen Warnhinweises umbenennen. |
   | Genehmigen | Genehmigen Sie Warnhinweise, um sie „offiziell“ zu machen. |
   | Aktivieren/deaktivieren | Sie können alle Warnhinweise mit Ausnahme der standardmäßigen Warnhinweise aktivieren oder deaktivieren. |
   | Verlängern | Wenn ein oder mehrere Warnhinweise ausgewählt sind, können sie verlängert werden. Dadurch wird ihr Ablaufdatum auf ein Jahr nach dem Tag, an dem auf [!UICONTROL Verlängern] geklickt wurde, verlängert, ungeachtet des ursprünglichen Ablaufdatums. |
   | In CSV exportieren | Siehe [Nutzungsbericht herunterladen](/help/admin/c-server-call-usage/report-suite-usage.md) |

