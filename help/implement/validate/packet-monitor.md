---
title: Paket-Analyzer
description: Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.
keywords: packet sniffer, http status, 200, 302, charles
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 60%

---


# Paket-Analyzer

Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.

Ähnlich dem Adobe Experience Cloud-Debugger zeigen Paketmonitore an, welche Datenparameter bei einer Bildanforderung übertragen werden. Paketmonitore bieten jedoch zusätzliche Funktionen:

* Anzeige von Bildanforderungen aus benutzerspezifischen Linktracking
* Anzeige von Bildanforderungen mit anderen Implementierungsmethoden als JavaScript (wie z. B. fest programmierte Bildanforderungen oder [!DNL Appmeasurement])

Zur Anzeige von Analytics-Anforderungen müssen Sie ausgehende Anforderungen mit „b/ss“ filtern.

In sehr seltenen Fällen meldet der Debugger eine Bildanforderung, obwohl keine solche Anforderung bei den [!DNL Analytics]-Verarbeitungsserver von Adobe einging. Mit einem Paketmonitor können Sie sich hundertprozentig sicher sein, dass eine bestimmte Bildanforderung erfolgreich veranlasst wird.

Adobe stellt zwar keinen offiziellen Paketmonitor bereit, jedoch finden Sie eine große Auswahl im Internet. Nachfolgend sind einige brauchbare Paketmonitore aufgeführt.

>[!TIP]
>
>Die Liste ist nicht vollständig, sondern dient zur Angabe häufig eingesetzter Monitore.

| Firefox | Internet Explorer | Chrome | Eigenständige Programme |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tamper Data](https://addons.mozilla.org/en-us/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe unterstützt oder behebt KEINE Probleme, die bei diesen Paketmonitoren auftreten. Hilfe erhalten Sie auf der Website des Paketbildschirms.

## Typische HTTP-Antwortstatuscodes

Wenn AppMeasurement Daten an Datenerfassungsserver der Adobe sendet, reagieren die Server mit einem Antwortstatuscode.

* **200 OK**: Die häufigste Antwort von Datenerfassungsservern. Die Bildanforderung wurde erfolgreich empfangen und ein transparentes Bild wurde zurückgegeben.
* **302 GEFUNDEN**: Es gibt mehrere mögliche Gründe, warum Sie diese Antwort erhalten:
   * Die erste Bildanforderung eines Besuchers: Eine Umleitung tritt auf, wenn ein Benutzer Ihre Site zum ersten Mal besucht. Diese Umleitung dient zum Abrufen eines Besucher-Cookies. Die Datenerfassung wird dadurch nicht beeinflusst.
   * Integration zwischen Comscore und Adobe: Wenn Ihr Unternehmen eine Comscore-/Analytics-Integration verwendet, ergibt jede Bildanforderung immer eine 302-Antwort.
* **404 NICHT GEFUNDEN**: Diese Antwort bedeutet, dass die Bildanforderung nicht gefunden wurde und keine Daten an die Datenerfassungsserver der Adobe gesendet werden. Diese Antwort ist auch möglich, wenn fest programmierte Bildanforderungen nicht korrekt formatiert sind. Wenden Sie sich an die Einzelperson oder das Team, die/das Analytics implementiert hat, um dieses Problem zu beheben.

## NS_BINDING_ABORTED in Antwortcodes

Diese Meldung tritt auf, weil die Bildanforderung zur Linktracking so konzipiert ist, dass der Browser zur nächsten Seite wechseln kann, bevor er auf eine Antwort von den Datenerfassungsservern der Adobe wartet.

Die Antwort von Adobe ist einfach nur ein leeres transparentes 1x1-Pixel-Bild, das für den Seiteninhalt irrelevant ist. If you see a line item in your packet monitor from Adobe, either with a **[!UICONTROL 200 OK]** response or an **[!UICONTROL NS_BINDING_ABORTED]** response, the data has reached Adobe&#39;s servers. Dann besteht kein Grund mehr, die Seite noch länger warten zu lassen.

Für Paketmonitore, die als Plug-in integriert sind, ist selten die vollständige Antwort sichtbar. Monitore neigen dazu, die Anforderung als abgebrochen zu betrachten, da die vollständige Antwort nicht erhalten wurde. Diese Monitore machen außerdem sehr selten die Unterscheidung, ob die Anforderung oder die Antwort abgebrochen wurde. Eigenständige Paketmonitore verfügen dagegen meist über detailliertere Informationen und melden daher den Status exakter. Beispiel: Ein Benutzer erhält in *Charles* eine Meldung, die besagt, dass der Client die Verbindung abgebrochen hat, bevor eine vollständige Antwort erhalten wurde. Das bedeutet, die Daten haben unsere Server erreicht, aber der Browser ist bereits auf der nächsten Seite, bevor das 1x1-Pixel erhalten wurde.

Wenn ein externer Paketmonitor meldet, dass die Datenerfassungsanforderung abgebrochen wurde, anstatt die Antwort, gibt dies Anlass zur Besorgnis. Adobe [!DNL Customer Care] kann Ihnen hier bei der Fehlerbehebung helfen.
