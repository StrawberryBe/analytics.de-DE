---
description: Eine Folge von Seitenansichten während einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen.
keywords: Besuch
seo-description: Eine Folge von Seitenansichten während einer Sitzung. Die Besuchsmetrik wird normalerweise in Berichten verwendet, die die Anzahl der Benutzersitzungen im gewählten Zeitraum anzeigen.
seo-title: Besuch
solution: Analytics
title: Besuch
topic: Metriken
uuid: 91317487-f 116-4546-8 cd 2-421418 c 49 a 7 a
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Besuch

Eine Folge von Seitenansichten während einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen.

>[!NOTE]
>
>For information about how visits and mobile app launches are calculated, see [Compare Visits and Mobile App Launches](https://helpx.adobe.com/analytics/kb/compare-visits-and-mobile-app-launches.html) in the Knowledge Base.

Die Besuchsmetrik wird immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn ein Besucher zu Ihrer Site zurückkehrt. Eine Sitzung beginnt, wenn der Benutzer auf Ihre Site zugreift, und endet in einem der folgenden Fälle:

* **30 Minuten Inaktivität:** Fast alle Sitzungen enden auf diese Weise. Wenn mehr als 30 Minuten zwischen Bildanforderungen vergangen sind, beginnt ein neuer Besuch.
* **12 Stunden andauernder Aktivität:** Wenn ein Benutzer 12 Stunden hintereinander ohne eine mindestens 30 minütige Pause Bildanforderungen sendet, beginnt automatisch ein neuer Besuch.
* **2500 Hits:** Wenn ein Benutzer zahlreiche Hits generiert, ohne eine neue Sitzung zu starten, wird nach 2500 Bildanforderungen ein neuer Besuch gezählt.
* **100 Hits in 100 Sekunden**: Wenn ein Besuch aus mehr als 100 Hits besteht, die in weniger als 100 Sekunden stattfinden, endet der Besuch automatisch. Dieses Verhalten weist normalerweise auf Bot-Aktivität hin. Diese Einschränkung wird durchgesetzt, um zu verhindern, dass diese rechenintensiven Besuche die Latenz und die Zeit für die Generierung von Berichten erhöhen.

>[!NOTE]
>
>Die Definition eines Besuchs kann für eine Report Suite gekürzt werden, wenn sie spezifisch angefordert wird, kann jedoch nicht verlängert werden. Bitten Sie einen der unterstützten Benutzer Ihres Unternehmens, diese Änderung beim Kundendienst anzufordern.

Folgende Fälle starten keinen neuen Besuch:

* Der Benutzer schließt den Browser oder den Tab, öffnet ihn erneut und navigiert innerhalb von 30 Minuten zurück zu Ihrer Website. Der Benutzer kann auch seinen Browser schließen oder sogar den Computer neu starten und wird dennoch als Einzelbesuch gezählt (vorausgesetzt, er navigiert innerhalb des 30-Minuten-Zeitraums zurück zu Ihrer Website).
* Benutzer navigieren auf mehreren Tabs über Ihre Website. Das Browsen mit mehreren Tabs erhöht die Zahl der Besuche bzw. Besucher nicht, wohl aber das Browsen mit einem anderen Browser. Das liegt daran, dass unterschiedliche Tabs dasselbe Cookie referenzieren, unterschiedliche Browser tun dies jedoch nicht.

Ein Besuch verläuft jedoch nicht unbedingt gleichzeitig mit einer Browsersitzung. Mit anderen Worten, wenn ein Besucher den Browser schließt, ihn erneut öffnet und fünf Minuten später zu Ihrer Website zurückkehrt, wird dies als Fortsetzung des gleichen Besuchs erkannt. Wenn zudem ein Besucher auf einer Seite 35 Minuten lang verweilt, wird der Besuch geschlossen und verarbeitet, und ein neuer Besuch beginnt, wenn der Besucher zu einer anderen Seite durchklickt.

Beim Ende eines Besuchs laufen alle Variablen mit Besuchsablauf ab und werden nicht länger beibehalten. Die Metrik „Besuchnummer“ wird beim nächsten Besuch dieses Besuchers erhöht.

>[!NOTE]
>
>If you are using Analytics as the reporting source for Adobe Target, refer to [Minimizing Inflated Visit and Visitor Counts in A4T](https://marketing.adobe.com/resources/help/en_US/target/a4t/minimizing-inflated-visit-and-visitor-counts-a4t.html) in the [!DNL Target] documentation.

Weitere Informationen finden Sie im Adobe Analytics-Implementierungshandbuch im Abschnitt zum [Identifizieren von Unique Visitors](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_overview.html).

**Zeiträume**

Ein Besuch wird für jeden Zeitraum berichtet, während dessen Aktivitäten verzeichnet wurden. Nehmen wir zum Beispiel an, dass ein Besuch am 1. Dezember um 23.45 Uhr beginnt und bis 00.30 Uhr am 2. Dezember fortgesetzt wird. Der Besuch wird am 1. und am 2. Dezember gezählt. Dies gilt auch für andere Zeiträume, wie einer Woche, einem Monat, einem Quartal und einem Jahr.
