---
description: Auf der Seite „Suchmethoden“ wird ermittelt, wie verschiedene Suchmethoden-Berichte Gutschriften für Konversionserfolgsereignisse auf Ihrer Site erhalten. Wenn beispielsweise eine Suchmaschine einen Besucher auf Ihre Site lotst und der Besucher auf Ihrer Site einen Einkauf tätigt, ist unter „Suchmethoden“ festgelegt, wie der Suchmaschine der Verweis gutgeschrieben wird.
title: Suchmethoden
feature: Admin Tools
uuid: 1053993e-7fc4-4874-84fa-367ecdcd7b45
exl-id: 58c4510c-2343-4b0a-9c09-5583f6d4250f
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# Suchmethoden

Auf der Seite „Suchmethoden“ wird ermittelt, wie verschiedene Suchmethoden-Berichte Gutschriften für Konversionserfolgsereignisse auf Ihrer Site erhalten. Wenn beispielsweise eine Suchmaschine einen Besucher auf Ihre Site lotst und der Besucher auf Ihrer Site einen Einkauf tätigt, ist unter „Suchmethoden“ festgelegt, wie der Suchmaschine der Verweis gutgeschrieben wird.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Suchmethoden]**.

## Suchmethoden – Beschreibungen {#section_8B6278DB75224EAB9F49D89A86274E8A}

<table id="table_8ABC1C9BD63F419082E4C4C69E401526"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Name </td> 
   <td colname="col2"> Die zu ändernde Suchmethode </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zuordnung </td> 
   <td colname="col2"> Gibt an, wie eine Gutschrift für einen Verweis angewendet werden soll. Die unterstützten Optionen für die Zuordnung umfassen: <p> <span class="uicontrol"> Zuletzt verwendet (Letzter):</span> Alle Gutschriften gehen an die letzte verweisende Stelle (Standard). </p> <p> <span class="uicontrol"> Ausgangswert:</span> Alle Gutschriften gehen an die erste verweisende Stelle. </p> <p> <span class="uicontrol"> Linear:</span> Gutschriften werden gleichberechtigt an alle verweisenden Stellen verteilt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Läuft ab nach </td> 
   <td colname="col2"> 
    <ul id="ul_95EB224CAD164E9997B148E08AFA5F9B"> 
     <li id="li_C240460C21E14AA498D2EA62B9354710"> <span class="uicontrol"> Besuch:</span> Nach einem bestimmten Zeitraum der Inaktivität, in der Regel ungefähr 30 Minuten. </li> 
     <li id="li_A3AE5438919E44B68DF99BEEA60C44EE"> <span class="uicontrol"> Seitenansicht:</span> Sobald eine Seite auf Ihrer Site aufgerufen wird. </li> 
     <li id="li_D5E20FEF313E4C5B99E7097CA175761A"> <span class="uicontrol"> Minute:</span> Nach einer Inaktivität von 1 Minute. </li> 
     <li id="li_7315AA3EDDBB47A2BEA3C173881378A1"> <span class="uicontrol"> Kauf:</span> Zum Zeitpunkt des Kaufs. </li> 
     <li id="li_C0CF07581654472C9C9EC944E6F18164"> <span class="uicontrol"> Produktansicht:</span> Wenn ein Besucher eine Produkt-Webseite anzeigt. </li> 
     <li id="li_A1B04065150B407491D2EC78EC0DBDF5"> <span class="uicontrol"> Öffnung des Warenkorbs:</span> Wenn ein Besucher einen neuen Online-Warenkorb öffnet. </li> 
     <li id="li_2AA50C6B9CB14500B67909CDF2AA700C"> <span class="uicontrol"> Warenkorb zur Kasse:</span> Wenn ein Besucher mit einem Online-Warenkorb zur Kasse geht. </li> 
     <li id="li_F58CE6FB8DCE4BE4927FFCB35A6D8E31"> <span class="uicontrol"> Hinzufügen zum Warenkorb:</span> Wenn ein Besucher einem Online-Warenkorb ein Produkt hinzufügt. </li> 
     <li id="li_AD7C846F46604FC48E0919ACB7515E14"> <span class="uicontrol"> Entnahme aus Warenkorb:</span> Wenn ein Besucher ein Produkt aus einem Online-Warenkorb entfernt. </li> 
     <li id="li_EB66E0563F564C9F985BE922DABD0A56"> <span class="uicontrol"> Öffnung des Warenkorbs:</span> Wenn ein Besucher den Inhalt eines Online-Warenkorb anzeigt. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Alle Suchmethoden laufen mit dem Ende des Besuchs ab. Wenn Sie für „Läuft ab nach“ ein anderes Ereignis auswählen (z. B. „Warenkorb zur Kasse“), läuft die Suchmethode ab, wenn dieses Ereignis während des Besuchs erfolgt. Wenn „Warenkorb zur Kasse“ nicht während des Besuchs erfolgt, läuft die Suchmethode trotzdem mit dem Besuch ab.
