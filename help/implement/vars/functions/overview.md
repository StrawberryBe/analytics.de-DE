---
title: Funktionen und Methoden
description: Erfahren Sie, wie Sie die Funktionen und Methoden verwenden können, die Adobe in Ihrer Implementierung anbietet.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 100%

---


# Funktionen und Methoden

Adobe bietet verschiedene Funktionen und Methoden an, die Sie bei Ihrer Implementierung verwenden können. Wenn Sie auf diese Funktionen oder Methoden verweisen, führen diese gewöhnliche Aufgaben mit einer einzelnen Codezeile aus.

Einige dieser Codezeilen gehören zu folgenden Kategorien:

* **Tracking-Aufrufe**: Die gängigsten Methoden und in vielen Implementierungen besonders wichtig. Dazu gehören die Methoden [`t()`](t-method.md) und [`tl()`](tl-method.md).
* **AppMeasurement-Dienstprogramme**: In früheren Versionen von AppMeasurement mussten Implementierungen ihren eigenen Code schreiben, um diese Aufgaben durchzuführen. Adobe stellt diese Dienstprogrammmethoden bereit, um diese gängigen Aufgaben zu optimieren. AppMeasurement-Dienstprogramme umfassen [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md) und [`Util.getQueryParam()`](util-getqueryparam.md).
* **Registrierfunktionen**: Sie können eigene Funktionen schreiben und von AppMeasurement automatisch ausführen lassen, bevor oder nachdem Sie einen Tracking-Aufruf an Adobe senden. Variablen, die unter diese Kategorie fallen, sind [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md) und [`registerPostTrackCallback()`](registerposttrackcallback.md).
