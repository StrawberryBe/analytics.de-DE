---
description: Zum Überprüfen der ordnungsgemäßen Aktivierung der serverseitigen Weiterleitung müssen Sie die HTTP-Antwort aus der Analytics-Verfolgungsanfrage inspizieren. Dazu können Sie die Entwicklertools eines Browsers oder ein Proxy-Tool wie Charles Web Debugger verwenden. Die folgenden Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um eine ordnungsgemäße Aktivierung der serverseitigen Weiterleitung zu gewährleisten.
seo-description: Zum Überprüfen der ordnungsgemäßen Aktivierung der serverseitigen Weiterleitung müssen Sie die HTTP-Antwort aus der Analytics-Verfolgungsanfrage inspizieren. Dazu können Sie die Entwicklertools eines Browsers oder ein Proxy-Tool wie Charles Web Debugger verwenden. Die folgenden Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um eine ordnungsgemäße Aktivierung der serverseitigen Weiterleitung zu gewährleisten.
seo-title: Überprüfen der Implementierung Ihrer serverseitigen Weiterleitung
solution: Audience Manager
title: Überprüfen der Implementierung Ihrer serverseitigen Weiterleitung
uuid: e 37296 cc -0120-486 a-a 4 ca -78 d 648 cf 6 a 11
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Überprüfen der Implementierung Ihrer serverseitigen Weiterleitung

Zum Überprüfen der ordnungsgemäßen Aktivierung der serverseitigen Weiterleitung müssen Sie die HTTP-Antwort aus der Analytics-Verfolgungsanfrage inspizieren. Dazu können Sie die Entwicklertools eines Browsers oder ein Proxy-Tool wie Charles Web Debugger verwenden. Die folgenden Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um eine ordnungsgemäße Aktivierung der serverseitigen Weiterleitung zu gewährleisten.

So überprüfen Sie den Status der serverseitigen Weiterleitung:

1. Laden Sie eine Testseite mit aktualisiertem AppMeasurement-Code.
1. Überprüfen Sie in den Debugging-Tools Ihres Browsers oder mithilfe Ihrer Proxy-Software die HTTP-Antwort von der Analytics-Verfolgungsanfrage (Sie können ganz einfach danach filtern, indem Sie einen beliebigen Pfad mit „b/ss“ auswählen).
1. Überprüfen Sie die HTTP-Antwort. Wenn die Antwort Audience Manager-Daten enthält (wie unten dargestellt), funktioniert die serverseitige Weiterleitung.

![](assets/ssf-succeed.png)

>[!CAUTION]
>
>If the response contains the key value pair `"status":"SUCCESS"` or a 2 x 2 image, then server-side forwarding * is not* configured correctly. Stellen Sie sicher, dass der Identitätsdienst ordnungsgemäß bereitgestellt ist. Sie haben das App Measurement-Modul bereitgestellt, die anwendbare Report Suite wurde dem richtigen IMS-Org zugeordnet und diese serverseitige Weiterleitung wurde in der Admin-Konsole von Analytics aktiviert.

>[!MORE_ LIKE_ THIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)

