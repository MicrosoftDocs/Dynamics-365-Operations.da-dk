---
title: Oprette et dataintegrationsprojekt
description: Dette emne forklarer, hvordan du opretter et dataintegrationsprojekt.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 956524e3778eed9898374952466f70c37c99163f
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968931"
---
# <a name="create-a-data-integration-project"></a>Oprette et dataintegrationsprojekt

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter et dataintegrationsprojekt.

1. Log på Microsoft Dynamics 365 Finance.
2. Gå til **Arbejdsområder \> Datastyring**, og vælg **Dataenheder**. Vent, indtil alle dataenheder er opdateret, før du går videre til næste trin.
3. Åbn [Power Apps-portalen](https://make.powerapps.com/), og udfør følgende trin:

    1. Vælg det relevante miljø.
    2. Vælg **Dataverse \> Forbindelser** i den venstre navigationsrude.
    3. Opret forbindelse til de relevante forekomster af følgende elementer:

        - Dynamics 365
        - Fin og Ops til Dynamics 365

4. Åbn [Power Apps-miljøer](https://admin.powerapps.com/environments), og udfør følgende trin:

    1. Vælg **Dataintegration**.
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

        - Resultat af indsigt i kundebetaling (CDS til Fin og Ops 10.0.17+)
        - Pengestrømsresultater for likviditetsserier (CDS Fin og Ops)
        - Budgetresultater for tidsserier (CDS Fin og Ops)

    2. Angiv den relevante planlægning for hvert projekt.

> [!NOTE]
> Hvis du ikke kan se de påkrævede enheder i CDS, skal du gå til **Kredit og rykkere > Opsætning > Finance Insights > Finance Insights-parametre**, aktivere funktionen Debitorbetalingsforudsigelser og klikke på knappen **Opret forudsigelsesmodel**. Når implementeringen af AI-modellen er fuldført (med eller uden succes), vil de CDS-enheder, der skal bruges til at oprette integrationen, blive installeret i CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
