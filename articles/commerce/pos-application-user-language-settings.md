---
title: Indstillinger for POS-program og brugersprog
description: Denne artikel beskriver, hvordan du ændrer indstillinger for sprog i Modern POS (MPOS) og Cloud POS.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288373"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Indstillinger for POS-program og brugersprog

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du ændrer indstillinger for sprog i Modern POS (MPOS) og Cloud POS.

## <a name="overview"></a>Oversigt
Modern POS (MPOS) og Cloud POS understøtter miljøer, hvor indstillinger for sprog og oversættelser kan variere mellem butikken og brugerindstillingerne. Butikken kunne for eksempel være placeret i et område, hvor engelsk er mest almindelige for deres kunder, men nogle arbejdere foretrækker at bruge programmet med franske oversættelser.

## <a name="data-language"></a>Datasprog

Uanset brugerens indstillinger bruger MPOS og sky POS altid butikkens sprogindstillinger til at bestemme de oversættelser, der bruges til data. Dette sikrer, at alle brugere og kunder får en ensartet oplevelse. Eksempler på data omfatter:

- Produkter
- Attributter og værdier
- Kategorinavne
- Transaktionskvitteringer, der er udskrevet eller sendt på mail
- Navne på betalingsmetoder
- Linjevisningsmeddelelser

Butikkens sprog bruges også til de hoved POS-logonskærmen, da brugeren ikke er kendt, inden du logger på. Hvis en oversættelse ikke er tilgængelig for butikkens sprog, gendannes POS til virksomhedens sprog.

### <a name="configuring-the-stores-language-setting"></a>Konfigurere butikkens sprogindstilling

Butikkens sprogindstilling er angivet fra **Alle butikker** på siden **Butik** under **Generelt &gt; Internationale indstillinger &gt; Sprog**. Brug rullelisten til at vælge sproget for hver butik.

## <a name="user-interface-language"></a>Sprog i brugergrænseflade

POS-brugerens sprogindstilling bestemmer de oversættelser, der bruges i programmets brugergrænseflade. Dette omfatter alle etiketter, menuer og lister, der ikke betragtes som data. Eneste undtagelse er den tekst, der vises på POS-knapmatricer. Knapmatricer understøtter ikke oversættelser, så de viser altid teksten, der er defineret på knappen. For at understøtte oversatte knapper skal du kopiere og vedligeholde særskilte knapmatricer og tildele dem til brugerne efter behov.

### <a name="configuring-the-users-language-setting"></a>Konfigurere brugerens sprogindstilling

POS-brugerens sprogindstilling er angivet under **Alle arbejdere** på siden **Arbejder** under **Retail og Commerce &gt; Sprog**. Den er ikke indstillet under Profil-hovedfanen. Denne indstilling bruges ikke af POS. Hvis brugerens sprog ikke er angivet, eller det er indstillet til et sprog, hvor oversættelser er ikke tilgængelige, vender POS tilbage til butikkens sprog.

| &nbsp;      | Sprog i brugergrænseflade                | Datasprog (produkter, kvitteringsformater, linjevisning osv.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Regnskab** | Standard                    | Standard                                                       |
| **Butik**   | Tilsidesætter firma          | Tilsidesætter firma                                             |
| **Bruger**    | Tilsidesætter butik eller firma | Aldrig                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
