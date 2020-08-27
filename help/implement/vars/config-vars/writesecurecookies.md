---
title: writeSecureCookies
description: Ermöglicht AppMeasurement das Setzen von Cookies mit dem Secure-Attribut.
translation-type: tm+mt
source-git-commit: defb701d01747685a421b89a553f47efe40f1432
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 86%

---


# writeSecureCookies

Mit der Variablen `writeSecureCookies` kann AppMeasurement [sichere Cookies](https://en.wikipedia.org/wiki/Secure_cookie) für Analytics einrichten. Diese Einstellung gilt sowohl für Besucher-ID-Cookies, die von AppMeasurement gesetzt werden, als auch für Cookies, die Sie mit der `Util.CookieWrite()`-Methode festlegen. Sie erfordert AppMeasurement 2.18.0 oder höher.

>[!IMPORTANT]
>
>Wenn Sie die Variable `writeSecureCookies` aktivieren, stellen Sie sicher, dass der gesamte Inhalt auf Ihrer Site sicher über HTTPS bereitgestellt wird. AppMeasurement funktioniert nicht, wenn diese Variable aktiviert ist und Sie unsicheren Inhalt auf Ihrer Seite haben.

## Schreiben sicherer Cookies in Adobe Experience Platform Launch

[!UICONTROL Schreiben sicherer Cookies] ist ein Kontrollkästchen unter dem Akkordeon &quot; [!UICONTROL Cookies] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Cookies] &quot;, das das Kontrollkästchen &quot;sichere Cookies  schreiben&quot;anzeigt.

## s.writeSecureCookies in AppMeasurement und im benutzerspezifischen Launch-Code-Editor

Die Variable `s.writeSecureCookies` ist ein boolescher Wert, der bestimmt, ob AppMeasurement beim Erstellen eines Cookies das Secure-Attribut einrichtet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn der gesamte Inhalt auf Ihrer Site sicher ist und Cookies, die von AppMeasurement gesetzt werden, das Secure-Attribut aufweisen sollen.

```js
s.writeSecureCookies = true;
```
