---
title: Callcenter-funktionalitet
description: Denne artikel indeholder en oversigt over de call center salgsfunktioner i Microsoft Dynamics 365 for operationer.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf93b1f91679cdb520ead2a12a5e52108a83fbb2
ms.lasthandoff: 03/31/2017


---

# <a name="call-center-functionality"></a>Callcenter-funktionalitet

Denne artikel indeholder en oversigt over de call center salgsfunktioner i Microsoft Dynamics 365 for operationer.

Detail og handel i Microsoft Dynamics AX understøtter callcentre som en slags detailkanal. I et callcenter tager arbejdere ordrer fra kunder over telefonen og opretter salgsordrer. Callcenterfunktioner omfatter funktioner, der er beregnet til at gøre det nemmere at tage telefonordre og håndtere kundeservice i hele ordreopfyldelsesprocesen. Eksempelvis call center arbejdere kan angive oplysninger om debitorbetalinger direkte til salgsordren, og kan se en detaljeret oversigt over gebyrer og betalinger, før de kan sende ordren. Arbejdere har også mulighed for at styre prisen og få adgang til forskellige data om debitorer, produkter og priser fra siden **Salgsordre**. Desuden har callcentre har forbedret funktionalitet til sporing af debitorers historik og ordrestatus. Hvert callcenter kan have sine egne brugere, betalingsmetoder, prisgrupper, økonomiske dimensioner og leveringsmåder. Du kan konfigurere disse indstillinger, når du opretter callcenteret. Du kan også bruge siden **Callcenter** til at aktivere eller deaktivere følgende grupper af funktioner, der er unikke for callcentre:

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



