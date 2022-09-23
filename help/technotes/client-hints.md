---
title: Client-Hinweise
description: Erfahren Sie, wie Client-Hinweise schrittweise den Benutzeragenten als Quelle der Geräteinformationen ersetzen.
source-git-commit: 788ab49fec9117e0ef2a736f609a627b913b9f8c
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 4%

---


# Überblick über Kundenhinweise und häufig gestellte Fragen

Client-Hinweise sind einzelne Informationen zum Gerät eines Benutzers. Sie werden von Chromium-Browsern wie Google Chrome und Microsoft Edge bereitgestellt. Bei diesen Browsern ersetzen Client-Hinweise schrittweise den Benutzeragenten als Quelle der Geräteinformationen. Adobe Analytics aktualisiert seinen Gerätesuchprozess, sodass zusätzlich zum Benutzeragenten Client-Hinweise zum Ermitteln von Geräteinformationen verwendet werden.

Google unterteilt Benutzeragenten-Clienthinweise in zwei Kategorien: Tiefentropie und hochentropische Hinweise.

* Tipps zur geringen Entropie enthalten generischere Informationen über Geräte. Diese Hinweise werden automatisch von Chromium-Browsern bereitgestellt.

* High-Entropy-Hinweise enthalten detailliertere Informationen. Diese Hinweise sind nur auf Anfrage verfügbar. Sowohl AppMeasurement als auch Web SDK können so konfiguriert werden, dass Hinweise mit hoher Entropie angefordert werden. Standardmäßig tun beide Bibliotheken dies **not** fordern Sie Hinweise mit hoher Entropie an.

>[!NOTE]
>
>Ab Oktober 2022 werden neue Versionen von Chromium-Browsern die in der Benutzeragenten-Zeichenfolge dargestellte Betriebssystemversion &quot;einfrieren&quot;. Das bedeutet, dass die im Benutzeragenten dargestellten Informationen zur Betriebssystemversion im Laufe der Zeit weniger genau werden. Betriebssystemversion ist ein Hinweis mit hoher Entropie. Um die Genauigkeit der Betriebssystemversion in Ihren Berichten zu gewährleisten, muss Ihre Sammlungsbibliothek so konfiguriert werden, dass diese Hinweise mit hoher Entropie erfasst werden. Im Laufe der Zeit werden andere Geräteinformationen des Benutzeragenten eingefroren, sodass Client-Hinweise die Genauigkeit der Geräteberichte wahren müssen.

## Häufig gestellte Fragen

+++**Wie kann ich die Sammlung von Client-Hinweisen aktivieren?**

Hinweise zur geringen Entropie werden automatisch vom Browser bereitgestellt und in den Geräteprozess der Adobe aufgenommen. Neuere Versionen von AppMeasurement (Start-TBD) und Web SDK (Start-TBD) können so konfiguriert werden, dass sie Hinweise mit hoher Entropie erfassen. Für beide Bibliotheken lautet die Sammlung von Hinweisen zur Entropie mit hoher Entropie **Standardmäßig deaktiviert**. Weitere Informationen zur Implementierung finden Sie hier .

+++

+++**Kann ich auswählen, welche hochentropischen Hinweise ich sammele?**

Zum jetzigen Zeitpunkt nicht. Sie können alle hochentropischen Hinweise oder keine sammeln.

+++

+++**Gibt es Änderungen an der Geräteberichterstellung in Analytics?**

Die für die Berichterstellung verfügbaren Gerätefelder ändern sich nicht. Die für dieses Feld erfassten Daten können sich je nach Feld und Konfiguration der Kollektion für Client-Hinweise ändern.

+++

