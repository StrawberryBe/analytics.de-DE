---
description: Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Das Ausschließen von Daten verbessert die Genauigkeit von Berichten, indem IP-Adressdaten ausgeschlossen werden. Darüber hinaus können Sie Daten aus der Dienstblockade oder anderen böswilligen Ereignissen entfernen, die Berichtdaten verfälschen können. Sie können den Ausschluss konfigurieren oder Ihre Firewall verwenden.
title: Nach IP-Adresse ausschließen
topic: Admin tools
uuid: 1ed6105f-e7c5-4c4f-b8f4-e5f66d0824bb
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Nach IP-Adresse ausschließen

Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Das Ausschließen von Daten verbessert die Genauigkeit von Berichten, indem IP-Adressdaten ausgeschlossen werden. Darüber hinaus können Sie Daten aus der Dienstblockade oder anderen böswilligen Ereignissen entfernen, die Berichtdaten verfälschen können. Sie können den Ausschluss konfigurieren oder Ihre Firewall verwenden.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Exclude by IP]**

>[!NOTE] Treffer, die nach IP-Adresse ausgeschlossen sind, werden als [Serveraufrufe](https://marketing.adobe.com/resources/help/de_DE/reference/primary_server_calls.html) in Rechnung gestellt.

## Ausschließen nach Cookie {#section_FB5A20AB5E514DA6BC596CC67F6A3A4C}

Hiermit können Sie diesen Computer von der Verfolgung in Ihrem Konto ausschließen. Wenn Sie Ihren Computer ausschließen, werden alle von Ihrem Computer erzeugten Daten nicht gezählt.

Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne die Traffic-Daten zu verfälschen. Sie können diese Funktion verwenden, wenn Sie keine statische IP-Adresse haben (z. B. eine DFÜ-Verbindung über einen Dienstleister) und sich selbst aus Ihren Kontodaten ausschließen möchten.

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL Add CNAME] | Erstellt einen Ausschluss-Link, den Sie zum Ausschluss Ihrer Domäne verwenden können. Wenden Sie sich zwecks Hilfe an die Support-Benutzer in Ihrem Unternehmen. <br>Sie können Ihren Datenverkehr aus der Berichterstattung in Ihren Report Suites ausschließen, indem Sie die Opt-out-Seite Ihres Unternehmens aufrufen und dort Ihren Browser aus der Messung ausschließen. <br>Wenn bei Ihrer Implementierung Cookies von Drittanbietern verwendet werden, finden Sie Ihre Opt-out-Seite [hier](https://democorp.112.2o7.net/optout.html?locale=de_DE&amp;popup=true). |

>[!NOTE] Der Ausschluss nach Computer funktioniert nur dann, wenn:
>
> * Sie von derselben Workstation aus auf Ihre Website zugreifen.
> * Cookies im derzeit verwendeten Browser aktiviert sind.
> * Ihre Cookies nicht gelöscht wurden.   Beim Löschen der Cookies müssen Sie sich selbst ausschließen.


## Nach IP-Adresse ausschließen {#section_609FB6461529409D840111A32FEF5C3D}

Eine IP-Adresse ist eine Internetadresse. Allen Internetbenutzern wird eine numerische IP-Adresse zugewiesen (in der Regel durch Internetdienstanbieter), die als elektronische Kennung fungiert.

Seitenzahlen werden gezählt und individuelle Besucher werden über IP-Adressen identifiziert. Indem Sie IP-Adressen ausschließen, können Sie verhindern, dass Adobe häufige Besucher verfolgt. Diese Funktion ermöglicht es Ihnen und Ihren Kollegen, Ihre Site zu besuchen, ohne die Traffic-Daten zu verfälschen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.

Sie können Platzhalterzeichen (*) verwenden, um eine Reihe von Adressen auszuschließen. Zum Beispiel würde `[!DNL 0.0.*.0]` sämtliche IP-Adressen zwischen `[!DNL 0.0.0.0]` und `[!DNL 0.0.255.0]` ausschließen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.

## Ausschließen nach Firewall {#section_3E7BFB71ADD941D39F923DB9557AD9CD}

Sie können die Datenerfassung auch mithilfe einer Firewall für bestimmte IP-Adressen sperren.

Siehe [IP-Adressen, die im Artikel Experience Cloud](https://marketing.adobe.com/resources/help/de_DE/home/index.html#kb-adobe-ip-addresses) verwendet werden.

## Auswirkung der IP-Verschleierung {#section_51B7529FFF16449CA016FDC51D87E2CA}

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, erfolgt dies vor der IP-Filterung. Daher wird das letzte Oktett durch den Wert 0 ersetzt, und die Regeln zum IP-Ausschluss sollten aktualisiert werden, damit IP-Adressen mit einer Null am Ende übereinstimmen. Übereinstimmung * sollte mit 0 übereinstimmen.
