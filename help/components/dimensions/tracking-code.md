---
title: Trackingcode
description: Der Name des Trackingcodes oder der Kampagne.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 17%

---


# Trackingcode

In der Dimension „Trackingcode“ werden die Namen der Trackingcodes auf Ihrer Site aufgelistet. Diese Dimension wird in der Regel mithilfe von Abfragezeichenfolgenparametern erfasst. Sie können Links mit verschiedenen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren. Diese Dimension gibt an, welche Links am erfolgreichsten dazu beigetragen haben, den Traffic auf Ihre Site zu lenken.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v0` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md)-Variable.

## Dimensionen

Zu den Elementen der Dimension gehören die Namen der Rückverfolgungscodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten.

## Vergleichen Sie die Dimension &quot;Rückverfolgungscode&quot;mit Marketing-Kanälen, die Rückverfolgungscodes erfassen

Einige Benutzer, die Verarbeitungsregeln für Marketing Kanal einrichten, konfigurieren eine Regel, die alle in der Dimension Rückverfolgungscode verwendeten Werte akzeptiert. Obwohl es sich um eine hervorragende Praxis handelt, unterscheiden sie sich aufgrund der inhärenten Verarbeitungs- und Architekturunterschiede. Die folgende Liste erklärt, warum diese beiden Dimensionen, auch wenn sie auf einen Blick ähnlich sind, nicht miteinander verglichen werden können.

* **Vorherige Kanal in Verarbeitungsregeln**: Marketing-Kanal, die die Verarbeitungsregeln höher in der Liste verarbeiten, können verhindern, dass Treffer Ihrem Tracking-Codes-Marketing-Kanal zugeordnet werden. Beispiel:

   1. Sie haben als erste Regel &quot;Social Networks&quot;und als zweite &quot;Trackingcodes&quot;eingerichtet.
   2. Ein Benutzer postet einen Link zu Ihrer Site, der einen Rückverfolgungscode auf einer Social Media-Site enthält, und mehrere Freunde klicken auf diesen Link zu Ihrer Site.

   Da &quot;Social Networks&quot;die erste Verarbeitungsregel für Marketingcodes ist, weisen diese Kanal dem Marketing-Kanal &quot;Social Networks&quot;und nicht Ihrem Marketing-Kanal für Rückverfolgungscodes zu.
* **Andere Marketing-Kanal können die Zuordnung** stehlen: Bei der Behandlung einer standardmäßigen Dimension &quot;Rückverfolgungscodes&quot;müssen Sie sich keine Gedanken über andere Teile Ihrer Site machen, die die Zuordnung von Rückverfolgungscodes stehlen. Bei Marketing-Kanälen kann ein Benutzer jedoch einer anderen Regel entsprechen und eine andere Zuordnung vornehmen. Beispiel:
   1. Sie haben &quot;Rückverfolgungscodes&quot;als ersten Kanal und &quot;Direkt&quot;als zweiten.
   2. Ein Benutzer gelangt zunächst über einen Rückverfolgungscode zu Ihrer Site, verlässt dann jedoch die Site.
   3. Am nächsten Tag geben sie Ihre URL in ihre Adressleiste ein und tätigen dann einen Kauf.

   Der Marketing-Kanal der Rückverfolgungscodes erhält keine Last Touch-Gutschrift für diesen Kauf. Stattdessen würde sie an den &quot;Direct&quot;-Marketing-Kanal weitergeleitet.
* **Ablaufunterschiede**: Marketing-Kanal haben einen rollierenden 30-Tage-Besucher-Interaktionsablauf, unabhängig davon, ob ein Kanal berührt wurde oder nicht. Rückverfolgungscodes haben einen Ablauf, der auf dem Zeitpunkt basiert, zu dem die Variable festgelegt wurde. Beispiel:
   1. Sie haben einen Besucher-Interaktionsablauf von 30 Tagen und konfiguriert, dass die Dimension &quot;Rückverfolgungscode&quot;nach 30 Tagen abläuft.
   2. Ein Benutzer gelangt über einen Rückverfolgungscode zu Ihrer Site. Sie durchsuchen die Site und gehen dann.
   3. Drei Wochen später kehren sie ohne Rückverfolgungscode oder Marketing-Kanal zurück und gehen dann wieder weg.
   4. Zwei weitere Wochen später (fünf Wochen nach dem ersten Besuch) kehren sie ohne Rückverfolgungscode oder Marketing-Kanal zurück und tätigen dann einen Kauf.
   Der Benutzer tätigte schließlich einen Kauf nach 30 Tagen, war aber nie länger als 30 Tage inaktiv. Der Umsatz, der dem Marketing-Kanal für Rückverfolgungscodes zugeordnet ist, wird Ihnen zwar angezeigt, jedoch nicht für die eigenständige Dimension.
