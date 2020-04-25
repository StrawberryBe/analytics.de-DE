---
description: Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.
keywords: instances
title: 'Instanzen '
topic: Metrics
uuid: fec94bdd-a1dc-4cb0-8983-ea575b69589f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Instanzen

Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.

Instanzen  werden für alle Hit-Typen gezählt, außer wenn ein Wert für eine Variable bei einem nachfolgenden Hit aufgrund der Persistenz aufgezeichnet wird.

Wenn ein Benutzer beispielsweise über [!DNL example.com] auf Ihre Site gelangt, enthält die erste Bildanforderung auf Ihrer Site den Referrer [!DNL example.com]. Wenn dieser Wert festgelegt wird, wird eine Instanz [!DNL example.com] zugeordnet, obwohl dieser Referrer für alle bei diesem Besuch angezeigten Seiten aufgezeichnet wird.

In Data Warehouse wurden Mitte 2011 Instanzen für Konversionsvariablen hinzugefügt, sodass Data Warehouse-Anforderungen eine bestimmte Konversionsvariableninstanz als Metrik behandeln können. Vor dem Zeitpunkt ihrer Einführung waren diese Metriken noch nicht für die Berichterstellung verfügbar.
