---
description: Verfügt neben dem gregorianischen Kalender noch über andere Kalenderoptionen. Zu den Optionen zählen die 4-4-5-, 4-5-4- und 5-4-4-Kalendermodelle, die alle als Standard im Einzelhandel genutzt werden. Darüber hinaus bietet die Berichterstellung eine Option für einen komplett individualisierbaren Kalender, den Sie selbst einrichten können.
title: Anpassen von Kalendern
feature: Admin Tools
exl-id: 2196c7b7-7183-43a8-bb91-5a1e479819d4
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: ht
source-wordcount: '514'
ht-degree: 100%

---

# Anpassen von Kalendern

Verfügt neben dem gregorianischen Kalender noch über andere Kalenderoptionen. Zu den Optionen zählen die 4-4-5-, 4-5-4- und 5-4-4-Kalendermodelle, die alle als Standard im Einzelhandel genutzt werden. Darüber hinaus bietet die Berichterstellung eine Option für einen komplett individualisierbaren Kalender, den Sie selbst einrichten können.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen **[!UICONTROL > Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Kalender benutzerspezifisch einstellen]**

>[!CAUTION]
>
>Wenn Sie Änderungen am Kalender vornehmen, ändern Sie die Art der Datenverarbeitung (d. h. die Definition der Unique Visitors pro Woche und pro Monat). Wenn die Definition von Wochen und Monaten eines Kalenders geändert wird, bleiben historische Daten unberührt. Diese Einstellung wirkt sich auch auf Segmente aus, die auf Datumsbereichen basieren.

Sie können den Kalender nutzen, um den ersten Tag der Woche und des Jahres zu definieren oder einen anderen Einzelhandelskalender-Stil verwenden. Die verschiedenen Kalenderformate dienen unterschiedlichen Zwecken, z. B. dem Vergleich von Verkaufszahlen und der Standardisierung von Prognosen, der Personalkostenanalyse oder der Inventurzahlenregulierung. Im Einzelhandel wird beispielsweise der 4-5-4-Kalender zur Unterstützung von Verkaufssaisons verwendet, die für die Branche typisch sind. Die einzelnen Kalenderformate werden im Folgenden beschrieben.

## Kalender benutzerspezifisch einstellen – Beschreibungen  {#section_B0D224DACB914A378902A4E0E1234889}

| Kalender | Beschreibung |
|--- |--- |
| Gregorianischer Kalender | Hier gilt das traditionelle Kalenderformat (Januar bis Dezember mit 30 bis 31 Tagen und einer variablen Anzahl von Wochen je Monat). |
| Modifizierter gregorianischer Kalender | Basiert auf dem traditionellen Gregorianischen Kalender, ermöglicht jedoch die Auswahl des ersten Monats des Jahres und des ersten Tages der Woche. |
| 4-5-4-Einzelhandelskalender | Hier werden Monate auf eine bestimmte Zahl Wochen reduziert. Das bedeutet, der Januar hat vier Wochen usw. Der Nationale Einzelhandelsverband (USA) verwendet das Kalenderformat 4-5-4. |
| Benutzerdefinierter Kalender | Bietet drei Formate, basierend auf der Anzahl der Wochen je Monat. Die Anzahl der Wochen in jedem Monat hängt vom ausgewählten ersten Tag des Jahres ab.  Ein Jahr hat 52 Wochen. Bei einer Aufteilung in vier Quartale kommen 13 Wochen pro Quartal heraus. Doch in einem Quartal sind drei Monate enthalten. Die Zahl 13 ist nicht durch 3 teilbar. Folglich muss die restliche Woche aus Konsistenzgründen zu einem der Monate hinzugefügt werden.<ul><li>5-4-4 bedeutet, dass die übrig gebliebene Woche im 1. Monat des Quartals ist. 4-5-4 bedeutet, dass sie im 2. Monat ist, usw. Im 5-4-4-Kalender wird die 53. Woche dem letzten Quartal des Jahres hinzugefügt.</li><li>4-5-4: Januar hat vier Wochen, Februar hat fünf Wochen, März hat vier Wochen usw.</li><li>4-4-5: Januar hat vier Wochen, Februar hat vier Wochen, März hat fünf Wochen usw.</li><li>5-4-4: Januar hat fünf Wochen, Februar hat vier Wochen, März hat vier Wochen usw.</li></ul> |

>[!NOTE]
>Diese Kalenderoptionen werden in allen Adobe Analytics-Tools (Analysis Workspace, Reports &amp; Analytics, Report Builder, Activity Map) unterstützt mit Ausnahme von Data Warehouse. Data Warehouse unterstützt nur den gregorianischen Kalender vollständig. Bei der Auswahl eines nicht-gregorianischen Kalenders verwendet Data Warehouse den erwarteten Datumsbereich des nicht-gregorianischen Kalenders. Die Aufschlüsselung nach Tag/Woche/Monat in den Berichtszeilen entspricht jedoch möglicherweise nicht den Erwartungen an einen nicht-gregorianischen Kalender.
