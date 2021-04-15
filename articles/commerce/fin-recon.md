---
title: Økonomisk afstemning i detailbutikker
description: Dette emne beskriver økonomisk afstemning i detailbutikker for POS til Microsoft Dynamics 365 Commerce.
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0f57f3119039337922dcd4035e1c4d64e6ae7295
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792385"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Økonomisk afstemning i detailbutikker

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 Commerce version 10.0.10 og tidligere giver den funktionalitet, som POS-klienten har i forbindelse med processer ved dagens afslutning i detailbutikker, mulighed for at lade butiksassistenter og butikschefer udføre aktiviteter i forbindelse med dagens afslutning. De kan f.eks. lave kasseoptællinger, foretage skift lukket uden kontrol, afstemme skifteposteringer og lukke skift. Men der er ingen mulighed i POS til at færdiggøre de økonomiske oplysninger for skift, så de kan bruges til bogføring af regnskaber i Commerce Headquarters. Butikschefer er typisk ansvarlige for at udføre denne opgave. Før de kan godkende et skift, skal de gennemgå oplysningerne, foretage eventuelle nødvendige rettelser og færdiggøre totalerne for det pågældende skift. De endelige totaler skal derefter bogføres i regnskabsmoduler i Commerce Headquarters.

Derudover kan butikschefer i Commerce version 10.0.10 og tidligere kontrollere og foretage nogle reguleringer af opgørelseslinjer i Commerce Headquarters. Muligheden er dog begrænset, og butikschefer har sjældent adgang til Commerce Headquarters-klienten. Desuden kan der kun foretages gennemsyn og regulering af en økonomisk detailopgørelse, når der oprettes opgørelser i Commerce Headquarters. Denne proces er dog typisk en, der kører natten over. Butikschefer skal derfor vente på godkendelse af skift, når der oprettes økonomiske detailopgørelser i Commerce Headquarters.

I Commerce version 10.0.11 og senere kan butikschefer gennemgå, justere og færdiggøre deres skift i POS-klienten. Disse oplysninger bruges derefter til at oprette og bogføre økonomiske detailopgørelser i Commerce Headquarters.

> [!NOTE]
> Den funktionalitet, der er relateret til økonomisk afstemning i detailbutikker, fungerer kun, hvis sivende feedbaseret ordreoprettelse er slået til. Du kan få flere oplysninger under [Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Konfigurere økonomisk afstemning

Udfør følgende trin for at bruge funktionen til økonomisk afstemning.

1. Gå til arbejdsområdet **Funktionsstyring**, og aktivér funktionen **Detailopgørelser (sivende feed)**.
1. I POS-funktionalitetsprofilen for den relevante butik skal du angive indstillingen **Aktivér økonomisk afstemning i butik** til **Ja**.

## <a name="more-information-about-financial-reconciliation"></a>Flere oplysninger om økonomisk afstemning

Når funktionen til økonomisk afstemning er slået til, synkroniseres nogle af de parametre, der er defineret i oversigtspanelet **Opgørelse/ultimo** på siden **Detailbutikker** i Commerce Headquarters, med kanaldatabasen. Det samme sæt beregningskriterier og beløbsgrænser, der bruges til detailopgørelser, gennemtvinges.

Når handlingen **Luk skift** aktiveres, kontrollerer systemet, at de systemberegnede beløb og de erklærede beløb stemmer overens. Hvis de er forskellige, og forskellen overskrider den definerede tærskelværdi, bliver brugeren spurgt, om han eller hun vil foretage de nødvendige justeringer.

Der kan foretages reguleringer for de enkelte betalingsmidler. Når der er valgt et betalingsmiddel, kan brugeren få vist totalerne for forskellige posteringstyper og redigere totalerne for en bestemt posteringstype. Under redigering viser systemet det oprindeligt beregnede beløb og det tilsidesatte beløb for den pågældende posteringstype. Brugeren kan også angive bemærkninger som en del af redigeringsprocessen. Bemærkninger kan bruges til revisionsformål.

Brugerne kan ignorere valideringsprompterne og -meddelelserne og fortsætte med at lukke skiftet. Men hvis en bruger ignorerer valideringsprompterne, opstår de samme problemer og skal rettes, når skiftet posterer regnskaber i Commerce Headquarters.

Handlingen **Luk skift** i POS validerer også, at alle transaktioner i offlinedatabasen synkroniseres med kanaldatabasen. Hvis der ikke synkroniseres nogen posteringer, modtager brugeren en advarsel, da denne situation kan medføre, at systembeløbene ikke beregnes korrekt. I denne situation kan brugeren afslutte handlingen **Luk skift** og prøve at synkronisere offlineposteringer med kanaldatabasen. Alternativt kan brugeren manuelt justere de systemberegnede beløb til kontoen for de posteringer, der ikke synkroniseres, så det korrekte sæt af økonomiske tal afsluttes og bogføres. 

Når sivende feedbaseret bogføring bruges, så bogføringen af posteringer adskilles fra bogføringen af regnskabet, kan du vælge at justere de systemberegnede beløb for manglende offlineposteringer. På denne måde sikrer du, at regnskaberne altid er bogført og posteret korrekt, uanset om der mangler posteringer. Offlinetransaktioner kan synkroniseres med kanaldatabasen og Commerce Headquarters og derefter bogføres senere separat fra de økonomiske posteringer.

Oplysninger om økonomisk afstemning for et skift synkroniseres til Commerce Headquarters ved hjælp af P-job.

Økonomiske detailopgørelser i Commerce Headquarters beregner ikke totaler for at få vist detaljerne på opgørelseslinjerne. I stedet bruges de endelige beløb i POS-klienten til at oprette og bogføre økonomiske detailopgørelser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]