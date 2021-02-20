---
title: Trackingcode
description: Der Name des Trackingcodes oder der Kampagne.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 100%

---


# Trackingcode

In der Dimension „Trackingcode“ werden die Namen der Trackingcodes auf Ihrer Site aufgelistet. Diese Dimension wird in der Regel mithilfe von Abfragezeichenfolgenparametern erfasst. Sie können Links mit verschiedenen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren. Diese Dimension gibt an, welche Links am erfolgreichsten dazu beigetragen haben, den Traffic auf Ihre Site zu lenken.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v0` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Trackingcodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten.

## Dimension „Trackingcode“ mit Dimension „Marketing-Kanäle“ vergleichen, die Trackingcodes erfasst

Einige Benutzer, die Verarbeitungsregeln für Marketing-Kanäle einrichten, konfigurieren eine Regel, die alle in der Dimension „Trackingcode“ verwendeten Werte berücksichtigt. Obwohl es sich um eine hervorragende Praxis handelt, unterscheiden sie sich aufgrund der inhärenten Verarbeitungs- und Architekturunterschiede. Die folgende Liste erklärt, warum diese beiden Dimensionen, auch wenn sie auf einen Blick ähnlich sind, nicht miteinander verglichen werden können.

* **Vorherige Kanäle in Verarbeitungsregeln**: Verarbeitungsregeln für Marketing-Kanäle weiter oben in der Liste können verhindern, dass Treffer Ihrem Marketing-Kanal für Trackingcodes zugeordnet werden. Beispiel:

   1. Sie haben als erste Regel „Soziale Netzwerke“ und als zweite „Trackingcodes“ eingerichtet.
   2. Ein Benutzer stellt einen Link zu Ihrer Site mit einem Trackingcode auf einer Social-Media-Website ein, und mehrere seiner Freunde klicken auf diesen Link zu Ihrer Site.

   Da „Soziale Netzwerke“ die erste Verarbeitungsregel für Marketing-Kanäle ist, werden diese Benutzer dem Marketing-Kanal „Soziale Netzwerke“ und nicht Ihrem Marketing-Kanal für Trackingcodes zugeordnet.
* **Andere Marketing-Kanäle können die Zuordnung stehlen**: Wenn es sich um eine Standarddimension „Trackingcodes“ handelt, brauchen Sie sich keine Sorgen zu machen, dass andere Teile Ihrer Site die Attribution stehlen. Bei Marketing-Kanälen kann ein Benutzer jedoch eine andere Regel anwenden und eine andere Attribution vornehmen. Beispiel:
   1. Sie haben „Trackingcodes“ als ersten Kanal und „Direkt“ als zweiten.
   2. Ein Benutzer gelangt zunächst über einen Trackingcode zu Ihrer Site, verlässt dann jedoch die Site.
   3. Am nächsten Tag geben sie Ihre URL in ihre Adressleiste ein und tätigen dann einen Kauf.

   Der Marketing-Kanal „Trackingcodes“ würde für diesen Kauf keinen Letztkontakt-Gutschrift erhalten. Stattdessen würde er dem Marketing-Kanal „Direkt“ gutgeschrieben.
* **Unterschiede in der Gültigkeit**: Marketing-Kanäle haben einen rollierenden Besucherinteraktionsablauf von 30 Tagen, unabhängig davon, ob ein Kanal verwendet wurde oder nicht. Die Gültigkeit von Trackingcodes basiert auf dem Zeitpunkt, zu dem die Variable festgelegt wurde. Beispiel:
   1. Sie haben einen Besucherinteraktionsablauf von 30 Tagen und die Dimension „Trackingcode“ so konfiguriert, dass sie nach 30 Tagen abläuft.
   2. Ein Benutzer gelangt über einen Trackingcode zu Ihrer Site. Er durchsucht die Site und verlässt sie anschließend.
   3. Drei Wochen später kehrt er ohne Trackingcode oder Marketing-Kanal zurück und verlässt die Seite erneut.
   4. Zwei weitere Wochen später (fünf Wochen nach dem ersten Besuch) kehrt er ohne Trackingcode oder Marketing-Kanal zurück und tätigt dann einen Kauf.
   Der Benutzer tätigte letztendlich einen Kauf nach mehr 30 Tagen, war aber nie länger als 30 Tage inaktiv. Der Umsatz würde dem Marketing-Kanal „Trackingcodes“ zugeordnet, aber nicht der eigenständigen Dimension.
