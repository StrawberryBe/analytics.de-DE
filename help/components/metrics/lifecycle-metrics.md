---
name: Mobile lifecycle metrics
description: Metriken basierend auf Daten, die mit dem Mobile SDK erfasst wurden.
feature: Metrics
exl-id: 64af4942-d249-47a5-a62f-6051f4c44ee3
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: ht
source-wordcount: '38'
ht-degree: 100%

---

# Lebenszyklusmetriken für Mobile

| Name der Lebenszyklusmetrik | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Erste Starts | | `a.InstallEvent` |
| Upgrades | | `a.UpgradeEvent` |
| Starts | | `a.LaunchEvent` |
| Abstürze | | `a.CrashEvent` |
| Gesamtsitzungslänge | | TBD |
| Aktionsdauer insgesamt | | `a.action.time.total` |
| Aktionsdauer in Anwendung | | `a.action.time.inapp` |
| Lebenszeitwert (Ereignis) | | `a.ltv.amount` |

{style="table-layout:auto"}
