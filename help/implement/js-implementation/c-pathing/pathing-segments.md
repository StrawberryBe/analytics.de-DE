---
description: Damit man erfahren kann, welche Wege bestimmte Typen von Benutzern auf einer Site einschlagen, müssen Pfade nach dem Benutzertyp segmentiert sein.
keywords: Analytics Implementation
title: Pfade nach Benutzertyp segmentieren
topic: Developer and implementation
uuid: 5c298f39-381d-453b-a608-109e3276b361
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

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
