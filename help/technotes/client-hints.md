---
title: Client-Hinweise
description: Erfahren Sie, wie Client-Hinweise schrittweise den Benutzeragenten als Quelle von Geräteinformationen ersetzen werden.
source-git-commit: f2f1e64a62796b58c24e6ff652db93b21f750669
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---


# Überblick über Client-Hinweise und häufig gestellte Fragen

Client-Hinweise sind spezifische Informationen zum Gerät eines Benutzers. Sie werden von Chromium-Browsern wie Google Chrome und Microsoft Edge bereitgestellt. Bei diesen Browsern wird der Benutzeragent schrittweise durch Client-Hinweise als Quelle von Geräteinformationen ersetzt. Adobe Analytics wird seinen Gerätesuchprozess aktualisieren, sodass zusätzlich zum Benutzeragenten Client-Hinweise zum Ermitteln von Geräteinformationen verwendet werden.

Google unterteilt Client-Hinweise von Benutzeragenten in zwei Kategorien: Hinweise mit niedriger oder hoher Entropie.

* **Hinweise mit niedriger Entropie** enthalten allgemeine Informationen über Geräte. Diese Hinweise werden automatisch von Chromium-Browsern bereitgestellt.

* **Hinweise mit hoher Entropie** enthalten detailliertere Informationen. Diese Hinweise sind nur auf Anfrage verfügbar. Sowohl AppMeasurement als auch Web SDK [können konfiguriert werden](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md), um Hinweise mit hoher Entropie anzufordern. Standardmäßig fordern beide Bibliotheken **keine** Hinweise mit hoher Entropie an.

>[!NOTE]
>
>Ab Oktober 2022 werden neue Versionen von Chromium-Browsern die in der Benutzeragenten-Zeichenfolge dargestellte Betriebssystemversion „einfrieren“. Wenn Benutzende ihre Geräte aktualisieren, ändert sich das Betriebssystem im Benutzeragenten nicht. Deshalb werden die im Benutzeragenten dargestellten Versionsinformationen im Laufe der Zeit weniger genau. Die Version des Betriebssystems ist ein Hinweis mit hoher Entropie. Um die Genauigkeit der Betriebssystemversion in Ihren Berichten zu gewährleisten, muss die Bibliothek Ihrer Sammlungen so konfiguriert werden, dass diese Hinweise mit hoher Entropie erfasst werden. Im Laufe der Zeit werden andere Geräteinformationen des Benutzeragenten eingefroren, sodass Client-Hinweise die Genauigkeit der Geräteberichte gewährleisten müssen.

## Häufig gestellte Fragen

+++**Wo erhalte ich weitere Informationen über Client-Hinweise?**

Dieser [Blogpost von Google](https://web.dev/user-agent-client-hints/) ist eine gute Referenz und ein geeigneter Ausgangspunkt.

+++

+++**Wie kann ich die Sammlung von Client-Hinweisen aktivieren?**

Hinweise mit niedriger Entropie werden automatisch vom Browser bereitgestellt und sind im Prozess von Adobe zum Erkennen von Geräte- und Browserinformationen enthalten. Neuere Versionen von AppMeasurement (ab 2.23.0) und Web SDK (ab 2.12.0) können so konfiguriert werden, dass sie Hinweise mit hoher Entropie erfassen. Für beide Bibliotheken ist die Sammlung von Hinweisen mit hoher Entropie **standardmäßig deaktiviert**.

+++

+++**Wie kann ich Hinweise hoher Entropie erfassen?**

Hinweise mit hoher Entropie können mit den Web-SDK- und AppMeasurement-Bibliotheken über ihre jeweiligen Tag-Erweiterungen oder direkt mit dem Flag „collectHighEntropyUserAgentHints“ konfiguriert werden.

+++

+++**Kann ich auswählen, welche Hinweise mit hoher Entropie ich erfasse?**

Zum jetzigen Zeitpunkt nicht. Sie können entweder alle Hinweise mit hoher Entropie oder keine erfassen.

+++

+++**Gibt es Änderungen am Geräte-Reporting in Analytics?**

Die für das Reporting verfügbaren Gerätefelder ändern sich nicht. Die in diesen Feldern erfassten Daten können sich je nach Feld und Konfiguration der Sammlung von Client-Hinweisen ändern.

+++

+++**Welche Analytics-Reporting-Felder werden vom Benutzeragenten befüllt?**

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=de)
* [Browser-Typ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=de)
* [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=de)
* [Betriebssystemtypen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=de)
* [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=de)
* [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=de)

