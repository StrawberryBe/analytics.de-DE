---
description: Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.
keywords: Data Feed;page;event;page_event;post_page_event
solution: Analytics
title: Seitenereignissuche
topic: Reports and analytics
uuid: 73af597c-5560-466e-94b2-ddd1d64797c8
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Seitenereignissuche

Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.

| Treffertyp | `page_event` value | `post_page_event` value |
| --- | --- | --- |
| Seitenansichten | 0: Alle Seitenansichtsaufrufe und -aufrufe von `trackState` mobilen SDKs | Gleicher Wert `post_page_event` |
| Linktracking  | 10: Benutzerspezifische Links und `trackAction` Aufrufe in den<br>11 des mobilen SDKs: Download-Links<br>12: Ausstiegslinks | 100: Benutzerspezifische Links und `trackAction` Aufrufe in Mobile SDKs<br>101: Download-Links<br>102: Ausstiegslinks |
| Meilensteinvideo | 31: Medienstart<br>32: Medienaktualisierungen (keine andere Variablenverarbeitung)<br>33: Medienaktualisierungen (mit anderen Variablen) | 76: Medienstart<br>77: Medienaktualisierungen (keine andere Variablenverarbeitung)<br>78: Medienaktualisierungen (mit anderen Variablen) |
| Heartbeat-Video | 50: Medienstream-Start (nicht Primetime)<br>51: Medienstream schließen (Nicht-Primetime)<br>52: Medienstream-Scrubbing (Nicht-Primetime)<br>53: Medienstream am Leben erhalten (Nicht-Primetime)<br>54: Medienstream-Anzeigenstart (nicht Primetime)<br>55: Medienstream-Anzeigenbeendigung (außerhalb von Primetime)<br>56: Medien-Stream-Anzeigen-Scrubbing (Nicht-Primetime)<br>60: Primetime-Medienstream starten<br>61: Primetime-Medienstream schließen<br>62: Primetime-Medien-Stream-Scrubbing<br>63: Primetime-Medienstream am Leben<br>erhalten 64: Primetime-Medienstream und Start<br>65: Primetime-Medienstream und Schließen<br>66: Primetime-Medien-Stream und Scrubbing | Gleicher Wert `post_page_event` |
| Survey | 40: Jeder Aufruf, der aus Survey generiert wurde | 80: Jeder Aufruf, der aus Survey generiert wurde |
| Analytics für Target | 70: Treffer enthält Target-Aktivitätsdaten | Gleicher Wert `post_page_event` |
