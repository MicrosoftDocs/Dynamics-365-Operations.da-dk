---
title: Opret og vedligehold en lagerblokering
description: Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549765"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opret og vedligehold en lagerblokering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter. Du kan køre proceduren i USMF-demodatafirmaet ved hjælp af eksempelværdierne, der vises. Du skal have en vare med en tilgængelig fysisk disponibel lagerbeholdning, før du begynder denne procedure.


## <a name="create-an-inventory-blocking"></a>Opret en lagerblokering
1. Gå til Lagerstyring > Periodiske opgaver > Lagerblokering.
2. Klik på Ny.
3. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
4. Vælg den vare, du vil bruge, på listen. 
    * Vælg et varenummer med fysisk disponibel lagerbeholdning, du vil blokere. Hvis du bruger USMF, kan du vælge vare M9201.  
5. Angiv et tal i feltet Antal.
    * Hvis du bruger vare M9201, skal du vælge mindre end 200.  
6. Slå udvidelsen af sektionen Lagerdimensioner til/fra.
7. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
8. Find og vælg den ønskede post på listen.
    * Hvis du bruger vare M9201, kan du vælge lagersted 51.  
9. Klik på Gem.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Opdater betingelserne for lagerblokeringen
1. Angiv et tal i feltet Antal.
    * Opdater feltet fast lagerantal for at afspejle mængden, der skal blokeres.  
2. Indtast en dato i feltet Forventet dato.
    * Du vil måske angive, hvornår det blokerede lager forventes at blive tilgængeligt for reservation ved at tildele en forventet dato. Hvis den indstillingen Forventede tilgange er markeret for lagerblokeringen, som den er som standard, når du manuelt opretter en blokering, vises denne dato på den forventede transaktion.  
3. Klik på Gem.

## <a name="remove-the-inventory-blocking"></a>Fjern lagerblokeringen
1. Klik på Slet.
2. Klik på Ja.
3. Luk siden.

