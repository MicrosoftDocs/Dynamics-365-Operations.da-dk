---
title: Momskoden kan ikke bestemmes
description: Dette emne forklarer, hvordan du kan rette fejlen "Der kunne ikke opnås adgang til momsservice" i momsberegningstjenesten.
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
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645387"
---
# <a name="tax-code-cannot-be-determined"></a>Momskoden kan ikke bestemmes

[!include [banner](../includes/banner.md)]

Dette emne forklarer de fejlfindingstrin, du kan udføre, hvis du modtager fejlen "Der blev ikke fundet nogen tilsvarende resultater" i tjenesten Momsberegning.

## <a name="symptom"></a>Symptom

Du får vist følgende fejlmeddelelse: "Overskrift/Linjer - 1, momskode kan ikke bestemmes". Du kan også finde fejlen i fejlfindingsfilen som vist i følgende eksempel. Du kan finde flere oplysninger under [Aktivere ændringssporing for enheder](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

Problemet opstår sandsynligvis, fordi momsgruppen og vareafgiftsgruppen ikke indbyrdes.

## <a name="troubleshoot"></a>Fejlfinding

Følg disse trin for at løse dette problem.

1. Kontrollér, at momsgruppen og vareskatsgruppen er fastlagt, i fejlfindingsfilen. Hvis værdierne for **Momsgruppe** og **Varemomsgruppe** er tomme, er momsgruppen og varemomsgruppen ikke fastlagt. Hvis de er fastlagt, kan resultaterne være forkerte.

    Her er et eksempel på en fejlfindingsfil.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. Kontroller, at indstillingen **Tilsidesæt salgsmoms** under fanen **Opsætning** af oplysningerne på salgsordrelinjen er aktiveret.

    - Hvis den er aktiveret, bestemmes momskoderne af værdierne for **Momsgruppen** og **Varemomsgruppen**, som du angiver på transaktionslinjen. Kontroller, at disse værdier er angivet korrekt.
    - Hvis den ikke er aktiveret, skal du kontrollere, at der er angivet korrekte værdier for felterne **Anvendelse af momsgruppe** og **Anvendelse af varemomsgruppe**. Yderligere oplysninger finder du i [Intet tilsvarende resultat](tcs-troubleshooting-no-matching-result.md).

3. Hvis momsgruppen og vareafgiftsgruppen er angivet korrekt, skal du afgøre, om der er et skæringspunkt for dem.

    1. I RCS skal du gå til **Momsfunktioner** \> **Momskoder og grupper** \> **Momsgruppe**.

        | Line.Tax-gruppe | Momskoder |
        |----------------|-----------|
        | Gruppe A        | A         |

    2. Gå til **Momsfunktioner** \> **Momskoder og grupper** \> **Varemomsgruppe**.

        | Line.Item-momsgruppe | Momskoder |
        |---------------------|-----------|
        | Gruppe B             | B         |

    Hvis der ikke er et skæringspunkt for momsgruppen og varemomsgruppen, bestemmes momskoden ikke.

## <a name="mitigation"></a>Afhjælpning

1. Gå gennem hvert trin i afsnittet [Fejlfinding](#troubleshoot) i dette emne, og ret installationen efter behov. Hvis momsgruppen og vareafgiftsgruppen ikke er fastlagt korrekt, kan du finde [Ingen tilsvarende resultater](tcs-troubleshooting-no-matching-result.md).
2. Hvis der ikke er et skæringspunkt for momsgruppen og vareafgiftsgruppen, skal du oprette en ny funktionsversion i RCS og rette opsætningen.

    - Gå til **Momsfunktioner** \> **Momskoder og grupper** > **Varemomsgruppe**.

        | Line.Item-momsgruppe | Momskoder |
        |---------------------|-----------|
        | Gruppe B             | A;B       |

    Momskoden fastsættes som **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
