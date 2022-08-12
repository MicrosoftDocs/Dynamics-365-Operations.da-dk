---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 5. april 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 5. april 2021.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067995"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 5. april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4074.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Begrænse medarbejdere i at redigere forretningskontaktoplysninger | [Begrænse medarbejdere i at redigere forretningskontaktoplysninger](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrænse redigering af personlige oplysninger](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem |  Beskrivende tekst |
| --- | --- | --- |
| 550852 | Knappen **Godkendelse** valideres ikke med obligatoriske felter angivet i formularen **Gennemse**. | Når du angiver et felt i formularen **Gennemse** som obligatorisk og publicerer ændringerne for rollen Leder, valideres formularen ikke som forventet. |
| 559564 | Historiske arbejderhandlinger for ændring af fast løn giver fejl for fratrådte brugere. | Arbejderhandlingen for en fratrådt medarbejders løn giver en fejl. Når en medarbejder er fratrådt, giver arbejderhandlingen forfremmelse før fratrædelse en fejl. |
| 560074 | Rullelisten Ansættelseskategori filtrerer ikke efter **Arbejdertype** og viser kategorier for medarbejdere og kontrahenter. | I formularen **Medarbejder** skal rullelisten **Ansættelseskategori** vise enten medarbejder- eller kontrahentkategorier baseret på medarbejderens arbejdertype. |
| 567388 | Nogle af oplysningerne for nyoprettede medarbejdere synkroniseres ikke med det samme til tabellen **cdm_worker** i Dataverse. | Når du opretter en ny medarbejderpost, synkroniseres den nye post med tabellen **cdm_worker** i Dataverse, men ikke alle egenskaber medtages i Dataverse-posten. |
| 563837 | Funktioner, der ikke er tilgængelige i visningen Human Resources. | Flere funktioner, der ikke gælder for Human Resources, vises i Funktionsstyring. Disse funktioner fjernes nu fra listen over funktioner, der er tilgængelige til aktivering i Human Resources. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |
| Platform update 10.0.17 (41) | Platform update 10.0.17 er planlagt til at begynde udrulning med den næste frigivelse den 19. april 2021. Du kan få mere at vide i [Platformsopdateringer til version 10.0.17 af programmer til finans og drift (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