+++**Welche Analytics-Berichtsfelder werden vom Benutzeragenten abgeleitet?**

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [Browser-Typ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [Betriebssystemtypen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)??
* Daten-Feeds (Beachten Sie, dass Benutzer aktualisieren müssen, um diese Felder zu erfassen. Darüber hinaus gibt es eine Abhängigkeit, in der wir keine mobile ID zusammen mit Geräteinformationen verfügbar machen können.)
* Analytics Source Connector (noch nicht bereit)

+++

+++**Welche Analytics-Berichtsfelder werden von Werten abgeleitet, die in hochentropy-Hinweisen gespeichert sind?**

Ab September 2022 wird die von Google veröffentlichte Timeline zum Einfrieren von Benutzeragenten-Hinweisen darauf hinweisen, dass die Betriebssystemversion ab Oktober 2022 nicht mehr aktualisiert wird. Ohne hohe Entropie wird die Genauigkeit der Betriebssystemversion, die in der Analytics-Dimension &quot;Betriebssystem&quot;enthalten ist, allmählich abnehmen.

Siehe [Zeitleiste veröffentlicht von Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) um den Zeitpunkt für das Einfrieren des Benutzeragenten anzuzeigen.

+++

+++**Welche Browser sind von Client-Hinweisen betroffen?**

Client-Hinweise gelten nur für Chrome-Browser wie Google Chrome und Microsoft Edge. Daten von anderen Browsern oder Apps werden nicht geändert.

+++

+++**Wie verwendet Adobe Client-Hinweise zum Ableiten von Geräteinformationen?**

Adobe verwendet einen Drittanbieter, Device Atlas, der sowohl die Client-Hinweise als auch den Benutzeragenten verwendet, um Geräteinformationen abzuleiten.

+++

+++**Sind Kundenhinweise in Daten-Feeds verfügbar?**

Ja. Weitere Informationen finden Sie in der Dokumentation (zu folgen).

+++

+++**Sind Client-Hinweise in Daten verfügbar, die über den Adobe Source Connector an AEP und CJA gesendet werden?**

Wir planen, im ersten Halbjahr 2023 über Adobe Source Connector Kundenhinweise in Daten aufzunehmen.

+++

+++**Wie werden Kundenhinweise in XDM dargestellt?**

Siehe [Schemadokumentation](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Wo erhalte ich weitere Informationen über Kundenhinweise?**

Diese [Google-Blogpost](https://web.dev/user-agent-client-hints/) ist eine gute Referenz und Ausgangspunkt.

+++

+++**Was sind die verschiedenen Eingabefelder? Welche betreffen die Geräteberichte?**

In der folgenden Tabelle werden die Kundenhinweise ab September 2022 beschrieben.

| Hinweis (Kopfzeile) | Hinweis | Hohe oder niedrige Entropie | Beispiel | Analytics-Berichtsfelder |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | Browser und wichtige Version | Niedrig | Google Chrome 84 | [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en) und [Browsertyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en) |
| Sec-CH-UA-Mobile | Mobilgerät (true oder false) | Niedrig | TRUE | [Mobilgerät und Mobilgerätetyp](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)?? |
| Sec-CH-UA-Platform | Betriebssystem/Plattform | Niedrig | Android | [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |
| Sec-CH-UA-Arch | Architektur der Site | Hoch | &quot;arm&quot; | Keine? |
| SEC-CH-UA-Bitness | SEC-CH-UA-Bitness | Hoch |  | Keine? |
| sec-CH-UA-full-version | Vollständige Version des Browsers | Hoch | &quot;84.0.4143.2&quot; | Keine? |
| sec-CH-UA-full-version-list | ??? | Hoch | ??? | Keine? |
| Sec-CH-UA-Modell | Gerätemodell | Hoch | &quot;Pixel 3&quot; | Keine? |
| Sec-CH-UA-Platform-Version | Betriebssystem/Plattform-Version | Hoch | &quot;10&quot; | [Betriebssystem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |

+++

+++**Wie kann ich Hinweise zur Entropie erfassen?**

High-Entropy-Hinweise können konfiguriert werden

* Direkt für AppMeasurement [Link zur Kennzeichnung im Implementierungshandbuch]
* In der Tag Analytics-Erweiterung
* Im Web SDK.

+++

+++**Welche Daten werden aus dem Benutzeragenten entfernt und wann?**

Siehe [Zeitleiste veröffentlicht von Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dies kann sich ändern.

+++