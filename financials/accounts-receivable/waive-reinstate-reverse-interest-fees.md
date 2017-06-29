---
title: "Frafalde, genindføre eller tilbageføre rentegebyrer"
description: "I denne artikel beskrives det, hvordan du kan frafalde, genindføre og tilbageføre gebyrer for renter og gebyrer."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 97f5aa378aa11cb89176cbcba63e32f690833d47
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="waive-reinstate-or-reverse-interest-fees"></a>Frafalde, genindføre eller tilbageføre rentegebyrer

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du kan frafalde, genindføre og tilbageføre gebyrer for renter og gebyrer.

Du kan bruge knapperne under fanen **Indsaml** på listesiden **Alle debitorer** for at frafalde, tilbageføre eller genindføre gebyrer:

-   Frafaldte gebyrer eftergives. Du kan frafalde et gebyr, hvis f.eks. en debitor bestrider gebyret, og du ønsker at bevare den gode forretningsrelation, du har med debitoren.
-   Genindsatte gebyrer bliver skyldige igen. Du kan også genindsætte gebyrer, der tidligere er frafaldet. Det være nødvendigt at genindføre gebyrer, hvis du mener, at de ikke bør være frafaldet.
-   Tilbageførte gebyrer fjernes fra en debitors konto og er ikke længere skyldige. Du kan f.eks. tilbageføre gebyrer, hvis der er valgt en forkert rentesats til beregning af det beløb, en kunde skylder. Du kan bruge en separat proces til at genberegne rente og oprette en rentenota, der indeholder nye gebyrer for debitoren.

Alle disse handlinger ændrer en rentenota. En rentenota er et forretningsdokument, der informerer debitorer om, hvornår rente eller gebyrer opkræves deres konto. Når du frafalder eller tilbagefører rente eller gebyrer, oprettes der automatisk en kreditnota eller en korrektionsfaktura til udligning af gebyrerne. Hvis du genindfører frafaldne gebyrer, oprettes der automatisk en faktura med et debetbeløb for at genindfører de gebyrer, kunden skylder. Resultaterne af hver handling beskrives i det følgende tabel.

| Handling                                                                                                                                                                                                            | Resultat for debitoren                                                                                             | Behandl                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Frafald hele rentenotaer sammen med alle de renter og gebyrer, de omfatter. –eller– Vælg og frafald gebyrer eller renteposteringer, som indgår i rentenotaer.                                        | Gebyrerne eftergives.                                                                                           | Der oprettes en kreditnota, eller en korrektionsfaktura, for debitoren. Kreditnotaen bruges automatisk til at udligne kreditnotaen eller de renteposteringer eller gebyrer, du har valgt. Det udlignede beløb svarer til det samlede beløb af gebyrerne minus evt. tidligere betalinger, som kunden har foretaget, og minus evt. beløb, der tidligere er frafaldet eller afskrevet. Hvis beløbet på kreditnotaen overskrider det beløb, debitoren skylder, kan du konvertere kreditnotaen til en kreditorfaktura. Derefter kan du give debitoren en refusion.                                                       |
| Genindsæt hele rentenotaer sammen med alle de renter og gebyrer, de omfatter. –eller– Vælg og genindsæt gebyrer eller renteposteringer, som indgår i rentenotaer.                                | Det frafaldte beløb er skyldigt igen.                                                                                     | Der oprettes en faktura med et debetbeløb, og beløbet udlignes automatisk med de gebyrer, der tidligere er frafaldet. De faktiske rentenotaer genindsættes ikke. I stedet oprettes en faktura, der viser det beløb, som debitoren skylder. Kreditnotaerne, eller korrektionsfakturaerne, som er oprettet for at udligne frafaldne rentenotaer, kan stadig findes, hvis de ikke er brugt til at udligne rentenotaerne. Når dette sker, annulleres de udestående kreditnotaer. Udestående kreditnotaer udlignes som regel, når rentenotaer frafaldes. Der kan dog stadig være en udestående kreditnota, hvis en debitor har betalt en rentenota, også selvom debitoren bestrider gebyrerne. |
| Tilbagefør hele rentenotaer. –eller–Tilbagefør udvalgte renteposteringer, som indgår i rentenotaer. **Bemærk:** Du kan ikke tilbageføre et gebyr. Men du kan tilbageføre en hel rentenota, der omfatter et gebyr. | Debitoren skylder ikke længere gebyrerne. Hvis der genberegnes rente, skyldes gebyrerne imidlertid igen. | Processen er den samme som processen, når rentenotaer eller udvalgte renteposteringer frafaldes. Der oprettes en kreditnota, eller en korrektionsfaktura, for debitoren. Kreditnotaen bruges til automatisk at udligne rentenotaen. Du kan bruge en separat proces til at genberegne rente og oprette en ny rentenota.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Du kan også bruge en separat proces til at afskrive tab på debitorer. I denne proces markeres alle debitorposteringer til udligning, i stedet for kun at frafalde gebyrer, der en del af rentenotaer.

