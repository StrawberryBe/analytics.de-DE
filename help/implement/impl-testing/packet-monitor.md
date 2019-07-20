---
description: Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an Datenerfassungsserver von Adobe gesendet werden.
keywords: Analytics-Implementierung
seo-description: Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an Datenerfassungsserver von Adobe gesendet werden.
seo-title: Paket-Analyzers
solution: Analytics
subtopic: Debugger
title: Paket-Analyzers
topic: Entwickler und Implementierung
uuid: 3597 c 23 a -1 c 72-46 e 6-909 d-f 661 cvc 490
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Paket-Analyzers

Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an Datenerfassungsserver von Adobe gesendet werden.

Ähnlich dem [!DNL DigitalPulse Debugger] zeigen Paketmonitore an, welche Datenparameter bei einer Bildanforderung übertragen werden. Paketmonitore bieten jedoch zusätzliche Funktionen:

* Anzeige von Bildanforderungen aus benutzerspezifischen Linktracking
* Anzeige von Bildanforderungen mit anderen Implementierungsmethoden als JavaScript (wie z. B. fest programmierte Bildanforderungen oder [!DNL Appmeasurement])

Zur Anzeige von Analytics-Anforderungen müssen Sie ausgehende Anforderungen mit „b/ss“ filtern.

In sehr seltenen Fällen meldet der Debugger eine Bildanforderung, obwohl keine solche Anforderung bei den [!DNL Analytics]-Verarbeitungsserver von Adobe einging. Mit einem Paketmonitor können Sie sich hundertprozentig sicher sein, dass eine bestimmte Bildanforderung erfolgreich veranlasst wird.

Adobe stellt zwar keinen offiziellen Paketmonitor bereit, jedoch finden Sie eine große Auswahl im Internet. Nachfolgend sind einige brauchbare Paketmonitore aufgeführt.

>[!NOTE]
>
>Diese Listen sollen nicht umfassend sein, sondern Informationen zu häufig verwendeten Monitoren. Wenn Sie einen Paketmonitor haben, der sich als nützlich erwiesen hat, können Sie über die Schaltfläche [!UICONTROL Feedback] rechts in diesem Fenster ein Feedback dazu abgeben.

| Firefox | Internet Explorer | Chrome | Eigenständige Programme |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tamper Data](https://addons.mozilla.org/en-us/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe bietet KEINE Unterstützung oder Fehlerbehebung bei Problemen, die mit diesen Paketmonitoren auftreten können. Wenden Sie sich bei Fragen und Problemen an die Website, von der Sie den Paketmonitor heruntergeladen haben.

<!-- 

debugger_ns_binding.xml

 -->

Der Grund für diesen Fehler liegt darin, dass die zur Linktracking dienende Bildanforderung es dem Browser erlauben soll, zur nächsten Seite zu wechseln, ohne auf eine Antwort von den Datenerfassungsservern von Adobe warten zu müssen.

Die Antwort von Adobe ist einfach nur ein leeres transparentes 1x1-Pixel-Bild, das für den Seiteninhalt irrelevant ist. Wenn Ihnen in Ihrem Paketmonitor eine Meldung von Adobe in der Form **[!UICONTROL 200 OK]** oder **NS_BINDING_ABORTED]angezeigt wird, bedeutet dies, dass die Daten bei unserem Server angekommen sind.[!UICONTROL ** Dann besteht kein Grund mehr, die Seite noch länger warten zu lassen.

Für Paketmonitore, die als Plug-in integriert sind, ist selten die vollständige Antwort sichtbar. Monitore neigen dazu, die Anforderung als abgebrochen zu betrachten, da die vollständige Antwort nicht erhalten wurde. Diese Monitore machen außerdem sehr selten die Unterscheidung, ob die Anforderung oder die Antwort abgebrochen wurde. Eigenständige Paketmonitore verfügen dagegen meist über detailliertere Informationen und melden daher den Status exakter. Beispiel: Ein Benutzer erhält in *Charles* eine Meldung, die besagt, dass der Client die Verbindung abgebrochen hat, bevor eine vollständige Antwort erhalten wurde. Das bedeutet, die Daten haben unsere Server erreicht, aber der Browser ist bereits auf der nächsten Seite, bevor das 1x1-Pixel erhalten wurde.

Wenn ein externer Paket-Sniffer meldet, dass die Datenerfassungsanforderung abgebrochen wurde (anstatt der Antwort), stellt dies ein Problem dar. Adobe [!DNL Customer Care] kann Ihnen hier bei der Fehlerbehebung helfen.
