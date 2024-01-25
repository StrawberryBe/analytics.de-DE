---
description: Zum Überprüfen der ordnungsgemäßen Aktivierung der serverseitigen Weiterleitung müssen Sie die HTTP-Antwort aus der Analytics-Verfolgungsanfrage inspizieren. Diese Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um sicherzustellen, dass die serverseitige Weiterleitung ordnungsgemäß aktiviert ist.
solution: Analytics
title: Überprüfen der Server-seitigen Weiterleitungsimplementierung
feature: Server-Side Forwarding
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 86%

---

# Überprüfen der serverseitigen Weiterleitungsimplementierung

Zum Überprüfen der ordnungsgemäßen Aktivierung der serverseitigen Weiterleitung müssen Sie die HTTP-Antwort aus der Analytics-Verfolgungsanfrage inspizieren. Dazu können Sie die Entwicklertools eines Browsers oder ein Proxy-Tool wie Charles Web Debugger verwenden. Die folgenden Anweisungen zeigen, welche Indikatoren vorhanden sein müssen, um sicherzustellen, dass die serverseitige Weiterleitung ordnungsgemäß aktiviert ist.

So überprüfen Sie den Status der serverseitigen Weiterleitung:

1. Laden Sie eine Testseite mit aktualisiertem AppMeasurement-Code.
1. Überprüfen Sie in den Debugging-Tools Ihres Browsers oder mithilfe Ihrer Proxy-Software die HTTP-Antwort von der Analytics-Verfolgungsanfrage (Sie können ganz einfach danach filtern, indem Sie einen beliebigen Pfad mit „b/ss“ auswählen).
1. Überprüfen Sie die HTTP-Antwort. Wenn die Antwort Audience Manager-Daten enthält (wie unten dargestellt), funktioniert die serverseitige Weiterleitung.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>Wenn die Antwort das Schlüssel/Wert-Paar „`"status":"SUCCESS"`“ oder ein 2-x-2-Bild enthält, ist die serverseitige Weiterleitung nicht korrekt konfiguriert. Stellen Sie sicher, dass der Identity Service ordnungsgemäß bereitgestellt ist, dass Sie das AppMeasurement-Modul bereitgestellt haben, dass die jeweilige Report Suite der korrekten Organisations-ID zugewiesen wurde und dass die Server-seitige Weiterleitung in den Analytics Admin-Tools aktiviert wurde.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)
