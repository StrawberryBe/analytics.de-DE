---
title: Allgemeine Bot-Signaturen
description: Erkennen Sie die üblichen Kennungen von Bots.
feature: Bot Removal
exl-id: 57622af6-c1d3-4ef1-b3e6-10c14f04a55c
source-git-commit: f6199620033af9c8e304bd0f537d4e0b052ed64d
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 100%

---

# Allgemeine Bot-Signaturen

Während die Identifizierung von Bots in einem Datensatz je nach Umgebung unterschiedlich ist, gibt es einige gängige Möglichkeiten, Bots zu erkennen.

## Hohe Anzahl an Seitenansichten pro Besuch

Sie können einen Data Warehouse-Bericht mit IP-Adresse, Ansichten und Unique Visitors abrufen. Erstellen Sie dann in Excel eine Berechnung für Seitenaufrufe pro Besuch und sortieren Sie vom höchsten zum niedrigsten Wert. Bots haben in der Regel eine sehr hohe Anzahl von Seitenansichten pro Besuch (mehrere Hundert bis Tausende). Wenn Sie sich dem tatsächlichen realen Traffic nähern, werden Sie einen starken Rückgang feststellen.

## Keine verweisende Stelle

Bots haben normalerweise keine verweisende URL. In der Segmentierung kann dies als `Referring Domain equals Typed/Bookmarked` gefiltert werden.

## Seltsame Benutzeragenten

Bots verwenden häufig benutzerdefinierte Benutzeragenten, die nicht in die Browser-Dimension klassifiziert sind oder als `unknown`-Version eines Standard-Browsers angezeigt werden. Unbekannte Safari- und unbekannte Opera-Einträge haben eine extrem hohe Wahrscheinlichkeit, Bots zu sein.

## Linux oder „Nicht angegeben“ als Betriebssysteme

Wir wollen das großartige Open-Source-Betriebssystem Linux nicht diskreditieren, aber anscheinend legen Bots es gerne als ihr angebliches Betriebssystem fest. Gehen Sie jedoch mit Bedacht vor, wenn Sie nicht legitimen Traffic von Linux-Benutzern ausschließen. Bots legen auch gerne gar kein Betriebssystem fest, was als `Operating System &#x200B;equals Not Specified` segmentiert werden kann.

## Seitenansichten = Besuche = Individuelle Besucher

Dies gilt insbesondere für den Benutzeragenten-Bericht. Wie Sie im folgenden Screenshot sehen können, hat die „unbekannte Version“ dieser Browser fast dieselbe Anzahl von Besuchern wie Unique Visitors (und fast dieselbe Anzahl von Seitenansichten). Dies kann in der Segmentierung isoliert werden, indem ein [!UICONTROL Include]-Container für `Single Page Visits equals Enabled` oder `Hit Depth is less than 2` erstellt wird.

![](assets/bots-browsers-unknown.png)

## Besuchsanzahl von 1

Bots erhalten in der Regel bei jeder Ausführung eine neue Besucher-ID, sodass nur ein Besuch stattfindet und ihr gesamter Traffic aus einer Besuchsanzahl von 1 besteht.

## Niedrigere Bildschirmauflösungen

Moderne Benutzer haben viel höhere Bildschirmauflösungen als in den letzten Jahren. Treffer mit den folgenden Auflösungen scheinen bei Bots sehr beliebt zu sein:

* 1024 x 768&#x200B;&#x200B;
* 1366 x 768
* 1600 x 864
* 800 x 600
* 1600 x 1200
* Nicht angegeben
* 1024 x 667

## Land und Zeitzone stimmen nicht überein

Sie könnten eine Diskrepanz zwischen dem Ursprungsland und der Zeitzone feststellen. Der Ort kann beispielsweise in den Vereinigten Staaten sein, während die Zeitzone GMT ist.

![](assets/bots-country-time-zone.png)

## Nicht angemeldet

Der Benutzer meldet sich zu keinem Zeitpunkt bei seinem Besuch an und seine eVars zur Benutzeridentifizierung bleiben nicht von vorherigen Besuchen erhalten. Während einige Bots für eine Authentifizierung eingerichtet werden können, sind die meisten nicht so intelligent.

## Keine KPIs beim Besuch

Bots fügen in der Regel keine Produkte zum Warenkorb hinzu und führen keinen Checkout durch. Meistens übermitteln sie keine Lead-Formulare oder andere Erfolgsereignisse, aber einige Bots übermitteln durchaus einfache HTML-Formulare.

## Spezifische Abfragezeichenfolge vorhanden

Manchmal versuchen Bots, den Cache zu sprengen oder anderweitig Websites zu zerstören, indem sie auf fehlerhafte oder nicht existierende URLs zugreifen (wie typische LAMP- oder Wordpress-Admin-Seiten) oder indem sie bestimmte Abfragezeichenfolgen anhängen.

## IP-Adressen, die von verteilten Computing-Plattformen stammen

Webhosting-Services wie Amazon Web Services oder Google Cloud können als Bot-Farmen missbraucht werden. Diese IP-Adressen sind mit einem hohen Risiko verbunden, Bots zu sein:
&#x200B;
* [Google Cloud](https://cloud.google.com/compute/): IP-Adresse beginnt mit `&#x200B;35.199` oder mit `35.194&#x200B;`
