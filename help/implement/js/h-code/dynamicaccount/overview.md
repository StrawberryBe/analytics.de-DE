---
title: Übersicht über dynamische Konten
description: Erfahren Sie, wie Sie eine Report Suite mit H-Code dynamisch auswählen.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# Übersicht über dynamische Konten

> [!IMPORTANT] Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder beim Starten der Adobe Experience Platform nicht unterstützt.

Dynamische Konten sind eine Implementierungsfunktion, mit der Sie anhand der von Ihnen definierten Kriterien festlegen können, welche Report Suite verwendet werden soll. Wenn Ihr Unternehmen mehr als eine Report Suite benötigt, aber dieselbe Implementierung zwischen Ihren Sites verwenden möchte, sind dynamische Konten eine gute Lösung.

> [!TIP] Adobe empfiehlt, Daten an eine einzelne Report Suite zu senden und dann bei Bedarf Virtual Report Suites zu verwenden, um Daten zu trennen. Weitere Informationen finden Sie unter Überlegungen[ zu ](../../../prepare/global-rs.md)globalen Report Suites.

3 Variablen werden zur dynamischen Auswahl einer Report Suite verwendet.

* [`dynamicAccountSelection`](dynamicaccountselection.md): Aktivieren oder deaktivieren Sie die dynamische Kontoauswahl.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): Bestimmt, welcher Wert zu beachten ist. Beispielsweise die URL oder eine Abfragezeichenfolge.
* [`dynamicAccountList`](dynamicaccountlist.md): Vergleicht die Werte mit `dynamicAccountMatch`und füllt bei Übereinstimmung die `account` Variable aus.

Wenn `dynamicAccountSelection = true`, wird der Wert innerhalb `dynamicAccountMatch` mit `dynamicAccountList`verglichen. Wenn die Werte übereinstimmen, `dynamicAccountList` wird die Report Suite-ID in die `account` Variable einbezogen.

## Standard-Report Suite

Die Variable `account` kann zuvor festgelegt werden und dient dann als Standardwert für den Fall, dass keine der angegebenen Zeichenfolgen gefunden wird. Beispiel:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

Wenn `location.hostname` weder `dev.example.com` noch `example.com`der Treffer vorhanden war, wird der Treffer an gesendet `examplersiddefault`.

## Multi-Suite-Tagging

Multi-Suite-Tagging kann mit der dynamischen Kontoauswahl verwendet werden. Beispiel:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

Wenn `location.hostname` er `example.com`enthält, wird der Treffer sowohl an `examplersid1` als auch `examplersid2`gesendet.
