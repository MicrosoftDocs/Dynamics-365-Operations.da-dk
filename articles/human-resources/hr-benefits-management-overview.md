---
title: Oversigt over administration af frynsegoder
description: Oversigt over funktionen Administration af frynsegoder i Dynamics 365 Human Resources. Tilbyd dine medarbejdere mulighed for ekstra frynsegoder via en brugervenlig onlineoplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819759"
---
# <a name="benefits-management-overview"></a>Oversigt over administration af frynsegoder

Hvis du vil forblive konkurrencedygtig, skal du tilbyde en lang række frynsegoder for at tiltrække og holde på dine bedste medarbejdere. Ud over standardfrynsekoder som sundhedsforsikring og tandlægedækning kan det også være en god idé at tilbyde udvidede tjenester som hjælp til adoption, rekreative ordninger og beklædningsgodtgørelse. Administration af frynsegoder i Microsoft Dynamics 365 Human Resources giver dig en fleksibel løsning, som understøtter en lang række frynsegodemuligheder. Personale inkluderer også en brugervenlig medarbejderoplevelse, der viser det, du tilbyder.

- Forbedrede frynsegodeplaner giver dig mulighed for at oprette og administrere unikke frynsegodeplaner og understøtte komplekse satstabeller for frynsegoder og indlejrede niveauer. Du kan nemt oprette frynsegodeprogrammer, pakker og regler for automatisk registrering, der gør det nemmere for medarbejderne.

- Med flekskreditprogrammer kan du gøre det muligt at understøtte pension og andre levetidshændelser.

- Omfattende berettigelsesregler sikrer, at de rigtige fordele stilles til rådighed for de rette medarbejdere.

- Onlinetilmeldinger til frynsegoder giver medarbejderne en nem oplevelse.

- Den kvalificerede levetidshændelsesproces understøtter fremtidige levetidshændelser.

Hvis du vil have adgang til demodataene, skal du geninstallere dit sandkassemiljø.

## <a name="enable-benefits-management"></a>Aktivere Administration af frynsegoder

I dette emne beskrives, hvordan du slår funktioner til i Human Resources. Den angiver også, hvilke eksisterende funktioner i Human Resources som Administration af frynsegoder erstatter, eller der deaktiveres, når du aktiverer Administration af frynsegoder.

> [!IMPORTANT]
> Når du aktiverer Administration af frynsegoder i et **produktionsmiljø**, kan du ikke deaktivere det. Vi anbefaler, at du aktiverer og tester Administration af frynsegoder i et **sandkassemiljø**, før du aktiverer det i et **produktionsmiljø**. Der er betydelige forskelle mellem den gamle frynsegodefunktionalitet og de nye funktioner til administration af frynsegoder, der kræver yderligere opsætning, og som skal testes, før de bringes i produktion.

- [Administrere funktioner](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Konfigurer medarbejderoplysninger

Før du kan tilmelde medarbejdere til frynsegoder, skal du angive de nødvendige oplysninger. Du skal melde en medarbejder til en **Fast lønstruktur** på medarbejderens startdato, og du skal vælge en **Frekvens for udbetaling af frynsegoder** i **Ansættelsesoplysninger** i formularen **Arbejder**.

Hvis du har en medarbejder, der modtager supplerende kompensation såsom provision, kan du tilføje et beløb for **Årlig frynsegodeløn** fra medarbejderposten. Human Resources skal bruge beløbet for **Årlig frynsegodeløn** til bestemmelse af dækningsbeløb i stedet for det årlige beløb for fast løn. **Årlig frynsegodeløn** skal være gyldig pr. medarbejderens startdato eller starten af frynsegodeperioden, afhængigt af hvad der er den seneste. Hvis der registreres både en fast løn og et årligt frynsegodebeløb for medarbejderen, vil de årlige frynsegoder blive brugt til at fastlægge dækningsbeløbene.

Når du opretter en frynsegodeplan, som bruger satser, der er baseret på køn eller alder, skal du angive medarbejderens fødselsdato og køn, som kan bruges til at beregne frynsegodeomkostningerne.

## <a name="configure-benefits-management"></a>Konfigurere administration af frynsegoder

Før du kan oprette frynsegodeplaner for dine medarbejdere, skal du konfigurere indstillinger for planerne.

- [Angive parametre for administration af frynsegoder](hr-benefits-setup-parameters.md)
- [Konfigurere berettigelsesregler og -indstillinger](hr-benefits-setup-eligibility-rules.md)
- [Konfigurere indstillinger for personlig kontaktberettigelse](hr-benefits-setup-contact-eligibility-options.md)
- [Oprette disponeringsindstillinger](hr-benefits-setup-coverage-options.md)
- [Konfigurere betalingshyppigheder](hr-benefits-setup-payment-frequencies.md)
- [Konfigurere livsbegivenhedstyper](hr-benefits-setup-life-event-types.md)
- [Oprette plantyper](hr-benefits-setup-plan-types.md)
- [Konfigurere årsagskoder](hr-benefits-setup-reason-codes.md)
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
- [Konfigurere flekskreditprogrammer](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Behandle frynsegodeplaner

Du skal behandle nogle af ændringerne for at gøre dem aktive.

- [Behandle tilmeldingsberettigelse](hr-benefits-process-enrollment-eligibility.md)
- [Behandle livshændelser](hr-benefits-process-life-events.md)
- [Behandle ændringer af livshændelse](hr-benefits-process-life-event-changes.md)
- [Behandle berettigelse til livshændelse](hr-benefits-process-life-event-eligibility.md)
- [Behandle satsændringer](hr-benefits-process-rate-changes.md)

