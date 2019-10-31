---
title: Fehlerbehebung bei Sitzungen in Adobe Analytics
description: Erfahren Sie, wie Sie Probleme bei der Abmeldung von Adobe Analytics lösen können.
seo-title: Fehlerbehebung bei Sitzungen in Adobe Analytics
seo-description: Erfahren Sie, wie Sie Probleme bei der Abmeldung von Adobe Analytics lösen können.
translation-type: tm+mt
source-git-commit: 5df7bc43587deed41786f6c85f472fb6f908caf8

---


# Fehlerbehebung bei Sitzungen in Adobe Analytics

Auf dieser Seite finden Sie Informationen zur Fehlerbehebung, d. h. Sie können sich erfolgreich anmelden, haben aber Probleme bei der Anmeldung. Wenn Sie Probleme bei der Anmeldung bei Adobe Analytics haben, lesen Sie [Fehlerbehebung bei der Anmeldung bei Adobe Analytics](troubleshoot-login.md).

Fast alle sitzungsbasierten Probleme stammen aus dem angepassten Unternehmensnetzwerk eines Unternehmens. Wenn Sie sich bei Adobe Analytics anmelden können, aber Probleme beim Anmelden haben, verwenden Sie diesen Artikel, um die Ursache zu ermitteln.

## Bestimmen Sie, ob das Problem auf das Netzwerk Ihres Unternehmens zurückzuführen ist.

Viele Unternehmen stellen zusätzliche Netzwerkfunktionen bereit, um die Sicherheit zu erhöhen, wie z. B. Proxyserver oder Firewalls. Diese Anpassungen können manchmal die Möglichkeit beeinträchtigen, eine aktive Sitzung in Adobe Analytics beizubehalten.

Um festzustellen, ob das Unternehmensnetzwerk, mit dem Sie verbunden sind, Probleme mit der Verwendung von Adobe Analytics verursacht, verwenden Sie Ihre Experience Cloud-Anmeldedaten auf einem Gerät außerhalb Ihres Unternehmensnetzwerks. Beispiele für Geräte können über Ihr Heimnetzwerk oder den Datenplan eines Mobilgeräts erfolgen. Wenn Sie erfolgreich von Seite zu Seite wechseln können, ohne abgemeldet zu werden, ist das Netzwerk Ihres Unternehmens der Grund für Ihre Abmeldung bei Adobe Analytics.

## Probleme aufgrund von Proxy

Adobe verwendet bei Anforderungen an Adobe einen Autorisierungs-Header. Einige Proxys wie Bluecoat (jetzt im Besitz von Symantec) entfernen wichtige Header-Informationen zur Autorisierung, die von Adobe Analytics verwendet werden. Wenn Adobe den Autorisierungsheader nicht anzeigt, läuft die Sitzung ab.

Um dieses Problem zu beheben, empfiehlt Adobe, mit dem IT-Team Ihres Unternehmens zusammenzuarbeiten, um den Autorisierungs-Header über den Proxy Ihres Unternehmens zuzulassen.

> [!NOTE] Mitglieder der Analytics-Community fanden die folgenden Links hilfreich, die allerdings nicht zu Adobe gehören. Berücksichtigen Sie diese Anmerkung bei der Anzeige der Inhalte.

Informationen zu Symantec-Proxys und Authentifizierungskopfzeilen finden Sie hier:

* [Konfigurieren der Upstream-Proxyauthentifizierung in einer Proxykettenbereitstellung auf einer ProxySG- oder ASG-Einheit](https://support.symantec.com/en_US/article.TECH246122.html)
* [ProxySG immer die Serverautorisierung vorwärts weiterleiten](https://support.symantec.com/en_US/article.TECH244708.html)
