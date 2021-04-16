---
description: Ein Veröffentlichungs-Widget ist ein Container, mit dem Sie Marketing-Berichte (nur Lesezeichen und Dashboards) in Webseiten einbetten können. Personen in Ihrem Unternehmen, die keinen Zugriff auf Marketing-Berichte haben, können damit die entsprechenden Daten betrachten.
title: Veröffentlichungs-Widget
feature: Admin Tools
uuid: 4ecf6a5a-8a4e-4707-b282-39890eba3c5d
exl-id: 97ec07d8-29ad-4ef3-9227-bfdc14a59b97
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 100%

---

# Veröffentlichungs-Widget

Ein Veröffentlichungs-Widget ist ein Container, mit dem Sie Analytics-Berichte (Lesezeichen und Dashboards) in Webseiten einbetten können. Personen in Ihrer Organisation, die keinen Zugriff auf Analytics-Berichte haben, können damit die entsprechenden Daten betrachten.

Sie können beispielsweise ein Dashboard bereitstellen, damit Führungskräfte des Unternehmens die Anzahl der Seitenbesucher, die Anzahl der Einzelseitenbesucher usw. einsehen können.

>[!CAUTION]
>
>Zum Anzeigen von Daten, die über das Veröffentlichungs-Widget veröffentlicht werden, ist keine Authentifizierung erforderlich. Die veröffentlichten Daten sind daher nicht stärker geschützt als Daten, die Sie an eine E-Mail-Gruppe oder an einen Listenserver senden. Beachten Sie beim Verwenden des Widgets die Sicherheitsvorschriften Ihres Unternehmens, bestehende vertragliche Verpflichtungen und die einschlägigen Gesetze. Das Veröffentlichungs-Widget bietet die Möglichkeit, die Veröffentlichung von Daten nach IP-Adresse oder Domänenpfad einzuschränken. Diese Mechanismen dienen jedoch ausschließlich dem Zweck, eine unbeabsichtigte Datenverbreitung zu verhindern; sie stellen kein wirksames Verfahren dar, den Zugriff auf Daten, die über das Veröffentlichungs-Widget verbreitet werden, abzusichern.
>
> Adobe lehnt jegliche Verantwortung oder Haftung für über das Veröffentlichungs-Widget offengelegte Daten ab.

Da Veröffentlichungs-Widgets potenziell zu hohem Traffic-Aufkommen führen, behält sich Adobe das Recht vor, nach eigenem Ermessen die Veröffentlichungs-Widgets eines Unternehmens zu deaktivieren, wenn unsachgemäße Nutzung oder übermäßiges Datenaufkommen zu Leistungsbeeinträchtigung führen.

## Fehlerbehebung – Cache des Veröffentlichungs-Widgets

Das Widget führt den Bericht aus, wenn ein beliebiger Nutzer erstmalig das bereitgestellte Veröffentlichungs-Widget ansieht. Nach der Ausführung des Berichts werden die Ergebnisse zu einem Cache hinzugefügt und bleiben eine Stunde gültig. Nachfolgende Benutzer, die das Veröffentlichungs-Widget innerhalb der nächsten Stunde ansehen, sehen die gecachete Version (diese wird sofort zurückgegeben). Nach Ablauf einer Stunde erzwingt eine erneute Ansicht durch einen weiteren Benutzer das Veröffentlichungs-Widget zu einer erneuten Ausführung des Berichts, wobei diese Daten zu einem Cache hinzugefügt werden, usw. Auf diese Weise wird sichergestellt, dass die Daten nicht älter als eine Stunde sind.

Wenn Sie Datenunterschiede zwischen dem Veröffentlichungs-Widget und der Berichterstellungsoberfläche feststellen, sollten Sie den Cache des Veröffentlichungs-Widgets löschen.

1. Klicken Sie in das Veröffentlichungs-Widget (damit das Widget im Fokus ist).
1. Klicken Sie im Widget auf **[!UICONTROL Speichern]**.
1. Führen Sie das Widget erneut aus. (Im Vorschaumodus wird der Cache des Widgets nicht verwendet.)

>[!NOTE]
>
>Veröffentlichungs-Widgets zeigen nur die erste Datenspalte eines Berichts an.

## Veröffentlichungs-Widgets – Beschreibungen {#section_D67478AECCA946B19A3E4C7071EB4871}

| Element | Beschreibung |
|--- |--- |
| Name | Der Name für das Widget. |
| Beschreibung | (Optional) Geben Sie eine Beschreibung des Widgets ein. |
| Bericht | Wählen Sie in der oberen Dropdownliste „Bericht“ einen Ordner oder ein Dashboard aus. Wählen Sie in der unteren Dropdown-Liste „Bericht“ ein Reportlet oder ein Lesezeichen aus.  Für diese Berichte ist keine Besucherauthentifizierung erforderlich. <br>Wenn ein Besucher eine Webseite lädt, die ein Veröffentlichungs-Widget enthält, zeigt das Widget den betreffenden Bericht mit aktuellen Berichtsdaten an. Änderungen am Veröffentlichungs-Widget, zum Beispiel die Änderung des zugehörigen Berichts, führen zu einer automatischen Aktualisierung der Berichtsausgabe sämtlicher Webseiten, die das Widget verwenden. Dafür müssen die Webseiten nicht erneut bereitgestellt werden.</br> |
| Ziel | Legen Sie die Zieladresse für das Widget fest.   Das Ziel muss ein gültiges URL-Format aufweisen, einschließlich des Präfix https:// oder https://. Die Ziele von Veröffentlichungs-Widgets sind inklusiv definiert, d. h., das Veröffentlichungs-Widget wirkt sich auf alle URLs aus, die das jeweilige Ziel enthalten. <br>So lässt das Ziel https://www.corp1.com/sales/ beispielsweise Veröffentlichungs-Widgets auf allen Webseiten auf bzw. unterhalb der Seite „sales“ auf der Website www.corp1.com zu.</br> |
