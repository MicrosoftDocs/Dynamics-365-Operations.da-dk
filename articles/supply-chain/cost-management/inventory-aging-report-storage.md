---
title: Rapporten Aldersfordelt lager
description: I dette emne beskrives de funktioner, der giver mulighed for at køre en aldersfordelt lagerrapport, og gøre outputtet tilgængeligt som en formel og et diagram.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201612"
---
# <a name="inventory-aging-report"></a>Rapporten Aldersfordelt lager


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du køre en rapport over **Lagerets aldersfordeling** og gøre outputtet tilgængeligt som en formular og et diagram. I formularen reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det konfigurerede layout. Diagrammet indeholder en visuel oversigt, der understøtter filtrering og giver dig mulighed for at gå i detaljer. Derudover giver en dataenhed ved navn **Aldersfordelt lagerrapport** dig mulighed for at eksportere resultaterne af en rapport over **Lagerets aldersfordeling** til et format som f.eks en Microsoft Excel-fil eller en PDF-fil.

Denne metode til kørsel af rapport over **Lagerets aldersfordeling** er nyttig i de tilfælde, hvor outputtet indeholder mange linjer. Outputtet indeholder f.eks. mange linjer, hvis du har 50.000 varer og 300 butikker, der oprettes som lagersteder, og du anmoder om lagerets aldersfordeling pr. vare, lokation og lagersted.

## <a name="run-an-inventory-aging-report"></a>Kør en Aldersfordelt lagerrapport

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lager for aldersfordelte lagerrapporter**.
1. Vælg **Ny**.
1. kriv et entydigt navn for rapporten i feltet **Procesidentifikator – Navn**.
1. Vælg rapporten **Identifikation – Id**, og filtrer den efter behov.

    Rapportafviklingen udføres altid i et batchjob.

1. Når batchjobbet er fuldført, vises outputtet på siden **Lager for aldersfordelt lagerrapport**.
1. Hvis du vil have vist outputtet som en formular med et traditionelt gitterlayout, skal du vælge **Vis detaljer**. Hvis du vil have vist outputtet som et samlet diagram, skal du vælge **Vis diagram**.

    > [!NOTE]
    > Formularen omfatter ikke subtotaler, der er defineret i rapportlayoutet.

Med dataenheden **Aldersfordelt lagerrapport** kan du eksportere outputtet fra en rapport for **Lagerets aldersfordeling** ved at anvende et filter i feltet **Procesindentifikator –Navn** for et hvilket som helst format, som Datastyring understøtter.
