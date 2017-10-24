---
title: Callcenter-funktionalitet
description: Denne artikel indeholder en oversigt over call center-salgsfunktioner i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-functionality"></a>Callcenter-funktionalitet

[!include[banner](includes/banner.md)]


Denne artikel indeholder en oversigt over call center-salgsfunktioner i Microsoft Dynamics 365 for Retail.

Dynamics 365 for Retail understøtter også callcentre som en slags detailkanal. I et callcenter tager arbejdere ordrer fra kunder over telefonen og opretter salgsordrer. Callcenterfunktioner omfatter funktioner, der er beregnet til at gøre det nemmere at tage telefonordre og håndtere kundeservice i hele ordreopfyldelsesprocesen. Eksempelvis kan call center-medarbejdere angive oplysninger om debitorbetalinger direkte til salgsordren og kan se en detaljeret oversigt over gebyrer og betalinger, før de kan sende ordren. Arbejdere har også mulighed for at styre prisen og få adgang til forskellige data om debitorer, produkter og priser fra siden **Salgsordre**. Desuden har callcentre har forbedret funktionalitet til sporing af debitorers historik og ordrestatus. Hvert callcenter kan have sine egne brugere, betalingsmetoder, prisgrupper, økonomiske dimensioner og leveringsmåder. Du kan konfigurere disse indstillinger, når du opretter callcenteret. Du kan også bruge siden **Callcenter** til at aktivere eller deaktivere følgende grupper af funktioner, der er unikke for callcentre:

-   **Ordrefuldførelse** – Denne gruppe omfatter funktioner, der er knyttet til betalinger og færdiggørelse på siden **Salgsordre**.
-   **Dirigeret salg** – Denne gruppe indeholder funktioner, der er relateret til kildekoder, scripts og kataloganmodninger.

Når du aktiverer disse funktioner i indstillingerne for callcenteret, er de tilgængelige på siden **Salgsordre** for brugere, der er knyttet til callcenteret. De fleste af disse funktioner kræver yderligere opsætning, før de kan bruges. Før brugere kan oprette callcenter-ordrer, skal du føje brugere til callcentret som callcenter-brugere. Dette trin aktiverer kanalspecifikke konfiguration og funktionalitet for callcenter. Her er nogle eksempler på funktioner, der bliver tilgængelige:

-   Vejledt salg indeholder konfigurationsindstillinger for telefonsalgsscripts og produktbilleder for at hjælpe og vejlede salgsassistenter, når de tager ordrer.
-   Ordrer kan ikke fuldføres, før salgsassistenten har hentet mindst én betalingsmetode.
-   Regler for mersalg og krydssalg kan konfigureres til at bede salgsassistenten om at reklamere for specifikke produkter til debitoren.
-   Salgsassistenten kan hente koden til det katalog, som en debitor bestiller fra.
-   Salgsassistenten kan føje en detailhandlers kuponer til ordren.
-   Salgsassistenten kan sælge kontinuitetsprogrammer.
-   Ordrer kan sættes på hold manuelt eller automatisk for at angive, at yderligere undersøgelse er påkrævet, før ordren kan behandles.





