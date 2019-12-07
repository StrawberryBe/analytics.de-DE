---
description: In der folgenden Tabelle sind Beispiele zu korrektem und fehlerhaftem Code aufgeführt.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Häufige Syntaxfehler
topic: Developer and implementation
uuid: 9845dcb9-9f10-4f65-a43d-2af41edaa122
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Häufige Syntaxfehler

In der folgenden Tabelle sind Beispiele zu korrektem und fehlerhaftem Code aufgeführt.

| Falsch | Richtig |
|---|---|
| prop1 | s.prop1 (verwendet „s.“) |
| s.evar1 | s.eVar1 (verwendet korrekte Großschreibung) |
| s.pagetype='errorpage'; | s.pageType='errorPage'; (verwendet korrekte Großschreibung) |
| s.tl(this,o,pageA) | s.tl(this,'o','pageA'); (korrekter Einsatz von einfachen Anführungszeichen) |
| s.events='event1'; s.events='event2'; | s.events='event1,event2'; (korrektes Format) |
| s.pageName="John" (intelligente Anführungszeichen aktiviert) | s.pageName="John" (intelligente Anführungszeichen deaktiviert) |
| s.products="shoes,UX4879,1,19.99" | s.products="shoes;UX4879;1;19.99" (verwendet Semikolons, keine Kommas) |
| s.products=";MacBook Air;1;$1999.99" | s.products=";MacBook Air;1;1999.99" (keine Verwendung des Dollarsymbols) |
| s.products=";Nikon SB-600 Speedlight Flash for Nikon Digital SLR Cameras;1;229.9489183" | s.products=";Nikon SB-600 Speedlight Flash for Nikon Digital SLR Cameras;1;229.95" (lange Preise runden oder abschneiden) |
| var s_account="rsid1, rsid2" | var s_account="rsid1,rsid2" (kein Leerzeichen zwischen Report Suite-IDs beim Multi-Suite-Tagging) |
| s.events="event1, event2" | s.events="event1,event2" (kein Leerzeichen zwischen Ereignis-IDs beim Multi-Suite-Tagging) |
| s.products="product name" | s.products=";product name" (Verwendung von Semikolon, wenn keine Produktkategorie angegeben ist) |

## Weitere Hinweise {#section_E2B6A9C966AD40A09578DD0F784DCAB9}

Löschen Sie nicht die abschließenden HTML-Kommentare am Ende des Adobe-Codes (auch nicht, wenn Sie den NOSCRIPT-Teil dieses Skripts verwenden).
