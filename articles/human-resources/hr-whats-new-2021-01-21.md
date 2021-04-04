---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 21. januar 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 21. januar 2021.
author: marcelbf
manager: tfehr
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fc3bb035686a46030514aca1f5ad03a2681845fd
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463520"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 21. januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2020-udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3866.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Platform update 10.0.16(40) | -- | [Platformsopdateringer til version 10.0.16 af Finance and Operations-apps (februar 2021)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| Udvidede anmodninger om og godkendelser af arbejdsprocesser | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Affordable Care Act (ACA) - overholdelsesopdateringer til blanket 1095-C, blanket 1095-B og elektronisk rapportering i ældre frynsegoder | -- | -- | 
| Frynsegodeadministration understøtter nu ACA-rapportering for overholdelse af USA-baserede juridiske enheder | -- | [Generere ACA-rapporter i Frynsegodeadministration](hr-benefits-management-aca-reports.md) |
| Frynsegodeadministration har nu vist lag med frynsegodesats og dobbelte lag af frynsegodeniveau  | -- | -- |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Udsted |  Beskrivelse |
| --- | --- | --- |
| 533079 | Navigationsfejlen "Formularen blev kaldt forkert", da vi prøver at se på fradrag. | Faste fejl, mens du ser på fradrag for frynsegoder med visningen **Fra og med**-dato. |
| 543641 | Postnummeret udfyldes ikke ved elektronisk rapportering.  | Fastsatte en intern kode på postnummeret, der ikke vises i elektroniske ACA-rapporter til frynsegodeadministration, når dækningskoden er M til Q. |
| 542815 | Skærmbilledet til personlig kontakt i Medarbejderselvbetjening giver medarbejderne mulighed for at se andres personlige kontakter. | Faste fejl, hvor personlige kontaktpersoner under **Redigering** af selvbetjening for medarbejdere ikke begrænser forespørgslen nok til at sikre, at der kun hentes en enkelt personlig kontaktperson, så en bruger kan bruge tastaturgenveje til at få vist andres kontaktpersoner. |
| 536157 | Integrationssiden i **Microsoft Dataverse** kan ikke åbnes i Systemadministration pga. IsVirtualEntityPackageInstalled(). | Problemer forhindrer, at **Microsoft Dataverse**-integrationssiden indlæses i Human Resources. |
| 533079 | Navigationsfejlen "Formularen blev kaldt forkert", da vi prøver at se på fradrag. | Faste fejl, der optræder i formularen **Fradrag** for Frynsegodeadministration, når den vises som **Fra og med-dato**. |
| 537264 | Fanen **Personlige**, der hurtigt mangler fra kandidatposten. | Kandidatens personlige oplysninger er nu tilgængelige i kandidatposten. |
| 537267 | **Erhvervserfaring** vises ikke i interne kandidatposter. | Fanen **Erhvervserfaring** vises ikke i interne kandidatposter. Hvis kandidaten var intern, blev **Erhvervserfaring** erstattet af **Ansættelseshistorik**, som er kandidatens ansættelseshistorik i organisationen. Begge kan anvendes og skal vises for interne ansøgere. |
| 537067 | **Tilladelse til at kontakte arbejdsgiver** vises ikke. | Administration af **Tilladelse til at kontakte arbejdsgiver** blev tilføjet ruden **Rediger erhvervserfaring** for en kandidatpost. |
| 525957 | **Kandidatstatus** opdateres ikke på interne ansøgere, når overførslen er fuldført. | Når en overførsel er fuldført (knappen **Skift stilling** eller **Fortsæt** er valgt på siden **Overfør arbejder til en ny stillingstildeling**), skal **status** for kandidatposten ændres til **Ansat**. |
| 537051 | Valutasymboler for den indisk rupee og tyrkiske lira synkroniseres ikke korrekt til Dataverse | Valutasymboler for den indisk rupee og tyrkiske lira synkroniseres nu korrekt til Dataverse. |
| 534846 | Rekrutteringstabeller skal aktiveres i Dataadministration. | De nye tabeller, der er oprettet til rekrutteringsanmodninger og ansøgerne, er nu aktiveret til Dataadministration. Det gør det muligt at aktivere sporing af ændringer for tabellerne, hvilket gør det muligt at spore OData-ændringer på de virtuelle Dataverse-tabeller. |
| 533474 | Ret manglende reference til Microsoft.SqlServer.XEvent.dll. | Undtagelser til assembly-indlæsning for Microsoft.SqlServer.XEvent.dll forhindrede virtuelle Dataverse-tabeller i at blive konfigureret i visse miljøer. |
| 481122 | Arbejdsområdet **Personale** viser stillinger, der har trukket sig tilbage. | TIlbagetrukne stillinger blev vist som åbne stillinger i **Personale**-arbejdsområdet. Tilbagetrukne stillinger vises ikke længere. | 
| 541978 | Tilføj primær e-mailadresse til BaseWorker-enheden. | Denne ændring har tilføjet arbejderens primære e-mailadresse til HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Integration med LinkedIn Talent Hub | [Integration med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn talent-hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Visning af orlov for ledere på tværs af firmaet | [Visning af orlov for medarbejdere på tværs af firmaet](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere parametre for orlov og fravær](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Give yderligere indsigt i orlovssaldi| [Give yderligere indsigt i orlovssaldi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Administrere medarbejderorlov](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Ledere, der kan sende rekrutteringsanmodninger om stillinger | [Ledere, der kan sende en rekrutteringsanmodning om åbne stillinger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Tilføje en rekrutteringsanmodning](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Udvidet kandidatprofil i Personalestyring | [Udvidet kandidatprofil i Personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Tilføje eller redigere en kandidatprofil](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Muliggøre forenklet integration med rekrutteringsudbydere | [Muliggøre forenklet integration med rekrutteringsudbydere](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobkandidater](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Kommer snart
| Funktion | Detaljer |
| --- | --- |
| Bekræftelse af e-mail til fordelsbetalinger | Med denne funktion sendes der en bekræftelses-email til medarbejdere, når de tjekker ud fra frynsegodetilmeldingsoplevelser i medarbejderselvbetjening. Der er flere oplysninger i [Konfigurere parametre administration af frynsegoder pr. firma](hr-benefits-setup-parameters-per-company.md). |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2020 udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologiopdateringer til Microsoft Dataverse

Gældende fra november 2020, Common Data Service er omdøbt til [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Se den [officielle meddelelse](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) på Power Apps-bloggen for at få mere at vide. Sammen med denne navneændring er en del af terminologien Dataverse blevet opdateret. F.eks. er *enhed* nu *tabeĺ*, og *felt* er nu *kolonne*. Yderligere oplysninger finder du i [Opdateringer af terminologi](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

I denne version er terminologi vedrørende Dynamics 365 Human Resources-integrationen med Dataverse opdateret i hele programmet, så den afspejler disse ændringer. Integrationsformen **Common Data Service** er nu **Microsoft Dataverse-integration**.

Du kan få mere at vide om Dynamics 365 Human Resources-integrationen med Microsoft Dataverse under [Konfigurere Microsoft Dataverse-integration](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) og [Konfigurere Microsoft Dataverse-virtuelle tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2020 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]