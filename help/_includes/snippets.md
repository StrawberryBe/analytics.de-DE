---
source-git-commit: 82bb289183f04ec6f795ebfa489436a7b0cc021f
workflow-type: ht
source-wordcount: '974'
ht-degree: 100%

---
# Snippets

## Mitteilung zum Ende der Nutzungsdauer von Reports &amp; Analytics {#ra-eol}

>[!IMPORTANT]
>
>Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://www.adobe.com/go/analytics_rnaeol_de) von Reports &amp; Analytics.

## Filterkriterien für Datenwörterbuch {#dd-filter-criteria}

1. (Optional) Wählen Sie das Symbol **Filter** ![Datenwörterbuchfilter-Symbol](/help/analyze/analysis-workspace/components/data-dictionary/assets/data-dictionary-filter-icon.png) und wählen Sie dann eine der folgenden Filteroptionen, um die Liste der Komponenten zu filtern:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Genehmigt**] | Nur Komponenten anzeigen, die von Admins als genehmigt markiert wurden. |
   | [!UICONTROL **Favoriten**] | Nur Komponenten anzeigen, die sich in Ihrer Favoritenliste befinden. Informationen zum Hinzufügen von Komponenten zur Favoritenliste finden Sie in der [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensionen**] | Nur Komponenten anzeigen, die Dimensionen sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Metriken**] | Nur Komponenten anzeigen, die Metriken sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Segmente**] | Nur Komponenten anzeigen, die Segmente sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) <!--this is Filters in CJA--> |
   | [!UICONTROL **Datumsbereiche**] | Zeigt nur Komponenten an, die Datumsbereiche sind. (Diese Option ist auch auf der Registerkarte [!UICONTROL **Schnellfilter**] verfügbar, wenn Sie das Datenwörterbuch zum ersten Mal aufrufen.) |
   | [!UICONTROL **Alle anzeigen**] | Alle Komponenten anzeigen. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Nicht genehmigt**] | Nur Komponenten anzeigen, die von Admins noch nicht als genehmigt markiert wurden. Für Admins beim Identifizieren von Komponenten hilfreich, die überprüft und genehmigt werden müssen. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Fehlende Beschreibung**] | Nur Komponenten anzeigen, die noch keine Beschreibung im Feld „Beschreibung“ haben. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Duplikate anzeigen**] | <p>Nur Komponenten anzeigen, die denselben Namen oder dieselbe Definition wie eine andere Komponente in der ausgewählten Report Suite aufweisen. Namen oder Definitionen müssen exakt übereinstimmen, damit sie als Duplikate angezeigt werden.</p><p>Diese Option steht nur Admins zur Verfügung.</p><p>**HINWEIS:** Für Definitionen umfasst dies sowohl von Ihnen erstellte als auch von Adobe bereitgestellte Komponenten. Für Namen umfasst dies derzeit nur von Ihnen erstellte Komponenten und nicht die von Adobe bereitgestellten Komponenten. Die Anzeige doppelter Namen für von Adobe bereitgestellte Komponenten wird in einer zukünftigen Version hinzugefügt.</p> |
   | [!UICONTROL **Keine aktuellen Daten**] | Nur Komponenten anzeigen, die in den letzten 90 Tagen keine Daten erfasst haben. Diese Option steht nur Admins zur Verfügung. |
   | [!UICONTROL **Erstellt von Adobe**] <!-- I don't see this option--> | Nur Komponenten anzeigen, die von Adobe erstellt wurden. Komponenten, die von Admins oder anderen Benutzenden in deren Organisation erstellt wurden, werden nicht angezeigt. |

   {style="table-layout:auto"}

## Komponenteninformationen für Datenwörterbuch {#dd-component-information}

