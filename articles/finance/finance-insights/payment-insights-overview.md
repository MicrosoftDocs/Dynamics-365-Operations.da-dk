---
title: Forudsigelser for debitorbetaling (prøveversion)
description: I dette emne beskrives muligheden for forudsigelse af betalinger, der hjælper med at forbedre forståelsen af kunders typiske betalingsmetoder. Denne funktion kan også hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end normalt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f306f9437b78005d8b8aa11f0b6f210ebdd4fd2a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995059"
---
# <a name="customer-payment-predictions-preview"></a>Forudsigelser for debitorbetaling (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne beskrives muligheden for forudsigelse af betalinger, der hjælper med at forbedre forståelsen af kunders typiske betalingsmetoder. Denne funktion kan også hjælpe dig med at identificere de omstændigheder, der berettiger start af indsamlingsprocesser tidligere end normalt.

## <a name="overview"></a>Overblik

Organisationer finde ofte svært for at forudsige, hvornår kunder betaler fakturaerne. Denne manglende indsigt kan forårsage følgende problemer:

- Mindre præcise likviditetsbudgetter
- Rykkerprocesser, der starter for sent
- Ordrer, der er frigivet til kunder, som kan have standard på deres betaling

Customer payment predictions (prøveversion) hjælper organisationer med at forudsige, hvornår en kundefaktura betales. De kan derfor oprette inkassostrategier, der medvirker til at øge sandsynligheden for, at de vil blive betalt til tiden.

## <a name="predictions"></a>Forudsigelser

Med kontant forudsigelser kan organisationer forbedre deres forretningsprocesser ved at hjælpe dem med at identificere de fakturaer, der forventes betalt for sent. Organisationen kan bruge disse oplysninger til at udføre handlinger, der forbedrer risikoen for, at de vil blive betalt til tiden.

Med Customer payment predictions-funktionen bruges en maskinel indlæringsmodel til at forudsige mere præcist, hvornår en kunde vil betale en udestående faktura. Denne maskinelle indlæringsmodel omfatter historiske fakturaer, betalinger og debitordata.

For hver åben faktura tildeler funktionen tre betalingssandsynligheder:

- Sandsynligheden for, at betalingen vil blive betalt til tiden
- Sandsynligheden for, at betalingen vil blive betalt senere
- Sandsynligheden for, at betalingen vil blive betalt meget senere

Funktionen indeholder også en samlet visning af forventede betalinger.

[![Samlet visning af betalings forudsigelser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hver faktura tildeles en sandsynlighed for, at der sker betaling til tiden. Fakturaer med en sandsynlighed for betaling til tiden er mindre end 50 %, markeres med en rød cirkel for at angive, at disse fakturaer muligvis kræver opmærksomhed i relation til opkrævning.

[![Liste over sandsynlighed for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Customer payment predictions-funktionen indeholder også kontekstafhængige oplysninger, der forklarer forudsigelse. Disse oplysninger omfatter de bedste faktorer, der har påvirket prognosen, den aktuelle forretningstilstand for kunden og detaljer om kundens historiske betalingsmåde.

I mange virksomheder er rykkerprocessen blevet en reaktiv aktivitet. Med andre ord starter rykkerprocessen først, når fakturaerne er forfaldne. Med Customer payment predictions kan organisationer være mere proaktiv i forbindelse med opkrævninger. De behøver ikke længere at vente på, at transaktionerne forfalder, før de indleder opkrævningsprocessen. De kan i stedet bruge funktionen betalingsforudsigelse til at bestemme, om proaktive opkrævninger vil forbedre sandsynligheden for at, der bliver betalt til tiden.

## <a name="methodology"></a>Metode

Tidligere har det ofte været vanskeligt at udvikle og installere en kunstig intelligens (AI)-løsning. Processen har krævet et team, der omfatter dataforskere, eksperter på området (SME'er) og ingeniører, der arbejder i længere tid på at formulere, udvikle, implementere og vedligeholde en brugbar AI-løsning. Med kundens betalingsforudsigelser er det nemt at implementere og bruge en AI-løsning i Microsoft Dynamics 365 Finance. Microsoft pakker AI-løsninger på forhånd, der er bygget oven på Microsoft AI Builder. Brugerne kan derfor anvende AI-løsningen med et enkelt klik med musen for at udnytte fordelene ved intelligent forudsigelser. Hvis du ikke er tilfreds med nøjagtigheden af forudsigelserne, kan en superbruger (igen med blot et enkelt klik) angive erfaringen med udvidelsen AI Builder og derefter vælge eller fravælge de felter, der bruges til at oprette forudsigelser. Når du er færdig, kan du "træne" modellen og udgive ændringerne. Den nyoplærte model vil automatisk blive valgt til at generere forudsigelser i Dynamics 365 Finance.

## <a name="release-details"></a>Frigiv detaljer

Financial Insights, offentlig prøveversion er tilgængelig for prøveimplementeringer i USA, Europa og Storbritannien. Microsoft tilføjer trinvist understøttelse af yderligere områder.

De offentlige prøveversionsfunktioner kan og bør kun aktiveres i sandkassemiljøer i niveau 2. Opsætnings- og AI-modeller, der er oprettet i et sandkassemiljø, kan ikke overføres til et produktionsmiljø. Yderligere oplysninger finder du under [Supplerende vilkår for anvendelse af Microsoft Dynamics 365 Prøveversioner](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]