---
title: Optælle lager på et lagersted
description: Dette emne fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokation på lagerstedet.
author: MarkusFogelberg
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cc89e3773005502c193364a721a835fe01dde9f1f22046e9c10c7d186b508d5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768137"
---
# <a name="count-inventory-in-a-warehouse"></a>Optælle lager på et lagersted

[!include [banner](../../includes/banner.md)]

Dette emne fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokation på lagerstedet. Proceduren gælder for "grundlæggende lagerfunktioner", der er tilgængelige i modulet Lager, ikke for den lagerfunktion, der er tilgængelig i modulet Lagerstedsstyring. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger dine egne data, skal du kontrollere, at produkter og lokaliteter er konfigureret, og at du har oprettet et lagerkladdenavn for optællingskladder. Optælling af lager udføres normalt af en lagermedarbejder.


## <a name="create-an-inventory-counting-journal"></a>Opret en lageroptællingskladde
1. Gå til **Navigationsrude > Moduler > Lagerstyring > Kladdeposteringer > Vareoptælling > Optælling**.
2. Vælg **Ny**.
3. I feltet **Navn** skal du vælge det lageroptællingskladdenavn, du vil bruge, på rullelisten. Nogle andre felter udfyldes baseret på opsætningen af det lageroptællingskladdenavn, du vælger.  
4. Vælg rullelisten i feltet **Arbejder** for at åbne opslaget.
5. **Vælg** den arbejder, du vil bruge, på listen.
6. Vælg **OK**.

## <a name="create-journal-lines"></a>Opret kladdelinjer
1. Vælg **Ny**.
2. Vælg den ønskede post på rullelisten i feltet **Varenummer**. Hvis du bruger demodatafirmaet USMF, skal du vælge **A0001**.  
3. Vælg den ønskede post på rullelisten i feltet **Sted**. Hvis du bruger demodatafirmaet USMF, skal du vælge stedet **2**.
4. Vælg den ønskede post på rullelisten i feltet **Lagersted**. Hvis du bruger demodatafirmaet USMF, skal du vælge lagerstedet **24**.  
5. Vælg den ønskede post på rullelisten i feltet **Lokation**. Hvis du bruger demodatafirmaet USMF, skal du vælge lokationen **BULK-001**.  
6. Angiv et tal i feltet Optalt. Hvis du angiver et optalt antal, der adskiller sig fra det tal, der vises i feltet **Beholdning**, opdateres feltet **Antal** for at vise forskellen.  
7. Vælg **Gem**.

## <a name="post-the-inventory-counting-journal"></a>Bogfør lageroptællingskladden
1. Vælg **Bogfør**. Når du bogfører en lageroptællingskladde, og det optalte beløb er forskelligt fra det beløb, der rapporteres i feltet **Beholdning**, bogføres en lagertilgang eller lagerafgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.
2. Vælg **OK**.

## <a name="view-inventory-transactions"></a>Få vist lagertransaktioner
1. Vælg **Lager**.
2. Vælg **Transaktioner**. Her kan du se alle relaterede posteringer, der oprettes, når du bogfører din lageroptællingskladde.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]