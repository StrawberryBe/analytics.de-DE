---
description: HTTP-Anforderungs- und Antwortheader dienen zur Erfassung zusätzlicher Daten, als bereits von AppMeasurement gesammelt werden. In diesem Abschnitt werden die bei der Datenerfassung eingesetzten Header beschrieben.
keywords: Analytics-Implementierung
seo-description: HTTP-Anforderungs- und Antwortheader dienen zur Erfassung zusätzlicher Daten, als bereits von AppMeasurement gesammelt werden. In diesem Abschnitt werden die bei der Datenerfassung eingesetzten Header beschrieben.
seo-title: Datenerfassungs-HTTP-Header
solution: Analytics
title: Datenerfassungs-HTTP-Header
topic: Entwickler und Implementierung
uuid: 3325 e 13 c-b 300-46 e 4-a 592-3 a 83 ed 59718 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Datenerfassungs-HTTP-Header

HTTP-Anforderungs- und Antwortheader dienen zur Erfassung zusätzlicher Daten, als bereits von AppMeasurement gesammelt werden. In diesem Abschnitt werden die bei der Datenerfassung eingesetzten Header beschrieben.

## HTTP-Anforderungsheader {#section_C1DE3416CCC241A898155C915A01A0FC}

<table id="table_84D1F4B54ABE4423A2EBE840C49D3876"> 
 <tbody> 
  <tr> 
   <td> <b>Header</b> </td> 
   <td> <b>Nutzung</b> </td> 
  </tr> 
  <tr> 
   <td> Cookie </td> 
   <td> <p>Dient zum Lesen der zuvor von unseren Datenerfassungsservern erstellten Cookies. </p> <p> Seit 2014 werden auf Adobe-Servern alle Cookies verworfen, die mit einem Server-Aufruf verbunden sind, mit Ausnahme der von Adobe festgelegten Cookies. Eine vollständige Liste der Cookies von Adobe finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/" format="https" scope="external">In Experience Cloud verwendete Cookies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td> User-Agent </td> 
   <td> Dient zur Erkennung von Browser, Betriebssystem und Mobilgerät. </td> 
  </tr> 
  <tr> 
   <td> X-Device-User-Agent </td> 
   <td> Bildet eine Alternative zum „User-Agent“-Header und dient zur korrekten Erkennung von Browser, Betriebssystem und Mobilgerät in einigen Browsern (wie OperaMini). </td> 
  </tr> 
  <tr> 
   <td> X-Original-User-Agent </td> 
   <td> Bildet eine Alternative zum „User-Agent“-Header und dient zur korrekten Erkennung von Browser, Betriebssystem und Mobilgerät in einigen Browsern (wie OperaMini). </td> 
  </tr> 
  <tr> 
   <td> X-OperaMini-Phone-UA </td> 
   <td> Bildet eine Alternative zum „User-Agent“-Header und dient zur korrekten Erkennung von Browser, Betriebssystem und Mobilgerät in einigen Browsern (wie OperaMini). </td> 
  </tr> 
  <tr> 
   <td> X-Skyfire-Phone </td> 
   <td> Bildet eine Alternative zum „User-Agent“-Header und dient zur korrekten Erkennung von Browser, Betriebssystem und Mobilgerät in einigen Browsern (wie OperaMini). </td> 
  </tr> 
  <tr> 
   <td> X-Bolt-Phone-UA </td> 
   <td> Bildet eine Alternative zum „User-Agent“-Header und dient zur korrekten Erkennung von Browser, Betriebssystem und Mobilgerät in einigen Browsern (wie OperaMini). </td> 
  </tr> 
  <tr> 
   <td> UA-OS </td> 
   <td> Dient als Alternative zur Identifizierung des Betriebssystems. </td> 
  </tr> 
  <tr> 
   <td> UA-Pixels </td> 
   <td> Dient als alternative Quelle für die Auflösung des Clientbildschirms. </td> 
  </tr> 
  <tr> 
   <td> UA-Color </td> 
   <td> Dient als alternative Quelle für die Farbtiefe des Clientbildschirms. </td> 
  </tr> 
  <tr> 
   <td> X-moz </td> 
   <td> Dient zur Erkennung, dass die Datenerfassungsanforderung im Zusammenhang mit dem Vorabrufen einer Webseite erfolgte. </td> 
  </tr> 
  <tr> 
   <td> X-Purpose </td> 
   <td> Dient zur Erkennung, dass die Datenerfassungsanforderung erfolgte, als im Browser eine Vorschau einer Webseite angezeigt wurde. </td> 
  </tr> 
  <tr> 
   <td> Accept </td> 
   <td> Dient zum Ermitteln der vom Browser unterstützten Bildformate, damit unser Webserver nachvollziehen kann, ob er ein GIF- oder ein WBMP-Bild zurücksenden soll. </td> 
  </tr> 
  <tr> 
   <td> Verweisende Stelle </td> 
   <td> Dient als Reserve für den Abruf von Informationen darüber, von welcher Seiten-URL die Datenerfassungsanforderung stammte, falls diese nicht in der Abfragezeichenfolge übergeben wurde oder sich von dem Wert in der Abfragezeichenfolge unterscheidet. </td> 
  </tr> 
  <tr> 
   <td> X-Forwarded-For </td> 
   <td> Dient zum Ermitteln der richtigen IP-Adresse für den Client, von dem die Datenerfassungsanforderung stammte. Anhand der IP-Adresse werden Berichte zur geografischen Region, zum Mobilnetzbetreiber und andere Berichte generiert. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Implementierungen mit dynamischen Variablen haben die Möglichkeit, in anderen, oben nicht aufgeführten HTTP-Anforderungsheadern zu lesen.

