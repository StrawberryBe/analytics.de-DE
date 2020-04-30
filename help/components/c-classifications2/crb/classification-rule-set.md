---
description: Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.
subtopic: Classifications
title: Klassifizierungsregelsätze
topic: Admin tools
uuid: c4d7b77c-fa98-44be-955f-9aee7f73480b
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Klassifizierungsregelsätze

Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.

## Klassifizierungsregelsätze

Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.

## Classification Rule Builder-Seite  {#section_C60B0888C76D49C596EF19F11808B718}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

The following fields and options are available on the [!UICONTROL Classifications Rule Builder].

<table id="table_A5D92409969747E39E041216A5AA32CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="/help/components/c-classifications2/crb/classification-rule-set.md"  > Regelsatz hinzufügen</a> </p> </td> 
   <td colname="col2"> <p>Erstellt einen Regelsatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln </p> </td> 
   <td colname="col2"> Zeigt die Anzahl der Regeln im Regelsatz an. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> Zeigt den Aktivitätsstatus des Regelsatzes an, beispielsweise „Entwurf“ oder „Aktiv“. Aktive Regeln werden täglich verarbeitet, wobei die zu untersuchenden Classification-Daten in der Regel einen Monat zurückgehen. Die Regeln suchen automatisch nach neuen Werten und laden die Classifications hoch. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zuletzt geändert </p> </td> 
   <td colname="col2"> Gibt den Zeitpunkt an, zu dem der Regelsatz bearbeitet wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duplizieren </p> </td> 
   <td colname="col2"> Dupliziert (kopiert) einen Regelsatz, so dass Sie diesen Regelsatz auf eine andere Variable anwenden können (oder auch auf dieselbe Variable in einer anderen Report Suite). </td> 
  </tr> 
 </tbody> 
</table>

## Erstellen eines Klassifizierungsregelsatzes {#create-classification-rule-set}

Benennen Sie den Classification-Regelsatz, wenden Sie die Variable an und legen Sie die Einstellungen für Überschreiben fest.

1. (Prerequisite) Define the classification structure in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

   (Informationen zum Hinzufügen von Classifications finden Sie unter [Classifications](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) in der Admin Tools-Hilfe.)

   Variables will display in the [!UICONTROL New Rule Set] panel only after they have at least one classification defined for that variable.

   Sie können Classifications für eine Variable unter **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Traffic]** > **[!UICONTROL Traffic Classifications]** (oder **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**) erstellen. Then select the variable, then click **[!UICONTROL Add Classification]**.

1. To create the rule set, click **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]** > **[!UICONTROL Add Rule Set]**.

   ![](assets/new_rule_set.png)

1. Benennen Sie den Regelsatz und klicken Sie auf **[!UICONTROL Create Rule Set]**.
1. Wählen Sie den zu bearbeitenden Regelsatz aus.

   ![](assets/classification_rules_page.png)

1. Klicken Sie auf **[!UICONTROL Select Report Suites and Variables]**.

   Die Report Suite und die Variablenliste werden mit allen klassifizierten Variablen ausgefüllt, die in allen Report Suites Ihres angemeldeten Unternehmens verfügbar sind. Eine Variable in einer Report Suite kann nur zu jeweils einem einzigen Regelsatz gehören.

   Siehe *`Variable`* in den Definitionen für die Seite [Classification Rule Builder](/help/components/c-classifications2/crb/classification-rule-definitions.md) für weitere Informationen.
1. Specify the report suites and variables to use, then click **[!UICONTROL Save]**.
1. Fahren Sie fort, indem Sie [Klassifizierungsregeln zum Regelsatz hinzufügen](/help/components/c-classifications2/crb/classification-rule-set.md).
