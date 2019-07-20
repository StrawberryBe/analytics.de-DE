---
description: Virtual Report Suites können als Ersatz für Multisuite-Tagging verwendet werden. Anstatt Daten an zwei separate Report Suites zu senden, können Sie z. B. Daten an eine Report Suite senden und virtuelle Report Suites nutzen, um den Umfang der Daten einzuschränken, auf die Benutzer zugreifen können. Der Datenzugriff ist jedoch nur einer der Gründe, aus denen separate Report Suites von Vorteil sein können. Befassen Sie sich eingehend mit den folgenden Anwendungsfällen, bevor Sie für Virtual Report Suites Änderungen der Implementierung durchführen.
keywords: Virtual Report Suite
seo-description: Virtual Report Suites können als Ersatz für Multisuite-Tagging verwendet werden. Anstatt Daten an zwei separate Report Suites zu senden, können Sie z. B. Daten an eine Report Suite senden und virtuelle Report Suites nutzen, um den Umfang der Daten einzuschränken, auf die Benutzer zugreifen können. Der Datenzugriff ist jedoch nur einer der Gründe, aus denen separate Report Suites von Vorteil sein können. Befassen Sie sich eingehend mit den folgenden Anwendungsfällen, bevor Sie für Virtual Report Suites Änderungen der Implementierung durchführen.
seo-title: Überlegungen zur globalen und globalen/Multi-Suite-Tagging
solution: Analytics
title: Überlegungen zur globalen und globalen/Multi-Suite-Tagging
topic: Reports and Analytics
uuid: f 17 d 3659-a 5 b 1-4807-a 01 d-a 1 b 420009 a 64
translation-type: tm+mt
source-git-commit: 800d4ed34a816bd331b339295dc3acd2a03a2cd5

---


# Überlegungen zur globalen und globalen/Multi-Suite-Tagging

Mit Virtual Report Suites werden Daten einer Report Suite angezeigt, die in Ihren digitalen Properties erfasst werden, aber über ein dauerhaft zugewiesenes Segment verfügen.

Da Virtual Report Suites wie Report Suites funktionieren und Benutzergruppen zugeordnet werden können, können Virtual Report Suites in manchen Fällen Multi-Suite-Tagging ersetzen, sodass [sekundäre Server-Aufrufe](/help/admin/c-server-call-usage/overage-overview.md) vermieden werden. (Multi-Suite-Tagging ist die Möglichkeit, Daten mithilfe einer einzigen Bildanforderung an mehrere Report Suites zu senden.) Anstatt beispielsweise Daten für zwei Ihrer Marken an zwei separate „untergeordnete“ Report Suites sowie eine „globale“ Report Suite zu senden, in der markenübergreifende Daten zusammengeführt werden, können Sie Daten von beiden Marken auch nur an die globale Report Suite senden. Mit Virtual Report Suites können Sie danach den Benutzerzugriff auf die Daten (nach Marken) einschränken, indem Sie die untergeordneten Report Suites replizieren.

Wenn Sie Multi-Suite-Tagging durch eine globale Report Suite und Virtual Report Suites ersetzen, können Sie Ihre Adobe Analytics-Implementierung vereinfachen und die Anzahl der Server-Aufrufe reduzieren. Dies wird allgemein als Best Practice empfohlen. Es gibt jedoch einige wichtige Einschränkungen bei Virtual Report Suites, die Sie berücksichtigen sollten, wenn Sie entscheiden, ob Sie Multi-Suite-Tagging oder eine einzelne globale Report Suite gemeinsam mit Virtual Report Suites verwenden. Die folgenden Richtlinien sollen Ihnen bei der Entscheidung helfen, ob auf einer globalen Report Suite erstellte Virtual Report Suites der richtige Ansatz für Sie sind.

## Richtlinien

>[!NOTE]
>
> Die folgenden Überlegungen gelten nur für diese Fälle:
>
>* Sie erwägen die Änderung Ihrer Implementierung, um untergeordnete Report Suites zu entfernen und sich allein auf virtual &gt; Report Suites zu verlassen, um die Ansichten für Endbenutzer zu steuern oder
>* Benutzer von Adobe Analytics in Ihrem Unternehmen sollen Virtual Report Suites als primäre Methode der Datenansicht verwenden.


