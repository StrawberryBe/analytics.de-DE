---
description: Die Import- und Exportdatei enthält sechs Spalten für jede Nummerisch 2 Classification.
seo-description: Die Import- und Exportdatei enthält sechs Spalten für jede Nummerisch 2 Classification.
seo-title: Nummerisch -2 Classifications importieren
solution: Analytics
subtopic: Classifications
title: Nummerisch -2 Classifications importieren
topic: Admin Tools
uuid: 82 a 3034 c-e 002-4991-900 f -22 dd 45 d 54910
translation-type: tm+mt
source-git-commit: 49e149fe57d5d66b8eda22b1bdf60e7c6200761c

---


# Nummerisch -2 Classifications importieren

>[!IMPORTANT]
>
>Die Möglichkeit, die Classifications „Numerisch 2“ und „Datumsaktiviert“ zu importieren, wurde aus der Codebasis entfernt. Diese Änderung wird mit der Wartungsversion vom Juli 2019 wirksam. Wenn die Importdatei die Spalte „Numerisch“ oder „Datumsaktiviert“ enthält, werden diese Zellen still ignoriert und alle anderen Daten in dieser Datei werden normal importiert. Vorhandene Classifications können weiterhin über den Standard-Classification-Arbeitsablauf exportiert werden und sind weiterhin in Berichten verfügbar.

Die Import- und Exportdatei enthält sechs Spalten für jede Nummerisch 2 Classification.

In den folgenden Definitionen wird davon ausgegangen, dass der Name Ihrer Nummerisch 2 Classification „MyCost“ lautet.

**~MyCost:** Ein beschreibender Name für die Zeile.

**~ Meinekosten ^~id~:** Die ID zum Bearbeiten einer vorhandenen Zeile. Wenn Sie eine neue Zeile hinzufügen, sollte diese leer sein. Eine ID wird automatisch zugewiesen, wenn Sie einen Export aus dem Classification-Manager vornehmen.

**~MyCost^~value~: **The value for the row. Wenn die Ratenspalte festgestellt (fixed) ist, ist dies ein Pauschalwert, der über den gesamten Zeitraum verteilt wird. Wenn die Ratenspalte ein Ereignis ist, ist dies der Multiplikator für das Ereignis. Dieser Eintrag sollte keine Kommas enthalten.

**~ Meinekosten ^~period~:** Der Zeitraum, auf den diese Zeile bezieht. Hierbei muss ein Anfangs- und ein Enddatum eingegeben werden, getrennt durch einen Bindestrich. Vor und nach dem Bindestrich muss ein Leerzeichen stehen. Die Definition muss das folgende Format aufweisen:

JJJJ/MM/TT – JJJJ/MM/TT

**~ Meinekosten ^~rate~:** Das Ereignis, das mit der [!UICONTROL Wert-] Spalte multipliziert werden soll. Gültige Werte sind:

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

**~ Meinekosten ^~hinge~:** Das Ereignis, mit dem der Wert während einer Aufschlüsselung verteilt wird. This value is often the same as [!UICONTROL ~MyCost^~rate~], unless you are using [!UICONTROL fixed]. The valid values for this column are identical to that of [!UICONTROL ~MyCost^~rate~], with the addition of [!UICONTROL none].
