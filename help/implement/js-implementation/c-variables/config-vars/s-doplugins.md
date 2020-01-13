---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---



# s.doPlugins

Die Variable „“ ist ein Verweis auf die Funktion „“ und soll dafür sorgen, dass die Funktion „“ in der JavaScript-Datei an der richtigen Stelle aufgerufen wird.

Die Funktion *`s_doPlugins`* wird jedes Mal aufgerufen, wenn eines der folgenden Ereignisse eintritt:

* Die Funktion *`t()`* wird aufgerufen
* Die Funktion *`tl()`* wird aufgerufen
* auf einen Exit- oder Downloadlink geklickt wird.
* auf ein Seitenelement geklickt wird, das mittels Besucherklickzuordnung nachverfolgt wird.

Die Variable *`doPlugins`* dient zum Ausführen angepasster Routinen für die Sammlung oder Änderungen von Daten. Wenn Sie einen anderen Objektnamen als „s“ verwenden, müssen Sie sicherstellen, dass *`s_doPlugins`* richtig umbenannt wird. Wenn Ihr Objektname beispielsweise „s_mc“ lautet, sollte die Funktion *`s_doPlugins`* „s_mc_doPlugins“ heißen.

## Syntax und mögliche Werte

Die Funktion *`s_doPlugins`* sollte nicht in Anführungszeichen gesetzt werden, und *`doPlugins`* muss immer dem genauen Namen der Funktion *`s_doPlugins`* zugeordnet werden (wenn diese Funktion umbenannt wird).

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

Keine

## Probleme, Fragen und Tipps

* Der einzige Grund, den Objektnamen zu ändern (z. B. von „s“ zu „s_mc“), wäre, wenn Sie Inhalt mit anderen Benutzern teilen oder von anderen Benutzern beziehen möchten. Beim Umbenennen der Funktion *`s_doPlugins`* in [!UICONTROL s_mc_doPlugins] stellt sicher, dass die JavaScript-Datei eines anderen Clients Ihre Funktion *`doPlugins`* nicht überschreibt.

* Wenn Sie unerwartet damit beginnen, Inhalte von einem anderen Adobe-Kunden abzurufen, und Ihre Funktion *`s_doPlugins`* überschrieben wird, können Sie die Funktion *`s_doPlugins`* einfach umbenennen, ohne den Objektnamen zu ändern. Wählen Sie einfach einen anderen Objektnamen, als andere JavaScript-Dateien auf der gleichen Seite verwenden würden – das ist zwar nicht erforderlich, stellt jedoch die beste Lösung dar.
