---
title: Regnskabsfordelinger
description: "Denne artikel indeholder oplysninger om regnskabsfordelinger og beskriver de indstillinger, der er tilgængelige ved behandling af dem. Regnskabsfordelinger bruges til at allokere pengebeløb til et kildedokument til bestemte finanskonti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a98ce08dc115bc96cec07c2d6ced10d774785fe9
ms.openlocfilehash: b1057caae6f47e5a17e194834fbbcb9d7d731605
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-distributions"></a>Regnskabsfordelinger

Denne artikel indeholder oplysninger om regnskabsfordelinger og beskriver de indstillinger, der er tilgængelige ved behandling af dem. Regnskabsfordelinger bruges til at allokere pengebeløb til et kildedokument til bestemte finanskonti. 

Regnskabsfordelinger er en funktion i hele programmet, der bruges og udvides med hvert kildedokument, som en indkøbsordre, kreditorfaktura, udgiftsrapport og fritekstfaktura. Som standard genereres der en regnskabsfordeling for hver kildedokumentlinje og pengebeløb og er betinget aktiveret til redigering. 

> [!Note] 
> Nogle dokumenter understøtter også hovedet dokument-pengebeløb, som gebyrer for ordrer og fakturaer. 

Funktioner til generisk regnskabsfordeling indeholder følgende indstillinger til behandling af regnskabsfordelinger:

-   **Distribuer beløb** – Få vist og ret de regnskabsmæssige fordelinger for et enkelt linje dokumenthoved eller en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter.
    -   For de øverste pengebeløbsfordelinger (overordnede fordelinger) kan hovedkonto og økonomiske dimensioner være redigerbare direkte i det segmenterede postkontrolelement i gitteret. Den udvidede pris er et typisk eksempel på en sådan overordnet fordeling.
    -   Fordelingsbeløbene er baseret på begrebet valuta for dokumentet. Denne valuta er typisk transaktionsvalutaen. Beløb i regnskabs- og rapporteringsvalutaen genereres som en del af regnskab for reskontro.
    -   Fordelingerne viser regnskabsdatoen og regnskabshændelse. Regnskabshændelsen er typisk indstillet til **Ingen**, indtil dokumentet er bogført/journaliseret. På dette tidspunkt bliver regnskabshændelsen **Oprindelig**. Når fordelingerne er bogført, kan du ikke redigere fordelingerne.
    -   **Opdel**-knappen kan være aktiveret for overordnede fordelinger. **Opdel** genererer nye regnskabsfordelinger, og opdelingen kan være baseret på procentdel, beløb eller antal.
    -   Knappen ** Fordel ligeligt** kan bruges i kombination med **Opdel** for automatisk at fordele beløbet ligeligt på tværs af alle fordelinger.
    -   Knappen **Nulstil** kan aktiveres for overordnede fordelinger, når der findes mere end én fordeling. **Nulstil** vender manuel ændring af fordelingen ved at slette alle eksisterende fordelinger og oprette standardfordelingerne igen.
    -   Alle underordnede fordelinger, f.eks. rabat, gebyr og moms, følger altid den overordnede fordeling. Du kan se overordnet/underordnet-relation til **Reference**&gt;**overordnede oplysninger**.
    -   Hovedkontoen og den økonomiske dimension kan også være redigerbar for børn.
    -   De økonomiske dimensioner på regnskabsfordelinger følger et standardmønster, som dokument kan udvide. Yderligere oplysninger finder du under relaterede artikler.
    -   Afvigelsesfordelinger kan genereres i matchende situationer, f.eks. som en matching mellem en kreditorfaktura og en købsordre. Du kan få vist de tilsvarende forbindelser mellem regnskabsfordelingen på **Reference**&gt;**dokumentoplysninger**.
    -   **Korrekt**-knappen vises og er aktiveret for dokumenter, der understøtter rettelser. **Korrekte** opretter nye fordelinger. Fordelinger der først skal oprettes, som tilbagefører de oprindelige fordelinger. Disse distributioner kan ikke ændres. Næste, nye korrekte regnskabsfordelinger oprettes. Disse fordelinger kan ændres, hvis de oprindelige fordelinger kunne ændres.
    -   Knappen ** projektoplysninger** er aktiveret som en udvidelse, når en linje er knyttet til et projekt. Projektregnskabsfordelinger giver dig mulighed for at redigere detaljer som finansieringskilde og linjeegenskab.
    -   Du kan få vist den aktuelle status til regnskab i **Reference**. Status er i hele dokumentet, og angiver, om dokumentet er i gang eller afsluttet.
-   ** Se fordelinger ** – få vist regnskabsfordelinger for alle linjer og pengemæssige beløb på dokumentet. Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.


Yderligere oplysninger finder du [regnskabsfordelinger og kladdeposteringer for reskontro til fri tekst fakturaer](accounting-distributions-subledger-journal-entries-vendor-invoices.md).

