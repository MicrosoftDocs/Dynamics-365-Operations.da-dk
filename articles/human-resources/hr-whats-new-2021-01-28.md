---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 28. januar 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 28. januar 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909753"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 28. januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3906.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Integrere årsagskoder til frynsegoder i arbejdsområdet **Personalstyring** | -- | [Definer årsagskoder](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.


| Fejlnummer | Problem |  Beskrivende tekst |
| --- | --- | --- |
| 539456 | Kalenderen viser orlovstypen tekst, når **Vis kun fravær uden detaljer** er aktiveret. | Når indstillingen **Vis kun fravær uden detaljer** er aktiveret, vises datoen for anmodningen nu i fraværsformat. |
| 528907 | Hvis medarbejdere får adgang til en juridisk enhed for medarbejderrollen, vil ledere ikke kunne se orlovsaktiviteten for medarbejdere i området til medarbejder-selvbetjening **My team**. |Indstilling af denne indstilling giver nu ledere mulighed for fortsat at se aktiviteten for orlovssaldoen. |
| 526280 | Rettighedsfejl på HcmWorkerEntity, HcmEmployeeEntity og HcmContractorEntity. | Brugere i en rolle som ikke-systemadministrator kunne ikke eksportere de enheder, der vises på grund af en rettighedsfejl i feltet NationalityCountryRegion. Brugerne vil fortsat have brug for følgende rettigheder for at kunne eksportere disse oplysninger: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain og HCMContractorEntityView. |
| 542147 | Felterne **Bankkontonummer** og **Registreringsnummer** skal udfyldes ved tilføjelse af bankkonto via Medarbejderselvbetjening. | Vi har rettet den fejl, hvor medarbejderne skulle angive felterne **Bankkontonummer** og **Registreringsnummer**, og de har tilføjet bankkontooplysninger. Disse felter er ikke længere obligatoriske, når du gemmer nye bankkontooplysninger. |
| 543641 | Postnummeret udfyldes ikke ved elektronisk rapportering. | Fastsæt en fejl, når postnummeret ikke udfyldes i ACA-rapporten for dækningskoder L til Q. |
| 545402 | Tilføj ruteændring for UserSysteming.js-filen for at fjerne 404 fejl. | Brugeren bør ikke længere se 404-fejl i konsollen. |

## <a name="in-preview"></a>Som eksempel   

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Visning af orlov for ledere på tværs af firmaet | [Visning af orlov for medarbejdere på tværs af firmaet](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere parametre for orlov og fravær](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Bekræftelse af e-mail til fordelsbetalinger | Med denne funktion sendes der en bekræftelses-email til medarbejdere, når de tjekker ud fra frynsegodetilmeldingsoplevelser i medarbejderselvbetjening. Denne funktion er tilgængelig den 1. februar. Der er flere oplysninger i [Konfigurere parametre administration af frynsegoder pr. firma](hr-benefits-setup-parameters-per-company.md). |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiopdateringer til Microsoft Dataverse

Gældende fra november 2020, Common Data Service er omdøbt til [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Se den [officielle meddelelse](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for at få mere at vide. Sammen med denne navneændring er en del af terminologien Dataverse blevet opdateret. F.eks. er *enhed* nu *tabeĺ*, og *felt* er nu *kolonne*. Yderligere oplysninger finder du i [Opdateringer af terminologi](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne version er terminologi vedrørende Dynamics 365 Human Resources-integrationen med Dataverse opdateret i hele programmet, så den afspejler disse ændringer. Integrationsformen **Common Data Service** er nu **Microsoft Dataverse-integration**.

Du kan få mere at vide om Dynamics 365 Human Resources-integrationen med Microsoft Dataverse under [Konfigurere Microsoft Dataverse-integration](./hr-admin-integration-common-data-service.md) og [Konfigurere Microsoft Dataverse-virtuelle tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]