Wenn Sie sich nicht sicher sind, ob die beschriebenen Anwendungsfälle auf Sie und Ihr Unternehmen zutreffen, wenden Sie sich an andere Administratoren von Adobe Analytics oder an Ihr Adobe Account-Team. Diese können Ihnen dabei helfen, Ihre Geschäftsanforderungen zu beurteilen, und eine Empfehlung abgeben.

Die Verwendung von Virtual Report Suites zum Ersetzen von Multi-Suite-Tagging wird unter folgenden Umständen empfohlen:

## Die Veröffentlichung von Segmenten aus Adobe Analytics in der übrigen Adobe Experience Cloud ist nur auf der Ebene der globalen Report Suite erforderlich und alle Benutzer, die Segmente veröffentlichen, haben Zugriff auf die globale Report Suite.

Zusammenfassung:

* Für Virtual Report Suites wird die Freigabe von Segmenten in Adobe Experience Cloud derzeit nicht unterstützt.
* Benutzer, die eine Freigabeberechtigung für ein Segment in Experience Cloud benötigen, müssen Zugriff auf eine reale Report Suite (über- oder untergeordnet) haben.

Derzeit können keine Segmente aus einer Virtual Report Suite für die Personalisierung und das Targeting in Adobe Experience Cloud veröffentlicht werden. Alle Benutzer, die Segmente veröffentlichen, benötigen für diesen Zweck Zugriff auf eine reale Report Suite. Beim Multi-Suite-Tagging werden untergeordnete Report Suites auf Marken-, Property-, Regionsebene usw. erstellt. Dadurch können Benutzer, die keinen Zugriff auf die globale Report Suite haben, Segmente veröffentlichen, die nur den Datensatz enthalten, der ihnen in der untergeordneten Report Suite zur Verfügung steht.

Nehmen wir an, Ihre Benutzer haben ausschließlich Zugriff auf Virtual Report Suites in ihrer geografischen Region, Sie möchten aber, dass sie auch Segmente aus Adobe Analytics erstellen und für das Targeting mit Adobe Target in Adobe Experience Cloud freigeben können. In diesem Fall wären diese Benutzer nicht in der Lage, Segmente zu veröffentlichen. Sie sollten deshalb Multi-Suite-Tagging verwenden, um dies zu ermöglichen.

## Sie benötigen keine Berichte zu Echtzeit- oder aktuellen Daten auf Ebene der Virtual Report Suite.

Zusammenfassung:

* Virtual Report Suites unterstützen keine Echtzeitberichte, weil die Daten segmentiert sind.
* Die Funktion „Aktuelle Daten“ wird in Virtual Report Suites nicht unterstützt, da sie keine Segmentierung unterstützt.

[Echtzeitberichte](/help/admin/admin/realtime/t-realtime-admin.md) und ["Aktuelle Daten"](../../technotes/latency.md) sind in Virtual Report Suites nicht verfügbar. Diese Funktionen von Reports &amp; Analytics bieten schnelleren Zugriff (Sekunden bis Minuten) auf eingeschränkte Datentypen. Zu den Einschränkungen dieser Ansichten zählt, dass keine Segmentierung unterstützt wird. Anders ausgedrückt, können Echtzeitdaten in Reports &amp; Analytics nicht segmentiert werden. Da eine Virtual Report Suite mithilfe von Segmentierung erstellt wird, ist sie mit Echtzeitberichten nicht kompatibel. Dies hat Auswirkungen auf Benutzer, die innerhalb von Sekunden oder wenigen Minuten nach der Datenerfassung auf Veränderungen in Adobe Analytics reagieren, wie z. B. Redakteure in einem Newsroom, die die Headlines entsprechend dem Echtzeitzugriff auf Inhalte anpassen. In diesem Fall sollten Sie Folgendes tun:

* Verwenden Sie Multi-Suite-Tagging, um sicherzustellen, dass jeder Benutzer nur die Echtzeitdaten sieht, die er sehen darf, oder
* Lassen Sie diese Benutzer auf eine reale (globale) Report Suite zugreifen, wenn sie Zugriff auf den vollständigen Datensatz haben sollten.

## Sie überschreiten in Ihren globalen Report Suites bei den wichtigsten Dimensionen keine Grenzwerte, oder es macht nichts aus, wenn Ihre Benutzer „Geringer Traffic“ in ihren Virtual Report Suites sehen.

Zusammenfassung:

