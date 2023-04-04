---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Workflow bei der Verwendung der Transaktions-ID-Datenquellen.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 54c88a275b48f2b401be450ce35767ab3ea9d40b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 10%

---

# Transaktions-ID-Datenquellen

Transaktions-ID-Datenquellen sind eine Variation von Zusammenfassungsdatenquellen, mit denen Sie Online- und Offline-Daten miteinander verknüpfen können. Dazu müssen Sie die [`transactionID`](/help/implement/vars/page-vars/transactionid.md)-Variablen in Ihrer Analytics-Implementierung verwenden.

* Wenn eine Zeile in einer Datenquellendatei eine Transaktions-ID enthält, die mit einer bereits von AppMeasurement erfassten Transaktions-ID übereinstimmt, werden die Dimensionen und Metriken an den Online-Treffer angehängt.
* Wenn eine Zeile in einer Datenquellendatei eine Transaktions-ID enthält, die keine Übereinstimmung enthält, wird die Zeile ähnlich wie die zusammenfassenden Datenquellen behandelt.

>[!NOTE]
>
>Bevor Sie Transaktions-ID-Datenquellen verwenden, müssen Sie sie zunächst in [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) für die gewünschte Report Suite.

Wenn Sie einen Online-Treffer senden, der eine [`transactionID`](/help/implement/vars/page-vars/transactionid.md) -Wert, erstellt Adobe einen &quot;Schnappschuss&quot;aller Variablen, die dann festgelegt oder beibehalten wurden. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Datenquellen hochgeladen wurde, werden die Offline- und Online-Daten miteinander verknüpft.

Transaktions-ID-Datenquellen haben die folgenden Eigenschaften:

* Die Online-Daten müssen zuerst erfasst und verarbeitet werden. Wenn eine Transaktions-ID-Datenquelle hochgeladen wird, bevor eine Report Suite einen Treffer verarbeitet, der mit dieser Transaktions-ID übereinstimmt, werden die Daten nicht verknüpft.
* Über AppMeasurement erfasste Transaktions-IDs laufen nach etwa 90 Tagen ab. Wenn Ihr Unternehmen ein längeres Transaktions-ID-Fenster benötigt, wenden Sie sich an die Kundenunterstützung von Adobe.
* Mit einer abgelaufenen Transaktions-ID hochgeladene Datenquellen werden ähnlich wie Daten behandelt, die ohne Transaktions-ID hochgeladen wurden.
* Wenn dieselbe Variable sowohl im Online-Treffer als auch in der Transaktions-ID-Datenquelle enthalten ist, wird der Wert aus der Transaktions-ID-Datenquelle verwendet.
* Wenn eine Variable in einem Online-Treffer, aber nicht in einem übereinstimmenden Transaktions-ID-Datenquellentreffer enthalten ist, wird die Online-Treffervariable beibehalten.
* Wenn Sie dieselbe Transaktions-ID für mehrere Online-Treffer festlegen, wird nur das erste Vorkommen mit Daten aus einer übereinstimmenden Transaktions-ID-Datenquelle geändert.
* Wenn Sie dieselbe Transaktions-ID für mehrere Datenquellenzeilen für dieselben Dimensionen festlegen, wird das neueste Dimensionselement verwendet.

Zum Beispiel:

1. Sie senden eine Seitenansicht aus AppMeasurement, in der:
   * `eVar1` gleich `blue`
   * `eVar2` gleich `water`
   * `events` gleich `event1`
   * `transactionID` gleich `1256`
2. Nachdem der Treffer erfasst und verarbeitet wurde, laden Sie eine Transaktions-ID-Datenquelle hoch, in der:
   * `eVar1` gleich `yellow`
   * `eVar3` gleich `bird`
   * `events` gleich `event2`
   * `transactionID` gleich `1256`
3. Sobald der Treffer der Datenquellen verarbeitet wurde, wird ein Bericht im Arbeitsbereich angezeigt. Die Daten zeigen Folgendes:
   * `eVar1` gleich `yellow`
   * `eVar2` gleich `water`
   * `eVar3` gleich `bird`
   * `events` gleich `event2`

Der eVar1-Wert `blue` und `event1` Metriken sind nicht in Berichten enthalten, da der Transaktions-ID-Treffer diese jeweiligen Werte überschrieben hat.
