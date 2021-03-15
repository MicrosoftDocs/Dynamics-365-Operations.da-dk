---
title: Konfigurere en enhed til at køre grænsefladen på produktionsudstyr
description: Grænsefladen til kørsel af produktionsudstyr konfigureres for alle enheder i produktionen. Virksomheder konfigurerer typisk hver enhed forskelligt, afhængigt af formålet med enheden. Et firma kan f.eks. have én enhed i modtagelsesområdet, hvor arbejderne stempler ind og ud, når de kommer og går, og et andet i produktionen, hvor arbejderne administrerer deres job.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d4529af21d9673512889b17aeb1e7fbd49969cdc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966267"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Konfigurere en enhed til at køre grænsefladen på produktionsudstyr

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Grænsefladen til kørsel af produktionsudstyr konfigureres for alle enheder i produktionen. Virksomheder konfigurerer typisk hver enhed forskelligt, afhængigt af formålet med enheden. Et firma kan f.eks. have én enhed i modtagelsesområdet, hvor arbejderne stempler ind og ud, når de kommer og går, og et andet i produktionen, hvor arbejderne administrerer deres job.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Indstille konfiguration og filtre for en bestemt enhed

Når du vil indstille konfigurations- og jobfiltre for en enhed, skal du logge på siden til **Kørsel af produktionsudstyr** ved hjælp af en konto med en sikkerhedsrolle, der omfatter pligten *Supervisor for vedligeholdelse af tid*. (Blandt de indbyggede sikkerhedsroller er det kun *Shop floor-supervisor*, der har denne pligt). Følg derefter disse trin.

1. Gå til den enhed, du vil konfigurere, og log på Microsoft Dynamics 365 Supply Chain Management som shop floor-supervisor. (Brug en konto, der omfatter pligten *Supervisor for vedligeholdelse af tid*).
1. Kontroller, at der er en konfiguration tilgængelig for den enhed, du konfigurerer. Hvis der ikke allerede findes en konfiguration, bliver der leveret en standardkonfiguration. Du kan finde flere oplysninger om, hvordan du kan konfigurere en konfiguration, under [Konfigurere grænsefladen til kørsel af produktionsudstyr](production-floor-execution-configure.md).
1. Gå til **Produktionsstyring \> Produktionsudførelse \> Kørsel af produktionsudstyr**.

    Hvis grænsefladen til kørsel af produktionsudstyr allerede er konfigureret mindst én gang på den aktuelle enhed, vises en logonside. Ellers vises en velkomstside.

1. Vælg **Konfigurer** på logonsiden eller velkomstsiden.
1. Vælg en konfiguration på listen.
1. Vælg **Næste**.
1. Vælg et eller flere filtre, der skal anvendes på den aktuelle enhed. Disse filtre vil være med til at sikre, at der kun vises relevante job på enheden. Hvis du vil angive et filter, skal du vælge filtertypen for at åbne en liste over værdier og derefter vælge den værdi, der skal filtreres efter. Følgende filtre er tilgængelige:

    - **Produktionsenhed** – Dette er filteret på højeste niveau. Det henviser typisk til et stort arbejdsområde med flere ressourcegrupper og individuelle ressourcer.
    - **Ressourcegruppe** – Dette er et filter på mellemniveau. Det refererer typisk til en samling relaterede ressourcer i et begrænset område af arbejdsområdet. Hvis du vælger et **Produktionsenhed**-filter først, viser listen over ressourcegrupper kun grupper fra denne enhed. Ellers vises alle tilgængelige ressourcegrupper.
    - **Ressource** – Dette er det mest specifikke filter. Den henviser typisk til en bestemt maskine eller en anden enkelt ressource. Hvis du vælger et **Ressourcegruppe**- og/eller et **Produktionsenhed**-filter først, viser listen over ressourcer kun ressourcer fra denne gruppe og/eller enhed. Ellers vises alle tilgængelige ressourcer.

1. Vælg **OK**.
1. Logonsiden vises, og enheden er klar til brug.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Tillade, at en arbejder tilsidesætter standardfiltrene

Du kan give bestemte arbejdere tilladelse til at ændre filterindstillingerne på en hvilken som helst enhed, de bruger. For arbejdere, der har denne tilladelse, indeholder produktionsudstyrets kørselsgrænseflade knappen **Filter** på siderne **Alle job** og **Aktive job**.

> [!NOTE]
> Hvis en arbejder ændrer et filter, anvendes det nye filter fremadrettet for alle de brugere, der logger på enheden.

Udfør følgende trin for at give en arbejder mulighed for at tilsidesætte de standardjobtyper, der er konfigureret for en enhed.

1. Gå til **Tid og fremmøde \> Opsætning \> Arbejdere, der registrerer tid**.
1. Vælg en arbejder på listen for at åbne arbejdernes side **Arbejdere, der registrerer tid**.
1. Under fanen **Tidsregistrering** skal du indstille **Angiv filtre** til *Ja*.

## <a name="run-the-interface-in-full-screen-mode"></a>Køre grænsefladen i fuldskærmstilstand

Ofte vil du køre grænsefladen til kørsel af produktionsudstyr på en enhed, der udelukkende bruges til dette formål. Det kan derfor være en god ide at køre grænsefladen i fuldskærmstilstand, uden at der vises navigation og/eller browseren Chrome.

- Hvis du vil skjule den navigationsrude, der vises i Supply Chain Management, skal du tilføje følgende tekst i slutningen af URL-adressen i browserens adresselinje: `\&limitednav=true`.
- Hvis du også vil skjule browserens adresselinje, skal du bruge browserens indbyggede fuldskærmstilstand. Yderligere oplysninger finder du i dokumentationen til browseren.

Den øverste del af nedenstående illustration viser, hvordan grænsefladen ser ud som standard. Den nederste del viser, hvordan den ser ud i fuldskærmstilstand, når navigationsruden er skjult.

![Standardgrænseflade i forhold til fuldskærmsgrænseflade](media/pfei-full-screen.png "Standardgrænseflade i forhold til fuldskærmsgrænseflade")

## <a name="extend-the-session-past-12-hours"></a>Udvide sessionen ud over de seneste 12 timer

Som standard bliver grænsefladen til kørsel af produktionsudstyr automatisk logget af, hvis ingen bruger den i 12 timer. En bruger af Supply Chain Management skal derefter logge på igen. Du kan dog forlænge timeoutgrænsen til op til 90 dage.

Hvis du vil forlænge grænsen for timeout, skal du logge på Supply Chain Management og gå til **Systemadministration \> Brugere \> Sessionsudvidelser**. Angiv den Supply Chain Management-brugerkonto, der bruges til at logge på enheden, og det antal timer, som sessionen skal være aktiv i.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]