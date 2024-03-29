---
title: Finansfordelingsregler
description: Denne artikel indeholder generelle oplysninger om finansfordelingsregler. Den beskriver de forskellige komponenter i disse fordelingsregler og de fordelingsmetoder, som kan bruges til dem.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: kfend
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0691c65e6a499f713952070811cefaa7a213af7b
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787547"
---
# <a name="ledger-allocation-rules"></a>Finansfordelingsregler

[!include [banner](../includes/banner.md)]

Denne artikel indeholder generelle oplysninger om finansfordelingsregler. Den beskriver de forskellige komponenter i disse fordelingsregler og de fordelingsmetoder, som kan bruges til dem.

Finansfordelingsregler bruges til automatisk at beregne og generere fordelingskladder og kontoposter for fordeling af finanssaldi eller faste beløb. Fordelingsmetoderne kan være variable eller faste. Fordelingen er baseret på værdien af transaktionsvalutaen. Regnskabsposter om gevinst/tab i udenlandsk valuta bogføres f.eks. for at regulere beløbene i regnskabs- og rapporteringsvalutaen. Disse poster er ikke underlagt fordelingsregler, da deres transaktionsvalutaværdi er 0,00. Følgende fordelingsmetoder kan bruges til finansfordelingsregler:

-   **Basis** – Denne variable metode bruges, når fordelingen afhænger af den faktiske finanssaldo baseret på filterkriterier. Du kan f.eks. fordele reklameomkostninger baseret på den enkelte afdelings salg i forhold til det samlede afdelingssalg.
-   **Fast procentdel** og **Fast vægt** – For disse metoder defineres fordelingsprocenten eller -vægten direkte for reglen. Reklameudgifter kan f.eks. fordeles, så afdeling A modtager 70 procent af reklameomkostninger, og afdeling B modtager 30 procent.
-   **Ligeligt** – Denne metode fordeler beløbet ligeligt mellem alle de destinationer, der er defineret. Hvis der f.eks. er fastsat bestemmelsessteder for afdeling A og afdeling B, kan reklameudgifter fordeles, så både afdeling A og afdeling B modtager 50 % af reklameudgiften.

Hvis Bases bruges som fordelingsmetoden til en fordelingsregel, skal du også definere separate basisregler for finansfordeling. I processen "Udfør fordelingsanmodning" kan brugerne behandle finansfordelingsreglen og få vist den resulterende fordelingskladde, før de enten bogfører eller sletter de beregnede fordelinger.

## <a name="components-of-ledger-allocation-rules"></a>Komponenter i finansfordelingsregler
Hver fordelingsregel består af fire komponenter: generel, kilde, destination og modregning. Der kræves en ekstra komponent, finansfordelingsbasisregler, hvis Basis bruges som fordelingsmetode. Hver af disse komponenter udgør en central del af de informationer, der skal bruges for at behandle fordelinger.

-   **Generelt** – Denne komponent er det sted, hvor brugeren angiver muligheder, f.eks. fordelingsmetode, indstillinger for regler for intern handel, og om reglen er aktiv eller ej.
-   **Kilde** – Denne komponent er det sted, hvor brugeren angiver kildedataene til fordelingen. Fordelingen kan baseres på finanssaldi (**Datakilde** = **Finans**) eller faste beløb (**Datakilde** = **Faste værdi**). Når **Datakilde** er angivet til **Finans**, skal der være defineret filterkriterier for finansfordelingsregel (f.eks. til reklameudgifter).
-   **Destination** – Denne komponent definerer, hvordan resultatet af fordelingsberegningen skal distribueres og gøres rede for. Der kan f.eks. være én destinationslinje for hver afdeling.
-   **Modregn** – Denne komponent definerer, hvordan hovedkonti og dimensioner skal bestemmes for de forskudte poster, som er afstemt på destinationsposterne. Brugerdefinerede indstillinger anvendes typisk i stedet for de konti og dimensioner, der er baseret på kilden. Når **Datakilde** er angivet til **Faste værdier**, kan **Kilde** ikke bruges som en indstilling.
-   **Finansfordelingsbasisregler** – Disse regler anvender deres filterkriterier til at bestemme, hvilke finanssaldi der skal bruges til fordeling (f.eks. omsætning pr. afdeling). De enkelte fordelingsbasisregler kan bruges til flere fordelingsregler.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
