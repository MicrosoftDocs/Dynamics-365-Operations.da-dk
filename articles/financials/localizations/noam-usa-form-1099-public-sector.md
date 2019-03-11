---
title: 1099-blanket i den offentlige sektor
description: Denne artikel indeholder tip og oplysninger om opsætning af 1099-blanketfunktionalitet til Kreditor i den offentlige sektor.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 26181
ms.assetid: 10f56dea-ea2d-48ea-9622-4ef715eb1179
ms.search.region: USA
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8154bc9d87f00561aaf89f538389ccf41e666f21
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370237"
---
# <a name="form-1099-in-the-public-sector"></a>1099-blanket i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder tip og oplysninger om opsætning af 1099-blanketfunktionalitet til Kreditor i den offentlige sektor.

1099-skatteblanketten er obligatorisk, hvis du handler med leverandører, der er underlagt amerikansk 1099-skat. I dette emne beskrives de 1099-funktioner, som er tilgængelige for den offentlige sektor. Det anbefales også, at du gennemgår det amerikanske skattevæsens (IRS) regelændringer for det pågældende skatteår, før du opretter og behandler 1099-opgørelser. Hvis du handler med leverandører, der er omfattet af amerikansk 1099-skat, skal du spore det beløb, du betaler til hver leverandør, og rapportere disse oplysninger til de amerikanske skattemyndigheder ved udgangen af kalenderåret. Leverandørerne er typisk virksomheder, der leverer ydelser til din organisation. Leverandørerne kan også være personer, der ikke er medarbejdere. Du skal også sende en opgørelse til hver 1099-leverandør, du handler med, for at oplyse leverandøren om det beløb, du indberetter til skattemyndighederne. Offentlige juridiske organisationer, der har en primær adresse i USA, kan sende blanketten 1099-G eller 1099-S til det amerikanske skattevæsen. 1099-G-indkomstskatteblanketten bruges til at rapportere indkomst fra myndighedskilder, som f.eks. statslige eller lokale skatterefusioner, ydelser ved arbejdsløshed eller tilskud. 1099-S indkomstskatteblanketten bruges til at rapportere indtægter fra salg eller skifte af visse typer af fast ejendom. I Microsoft Dynamics 365 for Finance and Operations skal 1099-opsætningsprocedurerne som regel kun fuldføres én gang. Du kan dog bruge oplysningerne senere, hvis du vil redigere eller få vist eksisterende poster.

## <a name="tips"></a>Tip!
-   Du har muligvis bemærket, at på mange sider findes feltet **s-2-bruttoudbytte** ikke. Dette felt vises ikke, hvis beløbet er det samme som beløbet i feltet **Afregnet 1099 på forbundsniveau**.
-   Der er tilknyttet en individuel 1099-rapport til hver 1099-S-faktura. Du kan bruge rapporten **1099-skat, detaljer** til at få vist detaljerede 1099-S-oplysninger.
-   På linjerne i mange af kladderne kan du ikke indtaste et S-2-beløb. Dette beløb er det samme som i feltet 1099-beløb. Du kan dog angive S-2-oplysninger under fanen **1099** på disse sider. Derudover kan du ikke vælge **S-5** på disse sider, da du skal indtaste dette beløb manuelt i feltet **S-5 købers del af ejendomsskat**.

## <a name="how-do-i-view-or-specify-vendor-settlement-for-1099s"></a>Hvordan få vist eller angiver kreditorudligning for 1099?
Du kan bruge siden **Kreditorudligning for 1099** til at angive eller få vist de 1099-beløb der gælder for dine kreditorer, til at forberede 1099-erklæringer, til at udskrive kopier til kreditorer og til at oprette eksportfiler. Den person eller organisation, der er udpeget som 1099-afsender, kan sende 1099-erklæringer til IRS ved anvendelse af magnetiske medier eller ved at indgive dem elektronisk. Du kan også vælge en kreditorkonto på siden **Alle kreditorer** i enten Kreditor eller Indkøb og forsyning ved at klikke på **Kreditor** i handlingsruden og derefter klikke på **Kreditorudligning for 1099**. **Noter**

-   Du kan ændre værdien i feltet **Rubrik i 1099** i oversigtspanelet **Rapporter 1099** på siden med kreditoroplysninger. Hvis du vælger **G-2** og prøver at opdatere alle kreditorposter, vil du blive bedt om at bekræfte opdateringen. Der angives typisk kun G-2-oplysninger efter en omhyggelig analyse af en individuel kreditor.
-   På siden **Kreditorudligning for 1099**, selvom et S-2 beløb er mindre end minimumkravet, skal det muligvis stadig rapporteres til det amerikanske skattevæsen. S-2 beløbet kan f.eks. være 0 (nul), og **S-4-overførsel eller modtaget ejendom eller ydelser** indstillingen er valgt. I dette tilfælde indstillingen **Indberettes til det amerikanske skattevæsen (IRS)?** også valgt.

## <a name="how-do-i-update-1099-information"></a>Hvordan opdaterer jeg 1099-oplysninger?
Du kan også bruge siden **Kreditorudligning for 1099** til at angive eller opdatere 1099-oplysninger for en kreditor. Du kan opdatere standardminimumbeløbene for blanketfelter i 1099-G eller 1099-S, hvis de er inkluderet. **Noter**

-   Visse felter er udeladt med vilje. **S-5**-feltet er f.eks. udeladt, fordi det bruges til ejendomsskatter, og der gælder ikke noget minimumbeløb i forhold til det amerikanske skattevæsen. Du kan også konfigurere 1099-G- og 1099-S-beløb på denne side, men det er stadig ikke muligt at spore og udskrive 1099-G- eller 1099-S-kreditoroplysninger.
-   Hvis et enkelt beløb på en side er større end minimumbeløbet, kan det amerikanske skattevæsen kræve, at alle beløb rapporteres, selvom alle andre beløb er mindre end minimumbeløbet.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Kreditor i den offentlige sektor](../public-sector/accounts-payable-public-sector.md)



