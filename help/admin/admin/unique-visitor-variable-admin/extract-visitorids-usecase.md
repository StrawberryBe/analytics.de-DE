---
description: Data Warehouse verfügt über eine Funktion, mit der Sie eine Liste mit Besucher-IDs extrahieren können. Diese IDs sind keine Cookie-IDs, sondern IDs, die Sie in einer der Konversionsvariablen erfassen. Obwohl diese Informationen auch auf andere Weise erhalten werden können, stellt das folgende Beispiel einen kürzeren Weg zum Generieren einer Data Warehouse-Anforderung dar.
title: Verwendungsfall – Extrahieren von Besucher-IDs
feature: Admin Tools
uuid: ed228334-619c-43d7-b781-a18af73b00bb
exl-id: b1fc41af-31c7-42cd-aab7-0c659577781d
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 100%

---

# Verwendungsfall – Extrahieren von Besucher-IDs

Data Warehouse verfügt über eine Funktion, mit der Sie eine Liste mit Besucher-IDs extrahieren können. Diese IDs sind keine Cookie-IDs, sondern IDs, die Sie in einer der Konversionsvariablen erfassen. Obwohl diese Informationen auch auf andere Weise erhalten werden können, stellt das folgende Beispiel einen kürzeren Weg zum Generieren einer Data Warehouse-Anforderung dar.

Nehmen Sie zum Beispiel einmal an, dass Ihre Firma Marketing-E-Mails an Kunden und Interessenten sendet. Jeder dieser E-Mail-Empfänger hat eine eindeutige ID in Ihrem E-Mail-System (wie z. B. *`EMAIL Contact ID`*). Sie richten Ihre E-Mails so ein, dass Kontakte eine E-Mail erhalten und auf einen darin enthaltenen Link klicken, wobei der Besucher dann mit einer Kampagnen-ID und einer eindeutigen EMAIL-Kontakt-ID auf Ihre Website geleitet wird. Der Link in der E-Mail kann zum Beispiel wie folgt aufgelöst werden:

```js
https://www.test.com/?cid=springmailblast&mid=1363660158
```

Durch Festlegung dieser Links in Konversionsvariablen (eVars) können Sie ermitteln, welche Leistung die einzelnen E-Mails erbracht haben (über die Kampagnen-ID) und wie häufig der Empfänger der E-Mail die Site besucht hat (über die EMAIL-Kontakt-ID).

Nehmen Sie einmal an, dass Sie diese IDs erfassen. Die meisten Anbieter möchten das Verhalten ihrer Website in Segmente aufschlüsseln und dann ermitteln, ob sie ein Remarketing für die Personen erzielen können, die bestimmte Kriterien erfüllen. So möchten Sie zum Beispiel eine Remarketing-E-Mail an alle E-Mail-Empfänger senden, die über die E-Mail auf Ihre Site gelangt sind und dann ein Formular auf der Website angesehen (oder ausgefüllt) haben. Hierzu müssen Sie die EMAIL-Kontakt-IDs der Besucher ermitteln, die das entsprechende Formular ausgefüllt haben.

Eine Möglichkeit besteht darin, einen Konversion-Subrelationsbericht zu verwenden, um den eVar-Wert der Formular-ID nach eVar der EMAIL-Kontakt-ID aufzuschlüsseln. Es steht jedoch auch eine integrierte Funktion zur Verfügung, um dies unter Verwendung Data Warehouse auszuführen. Mit dieser Funktion können Sie angeben, in welcher eVar die eindeutigen Benutzer-IDs (in diesem Fall die EMAIL-Kontakt-ID) gespeichert werden, und Sie können diese IDs mit Hilfe Data Warehouse problemlos extrahieren. Mit dieser Funktion können Sie automatisch eine Data Warehouse-Anforderung erstellen, bei der die Unique Visitor-IDs, die für Sie von Interesse sind, abgerufen werden.
