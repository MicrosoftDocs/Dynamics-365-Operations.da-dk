---
title: Personlige anbefalinger produktoversigt
description: "Dynamics 365 for operationer, kan produkt anbefalinger vises på salg (POS) enhed. Anbefalingerne er varer, som kunden er interesseret i at baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i mursten og mørtel butikker. Anbefalinger hjælpe kunden med registrering af produktet, for detailhandlere med store kataloger. Ved fremvisning af produkter, der er rettet mod en kundes interesser og køber vaner produktanbefalingerne detailhandlere kan hjælpe med at sælge og krydssælge og kan forbedre tilbageholdelse af debitorbetaling. I Dynamics 365 for operationer, er produkt anbefalinger udstyret med kognitive services og Microsoft Azure machine learning."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Personlige anbefalinger produktoversigt

Dynamics 365 for operationer, kan produkt anbefalinger vises på salg (POS) enhed. Anbefalingerne er varer, som kunden er interesseret i at baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i mursten og mørtel butikker. Anbefalinger hjælpe kunden med registrering af produktet, for detailhandlere med store kataloger. Ved fremvisning af produkter, der er rettet mod en kundes interesser og køber vaner produktanbefalingerne detailhandlere kan hjælpe med at sælge og krydssælge og kan forbedre tilbageholdelse af debitorbetaling. I Dynamics 365 for operationer, er produkt anbefalinger udstyret med kognitive services og Microsoft Azure machine learning.

<a name="scenarios"></a>Scenarier
---------

Produkt anbefalinger er aktiveret for følgende scenarier i POS. De er tilgængelige i skyen POS eller moderne POS (MPOS).

1.  På den **oplysninger om** side:

-   Hvis en butik knytte Besøg en **oplysninger om** side, når du kigger på tidligere posteringer på tværs af forskellige kanaler henstilling motoren foreslår yderligere elementer, der kan købes sammen.
-   Hvis butikken knytte føjer en kunde til transaktionen, og besøg derefter en **oplysninger om** side, motoren henstilling indeholder personlige anbefalinger ved hjælp af kundens transaktionsoversigt.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  På den **transaktion** side:

-   Motoren henstilling foreslår elementer baseret på hele listen over varer i din kurv.
-   Hvis butikken knytte føjer en kunde til transaktionen, motoren henstilling indeholder personlige anbefalinger ved hjælp af kundens transaktionsoversigt og listen over varer i din kurv.

**Note** til at vise anbefalinger på den **transaktion** side, formidleren skal opdatere skærmlayoutet i Dynamics 365 for operationer. Den **anbefalinger** kontrol skal slippes på den **transaktion** side. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  På den **kundeoplysninger** side:
    -   Motoren henstilling foreslår elementer baseret på bruger-ID og elementer på kundens ønske liste.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 for handlinger til at aktivere POS anbefalinger
Hvis du vil konfigurere produktanbefalingerne, skal du gøre følgende.

1.  Sørg for, at du har valgt den korrekte **juridiske enhed**.
2.  Gå til **enhed butik**, skal du vælge **Retail sales**, og klik derefter på **Opdater**. ** ** Derved bruge demo-data (eller data) fra databasen operationelle og flytte det til den store enhed.
3.  Valgfrit: For at få vist anbefalinger på skærmbilledet transaktion, gå til ** skærmlayout, **vælge din skærmlayout, Start den **skærmen layoutdesigneren**,** ** og derefter slippe den ** anbefalinger kontrol ** om nødvendigt.
4.  Gå til **Retail parametre**, skal du vælge **Machine learning**, skal du vælge ** Ja ** under **aktivere POS anbefalinger**.
5.  For at se anbefalinger på POS, i den globale konfiguration kørslen **1110**. For at afspejle ændringer i POS-skærmen layoutdesigneren, kørslen kanal konfiguration **1070**.

## <a name="how-does-it-work"></a>[]()Hvordan fungerer det?
Når du opdaterer de **store enhed** objektet følgende handlinger finder sted.

-   Dataene i det format, der kræves af de kognitive tjenester er udtrukket fra Dynamics-365 for operationer operationel database og sendes til butikken enhed.
-   Dataene bruges til at rense dataene ved hjælp af scripts til hive-filen som en del af ADF aktiviteter af Azure Data Factory (ADF). Rengøres data er gemt i blob storage.
-   Data fra blob storage bruges af kognitive services API til at uddanne en henstilling-model.

Når du slår **aktivere anbefalinger** og konfiguration af job køres, udføres følgende handlinger.

-   Modellen legitimationsoplysninger og ID er afhentet fra API og gemt i Dynamics-365 for operationer operationel database, i web.config til AOS og også i retail-server.
-   Modellen legitimationsoplysninger og ID er gjort tilgængelige for CRT, så kald til produkt anbefalinger fra sky POS og MPOS i online-tilstand kan blive respekteret.


<a name="see-also"></a>Se også
--------

[Tilføje et kontrolelement med anbefalinger til siden transaktion på POS-enhed](add-recommendations-control-pos-screen.md)


