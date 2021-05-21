---
title: Util.getQueryParam
description: Gibt den Wert eines Abfragezeichenfolgenparameters zurück.
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '256'
ht-degree: 100%

---

# Util.getQueryParam

Abfragezeichenfolgenparameter in einer Browser-URL enthalten häufig wichtige Daten für Analytics. Verwenden Sie die `Util.getQueryParam()`-Methode, um Daten aus der Abfragezeichenfolge abzurufen.

## Abrufen von Abfragezeichenfolgenparameterdaten in Adobe Experience Platform Launch

Sie können Abfragezeichenfolgenparameterdaten abrufen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] [!UICONTROL Core] aus und setzen Sie [!UICONTROL Datenelementtyp] auf [!UICONTROL Abfragezeichenfolgenparameter].
5. Geben Sie den Abfragezeichenfolgenparameter in das Textfeld ein.

Der Wert des Abfragezeichenfolgenparameters wird im Datenelement gespeichert. Anschließend können Sie auf das Datenelement in Regeln verweisen, um Analytics-Variablen zuzuweisen.

## s.Util.getQueryParam() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Rufen Sie die `s.Util.getQueryParam()`-Methode auf, um einen Abfragezeichenfolgenwert aus der Browser-URL abzurufen. Das Zeichenfolgenargument, das einen Abfragezeichenfolgenparameter enthält, ist erforderlich. Diese Methode gibt eine Zeichenfolge zurück, die Sie Analytics-Variablen zuweisen können:

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

Ein drittes optionales Argument ermöglicht es Ihnen, das Trennzeichen für die Abfragezeichenfolge anzupassen. Der Standardwert lautet `&`. Sie können diesen Wert ändern, wenn Ihre Abfragezeichenfolge ein anderes Trennzeichen verwendet.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

>[!TIP]
>
>Ein ähnliches Plug-in namens [`s.getQueryParam`](../plugins/getqueryparam.md) ist verfügbar. Dieses Plug-in enthält erweiterte Funktionen, ist aber auch komplexer und standardmäßig nicht in AppMeasurement enthalten.
