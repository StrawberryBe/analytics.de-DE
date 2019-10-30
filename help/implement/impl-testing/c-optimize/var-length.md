---
description: Die Länge von Analytics-Variablen hat Auswirkungen auf die Größe des HTML-Codeausschnitts, der JavaScript-Bibliotheksdatei und der Bildanforderung.
keywords: Analytics-Implementierung
seo-description: Die Länge von Analytics-Variablen hat Auswirkungen auf die Größe des HTML-Codeausschnitts, der JavaScript-Bibliotheksdatei und der Bildanforderung.
seo-title: Länge von Variablen
solution: Analytics
subtopic: Fehlerbehebung
title: Länge von Variablen
topic: Entwickler und Implementierung
uuid: 87deabb3-2acb-4797-9a65-769d9e2fbd62
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Länge von Variablen

Die Länge von Analytics-Variablen hat Auswirkungen auf die Größe des HTML-Codeausschnitts, der JavaScript-Bibliotheksdatei und der Bildanforderung.

Wenn viele Variablen vorliegen, die lang sind (60 Zeichen oder mehr), können die Werte durch kürzere Bezeichner ersetzt werden. Mithilfe von Daten-Classifications oder VISTA-Regeln können diese Bezeichner in verständliche Anzeigenamen übersetzt werden.

> [!NOTE] Die meisten Analytics-Variablen haben eine maximale Länge von 100 Zeichen (eVars sind maximal 255 Zeichen lang). In Internet Explorer dürfen URLs für GET-Bildanforderungen insgesamt höchstens 2.048 Zeichen lang sein. Der Grenzwert für Bildanforderungen gilt nicht nur für die Variablen, sondern auch für Informationen zum Browser, Betriebssystem und Browser-Plug-ins (nur Netscape/Mozilla).

