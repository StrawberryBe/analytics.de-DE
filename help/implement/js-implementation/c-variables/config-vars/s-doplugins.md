---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---



# s.doPlugins

Die Variable „“ ist ein Verweis auf die Funktion „“ und soll dafür sorgen, dass die Funktion „“ in der JavaScript-Datei an der richtigen Stelle aufgerufen wird.

The *`s_doPlugins`* function is called each time any of the following occurs:

* Die *`t()`* Funktion
* Die *`tl()`* Funktion
* auf einen Exit- oder Downloadlink geklickt wird.
* auf ein Seitenelement geklickt wird, das mittels Besucherklickzuordnung nachverfolgt wird.

Die Variable *`doPlugins`* dient zum Ausführen angepasster Routinen für die Sammlung oder Änderungen von Daten. If you are using an object name other than "s," make sure that the *`s_doPlugins`* is renamed appropriately. Wenn Ihr Objektname beispielsweise s_mc lautet, sollte die *`s_doPlugins`* Funktion s_mc_doPlugins heißen.

## Syntax und mögliche Werte

Die *`s_doPlugins`* Funktion sollte nicht in Anführungszeichen gesetzt werden und *`doPlugins`* immer dem genauen Namen der *`s_doPlugins`* Funktion zugeordnet werden (wenn diese Funktion umbenannt wird).

```js
s.doPlugins=s_doPlugins;
```

## Beispiele

```js
s.doPlugins=s_doPlugins;
```

```js
s_mc.doPlugins=s_mc_doPlugins;
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Der einzige Grund, den Objektnamen zu ändern (z. B. von „s“ zu „s_mc“), wäre, wenn Sie Inhalt mit anderen Benutzern teilen oder von anderen Benutzern beziehen möchten. Beim Umbenennen der  *`s_doPlugins`* function to [!UICONTROL s_mc_doPlugins] ensures that another client's JavaScript file does not overwrite your *`doPlugins`* function.

* Wenn Sie unerwartet damit beginnen, Inhalte von einem anderen Adobe-Kunden abzurufen, und Ihre *`s_doPlugins`* *`s_doPlugins`* Funktion überschrieben wird, können Sie die Funktion einfach umbenennen, ohne den Objektnamen zu ändern. Wählen Sie einfach einen anderen Objektnamen, als andere JavaScript-Dateien auf der gleichen Seite verwenden würden – das ist zwar nicht erforderlich, stellt jedoch die beste Lösung dar.