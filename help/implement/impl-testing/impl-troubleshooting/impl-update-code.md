---
description: Für Änderungen am Analytics-Code kann Adobe einige Best Practices empfehlen.
keywords: Analytics-Implementierung
seo-description: Für Änderungen am Analytics-Code kann Adobe einige Best Practices empfehlen.
seo-title: Ersetzen Ihres Analytics-Codes
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Ersetzen Ihres Analytics-Codes
topic: Entwickler und Implementierung
uuid: d 3 ea 6585-199 f -4 dbe -9 ee 8-15 b 204689 f 2 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Ersetzen Ihres Analytics-Codes

Für Änderungen am Analytics-Code kann Adobe einige Best Practices empfehlen.

Kunden setzen häufig Adobe [!UICONTROL Code-Manager] ein, um ihren Code durch die neueste Version auszutauschen. Das ist eine geeignete Vorgehensweise, sofern man dabei einige Punkte beachtet.

## Verwendung einer falschen Datenerfassungs-Server-ID {#section_1726CEB1ABEC408492569B06664410C8}

Manchmal werden Entwicklern, die den Code auf einer Website implementieren sollen, gewöhnliche [!DNL s_code.js]-Dateien übergeben, die nicht aus dem Adobe Code-Manager stammen. Das hat zur Folge, dass eine falsche Erfassungs-Server-ID (wie in der Variablen [!UICONTROL s.dc] angezeigt) verwendet wird. Neuer Code sollte am besten direkt aus dem [!UICONTROL Code-Manager] für eine bestimmte Report Suite generiert werden, anstatt den vorhandenen Code einer anderen Report Suite wiederzuverwenden. So lässt sich optimal sicherstellen, dass die Variable [!UICONTROL s.dc] korrekte Werte enthält.

## Plug-ins {#section_53650E52D6A54A4795F95E491E7548D1}

Manche Kunden implementieren Plug-ins, um ihre Adobe-Produkte zu erweitern. Wenn Sie Code austauschen, sollten Sie immer daran denken, dass zu diesem Code auch Plug-ins gehören. Da der über den [!UICONTROL Code-Manager] erstellte Code keinen Plug-in-Code enthält, müssen alle vorhandenen Plug-ins manuell zur neuen Codebasis migriert werden. Fertigen Sie eine Kopie Ihres vorhandenen Codes an, damit Sie über eine Sicherheitskopie verfügen, falls Sie zu Ihrem vorherigen Code wieder zurückwechseln möchten.
