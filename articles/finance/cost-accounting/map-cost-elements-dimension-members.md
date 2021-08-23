---
title: Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer
description: Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b9ac59f305afd55edfcfb3b47bf38ddd44d92a706904f55a069a6a9fc9050825
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728025"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer

[!include [banner](../includes/banner.md)]

Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål.

Hvis du er en global virksomhed og overholder lovpligtige regnskabsmæssige krav, kan du bruge flere kontoplaner. Når du importerer dimensionsmedlemmer for omkostningselementer fra forskellige kontoplaner, kan det ende med en blanding af konti. Men disse konti kan faktisk have samme karakter, og du kan måske analysere og allokere omkostninger til dem ved hjælp af et fælles format.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Knytte dimensionsmedlemmer for omkostningselementer til et fælles format
Følgende eksempel viser, hvordan du, som omkostningscontroller, kan oprette en ny dimension til omkostningselement i omkostningsregnskab, der knytter omkostningselementers dimensionsmedlemmer fra den amerikanske kontoplanstruktur og den franske kontoplanstruktur til et fælles sæt dimensionsmedlemmer for omkostningselement. Du kan derefter bruge det fælles sæt dimensionsmedlemmer for omkostningselement til at analysere omkostningsdata fra de to juridiske enheder i omkostningsregnskabet for Finans.

| Kilde: amerikansk kontoplan                                          | Kilde: fransk kontoplan                                          | Nyt sæt fælles dimensionsmedlemmer for omkostningselement                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importerede dimensionsmedlemmer for omkostningselement fra amerikanske kontoplaner | Importerede dimensionsmedlemmer for omkostningselement fra franske kontoplaner | Tilknytning af amerikanske og franske dimensionsmedlemmer for omkostningselement til et fælles sæt |
| 5001: salg                                                           | 5001: salg og marketing                                               | 5000: salg og marketing                                             |
| 5030: annoncer                                                     | 6390: lagerkøb\*                                                    | 7000: rengøringsudgifter                                                 |
| 7001: rengøringsudgifter                                               | 7001: rejseudgifter                                                      | 7001: rejseudgifter                                                   |

\* Det franske dimensionsmedlem for omkostningselement er ikke tilknyttet.

## <a name="currency-conversion"></a>Valutaomregning
De forskellige kontoplaner, som du bruger, kan konfigureres til at bruge forskellige valutaer. I dette tilfælde skal du angive en valutaomregning, så omkostningsdata der behandles ved hjælp af den rigtige valuta, som er defineret i omkostningsregnskabet for Finans, hvor dimensionsmedlemmer for omkostningselement anvendes. I ovenstående eksempel bruges amerikanske dollar (USD) i omkostningsregnskabet for Finans, så du skal oprette en valutaomregning fra USD til euro (EUR) for at behandle transaktioner for det tilknyttede omkostningselement dimensionsmedlemmer.

## <a name="update-mappings-at-any-time"></a>Opdatere tilknytninger efter behov
Du kan opdatere tilknytningsdefinitionerne af en dimension med omkostningselement når som helst. Da tilknytningerne ikke er datorelaterede, anvendes ændringer, næste gang du behandler omkostningsposteringer eller kører omkostningsberegninger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]