## HTTP-Antwortheader {#section_A9C7035198C84037A21A8033CC408F0E}

| **Header** | **Nutzung** |
|---|---|
| Access-Control-Allow-Origin | Hiermit kann in unseren Servern Unterstützung für Datenerfassungsanforderungen aktiviert werden, bei denen Daten zwecks Ressourcensharing aus unterschiedlichen Quellen stammen. |
| Läuft ab | Steuert die Zwischenspeicherung im Browser. |
| Last-Modified | Steuert die Zwischenspeicherung im Browser. |
| Cache-Control | Steuert die Zwischenspeicherung im Browser. |
| Pragma | Steuert die Zwischenspeicherung im Browser. |
| ETag | Steuert die Zwischenspeicherung im Browser. |
| Vary | Steuert die Zwischenspeicherung im Browser. |
| P3P | Gibt die standardmäßige oder benutzerdefinierte P3P-Richtlinie für die Datenerfassungsanforderung an. |
| Status | Enthält den Status „SUCCESS“ oder „FAILURE“ für Anforderungen ohne Inhalte. Wird nur verwendet, wenn laut der Anforderung keine Inhalte zurückgegeben werden sollen. |
| Grund | Enthält den Grund für den Status „Failure“ bei einer Anforderung ohne Inhalte. Wird nur verwendet, wenn laut der Anforderung keine Inhalte zurückgegeben werden sollen. |
| Stelle | Leitet den Client, von dem die Datenerfassungsanforderung stammt, zu einer anderen URL um. Ein Beispiel dazu wäre unser Cookie-Handshake, mit dem festgestellt werden soll, ob das Besucher-ID-Cookie gesetzt werden kann. |
| Content-Type | Gibt den Typ von Inhalt an, der an den Client zurückgesendet wird (GIF, Text, Javascript usw.). |
| Content-Length | Gibt die Größe des Inhalts an, der an den Client zurück gesendet wird. |

>[!NOTE]
>
>Andere HTTP-Header können in der Antwort für die interne Statusüberwachung festgelegt werden. Einige dieser Header werden möglicherweise an den Browser zurückgegeben; es ist jedoch nicht erforderlich, dass diese empfangen werden.
