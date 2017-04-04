---
title: "Tilknyttes et fælles sæt af medlemmer af dimensionen dimensionsmedlemmer til forskellige element"
description: "Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Tilknyttes et fælles sæt af medlemmer af dimensionen dimensionsmedlemmer til forskellige element

Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål.

Hvis du er en global virksomhed og overholder lovpligtige regnskabsmæssige krav, kan du bruge flere kontoplaner. Når du importerer dimensionsmedlemmer for omkostningselementer fra forskellige kontoplaner, kan det ende med en blanding af konti. Men disse konti kan faktisk have samme karakter, og du kan måske analysere og allokere omkostninger til dem ved hjælp af et fælles format.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Knytte dimensionsmedlemmer for omkostningselementer til et fælles format
Følgende eksempel viser, hvordan du, som omkostningscontroller, kan oprette en ny dimension til omkostningselement i omkostningsregnskab, der knytter omkostningselementers dimensionsmedlemmer fra den amerikanske kontoplanstruktur og den franske kontoplanstruktur til et fælles sæt dimensionsmedlemmer for omkostningselement. Du kan derefter bruge det fælles sæt dimensionsmedlemmer for omkostningselement til at analysere omkostningsdata fra de to juridiske enheder i omkostningsregnskabet for Finans.

| Kilde: amerikansk kontoplan                                          | Kilde: fransk kontoplan                                          | Nyt sæt fælles dimensionsmedlemmer for omkostningselement                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importerede dimensionsmedlemmer for omkostningselement fra amerikanske kontoplaner | Importerede dimensionsmedlemmer for omkostningselement fra franske kontoplaner | Tilknytning af amerikanske og franske dimensionsmedlemmer for omkostningselement til et fælles sæt |
| 5001: salg                                                           | 5001: salg og marketing                                               | 5000: salg og marketing                                             |
| 5030: annoncer                                                     | 6390: køb på lager\*                                                    | 7000: rengøringsudgifter                                                 |
| 7001: rengøringsudgifter                                               | 7001: rejseudgifter                                                      | 7001: rejseudgifter                                                   |

\*Dimensionsmedlemmet materiel køb franske omkostninger element ikke er tilknyttet.

## <a name="currency-conversion"></a>Valutaomregning
De forskellige kontoplaner, som du bruger, kan konfigureres til at bruge forskellige valutaer. I dette tilfælde skal du angive en valutaomregning, så omkostningsdata der behandles ved hjælp af den rigtige valuta, som er defineret i omkostningsregnskabet for Finans, hvor dimensionsmedlemmer for omkostningselement anvendes. I ovenstående eksempel bruges amerikanske dollar (USD) i omkostningsregnskabet for Finans, så du skal oprette en valutaomregning fra USD til euro (EUR) for at behandle transaktioner for det tilknyttede omkostningselement dimensionsmedlemmer.

## <a name="update-mappings-at-any-time"></a>Opdatere tilknytninger efter behov
Du kan opdatere tilknytningsdefinitionerne af en dimension med omkostningselement når som helst. Da tilknytningerne ikke er datorelaterede, anvendes ændringer, næste gang du behandler omkostningsposteringer eller kører omkostningsberegninger.


