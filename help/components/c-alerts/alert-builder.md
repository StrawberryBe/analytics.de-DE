---
description: 'null'
title: Warnhinweiserstellung
uuid: 86d00a33-dc99-4dc3-a732-0b895ba487bc
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '462'
ht-degree: 100%

---


# Warnhinweiserstellung

>[!IMPORTANT]
>
>Intelligente Warnhinweise sind nur für Kunden von Adobe [!DNL Analytics] Prime und Adobe [!DNL Analytics] Ultimate verfügbar.

Für den Zugriff auf die Warnhinweiserstellung gibt es vier Möglichkeiten:

* Mithilfe des folgenden Tastaturbefehls in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* Indem Sie zu **[!UICONTROL Workspace]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Neuer Warnhinweis]** navigieren.
* Indem Sie ein oder mehrere Freiform-Tabellenzeilenelemente auswählen, mit der rechten Maustaste klicken und **[!UICONTROL Warnhinweis aus Auswahl erstellen auswählen]**.
* Indem Sie von einem [!UICONTROL Reports &amp; Analytics]-Bericht aus zu **[!UICONTROL Mehr]** > **[!UICONTROL Warnhinweis hinzufügen]** navigieren.

Die Benutzeroberfläche der Warnhinweiserstellung ähnelt solchen mit erstellten Segmenten oder berechneten Metriken in [!DNL Analytics]:

![](assets/alert_builder.png)

**Warnungsname**

Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten.

**Zeitgranularität**

Geben Sie an, wann die Metrik überprüft werden soll: stündlich, täglich, wöchentlich oder monatlich.

>[!NOTE]
>
>Bei Report Suites mit einem benutzerdefinierten Kalender wird die monatliche Abstufung in der Warnhinweiserstellung nicht unterstützt.

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

* Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, damit ein Warnhinweis ausgegeben wird. Sie können diesen Wert auf einen Schwellenwert und anschließend auf eine der folgenden Bedingungen setzen:

   * Anomalie vorhanden
   * Anomalie liegt über erwartetem Wert
   * Anomalie liegt unter erwartetem Wert
   * Anomalie überschreitet
   * ist größer oder gleich
   * ist kleiner oder gleich
   * ändert sich um

* „Anomalie überschreitet“ ist eine neue Bedingung, die über die vorhandenen (statischen) Schwellenwerte hinausgeht. Sie bezieht Anomalieerkennungsalgorithmen mit ein, die den Auslöser dynamisch definieren. Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.
* Für die stündliche Granularität ist ein Schwellenwert von 99,75 % und für die tägliche Granularität ein Schwellenwert von 99 % festgelegt.
* Beachten Sie, dass Sie auch berechnete Metriken verwenden können.

*... Mit diesen Filtern*

Platzieren Sie mittels Drag-and-Drop Segmente oder Dimensionen, um Filter hinzuzufügen. Wenn Sie zum Beispiel ein Segment vom Typ „Nur Mobilgeräte“ hinzufügen, würde die Regel nur für Mobilgeräte ausgelöst werden.

Zusätzliche Filter werden mithilfe einer AND-Anweisung hinzugefügt.

**Eine Regel hinzufügen**

Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.

## Warnhinweisvorschau {#section_10D75BA7B77E4C5FAF58A719C082E070}

Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft damit zu rechnen ist, dass ein Warnhinweis ausgelöst wird.

Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.

Wenn Sie feststellen, dass Warnhinweise zu oft ausgelöst werden würden, können Sie den Schwellenwert im [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md) anpassen.

![](assets/alert_preview.png)
