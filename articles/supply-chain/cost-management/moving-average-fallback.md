---
title: Glidende gennemsnit, reserveomkostningssekvens
description: Dette emne indeholder oplysninger om reserveomkostninger til glidende gennemsnitsberegninger i Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 09da3c3a79b5540670db25d5466023132d2848f4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832268"
---
# <a name="moving-average-fallback-cost-sequence"></a>Glidende gennemsnit, reserveomkostningssekvens

Den ene måde, du kan beregne kostprisen på lageret på, er ved at bruge et _glidende gennemsnit_. Du kan knytte op til tre omkostningsværdier til hver lagervare:

- **Sidste afgang** – den sidste afgangsomkostning, der er tildelt, før lageret blev negativt
- **Aktiv omkostning** – De seneste omkostninger, der er aktiveret i en efterkalkulationsversion
- **Varepris** – Den omkostning, der er angivet for det frigivne produkt

Systemet bruger en _reserveomkostningssekvens_ til at fastlægge værdiernes prioritetsrækkefølge for at afgøre, hvilke af disse omkostningsværdier der skal bruges i forbindelse med beregning af det glidende gennemsnit. Hvis værdien for den foretrukne kostpris ikke er tilgængelig, bruger systemet den næste foretrukne værdi osv.

I tidligere versioner af Microsoft Dynamics 365 Supply Chain Management har systemet brugt en fast reserveomkostningssekvens (_Sidste afgang – Aktiv omkostning – Varepris_). I version 10.0.11 er denne sekvens stadig standardrækkefølgen. Du kan dog også slå en funktion til, der giver dig mulighed for at vælge mellem tre tilgængelige reserveomkostningssekvenser. Denne funktion kan især være nyttig for organisationer, der regelmæssigt bruger negative lagerværdier.

Hvis du vil gøre vælgeren for reserveomkostningssekvens tilgængelig, skal du (eller en administrator) bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at slå den funktion til, som hedder _Glidende gennemsnitlig reserveomkostningssekvens_.

Udfør følgende trin for at vælge reserveomkostningssekvensen til beregning af glidende gennemsnit.

1. Åbn siden **Parametre**:
2. Angiv en af følgende værdier i feltet **Reserveomkostningssekvens** på fanen **Lagerregnskab** i afsnittet **Glidende gennemsnit**:

    - **Sidste afgang – Aktiv kostpris – Varepris** – Denne sekvens er standardrækkefølgen. Det er den samme rækkefølge, som bruges, hvis funktionen _Glidende gennemsnit, reserveomkostningssekvens_ ikke er slået til.
    - **Aktiv omkostning – Sidste afgang**
    - **Aktiv kostpris – Varepris** – Organisationer kan opleve problemer med ydeevnen, hvis de bruger forretningsprocesser, hvor lageret regelmæssigt er negativt, og transaktionsmængden samtidigt er høj. Denne indstilling kan hjælpe med at reducere disse ydeevneproblemer.

![Parametre til Lagerregnskab](media/inventory-accounting-parameters.png "Parametre til Lagerregnskab")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]