---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 20. maj 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 20. maj 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc7e89fabe1651c858097a6c564b4910a524331f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692745"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 20. maj 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4189.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Platform update 10.0.18 (42) | -- | [Platformsopdateringer til version 10.0.18 af programmer til finans og drift (maj 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Human Resources-appen til Microsoft Teams understøtter nu halvdagsdefinitioner og mulighed for opdelt dag | -- | [Administrere fraværsanmodninger i Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Emne |  Betegnelse |
| --- | --- | --- |
| 583776 | Massetilmelding af medarbejdere til orlovsplaner medfører en dubleret post-fejl | Denne fejl er blevet rettet med den nyeste udgivelse, og massetilmeldinger til orlovsplaner behandles nu korrekt. |
| 582263 | Behandling af livshændelser kan ikke køres for alle arbejdere på én gang | Når feltet **Arbejder** ikke udfyldes til behandling af livshændelser, behandles alle arbejdere. |
| 558383 | Primær modtager er ikke markeret som 100 %, hvis standardmodtageren ikke er valgt | Fejlen er blevet rettet, så brugeren kun behøver at vælge til/fra-knappen for den primære modtager.|
| 509404 | Analyse af antal medarbejdere i afdelingen tager ikke hensyn til medarbejdernes bevægelser mellem afdelingerne |Analyserne er blevet opdateret til at omfatte overførsler af medarbejdere mellem afdelinger|
| 579420 | Funktionen til frysning af kolonner i gitre er ikke tilgængelig endnu | Funktionen **Frysning af kolonner i gitre**, som ikke er tilgængelig i Personale, blev angivet som tilgængelige i Funktionsstyring. Funktionen er blevet fjernet fra listen over funktioner, der kan aktiveres. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Understøttelse af brugerdefineret felt i berettigelsesregler for administration af frynsegoder | [Understøttelse af brugerdefineret felt for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfiguration af regler for berettigelse](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Arbejdsområde for frynsegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Forbedringer af arbejdsgang for orlov og fravær | [Forbedringer af arbejdsgang for orlov og fravær](https://go.microsoft.com/fwlink/?linkid=2147528) | [Anmod om fravær](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|
| Revision af transaktion til orlovsperiodisering | - | [Revision af transaktion til orlovsperiodisering](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
|  Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
