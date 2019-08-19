---
title: Generelle budgetreservationer
description: Dette emne indeholder oplysninger om generelle budgetreservationer i den offentlige sektor i Microsoft Dynamics 365 for Finance and Operations.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 674e9ef83caa095d71dc725f3f25368b17b4a91c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845831"
---
# <a name="general-budget-reservations"></a>Generelle budgetreservationer

[!include [banner](../includes/banner.md)]

En *generel budgetreservation* er et dokument, der undertiden også kaldes en *forpligtelse*. Offentlige myndigheder bruger ofte dette dokument til at afsætte eller øremærke budgetterede midler, så de ikke er tilgængelige til andre formål. Disse reservationer foretages typisk før, eventuelle leverandører er valgt til indkøbet. Ved hjælp af generelle budgetreservationer kan en organisation udtrykkeligt spore planlagte udgifter til administrations- og rapporteringsformål. Hver enkelt indkøbsrekvisition, indkøbsordre eller kreditorfaktura, der er genereret, kan knyttes til mindst én generel budgetreservation.

Generelle budgetreservationer er kun tilgængelige, hvis følgende betingelser er opfyldt:

- Du har Microsoft Dynamics 365 for Finance and Operations version 8.1 (oktober 2018) eller en nyere version.
- Konfigurationsnøglerne **Offentlig sektor**, **Behæftelsesproces** og **Budgetreservationsproces** er aktiveret.
- Du bruger bogføringsdefinitioner. (Du behøver dog ikke at bruge bogføringsdefinitioner, hvis du ikke aktiverer rammeaftaler).
- Konfigurationen af budgetstyring er aktiveret og konfigureret, og budgetstyring er slået til.

Generelle budgetreservationer indeholder linjer, der indeholder detaljer om formålet med reservationen og de planlagte reserverede midler. Disse oplysninger omfatter reservationens start- og slutdato. Du kan tilføje, ændre og slette linjer. Du kan også angive forskellige oplysninger, f.eks. den anmodede vare, valutaen, enhedsprisen og antallet og det samlede beløb. Generelle budgetreservationer er beregnet til brug af enheder i den offentlige sektor.

Enheder i den private sektor bruger udtrykket *budgetreservation* til at tale om behæftelser eller budgetreservationer. Men i modsætning til generelle budgetreservationer er disse budgetreservationer ikke dokumenter.

Du kan oprette forskellige typer generelle budgetreservationer for at angive forskellige egenskaber og krav baseret på dine indkøbsbehov. Specifikationerne omfatter den arbejdsgang, der bruges til reservationen, og standardværdier. Du opretter f.eks. tre reservationstyper. Du bruger én type til indkøbsrekvisitioner, en anden type til indkøbsordrer og endnu en type til kreditorfakturaer.

I den generelle budgetreservation kan du også få vist regnskabsfordelinger og kladdelinjerne for reskontro for posteringen.

Hvis du bruger projektregnskab, kan du aktivere sporing af bindende omkostninger for generelle budgetreservationer.

Du kan overføre generelle budgetreservationer fra det ene regnskabsår til det andet. Du kan også lukke eller færdiggøre en afsluttet eller udløbet generel budgetreservation i slutningen af året.

En generel budgetreservation eftergives på forskellige måder, afhængigt af det dokument, der refererer til den:

- Hvis dokumentet er en indkøbsordre, eftergives reservationen, når indkøbsordren er *bekræftet*.
- Hvis dokumentet er en faktura, som ikke henviser til en indkøbsordre eller købsaftale, eftergives den generelle budgetreservationen, når fakturaen *bogføres*.
- Hvis dokumentet er en indkøbsrekvisition, eftergives reservationen, når indkøbsrekvisitionen er *godkendt*.