* Virtual Report Suites haben keine eigenen Grenzwerte für Dimensionen, sondern übernehmen sie von ihrer übergeordneten Report Suite.
* Wenn Ihre Adobe Analytics-Benutzer Zugriff auf alle Werte einer Dimension benötigen, die häufig mehr als 500.000 individuelle Werte pro Monat aufweisen, sollten Sie die Verwendung von Multi-Suite-Tagging in Betracht ziehen.

In Fällen hoher Kardinalität (große Anzahl von individuellen Werten in einer bestimmten Dimension, wie z. B. Produktnummern oder Seiten) fasst Adobe Analytics die selten gefundenen Werte jeden Monat im Zeileneintrag „Geringer Traffic“ für eine Dimension in einer Report Suite zusammen. Werte, die im zusammengefassten Eintrag „Geringer Traffic“ enthalten sind, können nicht segmentiert werden. Auf diese Weise werden Adobe Analytics-Abfragen schnell durchgeführt und konzentrieren sich auf die 500.000 wichtigsten Zeileneinträge, die am häufigsten für die Dimension in Ihren digitalen Properties angezeigt werden. (Zum Beispiel könnten dies Ihre wichtigsten 500.000 Seitennamen sein.) Mehr über die individuellen Grenzwerte erfahren Sie [hier](../../technotes/low-traffic.md).

Virtual Report Suites verfügen nicht über einen eigenen Satz von 500.000 individuellen Werten pro Dimension und Monat. Wenn in einer Report Suite, auf der eine Virtual Report Suite basiert, 500.000 individuelle Werte für eine bestimmte Dimension überschritten wurden und niedrige Werte in der Zeile „Geringer Traffic“ für diese Dimension zusammengefasst werden, wird „Geringer Traffic“ auch in der Virtual Report Suite angezeigt.

**Beispiel**: Ein Medienkontextprogramm besitzt 100 Webeigenschaften. Jede Property veröffentlicht zusätzlich zu allen Artikeln aus den Vormonaten einige tausend Nachrichtenartikel im Monat, und alle Properties werden in einer globalen Report Suite zusammengefasst. Angenommen, die Dimension „Artikelname“ der globalen Report Suite enthält jeden Monat 4 Millionen individuelle Artikelnamen aus den verschiedenen Properties. Die wichtigsten 500.000 Werte, die den größten Teil des Datenverkehrs ausmachen, werden angezeigt und können segmentiert werden, aber die restlichen 3,5 Millionen Werte werden in der Zeile „Geringer Traffic“ zusammengefasst.

In diesem Fall könnten Sie 100 Virtual Report Suites für Teams erstellen, die an den einzelnen Properties arbeiten. Obwohl dies akzeptabel ist, sollten Sie bedenken, dass in der Dimension „Artikelname“ in jeder Virtual Report Suite nur die höchsten 500.000 Werte der globalen Report Suite für die jeweilige Property als einzelne Zeileneinträge angezeigt werden. In Virtual Report Suites werden die 500.000 individuellen Werte pro Dimension nicht einzeln zugeordnet. Werte, die in der globalen Report Suite im Eintrag „Geringer Traffic“ zusammengefasst wurden, werden in der Virtual Report Suite nicht einzeln dargestellt. Dies kann zu Verwirrung unter den Benutzern führen, die erwarten, in einer Virtual Report Suite einen vollständigen Satz von Dimensionswerten zu finden und stattdessen nur die Werte mit hohem Datenverkehr sehen.

Wenn Sie wissen, dass die Grenzwerte für individuelle Werte in Ihrer globalen Report Suite oder in Ihren bestehenden untergeordneten Report Suites regelmäßig überschritten werden, überlegen Sie, ob Benutzer Zugriff auf diese seltenen Werte benötigen, bevor Sie zu Virtual Report Suites wechseln. Wenn Ihre Benutzer Zugriff auf alle Werte in einer Dimension benötigen, deren Grenzwert in der globalen Report Suite überschritten wird, sollten Sie weiterhin Multi-Suite-Tagging verwenden, um diesen Zugriff zu gewährleisten.

Darüber hinaus kann die Kundenunterstützung von Adobe einzelne Grenzwerte in begrenztem Umfang für eine kleine Anzahl von Dimensionen für eine globale Report Suite erhöhen, wodurch dieses Problem möglicherweise vollständig behoben ist. Weitere Informationen erhalten Sie bei Ihrer Kundenbetreuung und Kundenunterstützung.

