---
description: In den meisten Fällen müssen Sie keine Änderungen am Integrationscode vornehmen, der vom Data Connector-Assistenten produziert wird.
seo-description: In den meisten Fällen müssen Sie keine Änderungen am Integrationscode vornehmen, der vom Data Connector-Assistenten produziert wird.
seo-title: Ändern des Integrationscodes
title: Ändern des Integrationscodes
uuid: 3 f 49 a 29 b-ad 38-4967-894 a-ef 7 ecf 4 d 268 f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Ändern des Integrationscodes{#modifying-the-integration-code}

In den meisten Fällen müssen Sie keine Änderungen am Integrationscode vornehmen, der vom Data Connector-Assistenten produziert wird.

Wenn Sie jedoch Anpassungen vornehmen müssen, werden einige der Code-Einstellungen unten beschrieben.

<table id="table_5405A73CEFD44466B3C39559F4A037C9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Codeeinstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s.maxDelay </td> 
   <td colname="col2">Die maximale Anzahl von Millisekunden, die die Adobe Analytics-Bildanforderung auf die Daten von "Demandbase" wartet, bevor Sie den Analytics-Erfassungsserver auslösen. <p>Hinweis: Diese Einstellung gilt für alle Integrationen, die möglicherweise über das Integrate-Modul ausgeführt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._Schlüssel </td> 
   <td colname="col2"> Ihr Demandbase-API-Schlüssel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Apiurl </td> 
   <td colname="col2"> Die URL-Vorlage für die Demandbase-API. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._delim </td> 
   <td colname="col2"> Das Trennzeichen, mit dem die Werte für die Demandbase-Dimension getrennt werden, wenn sie an Adobe Analytics gesendet werden. Eine Änderung dieser Einstellung kann dazu führen, dass die standardmäßigen Classification-Regeln nicht ordnungsgemäß funktionieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Settnt </td> 
   <td colname="col2">Wenn "true" , versucht der Integrationscode, eine ausgeblendete mbox zu verwenden, um die Demandbase-Dimensionen als Profilparameter an Adobe Target zu senden. <p>Hinweis: Dies erfordert, dass der mbox. js-Code auf der Seite vorhanden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Tntvarprefix </td> 
   <td colname="col2"> Diese Zeichenfolge wird jedem Demandbase-Dimensionsnamen vorangestellt, bevor sie an Adobe Target gesendet werden. Wenn diese Einstellung den Wert "db_" hat, wird dann die Dimension" Branche" an Adobe Target als "db_ industry" gesendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Dimensionsarray </td> 
   <td colname="col2"> Die standardmäßigen Demandbase-Dimensionen, die an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. Die Eigenschaft "max_ size" ist die Anzahl der zulässigen Zeichen für die Dimension, bevor die Kürzung erfolgt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Dimensionsarraycustom </td> 
   <td colname="col2"> Die benutzerdefinierten Demandbase-Dimensionen, die an Adobe Analytics gesendet werden. Die Eigenschaft "max_ size" ist die Anzahl der zulässigen Zeichen für die Dimension, bevor die Kürzung erfolgt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Cname </td> 
   <td colname="col2"> Der Name des Sitzungs-Cookies, mit dem der Status für die Kommunikation mit der Demandbase-API beibehalten wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Contextname </td> 
   <td colname="col2"> Der Name der contextdata-Variablen, mit der die Standardabmessungen an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Contextnamecustom </td> 
   <td colname="col2"> Der Name der contextdata-Variablen, mit der die benutzerdefinierten Dimensionen an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. </td> 
  </tr> 
 </tbody> 
</table>

