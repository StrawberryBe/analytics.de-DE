---
description: Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.
seo-description: Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.
seo-title: Unter-Classifications und der Regel-Builder - Verwendungsfall
solution: Analytics
subtopic: Classifications
title: Unter-Classifications und der Regel-Builder - Verwendungsfall
topic: Admin Tools
uuid: 6 db 6 a 4 a 9-b 93 c -413 b -8049-1 e 6 cc 1 ba 4 a 38
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Unter-Classifications und der Regel-Builder - Verwendungsfall

Sie können den Classification Rule Builder mit Unter-Classifications kombinieren, um die Classification-Verwaltung zu vereinfachen und die Anzahl der erforderlichen Regeln zu reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.

## Sub-classifications and the Rule Builder - use case {#concept_6C8672C242544D7487E82886BBFABE6E}

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
>These steps describe how to accomplish the use case described in [Sub-Classifications and the Rule Builder](../../../components/c-classifications2/crb/sub-classification-rule-builder.md).

1. Erstellen Sie Classifications und Unter-Classifications im [Classification-Manager](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=classifications).

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

   [Siehe Mehrstufige Klassifizierungen](../../../components/c-classifications2/c-sub-classifications.md#concept_35AD906CDDC4441DAAF70664CF76AA0A).

   Beispiel:

   | Schlüssel | Kanal | Code einer breiten Kampagne | Code und amp einer breiten Kampagne; Hat; Kampagnentyp | Code und amp einer breiten Kampagne; Hat; Kampagnenleiter | ... |
   |---|---|---|---|---|---|
   | * |  | 111 | Marke | Suzanne |  |
   | * |  | 222 | Marke | Frank |  |

1. Laden Sie eine kleine Datei (siehe oben) hoch, um die Suchtabellen zu pflegen. 

   You would upload this file, for example, when a new *`Broad Campaign code`* is introduced. Diese Datei würden dann für bereits klassifizierte Werte gelten. Oder wenn Sie eine neue Unter-Classification erstellen (z. B.  *`Creative Theme`* als Unterklassifizierung von *`Creative code`*), laden Sie statt der gesamten Classification-Datei nur die Unterklassifizierungsdatei hoch.

   Bei der Berichterstellung funktionieren die Unter-Classifications genauso wie die übergeordneten Classifications. So haben Sie weniger Verwaltungsaufwand, wenn Sie Unter-Classifications verwenden.
