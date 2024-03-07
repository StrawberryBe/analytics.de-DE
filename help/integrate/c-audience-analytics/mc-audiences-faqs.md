---
description: Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.
solution: Experience Cloud
title: Häufig gestellte Fragen zu Audience Analytics
feature: Audience Analytics
exl-id: 86e7967c-030c-44d6-8294-e7e6d41f6fc3
source-git-commit: 750c4b0ffb52c3f2cf25abcd76ef149a4521109e
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 31%

---

# Häufig gestellte Fragen

Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.

## FAQs zu rechtlichen Fragen {#legal}

+++ Woher weiß ich, ob ich persönlich identifizierbare Informationen (PII) in meinen Analytics-Daten verwende? Und wenn ja, was mache ich dagegen?

Wenn sich in einer Prop oder einer eVar E-Mails/Adressen/etc. befinden, sollten Sie die Daten während der Erfassung mit einem Hashing versehen. Wenn in Ihrem Land IP-Adressen als persönlich identifizierbare Informationen gelten, [IP-Verschleierung aktivieren](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/exclude-ip.html?lang=de). Sprechen Sie mit Ihrem Analytics-Administrator, um zu erfahren, was Sie erfassen. Sprechen Sie mit Ihrer Rechtsabteilung, um zu erfahren, was sie als personenbezogene Daten betrachten.

+++

+++ Woher weiß ich, ob meine Report Suites eine Personalisierung auf der Site oder ein Targeting auf der Site oder außerhalb der Site bzw. Site durchführen?

Dies gilt nicht für das Senden von Adobe Analytics-Daten an Adobe Audience Manager. Fragen Sie sich:

* Werden Sie ein von Analytics freigegebenes Segment mit einer MCA-Dimension wieder auf der Experience Cloud freigeben?

* Exportieren Sie (z. B. über Datenfeeds) in ein Business Intelligence-System (BI), das für diese Zwecke verwendet wird?

+++

## Adobe Audience Manager-spezifische FAQs {#aam-specific}

+++ Wie erstelle ich ein Analytics-Ziel in Audience Manager?

Siehe [Konfigurieren eines Analytics-Ziels in Adobe Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=de)&quot;.

+++

+++ Wie lange dauert es nach dem Erstellen und Speichern eines Analytics-Ziels, bis Daten in meinen ausgewählten Report Suites angezeigt werden?

Es kann einige Stunden dauern, Ihre Report Suites mit neuen Daten zu füllen.

+++

+++ Ich habe ein neues Analytics-Ziel erstellt, aber es wird nicht im Abschnitt Zielzuordnungen meiner verfügbaren Segmente angezeigt. Wohin ging das Ziel, oder wie finde ich es?

Ein Analytics-Ziel verschwindet aus dem Abschnitt Zielzuordnungen eines Segments, wenn Sie die **[!UICONTROL Alle aktuellen und zukünftigen Segmente automatisch zuordnen]** -Option in **[!UICONTROL Segmentzuordnungen]**. Um das zu vermeiden, wählen Sie statt der automatischen Option **[!UICONTROL Segmente manuell zuweisen]** aus.

+++

Erhalte ich damit alle Informationen aus Adobe Audience Manager in Analytics?

Nein, nur Daten, die sich auf Personen beziehen, die während oder nach der Aktivierung von Audience Manager-Zielgruppen und während oder nach der Qualifizierung des Segments auf Ihre Site kommen.

+++

+++ Erhalte ich damit eine gesamte adressierbare Zielgruppe pro Segment?

Nicht ganz. Sie erfahren die Anzahl der Besucher in diesem Segment, die während oder nach der Qualifizierung des Segments auf Ihre Site kamen.

+++

+++ Inwiefern unterscheidet sich dies vom alten Cookie-Ziel in Analytics?

Segmente werden für qualifiziert und in Echtzeit zurückgegeben - bei demselben Treffer. Die Anzeigenamen werden automatisch angezeigt.

+++

+++ Was passiert, wenn einige meiner Report Suites personenbezogene Daten haben und andere nicht?&lt;

Tipp: Erstellen Sie zwei Ziele – Fügen Sie die Report Suites mit persönlichen Daten zu einem Ziel hinzu und die Report Suites ohne persönliche Daten zum anderen.

+++

## Analytics-spezifische FAQs {#aa-specific}

+++ Wird diese Integration in Analytics als Dimension oder Segment angezeigt?

Als Dimensionen: Zielgruppen-ID und Zielgruppenname.

+++

+++ Wo kann ich diese Dimensionen in Analytics verwenden?

Überall werden sie wie jede andere in Analytics erfasste Dimension behandelt.

+++

+++ Warum kommen keine Daten in Analytics durch?

Wahrscheinlich gibt es zwischen Datenquelle und Ziel einen Konflikt zwischen den Datenschutzbestimmungen von Adobe Audience Manager.

+++

+++ Warum fehlen einige meiner Segmente in Analytics, obwohl ich ausgewählt habe, dass alle Segmente gesendet werden sollen?&lt;

* Ihre Adobe Audience Manager-Datenexportkontrollen für das Ziel und die Datenquellen der Segmente können in Konflikt geraten, was verhindert, dass bestimmte Segmente gesendet werden.

