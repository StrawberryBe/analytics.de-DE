---
description: Virtual Report Suites segmentieren die Adobe Analytics-Daten, sodass der Zugriff auf die einzelnen Segmente gesteuert werden kann.
title: Virtual Report Suites – Übersicht
uuid: 51c63c56-dd58-4c23-a997-ea6942480d22
translation-type: ht
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: ht
source-wordcount: '789'
ht-degree: 100%

---


# Virtual Report Suites – Übersicht

Virtual Report Suites segmentieren die Adobe Analytics-Daten, sodass der Zugriff auf die einzelnen Segmente gesteuert werden kann.

Bei vielen Kunden fließen Daten in eine globale Report Suite aber auch in kleinere Report Suites. In diesem Fall legen sie eine Variable für mehrere Report Suites fest und senden ihre Daten an mehrere Report Suites. Die Bezeichnung dafür lautet *Multisuite-Taggen* oder *zugrunde liegende/übergeordnete Report Suites*.

Beispielsweise können Sie alle Daten in einer einzelnen Report Suite erfassen, aber anschließend Report Suites einrichten, sodass die Personen in Ihrem Unternehmen Zugriff auf einen Teil der Daten haben, jedoch nicht auf alle. Die Daten können nach Region eingeteilt werden. Möglicherweise verwenden Sie für verschiedene Länder unterschiedliche Websites. Weitere Beispiele sind spezielle Marken, die zwar zu einem größeren Unternehmen gehören, aber jeweils über ein eigenes Marketingteam verfügen.

Mithilfe einer *Virtual Report Suite* (VRS) können Sie dieses Verzweigungskonzept reproduzieren, indem Sie anstelle von mehreren Report Suites Segmente verwenden. Die Daten werden an eine Report Suite gesendet und anschließend nach Segmenten aufgeteilt. Anhand des Beispiels mit mehreren Marken können Sie für die Marke, zu der ein Element gehört, eine Eigenschaft einrichten. Mithilfe von Segmenten können Sie einen Bericht zu den Elementen erstellen, die den einzelnen Eigenschaften zugewiesen sind. Alle diese Segmente erhalten eine eigene Ansicht, wobei gewissermaßen eine neue Report Suite erstellt wird. Es werden keine Daten an das jeweilige Segment gesendet, sondern nur an die globale Report Suite. Sie funktioniert jedoch in Ihren Berichten wie eine andere Report Suite.

Eine Virtual Report Suite erbt die meisten Service-Levels der zugrunde liegenden Report Suite, wie die eVar-Einstellungen, Verarbeitungsregeln, Classifications usw. Die folgenden Einstellungen werden NICHT vererbt:

* Report Suite-ID (RSID)
* Name der Report Suite
* Berechtigungsgruppen (Virtual Report Suites können eigenen Berechtigungsgruppen zugewiesen werden.)

## Vorteile von Virtual Report Suites {#section_3420422FE6DF46EAB151FD9442AAFDC4}

Die Kunden zahlen für sekundäre Serveraufrufe, sodass eine Eliminierung dieser Aufrufe zu deutlichen Einsparungen führen kann. Eine Virtual Report Suite ist zudem vollständig retroaktiv. Wenn die globale Report Suite bereits Daten enthält, werden die relevanten Daten automatisch in eine neue Virtual Report Suite einbezogen. Eine neue sekundäre Report Suite beginnt erst nach ihrer Erstellung mit dem Erfassen von Daten, sodass sie keine historischen Daten beinhaltet. Beim Implementieren von Analytics müssen Sie lediglich Daten an eine Report Suite senden, anstatt Implementierungen für die globale Report Suite und alle sekundären Report Suites erstellen zu müssen.

Virtual Report Suites sind für Folgendes hilfreich:

* Vereinfachung der Implementierung, weil Sie nur eine einzige Report Suite-ID (RSID) für alle Sites/Domänen verwenden können. Da sich alle Daten in einer einzigen Report Suite befinden, werden mit der nächsten Generation von Adobe Analytics Kundenanalysen möglich.
* Geschäftliche Benutzer in Ihrer Organisation sehen immer nur die für sie relevanten Datensegmente.
* Verbesserung der Sicherheit, da Administratoren nach der Implementierung den Datenzugriff einfacher kontrollieren und genauer steuern können.
* Nutzungsmöglichkeit der Co-op-Funktion des Geräts
* Metrik für Personen
* Einzelkundenansicht der Daten (künftig)
* Möglichkeit zur Erstellung unbegrenzter Virtual Report Suites zum Segmentieren von Daten

## Einschränkungen von Virtual Report Suites {#section_F22A6DEBDC9848429E446F4CC2C4EEDE}

Virtual Report Suites haben die folgenden Einschränkungen:

* Die Einschränkungen von Segmenten gelten auch für Virtual Report Suites

   Eine Virtual Report Suite ist lediglich ein Segment, das auf eine Report Suite angewendet wird. Da alle Report Suites über ein eigenes Data Warehouse und einen eigenen Datenfeed verfügen, führt die Verwendung mehrerer Report Suites zu einigen Vorteilen, die Segmente nicht bieten können.
* Echtzeitbericht
* Einstellungen und Variablennamen können nicht wie bei einer vollständigen Report Suite angepasst werden

## Virtual Report Suites vs. Multisuite-Taggen {#section_317E4D21CCD74BC38166D2F57D214F78}

| Funktion | Virtual Report Suite | Multisuite-Taggen |
|--- |--- |--- |
| Bietet Berichte mit Echtzeit- oder aktuellen Daten | Nein | Ja |
| Funktioniert in allen Analytics-Tools (Analysis Workspace, Report Builder usw.) | Ja. **Hinweis:** Diese können nur in Reports &amp; Analytics als Virtual Report Suites identifiziert und bearbeitet werden. Sie können in den anderen Tools jedoch in den Dropdown-Listen für Report Suites ausgewählt werden. | Ja |
| Hochladen von Daten (über Classifications, Datenfeeds usw.) | Nein | Ja |
| Unterstützt die Erstellung von DL-Berichten, Lesezeichen, Dashboards, Zielgruppen, Warnhinweisen, Segmenten, berechneten Metriken... | Ja | Ja |
| Kann einzeln zu Berechtigungsgruppen hinzugefügt werden | Ja | Ja |
| Kann Admin-Funktionen verwenden, um einzelne Einstellungen für diese Report Suite zu ändern (Admin > Report Suites) | Nein (Einstellungen werden von der übergeordneten Report Suite geerbt.) | Ja |

## Kombinieren von Virtual Report Suites und Multi-Suite-Tagging {#section_026FA3FCD7314DD18220E73EC5702AFF}

In einigen Fällen hat die Verwendung von Virtual Report Suites und des Multi-Suite-Taggens Vorteile.

Ein Einzelhändler kann beispielsweise eine Report Suite für jede Marke und Virtual Report Suites für die einzelnen Marken verwenden, um die Daten nach Region aufzuschlüsseln. Gleichermaßen kann eine Sportorganisation eine Report Suite für jedes Team verwenden und anschließend mithilfe von Virtual Report Suites die Fans in der Region der Teams von denen außerhalb der Region trennen.