## Sie können Ihren verfügbaren Satz benutzerdefinierter Dimensionen (eVars und Props) und Metriken (Ereignisse) in Ihrer globalen Report Suite verwenden, um alle kritischen Datenpunkte in allen Properties zu tracken.

Zusammenfassung:

* Virtual Report Suites verfügen nicht über eigene Dimensionen und Metriken, sondern übernehmen diese von der übergeordneten Report Suite.
* Die übergeordnete Report Suite muss daher in der Lage sein, alle relevanten Dimensionen und Metriken für alle Properties, die in ihr zusammengefasst sind, ausschließlich mithilfe der für die globale Report Suite verfügbaren benutzerdefinierten 325 Dimensionen und 1.000 Metriken zu erfassen.

Ein aktueller Vorteil des Multi-Suite-Tagging besteht darin, dass Sie verschiedene Properties, Marken, Regionen usw. verwenden können, um verschiedene Datentypen zu erfassen. Beispielsweise könnte eine Unternehmenseinheit eVar76 verwenden, um „Interne Suchbegriffe“ zu erfassen, während eine andere Einheit diese eVar verwenden könnte, um „Video-Namen“ zu erfassen. Gruppen können Adobe Analytics gemäß ihren individuellen Anforderungen implementieren.

Bei einer globalen Report Suite müssen alle Properties dieselben Datenpunkte an die gleiche Dimension und Metrik weiterleiten. Im vorherigen Beispiel müssten diese beiden Marken gemeinsam eVar76 entweder für „Interne Suchbegriffe“ oder für „Video-Namen“ verwenden und der andere Datenpunkt müsste dann in eine andere Dimension in den jeweiligen Implementierungen eingefügt werden. Geschieht dies nicht, kommt es zu einer Verfälschung der Dimensionen und/oder Metriken in der globalen Report Suite. Dies ist in Fällen problematisch, in denen verschiedene Properties, Marken, Regionen usw., die Sie (mit einzelnen Report Suites) unterstützen, ihr volles Kontingent verfügbarer benutzerspezifischer Dimensionen oder Metriken nutzen. Folglich wäre es nicht möglich, einige ihrer Dimensionen oder Metriken für die Tracking-Erfordernisse anderer Properties, Marken, Regionen usw. zu reservieren.

Die maximale Anzahl benutzerspezifischer Adobe Analytics-Dimensionen pro Report Suite beträgt 325 und die maximale Anzahl von benutzerspezifischen Ereignissen pro Report Suites beträgt 1.000. Wenn Sie zu einer globalen Report Suite wechseln, müssen Sie deshalb sicherstellen, dass alle wichtigen Datenpunkte aller digitalen Properties mit den gleichen 325 benutzerspezifischen Dimensionen und den gleichen 1.000 benutzerspezifischen Ereignissen getrackt werden können.

Wenn Sie sich in dieser Situation befinden und den Wechsel zu einer globalen Report Suite in Kombination mit Virtual Report Suites in Betracht ziehen, überprüfen Sie die verschiedenen Implementierungen von Adobe Analytics in Ihrem Unternehmen, um festzustellen, wie viele Überschneidungen und Unstimmigkeiten in diesen Implementierungen vorhanden sind und welche Dimensionen oder Metriken nicht entscheidend für den Geschäftserfolg sind. Erwägen Sie auch, [Klassifizierungen](/help/components/c-classifications2/c-classifications.md) in Ihrer globalen Suite zu nutzen, um in ihre Berichte Werte aufzunehmen, die derzeit eventuell eine eigene Dimension verwenden. Klassifizierungen sind automatisch für jede Virtual Report Suite verfügbar, die auf dieser globalen Suite basiert. Sie können zum Beispiel die Klassifizierung „Produktname“ auf der Grundlage der „Produkt“-Dimension erstellen, anstatt „Produktname“ in eVar5 zu erfassen.

Wenn Sie diese benutzerspezifischen Dimensionen und Ereignisse nicht zusammenfassen können, empfiehlt Adobe, weiterhin Multi-Suite-Tagging zu verwenden.

