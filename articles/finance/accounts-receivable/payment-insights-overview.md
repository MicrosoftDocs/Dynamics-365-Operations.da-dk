---
title: Indsigt i debitorbetaling (prøveversion)
description: I dette emne beskrives muligheden for indsigt i betalinger, der hjælper med at forbedre forståelsen af individuelle kunders typiske betalingsmetoder. Funktionen kan hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end det, du måtte have udført.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 82b301b4b8ba61375a53a8fe6220628500f6cf3d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359311"
---
# <a name="customer-payment-insights-preview"></a>Indsigt i debitorbetaling (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne beskrives muligheden for indsigt i betalinger, der hjælper med at forbedre forståelsen af individuelle kunders typiske betalingsmetoder. Funktionen kan hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end det, du måtte have udført. 

## <a name="overview"></a>Overblik

Det kan være svært at forudsige, hvornår kunder betaler fakturaerne. Denne manglende indsigt fører til mindre præcise likviditetsbudgetter, opkrævningsprocesser, der indledes for sent, og ordrer, der er frigivet til kunder, som kan være bagud med deres betaling. Indsigt i kundebetaling (prøveversion) hjælper organisationer med at forudsige, hvornår en kundefaktura betales. Disse oplysninger kan hjælpe organisationer med at oprette inkassostrategier, der forbedrer sandsynligheden for at de bliver betalt til tiden. 

## <a name="predictions"></a>Forudsigelser

Betalingsprognoser giver organisationer mulighed for at forbedre deres forretningsprocesser ved at hjælpe dem med nemt at identificere de fakturaer, der sandsynligvis bliver betalt for sent, og med at træffe passende foranstaltninger, der kan forbedre sandsynligheden for at få betalt til tiden.

Ved hjælp af en model til maskinlæring, som udnytter historiske data for fakturaer, betalinger og kundedata, giver indsigt i debitorbetalinger (Forhåndsvisning) en mere præcis forudsigelse for, hvornår en kunde betaler en udestående faktura.

For hver åben faktura forudsiger Customer payment insights (prøveversion) tre betalingssandsynligheder:

-   Sandsynlighed for, at betaling sker til tiden 
-   Sandsynlighed for, at der sker sen betaling
-   Sandsynlighed for, at der sker stor forsinkelse med betalingen

Customer payment insights (prøveversion) giver desuden en samlet visning over forventede betalingsbeløb, der kan hjælpe organisationer med at forstå det samlede betalingsbeløb , der kan forventes fra en kunde i en af følgende tre grupper, Til tiden, Sent og Meget sent.

[![Samlet visning af betalingsforudsigelser.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hver faktura tildeles desuden en sandsynlighed for, at der sker betaling til tiden. Hvis sandsynligheden for betaling til tiden er mindre end 50 %, markeres fakturaerne med en rød cirkel for at angive, at disse fakturaer muligvis kræver opmærksomhed i relation til opkrævning. 

[![Liste over sandsynlighed for betaling.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Indsigt i debitorbetaling (Forhåndsvisning) indeholder også kontekstafhængige oplysninger, der forklarer forudsigelsen, f.eks. de primære faktorer, der har påvirket forudsigelserne, den aktuelle tilstand for erhvervsinteraktioner med kunden, og oplysninger om tidligere debitorbetalinger. I mange virksomheder er opkrævningsprocessen blevet en reaktivt aktivitet; opkrævningsprocessen starter ikke, før fakturaerne forfalder. 

Med indsigt i debitorbetalinger (Forhåndsvisning) kan organisationer være mere proaktiv i forbindelse med opkrævninger. De behøver ikke længere at vente på, at transaktionerne forfalder, før de indleder opkrævningsprocessen. De kan i stedet bruge funktionen betalingsforudsigelse til at bestemme, om proaktive opkrævninger vil forbedre sandsynligheden for at, der bliver betalt til tiden. Betalingsforudsigelse giver også virksomhederne de oplysninger, der er nødvendige for, at opkrævningsprocessen kan påbegyndes tidligt.

## <a name="methodology"></a>Metode

Det er svært at udvikle og installere en AI-løsning. Det kræver et team af dataforskere, eksperter på området og ingeniører, som arbejder i længere tid på at formulere, udvikle, implementere og vedligeholde en brugbar AI-løsning. Vi gør det nemt at implementere og bruge AI-løsninger i Finance. Vi pakker AI-løsninger på forhånd i Finance, der er bygget oven på Microsoft AI Builder. En slutbruger kan med et enkelt klik på knappen implementere AI-løsningen og begynde at udnytte fordelene ved intelligent forudsigelser. Hvis en organisation ikke er tilfreds med nøjagtigheden af forudsigelserne, kan en superbruger, igen med blot et enkelt klik, angive erfaringen med udvidelsen AI Builder og derefter vælge eller fravælge de felter, der bruges til at oprette forudsigelser. Når de er færdige, kan de øve sig i og udgive ændringerne, og den nyligt oplærte model vil automatisk blive hentet til brug for forudsigelser i Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Sådan får du indsigt i debitorbetaling (Forhåndsvisning)

Send email til [Customer payment insights (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at prøve Customer payment insights (prøveversion).

## <a name="privacy-notice"></a>Privatlivserklæring

Forhåndsvisning (1) kan eksempler (1) anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]