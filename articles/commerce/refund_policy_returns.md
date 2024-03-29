---
title: Oprette og opdatere en politik for returneringer og refusion for en kanal
description: Denne artikel forklarer, hvordan du opretter en politik for returneringer og refusioner for en kanal.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: d01ad490301dd2f4103b8bd3f702db12b93a45a8
ms.sourcegitcommit: bd7b1ffe90b25eb4c68d6aaebd063bf33e09d9cd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2022
ms.locfileid: "9627490"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Oprette og opdatere en politik for returneringer og refusion for en kanal

[!include [banner](includes/banner.md)]

Med politikken for kanalreturnering i Dynamics 365 Commerce kan detailhandlere angive de håndhævelser, hvor betalingsmidler kan tillades, for at behandle en returvare på et POS.  

Denne artikel forklarer, hvordan du opretter en politik for returneringer og refusioner for en kanal.

Politikkens omfang er i øjeblikket begrænset til at angive de betalingsmidler, der kan tillades for en kanal. Listen "tilladt" er baseret på de betalingsmetoder, der bruges til at foretage købet. F.eks.:

- Hvis et er foretaget køb med et gavekort, er butikspolitikken kun at behandle refusioner til et nyt gavekort eller for at give butikskredit. 
- Hvis et salg foretages ved hjælp af kontanter, vil de indstillinger, der er tilladt for refusionen, være kontant, gavekort og kundekonto, men ikke kreditkort. 

## <a name="enable-return-policy"></a>Aktivere returneringspolitik

Denne funktion er som standard slået til. Du kan finde den i arbejdsområdet til **Funktionsstyring** ved at søge efter **Aktivér kanalreturneringspolitikker** på listen over funktionsnavne.


## <a name="configure-return-policy"></a>Konfigurere returneringspolitik

Udfør følgende trin for at konfigurere en returneringspolitik for en detailbutik eller en onlinedetailkanal.

1. Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Returneringer** \> **Kanalreturneringspolitik**.

1. Vælg **Ny** for at oprette en ny skabelon for returneringspolitik. Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude. I forbindelse med nye skabeloner skal du tilføje et navn og en beskrivelse, der kan hjælpe dig med at identificere politikken, når den anvendes på kanalen.

   ![Tilføje ny returneringspolitik.](media/Return-policy-page1.png)
     
   
1. Definer **Tilladte** returneringsbetalingsmidler, der er specifikke for de enkelte betalingsmåder, i sektionen **Tilladte betalingsmetoder for refundering**.
   ![Angive tilladte betalingsmetoder pr. betalingstype.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Betalingsmetoderne afledes af de betalingsmetoder, der er defineret for organisationen.
    > - Hvis du tilføjer en tilladt betalingsmiddeltype for hver angivet betalingsmåde, sikrer du, at der kan foretages returneringer til den tilladte betalingsmiddeltype for returneringer.
    
1. Knyt skabelonen for returneringspolitik til de butikker, hvor den vil blive brugt. Vælg **Tilføj** under fanen **Detailkanaler**, og tilknyt de tilgængelige kanaler. 

    - Vælg de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.
    - Der kan kun knyttes én skabelon for returneringspolitik til hver butik.
    - Brug pileknapperne til at vælge butikker, områder eller organisationer.
    - Gyldighedsdatoen for politikken er den dato, hvor politikkerne anvendes på kanalerne, og kanaljobbene køres. 

    ![Dialogboksen Vælg organisationsnoder.](media/Return-policy-page3.png)

1. På siden **Distributionsplan** skal du køre jobbet **1070** for at gøre kanalreturneringspolitikken tilgængelig for POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Se kanalreturneringspolitikken i POS

Følg trinnene i et af følgende eksempler for at få vist de tilladte betalingsmiddeltyper for returneringer i POS.

1. Log på POS som kasserer eller leder.
1. Vælg **Vis kladde** under **Skift og kasseapparat**.
1. Vælg den transaktion, der er en del af returneringen. 
1. Vælg de varer, der skal refunderes, og vælg betalingsmåden.  
    - Hvis det valgte betalingsmiddel er på den tilladte liste over betalingsmiddeltyper for returnering, kan kassereren fuldføre transaktionen.
    - Hvis det valgte betalingsmiddel ikke er tilladt, vises der en fejlmeddelelse.
    - Vælg **Skyldigt beløb** for at få vist en liste over alle tilladte betalingsmiddeltyper for returnering.

-eller-

1. Log på POS som kasserer eller leder.
1. Vælg **Returtransaktion**, og angiv kvitterings-id'et ved hjælp af en scanning af stregkode eller manuel indtastning. 
1. Vælg den transaktion, der er en del af returneringen. 
1. Vælg de varer, der skal refunderes, og vælg betalingsmåden.  
    - Hvis det valgte betalingsmiddel er på den tilladte liste over betalingsmiddeltyper for returnering, kan kassereren fuldføre transaktionen.
    - Hvis det valgte betalingsmiddel ikke er tilladt, vises der en fejlmeddelelse.
    - Vælg **Skyldigt beløb** for at få vist en liste over alle tilladte betalingsmiddeltyper for returnering.

![Refusionstype er ikke tilladt.](media/Return-policy-page6.png)



![Refusionstyper er tilladt.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
