---
title: Aktivere budgetforslag (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646199"
---
# <a name="enable-budget-proposals-preview"></a>Aktivere budgetforslag (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.

1. Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø. Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet. (Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Hvis din installation af Microsoft Dynamics 365 Finance er en Service Fabric-installation, kan du springe dette trin over. Finance Insights-team burde allerede have aktiveret funktionen til dig. Hvis du ikke kan se funktionen i arbejdsområdet **Administration af funktioner**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du sende en e-mail til [Finance Insights Preview team](mailto:fiap@microsoft.com).

2. Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:

    1. Vælg **Søg efter opdateringer**.
    2. Søg efter **Budgetforslag**, og aktiver funktionen.

3. Gå til **Budget \> Opsætning \> Grundlæggende budget \> Budgetforslag (prøveversion)**, og vælg **Aktiver funktion**.

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.
