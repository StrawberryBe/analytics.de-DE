---
description: Die Import- und Exportdatei enthält sechs Spalten für jede Numerisch 2 Classification.
subtopic: Classifications
title: Numerisch 2 Classifications importieren
topic: Admin tools
uuid: 82a3034c-e002-4991-900f-22dd45d54910
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Numerisch 2 Classifications importieren

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juli 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert, und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

Die Import- und Exportdatei enthält sechs Spalten für jede Numerisch 2 Classification.

In den folgenden Definitionen wird davon ausgegangen, dass der Name Ihrer Numerisch 2 Classification „MyCost“ lautet.

**~MyCost:** Ein beschreibender Name für die Zeile.

**~MyCost^~id~:** Die ID zum Bearbeiten einer bestehenden Zeile. Wenn Sie eine neue Zeile hinzufügen, sollte diese leer sein. Eine ID wird automatisch zugewiesen, wenn Sie einen Export aus dem Classification-Manager vornehmen.

**~MyCost^~value~:** Die Werte für die Zeile. Wenn die Ratenspalte festgestellt (fixed) ist, ist dies ein Pauschalwert, der über den gesamten Zeitraum verteilt wird. Wenn die Ratenspalte ein Ereignis ist, ist dies der Multiplikator für das Ereignis. Dieser Eintrag sollte keine Kommas enthalten.

**~MyCost^~period~:** Der Zeitraum, auf den diese Zeile sich bezieht. Hierbei muss ein Anfangs- und ein Enddatum eingegeben werden, getrennt durch einen Bindestrich. Vor und nach dem Bindestrich muss ein Leerzeichen stehen. Die Definition muss das folgende Format aufweisen:

JJJJ/MM/TT – JJJJ/MM/TT

**~MyCost^~rate~:** Das Ereignis, das mit der [!UICONTROL Wert]-Spalte multipliziert wird. Gültige Werte sind:

* fixed – zeigt an, dass es sich um einen festen Wert handelt, der über den Zeitraum verteilt wird.
* revenue
* order
* unit
* scopen
* scviews
* instance
* click
* checkout
* scadd
* scremove
* event 1
* event 2
* etc

**~MyCost^~hinge~:** Das Ereignis, mit dem der Wert während einer Aufschlüsselung verteilt wird. Dieser Wert ist oft mit dem Wert [!UICONTROL ~MyCost^~rate~] identisch, es sei denn, Sie verwenden den Zusatz [!UICONTROL fixed]. Die gültigen Werte für diese Spalte sind identisch mit denen von [!UICONTROL ~MyCost^~rate~], mit dem Zusatz [!UICONTROL none].
