---
title: Demodata til produktanbefalinger for omni-kanal
description: Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i trin-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225725"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Demodata til produktanbefalinger for omni-kanal

Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i trin-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.

Omni-kanalproduktanbefalinger giver et sæt redaktionelt leverede eller programmeringsmæssigt fremstillede lister over produkter. Disse lister kan bruges i flere forskellige scenarier, afhængigt af virksomhedens behov. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger.](product-recommendaitons-overview.md)

For niveau 2 og højere Dynamics-miljøer beregnes produktanbefalinger automatisk ud fra kundedata.
Hvis du bruger demodata til produktanbefalinger, deaktiveres ingen af de anbefalinger for produktløsninger, der allerede er klargjort i miljøet, og eventuelle omkostninger, der er forbundet med brugen af dem.

Produkt anbefalinger for niveau 1-miljøer er udelukkende baseret på de statiske demodata, der er gemt i en CSV-fil.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Aktivere demodata til produktanbefalinger i et miljø

Kunderne skal installere **Dynamics 365 Commerce Preview Demo Extension** i det respektive miljø, der automatisk aktiverer demodata til produktanbefalinger.

## <a name="default-demo-data"></a>Standarddemodata
Hvert Onebox-typemiljø indeholder et forudindlæst sæt demodata til produktanbefalinger, der er gemt i den kommaseparerede fil **'reco_demo_data.** , som er placeret i samme mappe som dette dokument på Retail Server.

Disse data er struktureret langs følgende kolonner

| Kolonnenavn         | Obligatorisk          | Beskrivelse                                                                                                                                 | Mulige værdier                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Den specifikke listetype for produktanbefalinger, som demodatapunktet skal generere.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Det specifikke driftsenhedsnummer, hvor produktanbefalinger forventes at bliver vist.                                        |                                                                              |
| Kategori            |                    |    Den kategori, som den specifikke liste skal returneres for. Hvis der ikke er angivet en kategori, gælder listen kun for det øverste navigationshierarki.    |                                                                              |
| SeedItemId          |                    |    Til lister, der kræver oprindelsesdata (RecoPeopleAlsoBuy og RecoCart), skal produktet indeholde supplerende produkter til disse lister.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Et eller flere produkter, der skal returneres som resultat, adskilt af **';'**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Tilpasse demodata
Kunder kan redigere standarddemodataene med eventuelle produkt- og kategorioplysninger, der er konfigureret i hovedkontoret. Når CSV-filen er opdateret, afspejler de produktanbefalinger, der returneres til kunderne, straks ændringerne.

Udvidelsen indeholder en datafil med navnet RecoMockDataset.csv, som giver kunden mulighed for at styre det datasæt, der bruges til at styrke de anbefalede resultater. Filnavnet kan styres via udvidelseskonfiguration ved hjælp af indstillingen **ext.Recommendations.DemoFilePath**. Det giver kunderne mulighed for at have flere tilgængelige datasæt, der kan skiftes mellem nemt og hurtigt under konfigurationen.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations-overview.md)

[Miljøplanlægning](environment-planning.md)
