---
title: Client-Hinweise
description: Erfahren Sie, wie Client-Hinweise schrittweise den User-Agent als Quelle der Geräteinformationen ersetzen.
source-git-commit: 72ef2d5e34220f1703714fac40a9dae4e76c1ab1
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 5%

---


# Überblick über Kundenhinweise und häufig gestellte Fragen

Client-Hinweise sind einzelne Informationen zum Gerät eines Benutzers. Sie werden von Chromium-Browsern wie Google Chrome und Microsoft Edge bereitgestellt. Bei diesen Browsern ersetzen Client-Hinweise schrittweise den Benutzeragenten als Quelle der Geräteinformationen. Adobe Analytics aktualisiert seinen Gerätesuchprozess, sodass zusätzlich zu User-Agent Client-Hinweise zum Ermitteln von Geräteinformationen verwendet werden.

Google unterteilt Benutzeragenten-Client-Hinweise in zwei Kategorien: Tiefentropie und hochentropische Hinweise.

* **Hinweise zur niedrigen Entropie** enthalten generischere Informationen über Geräte. Diese Hinweise werden automatisch von Chromium-Browsern bereitgestellt.

* **Hochentropie** Hinweise enthalten detailliertere Informationen. Diese Hinweise sind nur auf Anfrage verfügbar. Sowohl AppMeasurement als auch Web SDK [kann konfiguriert werden](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md) , um Hinweise mit hoher Entropie anzufordern. Standardmäßig tun beide Bibliotheken dies **not** fordern Sie Hinweise mit hoher Entropie an.

>[!NOTE]
>
>Ab Oktober 2022 werden neue Versionen von Chromium-Browsern die in der Benutzeragenten-Zeichenfolge dargestellte Betriebssystemversion &quot;einfrieren&quot;. Wenn Benutzer ihre Geräte aktualisieren, ändert sich das Betriebssystem im User-Agent nicht. So werden im Laufe der Zeit die im User-Agent dargestellten Versionsinformationen weniger genau. Betriebssystemversion ist ein Hinweis mit hoher Entropie. Um die Genauigkeit der Betriebssystemversion in Ihren Berichten zu gewährleisten, muss Ihre Sammlungsbibliothek so konfiguriert werden, dass diese Hinweise mit hoher Entropie erfasst werden. Im Laufe der Zeit werden andere Geräteinformationen des Benutzeragenten eingefroren, sodass Client-Hinweise die Genauigkeit der Geräteberichte gewährleisten müssen.

## Häufig gestellte Fragen

+++**Wo erhalte ich weitere Informationen über Kundenhinweise?**

Diese [Google-Blogpost](https://web.dev/user-agent-client-hints/) ist eine gute Referenz und Ausgangspunkt.

+++

+++**Wie kann ich die Sammlung von Client-Hinweisen aktivieren?**

Hinweise mit geringer Entropie werden automatisch vom Browser bereitgestellt und in den Prozess der Adobe zum Ableiten von Geräte- und Browserinformationen aufgenommen. Neuere Versionen von AppMeasurement (ab 2.23.0) und Web SDK (ab 2.12.0) können so konfiguriert werden, dass sie Hinweise mit hoher Entropie erfassen. Für beide Bibliotheken lautet die Sammlung von Hinweisen zur Entropie mit hoher Entropie **Standardmäßig deaktiviert**.

+++

+++**Wie kann ich Hinweise zur Entropie erfassen?**

High-Entropy-Hinweise können mit den Web SDK- und AppMeasurement-Bibliotheken über ihre jeweiligen Tags-Erweiterungen oder direkt mit dem Flag collectHighEntropyUserAgentHints konfiguriert werden.

+++

+++**Kann ich auswählen, welche hochentropischen Hinweise ich sammele?**

Zum jetzigen Zeitpunkt nicht. Sie können alle hochentropischen Hinweise oder keine sammeln.

+++

+++**Gibt es Änderungen an der Geräteberichterstellung in Analytics?**

Die für die Berichterstellung verfügbaren Gerätefelder ändern sich nicht. Die für diese Felder erfassten Daten können sich je nach Feld und Konfiguration der Kollektion für Client-Hinweise ändern.

+++

+++**Welche Analytics-Berichtsfelder werden vom User-Agent abgeleitet?**

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [Browser-Typ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [Betriebssystemtypen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)
* [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=de)

+++

+++**Welche Analytics-Berichtsfelder werden von Werten abgeleitet, die in hochentropy-Hinweisen gespeichert sind?**

Ab September 2022 wird die von Google veröffentlichte Timeline für &quot;Einfrieren&quot;von Benutzeragenten-Hinweisen darauf hinweisen, dass die Betriebssystemversion ab Oktober 2022 nicht mehr aktualisiert wird. Wenn Benutzer ihr Betriebssystem aktualisieren, wird die Betriebssystemversion im User-Agent nicht aktualisiert. Ohne hohe Entropie wird die Genauigkeit der Betriebssystemversion, die in der Analytics-Dimension &quot;Betriebssystem&quot;enthalten ist, allmählich abnehmen.

Siehe Abschnitt [Zeitleiste veröffentlicht von Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) um den Zeitpunkt für das Einfrieren anderer Teile des Benutzeragenten anzuzeigen.

+++

+++**Wie verwendet Adobe Client-Hinweise zum Ableiten von Geräteinformationen?**

Adobe verwendet einen Drittanbieter, Device Atlas, der sowohl die Client-Hinweise als auch den User-Agent verwendet, um Geräteinformationen abzuleiten.

+++

+++**Welche Browser sind von Client-Hinweisen betroffen?**

Client-Hinweise gelten nur für Chrome-Browser wie Google Chrome und Microsoft Edge. Daten von anderen Browsern oder Apps werden nicht geändert.

+++

+++**Sind Client-Hinweise in Daten verfügbar, die über den Adobe Source Connector an AEP und CJA gesendet werden?**

Wir planen, im ersten Halbjahr 2023 über Adobe Source Connector Kundenhinweise in Daten aufzunehmen.

+++

+++**Wie werden Kundenhinweise in XDM dargestellt?**

Siehe [Schemadokumentation](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Was sind die verschiedenen Eingabefelder? Welche betreffen die Geräteberichte?**

In der folgenden Tabelle werden die Kundenhinweise ab September 2022 beschrieben.

| Hinweis | Beschreibung | Hohe oder niedrige Entropie | Beispiel |
| --- | --- | --- | --- | 
| Sec-CH-UA | Browser und wichtige Version | Niedrig | &quot;Google Chrome 84&quot; |
| Sec-CH-UA-Mobile | Mobilgerät (true oder false) | Niedrig | TRUE |
| Sec-CH-UA-Platform | Betriebssystem/Plattform | Niedrig | &quot;Android&quot; |
| Sec-CH-UA-Arch | Architektur der Site | Hoch | &quot;arm&quot; |
| SEC-CH-UA-Bitness | Architekturstile | Hoch | &quot;64&quot; |
| sec-CH-UA-full-version | Vollständige Version des Browsers | Hoch | &quot;84.0.4143.2&quot; |
| sec-CH-UA-full-version-list | Liste der Marken mit ihrer Version | Hoch | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-Modell | Gerätemodell | Hoch | &quot;Pixel 3&quot; |
| Sec-CH-UA-Platform-Version | Betriebssystem/Plattform-Version | Hoch | &quot;10&quot; |

+++



+++**Welche Teile des Benutzeragenten werden &quot;eingefroren&quot;und wann?**

Siehe [Zeitleiste veröffentlicht von Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dies kann sich ändern.

+++
