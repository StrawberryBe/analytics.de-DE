---
description: Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.
seo-description: Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.
seo-title: Unterklassifizierungen und der Rule Builder – Anwendungsfall
solution: Analytics
subtopic: Classifications
title: Unterklassifizierungen und der Rule Builder – Anwendungsfall
topic: Admin Tools
uuid: 6db6a4a9-b93c-413b-8049-1e6cc1ba4a38
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Unterklassifizierungen und der Rule Builder – Anwendungsfall

Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.

## Unterklassifizierungen und der Rule Builder – Anwendungsfall {#concept_6C8672C242544D7487E82886BBFABE6E}

Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.

See [Sub-Classifications](../../../components/c-classifications2/c-sub-classifications.md#concept_19EE5513A7DC43C38CC396E96F306CFE) for conceptual information about sub-classifications.

**Beispiel**: 

Nehmen Sie als Beispiel den folgenden Trackingcode an:

`channel:broad_campaign:creative`

A classification hierarchy allows you to apply a classification to a classification (called *`sub-classification`*). Das bedeutet, Sie können den Importeur wie eine relationale Datenbank mit vielen Tabellen verwenden. In der einen Tabelle werden die vollständigen Trackingcodes Schlüsseln zugeordnet, während in einer anderen Tabelle diese Schlüssel dann anderen Tabellen zugeordnet werden.

![](assets/sub_class_table.png)

Wenn diese Struktur erstellt ist, können Sie den [Classifications Rule Builder](../../../components/c-classifications2/crb/classification-rule-builder.md) nutzen, um die kleinen Dateien hochzuladen, die dann die Suchtabellen (die grüne und rote Tabelle in der Abbildung) aktualisieren. Außerdem können Sie den Classification Rule Builder dazu verwenden, die Haupt-Classification-Tabelle stets auf dem aktuellsten Stand zu halten.

In der folgenden Aufgabe wird beschrieben, wie Sie das machen.

## Set up Sub-Classifications using the Rule Builder{#task_2D9016D8B4E84DBDAF88555E5369546F}

<!-- 

t_rule_builder_subclass.xml

 -->

In diesen Schritten wird beispielhaft beschrieben, wie Sie Unter-Classifications mit Hilfe des Regel-Builder hochladen können.

>[!NOTE]
>
>In diesen Schritten wird beschrieben, wie Sie den unter [Unterklassifizierungen und Regelaufbau](../../../components/c-classifications2/crb/sub-classification-rule-builder.md)beschriebenen Anwendungsfall ausführen.

1. Erstellen Sie Classifications und Unter-Classifications im [Classification-Manager](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html).

   Beispiel:

   ![Schritt-Info](assets/sub_class_create.png)

1. In the [Classifications Rule Builder](../../../components/c-classifications2/crb/classification-rule-builder.md#concept_C1F219E622044D43852EF5168FF7192A), classify the sub-classification key from the original tracking code.

   Verwenden Sie dazu einen regulären Ausdruck. In diesem Beispiel würde die Regel zum Auffüllen von  *`Broad Campaign code`* den folgenden regulären Ausdruck verwenden:

   | `#` | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
   |---|---|---|---|---|
   |  | Regulärer Ausdruck | `[^\:]:([^\:]):([^\:]`) | Code einer breiten Kampagne | `$1` |
   |  | Regulärer Ausdruck | `[^\:]:([^\:]):([^\:]`) | Kreativer Code | `$2` |

   >[!NOTE]
   >
   >At this point, you do not populate the sub-classifications *`Campaign Type`* and *`Campaign Director`*.

1. Laden Sie eine Classification-Datei hoch, die ausschließlich die angegebenen Unter-Classifications enthält.

   Siehe [Mehrstufige Klassifizierungen](../../../components/c-classifications2/c-sub-classifications.md#concept_35AD906CDDC4441DAAF70664CF76AA0A).

   Beispiel:

   | Schlüssel | Kanal | Code einer breiten Kampagne | Code &amp; amp für breite Kampagnen;Hat;Kampagnentyp | Code &amp; amp für breite Kampagnen;Hat;Kampagnenleiter | ... |
   |---|---|---|---|---|---|
   | * |  | 111 | Marke | Suzanne |  |
   | * |  | 222 | Marke | Frank |  |

1. Laden Sie eine kleine Datei (siehe oben) hoch, um die Suchtabellen zu pflegen. 

   You would upload this file, for example, when a new *`Broad Campaign code`* is introduced. Diese Datei würden dann für bereits klassifizierte Werte gelten. Oder wenn Sie eine neue Unter-Classification erstellen (z. B.  Als *`Creative Theme`* Unter-Classification von *`Creative code`*) laden Sie nur die Unter-Classification-Datei hoch und nicht die gesamte Classification-Datei.

   Bei der Berichterstellung funktionieren die Unter-Classifications genauso wie die übergeordneten Classifications. So haben Sie weniger Verwaltungsaufwand, wenn Sie Unter-Classifications verwenden.
