---
title: Dynamische Variablen
description: Kopieren Sie Variablen, ohne die Bildanforderungslänge zu erhöhen.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# Dynamische Variablen

Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die Bildanforderungslänge zu erhöhen. Sie sind hilfreich, wenn Sie dieselben Daten in mehreren Variablen erfassen.

In früheren Versionen von Analytics war die Länge der Bildanforderung wichtig, um abgeschnittene Daten zu verhindern. Verbesserungen an AppMeasurement ermöglichen wesentlich längere Abfragezeichenfolgen für Bildanforderungen, sodass dynamische Variablen normalerweise nicht benötigt werden.

Dynamische Variablen unterstützen Abfragezeichenfolgenparameter oder HTTP-Header in einer Bildanforderung. Eine vollständige Liste der verfügbaren Parameter, die referenziert werden können, finden Sie unter [Datenerfassungs-Abfrageparameter](../../validate/query-parameters.md) . Eine vollständige Liste der verfügbaren HTTP-Anforderungsfelder, die referenziert werden können, finden Sie unter [Standard-Anforderungsfelder](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields) in Wikipedia.

Wenn Adobe ein Präfix für dynamische Variablen erkennt, kopiert es automatisch die Abfragezeichenfolge oder den HTTP-Header-Wert in Ihrer Report Suite. Diese Aktion erfolgt vor jeder anderen Verarbeitung, einschließlich Verarbeitungsregeln und VISTA-Regeln.

> [!TIP] Achten Sie beim Kopieren von Variablen auf maximale Zeichenbeschränkungen. Beim Kopieren `eVar1` in `prop1`kann `prop1` beispielsweise ein abgeschnittener Wert verwendet werden, da er eine Beschränkung von 100 Byte aufweist (wohingegen `eVar1` eine Beschränkung von 255 Byte gilt).

## Dynamische Variablen beim Start der Adobe Experience Platform

Sie können dynamische Variablen in jedem Dimensionsfeld verwenden, das eine Zeichenfolge akzeptiert. Dimensionswerte werden normalerweise beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festgelegt.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den gewünschten Dimensionswert.

Platzieren Sie das Präfix der dynamischen Variablen in das Textfeld, gefolgt vom Abfragezeichenfolgenparameter oder dem HTTP-Header, auf den Sie verweisen möchten. Standardmäßig ist das Präfix der dynamischen Variablen `D=`festgelegt.

## Dynamische Variablen in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Dynamische Variablen sind Textzeichenfolgen, die anderen Variablen zugewiesen werden. Das standardmäßige Präfix für dynamische Variablen lautet `D=`. Bei dynamischen Variablen wird zwischen Groß- und Kleinschreibung unterschieden.

```js
// Copy eVar1 into eVar2. The query string parameter of eVar1 is v1.
s.eVar1 = "Example value";
s.eVar2 = "D=v1";

// Take the user agent string found in the image request HTTP header and place it in eVar1.
s.eVar1 = "D=User-Agent";

// Copy the page URL and place it in eVar1. The query string parameter of page URL is g.
s.eVar1 = "D=g";
```

> [!NOTE] Dynamische Variablen werden beim Debugging Ihrer Implementierung als Zeichenfolgen angezeigt. Werte werden serverseitig von Adobe-Datenerfassungsservern kopiert.
