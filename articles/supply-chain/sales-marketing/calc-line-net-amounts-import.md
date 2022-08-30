---
title: Genberegne nettobeløb for linjer ved import af salgsordrer, tilbud og returneringer
description: I denne artikel beskrives det, om og hvordan systemet genberegner nettobeløb for linjen, når salgsordrer, tilbud og returneringer importeres. Det forklarer også, hvordan du kan styre funktionsmåden i forskellige versioner af Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 08b30044a93e46c9c83848b60d69c595bc774570
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335549"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-quotations-and-returns"></a>Genberegne nettobeløb for linjer ved import af salgsordrer, tilbud og returneringer

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, om og hvordan systemet genberegner nettobeløb for linjen, når salgsordrer, tilbud og returneringer importeres. Det forklarer også, hvordan du kan styre funktionsmåden i forskellige versioner af Microsoft Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Hvordan opdateringer til nettolinjebeløb beregnes ved import

Supply Chain Management version 10.0.23 introduceret [fejlrettelse 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Denne fejlrettelse har ændret de betingelser, hvor feltet **Nettobeløb** på en linje kan opdateres eller genberegnes, når opdateringer til eksisterende salgsordrer, returordrer og tilbud importeres. I version 10.0.29 kan du erstatte denne fejlrettelse ved at deaktivere funktionen *Beregn linjenettobeløb ved import*. Denne funktion har en lignende effekt, men den indeholder en global indstilling, der giver dig mulighed for at vende tilbage til den gamle funktionsmåde, hvis det er nødvendigt. Selvom den nye funktionsmåde gør, at systemet fungerer mere effektivt, kan det give uventede resultater i specifikke scenarier, hvor følgende betingelser er opfyldt:

- Data, der opdaterer eksisterende poster, importeres via *Salgsordrelinjer V2*, *Salgstilbudslinjer V2* eller *Returordrelinjer* ved hjælp af Open Data Protocol (OData), herunder situationer, hvor du bruger dobbeltskrivning, import/eksport via Excel og tredjepartsintegration.
- [Politikker for evaluering af samhandelsaftale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper), som er på plads, etablerer en ændringspolitik, der begrænser opdateringer til feltet **Nettobeløb** på salgsordrelinjer, salgstilbudslinjer og/eller returordrelinjer.
- De importerede data omfatter ændringer i feltet **Nettobeløb** på linjer eller ændringer (f.eks. enhedspris, antal eller rabat), der vil medføre, at værdien i feltet **Nettobeløb** på linjer genberegnes for en eller flere eksisterende linjeposter.

I disse specifikke scenarier er virkningen af evalueringspolitikken for samhandelsaftalen, at der bliver sat en begrænsning på opdateringer af feltet **Nettobeløb** på linjen. Denne begrænsning kaldes en *ændringspolitik*. På grund af denne politik bliver du af systemet bedt om at bekræfte, om du vil foretage ændringen, når du bruger brugergrænsefladen til at redigere eller genberegne feltet. Når du importerer en post, skal systemet dog foretage et valg for dig. Før version 10.0.23 blev nettobeløbet for linjen uændret, medmindre nettobeløbet på den indgående linje var 0 (nul). I nyere versioner opdaterer eller genberegner systemet dog altid nettobeløbet efter behov, medmindre det udtrykkeligt bliver bedt om ikke at gøre det. Selvom den nye funktionsmåde er mere logisk, kan det give problemer for dig, hvis du allerede kører processer eller integrationer, der antager den ældre funktionsmåde. I denne artikel beskrives, hvordan du kan vende tilbage til den gamle metode, hvis det er nødvendigt.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Kontrollere beregninger af linjenettobeløb i version 10.0.29 og senere

Supply Chain Management-version 10.0.29 introducerede en funktion med navnet *Beregn linjenettobeløb ved import*. Denne funktion tilføjer en indstilling med navnet **Beregn linjenettobeløb** på siden **Debitorparametre**. Du kan bruge denne indstilling til at vælge mellem de nye og ældre funktioner til beregning af linjenettobeløb ved import.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Aktivere eller deaktivere funktionen til beregning af linjenettobeløb ved import

Når du opdaterer til version 10.0.29, er funktionen *Beregn linjenettobeløb ved import* som standard slået til, og den nye indstilling **Beregn linjenettobeløb** angives som standard til *Ja*. Indstillingen *Ja* svarer til den nye standardfunktionsmåde. Den stemmer overens med systemfunktionsmåden, når funktionen er deaktiveret, undtagen i tilfælde af funktionaliteten af [parameteren CalculateLineAmount](#CalculateLineAmount), som beskrevet senere i denne artikel. Indstillingen *Nej* stemmer overens med systemfunktionsmåden før version 10.0.23 og er hovedsageligt med for at understøtte ældre integrationsscenarier.

Administratorer kan aktivere eller deaktivere funktionen *Beregn linjenettobeløb ved import* ved hjælp af [arbejdsområdet til funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Angive indstillingen Beregn linjenettobeløb

Når funktionen *Beregn linjenettobeløb ved import* er slået til, kan du angive indstillingen **Beregn linjenettobeløb** ved at følge disse trin.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Under fanen **Priser** i oversigtspanelet **Beregning af linjenettobeløb via integration** skal du angive indstillingen **Beregn linjenettobeløb** til en af følgende værdier:

    - *Ja* – Systemet genberegner og opdaterer altid linjebeløb, hvis det er nødvendigt. (Det ignorerer derfor politikken for evaluering af samhandelsaftale).
    - *Nej* – Hvis det eksisterende eller indgående nettobeløb for en linje er 0 (nul), genberegnes værdien for den pågældende linje på basis af andre værdier (f.eks. enhedspris, antal og rabat). Hvis det eksisterende eller indgående nettobeløb afviger fra 0 (nul), og der er angivet en ændringspolitik for feltet **Nettobeløb** på linjen, genberegnes eller opdateres feltet ikke, selv når indgående ændringer i linjeprisen, antallet og/eller rabatten medfører, at linjetotalen burde genberegnes. Denne funktionsmåde stemmer overens med version 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Hvordan funktionen Beregn linjenettobeløb ved import påvirker parameteren CalculateLineAmount

Når funktionen *Beregn linjenettobeløb ved import* er aktiveret, har værdien af parameteren `CalculateLineAmount` for tabellerne `SalesLine` og `SalesQuotationLine` ingen virkning. I stedet styres funktionaliteten globalt af indstillingen **Beregn linjenettobeløb**, der er beskrevet i forrige afsnit. Når funktionen er aktiveret, må du derfor ikke være afhængig af `CalculateLineAmount`-værdien.

Når funktionen *Beregn linjenettobeløb ved import* er deaktiveret, fungerer parameteren `CalculateLineAmount` for tabellerne `SalesLine` og `SalesQuotationLine` som i Supply Chain Management version 10.0.23 til og med 10.0.28, som beskrevet i næste afsnit.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontrollere beregninger af linjenettobeløb i version 10.0.28 og tidligere

Da [fejlrettelse 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) blev introduceret i version 10.0.23, blev det muligt at vælge, hvordan hver relevante dataenhed skal opføre sig, når et linjenettobeløb blev redigeret eller skulle genberegnes på grund af andre ændringer (f.eks. en opdateret varepris). Du kan styre denne funktionsmåde ved at angive den nye `CalculateLineAmount`-parameter for hver linje til en af følgende værdier i den importerede fil:

- **`CalculateLineAmount` = *1*** – Feltet **Nettobeløb** på linjen genberegnes og opdateres altid, uanset om der er angivet en ændringspolitik for feltet, og uanset værdien af det indgående eller eksisterende nettobeløb på linjen.
- **`CalculateLineAmount` = *0*** – Hvis det eksisterende eller indgående nettobeløb for en linje er 0 (nul), genberegnes værdien for den pågældende linje på basis af andre værdier (f.eks. enhedspris, antal og rabat). Hvis det eksisterende eller indgående nettobeløb afviger fra 0 (nul), og der er angivet en ændringspolitik for feltet **Nettobeløb** på linjen, genberegnes eller opdateres feltet ikke.  

Systemfunktionsmåden afhænger af din version af Supply Chain Management:

- I version 10.0.22 og tidligere fungerer systemet altid som om, at `CalculateLineAmount` er angivet til *0*, og det er på ingen måde muligt at få det til at fungere, som om `CalculateLineAmount` er angivet til *1*.
- I version 10.0.23 til og med 10.0.28 fungerer systemet, som om `CalculateLineAmount` er angivet til *1* for alle linjer, hvor det ikke udtrykkeligt er angivet til *0* i importfilen.
