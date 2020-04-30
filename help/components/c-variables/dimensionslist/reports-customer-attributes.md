---
description: Häufig gestellte Fragen zu Analytics für Kundenattribute und Informationen zum Erstellen des Berichts „Kundenattribute“.
solution: Experience Cloud,Analytics
title: Kundenattribute
uuid: 94721265-ba23-45d5-8807-76f81b0b8a30
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Kundenattribute

Häufig gestellte Fragen zu Analytics für Kundenattribute und Informationen zum Erstellen des Berichts „Kundenattribute“.

**[!UICONTROL Reports]** **[!UICONTROL > Visitor Profile]** > **[!UICONTROL Customer Attributes]**

Wenn Sie Daten von Unternehmenskunden in einer CRM-Datenbank (Customer Relationship Management) erfassen, können Sie diese Daten in eine Datenquelle für Kundenattribute in die Experience Cloud hochladen. Nach dem Hochladen der Daten können Sie in „Reports &amp; Analytics“ den Bericht „Kundenattribute“ erstellen.

* [Kundenattribute und Berichterstattungsmetriken in Analytics](/help/components/c-variables/dimensionslist/reports-customer-attributes.md#section_EF343662146B460A882D3DF772ADD86D)
* [Häufig gestellte Fragen – Kundenattribute in Analytics](/help/components/c-variables/dimensionslist/reports-customer-attributes.md#section_E29641D1F3D649C1AC9EA5231921F038)

Informationen zum Hochladen von Kundenattributdaten erhalten Sie unter [Kundenattribute](https://docs.adobe.com/content/help/de-DE/core-services/interface/customer-attributes/attributes.html) in Experience Cloud.

## Kundenattribute und Berichterstattungsmetriken in Analytics  {#section_EF343662146B460A882D3DF772ADD86D}

Nach dem Hochladen von Kundenattributen und der Validierung des Schemas (in der Experience Cloud) erstellt das System Metriken basierend auf den freundlichen Namen (wie *`age`* oder *`gender`*), die Sie den Attributzeichenfolgen und -ganzzahlen zuordnen. Diese Metriken werden unter **[!UICONTROL Visitor Profile]** > **[!UICONTROL Customer Attributes]** Berichte angezeigt.

Beispiel:

**[!UICONTROL Visitor Profile]** > **[!UICONTROL Customer Attributes]** > **[!UICONTROL Age]**

![](assets/report_age.png)

**Beispiel – Metriken für das Alter**

Wenn Sie eine Zeichenfolge als *`age`* angeben, erstellt das System die folgenden Metriken und Dimensionen:

* Altersdimension: Sie können einen Bericht basierend auf dem Altersattribut erstellen.
* Altersmetrik: Eine Metrik, die Sie zu einem Bericht hinzufügen können, beispielsweise einem Unique Visitors-Bericht.
* Zählung der Altersmetrik: Sie können beispielsweise nachvollziehen, ob Besucher einen Wert für  *`age`* auf einem Formular angegeben haben.

Da Metriken in einer Berichtstabelle Summen darstellen, sollten Sie  [eine berechnete Metrik erstellen](https://docs.adobe.com/content/help/de-DE/analytics/components/calculated-metrics/cm-overview.html), über die Sie Informationen zum Durchschnittsalter erhalten. Die Formel für diese Metrik lautet `Age / Count of Age`.

## Häufig gestellte Fragen – Kundenattribute in Analytics {#section_E29641D1F3D649C1AC9EA5231921F038}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Warum ist es empfehlenswert, den Identity Service zu verwenden, um die Kunden-ID festzulegen, anstatt die Kunden-ID in eine Eigenschaft oder eVar einzugeben? </p> </td> 
   <td colname="col2"> <p>Die Verwendung des Identity Service bietet eine Reihe von Vorteilen: </p> 
    <ul id="ul_5D3659604D43419F9CA5920B4F93728E"> 
     <li id="li_BA2EF0715C5A47EFAFA7191CFAD088A4">Wenn Sie die Kunden-ID nicht mit dem Identity Service festlegen, sind die Kundendatensätze nur für Adobe Analytics verfügbar. Wenn Sie die Kundendatensätze für Echtzeit-Targeting verwenden möchten, müssen Sie den Identity Service verwenden. </li> 
     <li id="li_228358684E474A298E39578D427BF932">Durch die Verwendung des Identity Service für das Festlegen der Kunden-ID wird die Zeit zur Synchronisierung der IDs mit Experience Cloud verkürzt. Wenn Sie die Kunden-ID in eine Prop oder eVar eingeben, werden die Kunden-IDs über Back-End-Serversynchronisierung an Experience Cloud gesendet. Die Synchronisierung erfolgt in diesem Fall in Stapeln. Der Identity Service synchronisiert die Kunden-ID sofort mit Experience Cloud. </li> 
     <li id="li_BCF28219E4014FCF9F747C3D8D270526"> Wenn der Identity Service anstatt einer Eigenschaft oder einer eVar verwendet wird, kann diese Eigenschaft oder eVar für andere Zwecke verwendet werden. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich eine Kunden-ID bereits in einer Prop oder einer eVar speichere, warum sollte ich diese neue Funktion nutzen, anstatt meine Prop oder eVar mit CRM-Attributen zu klassifizieren? </p> </td> 
   <td colname="col2"> <p>Props und eVars unterliegen Uniques Exceeded-Einschränkungen. Dank dieser Funktion können Sie Attributdaten für eine unbegrenzte Anzahl an Kunden-IDs einfügen. Außerdem werden durch den Prop/eVar-Ansatz die CRM-Informationen für Analytics eingeschränkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie werden meine CRM-Attribute in Adobe Analytics angezeigt? </p> </td> 
   <td colname="col2"> <p>CRM-Attribute werden in Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis, der Berichterstellungs-API und in Report Builder angezeigt. Textattribute werden als Berichte/Dimensionen angezeigt. Numerische Attribute werden sowohl als Dimensionen als auch als Metriken angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Werden die CRM-Daten in Data Warehouse und in Datenfeeds verfügbar sein? </p> </td> 
   <td colname="col2"> <p>Die CRM-Daten stehen derzeit nicht in Data Warehouse oder im Analytics Data Feed zur Verfügung. </p> </td> 
  </tr> 
 </tbody> 
</table>

