---
description: Ein Veröffentlichungs-Widget ist ein Container, mit dem Sie Marketingberichte (Lesezeichen und Dashboards) in eine Webseite einbetten können. Mitarbeiter in Ihrem Unternehmen, die keinen Zugriff auf Marketing-Berichte haben, können relevante Daten Ansicht haben.
title: Veröffentlichungs-Widget
topic: Admin tools
uuid: 4ecf6a5a-8a4e-4707-b282-39890eba3c5d
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Veröffentlichungs-Widget

Ein Veröffentlichungs-Widget ist ein Container, mit dem Sie Analytics-Berichte (Lesezeichen und Dashboards) in Webseiten einbetten können. Personen in Ihrer Organisation, die keinen Zugriff auf Analytics-Berichte haben, können damit die entsprechenden Daten betrachten.

Sie können beispielsweise ein Dashboard bereitstellen, damit Führungskräfte des Unternehmens die Anzahl der Seitenbesucher, die Anzahl der Einzelseitenbesucher usw. einsehen können.

>[!CAUTION] Zum Anzeigen von Daten, die über das Veröffentlichungs-Widget veröffentlicht werden, ist keine Authentifizierung erforderlich. Die veröffentlichten Daten sind daher nicht stärker geschützt als Daten, die Sie an eine E-Mail-Gruppe oder an einen Listenserver senden. Verwenden Sie das Widget nur unter Einhaltung der Sicherheitsstandards Ihres Unternehmens, der bestehenden vertraglichen Anforderungen und der geltenden Gesetze. Das Veröffentlichungs-Widget bietet die Möglichkeit, die Veröffentlichung von Daten nach IP-Adresse oder Domänenpfad einzuschränken. Diese Mechanismen dienen jedoch ausschließlich dazu, eine unbeabsichtigte Datenverbreitung zu verhindern, und stellen keine effektive Möglichkeit dar, den Zugriff auf über das Veröffentlichungs-Widget verteilte Daten zu sichern.
>
> Adobe übernimmt keine Verantwortung oder Haftung für Daten, die über das Veröffentlichungs-Widget offen gelegt werden.

Da Veröffentlichungs-Widgets potenziell zu hohem Traffic-Aufkommen führen, behält sich Adobe das Recht vor, nach eigenem Ermessen Veröffentlichungs-Widgets einer Firma zu deaktivieren, wenn unsachgemäße Verwendung oder übermäßiges Datenaufkommen zu Leistungsbeeinträchtigung führen.

## Fehlerbehebung – Cache des Veröffentlichungs-Widgets

Wenn ein Benutzer das bereitgestellte Veröffentlichungs-Widget zum ersten Mal anzeigt, wird der Bericht vom Widget ausgeführt. Nach der Ausführung des Berichts werden die Ergebnisse einem Cache hinzugefügt und sind 1 Stunde gültig. Jeder nachfolgende Benutzer, der das Veröffentlichungs-Widget innerhalb der nächsten Stunde Ansicht, sieht die zwischengespeicherte Version (diese wird sofort zurückgegeben). Nach Ablauf einer Stunde zwingt jeder nachfolgende Benutzer, der das Veröffentlichungs-Widget Ansicht, den Bericht erneut auszuführen. Anschließend werden diese Ergebnisse zwischengespeichert usw. Auf diese Weise ist gewährleistet, dass die Daten maximal eine Stunde alt sind.

Wenn Sie Datenunterschiede zwischen dem Veröffentlichungs-Widget und der Benutzeroberfläche des Berichte sehen, müssen Sie möglicherweise den Cache des Veröffentlichungs-Widgets löschen.

1. Klicken Sie auf das Veröffentlichungs-Widget (damit das Widget den Fokus hat).
1. Click **[!UICONTROL Save]** on the widget.
1. Führen Sie das Widget erneut aus. (Im Vorschau-Modus wird der Cache des Widgets nicht verwendet.)

>[!NOTE] Veröffentlichungs-Widgets zeigen nur die erste Datenspalte eines Berichts an.

## Veröffentlichungs-Widgets – Beschreibungen {#section_D67478AECCA946B19A3E4C7071EB4871}

| Element | Beschreibung |
|--- |--- |
| Name | Der Name des Widgets. |
| Beschreibung | (Optional) Geben Sie eine Beschreibung für das Widget ein. |
| Bericht | Wählen Sie in der oberen Dropdown-Liste &quot;Bericht&quot;einen Ordner oder ein Dashboard aus. Wählen Sie in der unteren Dropdown-Liste „Bericht“ ein Reportlet oder ein Lesezeichen aus.  Für diese Berichte ist keine Besucherauthentifizierung erforderlich. <br>Wenn ein Besucher eine Webseite lädt, die ein Veröffentlichungs-Widget enthält, zeigt das Widget den betreffenden Bericht mit aktuellen Berichtsdaten an. Änderungen am Veröffentlichungs-Widget, zum Beispiel die Änderung des zugehörigen Berichts, führen zu einer automatischen Aktualisierung der Berichtsausgabe sämtlicher Webseiten, die das Widget verwenden. Dafür müssen die Webseiten nicht erneut bereitgestellt werden.</br> |
| Ziel | Legen Sie die Zieladresse für das Widget fest.   Das Ziel muss ein gültiges URL-Format aufweisen, einschließlich des Präfix https:// oder https://. Die Ziele von Veröffentlichungs-Widgets sind inklusiv definiert, d. h., das Veröffentlichungs-Widget wirkt sich auf alle URLs aus, die das jeweilige Ziel enthalten. <br>So lässt das Ziel https://www.corp1.com/sales/ beispielsweise Veröffentlichungs-Widgets auf allen Webseiten auf bzw. unterhalb der Seite „sales“ auf der Website www.corp1.com zu.</br> |
