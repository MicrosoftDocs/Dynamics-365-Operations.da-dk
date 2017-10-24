---
title: Afstemte kladder for regnskab mellem enheder
description: "Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Afstemte kladder for regnskab mellem enheder

[!include[banner](../includes/banner.md)]


Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans. 

Hvis kontoposter ikke afstemmes på samme niveau som de økonomiske dimensionsværdier, oprettes der automatisk flere poster for at afstemme kladden. Disse kontoposter bruger bogføringstyperne **Internt mellem enheder - debet** og **Internt mellem enheder - kredit** på siden **Konti til automatisk posteringer** til at bestemme hovedkontoen. Afdeling, som er det andet segment på finanskontoen, vælges f.eks. som den afstemmende økonomiske dimension, og følgende regnskabsposter er ved at blive oprettet.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

I så fald bestemmes følgende saldi:

-   For afdelingen MSP = 100,00 CR
-   For afdelingen NY = 100,00 DR

Følgende regnskabsposter oprettes derfor automatisk, så denne kladde afstemmes på niveauet for de økonomiske dimensionsværdier.

|                                   |           |
|-----------------------------------|-----------|
| (Internt mellem enheder - debet) – MSP – OU\_256 | 100,00 DR |
| (Internt mellem enheder - kredit) – NY – OU\_249 | 100,00 CR |






