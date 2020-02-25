---
title: Lagersøgning i POS
description: Dette emne beskriver de indstillinger, der er tilgængelige for visning af lageroplysninger i salgsstedet (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 1d6133d80d7674a1d896bc19a743a6bd4d0fb40f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022044"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Lagersøgning i POS

[!include [banner](includes/banner.md)]

Lagersøgning i salgsstedet (POS) hjælper detailhandlere med at opnå flotte resultater i realtid og få indsigt ved at forbinde butikker, salgstedet og administrationen. Denne funktion giver en præcis visning af produktlageret i realtid på tværs af butikker og distributionscentre. Det hjælper også detailhandlere med at fremme effektiviteten og omkostningsbesparelser ved at forbedre lagerplanlægning i realtid.

En præcis visning af lageret for hele virksomheden i realtid hjælper lagermedarbejdere med at levere rettidig og fremragende kundeservice. Det vigtigste tidspunkt, er det øjeblik, hvor kunden er klar til at træffe en købsbeslutning. Det er vigtigt, at kasserere i butikken har lageroplysninger i realtid ved hånden, så de kan garantere præcis produktlevering og afhentning.

Du kan åbne siden **Lagersøgning** fra arbejdsområdet **Retail Modern POS** eller **Retail Cloud POS**.

![Feltet Lagersøgning på POS-startside](media/POSHomepage.png)

På siden **Lagersøgning** kan du bruge det numeriske tastatur til at angive et produktnummer. Du kan derefter få vist det disponible antal for flere butikker og lagersteder.

![Standardside for lagersøgning](media/InventoryLookUp.png)

Antal, der er **Reserveret** og **Bestilt**, vises også for hver lokation.

- **Reserveret** – Dette antal refererer til værdien **Fysisk reserveret** fra administrationen for det angivne produktnummer på lokationen.
- **Bestilt** – Dette antal refererer til værdien **Bestilt i alt** fra administrationen for det angivne produktnummer på lokationen.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Lokationer, som oplysninger om disponibel lagerbeholdning vises for

Listen over lokationer indeholder to typer enheder:

- **Butikker** – Listen viser butikker, der er konfigureret ved hjælp af butikssøgergruppen for den aktuelle butik i hovedkontoret.
- **Distributionscentre** – Forskellige typer distributionscentre (f.eks. lagersteder) kan konfigureres i Commerce. Listen viser dog kun oplysninger om disponibel lagerbeholdning for distributionscentre af typen **Standard**.

    > [!NOTE]
    > Oplysninger om disponibel lagerbeholdning vises ikke for lagersteder af typerne **Transit**, **Karantæne** og **Varer undervejs** for POS.

På siden **Lagersøgning** kan du få vist disponibel til tilsagn (DTT) for hver butik foruden de aktuelle disponible mængder, reserverede mængder og bestilte mængder. Vælg den butik, du vil se DTT-oplysninger for, og vælg derefter **Vis butikkens tilgængelighed**.

![ATP-antal](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Åbning af dimensionsbaseret matrix for at få vist alle varianter

På siden **Produktdetaljer** for en produktmaster eller på siden **Lagersøgning** skal du vælge **Vis alle varianter** fra applinjen nederst på siden. Visningen **Dimensionsbaseret matrix** for den første start af disse sider viser oplysninger om lagertilgængelighed for alle varianter af et produkt for den aktuelle butik.

> [!NOTE]
> Knappen **Vis alle varianter** er kun tilgængelig for vareproduktmastere med produktvarianter. Den er ikke tilgængelig for enkeltstående produkter eller pakker.

![Knappen Vis alle varianter på siden Lagersøgning](media/StandardToMatrix.png)

Vælg **Vis alle varianter** på siden **Produktdetaljer** for en produktmaster eller på siden **Lagersøgning** uden at vælge en lokation for at gå til visningen **Dimensionsbaseret matrix** for at se oplysninger om lagertilgængeligheden for alle varianter af et produkt for den aktuelle butik.

![Visningen Dimensionsbaseret matrix for siden Lagersøgning](media/Matrix.png)

> [!NOTE]
> I den foregående illustration vises dimensionerne i alfabetisk rækkefølge, fordi visningsrækkefølgen for dimensioner ikke var konfigureret for det valgte produkt.

I visningen **Dimensionsbaseret matrix** omfatter cellerne for produktvarianter en værdi for disponibel lagerbeholdning i nederste højre hjørne. Følgende tabel forklarer betydningen af de forskellige værdier.

| Beholdningsværdi                            | Betegnelse |
|------------------------------------------|-------------|
| Numerisk værdi, der er større end 0 (nul) | En variant er frigivet til den valgte lokation, og du kan udføre yderligere handlinger i cellen. (Disse handlinger er beskrevet nærmere senere i dette emne.) |
| **0** (nul)                             | En variant er blevet frigivet til den valgte lokation, men varen er ikke tilgængelig i den valgte lokation. Du kan dog udføre yderligere handlinger i cellen. (Disse handlinger er beskrevet nærmere senere i dette emne.) |
| **i/t** eller en inaktiv celle              | En variant er blevet frigivet til den valgte lokation, og du kan ikke udføre yderligere handlinger i cellen. |

Du kan også ændre pivot for dimensioner ved at vælge den nye dimension, der skal bruges.

![Ændring af pivot](media/ChangePivot.png)

![Pivot ændret](media/PivotChanged.png)

> [!NOTE]
> I de foregående illustrationer er visningsrækkefølgen af dimensioner for det valgte produkt brugerdefineret (ikke-alfabetisk). Den er baseret på den visningsrækkefølge for dimensionen, der er angivet i administrationen.

I visningen **Dimensionsbaseret matrix** kan der udføres flere handlinger for at øge butiksmedarbejderens produktivitet. Her er nogle eksempler:

- Skift af butikslokationen for at søge efter lagertilgængeligheden for alle produktvarianter på andre lokationer. Disse lokationer omfatter andre butikker i butikssøgergruppen og distributionscentrene af typen **Standard**.
- Sælg en enkelt produktvariant til en debitor ved hjælp af Cash & Carry, afhentning i butikken eller levering til en adresse.
- Giv debitoren DTT-oplysninger for en individuel produktvariant for en bestemt lokation.

![Yderligere handlinger for variantfelter](media/VariantActions.png)

> [!NOTE]
> I den foregående illustration vises dimensionerne i alfabetisk rækkefølge, fordi visningsrækkefølgen for dimensioner ikke var konfigureret for det valgte produkt.

Følgende tabel indeholder flere oplysninger om yderligere handlinger, der er tilgængelige.

| Handling               | Betegnelse |
|----------------------|-------------|
| Sælg nu             | Føj den valgte varevariant til transaktionen, og omdiriger brugeren til skærmbilledet for transaktionen. (Denne handling er ikke tilgængelig, når den valgte lokation er et distributionscenter). |
| Afhent i butik     | Opret en debitorordre for den produktvariant, som vil blive plukket fra den valgte lokation, og omdiriger brugeren til skærmbilledet for transaktionen. (Denne handling er ikke tilgængelig, når den valgte lokation er et distributionscenter). |
| Afsend produkt         | Opret en debitorordre for den produktvariant, som vil blive afsendt fra den valgte lokation, og omdiriger brugeren til skærmbilledet for transaktionen. |
| Tilgængelighed         | Vis DTT-oplysninger for den valgte variantkombination for den valgte lokation. |
| Vis alle lokationer   | Skift til standardvisningen for lagersøgning, og fremhæv oplysninger om lagertilgængeligheden for varevarianten på tværs af alle butikker i butikssøgergruppen, og i distributionscentre af tyden **Standard**. |
| Få vist produktdetaljer | Omdiriger brugeren til siden **Produktdetaljer** for den tilknyttede produktmaster. |
