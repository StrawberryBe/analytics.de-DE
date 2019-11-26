---
title: Interner Kanal (Sitzungsaktualisierung)
description: Lesen Sie mehr über den Kanal "Intern"(Sitzungsaktualisierung).
translation-type: tm+mt
source-git-commit: cf05e9f5d666fd40e74028929a831dad57ee2007

---


# Interner Kanal (Sitzungsaktualisierung)

Der interne Kanal (häufig in Sitzungsaktualisierung umbenannt) besteht aus Besuchen auf der Site, bei denen die verweisende URL mit der Einrichtung der internen URL-Filter in der Admin-Konsole übereinstimmt. Das bedeutet, dass der Besucher von der Site kam, um seinen Besuch zu starten.

![](assets/int-channel1.png)

## Best Practices überschreiben

Es empfiehlt sich, die Option "Last Touch außer Kraft setzen"für direkte und interne Kanäle zu deaktivieren, damit sie keine Gutschriften von anderen (oder anderen) beständigen Last Touch-Kanälen erhalten.

>[!NOTE]In diesem Dokument wird davon ausgegangen, dass die Einstellungen für Direkt- und Sitzungsaktualisierung "Einstellungen überschreiben"deaktiviert sind.

![](assets/int-channel2.png)

## Einsatzzeitraum

Sowohl die First Touch- als auch die Last Touch-Kanäle eines Besuchers werden nach 30 Tagen Inaktivität in diesem Browser zurückgesetzt.

>[!NOTE] 30 Tage sind die Standardeinstellung und können bei Bedarf über die Admin-Einstellungen geändert werden.

Wenn der Besucher die Site häufig nutzt, wird das Interaktionsfenster mit ihm rolliert. Sie müssen 30 Tage inaktiv sein, damit der Zeitraum abläuft und die Kanäle zurückgesetzt werden.
Beispiel:

* Tag 1: Der Benutzer gelangt auf der Anzeige zur Site. First Touch- und Last Touch-Kanäle werden auf Display eingestellt.

* Tag 2: Der Benutzer gelangt auf die Seite "Kostenlose Suche". First Touch bleibt angezeigt, Last Touch ist auf "Kostenlose Suche"eingestellt.

* Tag 35: Der Benutzer ist seit 33 Tagen nicht mehr auf der Site und kehrt mit der Registerkarte zurück, die er in seinem Browser geöffnet hatte. Bei einem Interaktionsfenster von 30 Tagen wäre das Fenster geschlossen und die Marketingkanal-Cookies wären abgelaufen. Der First Touch- und Last Touch-Kanal wird zurückgesetzt und auf Session Refresh eingestellt, da der Benutzer von einer internen URL kam.

## Beziehung zwischen Erstkontakt und Letztkontakt

Um die Interaktion zwischen First Touch und Last Touch zu verstehen und zu bestätigen, dass Außerkraftsetzungen erwartungsgemäß funktionieren, können Sie einen First Touch-Kanalbericht abrufen, der sich auf einen Last Touch-Kanalbericht bezieht, wobei Ihre wichtigste Erfolgsmetrik hinzugefügt wird (siehe Beispiel unten). Das Beispiel zeigt die Interaktion zwischen First Touch- und Last Touch-Kanälen.

![](assets/int-channel3.png)

Die Kreuzung, an der "first equals last touch"markiert ist, wird orange hervorgehoben. Sowohl Direct- als auch Session Refresh erhalten nur dann eine Last Touch-Gutschrift, wenn sie auch der First Touch-Kanal sind, da sie keine Gutschrift von anderen beständigen Kanälen erhalten können (hervorgehobene Zeilen in Grau).

## Warum wird die Sitzung aktualisiert?

Da wir wissen, dass eine Aktualisierung der Sitzung nur bei einem First Touch-Ereignis erfolgen kann, erläutern die folgenden Szenarien, wie die Sitzungsaktualisierung ein First Touch-Kanal sein könnte.

### Szenario 1: Sitzungs-Timeout

Ein Besucher ruft die Website auf und lässt die Registerkarte dann in seinem Browser geöffnet, um sie später zu verwenden. Die Interaktionszeit des Besuchers läuft ab (oder sie löschen ihre Cookies freiwillig) und sie verwenden die Registerkarte "Öffnen", um die Website erneut zu besuchen. Da die verweisende URL eine interne Domäne ist, wird der Besuch als Sitzungsaktualisierung klassifiziert.

### Szenario 2: Nicht alle Seiten der Site sind mit Tags versehen

Ein Besucher landet auf Seite A, die nicht mit Tags versehen ist, und wechselt dann zu Seite B, die mit Tags versehen ist. Seite A wird als interne verweisende Stelle angesehen und der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 3: Umleitungen

Wenn eine Umleitung nicht so eingerichtet ist, dass Daten der verweisenden Stelle an die neue Seite der Landung weitergegeben werden, gehen die Daten der verweisenden Stelle verloren und jetzt erscheint die Umleitungsseite (wahrscheinlich eine interne Seite) als verweisende Domäne. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 4: Domänenübergreifender Traffic

Ein Besucher wechselt von einer Domäne, die zu Suite A auslöst, zu einer zweiten Domäne, die zu Suite B ausgelöst wird. Wenn in Suite B die internen URL-Filter die erste Domäne enthalten, wird der Besuch in Suite B als intern aufgezeichnet, da Marketingkanäle ihn als neuen Besuch in der zweiten Suite sehen. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 5: Lange Ladezeiten der Einstiegsseite

Ein Besucher landet auf Seite A, die stark mit Inhalt umgeht, und der Adobe Analytics-Code befindet sich unten auf der Seite. Bevor der gesamte Inhalt (einschließlich Adobe Analytics-Bildanforderung) geladen werden kann, klickt der Besucher auf Seite B. Seite B löst die Adobe Analytics-Bildanforderung aus. Da die Bildanforderung von Seite A nie geladen wurde, wird die zweite Seite als erster Treffer des Besuchs in Adobe Analytics angezeigt, wobei Seite A als verweisende Stelle dient. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 6: Löschen von Cookies mitten auf der Site

Ein Besucher besucht die Site, und während der Zwischensitzung werden die Cookies gelöscht. Sowohl First Touch- als auch Last Touch-Kanäle werden zurückgesetzt, und der Besuch wird als Sitzungsaktualisierung klassifiziert (weil die verweisende Stelle intern sein würde).
