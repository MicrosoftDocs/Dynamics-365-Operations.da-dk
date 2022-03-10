---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 19. november 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i enkeltstående Microsoft Dynamics 365 Human Resources for 19. november 2021.
author: marcelbf
ms.date: 12/03/2021
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
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087468"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 19. november 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Microsoft Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne version indeholder følgende fejlrettelser. Ændringerne gælder for build nummer 8.1.4591.

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne for at medtage rettelser i buildet, som er foretaget, efter dette emne blev udgivet.

| Fejlnummer | Emne | Beskrivelse |
|---|---|---|
| 626178 | Navigation mangler i arbejderfelterne i **Selvbetjening for leder** | Dette problem er nu løst. Navigationen er tilgængelig, så du kan se rapportdetaljerne i **Selvbetjening for leder**. |
| 632573 | Der opstår ingen valideringsfejl, når du gemmer et **kursus** | Dette problem er nu løst. Når du oprettede et kursus, hvor **Mindste antal deltagere** var større end 0, blev det stadig tilladt at gemme det, selvom **Maksimalt antal deltagere** er 0. |
| 615955 | Fejlen "Feltet **Formål** skal udfyldes" ved oprettelse af en ny placering til rekrutteringsanmodninger. | Når du opretter en adresse til en ny placering for rekrutteringsanmodninger, får du fejlen: "Feltet 'Formål' skal udfyldes." Feltet **Formål** er dog ikke tilgængeligt på siden. |
| 620797 | Fejl, der siger at feltet **Køn** er tomt, er misvisende | Når der ikke er angivet et køn for en personlig kontakt, viser rapporten 'Klik eller tryk her for at angive tekst' – Det er misvisende, da der ikke kan angives noget i feltet. |
| 620800 | Linket til oversigten over personalegoder er skjult | Oversigten over personalegoder kan som standard ikke vises i **Medarbejderselvbetjening**.  Der er tilføjet et link i højre side af **Medarbejderselvbetjening** under sektionen **Links** |
| 629778 | Problemer med ydeevnen ved CDS-integration. | Godkendelsesrelateret anmodning forårsagede problemer med ydeevnen. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering eller deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
|---|---|---|
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Kommer snart
Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
