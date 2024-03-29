---
title: Lagring af Rapporten Aldersfordelt lager
description: Denne artikel beskriver de funktioner, der giver mulighed for at køre en aldersfordelt lagerrapport, og gøre outputtet tilgængeligt som en formel og et diagram.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875562"
---
# <a name="inventory-aging-report-storage"></a>Lagring af Rapporten Aldersfordelt lager

[!include [banner](../includes/banner.md)]

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]