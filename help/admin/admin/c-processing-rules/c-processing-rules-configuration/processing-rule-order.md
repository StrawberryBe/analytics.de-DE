---
description: Um die Verarbeitungsregeln effektiv nutzen zu können, muss allen Beteiligten klar sein, zu welchem Zeitpunkt der Datenerfassung die Regeln angewendet werden.
seo-description: Um die Verarbeitungsregeln effektiv nutzen zu können, muss allen Beteiligten klar sein, zu welchem Zeitpunkt der Datenerfassung die Regeln angewendet werden.
seo-title: Auftrag wird bearbeitet
solution: Analytics
subtopic: Verarbeitungsregeln
title: Auftrag wird bearbeitet
topic: Admin Tools
uuid: cea 01 d 13-dfd 5-40 f 7-8 b 2 f-b 6 e 2 fe 8354 df
translation-type: tm+mt
source-git-commit: 01ac0011f2e47e6798a520df8ffe5d8393ac0c3c

---


# Auftrag wird bearbeitet

Um die Verarbeitungsregeln effektiv nutzen zu können, muss allen Beteiligten klar sein, zu welchem Zeitpunkt der Datenerfassung die Regeln angewendet werden.

![](assets/analytics_processing_order_test.png)

In den folgenden Tabellen sind die Daten aufgeführt, die in der Regel vor und nach der Anwendung der Verarbeitungsregeln verfügbar sind:

## Vor Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| Suche dynamischer Variablen | Variablen werden dynamisch ausgefüllt, indem Informationen aus HTTP-Kopfzeilen oder anderen Variablen abgerufen werden. For example, `s.eVar5="D=c1"` will put the value of prop1 into eVar5. |
| AppMeasurement | Funktionen und Plugins, die in AppMeasurement genutzt werden, werden im Browser oder der Client-Anwendung ausgeführt. |
| Dynamic Tag Management | Die unter „Dynamic Tag Management“ festgelegten Regeln werden per Definition ausgeführt. |
| Bot Rules | [Mit Bot-Regeln](../../../../admin/admin/bot-removal/bot-rules.md) können Sie Traffic entfernen, der von bekannten Spiders und Bots aus Ihrer Report Suite generiert wird. |

## Nach Verarbeitungsregeln

| Dimension | Beschreibung |
|--- |--- |
| Von VISTA hinzugefügte Daten | Verarbeitungsregeln werden vor VISTA angewendet. |
| Anzahl besuchter Seiten | Im Allgemeinen beziehen sich Verarbeitungsregeln nur auf die im aktuellen Treffer befindlichen Daten. Die Anzahl besuchter Seiten wird nach der Anwendung der Verarbeitungsregeln kompiliert. |
| Falls Seitenname nicht festgelegt ist, wird bereinigte URL-Adresse verwendet | Nachdem die Verarbeitungsregeln und die VISTA-Regeln angewendet wurden, wird die bereinigte URL-Adresse als Seitenname hinzugefügt, insofern kein Seitenname festgelegt wurde. Da dies nach der Anwendung der Verarbeitungsregeln geschieht, sollten Sie mit Hilfe einer Bedingung prüfen, ob die Angabe für den Seitennamen leer ist.  Wenn Sie den Site-Content &gt; Seitenbericht ausführen und Sie https:// Werte für Seitennamen sehen, ist der Seitenname wahrscheinlich leer und die URL wird verwendet. Sie können eine Bedingung einrichten, um zu prüfen, ob der Seitennamen-Eintrag leer ist bzw. ob dieser Eintrag bzw. der Eintrag für die URL-Adresse der Seite einen bestimmten Wert aufweist. Der Seitenname kann anschließend nach Bedarf festgelegt werden. |
| Marketingkanal-Verarbeitungsregeln | Mit Hilfe von Verarbeitungsregeln können Sie Daten für die Verarbeitung mit [Marketingkanal-Regeln](https://marketing.adobe.com/resources/help/en_US/mchannel/index.html?f=c_rules) vorbereiten. |
| GEO-Suche | Dies betrifft die Werte „Bundesstaat des Besuchers“ und „Postleitzahl des Besuchers“. |
| eVars-Speicherung | eVars aus einem vorherigen Treffer werden bei der Regelverarbeitung nicht bei jedem Treffer beibehalten. Es stehen jeweils nur die beim aktuell verarbeiteten Treffer festgelegten eVars zur Verfügung. |

## So werden Verarbeitungsregeln beim Kopieren von Hits mit VISTA angewandt {#section_576EE8C240A24CBA979BD614E8D5338D}

Wenn Sie eine VISTA-Regel zum Kopieren von Hits in eine andere Report Suite konfiguriert haben, werden die Hits über sämtliche in der anderen Report Suite definierten Verarbeitungsregeln versendet.

Wenn Sie Verarbeitungsregeln nutzen, die für die ursprüngliche Report Suite definiert sind, können diese je nachdem angewandt werden, wie die VISTA-Regel durch den technischen Support konfiguriert wurde. Um dies herauszufinden, können Sie Ihren Implementierungsspezialisten fragen, ob die VISTA-Regel die „prä“- oder „post“-Werte in die zusätzliche Report Suite kopiert. Wenn der „prä“-Wert kopiert wird, werden die in der ursprünglichen Report Suite definierten Verarbeitungsregeln nicht angewandt. Wenn der „post“-Wert kopiert wird, werden Verarbeitungsregeln angewandt, bevor der Hit kopiert wird.