| Option | Funktion |
|---------|----------|
| [!UICONTROL **Genehmigt**] | <p>Zeigt an, dass die Komponente vom Admins geprüft und genehmigt wurde.</p><p>Nachdem eine Komponente genehmigt wurde, können Admins die Genehmigung durch Auswahl der Schaltfläche **Genehmigt** entfernen.</p> |
| [!UICONTROL **Genehmigung erforderlich**] | <p>Zeigt an, dass die Komponente noch nicht von Admins geprüft und genehmigt wurde.</p><p>Admins wird eine Option zum [!UICONTROL **Genehmigen**] angezeigt. Bei Auswahl dieser Option wird die Komponente gegenüber Benutzenden als „Genehmigt“ gekennzeichnet.</p> |
| [!UICONTROL **Beschreibung**] | Beschreibt die beabsichtigte Funktion der Komponente. (Diese Informationen werden vom Analytics-Admins hinzugefügt, wie unter [Komponentenbeschreibungen hinzufügen](/help/analyze/analysis-workspace/components/add-component-descriptions.md) beschrieben.) |
| [!UICONTROL **Häufig verwendet mit**] | <p>Zeigt Komponenten an, die am häufigsten mit der Komponente verwendet werden, die Sie anzeigen.</p><p>Es werden bis zu 5 Komponenten für die 5 primären Komponententypen angezeigt: Metrik, Berechnete Metrik, Dimension, Segment und Datumsbereich.</p><p>Diese Liste basiert auf Daten aus den letzten 90 Tagen. Es werden nur Komponenten angezeigt, auf die Sie Zugriff haben.</p><p>Admins können die Komponenten, die Benutzende in diesem Abschnitt sehen, kuratieren, indem sie die gewünschten Komponenten in den Dropdown-Feldern [!UICONTROL **Immer einschließen**] und [!UICONTROL **Immer ausschließen**] auswählen. Bevor Sie die Komponenten kuratieren, die Benutzenden angezeigt werden, wenden Sie zunächst den Filter **Alle anzeigen** an, um sicherzustellen, dass Sie alle Komponenten sehen, die nicht für Sie freigegeben sind.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
| [!UICONTROL **Ähnlich wie**] | <p>Zeigt Komponenten mit ähnlichen Namen wie die angezeigte Komponente an.</p><p>Es werden bis zu 5 Komponenten für die 5 primären Komponententypen angezeigt: Metrik, Berechnete Metrik, Dimension, Segment und Datumsbereich.</p><p>Es werden nur Komponenten angezeigt, auf die Sie Zugriff haben.</p><p>Hier werden auch alle doppelten Komponenten in Ihrer Report Suite angezeigt. Analytics-Admins sollten alle doppelten Komponenten identifizieren und entfernen, wie unter [Überwachen des Zustands des Datenwörterbuchs](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md) beschrieben.</p><p>Adminis können die Komponenten, die Benutzende in diesem Abschnitt sehen, kuratieren, indem sie die gewünschten Komponenten in den Dropdown-Feldern [!UICONTROL **Immer einschließen**] und [!UICONTROL **Immer ausschließen**] auswählen. Bevor Sie die Komponenten kuratieren, die Benutzenden angezeigt werden, wenden Sie zunächst den Filter **Alle anzeigen** an, um sicherzustellen, dass Sie alle Komponenten sehen, die nicht für Sie freigegeben sind.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**HINWEIS:** Derzeit enthält der Abschnitt **Ähnlich wie** nur von Ihnen erstellte Komponenten und nicht die von Adobe bereitgestellten Komponenten. Von Adobe bereitgestellte Komponenten werden in einer zukünftigen Version hinzugefügt.</p> |
| [!UICONTROL **Tags**] | Zeigt alle Tags an, die auf die Komponente angewendet werden. Benutzende mit Adminrechten können bei der Bearbeitung der Komponente Tags hinzufügen. |
| [!UICONTROL **Typ der Komponente**] | Listet den Komponententyp auf, ob es sich um eine Dimension, eine Metrik, ein Segment oder einen Datumsbereich handelt. |
| [!UICONTROL **Erstellt von**] | Zeigt den Namen der Person an, die die Komponente erstellt hat. |
| [!UICONTROL **Vorschau**] | Zeigt eine Vorschau davon an, wie die Komponente im Analysis Workspace aussieht. |
| [!UICONTROL **Datum der letzten Änderung**] | Zeigt den Tag an, an dem die Komponente zuletzt geändert wurde. Dieser Abschnitt wird beim Anzeigen von Segmenten, berechneten Metriken und Datumsbereichen angezeigt. |

{style="table-layout:auto"}

## Eingeschränkte Testphase der Version {#release-limited-testing}

>[!AVAILABILITY]
>
>Die in diesem Artikel beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

## Abschnitt zur eingeschränkten Testphase der Veröffentlichung {#release-limited-testing-section}

>[!AVAILABILITY]
>
>Die in diesem Abschnitt beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).


## Plug-in-Haftungsausschluss {#plug-in}

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe bei diesem Plug-in benötigen, wenden Sie sich an das für Ihr Unternehmen zuständige Adobe-Kunden-Team. Sie können ein Treffen mit einer Beraterin oder einem Berater zur Unterstützung arrangieren.

