---
description: Bei einer Zeitunterteilung wird der Zeitstempel erfasster Hits in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilt.
title: Dimensionen für die Zeitunterteilung
uuid: c9fa7921-aa57-483c-b2f9-da55013ada17
feature: Grundlagen zu Workspace
role: Business Practitioner, Administrator
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '234'
ht-degree: 100%

---

# Dimensionen für die Zeitunterteilung

Bei einer Zeitunterteilung wird der Zeitstempel erfasster Hits in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilt.

Die Dimensionen für die Zeitunterteilung basieren auf der Zeitzone der Report Suite bzw. der virtuellen Report Suite. Diese Dimensionen sind in Analysis Workspace verfügbar und können bei der Beantwortung der folgenden Fragen hilfreich sein:

* Welches ist in einem umfangreichen Datumsbereich die bevorzugte Tageszeit, zu der Besucher meine Site oder Anwendung aufrufen?
* Gibt es Wochentage oder Zeiten, an bzw. zu denen auf meiner Site oder in meiner Anwendung mehr Konversionen erfolgen?
* Wie verhalten sich Verkäufe am Wochenende in Bezug auf Verkäufe während der Woche?
* Führt eine bestimmte Marketing-Kampagne eher am Morgen oder am Nachmittag zu einer höheren Konversionsrate?

>[!NOTE]
>
>Die Dimensionen für die Zeitunterteilung sind nur in Analysis Workspace verfügbar. Wenn Sie Dimensionen für die Zeitunterteilung in anderen Analytics-Lösungen verwenden möchten, können Sie das [getTimeParting-Plug-in](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/plugins/gettimeparting.html) implementieren.

Zu den Dimensionen für die Zeitunterteilung in Analysis Workspace zählen:

| Dimension | Beispielwerte |
|--- |--- |
| Stunde des Tages | 0–23 |
| Vormittag/Nachmittag | Vormittag (AM), Nachmittag (PM) |
| Wochentag | Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag, Sonntag |
| Wochenende/Wochentag | Wochenende, Wochentag |
| Tag des Monats | 1–31 |
| Monat des Jahres | Januar bis Dezember |
| Tag des Jahres | 1–366 |
| Quartal des Jahres | Q1, Q2, Q3, Q4 |
