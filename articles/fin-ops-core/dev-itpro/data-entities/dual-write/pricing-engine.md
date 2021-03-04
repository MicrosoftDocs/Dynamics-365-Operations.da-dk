---
title: Synkronisere med Dynamics 365 Supply Chain Management-prissætningsprogrammet efter anmodning
description: Dette emne beskriver, hvordan du bruger prissætningsprogrammet i Dynamics 365 Supply Chain Management fra Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 740ae20704abd9c59f64c2c7622fa96d65dccb1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4451007"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Synkronisere med Dynamics 365 Supply Chain Management-prissætningsprogrammet efter anmodning

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management indeholder et prissætningsprogram, der håndterer samhandelsaftaler, prislister, fordelskundeprogrammer, kampagner og rabatter. Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre. Når du bruger dobbeltskrivning, skal du enten bruge statisk prissætning eller prissætningsprogrammet fra Dynamics 365 Supply Chain Management på tilbuds- og ordresiderne i Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Brug prissætningsprogrammet fra Supply Chain Management i Sales

1. Gå til **Sales \> Ordrer** i Sales.
2. Vælg **Ny** for at oprette en ny ordre eller vælg en eksisterende ordre på listen **Mine ordrer**.
3. Tilføj en ny ordrelinje.
4. Hvis du opretter en ny ordre, skal du vælge **Prisordre** i handlingsruden. Hvis du opdaterer en eksisterende ordre, skal du vælge **Omberegn** i handlingsruden.

    Følgende felter udfyldes automatisk:

    + Detaljebeløb
    + Rabat %
    + Diskontering
    + Beløb før fragt
    + Fragtbeløb
    + Moms i alt
    + Samlet beløb
    
5. For at sikre, at der tages hensyn til handels-og salgsaftaler i beregning af prisen:
    1. Naviger til dit Supply Chain Management-miljø.
    2. Naviger til **Debitor \> Opsætning \> Debitorparametre**.
    3. Vælg fanen **Priser** på sidens navigationslinje.
    4. Fjern markeringen i afkrydsningsfeltet **Manuel indtastning** i oversigtspanelet **Evaluering af samhandelsaftale**.

## <a name="how-it-works"></a>Sådan fungerer det

Når du vælger **Prisordre** i Sales, kaldes funktionen **Totaler** under **Salgsordre \> fanen Visning** i Supply Chain Management for den tilknyttede salgsordre. Værdierne i ordretotalen bruges i Sales til at udfylde de tilsvarende felter i Supply Chain Management.

Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende samhandelsaftaler og salgsaftaler for kunden og de produkter, der er angivet i salgsordren. Oplysningerne bruges til at beregne totalerne. Når du har valgt **Prisordre**, afspejler Sales automatisk alle de opsætninger, der er udført i Supply Chain Management.

## <a name="limitations"></a>Begrænsninger

Når felterne i Sales er udfyldt, gælder følgende begrænsninger:

+ Opsætningen af gebyrer og gebyrtildelinger i Supply Chain Management replikeres ikke i Sales.
+ Prissætningen tager ikke hensyn til den særlige detailpris, der er angivet i feltet **Detailkanal** på siden med salgsordrelinjer i Supply Chain Management.
+ Rabatter, der er defineret i sektionen **Administration af handelstilladelse** i Supply Chain Management, tages ikke i betragtning.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]