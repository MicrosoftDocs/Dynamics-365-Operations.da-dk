---
title: Manuel afskrivning
description: Denne artikel indeholder en oversigt over den manulle afskrivningsmetode.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3545b863f14ac9553563caa9b6e57443ea378536
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723189"
---
# <a name="manual-depreciation"></a>Manuel afskrivning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over den manulle afskrivningsmetode.

Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Manuel** i feltet **Metode** på siden **Afskrivningsprofiler**, bestemmes den afskrivning, der tildeles afskrivningsprofilen for anlægsaktiver, af den procentdel, du har angivet for hvert interval i kalenderåret. De intervaller, som du angiver procentdele for, bogføres i overensstemmelse med den værdi, du vælger i feltet **Periodefrekvens** i oversigtspanelet **Generelt** på siden **Afskrivningsprofiler**. Her er de værdier, du kan vælge imellem:

- Årligt
- Månedligt
- Kvartalsvis
- Halvårlig
- Dagligt

Når du har valgt periodefrekvensen, skal du klikke på **Manuelle planer** og oprette procentdele for hvert posteringsinterval. De manuelle planer og posteringsintervaller definerer tilsammen afskrivningsbeløbet som vist i eksemplerne senere i denne artikel. Manuel afskrivning beregnes altid som en procentdel af anskaffelsesprisen. Ved manuel afskrivning skal de procentdele, som du angiver for afskrivningsintervallerne, ikke udgøre en samlet procent på 100. Manuel afskrivning er en fleksibel afskrivningsmetode, der ofte bruges til at definere en ekstraordinær afskrivningsprofil på siden **Bøger**, f.eks. en ikke-periodisk afskrivning til et specielt formål (f.eks. skat).

## <a name="examples"></a>Eksempler
Anskaffelsesprisen: 11.000,00 forventet scrapværdi: 1.000,00 I følgende tabel vises de intervaller og procentdele, som du har angivet på siden **Planer for anlægsaktivets afskrivningsprofil**.

| Intervalnummer | Procentdel |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

I følgende tabel vises, hvordan afskrivningen beregnes for hvert interval.

|  Intervalnummer | Beregning af det årlige afskrivningsbeløb | Den bogførte nettoværdi ved intervallets afslutning |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11.000 - 1.000) × 10 % = 1.000                | 10.000 (11.000 - 1.000)                   |
| 2                | (11.000 - 1.000) × 50 % = 5.000                | 5.000 (10.000 - 5.000)                    |
| 3                | (11.000 - 1.000) × 8 % = 800                   | 4.200 (5.000 - 800)                       |

Hvis du vælger **Månedligt** i feltet **Periodefrekvens**, opretter du 12 manuelle planlagte intervaller. I følgende tabel vises afskrivningsbeløbene for de første to intervaller.

| Interval | Afskrivningsbeløb            |
|----------|--------------------------------|
| Januar  | (11.000 - 1.000) × 10 % = 1.000 |
| Februar | (11.000 - 1.000) × 50 % = 5.000 |

Hvis du vælger <strong>Halvårlig</strong> i feltet *<strong><em>Periodefrekvens</em>*</strong>, opretter du to manuelle planlagte intervaller. I følgende tabel vises afskrivningsbeløbene for disse to intervaller.

| Interval    | Afskrivningsbeløb            |
|-------------|--------------------------------|
| 30. juni     | (11.000 - 1.000) × 10 % = 1.000 |
| 31. december | (11.000 - 1.000) × 50 % = 5.000 |

Den samlede procentdel for alle intervaller behøver ikke være 100. Men du modtager en meddelelse, hvis værdien i feltet **Akkumuleret procent** på siden **Planer for anlægsaktivets afskrivningsprofil** ikke er **100**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
