---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (10. september 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303788"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Nyheder eller ændringer i Dynamics 365 for Talent Core HR (10. september 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.138.0**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Tillad bestemt tidspunkter på dagen på anmodninger om fritid (halve dage)

Hvis orlov og fravær er konfigureret, så der sendes fritid i dage, kan du nu også aktivere en halv dag-definition. Derefter, når brugere sender anmodninger om fritid, kan de angive, om de anmoder om den første halvdel eller anden halvdel af dagen.

Denne indstilling er som standard slået fra. For medarbejdere, der anmoder om fritid den første halvdel eller anden halvdel af dagen, skal du slå denne indstilling til i **Orlov og fravær**-området af personaleparametre.

Sikkerhedsrettigheden for denne funktion er Vedligehold personaleparametre.

## <a name="validation-of-leave-and-absence-entries"></a>Validering af orlovs- og fraværsposter

Afhængigt af, hvordan orlov er konfigureret, vil medarbejdere, der forsøger at sende en fritidsanmodning, der er længere end deres arbejdsdag, modtage en advarselsmeddelelse. De bliver med andre ord advaret, hvis de forsøger at tage mere end en hel dag fri på en given dato.

Denne kontrol er altid aktiveret. Medarbejdere, der overstiger dagsgrænsen, der er defineret, modtager hver gang en advarsel i deres fritidsanmodning.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Flere felter til betingelsessætninger i arbejdsgange

Yderligere felter er føjet til betingelsessætninger og pladsholdere for flere arbejdsgange i Core HR.

Følgende felter er føjet til arbejdsgange for løn, fratrædelse og overførsel:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Stilling
- Fagforening
- Afdeling
- PositionType
- CompLocation
- Stilling
- Job
- JobType
- JobFamily
- JobFunction

Følgende felter er føjet til stillingens arbejdsgang:

- Stilling
- Fagforening
- Afdeling
- PositionType
- CompLocation
- Stilling
- Job
- JobType
- JobFamily
- JobFunction

Felterne i betingelsessætninger og pladsholdere er tilgængelige for alle brugere, der har adgang til at konfigurere de tidligere nævnte arbejdsgange.

## <a name="navigation-to-attract-from-personnel-management"></a>Navigation til Attract fra personalestyring

I personalestyring, hvis Attract ikke er konfigureret, vil **Kandidater, der skal ansættes**-afsnittet hjælpe brugerne i gang med Attract i stedet for at vise meddelelsen "Vi fandt ingenting at vise her".

## <a name="other-changes"></a>Andre ændringer

Denne version indeholder flere supplerende fejlrettelser:

- Når en kontrahent ansættes, skal fanen **Kompensation** ikke være tilgængelig på anmodnings-/handlingssiden.
- Du kan ikke fortsætte i processen Anmod om opsigelse, før alle obligatoriske felter indeholder data.
- Problemer med at få vist sorteringsrækkefølge og dato i analyser af Personalestyring er håndteret.
