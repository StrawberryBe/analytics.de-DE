---
title: writeSecureCookies
description: Ermöglicht AppMeasurement das Setzen von Cookies mit dem Secure-Attribut.
feature: Variables
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '242'
ht-degree: 100%

---

# writeSecureCookies

Mit der Variablen `writeSecureCookies` kann AppMeasurement [sichere Cookies](https://en.wikipedia.org/wiki/Secure_cookie) für Analytics einrichten. Diese Einstellung gilt sowohl für Besucher-ID-Cookies, die von AppMeasurement gesetzt werden, als auch für Cookies, die Sie mit der `Util.CookieWrite()`-Methode festlegen. Sie erfordert AppMeasurement 2.18.0 oder höher.

`writeSecureCookies` gilt nur für Cookies, die von AppMeasurement-JavaScript (`s_fid`, `s_cc` und `s_sq`) gesetzt werden. Cookies, die von der `https`-Antwort (`s_vi` und `s_ecid`) gesetzt werden, können auf „sicher“ gesetzt werden, indem Sie sich an die Kundenunterstützung von Adobe wenden.

Weitere Informationen zu Analytics-Cookies finden Sie [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=de).

>[!IMPORTANT]
>
>Wenn Sie die Variable `writeSecureCookies` aktivieren, stellen Sie sicher, dass der gesamte Inhalt auf Ihrer Site sicher über HTTPS bereitgestellt wird. AppMeasurement funktioniert nicht, wenn diese Variable aktiviert ist und Sie unsicheren Inhalt auf Ihrer Seite haben.

## Schreiben sicherer Cookies mithilfe von Tags in Adobe Experience Platform

[!UICONTROL Sichere Cookies schreiben] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Kontrollkästchen [!UICONTROL Sichere Cookies schreiben] angezeigt wird.

## s.writeSecureCookies in AppMeasurement und im benutzerspezifischen Code-Editor

Die Variable `s.writeSecureCookies` ist ein boolescher Wert, der bestimmt, ob AppMeasurement beim Erstellen eines Cookies das Secure-Attribut einrichtet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn der gesamte Inhalt auf Ihrer Site sicher ist und Cookies, die von AppMeasurement gesetzt werden, das Secure-Attribut aufweisen sollen.

```js
s.writeSecureCookies = true;
```
