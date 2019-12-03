---
title: Foretag sivende feedbaseret ordreoprettelse til transaktioner i detailbutik
description: I dette emne beskrives den sivende feedbaserede ordreoprettelse til transaktioner i detailbutik i Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693083"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Foretag sivende feedbaseret ordreoprettelse til transaktioner i detailbutik (offentlig prøveversion)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

I Dynamics 365 Retail-versionerne 10.0.4 og tidligere er bogføring af detailopgørelse en handling ved afslutningen af dagen, og alle transaktioner bogføres i bøgerne sidst på dagen. Store transaktioner skal derefter behandles i et begrænset tidsvindue, og det kan nogle gange resultere i belastning og låsning og fejl ved bogføring af opgørelse. Detailhandlere kan heller ikke genkende indtægter og betalinger i deres bøger i løbet af dagen.

Med den offentlige prøveversion af sivende feedbaseret ordreoprettelse der blev introduceret i Retail version 10.0.5, behandles transaktionerne i løbet af dagen, og det er kun den økonomiske afstemning af betalingsmidler og andre kassestyringstransaktioner, der behandles ved afslutningen af dagen. Denne funktion opdeler belastningen fra oprettelsen af salgsordrer, fakturaer og betalinger over hele dagen, hvilket giver en bedre formodet performance og muligheden for at genkende indtægter og betalinger i bøgerne i næsten realtid. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Sådan bruges sivende feedbaseret bogføring
  
1. Hvis du vil aktivere sivende feedbaseret bogføring af detailtransaktioner, skal du gå til **System administration > Konfiguration > Licenskonfiguration** og deaktivere nøglen **Detailopgørelser**.

2. På samme side skal du aktivere licensnøglen **Detailopgørelser (sivende feed) – prøveversion**. Når du aktiverer denne nøgle, skal du sikre dig, at der ikke er nogen opgørelser, der venter på at blive bogført. 

> [!Important]
> Før du aktiverer licensnøglen **Detailopgørelser (sivende feed) – prøveversion**, skal du sørge for, at der ikke er opgørelser, der venter på at blive bogført.

3. Det aktuelle opgørelsesdokument opdeles i to forskellige typer. Transaktionsopgørelse og regnskabsopgørelse.

      - Transaktionsopgørelsen samler alle ikke-bogførte og validerede detailtransaktioner og opretter salgsordrer, salgsfakturaer, betalings-og rabatkladder og indtægts-/udgiftstransaktioner med den hyppighed, der har konfigureret. Du skal konfigurere denne proces til at køre med en høj frekvens, så dokumenter oprettes, når detailtransaktionerne overføres til Retail Headquarters via P-jobbet. Da transaktionsopgørelsen allerede opretter salgsordrer og salgsfakturaer, er det egentlig ikke nødvendigt at konfigurere batchjobbet **Bogfør lager**. Du kan dog stadig bruge det til at imødekomme bestemte virksomhedskrav, som du måtte have.  
      
     - Regnskabet er beregnet til at blive udarbejdet ved dagens afslutning og understøtter kun afslutningsmetoden **Skift**. Denne opgørelse vil være begrænset til økonomisk afstemning og vil kun oprette kladder til differencebeløb mellem optalt beløb og posteringsbeløb for de forskellige betalingsmidler, samt kladder til andre kassestyringstransaktioner.   

4. Hvis du vil beregne transaktionsopgørelsen, skal du klikke på **Retail > Retail IT > POS-bogføring > Beregn transaktionsopgørelser i batch**. Hvis du vil bogføre transaktionsopgørelserne i batch, skal du klikke på **Retail > Retail IT > POS-bogføring > Bogfør transaktionsopgørelser i batch**.

5. Hvis du vil beregne regnskabet, skal du klikke på **Retail > Retail IT > POS-bogføring > Beregn regnskaber i batch**. Hvis du vil bogføre regnskabet, skal du klikke på **Retail > Retail IT > POS-bogføring > Bogfør regnskaber i batch**.

> [!NOTE]
> Menupunkterne **Retail > Retail IT > POS-bogføring > Beregn opgørelser i batch** og **Retail > Retail IT > POS-bogføring > Bogfør opgørelser i batch** fjernes med den nye funktion.

Du kan også oprette forskellige typer af transaktions- og regnskabsopgørelser manuelt. Gå til **Retail > Kanaler > Detailbutikker**, og klik på **Detailopgørelser**. Klik på **Ny**, og vælg derefter den type opgørelse, du vil oprette. Felter på siden **Detailopgørelser** og handlinger under **Opgørelsesgruppe** på siden, viser relevante data og handlinger, der er baseret på den valgte opgørelsestype.