## <a name="adjust-interest-for-invoices"></a>Regulere rente for fakturaer
Ud over regulering af rentenotaer kan du også fjerne rentegebyrerne på fakturaer med brug af en af nedenstående processer. Begge processer regulerer desuden de relaterede rentenotaer.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Korrigere en faktura, der har en tilknyttet rente

Du kan korrigere en bogført faktura, der er inkluderet i en rentenota. I denne proces kopieres detaljerne fra den eksisterende faktura til en ny faktura, så kun de ønskede korrektioner udføres. Denne faktura annulleres, og der oprettes en ny faktura. Renten på transaktionen tilbageføres også på rentenotaen, hvis rentenotaen er bogført. 

Du kan foretage rettelsen ved hjælp af knappen **Ret faktura** i handlingsruden på fritekstfakturaen. Denne funktion er kun tilgængelig, hvis konfigurationsnøglen **Fri tekst til rettelse af faktura** er valgt.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Tilbageføre en debitorpostering, der har en tilknyttet rente

Du kan tilbageføre en debitorpostering på en faktura, hvis en faktura er oprettet forkert. Hvis den tilbageførte debitorpostering har rente, der er inkluderet på en rentenota, og hvis rentenotaen er bogført, tilbageføres renten på posteringen også på rentenotaen. Rentenotaen annulleres, hvis den ikke er bogført. 

Du kan tilbageføre debitorposteringer ved hjælp af knappen **Tilbagefør**på siden **Debitorposteringer**.

## <a name="waive-or-reinstate-interest-notes"></a>Frafalde eller genindsætte rentenotaer
Du kan frakalde eller genindføre alle gebyrer på de rentenotaer, du vælger. Når du frafalder gebyrer, kan det samlede beløb, der kan frafaldes, ikke overstige evt. fastsatte beløbsgrænser. Du kan kun genindsætte en rentenota, hvis den tidligere er frafaldet. 

Du kan frafalde eller genindføre rentenotaer ved hjælp af knappen **Rentenota** på siden **Indsaml** på siden **Debitor**.

## <a name="waive-or-reinstate-interest-transactions"></a>Frafalde eller genindsætte renteposteringer
Du kan frafalde eller genindføre bestemte renteposteringer på en rentenota i stedet for at regulere alle gebyrer på denne rentenota. Når du frafalder gebyrer, kan det samlede beløb, der kan frafaldes, ikke overstige evt. fastsatte beløbsgrænser. Du kan kun genindsætte en rentepostering, hvis den tidligere er frafaldet. 

Du kan frafalde eller genindføre rentenotaer ved hjælp af knappen **Posteringsrente** på fanen **Indsaml** på siden **Debitor**.

## <a name="waive-or-reinstate-fees"></a>Frafalde eller tilbageføre gebyrer
Du kan frafalde eller genindføre bestemte gebyrer på en rentenota i stedet for at regulere alle gebyrer på denne rentenota. Når du frafalder gebyrer, kan det samlede beløb, der kan frafaldes, ikke overstige evt. fastsatte beløbsgrænser. Du kan kun genindsætte et gebyr, hvis det tidligere er frafaldet. 

Du kan frafalde eller genindføre rentenotaer ved hjælp af knappen **Gebyr** på siden **Indsaml** på siden **Debitor**.

## <a name="reverse-interest-notes"></a>Tilbagefør rentenotaer
Du kan tilbageføre alle gebyrer på de rentenotaer, du vælger. Tilbageførte gebyrer fjernes fra en debitors konto og er ikke længere skyldige. Når rentenotaen er tilbageført, kan du genberegne rente og oprette en ny rentenota. 

Du kan tilbageføre rentenotaer ved hjælp af knappen **Rentenota**på siden **Indsaml** på siden **Debitor**.

## <a name="reverse-interest-transactions"></a>Tilbageføre renteposteringer
Du kan tilbageføre alle de renteposteringer, du vælger. Tilbageførte gebyrer fjernes fra en debitors konto og er ikke længere skyldige. Når transaktionerne er tilbageført, kan du genberegne rente og oprette en ny rentenota.

Du kan tilbageføre renteposteringer ved hjælp af knappen **Posteringsrente** på siden **Indsaml** på siden **Debitor**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Få vist historikken over reguleringer af gebyrer, der er frafaldet, genindsat eller tilbageført
Du kan få vist den detaljerede historik over reguleringer, der er foretaget af rentenotaer, f.eks. den bruger, der har angivet reguleringen, reguleringstypen, beløbet og hvornår reguleringen blev indtastet. Det kan f.eks. være, at du vil have vist tidligere reguleringer, der er angivet for en rentenota, før du opretter en ny rentenota. 

Du kan tilbageføre renteposteringer ved hjælp af knappen **Oversigt**på siden **Indsaml** på siden **Debitor**.




