---
description: Der Kunde ist dafür verantwortlich, in der JS-Datei oder im HTML-Code vorgenommene Änderungen selbst zu testen. Dies muss erfolgen, bevor die Änderungen für Produktionswebsites veröffentlicht werden.
keywords: Analytics Implementation
solution: Analytics
title: Codeänderungen
topic: Developer and implementation
uuid: efac045e-15f5-45f6-a21a-de6c4b0a8185
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Codeänderungen

Der Kunde ist dafür verantwortlich, in der JS-Datei oder im HTML-Code vorgenommene Änderungen selbst zu testen. Dies muss erfolgen, bevor die Änderungen für Produktionswebsites veröffentlicht werden.

Achten Sie darauf, dass die Zeichen für Zeilenumbruch/Zeilenvorschub nicht von dem im HTML-Code oder in der [!DNL .JS]-Datei befindlichen Code abgeschnitten oder verändert werden. Vergewissern Sie sich, dass der JavaScript-Code auf allen Seiten und Seitenvorlagen ohne Fehler ausgeführt wird (Klicken Sie dazu in Internet Explorer auf „Internetoptionen“, wählen Sie die Registerkarte „Erweitert“ aus, und aktivieren Sie „Skriptfehler anzeigen“.).

Fügen Sie den Code bei Ihren Fehlertests in eine standardmäßige HTML-Seite ein, um festzustellen, ob der Fehler auch bei anderen auf der Seite enthaltenen Elementen/Objekten auftritt.

```js
<html><head></head><body>
...paste code here to debug...
</body></html>
```

