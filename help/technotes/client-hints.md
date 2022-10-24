---
title: Client-Hinweise
description: Erfahren Sie, wie Client-Hinweise schrittweise den Benutzeragenten als Quelle von Geräteinformationen ersetzen werden.
source-git-commit: 9dfeb0f5cc3bb488fa28fb0d21c6969dfdfc9ef6
workflow-type: ht
source-wordcount: '1073'
ht-degree: 100%

---


# Überblick über Client-Hinweise und häufig gestellte Fragen

Client-Hinweise sind spezifische Informationen zum Gerät eines Benutzers. Sie werden von Chromium-Browsern wie Google Chrome und Microsoft Edge bereitgestellt. Bei diesen Browsern wird der Benutzeragent schrittweise durch Client-Hinweise als Quelle von Geräteinformationen ersetzt. Adobe Analytics wird seinen Gerätesuchprozess aktualisieren, sodass zusätzlich zum Benutzeragenten Client-Hinweise zum Ermitteln von Geräteinformationen verwendet werden.

Google unterteilt Client-Hinweise von Benutzeragenten in zwei Kategorien: Hinweise mit niedriger oder hoher Entropie.

* **Hinweise mit niedriger Entropie** enthalten allgemeine Informationen über Geräte. Diese Hinweise werden automatisch von Chromium-Browsern bereitgestellt.

* **Hinweise mit hoher Entropie** enthalten detailliertere Informationen. Diese Hinweise sind nur auf Anfrage verfügbar. Sowohl AppMeasurement als auch Web SDK können konfiguriert werden, um Hinweise mit hoher Entropie anzufordern. Standardmäßig fordern beide Bibliotheken **keine** Hinweise mit hoher Entropie an.

>[!NOTE]
>
>Die Client-Hinweise werden ab Mitte Januar 2023 in den Prozess der Analytics-Gerätesuche integriert. Sowohl AppMeasurement als auch Web SDK unterstützen derzeit die Erfassung von Hinweisdaten, diese werden jedoch bis Mitte Januar nicht für die Gerätesuche verwendet. Damit soll eine mögliche Unterbrechung des Reportings während der kritischen Zeit zum Jahresende vermieden werden. Wie unten erwähnt, wird die Betriebssystemversion ab Oktober eingefroren, aber aufgrund eines schrittweisen Rollouts und der Tatsache, dass die meisten Benutzeragenten auf die korrekte Betriebssystemversion eingefroren werden, schätzen wir, dass dies weniger als 3 % der Besuchenden mit Chrome betreffen wird.

>[!NOTE]
>
>Ab Oktober 2022 werden neue Versionen von Chromium-Browsern die in der Benutzeragenten-Zeichenfolge dargestellte Betriebssystemversion „einfrieren“. Die Version des Betriebssystems ist ein Hinweis mit hoher Entropie. Um die Genauigkeit der Betriebssystemversion in Ihren Berichten zu gewährleisten, muss die Bibliothek Ihrer Sammlungen so konfiguriert werden, dass diese Hinweise mit hoher Entropie erfasst werden. Im Laufe der Zeit werden andere Geräteinformationen des Benutzeragenten eingefroren, sodass Client-Hinweise die Genauigkeit der Geräteberichte gewährleisten müssen.

>[!NOTE]
>
>AAM erfordert das Erfassen von Hinweisen mit hoher Entropie, um die vollständige Funktionalität zu erhalten. Wenn Sie [Server-seitige Weiterleitung an AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de) verwenden, sollten Sie die Erfassung von Hinweisen mit hoher Entropie aktivieren.

## Häufig gestellte Fragen

+++**Wo erhalte ich weitere Informationen über Client-Hinweise?**

