---
title: Plan for forbrugerprisindeks
description: Dette emne forklarer, hvordan du opretter listen over CPI-planer (forbrugerprisindeks), som du får fra internettet, og som er med til at bestemme eskaleringsgebyret i abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2a69e58095844286878e27a100fa49a44a4a71f4
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560475"
---
# <a name="consumer-price-index-schedule"></a>Plan for forbrugerprisindeks

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du kan oprette, slette, gennemse og behandle CPI-planer (forbrugerprisindeks). En CPI-plan kan bruges til at fastlægge priserne på forbrugsvarer og -tjenester, som du tilføjer som faktureringsplanlinjer. CPI-planen kan derefter bruges til eskalering og rabatprissætning på en faktureringsplan, eller den kan behandles manuelt for at opdatere faktureringsbeløbene i faktureringsplaner. Du kan angive CPI-planer manuelt, eller du kan importere dem ved at bruge den sammensatte enhed til CPI-plan.

Hvis du vil tilføje en CPI-plan, skal du følge disse trin.

1. På siden **Plan for forbrugerprisindeks** skal du vælge **Ny**.
2. Angiv et entydigt navn i feltet **Plan for forbrugerprisindeks**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Under fanen **Plan for forbrugerprisindeks** skal du vælge **Tilføj**.
5. Angiv den dato, hvor den nye CPI-plan bliver aktiv, i feltet **Dato for forbrugerprisindeks**.
6. Angiv det navn, du angav i trin 2, i feltet **Plan for forbrugerprisindeks**.
7. Vælg **Gem**.

Følg disse trin for at slette en dato for en CPI-plan.

1. Markér en eller flere linjer, som du vil slette, på siden **Plan for forbrugerprisindeks**, og vælg derefter **Fjern**.
2. Hvis du vil slette hele CPI-planen, skal du vælge **Slet** i handlingsruden. Du kan ikke slette den valgte CPI-plan, hvis den er knyttet til en faktureringsplan.
3. Vælg **Behandling** i handlingsruden for at opdatere de faktureringsplaner, der bruger den valgte CPI-plan. De seneste CPI-datoer og planbeløb bruges til at opdatere faktureringsplanens priser.
4. I oversigtspanelet **Proces for forbrugerprisindeks** kan du gennemse de opdaterede felter med **Faktureringsplannummer**, **Varenummer**, **Faktureringsstartdato**, **Faktureringsslutdato**, **Eskaleringsdato** og **Eskaleringsfrekvens**.

Når CPI-planer er konfigureret, kan de bruges til eskalering og rabatprisændringer i forbindelse med faktureringsplaner.

## <a name="cpi-calculation"></a>CPI-kalkulation

I disse eksempler er perioden fra 1. januar 2020 til og med 31. december 2022. CPI-basissatsen (CPI-værdien, når kontrakten starter) er 105,65. Den 1. januar 2021 er den aktuelle CPI 110,5. Den 1. januar 2022 er den aktuelle CPI 114,25. Det indledende beløb er $1.000.

**Eksempel 1**

På siden **Faktureringsparametre for tilbagevendende kontrakter** angiver du feltet **Beregning af forbrugerprisindeks** til **Basisforbrugsprisindeks**.

Det første eskaleringsbeløb beregnes for perioden 1. januar 2021 på følgende måde baseret på det indledende beløb:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Eskaleringsbeløbet beregnes for perioden 1. januar 2022 på følgende måde:

1.000 + (114,25 – 105,65) &divide; 105,65 &times; 1.000 = 1.081,40

**Eksempel 2**

På siden **Faktureringsparametre for tilbagevendende kontrakter** angiver du feltet **Beregning af forbrugerprisindeks** til **Tidligere forbrugsprisindeks**.

Det første eskaleringsbeløb beregnes for perioden 1. januar 2021 på følgende måde baseret på det indledende beløb:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Eskaleringsbeløbet beregnes for perioden 1. januar 2022 på følgende måde baseret på det første eskaleringsbeløb:

1.045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1.045,91 = 1.081,40

> [!NOTE]
> I eskaleringsprocessen bruges altid den seneste CPI-værdi uanset indeksdatoen. Hvis eskaleringen f.eks. er i september, men den seneste CPI-værdi er for juli, bruges indekset for juli. Der foretages ingen justeringer, efter at indekset i september er angivet.

## <a name="prorated-escalation"></a>Forholdsmæssig eskalering

Hvis eskaleringen sker midt i en faktureringsperiode, er beløbet forholdsmæssigt. Faktureringsperioden er f.eks. fra 1. august 2020 til og med 31. juli 2021. På CPI-datoen 1. september 2019 er CPI-værdien 244. På CPI-datoen 1. september 2020 er CPI-værdien 250. Hvis den tidligere sats er 1.000, bruges følgende formler til beregning af faktureringsbeløbet for perioden:

* *CPI-ændringer* = (250 – 244) &divide; 244 = 2,459 %
* *Aktuel sats* = 1.000 &times; 2,459 % = 1.024,59
* *Antal dage med den aktuelle sats* = 31. juli 2021 – 1. september 2020 = 334
* *Tidligere sats* = 1.000
* *Antal dage med den tidligere sats* = 31. august 2020 – 1. august 2020 = 31
* *Det samlede antal dage i faktureringsperioden* = 31. juli 2021 – 1. august 2020 + 1 = 365
* *Faktureringsbeløb for denne periode* = (1.000 &times; 31 &divide; 365) + (1.024,59 &times; 334 &divide; 365) = 1.022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalering, der bruger CPI og procentdel

Eskaleringer kan udføres ved hjælp af CPI. CPI plus en eskalering på 3 procent starter den 1. januar 2020, og den har en årlig frekvens.

- Det beløb, der faktureres for 1. januar 2019 til og med 31. december 2020, er 4.000.
- Den faktureringsperiode, der eskaleres, er 1. januar 2020 til og med 31. december 2020.
- På CPI-datoen 1. december 2018 er CPI-værdien 205,3. På CPI-datoen 1. december 2019 er CPI-værdien 219,6.

Hvis den tidligere sats er 4.000, bruges følgende formler til beregning af faktureringsbeløbet for denne periode:

- *CPI-ændringer* = (219,6 – 205,3) &divide; 205,3 = 6,965 %
- *Aktuel sats* = (4.000 &times; 6,965 %) – 4000 = 278,60
- *Procentændringer* = (4.000 &times; 1,03) – 4.000 = 120
- *Faktureringsbeløb* = 4.000 + 278,6 + 120 = 4.398,6
