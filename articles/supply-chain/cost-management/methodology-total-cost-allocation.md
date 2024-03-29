---
title: Metode til samlet omkostningsfordeling
description: Denne artikel indeholder retningslinjer for brug af samlet omkostningstildeling (TCA). Samlet omkostningstildeling er en metode til beregning af omkostningerne mellem den vigtigste formelvare for en batchordre og de samprodukter, der er defineret i formlen.
author: JennySong-SH
ms.date: 04/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 213db8303c27934050f5b414a67f6e510486dc94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862679"
---
# <a name="total-cost-allocation-method"></a>Metode til samlet omkostningsfordeling

[!include [banner](../includes/banner.md)]

Samlet omkostningstildeling (TCA) er en metode til beregning af omkostningerne mellem den vigtigste formelvare for en batchordre og de samprodukter, der er defineret i formlen. Denne metode er dynamisk. Omkostningen beregnes som et vægtet gennemsnit mellem de mængder, der er færdigmeldt for formelvaren og samprodukterne. Når TCA anvendes, behøver du ikke at gennemgå omkostningstildelinger for hver batchordre. Hvis TCA ikke bruges, bruger formelberegningen eksisterende funktionalitet.

## <a name="using-tca-for-coproducts"></a>Bruge TCA til samprodukter
Her er nogle af retningslinjerne for brug af TCA for samprodukter:

-   Hvis du indstiller skyderen **Samlet omkostningstildeling** til **Ja** for en formelversion, skal samprodukter have en kostpris, der er større end 0 (nul). Værdien kan hentes fra den aktive omkostningsversion for det samme sted eller til det første websted for en formel, der ikke er lokationsspecifik. Denne betingelse valideres, når formlen er godkendt.

    -   Du behøver ikke at angive omkostningsfordelingsprocenter for samprodukter manuelt. I stedet opretter systemet automatisk omkostningsfordelingsprocenten som gennemsnittet af de aktive kostpriser for samprodukter. 
    -   Du behøver ikke at angive standardkostpris for ikke-standardiserede omkostningselementer, der er samprodukter. Der findes to typer efterkalkulationsversioner i systemet: standardkostpris og planlagt omkostning 
    -   Hvis en vare ikke vurderes af metoden til evaluering af standardomkostninger, anbefales det, at du bruger en aktiv kostpris i versionen med planlagte omkostninger. Denne pris bruges til forkalkulation, f.eks., styklistekalkulation, forkalkulation af produktionsomkostninger og reserveprincipprisen i lagervurderingsprocessen. 

-   Hvis du indstiller skyderen **Samlet omkostningstildeling** til **Ja** for formelversionen og følgende betingelser er opfyldt, er metoden til omkostningstildeling **TCA**, og procentdelen af omkostningstildeling er uændret:
    -   Du har tilføjet samprodukter.
    -   Du har brugt en anden metode til omkostningstildeling for samprodukterne.
-   Hvis du indstiller skyderen **Samlet omkostningstildeling** til **Nej** for formelversionen og følgende betingelser er opfyldt, ændres metoden til omkostningstildeling til **Manuelt**, og procentdelen af omkostningstildeling er uændret:
    -   Du har tilføjet samprodukter.
    -   Procentdelen af omkostningstildelingen er mere end 0 (nul).
-   Før du kan udføre en beregning af formler, skal du vurdere procentsatser for omkostningstildelingen. Du kan udføre dette trin, enten manuelt eller ved hjælp af indstillingen **Forkalkulér omkostning** på siden **Samprodukter**. **Bemærk!** Indstillingen **Forkalkulér omkostning** er kun tilgængelig, når skyderen **Samlet omkostningstildeling** er indstillet til **Ja** for formelversionen. Du kan få vist den forventede fordeling, hvis de batch ordre-mængder, der er færdigmeldt, svarer til de mængder, der vises på formlen.
-   Når en batchordre oprettes manuelt, eller en planlagt batchordre autoriseres, kopieres værdien af skyderen **Samlet omkostningstildeling** for formelversionen til batchordren. Du kan dog ændre denne indstilling på batchordren. Hvis skyderen **Samlet omkostningstildeling** er indstillet til **Nej** for formelversionen og derefter ændres til **Ja** for batchordren, ændres metoden til omkostningstildeling for hver linje, der var angivet til **Manuel** til **TCA**. En omkostningstildeling på **Ingen** ændres ikke. Hvis skyderen **Samlet omkostningstildeling** er indstillet til **Ja** for formelversionen og derefter ændres til **Nej** for batchordren, ændres metoden til omkostningstildeling for hvert samprodukt af typen **Produktion** til **Manuel**. En anslået procentdel af omkostningstildelingen er uændret.
-   Siden **Omkostningstildeling for samprodukt** viser den beregnede procentdel af den samlede omkostningstildeling. Du kan åbne denne side fra siden **Batchordre**. Disse oplysninger er nyttige, når de produkter og mængder, der er rapporteret, adskiller sig fra de planlagte eller igangsatte mængder på batchordren. Når omkostningen er fuldført, vises disse nye procentvise allokeringer fra TCA på siden **Omkostningstildeling for samprodukt**.

## <a name="calculating-the-burden-for-byproducts"></a>Beregning af byrden for biprodukter
Feltet **Omkostningstildeling for biprodukt** på siden **Samprodukter** er et optællerfelt, der bruges kun til biprodukter. For samprodukter er værdien af dette felt er altid **Ingen**. Dette felt bestemmer, hvordan kostbeløbet for biproduktlinjen føjes til de samlede produktionsomkostninger for biproduktlinjer. Følgende valgmuligheder er tilgængelige:

-   **Ingen** – Der lægges ikke noget beløb til de samlede produktionsomkostninger for denne biproduktlinje.
-   **Procent** – Kostbeløbet beregnes som en procentdel af de samlede omkostninger til råmaterialer, der forbruges i produktionen. Den procentsats, der bruges til beregning, angives i feltet.
-   **Pr. serie** – Kostbeløbet beregnes som et beløb pr. standardbatchstørrelse af produktionsordren. Dette beløb er uafhængig af den mængde, der er rapporteret i produktionen. Det beløb, der bruges til beregningen, angives i feltet.
-   **Pr. antal** – Kostbeløbet beregnes som et beløb pr. rapporterede antal af formelvaren i produktionen. Det beløb, der bruges til beregningen, angives i feltet.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]