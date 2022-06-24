---
title: Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov
description: Denne artikel beskriver, hvordan du bruger prissætningsprogrammet i Microsoft Dynamics 365 Supply Chain Management fra Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 259bdd5f868945c3857b045fbd3cbd4fceb26951
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862213"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management indeholder et prissætningsprogram, der håndterer samhandelsaftaler, prislister, fordelskundeprogrammer, kampagner og rabatter. Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre. Når du bruger dobbeltskrivning, skal du enten bruge statisk prissætning eller prissætningsprogrammet fra Supply Chain Management på **Tilbud**- og **Ordre**-siderne i Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Brug prissætningsprogrammet fra Supply Chain Management i Sales

1. Gå til **Sales \> Ordrer** i Sales.
1. Vælg **Ny** for at oprette en ny ordre eller vælg en eksisterende ordre på listen **Mine ordrer**.
1. Tilføj en ny ordrelinje.
1. Hvis du opretter en ny ordre, skal du vælge **Prisordre** i handlingsruden. Hvis du opdaterer en eksisterende ordre, skal du vælge **Omberegn** i handlingsruden.
1. Følgende kolonner udfyldes automatisk:

    - Detaljebeløb
    - Rabat %
    - Rabat
    - Beløb før fragt
    - Fragtbeløb
    - Moms i alt
    - Samlet beløb

> [!NOTE]
> En lignende proces anvendes, når du opretter tilbud.

## <a name="how-it-works"></a>Sådan fungerer det

Når du opretter en ordre i Sales, synkroniseres denne ordre med det samme til Supply Chain Management ved hjælp af de værdier, du har angivet i Sales. Når du vælger **Prisordre** eller **Pristilbud** i Sales, beregner Supply Chain Management prisen for hver ordrelinje og totalordren ud fra de samhandelsaftaleregler, der er defineret i Supply Chain Management. De nye beregnede værdier synkroniseres derefter tilbage til Sales.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Angive indstillinger for evaluering af samhandelsaftale i Supply Chain Management

Du kan konfigurere Supply Chain Management til enten at overholde eller ignorere samhandelsaftaler, når programmet beregner prisen på en ordre, der blev oprettet i Sales. Benyt denne fremgangsmåde for at konfigurere denne indstilling.

1. Log på dit Supply Chain Management-miljø.
1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Tilføj eller fjern rækken for politikken for **Manuel indtastning** efter behov i oversigtspanelet **Evaluering af samhandelsaftale** under fanen **Priser**. Tilstedeværelse eller fravær af denne politik bestemmer, om prissætningsprogrammet til Supply Chain Management automatisk tilsidesætter den salgspris, der blev angivet i Sales.

    - Hvis politikken **Manuel indtastning** *ikke* findes i opsætningen af **Evaluering af samhandelsaftale**, er Supply Chain Management prismasteren. Når en bruger vælger **Prisordre** eller **Pristilbud** i handlingsruden i Sales, kaldes prissætningsprogrammet i Supply Chain Management, og den salgspris, der blev angivet i Sales, overskrives , medmindre den er lig med den salgspris, der er beregnet i Supply Chain Management.
    - Hvis politikken **Manuel indtastning** *findes* i opsætningen af **Evaluering af samhandelsaftale**, er Sales prismasteren. Den salgspris, der blev angivet i Sales, forhindres i at blive overskrevet automatisk, når en bruger vælger **Prisordre** eller **Pristilbud** i handlingsruden i Sales.
    - Ordrelinjer og tilbudslinjer, der har en **Pris pr. enhed** og/eller **Rabat**-værdi på *0* (nul) i Sales, behandles som en særlig sag. Hvis der findes en relevant pris fra en samhandelsaftale, vil Supply Chain Management *altid* anvende den på disse felter, uanset opsætningen af **Samhandelsaftaleevaluering**.

    Du kan se et eksempel på hver af disse sager i de følgende scenarier.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Eksempelscenario 1: Evaluering af samhandelsaftale uden indstillingen Manuel indtastning

I dette scenario vil opsætningen af **Evaluering af samhandelsaftale** i Supply Chain Management *ikke* inkludere **Manuel indtastning** som politik. En Sales-bruger angiver en ordrelinje, der har en salgspris, der ikke er nul i Sales, og der er ikke defineret en salgspris for varen i Supply Chain Management.

