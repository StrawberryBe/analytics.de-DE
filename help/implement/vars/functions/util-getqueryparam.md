---
title: Util.getQueryParam
description: Gibt den Wert eines Abfrage-String-Parameters zurück.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Util.getQueryParam

Abfragen-Zeichenfolgenparameter in einer Browser-URL enthalten häufig wichtige Daten für Analytics. Verwenden Sie die `Util.getQueryParam()` Methode, um Daten aus der Abfrage-Zeichenfolge abzurufen.

## Abrufen von Parameterdaten für Abfragen-Zeichenfolgen in Adobe Experience Platform Launch

Sie können Parameterdaten zu Abfragen-Zeichenfolgen abrufen, indem Sie Werte in Datenelementen festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Data Elements] Registerkarte und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Legen Sie die [!UICONTROL Extension] Dropdown-Liste auf [!UICONTROL Core]und die [!UICONTROL Data Element Type] auf [!UICONTROL Query String Parameter].
5. Geben Sie den Parameter für die Zeichenfolge der Abfrage in das Textfeld ein.

Der Parameterwert für die Abfrage-Zeichenfolge wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.getQueryParam() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Rufen Sie die `s.Util.getQueryParam()` Methode auf, um einen Abfragen-Zeichenfolgenwert aus der Browser-URL abzurufen. Das Zeichenfolgenargument, das einen Abfrage-String-Parameter enthält, ist erforderlich. Diese Methode gibt eine Zeichenfolge zurück, die Sie Analytics-Variablen zuweisen können:

```js
s.eVar1 = s.Util.getQueryParam("cid");
```

Ein zweites optionales Argument ermöglicht es Ihnen, die Zeichenfolge anzugeben, die auf Zeichenfolgenparameter für Abfragen überprüft werden soll. Standardmäßig überprüft das Dienstprogramm die Browser-URL.

```js
// Search a custom string for query string parameter
var customString = "https://example.com?q=search";

// eVar1 is set to "search"
s.eVar1 = s.Util.getQueryParam("q",customString);
```

Ein drittes optionales Argument ermöglicht es Ihnen, das Trennzeichen für Abfragen-Zeichenfolgen anzupassen. Its default value is `&`. Sie können diesen Wert ändern, wenn Ihre Abfrage-Zeichenfolge ein anderes Trennzeichen verwendet.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

> [!TIP] Ein ähnliches Plug-in namens [`s.getQueryParam`](../plugins/getqueryparam.md) ist verfügbar. Dieses Plug-in enthält erweiterte Funktionen, ist aber auch komplexer und ist standardmäßig nicht in AppMeasurement enthalten.