>[!IMPORTANT]
>
>With the introduction of [virtual report suite curation](/help/analyze/analysis-workspace/curate-share/curate-projects-vrs.md), you can now change the name of a given dimension or &gt;metric on a per-VRS basis. Wenn Sie Ihre Virtual Report Suite keimfrei segmentieren, können Sie jetzt die gleiche evar, Prop oder das Ereignis verwenden, um verschiedene Dinge in unterschiedlichen Virtual Report Suites zu erfassen. Wenn Sie jedoch zwei &gt; verschiedene Datenarten in derselben Dimension oder Metrik übergeben, kann dieser Datenpunkt in der &gt; globalen Report Suite praktisch unbrauchbar sein. Es kann auch zu Problemen mit der Zuordnung führen, wie in diesem Beispiel: Wenn ein Benutzer zwei &gt; Werte für evar 10 erhält, die eine'Interne Kampagne'für die Eigenschaft A und eine andere'Seitenname'auf &gt; B'ist, bedeutet dies, dass der Erfolg nun auf'Interne Kampagne'und auf'Seitenname'aufgeteilt wird, was auf unterschiedlichen Ebenen basiert. Daher empfiehlt Adobe im Allgemeinen nicht, die VRS-Kuration als Workaround &gt; für dieses Problem zu verwenden.

## Die Segmente, die Sie mit Virtual Report Suites verwenden, unterteilen die Daten nicht in einer Weise, die Ihre Benutzer verwirren könnte.

Zusammenfassung:

* Die Segmentierung von Daten einer globalen Report Suite in Virtual Report Suites kann zu differenzierten Ergebnissen führen, die einige Benutzer verwirren können.
* Überlegen Sie, wie sich Ihre Segmente in Virtual Report Suites auf Dimensionen und Funktionen wie Entrypage, Referrer-Domäne, Pfad usw. auswirken können.

Denken Sie daran, dass eine Virtual Report Suite nur ein Segment ist, das auf eine Report Suite angewendet wird; alle Differenzierungen der segmentierten Daten gelten für Virtual Report Suites. Unter Umständen können Daten durch Segmente (und damit Virtual Report Suites) so aufgeteilt werden, dass die Daten für Adobe Analytics-Anwender unlogisch erscheinen.

Angenommen, Sie haben zwei Marken, A und B, deren digitale Properties Daten an eine globale Report Suite senden. Einige Besucher wechseln von Website A zu Website B und umgekehrt, und dieser Wechsel ist im Pfadverlauf in der globalen Report Suite ersichtlich. Wenn Sie jedoch Virtual Report Suites für die Marken A und B erstellen, könnte es sein, dass Benutzer, die auf die Virtual Report Suite B zugreifen, unverständliche Ergebnisse für bestimmte Dimensionen und Metriken sehen. Ein Besuch, der mit Marke A begann und mit Marke B endete, zeigt keine Entrypage in der Virtual Report Suite B an, da die Entrypage für den Website-übergreifenden Besuch mit Marke A begann, die aus dieser Virtual Report Suite wegsegmentiert wurde.

Ein ähnliches Beispiel ist die „Besuch-Nr.“. In der Virtual Report Suite für Marke B könnten Benutzer einige Besucher sehen, die einen zweiten, dritten und vierten Besuch zu haben scheinen, aber keinen ersten Besuch. Dies wäre der Fall, wenn der Kunde zuerst Marke A besucht hat und alle weiteren Besuche bei Marke B stattfanden. Da die Daten von Marke A nicht in der Virtual Report Suite enthalten sind, sind alle Informationen über den ersten Besuch – einschließlich der Tatsache, dass er überhaupt stattgefunden hat – nicht in dieser Virtual Report Suite enthalten.

In diesen Szenarien oder in anderen Situationen, in denen ein Teil der Customer Journey außerhalb einer Virtual Report Suite stattfinden kann, empfiehlt Adobe die Verwendung von Multi-Suite-Tagging, so dass Ihre Benutzer nicht verwirrt werden. Mit dem Multi-Suite-Tagging können Sie eine Journey Property-übergreifend in einer globalen Report Suite tracken, aber auch den einzelnen Teams für jede Property einen separaten vollständigen Überblick über die Journey bereitstellen.

## Sie und Ihre Benutzer benötigen keine Ansicht von Transaktionen in verschiedenen Landeswährungen.

Zusammenfassung:

