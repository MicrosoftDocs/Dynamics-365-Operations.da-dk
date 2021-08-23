---
title: Nyheder eller ændringer i Dynamics 365 Human Resources, 22. juni 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 22. juni 2021.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 897c25df96017c5be1ae789027d178ca6b3ccc0410b4f65c7d2557b39e840134
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735345"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources, 22. juni 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4258.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Funktionen Informer brugere af arbejdere uden ansættelse – Når den avancerede adgang er slået til, og funktionen **Vis alle arbejdere uden ansættelse** er deaktiveret i funktionsstyring, vises der et banner for arbejderne uden ansættelsesformular. Banneret vil bede brugeren om at aktivere funktionen **Vis alle arbejdere uden ansættelse**. | Ikke anvendelig| [Arbejdere uden ansættelse](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Understøttelse af brugerdefineret felt for berettigelsesregler for administration af frynsegoder | [Understøttelse af brugerdefineret felt for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfiguration af regler for berettigelse](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Revision af transaktion til orlovsperiodisering | Ikke anvendelig | [Revision af transaktion til orlovsperiodisering](hr-leave-and-absence-accrue.md)|
| Forbedringer af arbejdsgang for orlov og fravær | [Forbedringer af arbejdsgang for orlov og fravær](https://go.microsoft.com/fwlink/?linkid=2147528) | [Anmod om fravær](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Emne |  Betegnelse |
| --- | --- | --- |
| 583052 | Brugere, der modtager feedback, kan redigere den feedback, der modtages | Når en medarbejder, der modtager feedback på en performancekladde, vælger **Tilføj eksternt link**, kan formularen redigeres, så medarbejderen kan redigere den performancefeedback, de har modtaget. |
| 522281 | Hvis du vælger antallet af medarbejdere i felterne i kompensationsstrukturen i Kompensationsstyring, medfører det forkerte resultater| Når du analyserer ned i kompensationsplanerne fra arbejdsområdet til kompensation, vises det korrekte antal medarbejdere nu. |
| 580683 | Brugere, der er tildelt rollerne Medarbejder og Leder, kan ikke tilknytte noter eller opdatere en performancekladde | Brugere, der er tildelt rollerne Medarbejder og Leder, kan ikke tilknytte noter eller opdatere en performancekladde. Brugeren modtager fejlen "Der kan ikke oprettes en post i performancekladdeposteringen (HcmPerfJournal). Tilladelse til sikkerhedspolitik nægtet". |
| 583077 | En medarbejders fødselsdato i firmakalenderen til orlov og fravær viser en forkert dato | Brugerne kan se den korrekte fødselsdato for medarbejderne i firmakalenderen til orlov og fravær. |
| 586996 | Funktionen for orlov på tværs af virksomheder medfører, at saldi er tomme, når adgang er begrænset til en enkelt virksomhed | Brugere kan få vist medarbejderens fremtidige orlovssaldi korrekt, når orlovsvisning på tværs af virksomheder er aktiveret. |
| 581014 | Hvis du aktiverer orlovs- og fraværsvisning på tværs af virksomheder, opstår der en fejl ved visning af fremtidige saldi | En fejl, der medførte, at brugere får vist de fremtidige orlovssaldi, hvor orlovsvisning på tværs af virksomheder er aktiveret, er blevet løst. |
| 509404 | Analyse af antal medarbejdere i afdelingen tager ikke hensyn til medarbejdernes bevægelser mellem afdelingerne. | Når en medarbejder migrerer fra én afdeling til en anden, afspejler dataene for antal medarbejdere i afdelingen ikke den gamle afdeling, hvor medarbejderen flyttes fra, hvis stillingsoplysningerne er udløbet i det indeværende år. |
| 584851 | Proportionalitetsreglen "Ingen" for frynsegodekredit giver aldrig kredit |Proportionalitetsreglen "Ingen" for flekskredit resulterede i, at medarbejdere modtog nul kreditter for frynsegodeperioden, uanset hvornår de blev ansat. Det er blevet rettet, så en medarbejder modtager alle flekskreditter, hvis de ansættes, før frynsegodeperioden begynder, og ingen, hvis de ansættes, efter perioden starter. |
| 584897 | Hvis du duplikerer tjenesten "Brug grundlæggende eksterne funktioner", resulterer det i en fejl | Når brugeren forsøgte at duplikere tjenesten "Brug grundlæggende eksterne funktioner", modtog brugeren fejlen "Der blev ikke fundet et objekt med id'et UserDefinedAppHostDialogView". |
| 575692 | Periodiseret orlov og fravær er ikke tilgængelig for ventende arbejdere | Orlovs- og fraværsperiodisering kan køres ved fremtidige ansættelser, når **Strømlinet medarbejderregistrering** er aktiveret. |
| 580110 | Når du føjer et firma til lønintegrationen, nulstilles integrationen, så den bruger alle enhederne, selvom indstillingen er angivet til ikke at opdatere projektet | Hvis en kunde har fjernet enheder eller ændret dataprojektet for lønintegration og har angivet indstillingen for at forhindre automatisk opdatering af projektet, ignoreres indstillingen, og projektet opdateres, når der føjes et nyt regnskab til integrationen.  |
| 584518 |Ydeevneproblemer ved behandling af tilmelding af frynsegoder | Denne rettelse løste problemer med ydeevnen i den tidligere proces for tilmelding af frynsegoder. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Platform update 10.0.19 (43) | Platformsopdatering 10.0.19 er planlagt til at starte udrulning med servicefrigivelse den 28. juni 2021. Få flere oplysninger i [Platformsopdateringer for version 10.0.19 af Finance and Operations-apps (juni 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Slå visning af Antal års tjeneste til/fra | Denne funktion giver mulighed for at bruge forskellige datoer til at beregne antal års tjeneste, der vises i formularerne **Strømlinet medarbejderindtastning** og **Personer**.  Det vil være tilgængeligt i Human Resources-parametre. |
|  Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Vedhæftede bemyndigelser til specifikke orlovstyper | Denne funktion giver administratorer mulighed for at tilføje vedhæftede bemyndigelser ved afsendelse af anmodninger om orlov for bestemte orlovstyper. |
|  Konfigurer orlovsenheder pr. orlovstype | Denne funktion giver administratorer mulighed for at konfigurere orlovsenheder (timer eller dage) for hver orlovstype.  |
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
