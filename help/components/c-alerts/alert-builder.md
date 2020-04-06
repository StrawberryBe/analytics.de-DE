---
description: 'null'
title: Warnhinweiserstellung
uuid: 86d00a33-dc99-4dc3-a732-0b895ba487bc
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Warnhinweiserstellung

>[!IMPORTANT]
>
>Intelligente Warnhinweise sind nur für Kunden von Adobe [!DNL Analytics] Prime und Adobe [!DNL Analytics] Ultimate verfügbar.

Sie haben vier Möglichkeiten, auf den Warnhinweiserstellung zuzugreifen:

* Mithilfe des folgenden Tastaturbefehls in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* Gehen Sie zu **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]**.
* By selecting one or more freeform table line items, right-clicking and selecting **[!UICONTROL Create Alert from Selection]**.
* Gehen Sie von innerhalb eines [!UICONTROL Reports & Analytics] Berichts zu **[!UICONTROL More]** > **[!UICONTROL Add Alert]**.

Die Benutzeroberfläche der Warnhinweiserstellung ähnelt solchen mit erstellten Segmenten oder berechneten Metriken in [!DNL Analytics]:

![](assets/alert_builder.png)

**Warnungsname**

Geben Sie einen Namen für die Warnung an. Der Warnungsname kann den Namen des Berichts oder den Schwellenwert für Metriken enthalten.

**Zeitgranularität**

Geben Sie an, wann die Metrik überprüft werden soll: stündlich, täglich, wöchentlich oder monatlich.

>[!NOTE] Bei Report Suites mit einem benutzerdefinierten Kalender wird die monatliche Abstufung in der Warnhinweiserstellung nicht unterstützt.

**Empfänger**

Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen [!DNL Analytics]-Benutzer, eine [!DNL Analytics]-Gruppe, eine E-Mail-Adresse oder eine Telefonnummer gesendet werden.

>[!IMPORTANT]
>
>Die Telefonnummer muss über ein vorangestelltes Pluszeichen („+“) und eine [Landesvorwahl](https://countrycode.org/) verfügen.

**Ablaufdatum**

Legen Sie das Ablaufdatum eines Warnhinweises fest.

**Warnhinweis senden, wenn...**

*... Jede dieser Metriken ist ein Auslöser*

* Ziehen Sie Metriken per Drag &amp; Drop in die Arbeitsfläche, um Auslöser hinzuzufügen.

   Hinweis: Wenn nicht alle Komponenten (Metriken/Dimensionen/Segmente) des Warnhinweises mit der aktuell ausgewählten Report Suite kompatibel sind, wird die Meldung **Nicht kompatible Komponenten** angezeigt.

* Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, bevor eine Warnung eingestellt wird. Sie können diesen Wert auf einen Schwellenwert und dann auf eine der folgenden Bedingungen setzen:

   * Anomalie vorhanden
   * Anomalie höher als erwartet
   * Anomalie niedriger als erwartet
   * Anomalie überschreitet
   * größer oder gleich
   * kleiner oder gleich
   * ändert sich nach

* &quot;Anomalie überschreitet&quot;ist eine neue Bedingung, die über die vorhandenen (statischen) Schwellenwerte hinausgeht. Er bezieht Anomalieerkennungsalgorithmen ein, die den Auslöser dynamisch definieren. Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.
* Die Granularitäten pro Stunde werden auf einen Schwellenwert von 99,75 % und die Granularitäten pro Tag auf 99 % festgelegt.
* Beachten Sie, dass Sie auch berechnete Metriken verwenden können.

*... Mit diesen Filtern*

Platzieren Sie mittels Drag-and-Drop Segmente oder Dimensionen, um Filter hinzuzufügen. Wenn Sie beispielsweise das Segment &quot;Nur Mobilgeräte&quot;hinzufügen, wird die Regel nur für Mobilgeräte ausgelöst.

Zusätzliche Filter werden mit einer AND-Anweisung hinzugefügt.

**Eine Regel hinzufügen**

Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.

## Warnhinweisvorschau {#section_10D75BA7B77E4C5FAF58A719C082E070}

Die interaktive Warnhinweis-Vorschau zeigt Ihnen, wie oft ein Warnhinweis auf der Grundlage vergangener Erfahrungen ausgelöst wird.

Wenn Sie beispielsweise die Zeitgranularität auf &quot;Täglich&quot;einstellen, kann Ihnen die Vorschau mitteilen, dass die Warnung während der letzten 30 oder 31 Tage für eine bestimmte Metrik x-mal ausgelöst worden wäre.

Wenn Sie feststellen, dass zu viele Warnungen ausgelöst wurden, können Sie den Schwellenwert im [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md)anpassen.

![](assets/alert_preview.png)
