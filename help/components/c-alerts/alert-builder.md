---
description: 'null '
seo-description: 'null '
seo-title: Warnhinweiserstellung
title: Warnhinweiserstellung
uuid: 86 d 00 a 33-dc 99-4 dc 3-a 732-0 b 895 ba 487 bc
translation-type: tm+mt
source-git-commit: 8b2feced9fd503395d06dc12c8e5d7985ca89161

---


# Warnhinweiserstellung

>[!IMPORTANT]
>
>Intelligent Alerts are available to Adobe [!DNL Analytics] Prime and Adobe [!DNL Analytics] Ultimate customers only.

Für den Zugriff auf die Warnhinweiserstellung gibt es vier Möglichkeiten:

* Mithilfe der folgenden Tastenkombination in Analysis Workspace:

   `ctrl (or cmd) + shift + a`
* By going to **[!UICONTROL Workspace]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL New Alert]**.
* Indem Sie ein oder mehrere Freiform-Tabellenzeilenelemente auswählen, mit der rechten Maustaste klicken und **[!UICONTROL Warnhinweis aus Auswahl erstellen auswählen]**.
* From within a [!UICONTROL Reports &amp; Analytics] report, by going to **[!UICONTROL More]** &gt; **[!UICONTROL Add Alert]**.

The Alert Builder interface is familiar to those who have built segments or calculated metrics in [!DNL Analytics]:

![](assets/alert_builder.png)

**Warnungsname**

Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten.

**Zeitgranularität**

Geben Sie an, wann die Metrik überprüft werden soll: stündlich, täglich, wöchentlich oder monatlich.

>[!NOTE]
>
>Für Report Suites mit einem benutzerdefinierten Kalender wird die monatliche Granularität in der Warnhinweiserstellung nicht unterstützt.

**Empfänger**

Geben Sie an, wo der Warnhinweis hingeschickt werden soll. An alert can be sent to an [!DNL Analytics] user, an [!DNL Analytics] group, a raw email address, or to a phone number.

>[!IMPORTANT]
>
>The phone number must be preceded by a "+" and a [country code](https://countrycode.org/).

**Ablaufdatum**

Legen Sie das Ablaufdatum eines Warnhinweises fest.

**Warnhinweis senden, wenn...**

*... Jede dieser Metriken ist ein Auslöser*

* Ziehen Sie Metriken per Drag &amp; Drop in die Arbeitsfläche, um Auslöser hinzuzufügen.

   Note that an **"incompatible components”** message will appear if not all the components (metrics/dimensions/segments) in the alert are compatible with the currently selected report suite.

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

Platzieren Sie mittels Drag &amp; Drop Segmente oder Dimensionen, um Filter hinzuzufügen. Wenn Sie zum Beispiel ein Segment vom Typ „Nur Mobilgeräte“ hinzufügen, würde die Regel nur für Mobilgeräte ausgelöst werden.

Zusätzliche Filter werden mithilfe einer AND-Anweisung hinzugefügt.

**Eine Regel hinzufügen**

Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.

## Warnhinweisvorschau {#section_10D75BA7B77E4C5FAF58A719C082E070}

Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft damit zu rechnen ist, dass ein Warnhinweis ausgelöst wird.

Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.

Wenn Sie feststellen, dass Warnhinweise zu oft ausgelöst werden würden, können Sie den Schwellenwert im [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md) anpassen.

![](assets/alert_preview.png)
