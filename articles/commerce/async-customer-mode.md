---
title: Oprettelsestilstand for asynkron kunde
description: I dette emne beskrives den asynkrone oprettelsestilstand for kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: ca7cceb066d30b7bba82265a3654f3bfb26f57f6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689096"
---
# <a name="asynchronous-customer-creation-mode"></a>Oprettelsestilstand for asynkron kunde

[!include [banner](includes/banner.md)]

I dette emne beskrives den asynkrone oprettelsestilstand for kunder i Microsoft Dynamics 365 Commerce.

Inden for handel findes der to kundeoprettelsesmåder: synkron og asynkron. Kunder oprettes som standard synkront. Det vil sige, at de oprettes i Commerce Headquarters i realtid. Det er en fordel med synkron kundeoprettelsestilstand, fordi nye kunder med det samme kan søges på tværs af kanaler. Det har dog også noget at gøre. Da den genererer [Commerce Data Exchange: Realtidsserviceopkald](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, kan ydeevnen påvirkes, hvis der foretages mange samtidige opkald til oprettelse af kunder.

Hvis indstillingen **Opret kunde i async-tilstand** er angivet til **Ja** i butikkens funktionalitetsprofil (**Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**), bruges Realtidsserviceopkald ikke til at oprette kundeposter i kanaldatabasen. Den asynkrone kundeoprettelsestilstand har ingen indflydelse på Commerce Headquarters-ydeevne. Der tildeles et midlertidigt globalt entydigt id (GUID) til alle nye asynkrone kundeposter, der bruges som debitorkonto-id. Dette GUID vises ikke for brugere af POS. Disse brugere får i stedet vist **Ventende synkronisering** som debitorkonto-id'et.

> [!IMPORTANT]
> Hvis POS skifter til offline, og selvom asynkron kundeoprettelsestilstand er deaktiveret, opretter systemet automatisk kunder asynkront. Uanset dit valg mellem synkron og asynkron kundeoprettelse, skal administratorer af Commerce Headquarters oprette og planlægge et batchjob, der gentages for **P-jobbet**, jobbet **synkroniser kunder og forretningspartnere fra asynkron tilstand** (tidligere kaldet **Synkroniser kunder og forretningspartnere fra jobbet asynkron tilstand**) og jobbet **1010**, så alle asynkrone kunder konverteres til synkrone kunder i Commerce Headquarters.

## <a name="async-customer-limitations"></a>Async-kundebegrænsninger

Funktionaliteten for asynkron kunde har i øjeblikket følgende begrænsninger:

- Async-debitorposter kan ikke redigeres, medmindre kunden er oprettet i Commerce Headquarters, og det nye debitorkonto-id er synkroniseret tilbage til kanalen.
- Fordelskundekort kan ikke udstedes til asynkrone kunder, medmindre det nye debitorkonto-id er synkroniseret tilbage til kanalen.

## <a name="async-customer-enhancements"></a>Forbedringer af asynkrone kunder

Fra og med Commerce version 10.0.24 kan du aktivere funktionen **Forbedret oprettelse af asynkrone kunder** i arbejdsområdet **Funktionsstyring**. Denne funktion bygger bro mellem asynkrone og synkrone kundeoprettelsestilstande i POS og e-handel på følgende måder:

- Tilhørsforhold kan knyttes til asynkrone kunder.
- Titler kan føjes til asynkrone kunder.
- Sekundære mailadresser og telefonnumre kan registreres for asynkrone kunder.

Fra og med Commerce version 10.0.22 kan du aktivere funktionen **Asynkron oprettelse af kundeadresser** i arbejdsområdet **Funktionsstyring**. Med denne funktion kan nyoprettede kundeadresser gemmes asynkront for både synkrone kunder og asynkrone kunder.

Når du har aktiveret ovennævnte funktioner, skal du planlægge et tilbagevendende batchjob til **P-jobbet**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Kundeoprettelse i POS-offlinetilstand

Som nævnt tidligere: Hvis POS skifter til offline, og selvom oprettelsestilstanden for asynkron kunde er deaktiveret, opretter systemet automatisk kunder asynkront. Derfor skal administratorer af Commerce Headquarters oprette og planlægge et tilbagevendende batchjob til **P-jobbet**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce Headquarters.

> [!NOTE]
> Hvis indstillingen **Filtrering af delte kundedatatabeller** er angivet til **Ja** på siden **Commerce channel-skema** (**Retail og Commerce \> Headquarters setup \> Commerce-planlægger \> Kanaldatabasegruppe**), er kundeposter ikke oprettet i POS-offline-tilstand. Du kan finde flere oplysninger under [Offline-dataudelukkelser](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundestyring i butikker](customer-mgmt-stores.md)

[Konvertere asynkrone kunder til synkrone kunder](convert-async-to-sync.md)

[Debitorattributter](dev-itpro/customer-attributes.md)

[Offline-dataudelukkelse](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
