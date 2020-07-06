---
title: Fehlerbehebung bei Sitzungen in Adobe Analytics
description: Erfahren Sie, wie Sie Probleme bei der Abmeldung von Adobe Analytics beheben können.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 100%

---


# Fehlerbehebung bei Sitzungen in Adobe Analytics

Auf dieser Seite finden Sie Informationen zur Fehlerbehebung bei Sitzungen. Bei entsprechenden Problemen können Sie sich zwar erfolgreich anmelden, haben jedoch Schwierigkeiten, angemeldet zu bleiben. Wenn Sie Probleme mit der Anmeldung bei Adobe Analytics haben, lesen Sie [Fehlerbehebung bei Anmeldeproblemen mit Adobe Analytics](troubleshoot-login.md).

Fast alle sitzungsbasierten Probleme haben ihre Ursache im angepassten Unternehmensnetzwerk. Wenn Sie sich bei Adobe Analytics anmelden können, aber Probleme dabei haben, angemeldet zu bleiben, verwenden Sie diesen Artikel, um die Ursache zu ermitteln.

## Bestimmen Sie, ob das Problem auf das Netzwerk Ihres Unternehmens zurückzuführen ist.

Viele Unternehmen stellen zusätzliche Netzwerkfunktionen bereit, um die Sicherheit zu erhöhen, wie z. B. Proxyserver oder Firewalls. Diese Anpassungen können manchmal die Möglichkeit beeinträchtigen, eine aktive Sitzung in Adobe Analytics beizubehalten.

Um festzustellen, ob das Unternehmensnetzwerk, mit dem Sie verbunden sind, Probleme mit der Verwendung von Adobe Analytics verursacht, verwenden Sie Ihre Experience Cloud-Anmeldedaten auf einem Gerät außerhalb Ihres Unternehmensnetzwerks. Nutzen Sie hierfür beispielsweise Ihr Heimnetzwerk oder den Datenplan eines Mobilgeräts. Wenn Sie erfolgreich von Seite zu Seite wechseln können, ohne abgemeldet zu werden, ist das Netzwerk Ihres Unternehmens der Grund für Ihre Abmeldung bei Adobe Analytics.

## Probleme aufgrund von Proxy

Adobe verwendet bei Anforderungen an Adobe einen Autorisierungs-Header. Einige Proxies wie Bluecoat (jetzt im Besitz von Symantec) entfernen wichtige Informationen aus dem Autorisierungs-Header, die von Adobe Analytics verwendet werden. Wenn Adobe den Autorisierungs-Header nicht empfängt, läuft die Sitzung ab.

Um dieses Problem zu beheben, empfiehlt Adobe, mit dem IT-Team Ihres Unternehmens zusammenzuarbeiten, um den Autorisierungs-Header über den Proxy Ihres Unternehmens zuzulassen.

>[!NOTE]
>
>Mitglieder der Analytics-Community fanden die folgenden Links hilfreich, die allerdings nicht zu Adobe gehören. Berücksichtigen Sie diese Anmerkung bei der Anzeige der Inhalte.

Informationen zu Symantec-Proxies und Authentifizierungs-Headern finden Sie hier:

* [Konfigurieren der Upstream-Proxy-Authentifizierung in einer Proxy-Kettenbereitstellung auf einer ProxySG- oder ASG-Appliance](https://support.symantec.com/en_US/article.TECH246122.html)
* [ProxySG immer erlauben, den Server-Autorisierungs-Upstream weiterzuleiten](https://support.symantec.com/en_US/article.TECH244708.html)
