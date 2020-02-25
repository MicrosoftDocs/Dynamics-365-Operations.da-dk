---
title: Oversigt over administration af frynsegoder
description: Prøveversionsfunktion til oversigt over administration af frynsegoder i Dynamics 365 Human Resources. Tilbyd dine medarbejdere mulighed for ekstra frynsegoder via en brugervenlig onlineoplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029457"
---
# <a name="benefits-management-overview"></a>Oversigt over administration af frynsegoder

[!include [banner](includes/preview-feature.md)]

Hvis du vil forblive konkurrencedygtig, skal du tilbyde en lang række frynsegoder for at tiltrække og holde på dine bedste medarbejdere. Ud over standardfrynsekoder som sundhedsforsikring og tandlægedækning kan det også være en god idé at tilbyde udvidede tjenester som hjælp til adoption, rekreative ordninger og beklædningsgodtgørelse. Prøveversionsfunktionen til Administration af frynsegoder i Microsoft Dynamics 365 Human Resources giver dig en fleksibel løsning, som understøtter en lang række frynsegodemuligheder. Personale inkluderer også en brugervenlig medarbejderoplevelse, der viser det, du tilbyder.

- Forbedrede frynsegodeplaner giver dig mulighed for at oprette og administrere unikke frynsegodeplaner og understøtte komplekse satstabeller for frynsegoder og indlejrede niveauer. Du kan nemt oprette frynsegodeprogrammer, pakker og regler for automatisk registrering, der gør det nemmere for medarbejderne.

- Med flekskreditprogrammer kan du gøre det muligt at understøtte pension og andre levetidshændelser.

- Omfattende berettigelsesregler sikrer, at de rigtige fordele stilles til rådighed for de rette medarbejdere.

- Onlinetilmeldinger til frynsegoder giver medarbejderne en nem oplevelse.

- Behandling af kvalificerede levetidshændelser integreres med Medarbejderselvbetjening og understøtter også fremtidige livshændelser.

Hvis du vil have adgang til demodataene, skal du geninstallere dit sandkassemiljø.

Du kan angive direkte feedback eller rapportere problemer til: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Kendte problemer i forbindelse med Administration af frynsegoder

### <a name="eligibility-processing"></a>Berettigelsesbehandling

Når du kører frynsegodeberettigelse, der bruger en 1-5X løn, % af løn og dækningsbeløb med fladt beløb, skal datoen for **frynsegodedetaljer** angives til **startdatoen for medarbejder** i **Ansættelseshistorik**. Du skal også inkludere **Antal arbejdstimer**, **Betalingshyppighed**og **Årlig frynsegodeløn**. Hvis arbejderen har fast løn, skal du angive **Antal arbejdstimer** og **Betalingshyppighed**. Det årlige lønbeløb beregnes. Hvis medarbejderen er fastansat, er der ikke behov for at angive **Antal arbejdstimer**. Det anbefales, at du angiver fast løn først, når du opretter nye arbejdere. Når du vil opdatere posten med frynsegodedetaljer skal du navigere til **Arbejder > Historik for arbejder > Detaljer om ansættelse**. Juster datoen efter arbejderens startdato.

### <a name="employee-self-service"></a>Medarbejderselvbetjening

Medarbejderbeløbet beregnes ikke ved opdatering af dækningsbeløbet for livsforsikring. Når en medarbejder f.eks. tilbydes en livsforsikringsplan, kan de vælge dækning på op til $50.000 til en pris af $,36 pr. dækning på $1.000.  Når medarbejderen opdaterer dækningsbeløbet, forbliver medarbejderens tilknyttede omkostninger nul.

For en frynsegodeplan, der kun tillader en enkelt markering af denne plantype, vil brugeren modtage en fejlmeddelelse, hvis de forsøger at frafalde en plan, efter at der er valgt en plan. En bruger vælger f.eks. en medicinsk plan og anbringer den i sin indkøbsvogn. Brugeren vælger derefter **Frafald** for en anden medicinsk plan. Brugeren vil modtage en fejlmeddelelse.

## <a name="enable-benefits-management"></a>Aktivere Administration af frynsegoder

Administration af frynsegoder er en prøveversionsfunktion, og den er kun tilgængelig i **sandkassemiljøer**. I disse artikler beskrives det, hvordan du kan aktivere prøveversionsfunktioner i Personale. De angiver også, hvilke eksisterende funktioner i Personale, som Administration af frynsegoder erstatter, eller som deaktiveres, når du aktiverer Administration af frynsegoder.

- [Administrere funktioner](hr-admin-manage-features.md)
- [Prøveversionsfunktion: Administration af frynsegoder](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Konfigurere Administration af frynsegoder

Før du kan oprette frynsegodeplaner for dine medarbejdere, skal du konfigurere indstillinger for planerne.

- [Angive parametre for administration af frynsegoder](hr-benefits-setup-parameters.md)
- [Konfigurere berettigelsesregler og -indstillinger](hr-benefits-setup-eligibility-rules.md)
- [Konfigurere berettigelsesindstillinger for personlige kontakter](hr-benefits-setup-contact-eligibility-options.md)
- [Oprette disponeringsindstillinger](hr-benefits-setup-coverage-options.md)
- [Konfigurere betalingsfrekvenser](hr-benefits-setup-payment-frequencies.md)
- [Konfigurere typer af livshændelser](hr-benefits-setup-life-event-types.md)
- [Oprette plantyper](hr-benefits-setup-plan-types.md)
- [Definer årsagskoder](hr-benefits-setup-reason-codes.md)
- [Konfigurere niveaukoder](hr-benefits-setup-tier-codes.md)
- [Konfigurere satser](hr-benefits-setup-rates.md)
- [Konfigurere fradrag](hr-benefits-setup-deductions.md)
- [Konfigurere ventedage](hr-benefits-setup-waiting-days.md)
- [Konfigurere venteperioder](hr-benefits-setup-waiting-periods.md)
- [Konfigurere afrundingsregler](hr-benefits-setup-rounding-rules.md)
- [Oprette ansættelseskategorier](hr-benefits-setup-employment-categories.md)
- [Konfigurere ansættelsestyper](hr-benefits-setup-employment-types.md)
- [Konfigurere medarbejderselvbetjening](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Oprette frynsegodeplaner

Disse artikler viser, hvordan du opretter frynsegodeplaner, herunder pakker og flekskreditprogrammer.

- [Konfigurere frynsegodeplaner](hr-benefits-plans-setup.md)
- [Oprette frynsegodeplaner for arbejdere](hr-benefits-plans-worker.md)
- [Konfigurere flekskreditprogrammer](hr-benefits-plans-flex-credit-programs.md)
- [Konfigurere fremtidige livshændelser](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Behandle frynsegodeplaner

Du skal behandle nogle af ændringerne for at gøre dem aktive.

- [Behandle tilmeldingsberettigelse](hr-benefits-process-enrollment-eligibility.md)
- [Behandle livshændelser](hr-benefits-process-life-events.md)
- [Behandle ændringer af livshændelse](hr-benefits-process-life-event-changes.md)
- [Behandle berettigelse til livshændelse](hr-benefits-process-life-event-eligibility.md)
- [Behandle satsændringer](hr-benefits-process-rate-changes.md)