+++

+++**Welche Analytics-Reporting-Felder werden mit Werten befüllt, die in Hinweisen mit hoher Entropie gespeichert sind?**

Der im September 2022 von Google veröffentlichte Zeitplan zum „Einfrieren“ von Benutzeragenten-Hinweisen weist darauf hin, dass die Betriebssystemversion ab Oktober 2022 nicht mehr aktualisiert wird. Wenn Benutzende ihr Betriebssystem aktualisieren, wird die Betriebssystemversion im Benutzeragenten nicht aktualisiert. Ohne Hinweise mit hoher Entropie wird die Genauigkeit der Betriebssystemversion, die in der Analytics-Dimension „Betriebssystem“ enthalten ist, allmählich abnehmen.

Die Zeiten für das Einfrieren anderer Teile des Benutzeragenten können Sie dem [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html), entnehmen.

+++

+++**Wie verwendet Adobe Client-Hinweise zum Erfassen von Geräteinformationen?**

Adobe verwendet einen Drittanbieter, Device Atlas, der sowohl Client-Hinweise als auch den Benutzeragenten verwendet, um Geräteinformationen zu erfassen.

+++

+++**Welche Browser sind von Client-Hinweisen betroffen?**

Client-Hinweise sind nur für Chromium-Browser wie Google Chrome und Microsoft Edge relevant. Daten von anderen Browsern oder Mobile Apps werden nicht geändert.

+++

+++** Werden Client-Hinweise über unsichere Verbindungen unterstützt?

Nein. Client-Hinweise können nur über eine sichere HTTP-Verbindung wie HTTPS erfasst werden.

+++

+++**Sind Client-Hinweise in Daten verfügbar, die über den Adobe Source Connector an AEP und CJA gesendet werden?**

Adobe plant, im ersten Halbjahr 2023 Client-Hinweise in Daten über den Adobe Source Connector zu erfassen.

+++

+++**Wie werden Client-Hinweise in XDM dargestellt?**

Siehe [Schemadokumentation](https://github.com/adobe/xdm/blob/master/components/datatypes/sessiondetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Was sind die verschiedenen Hinweisfelder? Welche sind für Geräteberichte relevant?**

In der folgenden Tabelle werden die Client-Hinweise ab September 2022 beschrieben.

| Hinweis | Beschreibung | Hohe oder niedrige Entropie | Beispiel |
| --- | --- | --- | --- | 
| Sec-CH-UA | Browser und Hauptversion | Niedrig | &quot;Google Chrome 84&quot; |
| Sec-CH-UA-Mobile | Mobilgerät (true oder false) | Niedrig | TRUE |
| Sec-CH-UA-Platform | Betriebssystem/Plattform | Niedrig | &quot;Android&quot; |
| Sec-CH-UA-Arch | Architektur der Site | Hoch | &quot;arm&quot; |
| Sec-CH-UA-Bitness | Architektur-Bitnes | Hoch | &quot;64&quot; |
| Sec-CH-UA-Full-Version | Vollständige Version des Browsers | Hoch | &quot;84.0.4143.2&quot; |
| Sec-CH-UA-Full-Version-List | Liste der Marken mit ihrer Version | Hoch | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-Model | Gerätemodell | Hoch | &quot;Pixel 3&quot; |
| Sec-CH-UA-Platform-Version | Betriebssystem/Platform-Version | Hoch | &quot;10&quot; |

+++



+++**Welche Teile des Benutzeragenten werden „eingefroren“ und wann?**

Siehe den [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dieser kann sich aber noch ändern.

+++
