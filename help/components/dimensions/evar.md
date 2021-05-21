---
title: eVar
description: Eine benutzerdefinierte Dimension, die Sie in Berichte verwenden können.
exl-id: ce7cc999-281d-4c52-b64d-d44cc320ab2d
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '788'
ht-degree: 100%

---

# eVar

*Auf dieser Hilfeseite wird beschrieben, wie eVars als Dimension funktionieren. Weitere Informationen zur Implementierung von eVars finden Sie unter [eVars](/help/implement/vars/page-vars/evar.md) im Implementierungs-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsdesigndokument](/help/implement/prepare/solution-design.md) verfügen, werden die meisten für Ihr Unternehmen spezifischen Dimensionen als eVars angezeigt. Standardmäßig bleiben eVars über den Treffer hinaus bestehen, auf den sie gesetzt wurden. Sie können ihre Gültigkeit und Zuordnung unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen anpassen.

Die Anzahl der verfügbaren eVars hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 250 eVars verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

Bei eVars muss nicht auf die Groß- und Kleinschreibung geachtet werden. Wenn Sie denselben Wert mit verschiedenen Groß- und Kleinschreibungen senden (z. B. `"DOG"` und `"Dog"`), gruppiert Analysis Workspace ihn in demselben Dimensionselement. Es wird die erste Groß- und Kleinschreibung verwendet, die zu Beginn des Berichtsmonats vorkam. Data Warehouse zeigt den ersten aufgefundenen Wert innerhalb des Anforderungszeitraums an.

## Füllen von eVars mit Daten

Jede eVar erfasst Daten aus der [`v1` – `v250`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `v1` Daten für eVar1, während der Abfragezeichenfolgenparameter `v222` Daten für eVar222 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `eVar1` – `eVar250`. Die Implementierungsrichtlinien finden Sie unter [eVar](/help/implement/vars/page-vars/evar.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da eVars benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede eVar gelten. Vergewissern Sie sich, dass Sie den Zweck jeder eVar und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

## Funktionsweise von eVars

Wenn Sie Daten an Adobe Analytics senden, übersetzen die Datenerfassungs-Server den Treffer in eine Datenzeile mit Hunderten von Spalten. Für jede eVar sind zwei Spalten vorgesehen: eine für die direkte Datenerfassung und die andere für persistente Werte.

* Eine Standardspalte enthält Daten, die von der Bildanforderung an Adobe gesendet werden.
* Eine Spalte „Post“ enthält persistente Daten, die von der Gültigkeit und Zuordnung der eVar abhängen.

Die Spalte `post_evar` wird fast immer in Berichten verwendet.

### Verknüpfung von eVars mit Metriken

Erfolgsereignisse und eVars werden häufig in verschiedenen Bildanforderungen definiert. In der Spalte `post_evar` können eVar-Werte mit Ereignissen verknüpft werden, sodass Daten in Berichten angezeigt werden. Nehmen Sie zum Beispiel den folgenden Besuch:

1. Ein Besucher erreicht Ihre Site auf Ihrer Startseite.
2. Sie suchen mithilfe der internen Suche Ihrer Site nach „cats“. Ihre Implementierung verwendet eVar1 für die interne Suche.
3. Sie sehen sich ein Produkt an und schließen den Checkout-Prozess ab.

Eine vereinfachte Version der Rohdaten würde wie folgt aussehen:

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` |  |  |  |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` |  | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` |  | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` |  | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` |  | `cats` | `purchase` |

* Die Spalte `visitor_id` verknüpft Treffer mit demselben Besucher. In den eigentlichen Rohdaten bestimmen die verketteten Werte von `visid_high` und `visid_low` Besucher-ID.
* Die Spalte `pagename` füllt die Dimension „Seiten“.
* Die Spalte `evar` bestimmt die Treffer, bei denen eVar1 explizit gesetzt wurde.
* `post_evar1` beinhaltet den vorherigen Wert, abhängig von der Zuordnung und Gültigkeit der Variablen in den Report Suite-Einstellungen.
* Die Spalte `event_list` enthält alle Metrikdaten. In diesem Beispiel ist `event1` „Suchen“. Die anderen Ereignissen sind standardmäßige Warenkorbmetriken. In den eigentlichen Rohdaten enthält `event_list` einen kommagetrennten Satz von Zahlen mit einer Zuordnungstabelle, die diese Zahlen mit einer Metrik verknüpft.

### Übersetzen der Datenerfassung in Berichte

Die Tools in Adobe Analytics wie Analysis Workspace verarbeiten diese erfassten Daten. Wenn Sie z. B. einen Bericht mit eVar1 als Dimension und Bestellungen als Metrik abrufen, wird ein Bericht ähnlich dem folgenden angezeigt:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace ruft diesen Bericht mit der folgenden Logik ab:

* Sehen Sie sich alle `event_list`-Werte an und wählen Sie alle Treffer aus, die `purchase` enthalten.
* Zeigen Sie von diesen Treffern den `post_evar1`-Wert an.

### Bedeutung von Zuordnung und Gültigkeit

Da Zuordnung und Gültigkeit bestimmen, welche Werte beibehalten werden, sind sie von entscheidender Bedeutung, um den größtmöglichen Nutzen aus einer Analyseimplementierung zu ziehen. Adobe empfiehlt dringend, dass Sie innerhalb Ihres Unternehmens besprechen, wie mehrere Werte für jedes eVar behandelt werden (Zuordnung) und wann eVars keine Daten mehr speichern (Gültigkeit).

* Standardmäßig verwendet ein eVar die letzte Zuordnung. Neue Werte überschreiben persistente Werte.
* Standardmäßig verwendet eine eVar eine Gültigkeit des Besuchs. Sobald ein Besuch endet, werden die Werte nicht mehr von Zeile zu Zeile in der Spalte `post_evar` kopiert.

Sie können die Gültigkeit und Zuordnung von eVars unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen ändern.

## Wert von eVars gegenüber Props

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Dies stützt sich auf Folgendes:

* eVars sind in Berichten auf 255 Byte begrenzt. Props sind auf 100 Byte begrenzt.
* Props bleiben standardmäßig nicht über den festgelegten Treffer hinaus erhalten. eVars haben eine benutzerdefinierte Gültigkeit, mit der Sie feststellen können, wann einer eVar ein nachfolgendes Ereignis nicht mehr gutgeschrieben wird. Wenn Sie jedoch die [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md) verwenden, können sowohl Props als auch eVars ein benutzerdefiniertes Zuordnungsmodell verwenden.
* Adobe unterstützt bis zu 250 eVars und nur 75 Props.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [Prop](prop.md).
