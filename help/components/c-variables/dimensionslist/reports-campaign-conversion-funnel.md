---
description: Zeigt Mittelwerte für die Metriken in der Berichterstellungsgruppe an. Standardmetriken sind Clickthroughs, Gesamtverkäufe, Bestellungen und Umsatz.
seo-description: Zeigt Mittelwerte für die Metriken in der Berichterstellungsgruppe an. Standardmetriken sind Clickthroughs, Gesamtverkäufe, Bestellungen und Umsatz.
seo-title: Kampagnenkonversionstrichter
solution: Analytics
title: Kampagnenkonversionstrichter
topic: 'Berichte    '
uuid: b 0 a 90917-e 4 c 7-40 da -854 e -58649 de 09742
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kampagnenkonversionstrichter

Zeigt Mittelwerte für die Metriken in der Berichterstellungsgruppe an. Standardmetriken sind Clickthroughs, Gesamtverkäufe, Bestellungen und Umsatz.

**[!UICONTROL Kampagnen]** &gt; **[!UICONTROL Kampagnenkonversionstrichter]**

Im oberen Bereich einer Trichtergrafik werden Konversionsdaten angezeigt. Im unteren Bereich werden basierend auf Bestellungen Statistiken für alle Ereignisse im oberen Bereich sowie bis zu zwei weitere Metriken, Umsatz und Einheiten, angezeigt.

Beachten Sie beim Interpretieren der Konversionstrichterdaten folgende Informationen:

* Statistiken für die aktuellen Zeiträume können bei der Anzeige von Daten ggf. nicht abgeschlossen werden, wodurch Trends von einem Vortag auf den aktuellen Tag bezogen beeinträchtigt werden können.
* Wenn kein Filter auf den Trichter angewendet wird, entspricht die Besuchemetrik Konversionsbesuchen oder Besuchen, während denen die Kampagnenvariable, eine eVar-Variable oder ein Erfolgsereignis ausgelöst wurde. In dieser Summe sind Besuche, bei denen keine dieser Eigenschaften an die Berichte weitergereicht wurde, nicht enthalten.
* Wenn ein Filter auf einen Trichter angewendet wird, entspricht die Besuchemetrik Instanzen (oder Clickthrough-Raten). Dieser Wert entspricht der Gesamthäufigkeit der Population einer gegebenen Variable durch Benutzer auf Ihrer Seite; hiervon ausgenommen sind Instanzen, die nicht die Filteranforderungen erfüllen. Ein einzelner Besuch kann mehrere Instanzen aufweisen.
* Möglicherweise melden tiefere Ebenen des Trichters höhere Zahlen als weniger tiefe Ebenen. Beispielsweise sehen Sie möglicherweise mehr Bestellungen als Clickthroughs oder mehr Checkouts als Produktansichten. Dafür kann es mehrere Gründe geben:

   * Sie haben mehr Bestellungen als Clickthrough-Raten, wenn die Trackingcode-Variable auf ein langes Ablaufdatum von Cookies eingestellt wird (zum Beispiel ein Monat) und Benutzer nur eine Clickthrough-Rate durchführen, aber wiederholt auf Ihre Seite zurückkehren und während des Zeitraums Bestellungen aufgeben, bevor der Trackingcode-Wert abläuft.
   * Sie erhalten mehr Checkouts als Produktansichten, wenn der Benutzer die Produktansichtsseite überspringen kann (was im Falle einer Upsell-Seite möglich ist) oder falls er den Warenkorb speichern kann und später zurückkehrt, um die Bestellung abzuschließen. Wenn die Produktansicht vor dem ausgewählten Datumsbereich auftritt und der Checkout danach erfolgt, wird ein Checkout aber keine Produktansicht angezeigt. Eine solche Abweichung deutet nicht auf ein Problem bei der Berichterstellung oder einen Fehler bei der Implementierung hin. Anhand dieser Daten können Sie erkennen, wie Benutzer mit Ihrer Site interagieren, selbst wenn dies vom erwarteten Verhalten des Trichters abweicht.

