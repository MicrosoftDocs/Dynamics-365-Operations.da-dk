---
title: Få produktanbefalinger ved hjælp af demo-data
description: Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042774"
---
# <a name="get-product-recommendations-using-demo-data"></a>Få produktanbefalinger ved hjælp af demo-data
Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.

Omni-kanalproduktanbefalinger giver et sæt redaktionelt leverede eller programmeringsmæssigt fremstillede lister over produkter. Disse lister kan bruges i flere forskellige scenarier, afhængigt af virksomhedens behov. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

For niveau 2 og højere Dynamics 365-miljøer beregnes produktanbefalinger automatisk ud fra kundedata. Hvis du bruger demodata til produktanbefalinger, deaktiveres ingen af de anbefalinger for produktløsninger, der allerede er klargjort i miljøet, og eventuelle omkostninger, der er forbundet med brugen af dem.

Produktanbefalinger for niveau 1-miljøer er udelukkende baseret på de statiske demodata, der er gemt i en .csv-fil.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivere demodata til produktanbefalinger i et miljø
Du skal udrulle Dynamics 365 Commerce-prøveversionens demoudvidelse i det respektive miljø for at aktivere demodata til produktanbefalinger. Hvis du gør det automatisk, aktiveres demodata til produktanbefalinger.

## <a name="default-demo-data"></a>Standarddemodata
Hvert Onebox-typemiljø indeholder et forudindlæst sæt demodata til produktanbefalinger, der er gemt i den kommaseparerede fil 'reco_demo_data.csv', som er placeret på Commerce Scale Unit.

Disse data er struktureret langs følgende kolonner.

| Kolonnenavn         | Obligatorisk          | Beskrivelse                                                                                                                                 | Mulige værdier                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Den specifikke listetype for produktanbefalinger, som demodatapunktet skal generere.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Det specifikke driftsenhedsnummer, hvor produktanbefalinger forventes at blive synlige.                                        |                                                                              |
| Kategori            |                    |    Den kategori, som den specifikke liste skal returneres for. Hvis der ikke er angivet en kategori, gælder listen kun for det øverste navigationshierarki.    |                                                                              |
| SeedItemId          |                    |    Til lister, der kræver oprindelsesdata (RecoPeopleAlsoBuy og RecoCart), skal produktet indeholde supplerende produkter til disse lister.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Et eller flere produkter, der skal returneres som resultat, adskilt af ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Tilpasse demodata
Du kan redigere standarddemodataene med eventuelle produkt- og kategorioplysninger, der er konfigureret i hovedkontoret. Når du opdaterer .csv-filen, afspejler de produktanbefalinger, der returneres til kunderne, straks ændringerne.

Udvidelsen indeholder en datafil med navnet 'RecoMockDataset.csv', som giver dig mulighed for at styre det datasæt, der bruges til at styrke de anbefalede resultater. Filnavnet kan styres via udvidelseskonfiguration ved hjælp af indstillingen **ext.Recommendations.DemoFilePath**. Det giver dig mulighed for at have flere tilgængelige datasæt, der kan skiftes mellem nemt og hurtigt under konfigurationen.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Miljøplanlægning](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
