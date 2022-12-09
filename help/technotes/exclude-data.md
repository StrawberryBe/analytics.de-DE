---
title: Ausschließen von Daten in Adobe Analytics
description: Lernen Sie verschiedene Methoden kennen, wie Sie Daten sowohl vor als auch nach der Datenerfassung ausschließen können.
exl-id: dee5bf3b-8bb3-48eb-908d-b4a981f17bfb
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 100%

---

# Ausschließen von Daten in Adobe Analytics

Das Ausschließen von Daten wird häufig verwendet, um zu verhindern, dass die Testaktivitäten Ihres Unternehmens in die Produktionsdaten einfließen, oder um zu verhindern, dass unerwünschte Daten die Berichte fälschlicherweise aufblähen. Verwenden Sie eine der folgenden Methoden, um Daten aus Adobe Analytics je nach Anwendungsfall auszuschließen.

## Daten nach der Datenerfassung ausschließen

Mit den folgenden Methoden können Sie Daten im Analytics-Reporting ausschließen, nachdem die Datenerfassungs-Server von Adobe Bildanforderungen empfangen haben. Daten, die mit diesen Methoden ausgeschlossen wurden, werden weiterhin für abrechnungsfähige Server-Aufrufe gezählt.

* **Nach IP ausschließen**: Adobe Analytics bietet grundlegende Funktionen zum Ausschließen von Daten für IP-Adressen oder Bereiche in einer Report Suite. Siehe [Nach IP ausschließen](/help/admin/admin/exclude-ip.md) im Admin-Benutzerhandbuch.
* **Bot-Regeln**: Bot-Regeln nehmen Traffic, der zu bekannten Zeichenfolgen von Bot-Benutzeragenten gehört, und schließen ihn aus Analytics-Berichten aus. Daten, die über Bot-Regeln ausgeschlossen werden, werden im Bots-Bericht platziert. Es können benutzerdefinierte Bot-Regeln erstellt werden, um zusätzliche Daten auszuschließen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).
* **VISTA-Regeln**: Je nach Bedarf Ihres Unternehmens werden Treffer, die Ihren Anforderungen entsprechen, an eine andere Report Suite gesendet, die speziell zum Empfang ausgeschlossener Daten verwendet wird. VISTA-Regeln werden häufig in Bezug auf IP-Adressen verwendet, sind jedoch nicht auf sie beschränkt. Sie können beliebige Dimensionen verwenden, um Daten in Report Suites ein- oder auszuschließen. VISTA-Regeln verursachen zusätzliche Kosten. Nähere Informationen dazu erhalten Sie vom Account Manager Ihres Unternehmens.
* **Ausschluss-Cookies**: Alle Besucher Ihrer Site können sich freiwillig gegen das Tracking in Adobe Analytics entscheiden, indem sie eine für Ihren Tracking-Server spezifische Seite besuchen. Siehe [Implementieren von Abmelde-Links](/help/implement/js/opt-out.md) im Implementierungs-Benutzerhandbuch.

>[!TIP]
>
>Verarbeitungsregeln können keine Daten ausschließen oder Daten an eine andere Report Suite senden. Bestimmte Variablen können jedoch bedingt festgelegt werden und ein Segment kann verwendet werden, um diese Daten vom Reporting auszuschließen.

## Daten vor der Datenerfassung ausschließen

Wenn Sie verhindern möchten, dass bestimmte Treffer die Datenerfassungs-Server von Analytics erreichen, verwenden Sie die Variable [`abort`](/help/implement/vars/config-vars/abort.md). Diese Kennzeichnung verhindert, dass die Bildanforderung gesendet wird. Abrechnungsfähige Server-Aufrufe werden für abgebrochene Bildanforderungen nicht mitgerechnet, da sie keine Datenerfassungs-Server von Adobe erreichen.
