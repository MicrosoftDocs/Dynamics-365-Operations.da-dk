---
title: Omkostningsanalyse for produktionsordre
description: "Denne artikel indeholder oplysninger om den omkostningsanalyse, du kan udføre for afsluttede og aktuelle produktionsordrer. Du kan analysere de forkalkulerede omkostninger og faktiske omkostninger ved hjælp af siden Prisberegning og efterkalkulationsrapporten. Du kan se oplysninger om de forventede og faktiske omkostninger (og antal) for de enkelte indgående varer, ruteoperationer og indirekte omkostninger."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 40ac5108216fd6d9eb5cd6e76fefd66828a7da84
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="production-order-cost-analysis"></a>Omkostningsanalyse for produktionsordre

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om den omkostningsanalyse, du kan udføre for afsluttede og aktuelle produktionsordrer. Du kan analysere de forkalkulerede omkostninger og faktiske omkostninger ved hjælp af siden Prisberegning og efterkalkulationsrapporten. Du kan se oplysninger om de forventede og faktiske omkostninger (og antal) for de enkelte indgående varer, ruteoperationer og indirekte omkostninger.

De faktiske omkostninger for en produktionsordre er baseret på det rapporterede forbrug af materiale og ruteoperationer. Du kan få adgang til detaljerede transaktioner om det rapporterede forbrug af materiale, ruteoperationer og indirekte omkostninger for en produktionsordre på siden **Produktionsbogføring**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Afvigelsesanalyse for en afsluttet produktionsordre
Afvigelserne afspejler en sammenligning af de rapporterede produktionsaktiviteter og beregningen af standardomkosterne på produktionsvaren. Afvigelserne kan ikke sammenlignes med produktionsordrens forventede kostpris. De rapporterede produktionsaktiviteter omfatter forbrug af materiale og ruteoperationer samt tilknyttede indirekte omkostninger og det færdigmeldte antal. Følgende fire typer afvigelser beregnes:

-   Afvigelse i lotstørrelse
-   Afvigelse i produktionsantal
-   Afvigelse i produktionspris
-   Afvigelse i produktionserstatning

I følgende diagram viser de fire afvigelser, der forklarer forskellen mellem de faktiske omkostninger i en produktionsordre og de beregnede omkostninger i varens kostprispost, når produktionsordren er afsluttet. 

![Afvigelser, der tager højde for forskelle i en afsluttet produktionsordre](./media/control.jpg) 

Du kan analysere produktionsafvigelser ved hjælp af siden **Afvigelse** eller rapporten **Afvigelse i produktion**. Brug visningsindstillinger til at få vist detaljerede afvigelser efter vare og operationsressource eller efter kostgruppe. Reglen for kostprisopdeling i lagerparametrene bestemmer, om afvigelserne skal spores efter kostprisgruppe. Du kan også bruge visningsindstillingerne **enkelt**, **flere** og **samlet** til at få vist opsummerede afvigelser. Oplysninger om detaljerede afvigelser kan hjælpe dig med at forstå kilden til hver afvigelse. Hvis du vil foregribe afvigelser, før en produktionsordre afsluttes, skal du analysere de detaljerede oplysninger, der findes i rapporten **For- og efterkalkulationer**.

## <a name="cost-analysis-for-current-production-orders"></a>Omkostningsanalyse for aktuelle produktionsordrer
Særskilte rapporter indeholder oplysninger om de enkelte typer af posteringer. Brug disse rapporter til at analysere omkostninger for rapporterede produktionsaktiviteter. Der vises kun oplysninger for aktuelle produktionsordrer, der har status **Igangsat** eller **Færdigmeldt**.

-   **Materialer i proces**− Denne rapport vises de pluklistetransaktioner, der er færdigmeldt i forhold til de aktuelle produktionsordrer pr. en bestemt posteringsdato. Rapporten angiver det komponentantal, der afgår og kostbeløbet for hver enkelt transaktion. Brug udvælgelseskriterierne for en enkelt komponentvare. Du kan f.eks. udskrive oplysninger om det afgåede antal til komponenten i forhold til de gældende produktionsordrer. Det antal, der afgik, opdateres ikke af det færdigmeldte antal, der er færdigmeldt for den overordnede vare. Derfor kan det faktiske antal råvarer i arbejde måske være angivet for højt.
-   **Igangværende forarbejdning**− Denne rapport vises de ruteposteringer (eller jobposteringer), der er færdigmeldt i forhold til de aktuelle produktionsordrer pr. en bestemt posteringsdato. Rapporten angiver de timer og antal (både antal gode og antal fejl), der er rapporteret for hver postering. Den indeholder også oplysninger som operationsnummer, handlings-id og operationsressource. Desuden viser denne rapport den samlede tid og det samlede beløb for alle transaktioner i forhold til produktionsordren og det antal, der er færdigmeldt.
-   **Indirekte omkostninger under afvikling**− Denne rapport viser de påløbne indirekte omkostninger for produktionsordrer. Disse data er baseret på det rapporterede forbrug af ruteoperationer og komponenter pr. en nærmere angivet posteringsdato. Rapporten angiver indirekte omkostningstype (tillæg eller sats), koden til kostprisarket til de indirekte omkostninger og kostbeløbet for hver enkelt transaktion. Denne rapport indeholder ikke oplysninger om den rutekort- eller pluklistetransaktion, der genererede de indirekte omkostninger.
-   **Efterkalkulation for igangværende produktion**− Denne rapport viser det samlede forbrug af materiale, ruteoperationer og indirekte omkostninger i forhold til produktionsordrerne pr. en bestemt posteringsdato.
-   **Færdigvarer i arbejde**− Denne rapport vises de aktuelle produktionsordrer og de færdigmeldte transaktioner pr. en bestemt posteringsdato.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Almindelige kilder til produktionsafvigelser](common-sources-of-production-variances.md)




