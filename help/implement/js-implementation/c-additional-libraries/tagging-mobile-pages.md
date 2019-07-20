---
description: Trackingcode für Mobilgeräte wird in Form eines vom Server generierten Bildes auf der Seite untergebracht.
keywords: Analytics-Implementierung; Mobilverfolgung; mobile Protokolle; Zwischenspeicherung verhindern; alt-Tag; Standardbildtyp
seo-description: Trackingcode für Mobilgeräte wird in Form eines vom Server generierten Bildes auf der Seite untergebracht.
seo-title: Tagging vonseiten für Mobilfunkprotokolle
solution: Analytics
title: Tagging vonseiten für Mobilfunkprotokolle
topic: Entwickler und Implementierung
uuid: beaf-f 309-4918-a 99 c-a 3 e 591668205
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Tagging vonseiten für Mobilfunkprotokolle

Trackingcode für Mobilgeräte wird in Form eines vom Server generierten Bildes auf der Seite untergebracht.

Trackingcode für Mobilgeräte wird in Form eines vom Server generierten Bildes auf der Seite untergebracht. Da Skriptsprachen wie JavaScript und WMLScript nicht generell auf allen Mobilgeräten unterstützt werden, kann das Tracking-Beacon nicht dynamisch über eine Skriptsprache generiert werden.

· Obwohl das Mobilfunk-Beacon-Bild eigentlich 2 x 2 Pixel groß ist, sollten Sie für die Höhe und die Breite den Wert 5 festlegen, um die Unterstützung aller Mobilgeräte zu gewährleisten. Beispiel:

```
<img sr c="https://metric.mydomain.com/b/ss/<Report_Suite_Name>/5/<random_number>?pageName=" alt="" width="5" height="5"/>
```

## Verhinderung von Zwischenspeicherung durch Einsatz einer Zufallszahl {#section_BF5C344A16034C439C8704632CF673A7}

Auch wenn Adobe-Server die Browser anweisen, das Tracking-Beacon nicht zwischenzuspeichern, kann nicht garantiert werden, dass sich alle Browser an diese Anweisung halten. Als weitere Vorsichtsmaßnahme wird daher empfohlen, dass serverseitig eine Zufallszahl im URL-Pfad des Bildes dynamisch generiert wird. Dadurch wird die Genauigkeit der Angaben in Berichten verbessert. Die Zufallszahl sollte im letzten Abschnitt des Pfades stehen:

```js
<img src="https://rsid.112.2O7.net/b/ss/rsid/5/H.5--WAP/12345?pageName=" />.
```

## Einfügen eines ALT-Tags {#section_FBD8B2FD1EA0429580C2B933DA300B07}

Bei einigen mobilen Browsern ist es erforderlich, dass das Image-Tag jedes Bildes einen alternativen Text enthält. Dieses ALT-Attribut im Image-Tag sieht wie folgt aus:

```js
<img src="https://rsid.112.2O7.net/b/ss/rsid/5/H.5--WAP/12345?pageName=" alt=""/>.
```

Wichtig ist, dass im Pfad immer korrekt die Zeichenfolge „/5/“ steht. Anhand dieser Zeichenfolge können Adobe-Server mobile Geräte erkennen. Wenn die standardmäßige Zeichenfolge „/1/“ verwendet wird, versuchen Adobe-Server, auf dem mobilen Gerät ein Cookie abzulegen.

## Ändern des Standard-Bildtyps {#section_2F969909010D4A64BF6E092A32ABADB7}

Wenn der Standard-Bildtyp auf einem bestimmten Gerät nicht unterstützt wird, werden keine Daten zurückgegeben. Um dies zu vermeiden, können Sie erzwingen, dass der Adobe-Datenerfassungsserver einen bestimmten Grafiktyp zurückgibt, den das Mobilgerät unterstützt. Der Code nach dem Report Suite-Namen gibt den Bildtyp an:

* `/5/` gibt den Standard-Bildtyp zurück.
* `/5.1/` oder `/1/` gibt immer ein GIF-Bild zurück.

* `/5.5/` gibt stets ein WBMP-Bild zurück.

See [Identifying Visitors using Mobile Protocols](../../../implement/js-implementation/c-unique-visitors/visid-mobile.md#concept_8C5557634014440AA3588FBB0CF6BB49).
