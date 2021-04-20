---
description: Vollständige Subrelationen sind für alle Konversionsberichte aktiviert. So lassen sich beliebige eVar-Elemente weiter aufschlüsseln. Das Menü „Unterteilung nach“ in der Berichtstabelle wurde passend zum standardmäßigen Menü für die Analytics-Berichterstellung gestaltet und sorgt so für ein einheitliches Aussehen.
title: Subrelationen
uuid: ca6df50f-5d4c-4f91-bf27-86ccd01391a2
feature: Reports & Analytics Basics & Analytics Basics
role: Business Practitioner, Administrator
exl-id: 615ed00e-91cd-45de-ae1f-e0d09ff01d26
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 98%

---

# Subrelationen

Vollständige Subrelationen sind für alle Konversionsberichte aktiviert. So lassen sich beliebige eVar-Elemente weiter aufschlüsseln. Das Menü „Unterteilung nach“ in der Berichtstabelle wurde passend zum standardmäßigen Menü für die Analytics-Berichterstellung gestaltet und sorgt so für ein einheitliches Aussehen.

![](assets/subrelations.png)

## Funktionsweise von Subrelationen {#section_5BD862BB74FE411B96B59204520E4631}

Um die Funktionsweise von Subrelationen zu verstehen, stellen Sie sich folgendes Beispiel vor:

1. Ein Benutzer kommt über Kampagne_A auf Ihre Website und landet zunächst auf der Startseite.
1. Der Benutzer sucht nach dem Begriff „Katzen“. Ihm werden die Suchergebnisse angezeigt. eVar1 verfolgt interne Suchbegriffe nach.
1. Der Benutzer meldet sich bei einer Mailingliste an, was von event1 nachverfolgt wird.
1. Ein anderer Benutzer kommt ebenfalls über Kampagne_A auf Ihre Website und landet zunächst auf der Startseite.
1. Dieser Benutzer sucht nach „Kätzchen“. Ihm werden die Suchergebnisse angezeigt (eVar1). Auch er meldet sich bei der Mailingliste an (event1).

Wenn Sie einen Trackingcode-Bericht generieren würden, sähe das Ganze wie folgt aus:

![](assets/subrel_1.png)

Wenn Sie einen eVar1-Bericht generieren würden, sähe das Ganze wie folgt aus:

![](assets/subrel_2.png)

Wenn Sie den Kampagnenbericht in Subrelation zu eVar1 setzen würden, käme folgendes Ergebnis heraus:

![](assets/subrel_3.png)

Wenn Sie den eVar1-Bericht in Subrelation zu Kampagnen setzen würden, käme folgendes Ergebnis heraus:

![](assets/subrel_4.png)

Wegen der Beständigkeit von Konversionsvariablen werden eVar-Werte in zwei Datenspalten gespeichert: der Wert, der ausgelöst wird, und der Wert, der bestehen bleibt. Wenn Sie einen Rohdatenexport für dieses Beispiel ansehen würden, sähe er wie folgt aus (vereinfachte Darstellung):

![](assets/subrel_5.png)

Unser Backend funktioniert, indem post_campaign und post_evar1 die in Kampagne und evar1 festgelegten Werte beibehalten können. Subrelationsberichte berücksichtigen ausdrücklich nur die Treffer, die Erfolgsereignisse enthalten (Zeilen, die hellgelb hervorgehoben sind). Anschließend erstellen sie die Subrelationsberichte basierend auf den fortbestehenden Werten (in diesem Fall: post_campaign und post_evar1; Zellen hellgelb hervorgehoben).

Zusammenfassend führen Subrelationen folgende Schritte aus, um den Bericht zu erstellen:

* Isolieren der Bildanforderungen, die die Erfolgsereignisse beinhalten, die Sie im Bericht anzeigen.
* Ausgeben der beibehaltenen Werte aller in der Subrelation verwendeten Konversionsvariablen.
* Organisieren der Werte basierend auf der Reihenfolge der Subrelation. Wenn eine Variable keinen fortbestehenden Wert enthält (wenn beispielsweise eine eVar nie definiert wurde oder abgelaufen ist), wird sie unter „Keine“ gespeichert.
