---
description: Der Kunde ist dafür verantwortlich, in der JS-Datei oder im HTML-Code vorgenommene Änderungen selbst zu testen. Dies muss erfolgen, bevor die Änderungen für Produktionswebsites veröffentlicht werden.
keywords: Analytics-Implementierung
seo-description: Der Kunde ist dafür verantwortlich, in der JS-Datei oder im HTML-Code vorgenommene Änderungen selbst zu testen. Dies muss erfolgen, bevor die Änderungen für Produktionswebsites veröffentlicht werden.
seo-title: Codeänderungen
solution: Analytics
title: Codeänderungen
topic: Entwickler und Implementierung
uuid: efac 045 e -15 f 5-45 f 6-a 21 a-de 6 c 4 b 0 a 8185
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Codeänderungen

Der Kunde ist dafür verantwortlich, in der JS-Datei oder im HTML-Code vorgenommene Änderungen selbst zu testen. Dies muss erfolgen, bevor die Änderungen für Produktionswebsites veröffentlicht werden.

Ensure that the linefeeds/return characters are not stripped or altered from the code that is placed within the HTML, or from within the [!DNL .JS] file. Vergewissern Sie sich, dass der JavaScript-Code auf allen Seiten und Seitenvorlagen ohne Fehler ausgeführt wird (Klicken Sie dazu in Internet Explorer auf „Internetoptionen“, wählen Sie die Registerkarte „Erweitert“ aus, und aktivieren Sie „Skriptfehler anzeigen“.).

Fügen Sie den Code bei Ihren Fehlertests in eine standardmäßige HTML-Seite ein, um festzustellen, ob der Fehler auch bei anderen auf der Seite enthaltenen Elementen/Objekten auftritt.

```js
<html><head></head><body>
...paste code here to debug...
</body></html>
```

