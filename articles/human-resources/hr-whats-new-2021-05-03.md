---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 3. maj 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 3. maj 2021.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01ebd15e09e181a7ea0ec5bf70c8df731d2169c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902854"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 3. maj 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4140.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Tilføj infolinje, når der oprettes livshændelser. | - | Når du opretter en livshændelse, vises der en meddelelse med angivelse af den type livshændelse, der er oprettet, på informationslinjen.

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem |  Beskrivende tekst |
| --- | --- | --- |
| 559312 |  Niveau vises ikke, når der oprettes en fast løn-plan for en medarbejder. |  Hvis der er en tidszoneuoverensstemmelse mellem brugerens tidszone og firmaets tidszone, kan kompensationsniveauet for jobbet ikke læses. Forespørgslen er opdateret, så den kan hentes på basis af UTC-tid. |
| 573676  | Du kan ikke tilføje en ny periode i formularen **Frynsegodeplan**. | Formularen er blevet opdateret, så knappen **Ny** er aktiveret under fanen **Periode** i oversigtspanelet **Frynsegodeplaner**. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Forbedringer af arbejdsgang for orlov og fravær | [Forbedringer af arbejdsgang for orlov og fravær](https://go.microsoft.com/fwlink/?linkid=2147528) | [Anmod om fravær](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|
| Revision af transaktion til orlovsperiodisering | - | [Revision af transaktion til orlovsperiodisering](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Platform update 10.0.18 (42) | Platformsopdatering 10.0.18 er planlagt til at starte udrulning med servicefrigivelse den 17. maj 2021. Du kan få mere at vide i [Platformsopdateringer til version 10.0.18 af Finans- og driftsapps (maj 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Understøttelse af brugerdefineret felt i berettigelsesregler for administration af frynsegoder  | [Understøttelse af brugerdefineret felt for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
