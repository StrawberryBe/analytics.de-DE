---
description: Mit „Bot-Regeln“ können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. Durch das Ausblenden des Bot-Traffics kann die Benutzeraktivität auf Ihrer Website genauer gemessen werden.
title: Verstehen und Konfigurieren von Bot-Regeln
feature: Bot Removal
role: Admin
exl-id: 1c0009f6-2746-4ef1-8dcb-e2693617e91e
source-git-commit: b5cca97861216751c5feae23e3c0121fa9c356b1
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 69%

---

# Verstehen und Konfigurieren von Bot-Regeln

Mit Bot-Regeln können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots generiert wird. Durch das Ausblenden des Bot-Traffics kann die Benutzeraktivität auf Ihrer Website genauer gemessen werden.

Nach der Definition von Bot-Regeln wird aller eingehender Traffic mit den definierten Regeln abgeglichen. Traffic, der mit einer dieser Regeln übereinstimmt, wird nicht in der Report Suite erfasst und ist nicht in Traffic-Metriken enthalten.

Mit der Entfernung von Bot-Traffic werden das Traffic-Volumen und die Konversionsmetriken vermindert. Viele Kunden stellen fest, dass die Entfernung von Bot-Traffic zu höheren Konversionsraten und zu höheren anderen Benutzerfreundlichkeitsmetriken führt.

Bot-Traffic-Daten werden in einem separaten Repository zur Anzeige in den Berichten &quot;Bots&quot;und &quot;Bot Pages&quot;gespeichert.

>[!NOTE]
>
>Adobe Experience Edge bietet eine [Bot-Erkennungsdienst](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html?lang=de) die Treffer, die als von Bots identifiziert wurden. Der Bot-Erkennungsvorgang von Adobe Analytics unterscheidet sich davon und verweist nicht auf den Bot-Wert, der in Daten enthalten ist, die über Experience Edge eingehen. Die beiden Systeme verwenden dieselbe IAB-Bot-Liste, daher sollten sie sich in dieser Hinsicht identisch verhalten.

## Aktualisieren oder Hochladen von Bot-Regeln

>[!IMPORTANT]
>
>Bevor Sie den Bot-Traffic entfernen, machen Sie Stakeholder darauf aufmerksam, damit diese die im Zuge der Änderung notwendigen Anpassungen an wichtige Kennzahlen vornehmen können. Wenn möglich, empfehlen wir, zunächst den Bot-Traffic aus einer kleinen Report Suite zu entfernen, um die potenziellen Auswirkungen abschätzen zu können.

Das folgende Video zeigt, wie Bot-Regeln konfiguriert werden:

>[!VIDEO](https://video.tv.adobe.com/v/335738/?quality=12)

So aktualisieren oder laden Sie Bot-Regeln hoch:

1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, in der Sie Bot-Regeln aktualisieren möchten, und wählen Sie dann **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Bot Rules]**.

