---
description: Hier finden Sie die Antwort, wenn Sie wissen möchten, wohin die Benutzer weiter navigieren, nachdem Sie über eine Kampagne auf Ihre Site gelangt sind.
keywords: Analytics-Implementierung
seo-description: Hier finden Sie die Antwort, wenn Sie wissen möchten, wohin die Benutzer weiter navigieren, nachdem Sie über eine Kampagne auf Ihre Site gelangt sind.
seo-title: Pfade nach Kampagne oder Rückverfolgungscode
solution: Analytics
title: Pfade nach Kampagne oder Rückverfolgungscode
topic: Entwickler und Implementierung
uuid: eb 6 e 3484-1 b 40-4 ec 6-8017-ac 1003 cdf 636
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pfade nach Kampagne oder Rückverfolgungscode

Hier finden Sie die Antwort, wenn Sie wissen möchten, wohin die Benutzer weiter navigieren, nachdem Sie über eine Kampagne auf Ihre Site gelangt sind.

Dazu müssen Sie eine [!UICONTROL sprop] festlegen, die für diesen Bericht verwendet werden soll. Dann müssen Sie die Daten, mit denen diese Eigenschaftsvariable aufgefüllt werden soll, auf eine Weise strukturieren, die bei aktivierter Pathing-Funktion sinnvoll ist.

Im folgenden Beispiel soll [!UICONTROL prop1] als Kampagnenpfadeigenschaft dienen. Nun wird in der [!UICONTROL sprop] der gleiche Wert eingetragen, der in der Variablen [!UICONTROL Seitenname] abgelegt wird. Das sieht dann so aus:

```js
s.prop1=s.pageName;
```

Dies sollten Sie auf allen Seiten durchführen, sofern der Benutzer nicht von einer Kampagne aus geklickt hat. Wenn Benutzer auf eine Kampagne geklickt haben und sich auf der Landingpage der Kampagne befinden, wird in dieser Eigenschaftsvariablen eine Kombination aus Kampagne und [!UICONTROL pagename] eingetragen. Das sieht dann so aus:

```js
 s.prop1=s.campaign + ‘ : ’ + s.pageName;
```

Wenn die angeklickte Kampagne „banner1234“ hieß und der Benutzer so auf die Einstiegsseite „Homepage“ gelangte, würde in dieser Eigenschaftsvariablen der Wert „banner1234 : Homepage“ stehen. Auf allen nachfolgenden Seiten wird der Wert von [!UICONTROL pagename] wie oben gezeigt zur Eigenschaftsvariablen hinzugefügt.

Wenn ein Benutzer auf diese Kampagne klickt und bei seinem Besuch insgesamt vier Seiten anzeigt, enthält die Eigenschaftsvariable die folgenden Werte in der entsprechenden Reihenfolge:

```js
“banner1234 : Home Page” > “Page 2” > “Page 3” > “Page 4”
```

Wenn die Daten auf diese Weise in der [!UICONTROL prop1] erfasst sind und die Pathing-Funktion aktiviert ist, können Sie in den verschiedenen Pfadsetzungsberichten erkennen, welchen Weg Besucher auf Ihrer Site eingeschlagen haben, nachdem sie auf eine Kampagne geklickt haben.

Sie können eine Startseite festlegen, von der aus der Pfadbericht beginnen soll. In diesem Fall würden Sie „banner1234 : Homepage“ auswählen, da Sie wissen möchten, zu welchen Unterseiten Ihre Besucher navigiert haben, nachdem sie auf die Kampagne „banner1234“ geklickt haben. Dieser Bericht ist nur einer von vielen Pfadsetzungsberichten.
