---
title: Organisationer og organisationshierarkier (Oprindelsesdata til handel)
description: "Oprindelsesdata til handel har tre typer interne organisationer, som du kan definere for at hjælpe en organisation med at udføre en forretningsproces eller nå et mål."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 17d434f5d49d544003ee7cb862391d88ac5c723a
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organisationer og organisationshierarkier (Oprindelsesdata til handel)

[!include[banner](includes/banner.md)]


Oprindelsesdata til handel har tre typer interne organisationer, som du kan definere for at hjælpe en organisation med at udføre en forretningsproces eller nå et mål. 

En organisation er en gruppe af personer, der arbejder sammen for at udføre en forretningsproces eller for at nå et mål. Et organisationshierarki repræsenterer relationerne mellem de virksomhedsenheder, som din organisation består af.

## <a name="organizations"></a>Organisationer
I Oprindelsesdata til handel kan du definere tre typer interne organisationer: juridiske enheder, driftsenheder og teams. I Microsoft Dynamics AX er alle interne organisationer typer af enheden Part. Disse organisationer benytter derfor et adressekartotek til opbevaring af adresser og andre kontaktoplysninger. En part kan være enten en person eller en organisation og kan tilhøre et eller flere adressekartoteker.
### <a name="legal-entities"></a>Juridiske enheder

En juridisk enhed er en organisation, der består af en registreret eller lovgivningsbaseret juridisk struktur. Juridiske enheder kan indgå juridisk bindende kontrakter og skal udarbejde opgørelser med afrapportering af deres præstation. Et firma er en type juridisk enhed i Microsoft Dynamics AX, og hver juridiske enhed får tilknyttet et firma-id. Denne tilknytning eksisterer, fordi et firma-id, eller DataAreaId, bruges i nogle datamodeller, hvor firmaer bruges som en afgrænsning for datasikkerhed. Brugere har kun adgang til data for det firma, som de er logget på.

### <a name="operating-units"></a>Driftsenheder

En driftsenhed er en organisation, der bruges til at opdele administrationen af økonomiske ressourcer og driftsprocesser i et firma. Personer i en driftsenhed er forpligtet til at maksimere brugen af knappe ressourcer, til at forbedre processer og til at redegøre for deres præstation. Typerne af driftsenheder i Oprindelsesdata til handel omfatter bærere, forretningsenheder, værdistrømme, afdelinger og detailkanaler. Tabellen nedenfor indeholder flere oplysninger om hver type driftsenhed.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Type driftsenhed** | **Beskrivelse**                                                                         | **Formål**                                                                                                                                 |
| Virksomhedsenhed           | En halvautomatisk driftsenhed, der er skabt for at nå strategiske forretningsmålsætninger. | Brug virksomhedsenheder til regnskabsaflægning, der er baseret på brancher eller produktlinjer, som organisationen betjener uafhængigt af juridiske enheder. |
| Detailkanal          | En driftsenhed, der repræsenterer en fysisk butik.                             | Bruges til at administrere og styre en eller flere butikker inden for eller på tværs af juridiske enheder.                                                               |

## <a name="organizational-hierarchies"></a>Organisationshierarkier
Hvert hierarki er tildelt et formål i Oprindelsesdata til handel. Formålet med et hierarki afgør, hvilke organisationstyper der kan medtages i hierarkiet. Formålet definerer også de anvendelsesscenarier, hierarkiet kan bruges i. For eksempel kan et detailhierarki bruges til at købe og sælge produkter i en detailbutik. Organisationer i et hierarki kan dele parametre, politikker og transaktioner. En organisation kan nedarve eller tilsidesætte parametrene for dens overordnede organisation. Delte masterdata, som f.eks. produkter og adressekartoteker, gælder dog for hele organisationen og kan ikke tilsidesættes for individuelle organisationer.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Best practices for konfiguration af en organisation i et hierarki

Overvej følgende bedste fremgangsmåder, når du implementerer et organisationshierarki:
-   Opret en afdeling for at angive skæringspunktet mellem en juridisk enhed og en virksomhedsenhed. Du kan derefter rulle data op fra en afdeling til en juridisk enhed for lovpligtig rapportering og fra en afdeling til en virksomhedsenhed for intern rapportering.
-   I en juridisk enhed skal du ikke konfigurere flere hierarkier til samme hierarkiformål.
-   Opret ikke et hierarki til hvert formål. Du kan sædvanligvis bruge samme hierarki til flere formål. Samme hierarki over driftsenheder kan f.eks. tildeles alle politikrelaterede formål.
-   Opret balancerede hierarkier. I et hierarki defineres alle noder, der har samme afstand til rodnoden, som et niveau. I et balanceret hierarki kan der kun forekomme én type driftsenhed på hvert niveau, og afstanden fra rodnoden til hvert niveau er den samme. Hvis der er mellemliggende niveauer mellem en afdeling og en juridisk enhed eller en virksomhedsenhed, kan det være nødvendigt at bruge pladsholderorganisationer, for at skabe et balanceret hierarki.
-   Opret ikke et separat hierarki af driftsenheder, hvis strukturen for juridiske enheder også er virksomhedens driftsstruktur. Et hierarki med en kombination af juridiske enheder og driftsenheder kan bruges til begge formål.
-   Før du oprettet større omstruktureringsscenarier, skal du bruge hierarkiets ikrafttrædelsesdatoer til at udføre en effektanalyse og en valideringstest.
-   Gem et hierarki som en kladde, hvis du eventuelt vil ændre et hierarki, før du udgiver det.
-   Begræns antallet af personer, der har rettigheder til at tilføje eller fjerne organisationer fra et hierarki i et produktionsmiljø. Et lavere antal reducerer risikoen for, at der kan forekomme dyre fejl, der kræver, at der gennemføres rettelser.

## <a name="retail-store-management"></a>Detailbutiksstyring
I følgende tabel beskrives de scenarier for Oprindelsesdata til handel, hvor du kan bruge organisationshierarkier.
| Opgave                                                                           | Beskrivelse                                                                                                                                                                                                                                                                                                | Hierarkiformål    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Administrere detailudvalg                                                      | Identificer de produkter, der er tilgængelige i hver detailbutik.                                                                                                                                                                                                                                             | Detailudvalg    |
| Administrere detailgenopfyldning                                                    | Gruppér butikker for at genopfylde lagerbeholdningen baseret på reglerne for genopfyldning.                                                                                                                                                                                                                                          | Detailgenopfyldning |
| Rapportere data til butikker                                                         | Gruppér butikker til rapportering.                                                                                                                                                                                                                                                                                | Detailrapportering     |
| Bogføre lager, beregne opgørelser eller bogføre opgørelser for en gruppe af butikker | Opret en gruppe af butikker, der kan tildeles til et batchjob. Når du definerer et batchjob til bogføring af lager, beregning af opgørelser eller bogføring af opgørelser, kan du angive, hvilke hierarki jobbet gælder for. Når butikker føjes til eller fjernes fra hierarkiet, behøver du ikke ændre batchjobbet. | Retail POS-postering   |