* Virtual Report Suites können derzeit nur die Währung der Report Suite anzeigen, auf der sie basieren.
* Adobe Analytics ermöglicht zwar die Konvertierung der Währung bei der Erstellung von Berichten. Der Wechselkurs ist jedoch der des aktuellen Tages – auch wenn es sich um historische Daten handelt.

Virtual Report Suites können derzeit nur die Währung der Report Suite anzeigen, auf der sie basieren. Wenn Ihr Unternehmen und Ihre Adobe Analytics-Benutzer ihre Analyse in einer einzigen Währung durchführen, verursacht dies kein Problem. Wenn Sie jedoch einen erheblichen Geschäftsbedarf für verschiedene regionale Teams haben, die in der Lage sein müssen, Umsätze und ähnliche Metriken in ihrer eigenen Landeswährung anzuzeigen (die mit dem Wechselkurs zum Zeitpunkt der Datenerfassung umgerechnet wird), sollten Sie Multi-Suite-Tagging verwenden.

Auf diese Weise können Sie Daten in verschiedenen Währungen gleichzeitig an Adobe Analytics senden. Mit Multi-Suite-Tagging kann eine Transaktion, die in der japanischen Version Ihrer App stattfindet, in der globalen Suite in USD erfasst werden. Sie kann zum Tageskurs aus JPY umgerechnet werden, wird aber weiterhin in Ihrer japanischen Report Suite in JPY angezeigt.

>[!NOTE]
>
>Virtual Report Suites ermöglichen es Ihnen nicht, Umsatzdaten zu einer historischen Rate in eine andere Währung umzuwandeln. &gt; Sie können jedoch trotzdem die Währung in einer Virtual Report Suite auf Ad-hoc-Basis konvertieren. Sie können den Wechselkurs " &gt;" des aktuellen Tages auf historische Daten anwenden, indem Sie" Komponenten" &gt; "Berichtseinstellungen" aufrufen.

## Sie können einen einzelnen Daten-Feed verwenden, um alle Ihre Daten aus einer globalen Report Suite zu empfangen.

Zusammenfassung:

* Daten-Feeds können nur basierend auf realen Report Suites erstellt werden, nicht auf Basis von Virtual Report Suites.
* Sie können jedoch einen Feed aus einer globalen Report Suite empfangen und dann nach Marke, Property, Region usw. aufgliedern.

Mit Daten-Feeds erhalten Sie einen täglichen oder stündlichen Export aller Adobe Analytics-Daten auf „Ereignis“- oder „Treffer“-Ebene. Da Daten-Feeds nicht vorsegmentiert werden können, bevor sie Ihnen zugestellt werden, bedeutet die Verwendung einer globalen Report Suite in Kombination mit Virtual Report Suites, dass Sie nur für Ihre globale Report Suite einen Daten-Feed erhalten können. Für Virtual Report Suites können Sie keine Daten-Feeds erstellen.

Sie können jedoch beliebig viele auf realen Report Suites basierende Daten-Feeds einrichten. Nachdem Sie diese Daten-Feeds erhalten haben, können Sie sie segmentieren und beliebig aufteilen. Nachdem Sie beispielsweise einen Daten-Feed für eine globale Report Suite erhalten haben, könnten Sie den Teil dieses Daten-Feeds, der sich auf Ihre Website bezieht, in ein separates Data Warehouse laden. Gleichzeitig könnten Sie den Teil, der sich auf Ihre mobile App bezieht, in ein anderes Data Warehouse laden.

Beachten Sie jedoch, dass einige vorberechnete Felder im Daten-Feed nach dem Empfang möglicherweise neu berechnet werden müssen. Unter Punkt 5 (oben) finden Sie Beispiele von Feldern, die eventuell neu berechnet werden müssen, wenn ein Daten-Feed nach bestimmten Kriterien gefiltert wird.

Wenn Ihr Unternehmen einen ausgeprägten Bedarf an individuellen Daten-Feeds für einzelne Marken, Properties, Regionen usw. hat, können Sie die Verwendung von Multi-Suite-Tagging in Betracht ziehen.

## Sie verwenden keine Exchange-Integration (Data Connectors), die nur ein Partnerkonto pro Report Suite erlaubt, und Sie haben nicht mehrere Partnerkonten, die Sie integrieren möchten.

Zusammenfassung:

