---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 0c7093518933a88c5057ba95cb3564d6ca0ebcad

---



# s.forcedLinkTrackingTimeout

Dieser Wert gibt die maximale Wartezeit an. Genauer gesagt wird die maximale Zeit in Millisekunden festgelegt, die auf die Fertigstellung der Verfolgung gewartet wird, bevor die Aktion `doneAction` durchgeführt wird, die an `s.tl` weitergeleitet wurde. Wenn der Verfolgungslink-Aufruf vor dieser Zeitdauer abgeschlossen ist, wird `doneAction` sofort ausgeführt. Wenn Sie bemerken, dass Verfolgungslink-Aufrufe nicht abgeschlossen werden, müssen Sie den Wert für diese Zeitüberschreitung eventuell erhöhen.

Standardwert = 250

Beispiel: `s.forcedLinkTrackingTimeout = 500`
