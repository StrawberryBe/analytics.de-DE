---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# purchaseID

Die „“ verhindert, dass eine Bestellung in Berichten mehrmals gezählt wird.


<!-- 

purchaseID.xml

 -->

Wann immer das [!UICONTROL Kaufereignis] auf Ihrer Site verwendet wird, sollten Sie die Variable *`purchaseID`* verwenden.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 20 Byte | purchaseID | Konversion &gt; Einkäufe &gt; Umsatzkonversion | "" |

Wenn ein Besucher einen Artikel auf Ihrer Site einkauft, wird *`purchaseID`* auf der Seite „Vielen Dank!“ an der gleichen Stelle aufgefüllt, an der das [!UICONTROL Kauf]ereignis ausgelöst wird. Wenn *`purchaseID`* aufgefüllt ist, werden die Produkte auf der Seite „Vielen Dank!“ nur einmal pro *`purchaseID`* gezählt. Das ist überaus wichtig, da viele Besucher die Dankseite oder die Bestätigungsseite für Informationszwecke speichern werden. Die Variable *`purchaseID`* verhindert, dass bereits getätigte Einkäufe jedes Mal gezählt werden, wenn die gespeicherte Seite erneut angezeigt wird.

Zusätzlich dazu, dass die Kaufdaten nicht doppelt gezählt werden, verhindert *`purchaseID`* bei Verwendung, dass alle Konversionsdaten in Berichten doppelt gezählt werden.

**Syntax und mögliche Werte** {#section_E352CE2370D54BA69A368E1F63A9C32D}

```js
s.purchaseID="unique_id"
```

*`purchaseID`* darf maximal 20 Zeichen lang sein und nur normale ASCII-Zeichen enthalten.

**Beispiele** {#section_60A5C1EAF42F4611898CD6A4F4CF5A28}

```js
s.purchaseID="11223344" 
s.purchaseID="a8g784hjq1mnp3"
```

**Konfigurationseinstellungen** {#section_1808631C96674380BF9C4A6D9A2C568E}

Keine

**Probleme, Fragen und Tipps** {#section_F5D010F234ED43F19AD1FCD2CD64E060}

Die Variable *`purchaseID`* ermöglicht es, dass alle auf der Seite enthaltenen Konversionsvariablen in Berichten nur einmal gezählt werden.
