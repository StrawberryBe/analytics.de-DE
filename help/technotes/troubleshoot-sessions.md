---
title: Fehlerbehebung für Sitzungen in Adobe Analytics
description: Erfahren Sie, wie Probleme bei der Abmeldung von Adobe Analytics gelöst werden.
seo-title: Fehlerbehebung für Sitzungen in Adobe Analytics
seo-description: Erfahren Sie, wie Probleme bei der Abmeldung von Adobe Analytics gelöst werden.
translation-type: tm+mt
source-git-commit: b5e3801454dafbcc47b93e65f8b5e7c59c3a8081

---


# Fehlerbehebung für Sitzungen in Adobe Analytics

Diese Seite enthält die Fehlerbehebung für Sitzungen, d. h. Sie können sich erfolgreich anmelden, aber weiterhin Probleme haben. If you are having issues logging in to Adobe Analytics, see [Troubleshoot logging in to Adobe Analytics](troubleshoot-login.md).

Fast alle sitzungsbasierten Probleme stammen aus dem benutzerdefinierten Unternehmensnetzwerk. Wenn Sie sich bei Adobe Analytics anmelden können, aber Probleme bei der Anmeldung haben, verwenden Sie diesen Artikel, um die Ursache zu bestimmen.

## Stellen Sie fest, ob das Problem auf das Netzwerk Ihres Unternehmens zurückzuführen ist.

Viele Unternehmen stellen zusätzliche Netzwerkfunktionen bereit, um die Sicherheit wie Proxy-Server oder Firewalls zu verbessern. Diese Anpassungen können manchmal die Fähigkeit beeinträchtigen, eine aktive Sitzung in Adobe Analytics beizubehalten.

Um festzustellen, ob das Unternehmensnetzwerk, mit dem Sie verbunden sind, Probleme bei der Verwendung von Adobe Analytics verursacht, verwenden Sie die Experience Cloud-Anmeldeinformationen auf einem Gerät außerhalb Ihres Unternehmensnetzwerks. Beispiele für Geräte können Ihr Heimnetzwerk oder der Datenplan eines Mobilgeräts sein. Wenn Sie ohne Abmeldung erfolgreich von Seite zu Seite wechseln können, ist das Netzwerk Ihres Unternehmens wahrscheinlich der Grund dafür, warum Sie aus Adobe Analytics abgemeldet werden.

## Probleme aufgrund von IP-Pooling

Einige Netzwerke verwenden eine Praxis namens IP-Pooling, bei der die IP-Adresse eines Geräts häufig in einem von der Organisation verwendeten Bereich geändert werden kann. Wenn eine IP-Adresse im Rahmen der Adobe-Sicherheitspraktiken mitten in der Sitzung geändert wird, ist diese Sitzung abgelaufen.

Wenn Ihr Unternehmen IP-Pooling verwendet, verwenden Sie die folgenden Anweisungen, um Ihre IP-Bereiche zur Whitelist von Adobe hinzuzufügen:

1. Arbeiten Sie mit dem IT-Team Ihres Unternehmens zusammen, um eine Liste der in Ihrer Organisation verwendeten IP-Bereiche abzurufen.
2. Bitten Sie einen Kundensupport-Stellvertreter, Adobe Kundenunterstützung zu kontaktieren und Adobe den IP-Bereichen bereitzustellen.
3. Der Agent gibt die IP-Bereiche in eine Whitelist ein, um zu verhindern, dass Sitzungen ablaufen, wenn sich beide Adressen innerhalb der angegebenen Bereiche befinden.

## Probleme aufgrund des Proxy

Adobe verwendet beim Anfordern von Anforderungen an Adobe eine Autorisierungskopfzeile. Einige Proxys, wie Bluecoat (jetzt im Besitz von Symantec), entfernen wichtige Autorisierungsheader-Informationen, die von Adobe Analytics verwendet werden. Wenn Adobe die Autorisierungskopfzeile nicht sieht, ist die Sitzung abgelaufen.

Um dieses Problem zu beheben, empfiehlt Adobe die Zusammenarbeit mit dem IT-Team Ihres Unternehmens, um die Autorisierung über den Proxy Ihres Unternehmens zuzulassen.

> [!NOTE] Hinweis
>
> Obwohl Mitglieder der Analytics-Community die folgenden Links hilfreich gefunden haben, befinden sie sich nicht von Adobe. Beachten Sie diese Hinweise bei der Anzeige ihres Inhalts.

Informationen zu Symantec-Proxys und Authentifizierungskopfzeilen finden Sie hier:

* [Upstream Proxy-Authentifizierung in einer Proxy-Chain-Bereitstellung auf einem proxysg oder ASG-Appgerät konfigurieren](https://support.symantec.com/en_US/article.TECH246122.html)
* [Proxysg darf Serverautorisierung immer vorwärts weiterleiten](https://support.symantec.com/en_US/article.TECH244708.html)
