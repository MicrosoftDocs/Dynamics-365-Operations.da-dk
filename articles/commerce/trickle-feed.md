---
title: Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik
description: I dette emne beskrives den sivende feedbaserede ordreoprettelse til butikstransaktioner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/11/2021
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964622"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 Commerce version 10.0.5 og senere anbefales det, at du skifter alle bogføringsprocesser for opgørelser til de sivende feedbaserede bogføringsprocesser for opgørelser. Der knytter sig betydelige ydeevne- og forretningsmæssige fordele ved brug af funktionaliteten til sivende feed. Salgstransaktioner behandles i løbet af dagen. Transaktioner i forbindelse med betalingsmidler og kassestyring behandles i regnskabet ved dagens afslutning. Funktioner til sivende feed giver mulighed for fortløbende behandling af salgsordrer, fakturaer og betalinger. Derfor opdateres og registreres lager, omsætning og betalinger i realtid.

## <a name="use-trickle-feed-based-posting"></a>Sådan bruges sivende feedbaseret bogføring

> [!IMPORTANT]
> Før du aktiverer sivende feedbaseret bogføring, skal du sikre dig, at der ikke er nogen beregnede og ikke-bogførte opgørelser. Bogfør alle opgørelser, før du aktiverer funktionen. Du kan kontrollere, om der er åbne opgørelser, i arbejdsområdet **Butiksregnskab**.

Hvis du vil aktivere sivende feedbaseret bogføring af detailtransaktioner, skal du aktivere funktionen **Detailopgørelser – Sivende feed** i arbejdsområdet **Funktionsstyring**. Opgørelser opdeles i to forskellige typer: transaktionsopgørelser og regnskabsopgørelser.

### <a name="transactional-statements"></a>Transaktionsopgørelser

Behandling af transaktionsopgørelser er beregnet til at blive kørt med en høj frekvens hele dagen, så dokumenter oprettes, når transaktionerne overføres til Commerce-hovedkontoret. Transaktioner indlæses fra butikkerne til Commerce-hovedkontoret, når du kører **P-job**. Du skal også køre jobbet **Valider butiksposteringer** for at validere transaktioner, så transaktionsopgørelsen henter dem.

Planlæg, at følgende job skal køres med høj frekvens:

- Hvis du vil beregne en transaktionsopgørelse, skal du køre jobbet **Beregn transaktionsopgørelser i batch** (**Retail og Commerce \> Retail og Commerce IT \> POS-bogføring \> Beregn transaktionsopgørelser i batch**). Dette job vil hente alle ikke-bogførte og validerede transaktioner og føje dem til en ny transaktionsopgørelse.
- Hvis du vil bogføre transaktionsopgørelser i en batch, skal du køre jobbet **Bogfør transaktionsopgørelser i batch** (**Retail og Commerce \> Retail og Commerce IT \> POS-bogføring \> Bogfør transaktionsopgørelser i batch**). Dette job kører bogføringsprocessen og opretter salgsordrer, salgsfakturaer, betalingskladder, rabatkladder og indtægts-/udgiftstransaktioner for ikke-bogførte opgørelser, der ikke indeholder fejl. 

### <a name="financial-statements"></a>Regnskaber

Regnskabsbehandlingen er beregnet til at være en proces, der køres ved dagens afslutning. Denne type behandling af opgørelser understøtter kun lukkemetoden **Skift** og henter kun lukkede skift. Opgørelser er begrænset til økonomisk afstemning. De opretter kun kladderne til differencebeløb mellem det optalte beløb og transaktionsbeløbet for betalingsmidler og kladder til andre kassestyringstransaktioner.

Regnskaber aktiverer også gennemgangen af følgende transaktioner: betalingsmiddeltransaktioner med kasseoptælling, betalingstransaktioner, betalingsmiddeltransaktioner i banken og betalingsmiddeltransaktioner lagt i pengeskab. Siden med betalingsmiddeldetaljer er kun synlig, når et regnskab er valgt.

![Et billede, der viser afsnittet med betalingsmiddeldetaljer af den bogførte opgørelsesformular, som kun er synlig, når et regnskab er valgt.](./media/Trickle-feed-posted-statements-transaction-view.png)

Planlæg start- og sluttider for følgende regnskabsjob baseret på den forventede afslutning af dagen:

- Hvis du vil beregne en regnskabsopgørelse, skal du køre jobbet **Beregn regnskaber i batch** (**Retail og Commerce \> Retail og Commerce IT \> POS-bogføring \> Beregn regnskaber i batch**). Jobbet indsamler alle ikke-bogførte økonomiske transaktioner og føjer dem til et nyt regnskab.
- Hvis du vil bogføre regnskaber i en batch, skal du køre jobbet **Bogfør regnskaber i batch** (**Retail og Commerce \> Retail og Commerce IT \> POS-bogføring \> Bogfør regnskaber i batch**).

### <a name="manually-create-statements"></a>Opret opgørelser manuelt

Transaktions- og regnskabstyper kan også oprettes manuelt. 

1. Gå til **Retail og Commerce \> Kanaler \> Butikker**, og vælg **Opgørelser**. 
2. Vælg **Ny**, og vælg derefter den type opgørelse, du vil oprette. Felter på siden **Opgørelser** viser data, der er relevante for den valgte opgørelsestype, og handlinger under **Opgørelsesgruppe** viser relevante handlinger.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
