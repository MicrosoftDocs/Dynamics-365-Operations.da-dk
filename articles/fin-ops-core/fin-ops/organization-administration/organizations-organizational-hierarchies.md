---
title: Oversigt over organisationer og organisationshierarkier
description: En organisation er en grupper personer, der arbejder sammen for at udføre en forretningsproces eller nå et mål. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc9064f0386fe7c0f4093fc30587be4baa259eb0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003673"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Oversigt over organisationer og organisationshierarkier

[!include [banner](../includes/banner.md)]

En organisation er en grupper personer, der arbejder sammen for at udføre en forretningsproces eller nå et mål. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af.

## <a name="organizations"></a>Organisationer

Du kan definere følgende typer interne organisationer: juridiske enheder, driftsenheder og team.

Alle interne organisationer er typer af enheden **Part**. Disse organisationer benytter derfor adressekartoteket til opbevaring af adresser og kontaktoplysninger. En par, som kan være enten en person eller en organisationer, kan tilhøre et eller flere adressekartoteker.

### <a name="legal-entities"></a>Juridiske enheder

En juridisk enhed er en organisation, der består af en registreret eller lovgivningsbaseret juridisk struktur. Juridiske enheder kan indgå juridisk bindende kontrakter og skal udarbejde opgørelser med afrapportering af deres præstation.

Et firma er en type juridisk enhed. I øjeblikket er firmaer den eneste slags juridiske enhed, som du kan oprette, og hver juridiske enhed får tilknyttet et firma-id. Denne tilknytning findes, da nogle funktionsområder i programmet bruger et firma-id, eller DataAreaId, i deres datamodeller. Firmaer bruges som en afgrænsning for datasikkerhed i disse funktionsområder. Brugere har kun adgang til data for det firma, som de er logget på.

### <a name="operating-units"></a>Driftsenheder

En driftsenhed er en organisation, der bruges til at opdele administrationen af økonomiske ressourcer og driftsprocesser i et firma. Personer i en driftsenhed er forpligtet til at maksimere brugen af knappe ressourcer, til at forbedre processer og til at redegøre for deres præstation.

Typerne af driftsenheder omfatter bærere, virksomhedsenheder, værdistrømme, afdelinger og handelskanaler. Tabellen nedenfor indeholder flere oplysninger om hver type driftsenhed.

| Type driftsenhed | Beskrivelser | Formål |
|---------------------|-------------|---------|
| Bærer         | En driftsenhed, hvor lederne er ansvarlige for de budgetterede og faktisk udgifter. | Bruges til administration og driftsstyring af forretningsprocesser i de juridiske enheder. |
| Virksomhedsenhed       | En halvautomatisk driftsenhed, der er skabt for at nå strategiske forretningsmålsætninger. | Bruges til regnskabsaflægning, der er baseret på brancher eller produktlinjer, som organisationen betjener uafhængigt af juridiske enheder. |
| Værdistrøm        | En driftsenhed, der kontrollerer en eller flere produktionsflow. | Bruges normalt ved lean produktion til kontrol af aktiviteter og flow, der er påkrævet for at levere et produkt eller en tjeneste til forbrugere. |
| Afdeling          | En driftsenhed, der repræsenterer en kategori eller funktionel del af en organisation, der udfører en bestemt opgave, som f.eks. salg eller regnskab. | Bruges til afrapportering for funktionelle områder. En afdeling kan have ansvar for driftsregnskabet og kan bestå af en gruppe af bærere. |
| Handelskanal      | En driftsenhed, der repræsenterer en fysisk butik, en onlinebutik eller en onlinemarkedsplads. | Bruges til styring og driftskontrol af en eller flere butikker inden for eller på tværs af juridiske enheder. |

### <a name="teams"></a>Team

Et team er en organisation, hvis medlemmer deler et fælles ansvar, en fælles interesse eller en fælles målsætning. Teams kan ikke bruges i organisationshierarkier.

## <a name="organizational-hierarchies"></a>Organisationshierarkier

Opret organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden. Du kan f.eks. oprette et hierarki for juridiske enheder til skattemæssig, juridisk eller lovpligtig rapportering. Opret et hierarki, der er baseret på driftsenheder, for at rapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til intern kontrol. Du kan f.eks. oprette et indkøbshierarki for at kontrollere indkøbspolitikker, regler og forretningsprocesser.

Hvert hierarki er tildelt et formål. Formålet med et hierarki afgør, hvilke organisationstyper der kan medtages i hierarkiet. Formålet definerer også de anvendelsesscenarier, hierarkiet kan bruges i.

Organisationer i et hierarki kan dele parametre, politikker og transaktioner. En organisation kan nedarve eller tilsidesætte parametrene for dens overordnede organisation. Delte masterdata, som f.eks. produkter og adressekartoteker, gælder for hele organisationen og kan ikke tilsidesættes for individuelle organisationer. Oprettelse af organisationer og hierarkier kræver omhyggelig planlægning. Du kan finde flere oplysninger under [Planlæg dit organisationshierarki](plan-organizational-hierarchy.md).
