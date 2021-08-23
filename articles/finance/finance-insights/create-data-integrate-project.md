---
title: Opret et dataintegratorprojekt (prøveversion)
description: Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: a32ad6eb1b1874a9f9ec452def3c213cd160c5faa2aec02b655a86e160e2b509
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768981"
---
# <a name="create-a-data-integrator-project-preview"></a>Opret et dataintegratorprojekt (prøveversion)

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter et dataintegratorprojekt.

1. Log på Microsoft Dynamics 365 Finance.
2. Gå til **Arbejdsområder \> Datastyring**, og vælg **Dataenheder**. Vent, indtil alle dataenheder er opdateret, før du går videre til næste trin.
3. Åbn [Power Apps-portalen](https://make.powerapps.com/), og udfør følgende trin:

    1. Vælg det relevante miljø.
    2. Vælg **Data \> Forbindelser** i den venstre navigationsrude.
    3. Opret forbindelse til de relevante forekomster af følgende elementer:

        - Dynamics 365
        - Fin og Ops til Dynamics 365

4. Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:

    1. Vælg **Dataintegrator**.
    2. Vælg **Forbindelsessæt**.
    3. Vælg **Nyt forbindelsessæt**.
    4. Angiv et navn for forbindelsen.
    5. Vælg de relevante forbindelser for følgende emner:

        - Dynamics 365
        - Fin og Ops til Dynamics 365

    6. Vælg den relevante organisationstilknytning.
    7. Vælg **Opret**.

5. Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:  

    1. Opret dataintegrationsprojekter til følgende skabeloner ved hjælp af det forbindelsessæt, du lige har oprettet:

        - Resultater af indsigt i kundebetaling (CDS til Fin og Ops)
            - Hvis du bruger version 10.0.17 eller senere, skal du bruge skabelonen med navnet Resultater af indsigt i kundebetaling (CDS til Fin og Ops 10.0.17+).
        - Pengestrømsresultater for likviditetsserier (CDS Fin og Ops)
        - Budgetresultater for tidsserier (CDS Fin og Ops)

    2. Angiv den relevante planlægning for hvert projekt.

> [!NOTE]
> Hvis du ikke kan se de påkrævede enheder i CDS, skal du gå til **Kredit og rykkere > Opsætning > Finance Insights > Finance Insights-parametre**, aktivere funktionen Debitorbetalingsforudsigelser og klikke på knappen **Opret forudsigelsesmodel**. Når implementeringen af AI-modellen er fuldført (med eller uden succes), vil de CDS-enheder, der skal bruges til at oprette integrationen, blive installeret i CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
