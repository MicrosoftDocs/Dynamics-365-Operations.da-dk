---
title: POS-forbedringer for serialiserede produkter
description: "Dette emne viser forbedringer, der er foretaget for serialiserede produkter, som kan hjælpe dig med at spare tid og blive mere produktiv."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 74a27761c065e475fa7c10c5812f0307df9f570e
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---

# <a name="pos-improvements-for-serialized-products"></a>POS-forbedringer for serialiserede produkter

[!INCLUDE [banner](includes/banner.md)]

## <a name="overview"></a>Overblik 
Baseret på indstillingerne i Retail Headquarters kan produkter klassificeres som enten serialiserede eller ikke-serialiserede. Når produkter er serialiserede, kan tildeles hver vare et entydigt nummer, der hjælper med at spore garantier, spore varer og bekræfte ejerskab. Selvom muligheden for at angive serienumre for serialiserede produkter fandtes i vores Modern/Cloud Point of Sale (POS), er der tilføjet nogle forbedringer, så kassererne kan spare tid og blive mere produktive.  

## <a name="pos-improvements"></a>POS-forbedringer

- **Serienumre er ikke nødvendige, før betaling ved kassen** – tidligere skulle en kasserer, der tilføjede et serialiseret produkt til transaktionen, angive et serienummer. Dette krav blev et problem i scenarier med kundeaktiviteter, hvis kasserere og salgsmedarbejdere havde en mulighed for mersalg af produkter. Indtil betalingstrinnet blev produkterne ofte opdateret i indkøbsvognen. Hver gang en kasserer tilføjede et nyt produkt, bad systemet derfor ham eller hende om serienummeret. Dialogboksen Serienummer indeholder nu knappen **Tilføj senere**. Derfor kan salgsmedarbejderen tilføje varen til transaktionen, men kan angive serienummeret senere. Salgsmedarbejdere kan hurtigt tilføje og erstatte serialiserede varer i indkøbsvognen, og derefter angive serienummeret lige inden betalingen ved kassen. Hvis serienummeret ikke er angivet for alle serialiserede produkter, får en kasserer, der forsøger at afslutte transaktionen, vist en fejlmeddelelse. Denne meddelelse angiver, at kassereren skal angive de manglende serienumre, før han eller hun kan fortsætte.

    For hver serialiseret vare, hvor serienummeret blev sprunget over, vises der en kommentar under transaktionslinjen. Denne kommentar angiver, at serienummeret ikke er blevet angivet for varen. Kassereren kan derfor hurtigt finde varer, der mangler et serienummer.

    En ny handling **Tilføj serienummer** angiver også serienummeret for varer, der mangler et serienummer. Når serienummeret er angivet, kan det ikke redigeres. Kassereren skal annullere linjen og tilføje produktet igen. 
    
- **Serienumre er ikke påkrævet ved afgivelse af kundeordrer** – Kundeordrer kan afgives i én butik og gennemføres fra en anden. En kasserer, der afgiver en kundeordre, behøver ikke at angive serienummeret. Serienummeret angives under trinnet med plukning eller afhentning. Der skal dog angives et serienummer for alle linjeelementer, hvor leveringstypen **Udfør** er markeret. Ellers kan transaktionen ikke fuldføres.    
- **Serialiserede produkter er ikke samlet på transaktionsskærmbilledet** – Indstillingen **Samling af produkter** i feltgruppen **Terminal** på siden **Funktionalitetsprofil** giver dig mulighed for at samle de samme ikke-serialiserede produkter på transaktionsskærmbilledet. Når de pågældende produkter samles, er de nemmere at se i transaktionsgitteret. Men da serienumre normalt er entydige, og salgsmedarbejderne ikke behøver at angive serienumre før ved betalingen ved kassen, gælder indstillingen **Samling af produkter** ikke for serialiserede produkter. Derfor samles serialiserede produkter ikke på transaktionsskærmbilledet., hvis indstillingen **Samling af produkter** er valgt.
- **Muligheden for at søge efter serienummer i kladderne** - Der kan nu også søges efter serienumre i kladderne. Det gør du ved at åbne handlingen "Kladder" og trykke på knappen "Avanceret søgning" på applinjen. Ved hjælp af knappen "Tilføj filter" kan et filter anvendes til at søge efter serienumrene også.

