---
title: Client-Hinweise
description: Erfahren Sie, wie Client-Hinweise schrittweise den Benutzeragenten als Quelle von Geräteinformationen ersetzen werden.
source-git-commit: 55747b79851696fd1bff8fb7cb4849dc8c813fc0
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 77%

---


# Überblick über Client-Hinweise und häufig gestellte Fragen

Client-Hinweise sind spezifische Informationen zum Gerät eines Benutzers. Sie werden von Chromium-Browsern wie Google Chrome und Microsoft Edge bereitgestellt. Bei diesen Browsern wird der Benutzeragent schrittweise durch Client-Hinweise als Quelle von Geräteinformationen ersetzt. Adobe Analytics wird seinen Gerätesuchprozess aktualisieren, sodass zusätzlich zum Benutzeragenten Client-Hinweise zum Ermitteln von Geräteinformationen verwendet werden.

Google unterteilt Client-Hinweise von Benutzeragenten in zwei Kategorien: Hinweise mit niedriger oder hoher Entropie.

* **Hinweise mit niedriger Entropie** enthalten allgemeine Informationen über Geräte. Diese Hinweise werden automatisch von Chromium-Browsern bereitgestellt.

* **Hinweise mit hoher Entropie** enthalten detailliertere Informationen. Diese Hinweise sind nur auf Anfrage verfügbar. Sowohl AppMeasurement als auch Web SDK [können konfiguriert werden](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md), um Hinweise mit hoher Entropie anzufordern. Standardmäßig fordern beide Bibliotheken **keine** Hinweise mit hoher Entropie an.

>[!NOTE]
>
>Ab Oktober 2022 werden neue Versionen von Chromium-Browsern die in der Benutzeragenten-Zeichenfolge dargestellte Betriebssystemversion „einfrieren“. Die Version des Betriebssystems ist ein Hinweis mit hoher Entropie. Um die Genauigkeit der Betriebssystemversion in Ihren Berichten zu gewährleisten, muss die Bibliothek Ihrer Sammlungen so konfiguriert werden, dass diese Hinweise mit hoher Entropie erfasst werden. Im Laufe der Zeit werden andere Geräteinformationen des Benutzeragenten eingefroren, sodass Client-Hinweise die Genauigkeit der Geräteberichte gewährleisten müssen.

>[!NOTE]
>
>AAM erfordert die Erfassung hoher Entropiehinweise, um die volle Funktionalität zu erhalten. Wenn Sie [serverseitige Weiterleitung an AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de) können Sie die Sammlung von hochgradigen Entropiehinweisen aktivieren.

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

+++**Was sind die verschiedenen Werte für Client-Hinweise?**

In der folgenden Tabelle werden die Client-Hinweise ab Oktober 2022 beschrieben.

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

+++**Gibt es Änderungen am Geräte-Reporting in Analytics?**

Die für das Reporting verfügbaren Gerätefelder ändern sich nicht. Die in diesen Feldern erfassten Daten können sich je nach Feld und Konfiguration der Sammlung von Client-Hinweisen ändern.

+++

+++**Welche Analytics-Reporting-Felder werden vom Benutzeragenten befüllt?**

Diese Felder werden direkt vom User-Agent abgeleitet, aber User-Agent kann verwendet werden, um Werte für andere gerätebezogene Felder abzuleiten, abhängig von den Gerätedetails.

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=de)
* [Browser-Typ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=de)
* [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=de)
* [Betriebssystemtypen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=de)
* [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=de)

+++

+++**Welche Analytics-Reporting-Felder werden mit Werten befüllt, die in Hinweisen mit hoher Entropie gespeichert sind?**

Dies ändert sich mit der Zeit, da Google mehr Teile des Benutzeragenten &quot;einfriert&quot;. Das erste Feld, das direkt betroffen ist, ist &quot;Betriebssystem&quot;, das die Betriebssystemversion enthält. Gemäß der von Google veröffentlichten Zeitleiste für &quot;Einfrieren&quot;von Benutzeragenten-Hinweisen wird die Betriebssystemversion ab Ende Oktober 2022 mit Chromium-Version 107 eingefroren. Zu diesem Zeitpunkt ist die Betriebssystemversion im User Agent in einigen Fällen ungenau.

Die Zeiten für das Einfrieren anderer Teile des Benutzeragenten können Sie dem [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html), entnehmen.

+++

+++**Wie verwendet Adobe Client-Hinweise zum Erfassen von Geräteinformationen?**

Adobe verwendet einen Drittanbieter, Device Atlas, der sowohl Client-Hinweise als auch den Benutzeragenten verwendet, um Geräteinformationen zu erfassen.

+++

+++**Welche Browser sind von Client-Hinweisen betroffen?**

Client-Hinweise gelten nur für Chrome-Browser wie Google Chrome und Microsoft Edge. Daten von anderen Browsern oder Mobile Apps werden nicht geändert.

+++

+++**Werden Client-Hinweise über unsichere Verbindungen unterstützt?**

Nein. Client-Hinweise können nur über eine sichere HTTP-Verbindung wie HTTPS erfasst werden.

+++

+++**Sind Client-Hinweise in Daten verfügbar, die über den Adobe Source Connector an AEP und CJA gesendet werden?**

Adobe plant, im ersten Halbjahr 2023 Client-Hinweise in Daten über den Adobe Source Connector zu erfassen.

+++

+++**Wie werden Client-Hinweise in XDM dargestellt?**

Siehe [Schemadokumentation](https://github.com/adobe/xdm/blob/master/components/datatypes/sessiondetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Welche Teile des Benutzeragenten werden „eingefroren“ und wann?**

Siehe den [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dieser kann sich aber noch ändern.

+++

+++**Unterstützt AAM serverseitige Weiterleitung Client-Hinweise?**

Ja. Client-Hinweise werden in die Daten aufgenommen, die an AAM weitergeleitet werden. Beachten Sie, dass AAM gesammelt werden müssen, um die volle Funktionalität zu erhalten. Wenn Sie [serverseitige Weiterleitung an AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) dann können Sie die Sammlung von hochentropischen Hinweisen aktivieren.

+++

