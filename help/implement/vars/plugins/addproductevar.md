---
title: addProductEvar
description: Fügt der Produktvariablen Merchandising-eVars hinzu.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe-Plug-in:addProductEvar

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `addProductEvar` Plug-in können Sie einfach eine Adobe Analytics-Merchandising-eVar hinzufügen, die die Produktsyntax verwendet, ohne sich Gedanken darüber zu machen, ob der bereits vorhandene Inhalt der Produktvariablen geändert, verschoben oder gelöscht werden soll. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie der `products` Variablen einfach Merchandising eVars für die Produktsyntax hinzufügen möchten. Sie müssen das `addProductEvar` -Plug-in nicht verwenden, wenn Sie keine Merchandising-eVars mit Produktsyntax verwenden.

> [!NOTE] Dieses Plug-In ersetzt keine eVars, die bereits in einem Produkteintrag vorhanden sind. Es werden nur Werte angehängt, die Sie mit diesem Plug-In festlegen. Gehen Sie beim Anhängen von eVars, die für dieses Produkt bereits vorhanden sind, mit Bedacht vor.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Fügen Sie für jede Startregel, bei der Sie das Plug-In verwenden möchten, eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialisieren von addProductEvar
1. Speichern und veröffentlichen Sie die Änderungen an der Regel

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
1. Erweitern Sie die [!UICONTROL Verfolgung mithilfe eines benutzerdefinierten Code] -Akkordeons, das die Schaltfläche zum [!UICONTROL Öffnen des Editors] anzeigt.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung `s_gi`). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: addProductEvar v1.0 */
s.addProductEvar=function(en,ev,ap){if("string"===typeof en&&"string"===typeof ev&&""!==ev)if(ap=ap||!1,this.products){var e=this.products.split(","),f=e.length;ap=ap?0:f-1;for(var a;ap<f;ap++)a=e[ap].split(";"),a[5]&&-1<a[5].toLowerCase().indexOf("evar")?a[5]=a[5]+"|"+en+"="+ev:a[5]?a[5]=en+"="+ev:a[5]||(a[4]||(a[4]=""),a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[5]=en+"="+ev),e[ap]=a.join(";");this.products=e.join(",")}else this.products=";;;;;"+en+"="+ev};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Das `addProductEvar` Plug-In verwendet die folgenden Argumente:

* **`en`**(erforderlich, Zeichenfolge): Die eVar, die zum letzten Eintrag hinzugefügt werden soll, der derzeit in der Produktvariablen enthalten ist. Wenn die Produktvariable leer ist, erstellt das Plug-In einen &quot;leeren&quot;Produkteintrag mit dem eVar-Wert am Ende des Eintrags.
* **`ev`**(erforderlich, Zeichenfolge): Der der eVar zugewiesene Wert.
* **`ap`**(optional, boolean): Wenn die Produktvariable derzeit mehr als einen Produkteintrag enthält, wird mit dem Wert true (oder 1) die eVar zu** allen **Produkteinträgen hinzugefügt.  Der Standardwert ist &quot;false&quot;(oder 0), wodurch die eVar nur dem** letzten **Eintrag in der Produktvariablen hinzugefügt wird.

Das `addProductEvar` Plug-In gibt nichts zurück. Stattdessen wird die im `en` und- `ev` Argument angegebene eVar (und der eVar-Wert) zur `products` Variablen hinzugefügt.

## Beispiele

```js
// Set a merchandising eVar to blue on the last product. The output for the products variable is ";product1;3;300,;product2;2;122,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
s.addProductEvar("eVar1", "blue");

// Set a merchandising eVar to blue on all products. The output for the products variable is ";product1;3;300;;eVar1=blue,;product2;2;122;;eVar1=blue,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
s.addProductEvar("eVar1", "blue", true);

// Set multiple merchandising eVars to the last product in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
s.addProductEvar("eVar23", "medium");
s.addProductEvar("eVar24", "women");
s.addProductEvar("eVar1", "red");

// Set multiple merchandising eVars to all products in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue|eVar23=medium|eVar24=women|eVar1=red,;product2;2;122;;eVar23=medium|eVar24=women|eVar1=red,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
s.addProductEvar("eVar23", "medium", true);
s.addProductEvar("eVar24", "women", true);
s.addProductEvar("eVar1", "red", true);

// If the products variable is not set, the plug-in creates an empty product string correctly delimited to the merchandising eVar. The output for the products variable is ";;;;;eVar1=blue"
s.addProductEvar("eVar1", "blue");
```

## Versionsverlauf

### 1.0 (7. Oktober 2019)

* Erstes Release.
