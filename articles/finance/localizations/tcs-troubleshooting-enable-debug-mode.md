---
title: Aktivere fejlfindingstilstand i tjenesten Momsberegning
description: Denne artikel forklarer, hvordan du aktiverer fejlfindingstilstand i tjenesten Momsberegning, så du kan undersøge problemer.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620892"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Aktivere fejlfindingstilstand i tjenesten Momsberegning

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du aktiverer fejlfindingstilstand i tjenesten Momsberegning, så du kan undersøge problemer.

1. Tilføj **&debug=vs%2CconfirmExit&** til URL-adressen til AOS (applikationsobjektserveren), og opdater derefter siden.
2. Når du vælger **moms** til beregning af moms, åbnes en tekstfil med navnet **TaxServiceTroubleshootingLog.txt**. Filen **TaxServiceTroubleshootingLog.txt** indeholder **TaxableDocument** og beregningsparameteren. Disse resultater returneres fra skattetjenesten og undtagelsesoplysninger i forbindelse med fejlfinding.

## <a name="sample"></a>Prøve

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
