---
title: Paket-Analyzer
description: Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Paket-Analyzer

Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.

Ähnlich dem Adobe Experience Cloud-Debugger zeigen Paketmonitore an, welche Datenparameter bei einer Bildanforderung übertragen werden. Paketmonitore bieten jedoch zusätzliche Funktionen:

* Anzeige von Bildanforderungen aus benutzerspezifischen Linktracking
* Anzeige von Bildanforderungen mit anderen Implementierungsmethoden als JavaScript (wie z. B. fest programmierte Bildanforderungen oder [!DNL Appmeasurement])

Zur Anzeige von Analytics-Anforderungen müssen Sie ausgehende Anforderungen mit „b/ss“ filtern.

In sehr seltenen Fällen meldet der Debugger eine Bildanforderung, obwohl keine solche Anforderung bei den [!DNL Analytics]-Verarbeitungsserver von Adobe einging. Mit einem Paketmonitor können Sie sich hundertprozentig sicher sein, dass eine bestimmte Bildanforderung erfolgreich ausgelöst wird.

Adobe stellt zwar keinen offiziellen Paketmonitor zur Verfügung, es gibt jedoch eine breite Palette von Paketen im Internet. Im Folgenden sind einige Paketmonitore aufgeführt, die andere für nützlich gehalten haben.

>[!NOTE] Die Liste ist nicht vollständig, sondern dient zur Angabe häufig eingesetzter Monitore. Wenn Sie einen Paketmonitor haben, den Sie erfolgreich verwenden und nützlich finden, können Sie mit der [!UICONTROL Feedback] Schaltfläche rechts in diesem Fenster Feedback geben.

| Firefox | Internet Explorer | Chrome | Eigenständige Programme |
|---|---|---|---|
| [Beobachtungspunkt](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [HttpWatch](https://www.httpwatch.com/) | [Beobachtungspunkt](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Manipulationsdaten](https://addons.mozilla.org/en-us/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE] Adobe bietet WEDER Support NOCH Fehlerbehebung bei Problemen mit diesen Paketmonitoren an. Wenden Sie sich bei Fragen und Problemen an die Website, von der Sie den Paketmonitor heruntergeladen haben.

## NS_BINDING_ABORTED in Antwortcodes

Dieser Fehler tritt auf, weil die Bildanforderung zur Linktracking so konzipiert ist, dass der Browser zur nächsten Seite wechseln kann, bevor er auf eine Antwort von den Adobe-Datenerfassungsservern wartet.

Die Antwort von Adobe ist einfach nur ein leeres transparentes 1x1-Pixel-Bild, das für den Seiteninhalt irrelevant ist. Wenn Ihnen in Ihrem Paketmonitor eine Meldung von Adobe in der Form **[!UICONTROL 200 OK]** oder **[!UICONTROL NS_BINDING_ABORTED]** angezeigt wird, bedeutet dies, dass die Daten bei unserem Server angekommen sind. Die Seite muss nicht länger gewartet werden.

Paketmonitore, die als Plug-In integriert sind, sehen selten die vollständige Antwort. Sie neigen dazu, die Anfrage als abgebrochen zu betrachten, da die vollständige Antwort nicht eingegangen ist. Bei diesen Monitoren wird auch selten unterschieden, ob die Anforderung oder Antwort abgebrochen wurde. Ein eigenständiger Paketmonitor hat in der Regel detailliertere Meldungen und meldet den Status genauer. Beispielsweise könnte ein Benutzer eine Meldung in *Charles* erhalten, die besagt, dass der Client die Verbindung geschlossen hat, bevor er die gesamte Antwort erhält. Das bedeutet, dass die Daten unsere Server erreicht haben, nur der Browser ging zur nächsten Seite, bevor das 1x1 Pixel empfangen wurde.

Wenn ein externer Paket-Sniffer der Berichte ist, dass die Datenerfassungsanforderung abgebrochen wird, anstatt der Antwort, gibt dies Anlass zur Besorgnis. Adobe [!DNL Customer Care] kann Ihnen hier bei der Fehlerbehebung helfen.
