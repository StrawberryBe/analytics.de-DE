---
description: Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.
keywords: Analytics-Implementierung
seo-description: Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.
seo-title: Pfade nach Benutzertyp segmentieren
solution: Analytics
title: Pfade nach Benutzertyp segmentieren
topic: Entwickler und Implementierung
uuid: 5c298f39-381d-453b-a608-109e3276b361
translation-type: ht
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# Pfade nach Benutzertyp segmentieren

Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.

Sie können den Benutzertyp und Seitennamen in einer [!UICONTROL Eigenschaftsvariablen] kombinieren und die Pathing-Funktion für die [!UICONTROL sprop] aktivieren.

Sie haben zwei Typen von Benutzern: _Registered_ und _Non-Registered_. Sie möchten auf jeder Seite zwischen diesen beiden Benutzertypen unterscheiden können. Daher setzen Sie diese Werte in eine dafür vorgesehene [!UICONTROL sprop] ein. Das Auffüllen der Eigenschaftsvariablen sieht wie folgt aus:

```js
 s.prop1=”Registered : “ + s.pageName;
```

Wenn der Benutzer ein registrierter Benutzer war, der die Homepage besucht hat, enthält die Eigenschaftsvariable den folgenden Wert:

```js
 “Registered : Home Page”
```

Wenn der Benutzer auf eine weitere Seite namens „Page 2“ geklickt hat, sieht der Wert für diese Seite so aus:

```js
 “Registered : Page 2”
```

Bei aktivierter [!UICONTROL Pathing]-Funktion werden Ihnen diese beiden Werte nacheinander angezeigt. Wenn Sie wissen möchten, welchen Weg registrierte Benutzer von der Homepage aus eingeschlagen haben, suchen Sie in einem der Pfadberichte nach dem Wert „Registered : Home Page“ und schauen Sie, welche Seiten danach besucht wurden. In diesem Fall wäre das „Page 2“.
