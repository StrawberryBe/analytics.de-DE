---
description: Vergewissern Sie sich, dass die von Serverskripts oder -code ausgefüllten Variablen keine Anführungszeichen ausgeben können, die zu Konflikten bei den Werten führen.
keywords: Analytics-Implementierung
seo-description: Vergewissern Sie sich, dass die von Serverskripts oder -code ausgefüllten Variablen keine Anführungszeichen ausgeben können, die zu Konflikten bei den Werten führen.
seo-title: Variablen und Werte
solution: Analytics
title: Variablen und Werte
topic: Entwickler und Implementierung
uuid: 2 ff 4857 a -9451-4794-9146-f 417 abd 1 d 1 ba
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Variablen und Werte

Vergewissern Sie sich, dass die von Serverskripts oder -code ausgefüllten Variablen keine Anführungszeichen ausgeben können, die zu Konflikten bei den Werten führen.

Beispiel:

```js
s.pageName="Article: "Article Name"" 
s.pageName='Company's Information' 
```

Stellen Sie sicher, dass die Werte der Variablen keine der im vorliegenden Dokument aufgeführten Grenzwerte überschreiten. Überstehende Zeichen werden bei den Datenerfassungsservern abgeschnitten. Diese könnten andernfalls dazu führen, dass es Probleme im Zusammenhang mit der Gesamtlänge gibt oder dass zu viel Bandbreite belegt wird oder dass sonstige Probleme auftreten.

Verwenden Sie in der Produktvariablen keines der folgenden Zeichen: $, ™, ®, © oder Kommas (,). Diese sind in [!DNL Analytics]-Variablen im Allgemeinen überflüssig und könnten bei der Interpretation von Feldern oder beim Export zu Problemen führen. Als Best Practice wird empfohlen, sich auf die ersten 127 ASCII-Zeichen zu beschränken.

Ensure that the events variable is populated with an appropriate value ( [!UICONTROL prodView], [!UICONTROL purchase], [!UICONTROL scAdd], [!UICONTROL scRemove], [!UICONTROL scOpen], or event1-event5) whenever *`products`* is populated. Achten Sie bei allen [!DNL Analytics]-Variablen und Funktionen auf die richtige Groß-/Kleinschreibung:

```js
s.pageName 
s.server 
s.channel 
s.pageType 
s.prop1 - s.prop20 
s.campaign 
s.state 
s.zip 
s.events 
s.products 
s.purchaseID 
s.eVar1 - s.eVar20 
var s_code=s.t();if(s_code)document.write(s_code)//--> 
```

Bei Seitennamen muss auf die richtige Groß-/Kleinschreibung geachtet werden, andernfalls werden mehrere verschiedene Datensätze angelegt. „Home“ und „home“ sind in [!DNL Analytics] zwei unterschiedliche Seiten.

>[!NOTE]
>
>Mehrere Seitendatensätze können in Berichten nicht kombiniert werden.

Überprüfen Sie, ob Links im Bericht [!UICONTROL Benutzerspezifische Links] aufgeführt werden. Vergewissern Sie sich, dass an die [!UICONTROL tl]-Funktion die richtigen Parameter übergeben werden. Weitere Informationen zu [!UICONTROL benutzerspezifischen Links] finden Sie unter [Linktracking](../../../implement/js-implementation/function-tl.md#concept_EA13689CB8EE4F308FC89A1293046D5E).
