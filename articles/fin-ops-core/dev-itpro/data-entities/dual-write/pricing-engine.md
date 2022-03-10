---
title: Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov
description: Dette emne beskriver, hvordan du bruger prissætningsprogrammet i Dynamics 365 Supply Chain Management fra Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 134bfc2ec0e69938c945e384a98676d3708c8e17
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783301"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management indeholder et prissætningsprogram, der håndterer samhandelsaftaler, prislister, fordelskundeprogrammer, kampagner og rabatter. Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre. Når du bruger dobbeltskrivning, skal du enten bruge statisk prissætning eller prissætningsprogrammet fra Dynamics 365 Supply Chain Management på tilbuds- og ordresiderne i Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Brug prissætningsprogrammet fra Supply Chain Management i Sales

1. Gå til **Sales \> Ordrer** i Sales.
2. Vælg **Ny** for at oprette en ny ordre eller vælg en eksisterende ordre på listen **Mine ordrer**.
3. Tilføj en ny ordrelinje.
4. Hvis du opretter en ny ordre, skal du vælge **Prisordre** i handlingsruden. Hvis du opdaterer en eksisterende ordre, skal du vælge **Omberegn** i handlingsruden.

    Følgende kolonner udfyldes automatisk:

    + Detaljebeløb
    + Rabat %
    + Diskontering
    + Beløb før fragt
    + Fragtbeløb
    + Moms i alt
    + Samlet beløb
    
5. For at sikre, at der tages hensyn til handelsaftaler i beregning af prisen:
    1. Naviger til dit Supply Chain Management-miljø.
    2. Naviger til **Debitor \> Opsætning \> Debitorparametre**.
    3. Vælg fanen **Priser** på sidens navigationslinje.
    4. Fjern markeringen i afkrydsningsfeltet **Manuel indtastning** i oversigtspanelet **Evaluering af samhandelsaftale**.

## <a name="how-it-works"></a>Sådan fungerer det

Når du vælger **Prisordre** i Sales, kaldes funktionen **Totaler** under **Salgsordre \> fanen Visning** i Supply Chain Management for den tilknyttede salgsordre. Værdierne i ordretotalen bruges i Sales til at udfylde de tilsvarende kolonner i Supply Chain Management.

Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende samhandelsaftaler for kunden og de produkter, der er angivet i salgsordren. Oplysningerne bruges til at beregne totalerne. Når du har valgt **Prisordre**, afspejler Sales automatisk alle de opsætninger, der er udført i Supply Chain Management.

## <a name="limitations"></a>Begrænsninger

Når kolonnerne i Sales er udfyldt, gælder følgende begrænsninger:

+ Opsætningen af gebyrer og gebyrtildelinger i Supply Chain Management replikeres ikke i Sales.
+ Prissætningen tager ikke hensyn til den særlige detailpris, der er angivet i kolonnen **Detailkanal** på siden med salgsordrelinjer i Supply Chain Management.
+ Rabatter, der er defineret i sektionen **Administration af handelstilladelse** i Supply Chain Management, tages ikke i betragtning.
+ Prisfastsættelse tager ikke højde for salgsaftaler.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
