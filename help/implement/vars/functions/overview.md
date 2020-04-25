---
title: Funktionen und Methoden
description: Erfahren Sie, wie Sie die Funktionen und Methoden verwenden können, die Adobe in Ihrer Implementierung anbietet.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Funktionen und Methoden

Adobe Angebot verschiedene Funktionen und Methoden, die Sie in Ihrer Implementierung verwenden können. Wenn Sie auf diese Funktionen oder Methoden verweisen, führen sie häufige Aufgaben mit einer einzigen Codezeile durch.

Einige dieser einzelnen Codezeilen gehören zu den folgenden Kategorien:

* **Verfolgungsaufrufe**: Die gängigsten Methoden und die wichtigste in vielen Implementierungen. Dazu gehören die [`t()`](t-method.md) und die [`tl()`](tl-method.md) Methoden.
* **AppMeasurement-Dienstprogramme**: In früheren Versionen von AppMeasurement mussten Implementierungen ihren eigenen Code schreiben, um diese Aufgaben durchzuführen. Adobe stellt diese Dienstprogrammmethoden bereit, um diese gängigen Aufgaben zu optimieren. AppMeasurement-Dienstprogramme umfassen [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md)und [`Util.getQueryParam()`](util-getqueryparam.md).
* **Registerfunktionen**: Sie können eigene Funktionen schreiben und AppMeasurement automatisch ausführen lassen, bevor oder nachdem Sie einen Verfolgungsaufruf an Adobe gesendet haben. Variablen, die unter diese Kategorie fallen, sind [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md)und [`registerPostTrackCallback()`](registerposttrackcallback.md).
