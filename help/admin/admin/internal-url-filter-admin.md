---
description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
seo-description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
seo-title: Interne URL-Filter
solution: Analytics
title: Interne URL-Filter
topic: Admin Tools
uuid: 70868 edb -208 d -4 dad -9401-70967468 d 40 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Interne URL-Filter

Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.

Ein Referrer oder eine verweisende Seite ist normalerweise die Seite, von der aus Besucher Ihre Website aufgerufen haben. Um Datenverzerrungen zu vermeiden, können Sie interne Seiten als Referrer herausfiltern. Berichte schließen gefilterte Referrer aus [Berichte zu verweisenden Stellen](/help/components/c-variables/dimensionslist/reports-referrers.md), [verweisenden Domänen und anderen Suchmethoden](/help/components/c-variables/dimensionslist/reports-referring-domains.md)-Berichten

Der häufigste Grund, aus dem Berichte zu Traffic-Quellen keine Daten enthalten, besteht darin, dass keine interne URL-Filterliste definiert ist. Gehen Sie wie folgt vor, um zu prüfen, welche internen URL-Filter für eine Report Suite festgelegt wurden. Entfernen Sie, um dies zu vermeiden, die Regel, die einen Punkt (.) als Filter enthält und fügen Sie Ihre eigene Site hinzu.

Ein Punkt ist der standardmäßige interne URL-Filter, damit Daten im Bericht „Seiten“ erfasst werden können. Wenn Treffer nicht mit den internen URL-Filtern übereinstimmen, werden alle Seiten als „Sonstige“ eingestuft. Ein Punkt befindet sich immer in der URL und garantiert daher, dass der Bericht „Seiten“ ausgefüllt wird.
