---
description: Wenn ein Bericht eine große Anzahl eindeutiger Werte aufweist, kann mit Adobe nun sichergestellt werden, dass die wichtigsten Werte in Ihrem Bericht auftauchen.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: Metriken
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: 65190776da25437e854e0226cd349e3ba13fc8c9
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 52%

---

# Wert „Geringer Datenverkehr“ in Adobe Analytics

Wenn ein Bericht viele eindeutige Werte aufweist, stellt Adobe Funktionen bereit, mit denen sichergestellt wird, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden. Eindeutige Variablenwerte, die nach etwa 500.000 vorhandenen Werten gesammelt wurden, werden unter einem Zeileneintrag mit dem Titel **[!UICONTROL Geringer Traffic]** aufgeführt.

## Funktionsweise von [!UICONTROL Geringer Traffic]

* Das Reporting ist nicht betroffen, wenn die Variable in einem bestimmten Monat nicht 500.000 eindeutige Werte erreicht.
* Wenn eine Variable diesen ersten Schwellenwert von 500.000 erreicht, werden die Daten unter „Geringer Datenverkehr“ erfasst. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten angezeigt wird, fügen Sie ihn wie gewohnt hinzu.
   * Wenn ein Wert noch nicht in Berichten angezeigt wird, wird er im Zeileneintrag [!UICONTROL Geringer Traffic] angezeigt. Wenn ein Wert, der im Zeileneintrag [!UICONTROL Geringer Traffic] enthalten ist, innerhalb kurzer Zeit sehr häufig angezeigt wird, wird er als eigener Zeileneintrag erkannt. Die beträchtliche Anzahl der zu sehenden Elemente weist viele Abhängigkeiten auf, z. B. die Anzahl der Verarbeitungsserver und Daemonen, die Daten für diese Report Suite verarbeiten.
* Wenn eine Report Suite mehr als 1.000.000 eindeutige Werte erreicht, wird eine aggressivere Filterung angewendet:
   * Wenn ein Wert bereits in Berichten angezeigt wird, fügen Sie ihn wie gewohnt hinzu.
   * Wenn ein Wert noch nicht in Berichten angezeigt wird, wird er im Zeileneintrag [!UICONTROL Geringer Traffic] angezeigt. Wenn ein Wert, der im Zeileneintrag [!UICONTROL Geringer Traffic] enthalten ist, innerhalb kurzer Zeit sehr häufig angezeigt wird, wird er als eigener Zeileneintrag erkannt. Die beträchtliche Anzahl der zu sehenden Elemente weist viele Abhängigkeiten auf, z. B. die Anzahl der Verarbeitungsserver und Daemonen, die Daten für diese Report Suite verarbeiten.

Warum verschiebt Adobe ein Element aus dem Zeileneintrag [!UICONTROL Geringer Traffic] in einen eigenen Zeileneintrag? Beispielsweise erkennt dieser Schritt möglicherweise eine beliebte neue Seite oder ein neues Element, das später im Monat hinzugefügt wurde (nachdem eindeutige Werte überschritten wurden) und das viele Treffer/Ansichten erhält. Die Verschiebung soll nicht alle Elemente erfassen, die eine bestimmte Anzahl von Treffern/Ansichten pro Tag oder Monat erhalten.

## Ändern der Schwellenwerte für eindeutige Werte

Die Schwellenwerte liegen standardmäßig bei 500.000 und einer Million eindeutigen Werten. Diese Beschränkungen können variablenweise geändert werden. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um diese Änderung anzufordern. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert erhöhen möchten
* Sowohl den ersten als auch den zweiten gewünschten Schwellenwert

Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen achtsam vorzugehen.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Bitten Sie einen unterstützten Anwender Ihres Unternehmens, sich an die Adobe-Kundenunterstützung zu wenden, wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## „Geringer Datenverkehr“ mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **Data Warehouse:** Die Anzahl der eindeutigen Werte in Data-Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht das Reporting beliebig vieler eindeutiger Werte.
   * In einigen eingeschränkten Szenarien können weiterhin „Geringer Datenverkehr“-Werte angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl eindeutiger Werte enthalten, werden unter „Geringer Datenverkehr“ erfasste Werte nicht berücksichtigt.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Classification unter „Geringer Datenverkehr“ fällt, wird der Wert nicht klassifiziert.
   * Klassifizierungswerte für geringen Traffic, die über den Importer bezogen wurden, können in Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * Klassifizierungswerte für geringen Traffic, die über den Regelaufbau erhalten wurden, *können nicht* in Data Warehouse angezeigt werden. <!-- AN-122872 -->
