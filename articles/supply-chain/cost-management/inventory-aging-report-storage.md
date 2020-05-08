---
title: Lagring af Rapporten Aldersfordelt lager
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
ms.openlocfilehash: 9148a9032615222a1fdfe453488e716bacadbabc
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275573"
---
# <a name="inventory-aging-report-storage"></a>Lagring af Rapporten Aldersfordelt lager


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du køre rapporten **Lager for aldersfordelt lagerrapport** og gøre outputtet tilgængeligt som en formular og et diagram. I formularen reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det konfigurerede layout. Diagrammet indeholder en visuel oversigt, der understøtter filtrering og giver dig mulighed for at gå i detaljer. Derudover giver en dataenhed ved navn **Aldersfordelt lagerrapport** dig mulighed for at eksportere resultaterne af rapporten **Lager for aldersfordelt lagerrapport** til et format som f.eks en Microsoft Excel-fil eller en PDF-fil.

Denne metode til kørsel af rapporten **Lager for aldersfordelt lagerrapport** er nyttig i de tilfælde, hvor outputtet indeholder mange linjer. Outputtet indeholder f.eks. mange linjer, hvis du har 50.000 varer og 300 butikker, der oprettes som lagersteder, og du anmoder om lagerets aldersfordeling pr. vare, lokation og lagersted.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Aktivere lagerrapportfunktionen for lagerværdi

Før du kan bruge denne funktion, skal du aktivere den i dit system. Administratorer kan bruge indstillingerne [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Her er funktionen angivet som:

- **Modul** - Omkostningsstyring
- **Funktionsnavn** - Lager for aldersfordelt lagerrapport

## <a name="run-an-inventory-aging-report-storage"></a>Køre en Lager for aldersfordelt lagerrapport

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lager for aldersfordelte lagerrapporter**.
1. Vælg **Ny**.
1. kriv et entydigt navn for rapporten i feltet **Procesidentifikator – Navn**.
1. Vælg rapporten **Identifikation – Id**, og filtrer den efter behov.

    Rapportafviklingen udføres altid i et batchjob.

1. Når batchjobbet er fuldført, vises outputtet på siden **Lager for aldersfordelt lagerrapport**.
1. Hvis du vil have vist outputtet som en formular med et traditionelt gitterlayout, skal du vælge **Vis detaljer**. Hvis du vil have vist outputtet som et samlet diagram, skal du vælge **Vis diagram**.

    > [!NOTE]
    > Formularen omfatter ikke subtotaler, der er defineret i rapportlayoutet.

Med dataenheden **Aldersfordelt lagerrapport** kan du eksportere outputtet fra rapporten **Lager for aldersfordelt lagerrapport** ved at anvende et filter i feltet **Procesindentifikator – Navn** for et hvilket som helst format, som Datastyring understøtter.
