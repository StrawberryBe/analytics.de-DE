---
title: Fehlerbehebung bei Sitzungen in Adobe Analytics
description: Erfahren Sie, wie Sie Probleme bei der Abmeldung von Adobe Analytics beheben können.
feature: Analytics Basics
exl-id: 191250ef-8313-47be-9717-046cce870998
source-git-commit: d3d5b01fe17f88d07a748fac814d2161682837c2
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 99%

---

# Fehlerbehebung bei Sitzungen in Adobe Analytics

Auf dieser Seite finden Sie Informationen zur Fehlerbehebung bei Sitzungen. Bei entsprechenden Problemen können Sie sich zwar erfolgreich anmelden, haben jedoch Schwierigkeiten, angemeldet zu bleiben. Wenn Sie Probleme mit der Anmeldung bei Adobe Analytics haben, lesen Sie [Fehlerbehebung bei Anmeldeproblemen mit Adobe Analytics](troubleshoot-login.md).

Fast alle sitzungsbasierten Probleme haben ihre Ursache im angepassten Unternehmensnetzwerk. Wenn Sie sich bei Adobe Analytics anmelden können, aber Probleme dabei haben, angemeldet zu bleiben, verwenden Sie diesen Artikel, um die Ursache zu ermitteln.

## Bestimmen Sie, ob das Problem auf das Netzwerk Ihres Unternehmens zurückzuführen ist. {#network}

Viele Unternehmen stellen zusätzliche Netzwerkfunktionen bereit, um die Sicherheit zu erhöhen, wie z. B. Proxyserver oder Firewalls. Diese Anpassungen können manchmal die Möglichkeit beeinträchtigen, eine aktive Sitzung in Adobe Analytics beizubehalten.

Um festzustellen, ob das Unternehmensnetzwerk, mit dem Sie verbunden sind, Probleme mit der Verwendung von Adobe Analytics verursacht, verwenden Sie Ihre Experience Cloud-Anmeldedaten auf einem Gerät außerhalb Ihres Unternehmensnetzwerks. Nutzen Sie hierfür beispielsweise Ihr Heimnetzwerk oder den Datenplan eines Mobilgeräts. Wenn Sie erfolgreich von Seite zu Seite wechseln können, ohne abgemeldet zu werden, ist das Netzwerk Ihres Unternehmens der Grund für Ihre Abmeldung bei Adobe Analytics.

## Probleme aufgrund von Proxy {#proxy}

Adobe verwendet bei Anforderungen an Adobe einen Autorisierungs-Header. Einige Proxys wie Edge Secure Web Gateway (früher Bluecoat) entfernen wichtige Informationen vom Autorisierungs-Header, die von Adobe Analytics verwendet werden. Wenn Adobe den Autorisierungs-Header nicht empfängt, läuft die Sitzung ab.

Um dieses Problem zu beheben, empfiehlt Adobe, mit dem IT-Team Ihres Unternehmens zusammenzuarbeiten, um den Autorisierungs-Header über den Proxy Ihres Unternehmens zuzulassen.

>[!NOTE]
>
>Mitglieder der Analytics-Community fanden die folgenden Links hilfreich, die allerdings nicht zu Adobe gehören. Berücksichtigen Sie diese Anmerkung bei der Anzeige der Inhalte.

Informationen zu Symantec-Proxys und Authentifizierungs-Headern finden Sie hier:

* [Konfigurieren der Upstream-Proxy-Authentifizierung in einer Proxy-Kettenbereitstellung auf einer ProxySG- oder ASG-Appliance](https://techdocs.broadcom.com/us/en/symantec-security-software/web-and-network-security/edge-swg/7-3/authentication_co.html)
* [Weiterleiten von Anmeldeinformationen von Benutzern an einen Server hinter der ProxySG-Einheit](https://knowledge.broadcom.com/external/article/165859/how-to-forward-user-credentials-to-a-ser.html)
