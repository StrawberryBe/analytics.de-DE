---
description: Eine Folge von Ansichten in einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen.
keywords: visit
title: Besuch
topic: Metrics
uuid: 91317487-f116-4546-8cd2-421418c49a7a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Besuch

Eine Folge von Ansichten in einer Sitzung. Die Besuchsmetrik wird häufig in Berichten verwendet, die die Anzahl der Besuchersitzungen in dem ausgewählten Zeitraum anzeigen.

>[!NOTE] Informationen dazu, wie Besuche und Aufrufe mobiler Apps berechnet werden, finden Sie unter [Vergleich von Besuchen und Aufrufen mobiler Apps](https://helpx.adobe.com/de/analytics/kb/compare-visits-and-mobile-app-launches.html) in der Knowledge Base.

Die Besuchsmetrik wird immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn ein Besucher zu Ihrer Site zurückkehrt. Eine Sitzung Beginn, wenn der Benutzer zum ersten Mal auf Ihre Site gelangt und in einem der folgenden Szenarien endet:

* **30 Minuten Inaktivität:** Fast alle Sitzungen enden auf diese Weise. Wenn mehr als 30 Minuten zwischen Bildanforderungen vergangen sind, beginnt ein neuer Besuch.
* **12 Stunden konsistente Aktivität:** Wenn ein Benutzer 12 Stunden lang keine Bildanforderungen mit einer Zeitspanne von mehr als 30 Minuten auslöst, wird automatisch ein neuer Besuch Beginn.
* **2500 Treffer:** Wenn ein Benutzer eine große Anzahl von Treffern generiert, ohne eine neue Sitzung zu starten, wird ein neuer Besuch nach 2500 Bildanforderungen gezählt.
* **100 Treffer in 100 Sekunden**: Wenn ein Besuch aus mehr als 100 Treffern besteht, die in weniger als 100 Sekunden stattfinden, endet der Besuch automatisch. Dieses Verhalten weist in der Regel auf eine Bot-Aktivität hin. Diese Einschränkung wird erzwungen, um zu verhindern, dass diese rechenintensiven Besuche die Latenz erhöhen und die Zeit für die Erstellung von Berichten erhöhen.

>[!NOTE] Die Definition eines Besuchs kann für eine Report Suite auf expliziten Wunsch hin gekürzt werden, sie kann aber nicht verlängert werden. Bitten Sie einen unterstützten Benutzer Ihres Unternehmens, sich an den Kundendienst zu wenden, um diese Änderung anzufordern.

In den folgenden Szenarien wird ein neuer Besuch nicht Beginn:

* Der Benutzer schließt die Registerkarte, öffnet sie erneut und navigiert innerhalb von 30 Minuten zurück zu Ihrer Site. Der Benutzer kann auch seinen Browser schließen oder den Computer neu starten und dennoch als Einzelbesuch gezählt werden (vorausgesetzt, der Besucher kehrt innerhalb des 30-Minuten-Zeitraums zu Ihrer Site zurück).
* Benutzer navigieren auf mehreren Registerkarten zu Ihrer Site. Das Browsen mit mehreren Tabs erhöht zwar nicht die Anzahl der Besuche oder Besucher, aber die Verwendung eines separaten Browsers ist dies nicht der Fall. Dies liegt daran, dass die verschiedenen Registerkarten auf dieselben Cookies verweisen, während separate Browser dies nicht tun.

Ein Besuch fällt nicht unbedingt mit einer Browsersitzung zusammen. Wenn ein Besucher beispielsweise den Browser schließt, den Browser erneut öffnet und fünf Minuten später zu Ihrer Site gelangt, wird dies als Fortsetzung desselben Besuchs erkannt. Das bedeutet auch, dass ein Besucher, der 35 Minuten lang auf einer Seite bleibt, geschlossen und verarbeitet wurde und ein neuer Besuch Beginn wird, wenn er zu einer anderen Seite durchklickt.

Wenn ein Besuch endet, sind alle Variablen mit Besuchsablauf abgelaufen und nicht mehr persistent. Die Besuchnummer-Metrik wird beim nächsten Besuch für diesen Besucher inkrementiert.

>[!NOTE] Wenn Sie Analytics als Quelle für die Berichterstellung für Adobe Target verwenden, schlagen Sie in der [!DNL Target]-Dokumentation unter [Minimieren zu hoher Besuchs- und Besucherzahlen in A4T](https://marketing.adobe.com/resources/help/de_DE/target/a4t/minimizing-inflated-visit-and-visitor-counts-a4t.html) nach.

Weitere Informationen finden Sie unter [Identifizieren individueller Besucher](https://marketing.adobe.com/resources/help/de_DE/sc/implement/visid_overview.html) im Implementierungshandbuch zu Adobe Analytics.

**Zeiträume**

Ein Besuch wird in jedem Zeitraum gemeldet, in dem die Aktivität eingetreten ist. Angenommen, ein Besuch beginnt am 1. Dezember um 23:45 Uhr und dauert bis 2. Dezember 12:30 Uhr. Der Besuch wird am 1. und 2. Dezember gezählt. Dieser Berichte gilt für andere Zeiträume, einschließlich Wochen-, Monats-, Quartals- und Jahreszeiten.
