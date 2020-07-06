---
description: Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Durch das Ausschließen von Daten nach der IP-Adresse wird die Genauigkeit der Berichte erhöht. Zudem können Sie Daten entfernen, die auf DoS-Angriffen oder anderen böswilligen Ereignissen beruhen und Ihre Berichte verfälschen könnten. Die Ausschlüsse lassen sich wahlweise oder über die Firewall konfigurieren.
title: Nach IP-Adresse ausschließen
topic: Admin tools
uuid: 1ed6105f-e7c5-4c4f-b8f4-e5f66d0824bb
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 100%

---


# Nach IP-Adresse ausschließen

Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Durch das Ausschließen von Daten nach der IP-Adresse wird die Genauigkeit der Berichte erhöht. Zudem können Sie Daten entfernen, die auf DoS-Angriffen oder anderen böswilligen Ereignissen beruhen und Ihre Berichte verfälschen könnten. Die Ausschlüsse lassen sich wahlweise oder über die Firewall konfigurieren.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Nach IP ausschließen]**

>[!NOTE]
>
>Treffer, die nach IP-Adresse ausgeschlossen sind, werden als [Serveraufrufe](https://docs.adobe.com/content/help/de-DE/analytics/technotes/terms.html) in Rechnung gestellt.

## Ausschließen nach Cookie {#section_FB5A20AB5E514DA6BC596CC67F6A3A4C}

Hiermit schließen Sie diesen Computer von der Rückverfolgung in Ihrem Konto aus. Wenn Sie Ihren Computer ausschließen möchten, werden alle von Ihrem Computer erzeugten Daten nicht gezählt.

Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne die Traffic-Daten zu verfälschen. Diese Funktion können Sie nutzen, wenn Sie nicht über eine statische IP-Adresse verfügen (z. B. über DFÜ-Verbindung mit dem ISP) und sich selbst aus den Kontendaten ausschließen möchten.

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL CNAME hinzufügen] | Erzeugt einen Ausschluss-Link, mit dem Sie Ihre Domäne ausschließen. Wenden Sie sich zwecks Hilfe an die Support-Benutzer in Ihrem Unternehmen. <br>Sie können Ihren Datenverkehr aus der Berichterstattung in Ihren Report Suites ausschließen, indem Sie die Opt-out-Seite Ihres Unternehmens aufrufen und dort Ihren Browser aus der Messung ausschließen. <br>Wenn bei Ihrer Implementierung Cookies von Drittanbietern verwendet werden, finden Sie Ihre Opt-out-Seite [hier](https://democorp.112.2o7.net/optout.html?locale=de_DE&amp;popup=true). |

>[!NOTE]
>
>Der Ausschluss nach Computer funktioniert nur dann, wenn:
>
> * Sie von derselben Workstation aus auf Ihre Website zugreifen.
> * Cookies im derzeit verwendeten Browser aktiviert sind.
> * Ihre Cookies nicht gelöscht wurden. Beim Löschen der Cookies müssen Sie sich selbst ausschließen.


## Nach IP-Adresse ausschließen {#section_609FB6461529409D840111A32FEF5C3D}

Eine IP-Adresse ist eine Internet-Adresse. Allen Internetbenutzern wird eine numerische IP-Adresse zugewiesen (in der Regel durch Internetdienstanbieter), die als elektronische Kennung fungiert.

Seitenansichten und individuelle Seitenbesucher werden anhand ihrer IP-Adressen gezählt bzw. identifiziert. Indem Sie IP-Adressen aus der Erfassung ausschließen, können Sie verhindern, dass Adobe die Aktivität häufiger Besucher verfolgt. Mit dieser Funktion können Sie und Ihre Kollegen Ihre Website besuchen, ohne dadurch die Traffic-Daten zu verfälschen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.

Mit Platzhaltern (*) können Sie einen ganzen Adressenbereich ausschließen. Zum Beispiel würde `[!DNL 0.0.*.0]` sämtliche IP-Adressen zwischen `[!DNL 0.0.0.0]` und `[!DNL 0.0.255.0]` ausschließen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.

## Ausschließen nach Firewall {#section_3E7BFB71ADD941D39F923DB9557AD9CD}

Sie können die Datenerfassung auch mithilfe einer Firewall für bestimmte IP-Adressen sperren.

Weitere Informationen finden Sie im Artikel [In der Experience Cloud verwendete IP-Adressen](https://helpx.adobe.com/de/analytics/kb/adobe-ip-addresses.html).

## Auswirkung der IP-Verschleierung {#section_51B7529FFF16449CA016FDC51D87E2CA}

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten angepasst werden, um IP-Adressen mit einer Null am Ende zu berücksichtigen. Übereinstimmung * sollte mit 0 übereinstimmen.
