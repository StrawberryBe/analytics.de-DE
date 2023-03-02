---
source-git-commit: fb9be2d52ebe02603a7255b0ff6d5a7c2efdeed7
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 84%

---
# Snippets

## Mitteilung zum Ende der Nutzungsdauer von Reports &amp; Analytics {#ra-eol}

>[!IMPORTANT]
>
>Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://express.adobe.com/page/6WnF8JK6IRDhf/) von Reports &amp; Analytics.

## Filterkriterien für Datenwörterbuch {#dd-filter-criteria}

1. (Optional) Wählen Sie das Symbol **Filter** ![Datenwörterbuchfilter-Symbol](/help/analyze/analysis-workspace/components/data-dictionary/assets/data-dictionary-filter-icon.png) und wählen Sie dann eine der folgenden Filteroptionen, um die Liste der Komponenten zu filtern:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Genehmigt**] | Nur Komponenten anzeigen, die von Admins als genehmigt markiert wurden. |
   | [!UICONTROL **Favoriten**] | Nur Komponenten anzeigen, die sich in Ihrer Favoritenliste befinden. Informationen zum Hinzufügen von Komponenten zur Favoritenliste finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensionen**] | Nur Komponenten anzeigen, die Dimensionen sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Metriken**] | Nur Komponenten anzeigen, die Metriken sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Segmente**] | Nur Komponenten anzeigen, die Segmente sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) <!--this is Filters in CJA--> |
   | [!UICONTROL **Datumsbereiche**] | Zeigt nur Komponenten an, die Datumsbereiche sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Alle anzeigen**] | Alle Komponenten anzeigen. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Nicht genehmigt**] | Nur Komponenten anzeigen, die noch nicht von einem Administrator als genehmigt gekennzeichnet wurden. Als Administrator ist dies hilfreich, wenn Sie Komponenten identifizieren, die Ihre Überprüfung und Genehmigung erfordern. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Fehlende Beschreibung**] | Nur Komponenten anzeigen, die noch keine Beschreibung im Feld „Beschreibung“ haben. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Duplikate anzeigen**] | Nur Komponenten anzeigen, die dieselbe Kennzeichnung oder dieselbe Beschreibung wie in einer anderen Komponente in der ausgewählten Report Suite aufweisen. Dazu gehören Komponenten, die Sie erstellen, sowie Komponenten, die von Adobe bereitgestellt werden. Kennzeichnungen oder Beschreibungen müssen exakt übereinstimmen, damit sie als Duplikate angezeigt werden. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Keine aktuellen Daten**] | Nur Komponenten anzeigen, die in den letzten 90 Tagen keine Daten erfasst haben. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Erstellt von Adobe**] <!-- I don't see this option--> | Nur Komponenten anzeigen, die von Adobe erstellt wurden. Komponenten, die von Admins oder anderen Benutzenden in deren Organisation erstellt wurden, werden nicht angezeigt. |

   {style=&quot;table-layout:auto&quot;}

## Komponenteninformationen für Datenwörterbuch {#dd-component-information}

| Option | Funktion |
|---------|----------|
| [!UICONTROL **Genehmigt**] | <p>Zeigt an, dass die Komponente vom Admins geprüft und genehmigt wurde.</p><p>Administratoren erhalten eine Option zum [!UICONTROL **Nicht genehmigen**]. Wenn Sie diese Option auswählen, wird die Komponente für Benutzer als &quot;Nicht genehmigt&quot;gekennzeichnet.</p> |
| [!UICONTROL **Nicht genehmigt**] | <p>Gibt an, dass die Komponente noch nicht vom Administrator überprüft und genehmigt wurde.</p><p>Administratoren erhalten eine Option zum [!UICONTROL **Genehmigen**]. Wenn Sie diese Option auswählen, wird die Komponente Benutzern als &quot;Genehmigt&quot;gekennzeichnet.</p> |
| [!UICONTROL **Beschreibung**] | Beschreibt die beabsichtigte Funktion der Komponente. (Diese Informationen werden vom Analytics-Admins hinzugefügt, wie unter [Komponentenbeschreibungen hinzufügen](/help/analyze/analysis-workspace/components/add-component-descriptions.md) beschrieben.) |
| [!UICONTROL **Häufig verwendet mit**] | <p>Zeigt Komponenten an, die am häufigsten mit der Komponente verwendet werden, die Sie anzeigen.</p><p>Es werden bis zu 5 Komponenten für die 5 primären Komponententypen angezeigt: Metrik, Berechnete Metrik, Dimension, Segment und Datumsbereich.</p><p>Diese Liste basiert auf Daten aus den letzten 90 Tagen. Es werden nur Komponenten angezeigt, auf die Sie Zugriff haben. <!--Add info about how users with administrator access can control these after the feature is available. How?--></p> |
| [!UICONTROL **Ähnlich wie**] | <p>Zeigt Komponenten mit ähnlichen Kennzeichnungen wie die angezeigte Komponente an.</p><p>Es werden bis zu 5 Komponenten für die 5 primären Komponententypen angezeigt: Metrik, Berechnete Metrik, Dimension, Segment und Datumsbereich.</p><p>Es werden nur Komponenten angezeigt, auf die Sie Zugriff haben.</p><p>Hier werden alle doppelten Komponenten in Ihrer Report Suite angezeigt. Analytik-Admins sollten alle doppelten Komponenten identifizieren und entfernen, wie in [Überwachung des Zustands des Datenwörterbuchs](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md) beschrieben. <!--Add info about how users with administrator access can control these after the feature is available. How?--></p> |
| [!UICONTROL **Tags**] | Zeigt alle Tags an, die auf die Komponente angewendet werden. Benutzende mit Adminrechten können bei der Bearbeitung der Komponente Tags hinzufügen. |
| [!UICONTROL **Typ der Komponente**] | Listet den Komponententyp auf, ob es sich um eine Dimension, eine Metrik, ein Segment oder einen Datumsbereich handelt. |
| [!UICONTROL **Erstellt von**] | Zeigt den Namen der Person an, die die Komponente erstellt hat. |
| [!UICONTROL **Vorschau**] | Zeigt eine Vorschau davon an, wie die Komponente im Analysis Workspace aussieht. |
| [!UICONTROL **Datum der letzten Änderung**] | Zeigt den Tag an, an dem die Komponente zuletzt geändert wurde. Dieser Abschnitt wird beim Anzeigen von Segmenten, berechneten Metriken und Datumsbereichen angezeigt. <!--for CJA, it is displayed for all components--> |

{style=&quot;table-layout:auto&quot;}

## Eingeschränkte Testphase der Version {#release-limited-testing}

>[!AVAILABILITY]
>
>Die in diesem Artikel beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

## Abschnitt zur eingeschränkten Testphase der Veröffentlichung {#release-limited-testing-section}

>[!AVAILABILITY]
>
>Die in diesem Abschnitt beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

