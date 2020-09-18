---
description: Verfügt neben dem gregorianischen Kalender noch über andere Kalenderoptionen. Zu den Optionen zählen die 4-4-5-, 4-5-4- und 5-4-4-Kalendermodelle, die alle als Standard im Einzelhandel genutzt werden. Darüber hinaus bietet die Berichterstellung eine Option für einen komplett individualisierbaren Kalender, den Sie selbst einrichten können.
title: Anpassen von Kalendern benutzerspezifisch einstellen
topic: Admin tools
uuid: 4e5e538b-54c9-4c2f-8b6c-9f91b6c7bcc7
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 95%

---


# Anpassen von Kalendern benutzerspezifisch einstellen

Verfügt neben dem gregorianischen Kalender noch über andere Kalenderoptionen. Zu den Optionen zählen die 4-4-5-, 4-5-4- und 5-4-4-Kalendermodelle, die alle als Standard im Einzelhandel genutzt werden. Darüber hinaus bietet die Berichterstellung eine Option für einen komplett individualisierbaren Kalender, den Sie selbst einrichten können.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > Einstellungen **[!UICONTROL bearbeiten]** > **[!UICONTROL Allgemein]** > Kalender **[!UICONTROL anpassen]**

>[!CAUTION]
>
>Wenn Sie Änderungen am Kalender vornehmen, ändern Sie die Art der Datenverarbeitung (d. h. die Definition der wöchentlichen und monatlichen Unique Visitors). Von der Änderung der Kalenderdefinitionen für Wochen und Monate bleiben historische Daten unberührt. Diese Einstellung wirkt sich auch auf Segmente aus, die auf Datumsbereichen basieren.

Sie können den Kalender nutzen, um den ersten Tag der Woche und des Jahres zu definieren oder einen anderen Einzelhandelskalender-Stil verwenden. Die verschiedenen Kalenderformate dienen unterschiedlichen Zwecken, z. B. dem Vergleich von Verkaufszahlen und der Standardisierung von Prognosen, der Personalkostenanalyse oder der Inventurzahlenregulierung. Im Einzelhandel wird beispielsweise der 4-5-4-Kalender zur Unterstützung von Verkaufssaisons verwendet, die für die Branche typisch sind. Die einzelnen Kalenderformate werden im Folgenden beschrieben.

## Kalender benutzerspezifisch einstellen – Beschreibungen {#section_B0D224DACB914A378902A4E0E1234889}

<table id="table_E609632569EB499184E56618C2CEF742"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kalender </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gregorianischer Kalender </p> </td> 
   <td colname="col2"> <p> Hier gilt das traditionelle Kalenderformat (Januar bis Dezember mit 30 bis 31 Tagen und einer variablen Anzahl von Wochen je Monat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modifizierter gregorianischer Kalender </p> </td> 
   <td colname="col2"> <p> Basiert auf dem traditionellen Gregorianischen Kalender, ermöglicht jedoch die Auswahl des ersten Monats des Jahres und des ersten Tages der Woche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4-5-4-Einzelhandelskalender </p> </td> 
   <td colname="col2"> <p> Hier werden Monate auf eine bestimmte Zahl Wochen reduziert. Das bedeutet, der Januar hat vier Wochen usw. Der Nationale Einzelhandelsverband (USA) verwendet das Kalenderformat 4-5-4. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierter Kalender </p> </td> 
   <td colname="col2"> <p> Bietet drei Formate, basierend auf der Anzahl der Wochen je Monat. Die Anzahl der Wochen je Monat hängt von dem ausgewählten ersten Tag des Jahres ab. </p> <p>Ein Jahr hat 52 Wochen. Bei einer Aufteilung in vier Quartale kommen 13 Wochen pro Quartal heraus. Doch in einem Quartal sind drei Monate enthalten. Die Zahl 13 ist nicht durch 3 teilbar. Folglich muss die übrig gebliebene Woche aus Konsistenzgründen einem der Monate hinzugefügt werden. 5-4-4 bedeutet, dass die übrig gebliebene Woche im 1. Monat des Quartals ist. 4-5-4 bedeutet, dass sie im 2. Monat ist, usw. Im 5-4-4-Kalender wird die 53. Woche dem letzten Quartal des Jahres hinzugefügt. </p> 
    <ul id="ul_1579FD106A47419486B03E248A5E6ED5"> 
     <li id="li_E9B9E8F03E324DBDA9139C2D0D599092"><b>4-5-4</b>: Januar hat vier Wochen, Februar hat fünf Wochen, März hat vier Wochen usw. </li> 
     <li id="li_D0675DBDEC4641D2A8645B5CDFC565AB"><b>4-4-5</b>: Januar hat vier Wochen, Februar hat vier Wochen, März hat fünf Wochen usw. </li> 
     <li id="li_6743BBB9AC9A4CFEAA0CBCE51052BC29"><b>5-4-4</b>: Januar hat fünf Wochen, Februar hat vier Wochen, März hat vier Wochen usw. </li> 
    </ul> <p>Hinweis: Diese Kalenderoption wird in allen Adobe Analytics-Tools (Analysis Workspace, Reports &amp; Analytics, Report Builder, Activity Map, Ad Hoc Analysis) unterstützt mit Ausnahme von Data Warehouse, das keine benutzerdefinierten Kalender unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

