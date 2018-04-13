--- 
title: "Oprette og bogføre en projektfaktura for en debitor i den offentlige sektor (Danmark)"
description: "Denne opgave hjælper dig med at oprette og bogføre en projektfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34dfd679d2f16367f59c5d688bb234eca0c56870
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-post-a-project-invoice-for-a-public-sector-customer-denmark"></a>Oprette og bogføre en projektfaktura for en debitor i den offentlige sektor (Danmark)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave hjælper dig med at oprette og bogføre en projektfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering. 



Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.



Det er den sjette af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge. Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.



Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.


## <a name="update-a-project-contract"></a>Opdater en projektkontrakt
1. Gå til Projektstyring og regnskab > Projekter > Projektkontrakter.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Projektkontrakt-id med værdien "000057".
    * Vælg en projektkontrakt, der har en debitorfinansieringskilde, der er aktiveret til elektronisk fakturering.  
3. Åbn detaljer for en projektkontrakt.
4. Udvid sektionen Finansieringskilder.
5. Klik på Detaljer.
6. Udvid afsnittet Andet.
7. Skriv en værdi i feltet Debitorrekvisition.
8. Skriv en værdi i feltet Kundereference.
9. Indtast eller vælg en værdi i feltet Kontakt-id.
10. Klik på Gem.

## <a name="create-a-project-transaction"></a>Opret en projekttransaktion
1. Gå til Projektstyring og regnskab > Vareopgaver > Varebehov.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Projekt-id.
    * Som et eksempel kan du bruge projekt-id '000057'.  
4. Indtast eller vælg en værdi i feltet Varenummer.
    * Som et eksempel kan du bruge varenummer 'D0001'.  
5. Klik på Administrer i handlingsruden.
6. Klik på Bogføring.
7. Klik på følgeseddel.
8. Udvid sektionen Parametre.
9. Vælg "Alle" i feltet Antal.
10. Klik på OK.
11. Klik på OK.

## <a name="create-a-proposal-and-post-an-invoice"></a>Oprette et forslag og bogføre en faktura 
1. Gå til Projektstyring og regnskab > Projektfakturaer > Projektfakturaforslag.
2. Klik på Ny.
3. Klik på Fakturaforslag.
4. Indtast eller vælg en værdi i feltet Projekt.
5. Klik på OK.
6. Klik på Bogfør.
7. Klik på OK.
8. Klik på OK.

## <a name="generate-an-oioubl-project-invoice"></a>Oprette en OIOUBL projektfaktura
1. Gå til Projektstyring og regnskab > Projektfakturaer > Projektfakturaer.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Projektkontrakt-id med værdien "000057".
3. Klik på Projektfaktura i handlingsruden.
4. Klik på Send.
5. Klik på Oprindelig.

## <a name="view-an-oioubl-electronic-invoice"></a>Se en elektronisk OIOUBL faktura
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Elektroniske rapporteringsjob.
2. Klik på Vis filer.
3. Klik på Åbn.


