---
title: writeSecureCookies
description: Ermöglicht AppMeasurement das Setzen von Cookies mit dem Secure-Attribut.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 100%

---


# writeSecureCookies

Mit der Variablen `writeSecureCookies` kann AppMeasurement [sichere Cookies](https://en.wikipedia.org/wiki/Secure_cookie) für Analytics einrichten. Diese Einstellung gilt sowohl für Besucher-ID-Cookies, die von AppMeasurement gesetzt werden, als auch für Cookies, die Sie mit der `Util.CookieWrite()`-Methode festlegen. Sie erfordert AppMeasurement 2.18.0 oder höher.

>[!IMPORTANT]
>
>Wenn Sie die Variable `writeSecureCookies` aktivieren, stellen Sie sicher, dass der gesamte Inhalt auf Ihrer Site sicher über HTTPS bereitgestellt wird. AppMeasurement funktioniert nicht, wenn diese Variable aktiviert ist und Sie unsicheren Inhalt auf Ihrer Seite haben.

## Schreiben sicherer Cookies in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.writeSecureCookies in AppMeasurement und im benutzerspezifischen Launch-Code-Editor

Die Variable `s.writeSecureCookies` ist ein boolescher Wert, der bestimmt, ob AppMeasurement beim Erstellen eines Cookies das Secure-Attribut einrichtet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn der gesamte Inhalt auf Ihrer Site sicher ist und Cookies, die von AppMeasurement gesetzt werden, das Secure-Attribut aufweisen sollen.

```js
s.writeSecureCookies = true;
```