1. I Sales opretter en bruger en ordrelinje, der har en **Pris pr. enhed**-værdi på 1 amerikansk dollar (USD).
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 1 USD.
1. I Sales vælger brugeren **Prisordre** i handlingsruden.
1. Supply Chain Management søger efter relevante priser og rabatter og beregner derefter totaler. Da varen ikke har nogen salgspris i Supply Chain Management, opdaterer beregningen linjen, så den har en salgspris på 0 USD.
1. Linjens nye salgspris synkroniseres tilbage til Sales.
1. Resultatet er en ordrelinje i Sales, der har en salgspris på 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Eksempelscenario 2: Evaluering af samhandelsaftale med indstillingen Manuel indtastning

I dette scenario vil opsætningen af **Evaluering af samhandelsaftale** i Supply Chain Management *inkludere* **Manuel indtastning** som politik. En Sales-bruger angiver en ordrelinje, der har en salgspris på ikke-nul i Sales. Supply Chain Management indeholder en samhandelsaftale, der angiver en salgspris på 2 USD for den bestilte vare.

1. I Sales opretter en bruger en ordrelinje for en vare, der har en **Pris pr. enhed**-værdi på 1 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 1 USD.
1. I Sales vælger brugeren **Prisordre** i handlingsruden.
1. Da konfigurationen **Evaluering af samhandelsaftale** i Supply Chain Management omfatter politikken **Manuel indtastning**, er salgsprisen ikke ændret, selvom der i en gældende samhandelsaftale er angivet en anden salgspris.
1. Salgsprisen forbliver uændret i Sales og Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Eksempel scenario3: Evaluering af samhandelsaftale for en vare, der har en salgspris på nul i Sales

I dette scenario vil opsætningen af **Evaluering af samhandelsaftale** i Supply Chain Management *inkludere* **Manuel indtastning** som politik. Sales-brugeren angiver en ordrelinje, der har en salgspris på 0 (nul) i Sales. Supply Chain Management indeholder en samhandelsaftale, der angiver en salgspris på 2 USD for en bestilt vare.

1. I Sales opretter en bruger en ordrelinje, der har en **Pris pr. enhed**-værdi af 0 USD og en værdi af **Linjerabat** på 0 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 0 USD.
1. Da den har modtaget en ordrelinje med en salgspris på 0 (nul), kalder Supply Chain Management dets prissætningsprogram, selvom indstillingen **Manuel indtastning** er aktiveret. Prissætningsprogrammet returnerer salgsprisen på 2 USD, der er oprettet af samhandelsaftalen, og opdaterer ordrelinjen i Supply Chain Management.
1. Den opdaterede salgspris er endnu ikke synkroniseret med ordrelinjen i Sales.
1. I Sales vælger brugeren **Prisordre** i handlingsruden.
1. Ordrelinjen i Supply Chain Management beholder salgsprisen på 2 USD, der nu synkroniseres tilbage til Sales. Værdien af **Pris pr enhed** for ordrelinjen i Sales opdateres derfor fra 0 USD til 2 USD.
1. I Sales angiver brugeren en ny værdi af **Linjerabat** på 0,50 USD. Nu beregner Sales, at værdien af **Udvidet beløb** for linjen er 1,50 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med værdi af **Linjerabat** på 0,50 USD.
1. I Sales vælger brugeren **Prisordre** i handlingsruden.
1. Der ændres ingen priser eller rabatter for ordrelinjen i Sales.

## <a name="limitations"></a>Begrænsninger

Når kolonnerne i Sales er udfyldt, gælder følgende begrænsninger:

- Opsætningen af gebyrer og gebyrtildelinger i Supply Chain Management replikeres ikke i Sales.
- Prissætningen tager ikke hensyn til den særlige detailpris, der er angivet i kolonnen **Detailkanal** på siden med salgsordrelinjer i Supply Chain Management.
- Rabatter, der er defineret i sektionen **Administration af handelstilladelse** i Supply Chain Management, tages ikke i betragtning.
- Prisfastsættelse tager ikke højde for salgsaftaler.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
