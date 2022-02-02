---
title: Synkronisere momsopsætningen fra momsberegningstjenesten til Dynamics 365 Finance
description: Dette emne forklarer, hvordan du synkroniserer masterdata i momsopsætningen fra Momsberegningstjeneste til Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d5d994934014a146f825431cb53dfbef8fe20bc8
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965136"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Synkronisere momsopsætningen fra momsberegningstjenesten til Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du synkroniserer masterdata i momsopsætningen fra Momsberegningstjeneste til Microsoft Dynamics 365 Finance.

Når du har fuldført de nødvendige opsætningstrin i [Kom i gang med momsberegning](global-get-started-with-tax-calculation-service.md), synkroniseres følgende momsopsætningsdata automatisk fra Momsberegningstjeneste til Finance.

## <a name="sales-tax-code"></a>Momskode

| Momsberegningstjeneste           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Skattekode                          | Momskode                      |
| Beskrivelse                       | Navn                                |
| Brugerinput                        | Afregningsperiode                   |
| Brugerinput                        | Finanskonteringsgruppe                |
| Brugerinput                        | Momsvaluta                  |
| En negativ momssats konfigureres | Tillad en negativ momsprocent |

## <a name="tax-value"></a>Momsværdi

| Momsberegningstjeneste | Finance                   |
| ----------------------- | ------------------------- |
| Fra posteringsdato   | Fra-dato                 |
| Til posteringsdato     | Til-dato                   |
| Minimumsbeløb          | Minimumsgrænse             |
| Maksimalt beløb          | Maksimumgrænse             |
| Momssats                | Værdi                     |
| Ikke-fradragsberettiget sats     | Ikke-fradragsberettiget procent |

## <a name="tax-limits"></a>Momsgrænser

| Momsberegningstjeneste | Finance           |
| ----------------------- | ----------------- |
| Fra posteringsdato   | Fra-dato         |
| Til posteringsdato     | Til-dato           |
| Minimummomsbeløb      | Minimumsmoms |
| Maksimummomsbeløb      | Maksimumsmoms |

## <a name="sales-tax-group"></a>Momsgruppe

| Momsberegningstjeneste                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Skattegruppe                                       | Momsgruppe                            |
| Momskoder i denne momsgruppe                  | Varemomskoder i denne varemomsgruppe |
| Momskoden er markeret som **Er momsfri**         | Frit                                     |
| Momskoden er markeret som **Er momsfri**         | Fritagelseskode                                |
| Momskoden er markeret som **Er modtagermoms** | Modtagermoms                             |
| Momskoden er markeret som **Er importmoms**        | Importmoms                                    |

## <a name="item-sales-tax-group"></a>Varemomsgruppe

| Momsberegningstjeneste             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Varemomsgruppe                      | Varemomsgruppe                            |
| Momskoder i denne varemomsgruppe | Varemomskoder i denne varemomsgruppe |

Når synkroniseringen er fuldført, skal du fortsætte med at vedligeholde de resterende parametre i Finance til bogførings- og rapporteringsformål.

> [!NOTE]
> Synkronisering af momsopsætningen fra Finance til Momsberegningstjeneste understøttes ikke. I et eksisterende Finance-miljø skal du først oprette momsopsætningen i Momsberegningstjeneste. Synkroniser derefter konfigurationsdataene tilbage til Finance-miljøet.
