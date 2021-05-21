---
title: Funktionen und Methoden
description: Erfahren Sie, wie Sie die Funktionen und Methoden verwenden können, die Adobe in Ihrer Implementierung anbietet.
exl-id: 9ef5bd92-fae1-4fe4-90ea-c735e8ff4b9c
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '142'
ht-degree: 100%

---

# Funktionen und Methoden

Adobe bietet verschiedene Funktionen und Methoden an, die Sie bei Ihrer Implementierung verwenden können. Wenn Sie auf diese Funktionen oder Methoden verweisen, führen diese gewöhnliche Aufgaben mit einer einzelnen Codezeile aus.

Einige dieser Codezeilen gehören zu folgenden Kategorien:

* **Tracking-Aufrufe**: Die gängigsten Methoden und in vielen Implementierungen besonders wichtig. Dazu gehören die Methoden [`t()`](t-method.md) und [`tl()`](tl-method.md).
* **AppMeasurement-Dienstprogramme**: In früheren Versionen von AppMeasurement mussten Implementierungen ihren eigenen Code schreiben, um diese Aufgaben durchzuführen. Adobe stellt diese Dienstprogrammmethoden bereit, um diese gängigen Aufgaben zu optimieren. AppMeasurement-Dienstprogramme umfassen [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md) und [`Util.getQueryParam()`](util-getqueryparam.md).
* **Registrierfunktionen**: Sie können eigene Funktionen schreiben und von AppMeasurement automatisch ausführen lassen, bevor oder nachdem Sie einen Tracking-Aufruf an Adobe senden. Variablen, die unter diese Kategorie fallen, sind [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md) und [`registerPostTrackCallback()`](registerposttrackcallback.md).