Dieser [Blogpost von Google](https://web.dev/user-agent-client-hints/) ist eine gute Referenz und ein geeigneter Ausgangspunkt.

+++

+++**Wie kann ich die Sammlung von Client-Hinweisen aktivieren?**

Hinweise mit niedriger Entropie werden automatisch vom Browser bereitgestellt und zur Ermittlung von Geräte- und Browserinformationen aufgenommen. Neuere Versionen des Web SDK (beginnend mit 2.12.0) und AppMeasurement (beginnend mit 2.23.0) können über ihre jeweiligen Tags-Erweiterungen oder direkt über eine Konfigurationsoption so konfiguriert werden, dass sie Hinweise mit hoher Entropie erfassen. Siehe Anleitungen für [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html?lang=de#enabling-high-entropy-client-hints) und [AppMeasurement](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/collecthighentropyuseragenthints.html?lang=de).

Für beide Bibliotheken ist die Sammlung von Hinweisen mit hoher Entropie **standardmäßig deaktiviert**.

+++

+++**Kann ich auswählen, welche Hinweise mit hoher Entropie ich erfasse?**

Zum jetzigen Zeitpunkt nicht. Sie können entweder alle Hinweise mit hoher Entropie oder keine erfassen.

+++

+++**Wie lauten die verschiedenen Werte für Client-Hinweise?**

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

Diese Felder werden direkt vom Benutzeragenten abgeleitet, aber der Benutzeragent kann abhängig von den Gerätedetails zur Ableitung von Werten für andere gerätebezogene Felder verwendet werden.

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=de)
* [Browser-Typ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=de)
* [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=de)
* [Betriebssystemtypen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=de)
* [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=de)

+++

+++**Welche Teile des Benutzeragenten werden „eingefroren“ und wann?**

Siehe den [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dieser kann sich aber noch ändern.

+++

+++**Welche Analytics-Reporting-Felder werden mit Werten befüllt, die in Hinweisen mit hoher Entropie gespeichert sind?**

Dies ändert sich im Laufe der Zeit, da Google weitere Teile des Benutzeragenten „einfriert“. Das erste unmittelbar betroffene Feld ist „Betriebssystem“, das die Betriebssystemversion beinhaltet. Nach dem von Google veröffentlichten Zeitplan für das „Einfrieren“ von Benutzeragenten-Hinweisen wird die Betriebssystemversion ab Ende Oktober 2022 beginnend mit Chromium Version 107 eingefroren. Zu diesem Zeitpunkt ist die Betriebssystemversion im Benutzeragenten in einigen Fällen ungenau.

Die Zeiten für das Einfrieren anderer Teile des Benutzeragenten können Sie dem [von Google veröffentlichten Zeitplan](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html), entnehmen.

+++

+++**Wie verwendet Adobe Client-Hinweise zum Erfassen von Geräteinformationen?**

Adobe verwendet Device Atlas, einen Drittanbieter, der sowohl die Client-Hinweise als auch den Benutzeragenten zur Ermittlung von Geräteinformationen verwendet.

+++

+++**Welche Browser sind von Client-Hinweisen betroffen?**

Die Client-Hinweise gelten nur für Chromium-Browser wie Google Chrome und Microsoft Edge. Daten von anderen Browsern oder Mobile Apps werden nicht geändert.

+++

+++**Werden Client-Hinweise über unsichere Verbindungen unterstützt?**

Nein. Client-Hinweise können nur über eine sichere HTTP-Verbindung wie HTTPS erfasst werden.

+++

+++**Wie binde ich bei der Verwendung der API-Übermittlung Client-Hinweisdaten ein?**

Siehe Dokumentation zur Einbindung dieser Daten über die [Bulk-Dateneinfüge-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/file-format/).

+++

+++**Sind Client-Hinweise in Daten verfügbar, die über den Adobe Source Connector an AEP und CJA gesendet werden?**

Adobe plant, im ersten Halbjahr 2023 Client-Hinweise in Daten über den Adobe Source Connector zu erfassen.

+++

+++**Wie werden Client-Hinweise in XDM dargestellt?**

Siehe [Schemadokumentation](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Unterstützt die Server-seitige Weiterleitung an AAM Client-Hinweise?**

Ja. Client-Hinweise werden in den an AAM weitergeleiteten Daten enthalten sein. Beachten Sie, dass AAM die Sammlung von Hinweisen mit hoher Entropie erfordert, um die volle Funktionalität zu beizubehalten. Wenn Sie die [Server-seitige Weiterleitung an AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de) verwenden, sollten Sie die Sammlung von Hinweisen mit hoher Entropie aktivieren.

+++

