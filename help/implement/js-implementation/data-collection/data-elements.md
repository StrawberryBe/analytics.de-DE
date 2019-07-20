---
description: Sie können die Werte von Formularelementen (z. B. Optionsfelder oder Kontrollkästchen) in Berichten erfassen. Dies hilft Ihnen bei der Analyse der wahrscheinlichsten Auswahlmöglichkeiten in Ihren Onlineformularen.
keywords: Analytics-Implementierung
seo-description: Sie können die Werte von Formularelementen (z. B. Optionsfelder oder Kontrollkästchen) in Berichten erfassen. Dies hilft Ihnen bei der Analyse der wahrscheinlichsten Auswahlmöglichkeiten in Ihren Onlineformularen.
seo-title: Daten aus Formularelementen erfassen
solution: Analytics
title: Daten aus Formularelementen erfassen
topic: Entwickler und Implementierung
uuid: e 0 c 13 b 96-e 1 ca -4744-a 912-60 ca 2 b 8 f 25 c 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Daten aus Formularelementen erfassen

Sie können die Werte von Formularelementen (z. B. Optionsfelder oder Kontrollkästchen) in Berichten erfassen. Dies hilft Ihnen bei der Analyse der wahrscheinlichsten Auswahlmöglichkeiten in Ihren Onlineformularen.

Wenn es zum Beispiel eine Optionsschaltfläche gibt, über die der Benutzer seine bevorzugte Musikrichtung auswählen kann (z. B. Rock, Rap, Klassik oder Jazz), können Sie die getroffenen Entscheidungen in einer Variablen erfassen, um die Musikvorlieben Ihrer gesamten Zielkundschaft zu ermitteln.

Auf welche Weise diese Daten am besten erfasst werden, hängt davon ab, wie Ihre Formulare verarbeitet werden. Außerdem kommt es auch darauf an, ob die zu erfassenden Formular-Auswahlmöglichkeiten in der Abfragezeichenfolge auf der Seite, die der Formularübermittlung folgt, verfügbar sind. Die Beispiele in diesem Artikel sind in PHP angegeben. Sie können diese Konzepte aber auch in anderen Sprachen adaptieren, abhängig von Ihrer Serverumgebung.

Diese Informationen sind für fortgeschrittene Benutzer gedacht, die sowohl mit der Berichterstellung als auch der Implementierung gut vertraut sind. Änderungen sollten Sie an Ihrer Implementierung nur dann vornehmen, wenn Sie genau wissen, welche Folgen dies hat. Falls Implementierungsänderungen erforderlich sind, wenden Sie sich an den Account-Manager Ihres Unternehmens.

## GET-Methode {#section_7A2B35822BFF4F6EB57940B31AE6303A}

Wenn Ihr Formular die [!UICONTROL GET]-Methode zur Datenübermittlung nutzt, können Sie in der Abfragezeichenfolge der URL für die auf die Formularübermittlung folgende Seite auf die gewünschten Daten zugreifen. Sie können das Plug-in  [!UICONTROL getQueryParam] nutzen, um diese Daten aus der Abfragezeichenfolge automatisch zu erfassen und es in der Variablen Ihrer Auswahl zu platzieren.

## POST-Methode {#section_56715C30EF374BA7AA12B946B50E4A9A}

Wenn Ihr Formular Daten mittels einer [!UICONTROL POST]-Methode überträgt (was der gängigere Weg ist), stehen Ihnen die Ergebnisse für jedes einzelne Formularelement in [!UICONTROL $_POST superglobal] zur Verfügung. Um dies in einer Variablen zu erfassen, müssen Sie den Namen des jeweils gewünschten Formularelements ermitteln. Für das oben gezeigte Beispiel zum Musikgenre würde der Teil mit dem betreffenden Formularelement wie folgt aussehen:

```
<input type="radio" name="music_genre" value="rock">
```

Dieses Optionsfeld gehört zum Formularelement „musik_genre“. You then have access to the user's selected value by using $_POST['music_genre']. Dieser könnte in eine Variable geschrieben werden, die auf der Seite hinter der Formularübermittlung steht:

```js
s.eVar1="<?=$_POST['music_genre'];?>"
```

Diese [!UICONTROL eVar1]-Variable erhält dann eine Kopie des Wertes, der über das Formular an Ihren Server übermittelt wurde (in der Form Wert=Eigenschaft).

Für weitere Informationen zu dieser benutzerspezifischen Implementierungsmethode wenden Sie sich bitte an den Kundenbetreuer Ihrer Organisation. Dieser kann dann ein Treffen mit einem Ihrer Implementierungsberater ansetzen, um die von Ihnen gewünschte Hilfe zu leisten.
