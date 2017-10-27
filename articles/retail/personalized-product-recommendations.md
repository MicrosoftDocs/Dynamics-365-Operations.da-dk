---
title: Oversigt over tilpassede produktanbefalinger
description: "I Dynamics 365 for Retail kan produktanbefalinger vises på POS-enheden. Anbefalingerne er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker. For detailhandlere med store kataloger hjælper anbefalingerne kunden med opdagelse af produkter. Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg og krydssalg, og de kan forbedre fastholdelsen af kunderne. I Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a>Oversigt over tilpassede produktanbefalinger

[!include[banner](includes/banner.md)]


> [!NOTE]
> Denne funktion er i øjeblikket kun tilgængelig i topologier med sandkasse- og produktionsinstallationer (med høj tilgængelighed). 

I Dynamics 365 for Retail kan produktanbefalinger vises på POS-enheden. Anbefalingerne er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker. For detailhandlere med store kataloger hjælper anbefalingerne kunden med opdagelse af produkter. Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg og krydssalg, og de kan forbedre fastholdelsen af kunderne. I Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning.


<a name="scenarios"></a>Scenarier
---------

Produktanbefalinger er aktiveret for følgende POS-scenarier. De er tilgængelige i Cloud POS eller Modern POS (MPOS).

1.  På siden **Produktdetaljer**:

-   Hvis en butiksansat går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingsprogrammet yderligere varer, det er sandsynligt at købe sammen.
-   Hvis den butiksansatte føjer en kunde til transaktionen og derefter besøger derefter siden **Produktdetaljer**, giver anbefalingsprogrammet tilpassede anbefalinger ved hjælp af kundens transaktionshistorik.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  På siden **Transaktion**:

-   Anbefalingsprogrammet foreslår varer baseret på hele listen over varer i indkøbskurven.
-   Hvis den butiksansatte føjer en kunde til transaktionen, giver anbefalingsprogrammet personlige anbefalinger ved hjælp af kundens transaktionshistorik og listen over varer i indkøbskurven.

> [!NOTE]
> For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 for Retail. Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  På siden **Kundeoplysninger**:
    -   Anbefalingsprogrammet foreslår varer baseret på bruger-id'et og varer på kundens ønskeliste.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurer Dynamics 365 for Retail til at aktivere POS-anbefalinger
Hvis du vil konfigurere produktanbefalinger, skal du konfigurere følgende.

1.  Sørg for, at du har valgt den korrekte **juridiske enhed**.
2.  Gå til **Enhedslager**, vælg **Detailsalg**, og klik derefter på **Opdater**. Derved anvendes demodataene (eller dine data) fra driftsdatabasen og flyttes til enhedslageret.
3.  Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout**, vælge dit skærmlayout, starte **skærmlayoutdesigneren** og derefter slippe kontrolelementet med **anbefalinger**, hvor der er behov for det.
4.  Gå til **Detailparametre**, vælg **Maskinel indlæring** og vælg **Ja** under **Aktivér POS-anbefalinger**.
5.  For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**. For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.

## <a name="how-does-it-work"></a>[]()Hvordan fungerer det?
Når du opdaterer enheden **Enhedslager**, udføres følgende handlinger.

-   Dataene i det format, der kræves af Cognitive Services, udtrækkes fra driftsdatabasen i Dynamics-365 for Retail og sendes til enhedslageret.
-   Dataene bruges til at rense dataene ved hjælp af Hive-scripts som en del af ADF-aktiviteterne i Azure Data Factory (ADF). Rengjorte data gemmes i blob-lager.
-   Data fra blob-lager bruges af API'en i Cognitive Services til at træne en anbefalingsmodel.

Når du aktiverer **Aktivér anbefalinger** og kører konfigurationsjobbene, udføres følgende handlinger.

-   Legitimationsoplysninger og id for modellen hentes fra API'en og gemmes i driftsdatabasen i Dynamics-365 for Retail i web.config til AOS og også i detailserveren.
-   Legitimationsoplysninger og id for modellen er gjort tilgængelige for CRT, så kald til produktanbefalinger fra Cloud POS og MPOS i onlinetilstand kan opfyldes.


<a name="see-also"></a>Se også
--------

[Føj et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed](add-recommendations-control-pos-screen.md)



