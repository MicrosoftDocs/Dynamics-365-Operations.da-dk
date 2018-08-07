---
title: "Optælle lager på et lagersted"
description: "Denne procedure fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokalitet på lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Optælle lager på et lagersted

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokalitet på lageret. Proceduren gælder for "grundlæggende lagerfunktioner", der er tilgængelige i modulet Lager, ikke for den lagerfunktion, der er tilgængelig i modulet Lagerstedsstyring. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger dine egne data, skal du kontrollere, at produkter og lokaliteter er konfigureret, og at du har oprettet et lagerkladdenavn for optællingskladder. Optælling af lager udføres normalt af en lagermedarbejder.


## <a name="create-an-inventory-counting-journal"></a>Opret en lageroptællingskladde
1. Gå til Lagerstyring > Kladdeposteringer > Vareoptælling > Optælling.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. På listen skal du klikke på det lageroptællingskladdenavn, du vil bruge
    * Nogle andre felter udfyldes baseret på opsætningen af det lageroptællingskladdenavn, du vælger.  
5. Klik på rullelisten i feltet Arbejder for at åbne opslaget.
6. Vælg den arbejder, du vil bruge, på listen.
7. Klik på Vælg.
8. Klik på OK.

## <a name="create-journal-lines"></a>Oprette journallinjer
1. Klik på Ny.
2. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
    * Hvis du bruger demodatafirmaet USMF, kan du vælge 'A0001'.  
4. Klik på rullelisten i feltet Sted for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
    * Hvis du bruger demodatafirmaet USMF, skal du vælge stedet '2'.  
6. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
    * Hvis du bruger demodatafirmaet USMF, skal du vælge lagerstedet '24'.  
8. Klik på rullelisten i feltet Lokation for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
    * Hvis du bruger demodatafirmaet USMF, skal du vælge lokaliteten 'BULK-001'.  
10. Angiv et tal i feltet Optalt.
    * Hvis du angiver et optalte antal, der adskiller sig fra det tal, der vises i feltet Beholdning, opdateres feltet Antal for at vise forskellen.  
11. Klik på Gem.

## <a name="post-the-inventory-counting-journal"></a>Bogfør lageroptællingskladden
1. Klik på Bogfør.
    * Når du bogfører en lageroptællingskladde, og det optalte beløb er forskelligt fra det beløb, der rapporteres i feltet Beholdning, bogføres en lagertilgang eller lagerafgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.  
2. Klik på OK.

## <a name="view-inventory-transactions"></a>Få vist lagertransaktioner
1. Klik på lager.
2. Klik på Transaktioner.
    * Her kan du se alle relaterede posteringer, der oprettes, når du bogfører din lageroptællingskladde.   

