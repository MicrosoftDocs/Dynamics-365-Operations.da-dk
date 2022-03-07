---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (26. september 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 26. september 2020.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8b0260c4d1bafe271a08336ceed7dc3742f1d590
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061378"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (26. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources. Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2020-udgivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3589-hf.3.

### <a name="new-features"></a>Nye funktioner

Følgende funktion er generelt tilgængelig med denne udgivelse:

- **Platform update 10.0.13 er nu tilgængelig**: Yderligere oplysninger om opdateringen finder du i [Platformsopdateringer til version 10.0.13 af Finans- og driftsapps (oktober 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Der kan være opdateringer til dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Fejl | Beskrivelse |
| --- | --- | --- |
| 469495 | Opdatere gitteret og dialogboksen for økonomiske standarddimensioner | Gitter og dialogboks for økonomiske dimensioner er opdateret overalt i Human Resources. |
| 474887 | Workflowopgaven for orlovsanmodning åbner et forkert link i en manuel beslutning | Når en arbejdsproceskonfiguration indeholder en manuel beslutning, og du navigerer til orlovsanmodningen fra **Workflowopgaver, der er tildelt til mig**, åbnes det forkerte link, og der vises enten en tom formular eller en orlovsanmodning, der er oprettet af den aktuelle bruger, i stedet for den, der er tildelt brugeren til den manuelle beslutning. |
| 474962 | Enheden Parametre for orlov og fravær indeholder felter med flertydige navne | Enhedsnavnene i Parametre for orlov og fravær er blevet opdateret, så de er klarere. |
| 481401 | Periodiseringsprocesser hænger, når grundlaget for periodiseringsdatoen ligger efter den periodiserede startdato og ved afslutningen af måneden | Periodiseringsprocesser er opdateret, så de ikke at have en forsinkelse, når periodiseringsdatogrundlaget er efter den periodiserede startdato og ved udgangen af måneden. |
| 447167 | Lister over poster, der udløber, omfatter inaktive arbejdere | Fanen **Udløbende poster** i **Personalestyring** omfatter inaktive arbejdere. Nu omfatter den kun aktive arbejdere. |
| 486840 | Forkert orlovsanmodning åbnes fra **Workflowopgaver, der er tildelt til mig** | Valg af en orlovsanmodning fra **Workflowopgaver, der er tildelt til mig** åbner ikke længere den seneste orlovsanmodning, der er tildelt den aktuelle bruger. |
| 506868 | Dataverse-feltet **Stilling** er ikke indstillet til enheden **Stilling** | Feltet **Titel** i enhederne **Job** og **Stilling** vises som ikke angivet. Feltet **Titel** vises nu. |
| 430359 | Der er ikke adgang til offboarding-kontrollisteopgaver, når leder- og medarbejderroller er tildelt | Arbejdere med en fremtidig fratrædelsesdato kunne ikke få adgang til deres kontrollisteopgaver, hvis de kun havde rollen som medarbejder eller leder. Nu kan brugere, der kun har en medarbejder- eller lederrolle, få adgang til offboarding-opgaver med en fremtidig fratrædelsesdato. |
| 458102 | Ny medarbejder vises ikke i enheden med **lønoplysninger for arbejder** ved oprettelsen | Nye medarbejdere inkluderes i enheden med arbejderes lønoplysninger uden at skulle åbne medarbejderens lønoplysninger, før enheden eksporteres. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Udvidede anmodninger om og godkendelser af arbejdsprocesser | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Kommer snart

Følgende ny funktion er planlagt til en fremtidig udgivelse:

- [Brugerdefinerede links i selvbetjening for leder](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2019 udgivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Yderligere ressourcer

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)
[Oversigt over Dynamics 365 Human Resources 2020 udgivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Opdateringsproces](hr-admin-setup-update-process.md)
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]