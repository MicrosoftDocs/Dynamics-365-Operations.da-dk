---
title: "Overføre fysisk lager på lagersted"
description: "Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde med henblik på at registrere flytning af en vare fra én lokalitet på et lagersted til en anden."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Overføre fysisk lager på lagersted

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde med henblik på at registrere flytning af en vare fra én lokalitet på et lagersted til en anden. Du skal have oprettet et lagerkladdenavn for lageroverførsler, før du begynder på dette. Du kan gennemgå denne procedure i demodatafirmaet USMF ved hjælp af eksempel-værdierne, der vises, eller du kan bruge dine egne data, hvis du har konfigurerede produkter og lokaliteter. Disse opgaver udføres normalt af en lagermedarbejder.


## <a name="create-an-inventory-transfer-journal"></a>Oprette en lageroverførselskladde
1. Gå til Overfør.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Navn.
4. Klik på OK.
    * Der er mulighed for at angive 'Fra' og 'Til'-dimensioner for hver kladdelinje. Disse er væsentlige for denne kladdetype. Du kan overflytte varer til lokalitet ved hjælp af forskellige regler. I dette eksempel vil vi overføre en vare inden for det samme lager fra en nummerpladestyret lokalitet til en lokalitet, der ikke er nummerpladestyret.   

## <a name="create-journal-lines"></a>Oprette journallinjer
1. Klik på Ny.
2. Indtast eller vælg en værdi i feltet Varenummer.
    * Hvis du bruger USMF, kan du vælge 'A0001'.  
3. Indtast eller vælg en værdi i feltet Fra sted.
    * Hvis du bruger USMF, kan du vælge '2'.  
4. Indtast eller vælg en værdi i feltet Til sted.
    * Hvis du bruger USMF, kan du vælge '2'.  
5. Indtast eller vælg en værdi i feltet Fra lagersted.
    * Hvis du bruger USMF, kan du vælge '24'.  
6. Indtast eller vælg en værdi i feltet Til lagersted.
    * Hvis du bruger USMF, kan du vælge '24'.  
7. Indtast eller vælg en værdi i feltet Fra lokalitet.
    * Hvis du bruger USMF, kan du vælge 'FL-001'.  
8. Indtast eller vælg en værdi i feltet Til lokalitet.
    * Hvis du bruger USMF, kan du vælge 'BULK-001'.  
9. Angiv et tal i feltet Antal.
10. Klik på fanen Lagerdimensioner.
11. Indtast eller vælg en værdi i feltet Nummerplade.
    * Hvis du bruger USMF, kan du vælge '24'.  
12. Klik på Gem.

## <a name="post-the-inventory-transfer-journal"></a>Bogfør lageroverførselskladden
1. Klik på Bogfør.
2. Klik på OK.

## <a name="view-inventory-transactions"></a>Få vist lagertransaktioner
1. Klik på lager.
2. Klik på Transaktioner.
    * Her kan du se de posteringer, der blev oprettet, da du bogførte kladden.  