* Bestimmte Adobe-Partner-Integrationen in Adobe Analytics sind auf ein Partnerkonto pro Report Suite beschränkt.
* Einige Unternehmen möchten eventuell mehrere Partnerkonten in Adobe Analytics verwenden, was Multi-Suite-Tagging erfordert.

Adobe Exchange ermöglicht die Integration anderer Marketing- und Anzeigentechnologie-Lösungen mit Adobe Analytics. Beispiele für verfügbare Integrationen sind Display-Werbung, E-Mail, VOC und Call Center. Aufgrund von Unterschieden in der Art und Weise, wie Daten erfasst, präsentiert und integriert werden, sind einige Produkte von Adobe-Partnern, die Sie eventuell mit Adobe Exchange verwenden möchten, bei der Integration auf eine einzige Instanz pro Report Suite beschränkt. Jede Instanz wird einem Partnerkonto zugeordnet.

Ein Beispiel hierfür ist Google DCM. Viele Unternehmen haben mehrere DCM-Konten, die verschiedene Marken, Geschäftsbereiche, Regionen usw. betreuen, wodurch die Display-Anzeigen unabhängig voneinander verwaltet werden können. Bei der Integration von DCM mit Adobe Analytics können Sie jedoch nur ein einziges DCM-Konto pro Report Suite verwenden. Sie können nicht alle verschiedenen DCM-Konten in die gleiche Report Suite integrieren. Sie können auch keine direkte Integration in eine Virtual Report Suite einrichten.

Daher ist Multi-Suite-Tagging die empfohlene Methode, wenn verschiedene Teams in Ihrem Unternehmen ihre eigenen Kontodaten in Adobe Analytics für einen Adobe Exchange-Partner benötigen. Wenn Sie eine Adobe Exchange-Integration verwenden (oder verwenden werden), bei der verschiedene Gruppen unterschiedliche Konten verwalten, erkundigen Sie sich beim Adobe-Partner, ob mehrere Konten pro Report Suite zulässig sind.

>[!NOTE]
>
>Der Begriff "Konto" kann verschiedene Dinge für verschiedene Anbieter bedeuten. Im Kontext der Marketingtechnologie bezieht sich dies normalerweise nicht auf ein einzelnes Benutzerkonto, sondern auf eine Reihe von Diensten, die einem &gt; kompletten Team oder einer Organisation zur Verfügung gestellt werden. Wenn Sie also mehrere Benutzernamen haben, die sich bei einem Adobe-Partner anmelden, können &gt; alle diese Benutzernamen zu demselben Konto gehören.

>[!NOTE]
>
>Alle "Vor-Klick" -Metriken (zusammengefasste/aggregierte), die von einem Adobe Exchange-Partner importiert werden, sind nicht &gt; für die Segmentierung verfügbar und werden daher möglicherweise nicht in einer Virtual Report Suite angezeigt. Beispiele für solche Metriken &gt; sind E-Emails oder Display-Anzeigenimpressionen, die beide Offsite/Offapaterial aufrufen und in Adobe &gt; Analytics in einem aggregierten Formular importiert werden.

## Sie hängen nicht stark von Zusammenfassungsdatenquellen in einer Eigenschaft, Marke, Region usw. ab. usw.

Zusammenfassung:

* Mit „Zusammenfassung der Data Sources“ können Sie aggregierte Metriken auf Report Suite-Ebene in Adobe Analytics importieren.
* Der Wechsel zu einer globalen Report Suite mit Virtual Report Suites würde erfordern, dass alle Uploads von „Zusammenfassung der Data Sources“ in der globalen Report Suite stattfinden.

Mit „Zusammenfassung der Data Sources“ können Sie voraggregierte Metriken in eine reale Report Suite in Adobe Analytics importieren. Beispiele für „Zusammenfassung der Data Sources“ sind Metriken wie „Offline-Umsatz“ oder „Seitenansicht“, die in einer anderen Lösung vor der Implementierung von Adobe Analytics entstanden sind. Da Uploads von „Zusammenfassung der Data Sources“ aggregierte Metriken enthalten, können sie nicht segmentiert werden. Folglich werden sie in Virtual Report Suites nicht segmentiert angezeigt.

