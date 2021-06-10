---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 22. februar 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 22. februar 2021.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cac3c188e372521a1f63833cd0032f0e9ff7ebe3
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052379"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 22. februar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3988.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Dynamics 365 Human Resources-app til Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Udsted |  Beskrivelse |
| --- | --- | --- |
| 529994 | Redigering af feltet **Kendt som** i formularen **Arbejder** udløser ikke en Dataverse-opdatering | Har løst et problem, hvor Dataverse ikke opdateres, når feltet **Kendt som** opdateres i formularen **Arbejder**. |
| 532651 | Kompensationsanalysens PBI-rapport bruger ikke valutaomregning ved beregning af målepunkter for alle virksomheder | Har løst et problem, hvor PBI-rapportens kompensationsanalyse ikke foretager valutaomregninger korrekt. |
| 552226 | Behandling af livshændelser lukker og genåbner planer flere gange for en enkelt livshændelse  | Har løst et problem, hvor en medarbejder er i flere juridiske enheder, og der indtræffer en livshændelse, og der genereres en hændelsespost for hvert af de juridiske enheder, som medarbejderen er i. Når livshændelser behandles, skal den juridiske enhed, der skal behandles, vælges. Behandlingslogikken begrænser dog ikke sig selv til denne juridiske enhed. Den behandler i stedet alle juridiske enheder og lukker og genåbner planerne i den valgte juridiske enhed. Denne handling for en levetidshændelse behandles flere gange i den samme juridiske enhed, hvilket medfører flere lukninger/genåbninger af hver af de planer, der er påvirket af livshændelsen. |
| 518064 | Kun én afhængig er valgt i berettigede planer, når mere end én er markeret som standardudpeget | Har løst et problem, hvor flere standardudpegede ikke er valgt automatisk i berettigede planer. Du kan nu også angive en primær modtager for en personlig kontakt. Den primære modtager er angivet som 100 % i berettigede planer, når der er flere modtagere. |
| 552365 | Brug din egen database (BYOD)-eksportjob mislykkes efter opgradering til Platform update 40 | Har løst et problem, hvor BYOD-eksport mislykkes efter anvendelse af Platform update 40 på miljøet. |
| 547123 | Begrænse antallet af opgaver, der forespørges på opgavelisten på dashboard | Antallet af opgaver, der vises på opgavelisten, er nu begrænset til 15 for at løse et ydeevneproblem, der skyldes, at der er for mange opgaver, der forsøger at blive indlæst. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Visning af orlov for ledere på tværs af firmaet | [Visning af orlov for medarbejdere på tværs af firmaet](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere parametre for orlov og fravær](./hr-leave-and-absence-parameters.md) |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for personalegodeadministration](hr-benefits-management-workspace.md) |
| Begrænse medarbejdere i at redigere forretningskontaktoplysninger | [Begrænse medarbejdere i at redigere forretningskontaktoplysninger](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiopdateringer til Microsoft Dataverse

Gældende fra november 2020, Common Data Service er omdøbt til [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Se den [officielle meddelelse](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for at få mere at vide. Med denne navneændring er en del af terminologien i Dataverse blevet opdateret. F.eks. er *enhed* nu *tabeĺ*, og *felt* er nu *kolonne*. Yderligere oplysninger finder du i [Opdateringer af terminologi](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne version er terminologi vedrørende Dynamics 365 Human Resources-integrationen med Dataverse opdateret i hele programmet, så den afspejler disse ændringer. Integrationsformen **Common Data Service** er nu **Microsoft Dataverse-integration**.

Du kan få mere at vide om Dynamics 365 Human Resources-integrationen med Microsoft Dataverse under [Konfigurere Microsoft Dataverse-integration](./hr-admin-integration-common-data-service.md) og [Konfigurere Microsoft Dataverse-virtuelle tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Opdateringer til implementering af tjenester

Fra og med 22. februar 2021 versionen justerer vi installationen af vores regionale tjenesteopdatering. Justeringerne omfatter ændringer i den rækkefølge, hvori globale regioner modtager opdateringer til tjenesten Human Resources, og ændringer i ventetiden mellem opdateringsstadier. Disse ændringer bringer os mere i overensstemmelse med sikker implementeringspraksis (Safe Deployment Practices - SDP) med henblik på at forbedre tjenestens sikkerhed, kvalitet og understøttelse.

Vi fortsætter med at følge det to ugers implementeringsinterval. Men kunderne bemærker måske, at opdateringer typisk anvendes på deres Human Resources-miljøer på en anden dag i den to ugers periode end i de tidligere versioner.

Du kan finde flere oplysninger om opdateringsprocessen for tjenesten i [opdateringsprocessen](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]