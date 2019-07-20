---
description: Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.
keywords: Instanzen
seo-description: Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.
seo-title: Instanzen
solution: Analytics
title: Instanzen
topic: Metriken
uuid: fec 94 bdd-a 1 dc -4 cb 0-8983-ea 775 b 69589 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Instanzen

Gibt an, wie oft ein Wert für eine Variable festgelegt wurde.

Instanzen werden für alle Hit-Typen gezählt, außer wenn ein Wert für eine Variable bei einem nachfolgenden Hit aufgrund der Persistenz aufgezeichnet wird.

Wenn ein Benutzer beispielsweise über [!DNL example.com] auf Ihre Site gelangt, enthält die erste Bildanforderung auf Ihrer Site den Referrer [!DNL example.com]. Wenn dieser Wert festgelegt wird, wird eine Instanz [!DNL example.com] zugeordnet, obwohl dieser Referrer für alle bei diesem Besuch angezeigten Seiten aufgezeichnet wird.

In Data Warehouse wurden Mitte 2011 Instanzen für Konversionsvariablen hinzugefügt, sodass Data Warehouse-Anforderungen eine bestimmte Konversionsvariableninstanz als Metrik behandeln können. Vor dem Zeitpunkt ihrer Einführung waren diese Metriken noch nicht für die Berichterstellung verfügbar.
