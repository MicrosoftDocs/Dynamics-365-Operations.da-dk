---
title: Fast tilgangspris
description: Denne artikel forklarer, hvordan du kan konfigurere og bruge faste tilgangspriser i Microsoft Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907574"
---
# <a name="fixed-receipt-price"></a>Fast tilgangspris

[!include [banner](../includes/banner.md)]

**Fast tilgangspris** er en indstilling, som du kan vælge i en varemodelgruppe, når du bruger en anden lagermodel end *Standardomkostning* eller *Glidende vægtet gennemsnit*. I tidligere versioner af Microsoft Dynamics AX kaldtes denne indstilling **Standardomkostning**. Den blev omdøbt til **Fast tilgangspris**, da den nye lagermodel for standardomkostninger blev introduceret i Dynamics AX 2012. Denne artikel forklarer, hvordan du kan konfigurere og bruge faste tilgangspriser i Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Om faste tilgangspriser

Når du markerer afkrydsningsfeltet **Fast tilgangspris** på siden **Varemodelgruppe** for en vare, bruger systemet tilgangsprisen som en standardomkostning for lagertilgangen. Hvis købsprisen og standardkostprisen, der er konfigureret for et produkt, er forskellige, bogføres differencen på kontoen **Vind ved fast tilgangspris** eller **Tab ved fast tilgangspris** og modposteres på den modkonto for **Modposteret fast tilgangspris**, som du angiver på siden **Lagerposteringsprofil**.

Da indstillingen **Fast tilgangspris** bruges sammen med forskellige lagermodeller (f.eks. FIFO (First In, First Out), LIFO (Last In, First Out) og vægtet gennemsnit), opretter processen *Lagerlukning og -regulering* stadig udligninger og reguleringer i henhold til det lagerprincip, du vælger på siden **Varemodelgruppe**. Reguleringerne foretages dog kun for afgange fra lageret.

Du har f.eks. konfigureret et produkt med en varemodelgruppe, hvor feltet **Lagermodel** er angivet til *FIFO*, og indstillingen **Fast tilgangspris** er markeret. Når du modtager lagerbeholdning via en indkøbsordre, angives lagerværdien til værdien af varens standardkostpris på tidspunktet for produkttilgangen. Når du fakturerer indkøbsordren, bogfører systemet standardkostprisen for det frigivne produkt på lagerkontoen, hvis fakturaprisen er anderledes. Det bogfører differencen på driftskontoen for fast tilgangspris. Når du senere sælger eller forbruger produktet, bruger systemet det løbende gennemsnit for varen på det tidspunkt, hvor salgsordrefakturaen blev bogført (medmindre du bruger afmærkning).

Når du kører *Lagerlukning og -regulering*, opretter systemet en udligning af den første afgang med den første tilgang. Forskellen mellem den tilgangspris, der er brugt på tilgangen, og det løbende gennemsnit, der er brugt på afgangen, bogføres i et nyt bilag.

## <a name="enable-fixed-receipt-prices"></a>Aktivere faste tilgangspriser

Benyt følgende fremgangsmåde for at aktivere faste tilgangspriser for en vare.

1. Gå til **Lagerstyring \> Opsætning \> Lagerbeholdning \> Varemodelgrupper**.
2. Opret en ny varemodelgruppe, eller vælg en eksisterende modelgruppe.
3. Markér afkrydsningsfeltet **Fast tilgangspris** i oversigtspanelet **Efterkalkulationsmetode og omkostningsindregning**.

    > [!NOTE]
    > Du kan ikke markere afkrydsningsfeltet **Fast tilgangspris**, hvis feltet **Lagermodel** er angivet til *Standardomkostning* eller *Glidende gennemsnit*.

4. Luk siden.

Når du har aktiveret indstillingen **Fast tilgangspris**, skal du opdatere lagerposteringsprofilen ved at følge disse trin.

1. Gå til **Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**.
1. Vælg **Vind ved fast tilgangspris** i kolonnen **Vælg** under fanen **Indkøbsordre**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Konfigurer den nye række, så den anvendes på den varemodelgruppe, du har aktiveret fast tilgangspris for, og angiv den hovedkonto, der bruges til at registrere vind ved fast tilgangspris for indkøbsordrer. Konfigurer andre indstillinger efter behov.
1. Vælg **Tab ved fast tilgangspris** i kolonnen **Vælg**. Tilføj en ny række, så den anvendes på den varemodelgruppe, du har aktiveret fast tilgangspris for, og angiv den hovedkonto, der bruges til at registrere tab ved fast tilgangspris for indkøbsordrer. Konfigurer andre indstillinger efter behov.
1. Vælg **Modposteret fast tilgangspris** i kolonnen **Vælg**. Tilføj en ny række, så den anvendes på den varemodelgruppe, du har aktiveret fast tilgangspris for, og angiv den hovedkonto, der bruges til at registrere modposteret fast tilgangspris for indkøbsordrer. Konfigurer andre indstillinger efter behov.
1. Vælg **Vind ved fast tilgangspris** i kolonnen **Vælg** under fanen **Lager**. Tilføj en ny række, så den anvendes på den varemodelgruppe, du har aktiveret fast tilgangspris for, og angiv den hovedkonto, der bruges til at registrere vind ved fast tilgangspris for lager. Konfigurer andre indstillinger efter behov.
1. Vælg **Tab ved fast tilgangspris** i kolonnen **Vælg**. Tilføj en ny række, så den anvendes på den varemodelgruppe, du har aktiveret fast tilgangspris for, og angiv den hovedkonto, der bruges til at registrere tab ved fast tilgangspris for lager. Konfigurer andre indstillinger efter behov.

> [!NOTE]
> Det anbefales normalt, at der i felterne **Vind ved fast tilgangspris** og **Tab ved fast tilgangspris** bruges samme hovedkonto til både indkøbsordrer og lager.

> [!IMPORTANT]
> Når du ændrer værdien i feltet **Pris** i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produkter**, værdireguleres det disponible lager ikke automatisk. Som en manuel løsning skal du åbne siden **Lukning og regulering** og vælge **Regulering \> Beholdning** i handlingsruden. Vælg derefter de varer, der er på lager, og reguler dem til den aktuelle pris. En klar fordel ved at bruge lagermodellen for standardomkostninger er, at den får systemet til automatisk at regulere lagerbeholdningen.
