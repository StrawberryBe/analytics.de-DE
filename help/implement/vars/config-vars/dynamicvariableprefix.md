---
title: dynamicVariablePrefix
description: Ermöglicht die Anpassung der Zeichenfolge zur Identifizierung dynamischer Variablen.
translation-type: tm+mt
source-git-commit: 03a4c0d5e080219a7fd96dff33ce122669351ac3
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 100%

---


# dynamicVariablePrefix

Dynamische Variablen sind ein Kurzkonzept, mit dem Sie Werte von einer Variablen in eine andere kopieren können. Sie sind für lange Variablenwerte nützlich, da sie dazu beitragen, die URL-Länge einer Bildanforderung zu verkürzen. Weitere Informationen zu diesem Konzept finden Sie unter [Dynamische Variablen](../page-vars/dynamic-variables.md).

Dynamische Variablen verwenden standardmäßig das Präfix `D=`. Mit der `dynamicVariablePrefix`-Variablen können Sie die Zeichenfolge zur Identifizierung dynamischer Variablen anpassen. Dabei ist die Groß-/Kleinschreibung zu beachten.

## Dynamisches Variablenpräfix in Adobe Experience Platform Launch

„Dynamisches Variablenpräfix“ ist ein Feld unter dem Akkordeon [!UICONTROL Globale Variablen] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Globale Variablen], wodurch das Feld [!UICONTROL Dynamisches Variablenpräfix] angezeigt wird.

Dieses Feld enthält standardmäßig `D=`. Sie können den Wert ändern, wenn Sie ein anderes Präfix für dynamische Variablen verwenden möchten. Sie können jeden gewünschten Wert verwenden, sofern er mit der Zeichencodierung auf Ihrer Website übereinstimmt.

## s.dynamicVariablePrefix in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.dynamicVariablePrefix`-Variable ist eine Zeichenfolge, die eine beliebige Folge von Zeichen enthalten kann. Wenn diese Variable nicht definiert ist, verwendet AppMeasurement standardmäßig die Zeichenfolge `D=`.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
