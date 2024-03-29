---
title: Generelle budgetreservationer
description: Denne artikel indeholder oplysninger om generelle budgetreservationer i den offentlige sektor.
author: brpotter
ms.date: 08/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.search.industry: Public sector
ms.search.form: BudgetReservation_PSN
ms.openlocfilehash: 61fb3e48ac177be9cb0a2be2a89511d79788c5e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275863"
---
# <a name="general-budget-reservations"></a>Generelle budgetreservationer

[!include [banner](../includes/banner.md)]

En *generel budgetreservation* er et dokument, der undertiden også kaldes en *forpligtelse*. Offentlige myndigheder bruger ofte dette dokument til at afsætte eller øremærke budgetterede midler, så de ikke er tilgængelige til andre formål. Disse reservationer foretages typisk før, eventuelle leverandører er valgt til indkøbet. Ved hjælp af generelle budgetreservationer kan en organisation udtrykkeligt spore planlagte udgifter til administrations- og rapporteringsformål. Hver enkelt indkøbsrekvisition, indkøbsordre eller kreditorfaktura, der er genereret, kan knyttes til mindst én generel budgetreservation.

Generelle budgetreservationer er kun tilgængelige, hvis følgende betingelser er opfyldt:

- Du har version 8.1 eller nyere.
- Konfigurationsnøglerne **Offentlig sektor**, **Behæftelsesproces** og **Budgetreservationsproces** er aktiveret.
- Du bruger bogføringsdefinitioner. (Du behøver dog ikke at bruge bogføringsdefinitioner, hvis du ikke aktiverer rammeaftaler).
- Konfigurationen af budgetstyring er aktiveret og konfigureret, og budgetstyring er slået til.

Generelle budgetreservationer indeholder linjer, der indeholder detaljer om formålet med reservationen og de planlagte reserverede midler. Disse oplysninger omfatter reservationens start- og slutdato. Du kan tilføje, ændre og slette linjer. Du kan også angive forskellige oplysninger, f.eks. den anmodede vare, valutaen, enhedsprisen og antallet og det samlede beløb. Generelle budgetreservationer er beregnet til brug af enheder i den offentlige sektor.

Enheder i den private sektor bruger udtrykket *budgetreservation* til at tale om behæftelser eller budgetreservationer. Men i modsætning til generelle budgetreservationer er disse budgetreservationer ikke dokumenter.

Du kan oprette forskellige typer generelle budgetreservationer for at angive forskellige egenskaber og krav baseret på dine indkøbsbehov. Specifikationerne omfatter den arbejdsgang, der bruges til reservationen, og standardværdier. Du opretter f.eks. tre reservationstyper. Du bruger én type til indkøbsrekvisitioner, en anden type til indkøbsordrer og endnu en type til kreditorfakturaer.

I den generelle budgetreservation kan du også få vist regnskabsfordelinger og kladdelinjerne for reskontro for posteringen.

> [!NOTE]
> Finanskonti, der bruges i generelle budgetreservationer, skal medtages i budgetstyring. Hvis disse konti ikke er inkluderet i budgetstyring, sker følgende. 
>- Generel budgetreservation og deres forbrugende dokumenter behæftes ikke eller behæftes på forhånd. 
>- Med overførsler oprettes der ikke budgetregisterposter. 
>- Annullering og færdiggørelse af generelle budgetreservationer reducerer ikke det oversendte budget.
>- Finanskonti medtages ikke i forespørgslerne til budgetanalyser og budgetstyring.

Hvis du bruger projektregnskab, kan du aktivere sporing af bindende omkostninger for generelle budgetreservationer.

Du kan overføre generelle budgetreservationer fra det ene regnskabsår til det andet. Du kan også lukke eller færdiggøre en afsluttet eller udløbet generel budgetreservation i slutningen af året.

En generel budgetreservation eftergives på forskellige måder, afhængigt af det dokument, der refererer til den:

- Hvis dokumentet er en indkøbsordre, eftergives reservationen, når indkøbsordren er *bekræftet*.
- Hvis dokumentet er en faktura, som ikke henviser til en indkøbsordre eller købsaftale, eftergives den generelle budgetreservationen, når fakturaen *bogføres*.
- Hvis dokumentet er en indkøbsrekvisition, eftergives reservationen, når indkøbsrekvisitionen er *godkendt*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
