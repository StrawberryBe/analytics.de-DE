---
title: Kanal „Intern“ (Sitzungsaktualisierung)
description: Lesen Sie mehr über den Kanal „Intern“ (Sitzungsaktualisierung).
translation-type: ht
source-git-commit: 490a856effac7ec3ff2430dff0ffdcee587bf933

---


# Kanal „Intern“ (Sitzungsaktualisierung)

Der Kanal „Intern“ (häufig in „Sitzungsaktualisierung“ umbenannt) besteht aus Besuchen auf der Site, bei denen die verweisende URL mit der Einrichtung von internen URL-Filtern in der Admin Console übereinstimmt. Das bedeutet, dass der Besucher seinen Besuch innerhalb der Site gestartet hat.

![](assets/int-channel1.png)

## Überschreiben von Best Practices

Es empfiehlt sich, die Option zum Außerkraftsetzen des Letztkontakts für die Kanäle „Direkt“ und „Intern“ zu deaktivieren, damit sie keine Gutschriften von anderen persistenten Letztkontakt-Kanälen (oder voneinander) erhalten.

>[!NOTE]In diesem Dokument wird davon ausgegangen, dass die Einstellungen zum Außerkraftsetzen für Direkt- und Sitzungsaktualisierung deaktiviert sind.

![](assets/int-channel2.png)

## Interaktionszeitraum

Sowohl die Erstkontakt- als auch die Letztkontakt-Kanäle eines Besuchers werden nach 30 Tagen Inaktivität in diesem Browser zurückgesetzt.

>[!NOTE] 30 Tage sind die Standardeinstellung, die bei Bedarf über die Admin-Einstellungen geändert werden kann.

Wenn der Besucher die Site häufig nutzt, passt sich das Interaktionsfenster daran an. Der Besucher muss 30 Tage lang inaktiv sein, damit der Zeitraum abläuft und die Kanäle zurückgesetzt werden.
Beispiel:

* Tag 1: Der Benutzer gelangt per Anzeige zur Site. Erstkontakt- und Letztkontakt-Kanäle werden auf „Anzeige“ eingestellt.

* Tag 2: Der Benutzer gelangt per natürlicher Suche zur Site. Erstkontakt bleibt „Anzeige“, Letztkontakt wird auf „Natürliche Suche“ eingestellt.

* Tag 35: Der Benutzer war seit 33 Tagen nicht mehr auf der Site und kehrt über die Registerkarte zurück, die er in seinem Browser geöffnet hatte. Bei einem Interaktionsfenster von 30 Tagen wäre das Fenster geschlossen, und die Marketingkanal-Cookies wären abgelaufen. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt und auf „Sitzungsaktualisierung“ eingestellt, da der Benutzer von einer internen URL kam.

## Beziehung zwischen Erstkontakt und Letztkontakt

Um die Interaktion zwischen Erstkontakt und Letztkontakt zu verstehen und zu bestätigen, dass Außerkraftsetzungen erwartungsgemäß funktionieren, können Sie einen Erstkontakt-Kanalbericht abrufen, der sich auf einen Letztkontakt-Kanalbericht bezieht, wobei Ihre wichtigste Erfolgsmetrik hinzugefügt wird (siehe Beispiel unten). Das Beispiel zeigt die Interaktion zwischen Erstkontakt- und Letztkontakt-Kanälen.

![](assets/int-channel3.png)

Die Schnittmenge, bei der Erstkontakt mit Letztkontakt übereinstimmt, ist orange hervorgehoben. Sowohl „Direkt“ als auch „Sitzungsaktualisierung“ erhalten nur dann eine Letztkontakt-Gutschrift, wenn sie auch der Erstkontakt-Kanal sind, da sie keine Gutschrift von anderen persistenten Kanälen erhalten können (grau hervorgehobene Zeilen).

## Warum kommt es zu einer Sitzungsaktualisierung?

Da wir wissen, dass eine Letztkontakt-Sitzungsaktualisierung nur erfolgen kann, wenn es sich gleichzeitig um den Erstkontakt handelt, wird in den Szenarien unten erläutert, wie die Sitzungsaktualisierung ein Erstkontakt-Kanal sein kann.

### Szenario 1: Sitzungstimeout

Ein Besucher ruft die Website auf und lässt die Registerkarte dann in seinem Browser geöffnet, um sie später erneut zu verwenden. Der Interaktionszeitraum des Besuchers läuft ab (oder er löscht seine Cookies freiwillig), und er verwendet die geöffnete Registerkarte, um die Website erneut zu besuchen. Da die verweisende URL eine interne Domäne ist, wird der Besuch als Sitzungsaktualisierung klassifiziert.

### Szenario 2: Nicht alle Seiten der Site sind mit Tags versehen

Ein Besucher landet auf Seite A, die nicht mit Tags versehen ist, und wechselt dann zu Seite B, die mit Tags versehen ist. Seite A wird als interner Referrer angesehen, und der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 3: Umleitungen

Wenn eine Umleitung nicht so eingerichtet ist, dass Referrer-Daten an die neue Landingpage weitergegeben werden, gehen die Referrer-Daten verloren, und die Umleitungsseite (wahrscheinlich eine interne Seite) erscheint als Referrer-Domäne. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 4: Domänenübergreifender Traffic

Ein Besucher wechselt von einer Domäne, die zu Suite A führt, zu einer zweiten Domäne, die zu Suite B führt wird. Wenn in Suite B die internen URL-Filter die erste Domäne enthalten, wird der Besuch in Suite B als intern aufgezeichnet, da Marketingkanäle ihn als neuen Besuch in der zweiten Suite sehen. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 5: Lange Ladezeiten der Entrypage

Ein Besucher landet auf Seite A mit viel Inhalt, und der Adobe Analytics-Code befindet sich unten auf der Seite. Bevor der gesamte Inhalt (einschließlich Adobe Analytics-Bildanforderungen) geladen werden kann, klickt der Besucher auf Seite B. Seite B löst ihre Adobe Analytics-Bildanforderung aus. Da die Bildanforderung von Seite A nie geladen wurde, wird die zweite Seite als erster Treffer des Besuchs in Adobe Analytics angezeigt, wobei Seite A als Referrer dient. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

### Szenario 6: Löschen von Cookies mitten auf der Site

Ein Besucher besucht die Site und löscht seine Cookies während der Sitzung. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt, und der Besuch wird als Sitzungsaktualisierung klassifiziert (weil der Referrer intern ist).
