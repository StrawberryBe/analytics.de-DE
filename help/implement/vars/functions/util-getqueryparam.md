---
title: Util.getQueryParam
description: Gibt den Wert eines Abfragezeichenfolgenparameters zurück.
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Util.getQueryParam

Abfragezeichenfolgenparameter in einer Browser-URL enthalten häufig wichtige Daten für Analytics. Verwenden Sie die `Util.getQueryParam` Methode, um Daten aus der Abfragezeichenfolge abzurufen.

## Abrufen von Abfragezeichenfolgen-Parameterdaten in Adobe Experience Platform Launch

Sie können Abfragezeichenfolgen-Parameterdaten abrufen, indem Sie Werte in Datenelementen festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Setzen Sie das [!UICONTROL Erweiterungs] -Dropdown auf [!UICONTROL Core]und den [!UICONTROL Datenelementtyp] auf [!UICONTROL Abfragezeichenfolgenparameter].
5. Geben Sie den Abfragezeichenfolgenparameter in das Textfeld ein.

Der Parameterwert für die Abfragezeichenfolge wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.getQueryParam() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Rufen Sie die `s.Util.getQueryParam()` Methode auf, um einen Abfragezeichenfolgenwert aus der Browser-URL abzurufen. Das Zeichenfolgenargument, das einen Abfragezeichenfolgenparameter enthält, ist erforderlich. Diese Methode gibt eine Zeichenfolge zurück, die Sie Analytics-Variablen zuweisen können:

```js
s.eVar1 = s.Util.getQueryParam("cid");
```

Ein zweites optionales Argument ermöglicht es Ihnen, die Zeichenfolge anzugeben, die auf Abfragezeichenfolgenparameter überprüft werden soll. Standardmäßig überprüft das Dienstprogramm die Browser-URL.

```js
// Search a custom string for query string parameter
var customString = "https://example.com?q=search";

// eVar1 is set to "search"
s.eVar1 = s.Util.getQueryParam("q",customString);
```

Ein drittes optionales Argument ermöglicht es Ihnen, das Trennzeichen für die Abfragezeichenfolge anzupassen. Its default value is `&`. Sie können diesen Wert ändern, wenn Ihre Abfragezeichenfolge ein anderes Trennzeichen verwendet.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

> [!NOTE] In früheren Versionen von AppMeasurement war ein Plug-in mit dem Namen `s.getQueryParam` verfügbar. Dieses Plug-in ist nicht mehr erforderlich, da es jetzt standardmäßig in AppMeasurement enthalten ist.
