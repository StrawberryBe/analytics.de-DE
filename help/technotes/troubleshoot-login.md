---
title: Fehlerbehebung bei der Anmeldung bei Adobe Analytics
description: Schritte für den Fall, dass Sie sich nicht bei Adobe Analytics anmelden können.
exl-id: e670a043-c55b-4717-9b60-613ea4d04382
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 2%

---

# Fehlerbehebung bei der Anmeldung bei Adobe Analytics

Adobe Analytics verwendet mehrere Authentifizierungsmethoden, um sich anzumelden:

* Adobe ID durch das Experience Cloud
* Legacy-Analytics-ID
* Single Sign-On

**Wenn Sie regelmäßig auf Analytics und zufällig auftretende Beginn zugreifen und Probleme bei der Anmeldung auftreten, werden die meisten Probleme durch Löschen der Cookies und des Cache des Browsers behoben.**

In einigen Fällen können Probleme mit der Verfügbarkeit die Möglichkeit zur Anmeldung beeinträchtigen. Überprüfen Sie [status.adobe.com](https://status.adobe.com) auf offene Fälle. Verwenden Sie andernfalls den entsprechenden Abschnitt, der von der Authentifizierungsmethode Ihres Unternehmens abhängt.

## Adobe ID

Beheben Sie Probleme bei der Anmeldung bei Adobe Analytics mit dem Experience Cloud.

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com). Wenn Sie nicht auf diese Site zugreifen können, wird diese Domäne von Ihrem Unternehmen möglicherweise nicht über Ihre Firewall zugelassen. Wenden Sie sich an das IT-Team Ihres Unternehmens, um dies zuzulassen. Unter [IPs und Domänen, die im Adobe Experience Cloud](https://helpx.adobe.com/de/analytics/kb/adobe-ip-addresses.html) verwendet werden, finden Sie hilfreiche Informationen für Ihr IT-Team.

2. Authentifizierung mit Adobe ID: Klicken Sie auf **[!UICONTROL Anmelden mit einem Adobe ID]**. Wenn Sie sich nicht anmelden können, überprüfen Sie bei der Dublette, ob Ihre E-Mail-Adresse korrekt eingegeben wurde. Klicken Sie andernfalls auf **[!UICONTROL Kennwort zurücksetzen]** und befolgen Sie die Anweisungen zum Zurücksetzen des Adobe ID-Kennworts.

3. Zugriff auf Analytics nach der Authentifizierung: Klicken Sie oben rechts auf das 9-Raster-Symbol und dann auf Analytics. Wenn Sie diese Option nicht haben oder sie ausgegraut ist, wenden Sie sich an einen Produktadministrator in Ihrem Unternehmen, um sicherzustellen, dass Sie über die richtigen Berechtigungen für den Zugriff auf Analytics verfügen.

## Legacy-Analytics-ID

Ein Benutzer in Ihrer Organisation kann die folgende Fehlermeldung erhalten, wenn er versucht, sich anzumelden:

*Als Sicherheitsmaßnahme wurde dieses Konto aufgrund zu vieler fehlgeschlagener Anmeldeversuche gesperrt.*

Wenn das Problem durch Löschen der Cookies/des Cache des Browsers nicht behoben wird, setzen Sie das Kennwort des Benutzers mit einem Analytics-Administrator in Ihrem Unternehmen zurück.

>[!IMPORTANT]
>
>Die folgenden Schritte zum Zurücksetzen des Passworts eines Benutzers gelten nur für Legacy-Analytics-IDs, nicht für Adobe ID. Wenn Ihr Unternehmen Adobe ID verwendet, können Sie Benutzerkonten unter [adminconsole.adobe.com](https://adminconsole.adobe.com) verwalten.

1. Melden Sie sich bei Adobe Analytics mit einem Konto an, das über Administratorrechte verfügt.
2. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Benutzerverwaltung]**.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Benutzer]** und dann auf **[!UICONTROL Bearbeiten]** neben dem gewünschten Benutzer.
4. Ändern Sie das Kennwort in einen beliebigen Wert und aktivieren Sie das Kontrollkästchen **[!UICONTROL Erfordert Passwortänderung durch den Benutzer bei der nächsten Anmeldung]**.
5. Informieren Sie den Benutzer über das neue Kennwort.

## Single Sign-On

Wenden Sie sich an einen Administrator in Ihrer Organisation, um Single Sign-On-Probleme zu lösen.

## Abgelaufene Anmeldungen

Ein Benutzer in Ihrer Organisation kann die folgende Fehlermeldung erhalten, wenn er versucht, sich anzumelden:

*Fehler: Diese Anmeldung ist abgelaufen.*

Dieser Fehler funktioniert wie beabsichtigt. Adobe Analytics bietet Administratoren die Möglichkeit, einen Datumsbereich festzulegen, in dem ein Benutzerkonto gültig ist. Wenn das aktuelle Datum außerhalb des gültigen Datumsbereichs für das Konto liegt, können sie sich nicht anmelden. Wenden Sie sich an einen Analytics-Administrator in Ihrem Unternehmen, um den gültigen Datumsbereich der Anmeldung zu erweitern. Adobe Die Kundenunterstützung ist nicht berechtigt, gültige Anmeldedatumsbereiche für Benutzerkonten zu ändern.

## Andere Anmeldeprobleme

Wenn keiner der oben genannten Schritte funktioniert, ermitteln Sie den Umfang des Anmeldeproblems:

* Tritt das Problem bei der Verwendung eines anderen Browsers auf, oder ist es in allen Browsern vorhanden?
* Tritt das Problem auf einem anderen Computer im Netzwerk auf oder ist es auf mehreren Computern vorhanden?
* Versuchen Sie, sich mit einem anderen Netzwerk wie einer mobilen Datenverbindung, einer Bibliothek oder einem Heimnetzwerk anzumelden. Ist das Problem netzübergreifend vorhanden?

Wenn das Problem in Ihrem Netzwerk isoliert ist, wenden Sie sich an das IT-Team Ihres Unternehmens, um es zu beheben. Wenden Sie sich an den Kundendienst der Adobe, wenn Sie nicht auf ein einzelnes Netzwerk beschränkt sind.