Multi-Suite-Tagging ermöglicht Ihrem Unternehmen, aggregierte Metriken in einzelne Report Suites zu importieren. Wenn Marke A Offline-Umsätze importieren möchte, kann dies getrennt von Marke B erfolgen. Diese Daten werden dann in der Report Suite von Marke A angezeigt. Marke B könnte dasselbe tun. Wenn Ihr Unternehmen „Zusammenfassung der Data Sources“ für Properties, Marken, Regionen usw. verwendet oder verwenden möchte, sollten Sie Multi-Suite-Tagging anstelle von Virtual Report Suites in Betracht ziehen.

## Schritte, die bei der Verwendung von Virtual Report Suites zu befolgen sind

Hier finden Sie Anweisungen zu den erforderlichen Schritten, wenn Sie die oben stehenden Punkte gelesen und sich entschieden haben, sekundäre Server-Aufrufe zu vermeiden und Virtual Report Suites zu verwenden:

**Erstellen Sie zunächst** Virtual Report Suites, um den Daten in Ihren sekundären/untergeordneten Report Suites zu entsprechen. Segmentieren Sie nach einer benutzerdefinierten Dimension wie „Marke“, „Plattform“, „Domain“. Wählen Sie eine Dimension, mit der eine digitale Property einfach von einer anderen unterschieden werden kann, und wenden Sie diese Segmente auf Virtual Report Suites an.

* Wenn Sie von einer bestehenden Multi-Suite-Tagging-Implementierung in Adobe Analytics migrieren, denken Sie daran, die Segmente der Virtual Report Suites mit Ihren bestehenden untergeordneten Report Suites zu vergleichen, bevor Sie Ihre Benutzer migrieren. Stellen Sie dabei sicher, dass Sie die richtigen Segmente in den Virtual Report Suites verwenden.

* Passen Sie ggf. die Segmente für die Virtual Report Suites an.

* Verwenden Sie als Best Practice möglichst die [Segmentstapelung](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md), sodass Sie ein Segment an einem Ort bearbeiten und es auf alle Virtual Report Suites anwenden können, die dieses Segment verwenden. Möchten Sie beispielsweise eine VRS für „Benutzer von Mobilgeräten in Europa“ und eine weitere für „Benutzer von Mobilgeräten in Asien“ erstellen, erstellen Sie ein Segment für Benutzer von Mobilgeräten und anschließend zwei verschiedene Segmente für Benutzer aus Asien und aus Europa. Möchten Sie später die Definition Ihres „Mobilbenutzersegments“ aktualisieren, müssen Sie dazu nur ein Segment ändern, ohne dass die Einstellungen für die verschiedenen Regionen einzeln angepasst werden müssten.

* Möglicherweise benötigen Sie in Ihren Virtual Report Suites sich gegenseitig ausschließende Datensätze. Beispiel: Sie möchten „Domain A“ und „Domain B“ als separate Report Suites darstellen, möchten aber keinen Traffic von Domain A in der Report Suite von Domain B anzeigen. Verwenden Sie in diesem Fall für Ihre Segmente einen „Treffer“-Container.

**Wenn Sie zweitens**&#x200B;überprüft haben, dass die erstellten Virtual Report Suites richtig eingerichtet wurden und die Anforderungen Ihres Teams erfüllen, entfernen Sie die sekundären Report Suite-IDs aus Ihrer Implementierung.

So entfernen Sie sekundäre Report Suites:

* Klicken Sie in Adobe Experience Platform Launch auf das "x" neben allen Report Suites, die Sie nicht mehr verwenden möchten.
* Suchen Sie in DTM die betreffende Property und das Adobe Analytics-Tool. Entfernen Sie in den Feldern „Produktionskonto-ID“ und „Testkonto-ID“ alle IDs der Report Suite, die nicht mehr verwendet werden sollen.
* In legacy JavaScript implementations, locate the `s.account` variable and remove any report suites that you no longer wish to use.

Behalten Sie nur die IDs der globalen/übergeordneten Report Suites bei, die Daten Ihrer Sites und Apps erfassen. In der Benutzeroberfläche von Adobe Analytics können Sie ältere Report Suites vor Ihren Benutzern verbergen, indem Sie zu Administration &gt; Unternehmenseinstellungen gehen.

Sollte sich die Implementierung nicht bearbeiten lassen, wenden Sie sich an die Kundenbetreuung von Adobe. Sie kann Ihnen dabei behilflich sein, zu verhindern, dass sekundäre Server-Aufrufe von Adobe Analytics verarbeitet werden.