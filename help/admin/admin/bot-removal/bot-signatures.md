---
title: Allgemeine Bot-Signaturen
description: Erkennen Sie die allgemeinen Bezeichner von Bots.
translation-type: tm+mt
source-git-commit: 2f4c54ec57eeddc03f0b0d12a0a7f391e36ab0fc
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 1%

---


# Allgemeine Bot-Signaturen

Während die Identifizierung von Bots in einem Datensatz je nach Umgebung unterschiedlich ist, gibt es einige gängige Möglichkeiten, Bots zu identifizieren.

## Hohe Anzahl an Ansichten pro Besuch

Sie können einen Bericht zur Data Warehouse mit IP-Adresse, Ansichten und eindeutigen Besuchern abrufen. Erstellen Sie dann in Excel eine &#x200B; &#x200B; für die Ansichten pro Besuch und sortieren Sie vom höchsten zum niedrigsten. Bots haben in der Regel eine sehr hohe Anzahl von Ansichten pro Besuch (mehrere Hundert bis Tausende). Wenn Sie sich in echten Traffic bewegen, wird es einen starken Rückgang geben.

## Kein Werber

Bots haben normalerweise keine verweisende URL. In der Segmentierung kann dies als `Referring Domain equals Typed/Bookmarked` gefiltert werden.

## Seltsame Benutzeragenten

Bots verwenden häufig benutzerdefinierte Benutzeragenten, die nicht in die Browser-Dimension klassifiziert sind oder als `unknown`-Version eines Standardbrowsers angezeigt werden. Unbekannte Safari und unbekannte Opera haben eine extrem hohe Wahrscheinlichkeit, Bots zu sein.

## Linux- oder &quot;Nicht angegeben&quot;-Betriebssysteme

Wir wollen das großartige Open-Source-Linux-Betriebssystem nicht diskreditieren, aber anscheinend stellen Bots es gerne als Betriebssystem ein. Achten Sie jedoch darauf, legitimen Traffic von Linux-Benutzern auszuschließen. Bots legen auch gerne kein Betriebssystem fest, das als `Operating System &#x200B;equals Not Specified` segmentiert werden kann.

## Ansichten der Seite = Besuche = Individuelle Besucher

Dies gilt insbesondere für den Benutzeragenten-Bericht. Wie Sie im folgenden Screenshot sehen können, hat die &quot;unbekannte Version&quot;dieser Browser fast dieselbe Anzahl von Besuchern wie individuelle Besucher (und fast dieselbe Anzahl von Ansichten). Dies kann in der Segmentierung isoliert werden, indem ein [!UICONTROL Include]-Container für `Single Page Visits equals Enabled` oder `Hit Depth is less than 2` erstellt wird.

![](assets/bots-browsers-unknown.png)

## Besuch Nr. 1

Bots erhalten in der Regel bei jeder Ausführung eine neue Besucher-ID, sodass nur ein Besuch stattfindet und der gesamte Traffic aus einer Besuchsnummer von 1 besteht.

## Niedrigere Bildschirmauflösungen

Moderne Benutzer haben viel höhere Bildschirmauflösungen als in den letzten Jahren. Treffer mit den folgenden Auflösungen scheinen bei Bots sehr beliebt zu sein:

* 1024 x 768&#x200B;&#x200B;
* 1366 x 768
* 1600 x 864
* 800 x 600
* 1600 x 1200
* Nicht angegeben
* 1024 x 667

## Land- und Zeitzonenabweichung

Sie würden eine Diskrepanz zwischen dem Ursprungsland und der Zeitzone feststellen. Der Ort könnte beispielsweise die Vereinigten Staaten sein, aber die Zeitzone könnte GMT sein.

![](assets/bots-country-time-zone.png)

## Nicht angemeldet

Der Benutzer meldet sich zu keinem Zeitpunkt bei seinem Besuch an, und seine eVars zur Benutzeridentifizierung bleiben nicht von vorherigen Besuchen erhalten. Während einige Bots für die Authentifizierung eingerichtet werden können, sind die meisten nicht so intelligent.

## Keine KPIs beim Besuch

Bots fügen in der Regel keine Produkte zum Einkaufswagen hinzu oder checken aus. Meistens senden sie keine Interessentenformulare oder andere Erfolgsformulare, aber einige Bots senden einfache HTML-Ereignisse. &#x200B;

## Spezifische Abfrage vorhanden

Manchmal versuchen Bots, Sites zu zwischenspeichern oder auf andere Weise zu umbrechen, indem sie fehlerhafte URLs oder URLs, die nicht vorhanden sind (wie z. B. LAMP- oder Wordpress-Admin-Seiten) oder bestimmte Abfragen-Zeichenfolgen anhängen.

## IP-Adressen, die von verteilten Computing-Plattformen stammen

Webhosting-Dienste wie Amazon Web Services oder Google Cloud können als Bot-Farmen missbraucht werden. Diese IP-Adressen sind mit einem hohen Risiko verbunden, Bots zu sein:
&#x200B;
* [Google Cloud](https://cloud.google.com/compute/): IP-Adressen-Beginn mit  `&#x200B;35.199` oder  `35.194&#x200B;`
