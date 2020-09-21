---
description: Erstellen Sie ein Datenelement mit dem Dynamic Tag Management.
keywords: Dynamic Tag Management;data element;create new data element;name;type;default value;force lowercase value;remember this value for
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Datenelement erstellen
uuid: eacd5c60-6197-4129-a9e1-a39e9a58b38a
translation-type: ht
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8
workflow-type: ht
source-wordcount: '331'
ht-degree: 100%

---


# Datenelement erstellen

Erstellen Sie ein Datenelement mit dem Dynamic Tag Management.

1. [Erstellen Sie eine Webeigenschaft](/help/implement/other/dtm/t-create-web-property.md), falls noch keine vorhanden ist.
1. Klicken Sie in der Webeigenschaft auf **[!UICONTROL Regeln]** > **[!UICONTROL Datenelemente]**.
1. Klicken Sie auf **[!UICONTROL Neues Datenelement erstellen]**.
1. Füllen Sie die folgenden Felder und Optionen aus:

   <table id="choicetable_681F7D5B86534FF0B6DB67E117B8E381"> 
    <thead class="chhead sthead"> 
      <th class="choptionhd"> Option</th> 
      <th class="chdeschd"> Beschreibung</th> 
    </thead> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Name</strong></td> 
      <td class="chdesc stentry"> <p>Der Anzeigename für das Datenelement, den ein Marketing-Experte erkennen kann. Beispiel: 
        <code>
          Product ID
        </code>. </p> <p> <p>Hinweis: Der Name wird durch den Regel-Builder referenziert, nicht durch eine ID. Sollten Sie den Namen des Datenelements ändern, müssen Sie die Referenz in jeder Regeln anpassen, die dieses Element verwendet. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Typ</strong></td> 
      <td class="chdesc stentry"> <p> Legt fest, von wo die Daten bezogen werden, zu den Quellen gehören beispielsweise JS-Objekt, CSS-Selektor, Cookies, URL-Parameter oder benutzerdefinierter Code. </p> <p>Abhängig vom gewählten Typ stehen verschiedene Optionen zur Auswahl. Weitere Informationen und Beispiele finden Sie unter <a href="https://docs.adobe.com/content/help/de-DE/dtm/using/resources/data-elements.html">Datenelement-Typen</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Standardwert</strong></td> 
      <td class="chdesc stentry"> <p>Ein Standardelement. Mit diesem Wert wird sichergestellt, dass das Datenelement immer einen Wert aufweist, selbst wenn kein URL-Parameter vorhanden ist oder vom Dynamic Tag Management nicht gefunden werden kann. </p> <p> <p>Hinweis: Sollte weder ein Wert noch ein Standardwert vorhanden sein, wird kein Wert zurückgegeben. Diejenigen Variablen, die sich auf dieses Datenelement beziehen, werden nicht festgelegt. Beachten Sie zudem, dass das Feld mit dem Standardwert ignoriert wird, wenn es sich um ein Datenelement mit benutzerdefiniertem Code handelt. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Kleinbuchstaben erzwingen</strong></td> 
      <td class="chdesc stentry"> <p>Das Dynamic Tag Management verwandelt den Wert automatisch in einen Wert, der nur aus Kleinbuchstaben besteht. </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Diesen Wert speichern für</strong></td> 
      <td class="chdesc stentry"> <p>Wie lange dieser Wert im Dynamic Tag Management gespeichert werden soll. </p> <p> Zu gültigen Werten gehören: </p> 
      <ul id="ul_52F6CD8FC22942208F3F45492E914104"> 
        <li id="li_32E4366C5B2E46D788CD8478620FE3E0"> <p>Sitzung: Die sitzungsbezogene Zeitdauer kann je nach Implementierung variieren. Sitzungsdatenelemente werden auf das Sitzungscookie festgelegt. Diese Einstellung könnte sich auf einen Webserver oder den Browser beziehen. Die Einstellung bezieht sich nicht auf die Sitzung, die für Marketing Reports &amp; Analytics verwendet wird. </p> </li> 
        <li id="li_8A944564BF7643E4B21F0EF2394B3FE8"> <p>Seitenansicht. </p> </li> 
        <li id="li_5C8A2F2392FD475AA89DDA7D5B5CF88B"> <p>Besucher. </p> </li> 
      </ul> </td> 
    </tr> 
   </table>

   Weitere Informationen zur Verwendung dieser Datenelemente finden Sie unter [Datenelemente](https://docs.adobe.com/content/help/de-DE/dtm/using/resources/data-elements.html) in der Adobe-Produktdokumentation zum Adobe Tag Management.
1. Klicken Sie auf **[!UICONTROL Datenelement speichern]**.
