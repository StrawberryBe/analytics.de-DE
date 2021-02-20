---
title: Daten in Adobe Analytics ausschließen
description: Erfahren Sie, wie Sie Daten sowohl vor als auch nach der Datenerfassung ausschließen.
translation-type: tm+mt
source-git-commit: 47b14bde1bb1217bcb172c6d4f01d68f917d44db
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---


# Daten in Adobe Analytics ausschließen

Das Ausschließen von Daten wird häufig verwendet, um zu verhindern, dass die Testbemühungen Ihres Unternehmens Produktionsdaten ausfüllen oder um zu verhindern, dass unerwünschte Daten fälschlicherweise Berichte aufblähen. Verwenden Sie eine der folgenden Methoden, um Daten aus Adobe Analytics je nach Anwendungsfall auszuschließen.

## Datennachdatenerfassung ausschließen

Mit den folgenden Methoden können Sie Daten in Analytics Berichte ausschließen, nachdem die Datenerfassungsserver der Adobe Bildanforderungen empfangen haben. Daten, die mit diesen Methoden ausgeschlossen wurden, werden weiterhin für abrechnungsfähige Server-Aufrufe gezählt.

* **Nach IP** ausschließen: Adobe Analytics bietet grundlegende Funktionen zum Ausschließen von Daten für IP-Adressen oder Bereiche in einer Report Suite. Siehe [Nach IP ausschließen](/help/admin/admin/exclude-ip.md) im Admin-Benutzerhandbuch.
* **Bot-Regeln**: Bot-Regeln nehmen Traffic von bekannten Bot-Benutzeragenten-Zeichenfolgen auf und schließen sie aus Analytics-Berichten aus. Daten, die über Bot-Regeln ausgeschlossen werden, werden im Bots-Bericht platziert. Benutzerdefinierte Bot-Regeln können erstellt werden, um zusätzliche Daten auszuschließen. Siehe [Bot Rules](/help/admin/admin/bot-removal/bot-rules.md) im Admin-Benutzerhandbuch.
* **VISTA-Regeln**: Je nach Bedarf Ihres Unternehmens werden Treffer, die Ihren Anforderungen entsprechen, an eine andere Report Suite gesendet, die zum Empfang ausgeschlossener Daten verwendet wird. VISTA-Regeln werden häufig gegen IP-Adressen verwendet, sind jedoch nicht auf sie beschränkt. Sie können beliebige Dimensionen verwenden, um Daten in Report Suites einzuschließen oder auszuschließen. VISTA-Regeln unterliegen zusätzlichen Kosten; Nähere Informationen erhalten Sie vom Kundenbetreuer Ihres Unternehmens.
* **Ausschluss-Cookies**: Alle Besucher Ihrer Site können freiwillig Opt-out, in Adobe Analytics verfolgt zu werden, indem sie eine für Ihren Tracking-Server spezifische Seite besuchen. Siehe [Implement opt-out links](/help/implement/js/opt-out.md) im Implementierungs-Benutzerhandbuch.

>[!TIP]
>
>Verarbeitungsregeln können keine Daten ausschließen oder Daten an eine andere Report Suite senden. Bestimmte Variablen können jedoch bedingt festgelegt werden, und ein Segment kann verwendet werden, um diese Daten vom Berichte auszuschließen.

## Daten vor der Datenerfassung ausschließen

Wenn Sie verhindern möchten, dass bestimmte Treffer Analytics-Datenerfassungsserver erreichen, verwenden Sie die Variable [`abort`](/help/implement/vars/config-vars/abort.md). Dieses Flag verhindert, dass die Bildanforderung gesendet wird. Abrechnungsfähige Serveraufrufe werden für abgebrochene Bildanforderungen nicht inkrementiert, da sie keine Datenerfassungsserver der Adobe erreichen.
