---
description: Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.
keywords: Analytics-Implementierung
seo-description: Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.
seo-title: Pfade nach Benutzertyp segmentieren
solution: Analytics
title: Pfade nach Benutzertyp segmentieren
topic: Entwickler und Implementierung
uuid: 5c298f39-381d-453b-a608-109e3276b361
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Pfade nach Benutzertyp segmentieren

Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.

Sie können den Benutzertyp und Seitennamen in einer [!UICONTROL Eigenschaftsvariablen] kombinieren und die Pathing-Funktion für die [!UICONTROL sprop] aktivieren.

Sie haben zwei Typen von Benutzern: _Registered_ und _Non-Registered_. Sie möchten auf jeder Seite zwischen diesen beiden Benutzertypen unterscheiden können. Daher setzen Sie diese Werte in eine dafür vorgesehene [!UICONTROL sprop] ein. Das Auffüllen der Eigenschaftsvariablen sieht wie folgt aus:

```js
 s.prop1="Registered : " + s.pageName;
```

Wenn der Benutzer ein registrierter Benutzer war, der die Homepage besucht hat, enthält die Eigenschaftsvariable den folgenden Wert:

```js
 "Registered : Home Page"
```

Wenn der Benutzer auf eine weitere Seite namens „Page 2“ geklickt hat, sieht der Wert für diese Seite so aus:

```js
 "Registered : Page 2"
```

Bei aktivierter [!UICONTROL Pathing]-Funktion werden Ihnen diese beiden Werte nacheinander angezeigt. Wenn Sie wissen möchten, welchen Weg registrierte Benutzer von der Homepage aus eingeschlagen haben, suchen Sie in einem der Pfadberichte nach dem Wert „Registered : Home Page“ und schauen Sie, welche Seiten danach besucht wurden. In diesem Fall wäre das „Page 2“.
