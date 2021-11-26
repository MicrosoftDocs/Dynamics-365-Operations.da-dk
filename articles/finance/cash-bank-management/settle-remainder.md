---
title: Udlign rest
description: Du kan udligne restbeløbet fra udligningsaktivitet ved at anvende dette beløb på en finanskonto.
author: roschlom
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 216c5c1d7db72e5f5071f2cd03656df538a64e72
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7754090"
---
# <a name="settle-remainder"></a>Udlign rest

[!include [banner](../includes/banner.md)]

Du kan udligne restbeløbet fra udligningsaktivitet ved at anvende dette beløb på en finanskonto eller på en anden debitor. Du kan udligne restbeløbet, når du udligner beløb, der er angivet i en kladde, eller når du kun udligner åbne posteringer.

## <a name="setting-up-defaults"></a>Konfigurere brugerstandarder 
Du skal aktivere funktionen Udlign rest og konfigurere standardindstillingerne, før du kan bruge Udlign rest

1)  Klik på **Debitor > Parametre > Udligninger** eller **Kreditor > Parametre > Udligninger**
2)  Vælg fanen **Udligning**, og klik på **Aktivér udlign rest**
3)  I **Standardårsagskode** skal du vælge en standardårsagskode. Årsagskoderne skal allerede være oprettet **Debitor > Opsætning > Årsagskoder for debitorafskrivning** eller **Kreditor > Opsætning > Årsagskoder for debitorafskrivning**. **Standardudligningskonto for rest** bliver standard for den konto, der er tildelt til årsagskoden for afskrivningen.
3)  Opdater **Standardudligningskonto for rest** efter behov.
4)  I **Standardkladdenavn** skal du vælge en betalingskladde, der skal bruges, hvis du vil oprette en betalingskladde, når du kun udligner åbne posteringer. Hvis du aktiverer funktionen til udligning af restbeløb, skal du tilføje et standardkladdenavn.

## <a name="settle-remainder-from-a-journal"></a>Udligne rest fra en kladde
Hvis du ikke aktiverer funktionen **Udlign rest**, kan du stadig angive en transaktion i en kladde og derefter udligne posteringer mod den som tidligere. Når du klikker på knappen **OK**, reduceres den åbne saldo på fakturaen med kontantbeløbet. Hvis beløbet ikke helt udligner fakturaen, forbliver fakturaen åben med et restbeløb, der skal udlignes på et senere tidspunkt.

Når funktionen **Udlign rest** er aktiveret, kan du udligne det resterende beløb på en finanskonto. Du kan også overføre restbeløbet til en anden debitorkonto (for debitorposteringer) eller en anden kreditor (for kreditorposteringer) i stedet for at lade fakturaerne forblive åbne. 

Gør følgende for at udligne restbeløbet fra siden **Udligning**:

1)  På siden **Udligning** skal du markere de fakturaer eller posteringer, der skal udlignes.
2)  Klik på knappen **Udlign rest**.
3)  En dialogboks viser det beløb, der udlignes mod en finanskonto, den dato, hvor restbeløbet udlignes, standardårsagskoden fra parametrene og standardkontoen fra parametrene. 
4)  Vælg en ny udligningsårsag, hvis du vil ændre standardårsagen. Udligningskontoen ændres til den konto, der er knyttet til årsagskoden.
5)  Rediger udligningskontoen, hvis du vil ændre den.
6)  Hvis du udligner debitorposteringer, og du vil flytte restbeløbet til en anden debitor, skal du vælge en debitor i **Udlign rest mod debitorkonto**. Hvis du udligner kreditorposteringer, og du vil flytte restbeløbet til en anden kreditor, skal du vælge en kreditor i **Udlign rest mod kreditorkonto**.
6)  Klik på **Udlign rest**.
7)  Siden **Kladde** vises. Der føjes en ekstra linje til kladden med restudligningsbeløbet som beløbet og kontoen for udligningsrestbeløbet som modkonto. Hvis du har tilføjet en debitor eller kreditor, så du kan flytte udligningsbeløbet til en anden debitor eller kreditor, føjes der en ekstra linje til kladden, så udligningsbeløbet kan flyttes til den pågældende debitor eller kreditor.

Når du bogfører kladden, udlignes den åbne postering helt. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Udligne rest, når du kun udligner åbne posteringer
Du kan også udligne resten, når du udligner åbne posteringer uden en kladde.

For at udligne restbeløbet skal du udføre følgende trin:

1)  På siden **Udligning** skal du markere de fakturaer eller posteringer, der skal udlignes.
2)  Klik på **Udlign rest**.
3)  En dialogboks viser det beløb, der udlignes mod en finanskonto, den dato, hvor restbeløbet udlignes, standardårsagskoden fra parametrene og standardkontoen fra parametrene. 
4)  Vælg en ny udligningsårsag, hvis du vil ændre standardårsagen. Udligningskontoen ændres til den konto, der er knyttet til årsagskoden.
5)  Rediger **udligningskontoen**, hvis du vil ændre den.
6)  Hvis du udligner debitorposteringer, og du vil flytte restbeløbet til en anden debitor, skal du vælge en debitor i **Udlign rest mod debitorkonto**. Hvis du udligner kreditorposteringer, og du vil flytte restbeløbet til en anden kreditor, skal du vælge en kreditor i **Udlign rest mod kreditorkonto**.
7)  Du kan også vælge at oprette en betalingskladde med udligningsrestbeløbet eller blot bogføre det uden en kladde. Vælg **Ja** for **Rediger i kladde** for at oprette en betalingskladde. Du kan redigere den betalingskladde, som du opretter.
8)  Klik på **Udlign rest**. Hvis du vælger at oprette en kladde, ændres knappen til **Opret kladde**. Klik på **Opret kladde** i stedet.
9)  Hvis du har oprettet en betalingskladde, åbnes kladdesiden, når du klikker på **Udlign rest**. Der føjes en linje til kladden med restudligningsbeløbet som beløbet og kontoen for udligningsrestbeløbet som modkonto. Hvis du har tilføjet en debitor eller kreditor, så du kan flytte udligningsbeløbet til en anden debitor eller kreditor, føjes der en ekstra linje til kladden, så udligningsbeløbet kan flyttes til den pågældende debitor eller kreditor.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
