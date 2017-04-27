---
title: Indstillinger for POS-program og brugersprog
description: "Dette emne beskriver, hvordan du ændrer indstillinger for sprog i Retail Modern POS (MPOS) og Cloud POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Indstillinger for POS-program og brugersprog

[!include[banner](includes/banner.md)]


Dette emne beskriver, hvordan du ændrer indstillinger for sprog i Retail Modern POS (MPOS) og Cloud POS.

<a name="overview"></a>Overblik
========

Retail Modern POS (MPOS) og Cloud POS understøtter miljøer, hvor indstillinger for sprog og oversættelser kan variere mellem butikken og brugerindstillingerne. Butikken kunne for eksempel være placeret i et område, hvor engelsk er mest almindelige for deres kunder, men nogle arbejdere foretrækker at bruge programmet med franske oversættelser.

## <a name="data-language"></a>Datasprog
Uanset brugerens indstillinger bruger MPOS og sky POS altid butikkens sprogindstillinger til at bestemme de oversættelser, der bruges til data. Dette sikrer, at alle brugere og kunder får en ensartet oplevelse.  Eksempler på data omfatter:

-   Produkter
-   Attributter og værdier
-   Kategorinavne
-   Transaktionskvitteringer, der er udskrevet eller sendt på mail
-   Navne på betalingsmetoder
-   Linjevisningsmeddelelser

Butikkens sprog bruges også til de hoved POS-logonskærmen, da brugeren ikke er kendt, inden du logger på. Hvis en oversættelse ikke er tilgængelig for butikkens sprog, gendannes POS til virksomhedens sprog.

### <a name="configuring-the-stores-language-setting"></a>Konfigurere butikkens sprogindstilling

Butikkens sprogindstilling er angivet fra **Alle detailbutikker** på siden **Detailbutik** under **Generelt &gt; Internationale indstillinger &gt; Sprog. **Brug rullelisten til at vælge sproget for hver butik.

## <a name="user-interface-language"></a>Sprog i brugergrænseflade
POS-brugerens sprogindstilling bestemmer de oversættelser, der bruges i programmets brugergrænseflade. Dette omfatter alle etiketter, menuer og lister, der ikke betragtes som data. Eneste undtagelse er den tekst, der vises på POS-knapmatricer. Knapmatricer understøtter ikke oversættelser, så de viser altid teksten, der er defineret på knappen. For at understøtte oversatte knapper skal du kopiere og vedligeholde særskilte knapmatricer og tildele dem til brugerne efter behov.

### <a name="configuring-the-users-language-setting"></a>Konfigurere brugerens sprogindstilling

POS-brugerens sprogindstilling er angivet under **Alle arbejdere** på siden **Arbejder** under **Detail &gt; Sprog**.  Det er ikke angivet under hovedfanen Profil.  Denne indstilling bruges ikke af POS. Hvis brugerens sprog ikke er angivet, eller det er indstillet til et sprog, hvor oversættelser er ikke tilgængelige, vender POS tilbage til butikkens sprog.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Sprog i brugergrænseflade** ** **      | **Datasprog (produkter, kvitteringsformater, linjevisning osv.)** |
| **Regnskab** | Standard                    | Standard                                                           |
| **Butik**   | Tilsidesætter firma          | Tilsidesætter firma                                                 |
| **Bruger**    | Tilsidesætter butik eller firma | Aldrig                                                             |