1. Verwenden Sie eine der folgenden Optionen, um Bot-Regeln für die Report Suite zu aktualisieren oder hochzuladen:

   * Auswählen [!UICONTROL **IAB Bot-Filterungsregeln aktivieren**] Entfernen von Bots in der Liste &quot;International Spiders &amp; Bots List&quot;von IAB (International Advertising Bureau), um Bot-Traffic zu entfernen.

     Es wird empfohlen, diese Option mindestens auszuwählen.

     Weitere Informationen finden Sie im folgenden Abschnitt: [IAB-Standardregeln](#standard-iab-bot-rules).

   * Auswählen [!UICONTROL **Regel hinzufügen**] , um benutzerspezifische Bot-Regeln zu definieren und hinzuzufügen, die auf Benutzeragenten, IP-Adressen oder IP-Bereichen basieren.

     Weitere Informationen finden Sie im folgenden Abschnitt: [Benutzerdefinierte Bot-Regeln](#custom-bot-rules).

   * Neben dem [!UICONTROL **CSV Bot-Datei zum Importieren auswählen**] Bereich, auswählen [!UICONTROL **Datei auswählen**] und wählen Sie dann die CSV-Datei aus, die die Bot-Regeln definiert.

     Weitere Informationen finden Sie im folgenden Abschnitt: [Hochladen von Bot-Regeln](#upload-bot-rules).

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Standard-IAB-Bot-Regeln

Standard-IAB-Bot-Regeln können aktiviert werden, indem Sie das Kontrollkästchen [!UICONTROL IAB Bot-Filterungsregeln aktivieren] aktivieren. Diese Auswahl entfernt Bots in der Liste „International Spiders &amp; Bots List“ von IAB (International Advertising Bureau), um Bot-Traffic zu entfernen. Adobe aktualisiert diese Liste von IAB monatlich.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-iab-checkbox.png)

Adobe kann die detaillierte IAB-Bot-Liste nicht an Kunden weitergeben, aber Sie können den Bericht „Bots“ verwenden, um eine Liste der Bots anzuzeigen, die auf Ihre Website zugegriffen haben. Um einen Bot an die IAB-Liste zu senden, gehen Sie zu [IAB](https://www.iab.com).

Informationen zum Aktivieren standardmäßiger IAB-Bot-Regeln in einer Report Suite finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

## Benutzerdefinierte Bot-Regeln

>[!NOTE]
>
>: In der Benutzeroberfläche können 500 Regeln manuell definiert werden. Wenn diese Grenze erreicht wurde, müssen Regeln über die Optionen „Datei importieren“ und „Bot-Regeln exportieren“ stapelweise verwaltet werden.

Mit benutzerspezifischen Bot-Regeln können Sie Traffic-basierte Bedingungen filtern, die Sie definieren. Informationen zum Starten der Aktivierung benutzerdefinierter Bot-Regeln in einer Report Suite finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

Benutzerspezifische Bot-Regeln werden mithilfe der folgenden Bedingungstypen definiert:

* Benutzeragent
* IP-Adresse
* IP-Bereich

Für eine einzige Regel können mehrere Bedingungen definiert werden. Mehrere Bedingungen werden mithilfe des „oder“-Befehls zugewiesen. Wenn Sie beispielsweise einen Wert für Benutzeragent und IP-Adresse bereitstellen, wird der Traffic als Bot-Traffic gewertet, wenn eine dieser beiden Bedingungen erfüllt ist.

### Benutzeragent

Eine Benutzeragent-Bedingung prüft den Benutzeragentenwert, um zu sehen, ob dieser mit der angegebenen Zeichenfolge **[!UICONTROL beginnt]** oder diese **[!UICONTROL enthält]**. Wenn **[!UICONTROL enthält]** ausgewählt wurde, wird die Unter-Zeichenfolge zugewiesen, wenn sie an einer beliebigen Stelle im Benutzeragenten auftaucht.

Optionale Werte können in die Liste **[!UICONTROL enthält nicht]** aufgenommen werden, um Werte zu definieren, die der Benutzeragent für eine erfolgreiche Übereinstimmung nicht enthalten darf. Sie können mehrere Werte spezifizieren, indem Sie einen Wert pro Zeile aufnehmen. Wenn der Benutzeragent die in der Übereinstimmungszeichenfolge spezifizierten Kriterien erfüllt, aber auch eine Zeichenfolge enthält, die auf der „enthält nicht“-Liste steht, wird er nicht als Übereinstimmung gewertet.

Das Feld **[!UICONTROL enthält]** ist auf 100 Zeichen begrenzt. Die „enthält nicht“-Liste ist auf 255 Zeichen abzüglich eines Trennzeichens für jede neue Zeile begrenzt. (Dies entspricht der Anzahl der Zeichenfolgen – 1. Wenn Sie vier *enthält nicht*-Zeichenfolgen spezifizieren, werden drei Trennzeichen benötigt.) Bei allen Zeichenfolgen-Übereinstimmungen wird zwischen Groß- und Kleinschreibung unterschieden.

### IP-Adresse (inklusive Wildcard-Übereinstimmungen)

Weist eine oder mehrere IP-Adressen im selben Block mithilfe von Wildcards (&#42;) zu. Geben Sie die numerischen Werte der IP-Adresse an, für die Sie eine Übereinstimmung suchen. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch eine Wildcard (&#42;). Die folgende Liste enthält Beispiele der IP-Adressen-Übereinstimmungszeichenfolge:

```
10.10.10.1
10.10.10.*
```

### IP-Adressbereich

Geben Sie die Start- und Endbereiche der zuzuweisenden IP-Adressen an. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch eine Wildcard (&#42;).

### Definieren einer benutzerdefinierten Bot-Regel

1. Wechseln Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]**, wählen Sie eine oder mehrere Report Suites aus und klicken Sie auf **[!UICONTROL Allgemein]** > **[!UICONTROL Bot-Regeln]**.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und definieren Sie eine oder mehrere Übereinstimmungsbedingungen.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Die Änderung sollte binnen 30 Minuten in Kraft treten.

## Hochladen von Bot-Regeln

Für einen Massenimport von Bot-Regeln können Sie eine CSV-Datei hochladen, in der die Regeln definiert sind.

1. Informationen zum Starten des Hochladens von Bot-Regeln in eine Report Suite finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

1. Erstellen Sie eine CSV-Datei mit den folgenden Spalten in Zeile 1 des Arbeitsblatts und in der angegebenen Reihenfolge:

   | Spalte 1, Zeile 1 | Spalte 2, Zeile 1 | Spalte 3, Zeile 1 | Spalte 4, Zeile 1 | Spalte 5, Zeile 1 | Spalte 6, Zeile 1 |
   |--- |--- |---|---|---|---|
   | Bot-Name | IP-Beginn | IP-Ende | Regel<br>(enthält oder beginnt mit)</br> | Benutzeragent - enthalten | Benutzeragent ausschließen<br>(Längenbeschränkung von 255 Zeichen)</br> |

   Sie können drei Arten von Bot-Regeln definieren:

   * Benutzeragent enthält oder beginnt mit
   * Einzelne IP-Adresse oder Wildcard-Übereinstimmung
   * IP-Bereichsübereinstimmung

   Jede Zeile in der Importdatei kann nur eine der folgenden Bot-Definitionen enthalten:

   >[!NOTE]
   >
   >   Um eine Übereinstimmung für einen Bot mithilfe einer OR-Kombination aus Regeln zu finden (z. B. Benutzeragent ODER IP-Adresse), geben Sie einen identischen Namen für alle Regeln an, die Sie in dem Bot-Namensfeld kombinieren möchten. AND-Übereinstimmungen werden nicht unterstützt.


   * **Benutzeragent enthält oder beginnt mit:** Geben Sie eine einzige Benutzeragent-Zeichenfolge zur Übereinstimmung in der Spalte „Agent einschließlich“ ein. Legen Sie den gewünschten Übereinstimmungstyp fest, indem Sie im Feld zur Agent-Übereinstimmungsregel den Vermerk *enthält* oder *beginnt mit* platzieren. Ein optionaler Wert kann in die Spalte „Agent ausschließlich“ aufgenommen werden, der eine oder mehrere längsstrichgetrennte (`|`) Zeichenketten definiert, die der Agent nicht enthalten darf. Bei Zeichenfolgen-Übereinstimmungen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Sowohl die Spalte „IP-Start“ als auch „IP-Ende“ müssen leer sein.

   * **Einzelne IP-Adresse oder Wildcard-Übereinstimmung**: Um eine Übereinstimmung mit einer einzelnen IP-Adresse (`10.10.10.1`) oder einer Platzhalter-IP-Adresse (`10.10.*.*`) herzustellen, platzieren Sie denselben Wert in den Spalten „IP-Start“ und „IP-Ende“. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

   * **IP-Bereichs-Übereinstimmung**: Definieren Sie einen Bereich von IP-Adressen mithilfe der Spalten „IP-Start“ und „IP-Ende“. Sie können Platzhalter nutzen, um Übereinstimmungen für IP-Bereiche zu finden, z. B. `10.10.10.*` bis `10.10.20.*`. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

1. Auf der Seite &quot;Bot Rules&quot;im Report Suite Manager neben dem [!UICONTROL **CSV Bot-Datei zum Importieren auswählen**] Bereich, auswählen [!UICONTROL **Datei auswählen**] und wählen Sie dann die CSV-Datei aus, die die zu importierenden Bot-Regeln definiert.

1. (Optional) Wählen Sie die **[!UICONTROL Vorhandene Regeln überschreiben]** aktivieren, um alle vorhandenen Regeln zu löschen und sie durch die in der Upload-Datei definierten Regeln zu ersetzen.

1. Auswählen [!UICONTROL **Importdatei**].

1. Im [!UICONTROL **Regelsätze**] überprüfen Sie die importierten Regeln.

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Exportieren von Bot-Regeln

So exportieren Sie alle in der Benutzeroberfläche definierten Regeln in ein CSV-Format:

1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die die zu exportierenden Bot-Regeln enthält, und wählen Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Bot Rules]**.

1. Auswählen **[!UICONTROL Bot-Regeln exportieren]**, speichern Sie die CSV-Datei dann in Ihrem Dateisystem.

## Auswirkung von Bot-Regeln auf die Datenerfassung {#section_F01A3130E7A04A9993371CF26F6586F2}

Bot-Regeln gelten für alle Analysedaten. Mithilfe von Bot-Regeln entfernte Daten sind nur in den Berichten „Bots“ und „Bot-Seiten“ sichtbar.

VISTA-Regeln werden nach Bot-Regeln angewendet. Weitere Informationen finden Sie im Technote-Benutzerhandbuch unter [Verarbeitungsreihenfolge](/help/technotes/processing-order.md).

**Verarbeitung von Besuchen mit hoher Hit-Zahl:** Wenn mehr als 100 Hits in einem Besuch auftreten, wird bei der Berichterstellung ermittelt, ob der Zeitraum des Besuchs (in Sekunden) kleiner oder gleich der Anzahl der Hits bei diesem Besuch ist. In dieser Situation beginnt die Berichterstellung mit dem nächsten Besuch neu, da die Verarbeitung langer, intensiver Besuche hohe Kosten verursacht. Besuche mit hoher Hit-Zahl werden in der Regel durch Bot-Angriffe verursacht und gelten nicht als normales Browsen von Besuchern.

>[!NOTE]
>
>Treffer, die als *`bots`* markiert sind, werden als [Server-Aufrufe](/help/admin/admin/c-server-call-usage/overage-overview.md) in Rechnung gestellt.

## Auswirkung der IP-Verschleierung auf die Bot-Filterung {#section_92E60B95BE8940D983F28C79E0CD6B12}

Die IAB-Bot-Liste basiert lediglich auf dem Benutzeragenten, so dass das Filtern auf der Basis dieser Liste nicht durch die IP-Verschleierungseinstellungen beeinträchtigt wird. Bei Nicht-IAB-Bot-Filterung (benutzerdefinierte Regeln) kann die IP Bestandteil der Filterkriterien sein. Beim Filtern von Bots mithilfe von IP erfolgt die Bot-Filterung nach Entfernung des letzten Oktetts, sofern diese Einstellung aktiviert ist, jedoch vor den anderen IP-Verschleierungseinstellungen wie z. B. dem Löschen der gesamten IP oder dem Austausch durch eine eindeutige ID.

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten aktualisiert werden, sodass sie IP-Adressen mit einer Null am Ende berücksichtigen. Übereinstimmende &#42; sollten 0 entsprechen.
