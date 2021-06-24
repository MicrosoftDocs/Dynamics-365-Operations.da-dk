---
title: Aktivere budgetforslag (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222528"
---
# <a name="enable-budget-proposals-preview"></a>Aktivere budgetforslag (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du aktiverer funktionen budgetforslag i Finance Insights.

1. Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø. Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet. (Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Spring dette trin over, hvis du bruger version 10.0.20 eller senere, eller hvis du bruger en installation af Service Fabric. Finance Insights-team burde allerede have aktiveret funktionen til dig. Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.

2. Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:

    1. Vælg **Søg efter opdateringer**.
    2. Søg efter **Budgetforslag**, og aktiver funktionen.

3. Gå til **Budget \> Opsætning \> Grundlæggende budget \> Budgetforslag (prøveversion)**, og vælg **Aktiver funktion**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
