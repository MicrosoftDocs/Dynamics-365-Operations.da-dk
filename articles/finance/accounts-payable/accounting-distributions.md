---
title: Regnskabsfordelinger
description: Dette emne indeholder oplysninger om regnskabsfordelinger og beskriver de indstillinger, der er tilgængelige ved behandling af dem.
author: ShylaThompson
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a627ba33065086d21c758a1b8d8f2fa2f6ef02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441715"
---
# <a name="accounting-distributions"></a>Regnskabsfordelinger

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om regnskabsfordelinger og beskriver de indstillinger, der er tilgængelige ved behandling af dem. Regnskabsfordelinger bruges til at allokere pengebeløb til et kildedokument til bestemte finanskonti. 

Regnskabsfordelinger er en funktion i hele programmet, der bruges og udvides med hvert kildedokument, som en indkøbsordre, kreditorfaktura, udgiftsrapport og fritekstfaktura. Som standard genereres der en regnskabsfordeling for hver kildedokumentlinje og pengebeløb og er betinget aktiveret til redigering. 

> [!NOTE] 
> Nogle dokumenter understøtter også pengebeløb i dokumenthovedet, f.eks. gebyrer for ordrer og fakturaer. 

Funktioner til generisk regnskabsfordeling indeholder følgende indstillinger til behandling af regnskabsfordelinger:

-   **Distribuer beløb** – Få vist og ret de regnskabsmæssige fordelinger for et enkelt linje dokumenthoved eller en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter.
    -   For de øverste pengebeløbsfordelinger (overordnede fordelinger) kan hovedkonto og økonomiske dimensioner være redigerbare direkte i det segmenterede postkontrolelement i gitteret. Den udvidede pris er et typisk eksempel på en sådan overordnet fordeling.
    -   Fordelingsbeløbene er baseret på begrebet valuta for dokumentet. Denne valuta er typisk transaktionsvalutaen. Beløb i regnskabs- og rapporteringsvalutaen genereres som en del af regnskab for reskontro.
    -   Fordelingerne viser regnskabsdatoen og regnskabshændelse. Regnskabshændelsen er typisk indstillet til **Ingen**, indtil dokumentet er bogført/journaliseret. På dette tidspunkt bliver regnskabshændelsen **Oprindelig**. Når fordelingerne er bogført, kan du ikke redigere fordelingerne.
    -   **Opdel**-knappen kan være aktiveret for overordnede fordelinger. **Opdel** genererer nye regnskabsfordelinger, og opdelingen kan være baseret på procentdel, beløb eller antal.
    -   Knappen **Fordel ligeligt** kan bruges i kombination med **Opdel** for automatisk at fordele beløbet ligeligt på tværs af alle fordelinger.
    -   Knappen **Nulstil** kan aktiveres for overordnede fordelinger, når der findes mere end én fordeling. **Nulstil** vender manuel ændring af fordelingen ved at slette alle eksisterende fordelinger og oprette standardfordelingerne igen.
    -   Alle underordnede fordelinger, f.eks. rabat, gebyr og moms, følger altid den overordnede fordeling. Du kan få vist den overordnede/underordnede relation til **Reference** &gt; **Overordnede oplysninger**.
    -   Hovedkontoen og den økonomiske dimension kan også være redigerbar for børn.
    -   De økonomiske dimensioner på regnskabsfordelinger følger et standardmønster, som dokument kan udvide.
    -   Afvigelsesfordelinger kan genereres i matchende situationer, f.eks. som en matching mellem en kreditorfaktura og en købsordre. Du kan få vist de tilsvarende forbindelser mellem regnskabsfordelingen i **Reference** &gt; **Dokumentoplysninger**.
    -   **Korrekt**-knappen vises og er aktiveret for dokumenter, der understøtter rettelser. **Korrekt** opretter nye fordelinger. Først oprettes fordelinger, som tilbagefører de oprindelige fordelinger. Disse fordelinger kan ikke ændres. Derefter oprettes nye korrekte regnskabsfordelinger. Disse fordelinger kan ændres, hvis de oprindelige fordelinger kunne ændres.
    -   Knappen **Projektoplysninger** er aktiveret som en udvidelse, når en linje er knyttet til et projekt. Projektregnskabsfordelinger giver dig mulighed for at redigere detaljer som finansieringskilde og linjeegenskab.
    -   Du kan se den aktuelle regnskabsstatus i **Reference**. Status er for hele dokumentet, og angiver, om dokumentet er i gang eller afsluttet.
-   **Få vist fordelinger** – Få vist regnskabsfordelingerne for alle linjerne og pengebeløbene i dokumentet. Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.

I version 10.0.13 er der tilføjet en funktion, der validerer regnskabsfordelingstabellen for at sikre, at nye felter konfigureres korrekt. Denne funktion kaldes **Aktivér yderligere validering af data for dokumenter ved hjælp af kildedokumentets regnskabsstruktur**. Hvis du vil bruge denne funktion, skal du aktivere den ved hjælp af arbejdsområdet **Funktionsstyring**. Hvis du vil aktivere funktionen, skal du søge efter funktionsnavnet i feltet **Søg** på siden **Funktionsstyring** og derefter vælge **Aktivér nu**.

Du kan finde flere oplysninger under [Regnskabsfordelinger og kladdeposteringer for reskontro til kreditorfakturaer](accounting-distributions-subledger-journal-entries-vendor-invoices.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]