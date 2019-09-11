---
title: Opret og vedligehold en lagerblokering
description: Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916593"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opret og vedligehold en lagerblokering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter. Du kan køre proceduren i USMF-demodatafirmaet ved hjælp af eksempelværdierne, der vises. Du skal have en vare med en tilgængelig fysisk disponibel lagerbeholdning, før du begynder denne procedure.


## <a name="create-an-inventory-blocking"></a>Opret en lagerblokering
1. I **navigationsruden** skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Lagerblokering**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
4. Vælg den vare, du vil bruge, på listen. Vælg et varenummer med fysisk disponibel lagerbeholdning, du vil blokere. Hvis du bruger USMF, kan du vælge vare M9201.  
5. Angiv et tal i feltet **Antal**. Hvis du bruger vare M9201, skal du vælge mindre end 200.
6. Udvid oversigtspanelet **Lagerdimensioner**.
7. Klik på rullelisten i feltet **Lagersted** for at åbne opslaget.
8. Find og vælg den ønskede post på listen. Hvis du bruger vare M9201, kan du vælge lagersted 51.  
9. Klik på **Gem**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Opdater betingelserne for lagerblokeringen
1. Skriv et tal i feltet **Antal** i oversigtspanelet **Generelt**. Opdater feltet fast lagerantal for at afspejle mængden, der skal blokeres.  
2. Indtast en dato i feltet **Forventet dato**. Du vil måske angive, hvornår det blokerede lager forventes at blive tilgængeligt for reservation ved at tildele en forventet dato. Hvis den indstillingen Forventede tilgange er markeret for lagerblokeringen, som den er som standard, når du manuelt opretter en blokering, vises denne dato på den forventede transaktion.  
3. Klik på **Gem**.

## <a name="remove-the-inventory-blocking"></a>Fjern lagerblokeringen
1. Klik på **Slet** i **handlingsruden**.
2. Klik på **Ja**.
3. Luk siden.

