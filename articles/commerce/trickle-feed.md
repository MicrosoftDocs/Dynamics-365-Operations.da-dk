---
title: Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik
description: I dette emne beskrives den sivende feedbaserede ordreoprettelse til butikstransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991328"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik

[!include [banner](includes/banner.md)]

I Dynamics 365 Retail version 10.0.4 og tidligere er opgørelsesbogføring en handling ved afslutningen af dagen, og alle transaktioner bogføres i bøgerne sidst på dagen. Store transaktioner skal derefter behandles i et begrænset tidsvindue, og det kan nogle gange resultere i belastning og låsning og fejl ved bogføring af opgørelse. Detailhandlere kan heller ikke genkende indtægter og betalinger i deres bøger i løbet af dagen.

Med den sivende feedbaseret ordreoprettelse der blev introduceret i Retail version 10.0.5, behandles transaktionerne i løbet af dagen, og det er kun den økonomiske afstemning af betalingsmidler og andre kassestyringstransaktioner, der behandles ved afslutningen af dagen. Denne funktion opdeler belastningen fra oprettelsen af salgsordrer, fakturaer og betalinger over hele dagen, hvilket giver en bedre formodet performance og muligheden for at genkende indtægter og betalinger i bøgerne i næsten realtid. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Sådan bruges sivende feedbaseret bogføring
  
1. Hvis du vil aktivere sivende feedbaseret bogføring af detailtransaktioner, skal du aktivere funktionen **Detailopgørelser – Sivende feed** ved hjælp af Funktionsstyring.

    > [!IMPORTANT]
    > Før du aktiverer funktionen, skal du sikre dig, at der ikke er nogen opgørelser, der venter på at blive bogført.

2. Det aktuelle opgørelsesdokument opdeles i to forskellige typer: transaktionsopgørelse og regnskabsopgørelse.

      - Transaktionsopgørelsen samler alle ikke-bogførte og validerede transaktioner og opretter salgsordrer, salgsfakturaer, betalings-og rabatkladder og indtægts-/udgiftstransaktioner med den hyppighed, der har konfigureret. Du skal konfigurere denne proces til at køre med en høj frekvens, så dokumenter oprettes, når transaktionerne overføres til Headquarters via P-jobbet. Da transaktionsopgørelsen allerede opretter salgsordrer og salgsfakturaer, er det egentlig ikke nødvendigt at konfigurere batchjobbet **Bogfør lager**. Du kan dog stadig bruge det til at imødekomme bestemte virksomhedskrav, som du måtte have.  
      
     - Regnskabet er beregnet til at blive udarbejdet ved dagens afslutning og understøtter kun afslutningsmetoden **Skift**. Denne opgørelse vil være begrænset til økonomisk afstemning og vil kun oprette kladder til differencebeløb mellem optalt beløb og posteringsbeløb for de forskellige betalingsmidler, samt kladder til andre kassestyringstransaktioner.   

3. Hvis du vil beregne transaktionsopgørelsen, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn transaktionsopgørelser i batch**. Hvis du vil bogføre transaktionsopgørelserne i batch, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør transaktionsopgørelser i batch**.

4. Hvis du vil beregne regnskabet, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn regnskaber i batch**. Hvis du vil bogføre regnskabet i batch, skal du gå til **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør regnskaber i batch**.

> [!NOTE]
> Menupunkterne **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Beregn opgørelser i batch** og **Retail og Commerce > Retail og Commerce IT > POS-bogføring > Bogfør opgørelser i batch** fjernes med den nye funktion.

Du kan også oprette forskellige typer af transaktions- og regnskabsopgørelser manuelt. Gå til **Retail og Commerce > Kanaler > Butikker**, og klik på **Opgørelser**. Klik på **Ny**, og vælg derefter den type opgørelse, du vil oprette. Felter på siden **Opgørelser** og handlinger under **Opgørelsesgruppe** på siden, viser relevante data og handlinger, der er baseret på den valgte opgørelsestype.