* Wenn Sie Eigenschaften mit Drittpartei-Daten in Ihren Segmenten verwenden, können diese Segmente nicht an ein Ziel (einen Satz von Report Suites) weitergeleitet werden, das persönliche Daten enthält.

+++

+++ Warum wird in meinem Analytics-Bericht &quot;Zielgruppenlimit erreicht&quot;angezeigt? (Hinweis: Dies wird auch als Zielgruppen-ID = -1 und `::max_audiences_exceeded::` in Data Warehouse)

Standardmäßig sendet die Audience Analytics-Integration für Adobe Audience Manager alle-Segmente, für die sich ein Besucher pro Treffer qualifiziert, an Analytics. Wenn ein Besucher bei einem einzelnen Treffer zu mehr als 150 Adobe Audience Manager-Segmenten gehört, wird die **150 zuletzt qualifizierte Segmente** werden an Analytics gesendet, während die verbleibende Liste abgeschnitten ist. Es wird ein zusätzliches Warnsignal an Analytics gesendet, das anzeigt, dass die Segmentliste gekürzt wurde. Dieses Warnsignal wird in der Dimension „Zielgruppendimension“ als „Zielgruppenlimit erreicht“ und in der Dimension „Zielgruppen-ID“ als „-1“ dargestellt.

Es ist zwar unwahrscheinlich, dass sich ein Besucher bei einem bestimmten Treffer für mehr als 150 Segmente qualifiziert, aber es kann in seltenen Fällen vorkommen. Wenn Ihnen in Ihrer Berichterstellung die Meldung „Zielgruppenlimit erreicht“ angezeigt wird, haben Sie zwei Optionen:

* Option 1: Lassen Sie die Integration weiterhin in ihrem vordefinierten Zustand funktionieren und senden Sie die 150 Segmente, die für einen bestimmten Besucher am häufigsten qualifiziert wurden.

* Option 2: Wählen Sie in Adobe Audience Manager die 150 Segmente aus, die für Ihr Unternehmen am wichtigsten sind. Adobe Audience Manager überprüft dann Besucher nur anhand der 150 Segmente. Der Nachteil dieser Vorgehensweise ist, dass Sie bei allen Besuchern nur noch diese 150 Segmente erhalten. Dahingegen liefert die Vorgehensweise in Option 1 dadurch, dass die Integration pro Treffer Segmente sendet, eine unbegrenzte Anzahl an Segmenten.

+++

+++ Werden Analytics für diese Integration zusätzliche Server-Aufrufe in Rechnung gestellt?

Nein. Adobe Audience Manager-Zielgruppen sind serverseitig in Analytics-Treffer integriert. Dabei fallen keine zusätzlichen Server-Aufrufe für Analytics an (primär oder sekundär).

+++

## FAQs zur serverseitigen Weiterleitung {#SSF}

+++ Muss ich, wenn ich die alte SSF implementiert habe, auch zu Analytics Admin gehen und die Report Suite-SSF aktivieren?

Ja. In der Adobe Audience Manager-Zieleinrichtung werden nur Report Suites angezeigt, bei denen SSF aktiviert ist.

+++

+++ Warum kann ich bestimmte Report Suites für SSF nicht in Analytics Admin aktivieren?

Es können nur Suites aktiviert werden, die Ihrer Experience Cloud-Org zugeordnet sind.

Weitere häufig gestellte Fragen zu diesem Thema finden Sie unter [FAQs zur serverseitigen Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md).

+++

## Allgemeine FAQs {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

+++ Warum unterscheiden sich die Besucherzahlen für Segmente zwischen Audience Manager und Analytics?

Siehe [Unterschiede in der Besucherzahl](/help/integrate/c-audience-analytics/visitor-count-reconciliation.md).

+++

+++ Was ist der Unterschied zwischen &quot;Zielgruppen&quot;in Adobe Audience Manager und &quot;Segmenten&quot;in Analytics?

Siehe [Segmente in Analytics und Audience Manager - Grundlagen](/help/integrate/c-audience-analytics/aam-analytics-segments.md). Adobe Audience Manager-Zielgruppen werden gesendet und als &quot;Dimensionskomponenten&quot;freigegeben, die in Analytics verwendet werden können. Sie werden beispielsweise nicht als Segmente im Segment Builder angezeigt, sondern als Dimensionen, mit denen Sie Segmente erstellen können.

+++

+++ Was ist der Unterschied zwischen Kundenattributen und in Adobe Audience Manager integrierten Kundendaten?

Kundenattribute sind nicht zeitbasiert; sie gelten rückwirkend und werden weiterverwendet. Adobe Audience Manager-integrierte Daten sind zeitbasiert und nur zukünftig verfügbar. Darüber hinaus sind Kundenattribute eine Suchtabelle für Experience Cloud-Besucher-IDs, während die Adobe Audience Manager-Integration Daten enthält, die bei jedem Treffer für einen Besucher zugeordnet werden.

+++

+++ Wie verhält es sich mit veralteten Ansätzen für dieses Problem, z. B. den alten Beta- oder Consulting-Plug-in-Cookie-Zielen?

Wir empfehlen Ihnen, die neue Integration zu implementieren und alte Ziele zu entfernen.

+++
