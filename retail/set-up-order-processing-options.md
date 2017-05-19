---
title: Konfigurer indstillinger for ordrebehandling
description: Dette emne indeholder oplysninger om, hvordan du behandler ordrer for callcentre ved brug af Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 12da2010c48f1563883f506399d2b7aab36baead
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-order-processing-options"></a>Konfigurer indstillinger for ordrebehandling

[!include[banner](includes/banner.md)]


Dette emne indeholder oplysninger om, hvordan du behandler ordrer for callcentre ved brug af Microsoft Dynamics 365 for Operations - Retail. 

Detail og handel i Dynamics 365 for Operations understøtter flere detailkanaler, f.eks. onlinebutikker, fysiske butikker og callcentre. I et callcenter tager arbejdere ordrer fra kunder over telefonen og opretter salgsordrer. Dette emne beskriver, hvordan du opretter et callcenter og konfigurerer indstillingerne for callcenteret. Hvert callcenter kan have sine egne brugere, betalingsmetoder, prisgrupper, økonomiske dimensioner og leveringsmåder. Du kan konfigurere disse indstillinger, når du opretter callcenteret. **Vigtigt:** Når den aktuelle Dynamics AX-bruger opretter salgsordrer, skal brugeren tildeles til callcentret som callcenterbruger, før callcenterarbejdsgangen kan bruges. Du kan bruge siden **Callcenter** til at aktivere eller deaktivere grupper af funktioner, der er unikke for callcentre. Følgende grupper af funktioner kan aktiveres:

-   **Ordrefuldførelse** – Denne gruppe omfatter funktioner, der er knyttet til betalinger og færdiggørelse på siden **Salgsordre**.
-   **Dirigeret salg** – Denne gruppe indeholder funktioner, der er relateret til kildekoder, scripts og kataloganmodninger.

Når du aktiverer disse funktioner i indstillingerne for callcenteret, er de tilgængelige på siden **Salgsordre** for brugere, der er knyttet til callcenteret. De fleste af disse funktioner kræver yderligere opsætning, før de kan bruges. Billeder og scripts er aktiveret som en del af indstillingen for dirigeret salg for det specifikke callcenter. Hvis disse funktioner er aktiveret, vises scripts og produktbilleder i faktaboksruden på siden **Salgsordre**. Standardbilledet, der er angivet for et produkt, vises. Scripts kan konfigureres for en vare, katalog, debitor eller vare i forbindelse med et katalog. Callcenterordrer kan vise flere oplysninger om, hvordan prisen for en bestemt ordrelinje blev afledt. Ordrerne viser f.eks., hvilke rabatter der blev anvendt. Du kan aktivere funktionen under **Debitor** &gt; **Opsætning** &gt; **Debitorparametre** &gt; **Priser** &gt; **Prisdetaljer**. Du kan få adgang til siden **Prisdetaljer** på rullelisten **Salgsordrelinje**. Du kan bruge ordrehændelsessporing til overvågningsformål, til at gennemse de handlinger, der er udført for en ordre i ordrens livscyklus, eller til at spore handlinger for en bestemt bruger. Du kan for eksempel optage handlingen, hver gang en bruger opretter en salgsordre, sætter en ordre på hold, tilsidesætter et gebyr eller opdaterer en ordrelinje. Du kan konfigurere ordrehændelser til at spore handlinger for bestemte brugere, grupper af brugere eller alle brugere i en bestemt periode. Du kan få vist de handlinger, der er udført på et dokument, ved at åbne siden **Ordrehændelser** fra handlingsruden på siden for det pågældende dokument. Du kan konfigurere ordrehændelser på **Salgs og marketing** &gt; **Opsætning** &gt; **Hændelser** &gt; **Ordrehændelser**. Når en debitors ordre ikke kan leveres til tiden, kan en virksomhed automatisk sende mailbeskeder til debitoren for at forklare ordrestatussen og giver debitoren en mulighed for at annullere ordren. Hvis forsinkelsen rækker ud over en bestemt tærskel, kan ordren annulleres automatisk. Der kan sendes op til tre mailbeskeder med bestemte intervaller:

1.  **Første varsel om automatisk annullering** – Debitoren kan vælge at annullere ordren.
2.  **Andet varsel om automatisk annullering** – Debitoren kan vælge at annullere ordren.
3.  **Endeligt varsel om automatisk annullering** – Systemet annullerer ordren, og debitoren får besked om annulleringen.

Du kan undtage individuelle debitorer og produkter fra den automatiske proces til beskeder og annullering. Der udløses en vigtig besked om avance, når du føjer en vare til en ordre. Beskeden indeholder vigtige oplysninger om varen, f.eks. DB for pris og varerentabilitet. Du kan bruge disse oplysninger til at afgøre, om en prisændring er passende, når du tilføjer en vare til salgsordren. Du kan for eksempel konfigurere grænseværdier for handelsavancer for at angive, at en grænseværdi på 40 % eller mere over omkostninger er acceptabelt for en vare, men en grænse på 20 til 39 % over omkostninger er diskutabelt. I dette tilfælde udløser en vare med en grænse mellem 20 og 39 % en advarsel. Alle varer, der har en grænse på mindre end 20 % over omkostninger kan ikke sælges, og vareprisen kan ikke justeres. Du kan konfigurere vigtige beskeder om avance på **Debitor** &gt; **Opsætning** &gt; **Debitorparametre** &gt; **Vigtige beskeder om avance**. Når du konfigurerer momstildelingen, der er baseret på standardregler, kan du bestemme en tilsvarende prioritet for adresseelementer. Du kan f.eks. angive, at det har højere prioritet at sammenholde en momsgruppe efter postnummer end stat. Når du indtaster nye kundeadresseposter, tildeles momsgruppen automatisk baseret på, hvordan kundens adresse stemmer overens med standardreglerne og prioriteten, der svarer til det, du definerede. Du kan konfigurere denne funktion på siden **Finansparametre**.




