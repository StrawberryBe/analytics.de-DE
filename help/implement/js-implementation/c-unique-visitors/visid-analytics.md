---
description: 'Wenn ein Benutzer Ihre Site besucht, wird ein beständiges Cookie vom Adobe-Webserver gesetzt, indem es in die HTTP-Antwort an den Browser aufgenommen wird. Dieses Cookie wird in der angegebenen Datenerfassungsdomäne gesetzt. '
keywords: Analytics-Implementierung
seo-description: 'Wenn ein Benutzer Ihre Site besucht, wird ein beständiges Cookie vom Adobe-Webserver gesetzt, indem es in die HTTP-Antwort an den Browser aufgenommen wird. Dieses Cookie wird in der angegebenen Datenerfassungsdomäne gesetzt. '
seo-title: Analytics-Besucher-ID
solution: Analytics
title: Analytics-Besucher-ID
topic: Entwickler und Implementierung
uuid: fa 7737 cc -0190-4 d 27-af 1 b -87301 a 715 df 2
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics-Besucher-ID

Wenn ein Benutzer Ihre Site besucht, wird ein beständiges Cookie vom Adobe-Webserver gesetzt, indem es in die HTTP-Antwort an den Browser aufgenommen wird. Dieses Cookie wird in der angegebenen Datenerfassungsdomäne gesetzt. 

Wenn eine Anforderung an den Adobe-Datenerfassungsserver gesendet wird, wird geprüft, ob der Header das Besucher-ID-Cookie (`s_vi`) enthält. Wenn der Cookie in der Anforderung enthalten ist, wird er zur Identifizierung des Besuchers verwendet. Wenn der Cookie nicht in der Anforderung enthalten ist, generiert der Server eine Unique Visitor-ID, setzt diese als Cookie im HTTP-Antwort-Header, und sendet diesen mit der Anforderung zurück. Der Cookie wird im Browser gespeichert und bei nachfolgenden Besuchen auf der Website zurück zum Datenerfassungsserver gesendet, sodass der Besucher bei allen Besuchen identifiziert werden kann.

## Drittanbieter-Cookies und CNAME-Datensätze {#section_61BA46E131004BB2B75929C1E1C93139}

Einige Browser, wie Apple Safari, speichern keine Cookies mehr, die im HTTP-Header gesetzt sind von Domänen, die nicht mit der Domäne der aktuellen Website übereinstimmen (dies ist ein Cookie, das in einem Drittanbieterkontext verwendet wird, bzw. ein Drittanbieter-Cookie). Wenn Ihre Domäne z. B. `mysite.com` ist und sich Ihr Datenerfassungsserver unter der Domäne `mysite.omtrdc.net` befindet, wird der von `mysite.omtrdc.net` im HTTP-Header zurückgegebene Cookie möglicherweise vom Browser abgewiesen.

Um dies zu vermeiden, haben viele Kunden für ihre Datenerfassungsserver CNAME-Einträge als [Erstanbieter-Cookie-Implementierung](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/) implementiert. Wenn ein CNAME-Eintrag so konfiguriert wurde, dass ein Hostname unter der Domäne des Kunden einem Datenerfassungsserver zugeordnet wird (z. B. die Zuordnung von `metrics.mysite.com` zu `mysite.omtrdc.net`), wird der Besucher-ID-Cookie gespeichert, da die Datenerfassungsdomäne nun mit der Domäne der Website übereinstimmt. Somit besteht zwar eine höhere Wahrscheinlichkeit, dass der Besucher-ID-Cookie gespeichert wird, aber es entsteht auch etwas Mehraufwand, da CNAME-Einträge konfiguriert und SSL-Zertifikate für Datenerfassungsserver verwaltet werden müssen.

## Cookies auf Mobilgeräten {#section_7D05AE259E024F73A95C48BD1E419851}

Wenn Mobilgeräte anhand von Cookies nachverfolgt werden, können Sie den Ablauf von Messungen anhand einiger Einstellungen anpassen. Die Lebensdauer von Cookies beträgt fünf Jahre, aber Sie können diesen Standardwert mit der Abfrageparametervariablen für die Lebensdauer von Cookies (`s.cookieLifetime`) andern. Mit der CDP-Abfragezeichenfolge `s.cookieDomainPeriods` können Sie den Cookie-Speicherort für CNAME-Implementierungen festlegen. Der Standardwert ist 2, sofern kein anderer Wert festgelegt wird, und der Standard-Speicherort ist „domain.com“. Bei Implementierungen, die keine CNAME-Einträge verwenden, befindet sich der Speicherort für den Besucher-ID-Cookie unter der Domäne „207.net“.
