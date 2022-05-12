---
title: Der blev ikke fundet noget matchende resultat
description: Dette emne forklarer, hvordan du kan foretage fejlfinding af fejlen "Der kunne ikke findes nogen tilsvarende resultat" i serivce for momsberegning.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645392"
---
# <a name="no-matching-result-could-be-found"></a>Der blev ikke fundet noget matchende resultat

[!include [banner](../includes/banner.md)]

Dette emne forklarer de fejlfindingstrin, du kan udføre, hvis du modtager fejlen "Der blev ikke fundet nogen tilsvarende resultater" i tjenesten Momsberegning.

## <a name="symptom"></a>Symptom

Du får vist følgende fejlmeddelelse: "Overskrift/Linjer - 1, Momsgruppe, der blev ikke fundet nogen tilsvarende resultat".

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Årsag

Problemet opstår, når funktionsopsætningen i RCS (Regulatory Configuration Service) ikke er korrekt.

## <a name="troubleshoot"></a>Fejlfinding

1. Hent fejlfindingsfilen. Du kan finde flere oplysninger under [Aktivere ændringssporing for enheder](tcs-troubleshooting-enable-debug-mode.md).
2. Sammenlign indgående momsserviceberegning med funktionsopsætningen for at rette opsætningsproblemet.

    I følgende eksempel vises input til beregning af momstjenesten.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Følgende tabel viser anvendeligheden af momsgruppen i RCS.

    | Overskrift: Forretningsproces | Linjer. Virksomhedsenhed | Header.Ship Fra postnummer | Momsgruppe |
    |-------------------------|---------------------|---------------------------|-----------|
    | Kladde                 |                     |                           | Gruppe A   |
    | Sales                   |                     | 30160                     | Gruppe B   |

    Ifølge indgående momsserviceberegning er værdien for **forretningsprocessen** i overskriften **Salg**, og værdien **Afsendelse fra postnummer** er **30159**. Dette input er baseret på opsætningen af anvendelighedsregler i RCS. Da der ikke findes en tilsvarende linje, opstår fejlen.

    > [!NOTE]
    > Hvis værdien i anvendelsesreglen er tom, gælder reglen for alle værdier.

## <a name="mitigation"></a>Afhjælpning

Du kan løse denne fejl ved at udføre disse trin:

1. Gå til **Globaliseringsfunktionerne** \> **Momsberegning** i RCS.
2. Opret en ny version af funktionen.
3. Tilføj en linje for tilhørende oplysninger.

    | Overskrift: Forretningsproces | Linjer. Virksomhedsenhed | Header.Ship Fra postnummer| Momsgruppe |
    |-------------------------|---------------------|--------------------------|-----------|
    | Kladde                 |                     |                          | Gruppe A   |
    | Sales                   |                     | 30160                    | Gruppe B   |
    | Sales                   |                     | 30159                    | Gruppe B   |

4. Udgiv versionen af funktionsopsætningen.
5. I Microsoft Dynamics 365 Finance skal du gå til **Moms** \> **Opsætning** \> **Momskonfiguration** \> **Momsberegningsparametre** og vælge en ny version.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
