---
title: Ende der Lebensdauer für IP-Anmeldebeschränkungen [!UICONTROL erzwingen]
description: Erfahren Sie mehr über den Ablauf und die Auswirkungen auf die [!UICONTROL Erzwingung von IP-Anmeldebeschränkungen]
translation-type: tm+mt
source-git-commit: 490a856effac7ec3ff2430dff0ffdcee587bf933

---


# Ende der Lebensdauer für IP-Anmeldebeschränkungen [!UICONTROL erzwingen]

Mit der Funktion IP-Anmeldebeschränkungen **[erzwingen](/help/admin/company/security-manager.md)** in Adobe Analytics können Sie bestimmte IP-Adressen (die als sicher gelten) auf eine Positivliste setzen, um eine erfolgreiche Anmeldung und den Zugriff auf Ihre Adobe Analytics-Umgebung zu ermöglichen. In vielen Fällen wird diese Funktion verwendet, um eine Unternehmens-IP-Adresse als einzige sichere IP-Adresse einzurichten, von der aus Benutzer sich anmelden können. Um Adobe Analytics verwenden zu können, müssen sich die Benutzer daher entweder in einer Firmenzentrale befinden oder sich über VPN im Netzwerk anmelden.

Wir planen, diese Funktion im Oktober 2020 zu beenden.

## Warum sind wir am Ende dieser Funktion?

Diese Funktion wird unter bestimmten Umständen durch die Migration der Experience Cloud-Anmeldung und/oder die Experience Cloud-Anmeldung unterbrochen. Es ist bekannt, dass es für Kunden mit **[!UICONTROL Kundenattributen]** oder **[!UICONTROL Zielgruppenbibliothek]** beschädigt wird.

Wenn Sie über mehrere Experience Cloud-Lösungen verfügen, können Sie diese Anforderung umgehen, indem Sie sich mit einer der anderen Lösungen bei der Experience Cloud anmelden, da diese Funktion außerhalb von Analytics selbst nicht vorhanden ist oder nicht unterstützt wird. Benutzer können dies auch über IP-Spoofing umgehen.

Schließlich verfügt Adobe über eine funktionierende und weitaus überlegene Alternativlösung mit Single-Sign-On- und Federated-IDs. Diese Funktion bietet Ihnen mehr Kontrolle und Sicherheit über die Anmeldeerfahrung Ihrer Benutzer. Weitere Informationen finden Sie unten.

## Wie wirkt sich das Entfernen dieser Funktion auf Sie aus?

Für alle Kunden, die IP-Anmeldebeschränkungen **[!UICONTROL erzwingen]** , wird diese Funktion im Oktober 2020 entfernt. Zu diesem Zeitpunkt werden noch geltende IP-Anmeldebeschränkungen nicht mehr erzwungen. Wenn Sie die Anmeldung weiterhin nach IP-Adresse beschränken müssen, sollten Sie die empfohlene Lösung für Single-Sign-On und Federated IDs (weitere Informationen und Ressourcen unten) überprüfen und implementieren.

Außerdem wird die Einstellung IP-Anmeldebeschränkungen **** erzwingen aus der **[!UICONTROLABenutzeroberfläche von Analytics unter "dmin"&gt; "Unternehmenseinstellungen"&gt; "Sicherheitsmanager]** "entfernt (siehe unten).

![](assets/sec-manager2.png)

## Welche anderen Optionen haben Sie?

Wie oben erläutert, wird diese Analytics-Funktion beendet. Damit Sie Zeit haben, SSO- und Federated IDs zu implementieren, haben wir das EOL-Datum auf Oktober 2020 verschoben.

Sowohl SSO- als auch Federated IDs sind überlegene Lösungen für die IP-Anmeldebeschränkung, die wir heute haben, und bieten Ihnen mehr Kontrolle, Sicherheit und Funktionen. Informationen zum Einrichten von SSO/Federated IDs finden Sie in der folgenden Hilfedokumentation. Sie sollten diese gründlich lesen und mit Ihrer IT-Abteilung zusammenarbeiten, um sie implementieren zu können:

* [Single Sign-On und die Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [Admin-Konsole - Dokumentation zur Identitätseinrichtung](https://helpx.adobe.com/enterprise/using/set-up-identity.html)
* [Admin-Konsole - Lernprogramm zur Identitätseinrichtung (Video)](https://helpx.adobe.com/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Übungen zur Konfiguration von Federated ID (Video)](https://helpx.adobe.com/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Single-Sign-On - häufige Fragen](https://helpx.adobe.com/enterprise/using/sso-faq.html)
* [Von Adobe unterstützte Identitätstypen](https://helpx.adobe.com/enterprise/using/identity.html)

Wenn Sie weiterhin Ihre Unterstützung für IP-Anmeldebeschränkungen äußern und beantragen möchten, dass diese von Experience Cloud bereitgestellt wird, können Sie auf unserer [Forumsseite](https://forums.adobe.com/ideas/11648)für diese Funktion stimmen.