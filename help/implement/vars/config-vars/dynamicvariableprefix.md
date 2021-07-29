---
title: dynamicVariablePrefix
description: Ermöglicht die Anpassung der Zeichenfolge zur Identifizierung dynamischer Variablen.
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 89%

---

# dynamicVariablePrefix

Dynamische Variablen sind ein Kurzkonzept, mit dem Sie Werte von einer Variablen in eine andere kopieren können. Sie sind für lange Variablenwerte nützlich, da sie dazu beitragen, die URL-Länge einer Bildanforderung zu verkürzen. Weitere Informationen zu diesem Konzept finden Sie unter [Dynamische Variablen](../page-vars/dynamic-variables.md).

Dynamische Variablen verwenden standardmäßig das Präfix `D=`. Mit der `dynamicVariablePrefix`-Variablen können Sie die Zeichenfolge zur Identifizierung dynamischer Variablen anpassen. Dabei ist die Groß-/Kleinschreibung zu beachten.

## Dynamisches Variablenpräfix mithilfe von Tags in Adobe Experience Platform

„Dynamisches Variablenpräfix“ ist ein Feld unter dem Akkordeon [!UICONTROL Globale Variablen] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Globale Variablen], wodurch das Feld [!UICONTROL Dynamisches Variablenpräfix] angezeigt wird.

Dieses Feld enthält standardmäßig `D=`. Sie können den Wert ändern, wenn Sie ein anderes Präfix für dynamische Variablen verwenden möchten. Sie können jeden gewünschten Wert verwenden, sofern er mit der Zeichencodierung auf Ihrer Website übereinstimmt.

## s.dynamicVariablePrefix in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die `s.dynamicVariablePrefix`-Variable ist eine Zeichenfolge, die eine beliebige Folge von Zeichen enthalten kann. Wenn diese Variable nicht definiert ist, verwendet AppMeasurement standardmäßig die Zeichenfolge `D=`.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
