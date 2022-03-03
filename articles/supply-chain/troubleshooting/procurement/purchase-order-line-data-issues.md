---
title: Uoverensstemmelser i indkøbsordrelinjedata
description: Du kan se datauoverensstemmelser eller fejl i data på indkøbsordrelinjerne.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100798"
---
# <a name="purchase-order-line-data-discrepancies"></a>Uoverensstemmelser i indkøbsordrelinjedata

## <a name="symptoms"></a>Symptomer

Når du inspicerer linjerne i en indkøbsordre, bemærker du en eller flere af følgende problemer:

- Der er en uoverensstemmelse eller fejl i indkøbsordrelinjens rest (levering eller faktura).
- Der er fejl i en indkøbsordrelinje eller overskriftsstatus.
- Du kan ikke fakturere en indkøbsordre, fordi du f.eks. modtager en eller flere af følgende fejlmeddelelser:

    - "Stoppet (fejl): Transaktionen er allerede bogført."
    - "Antallet kan ikke faktureres, fordi lagertransaktioner med statussen Modtaget ikke er tilstrækkelige."
    - "Utilstrækkelige lagertransaktioner med status "Købt" for vare %0 antal %1."

- Du kan ikke færdiggøre eller lukke en indkøbsordre, f.eks. fordi du har en af følgende problemer:

    - Knappen **Færdiggør** er ikke tilgængelig.
    - Du kan ikke annullere det bestilte antal på en indkøbsordrelinje for en indkøbsordre, der er i bekræftet og modtaget tilstand.

## <a name="cause"></a>Årsag

Disse problemer skyldes som regel, at data er blevet beskadiget, eller at de resterende antal er uoverensstemmende for en eller flere indkøbsordrelinjer.

## <a name="resolution"></a>Løsning

Du kan normalt løse disse problemer ved at opdatere indkøbsstatus, restlevering og/eller restfakturaer for de relevante indkøbsordrelinjer som beskrevet i følgende procedure.

1. Gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Ret indkøbsordrelinjer manuelt**.
1. Find og vælg den indkøbsordre, der giver dig problemer, i feltet **Indkøbsordre**.
1. Vælg en linje i sektionen **Indkøbsordrelinjer**, hvor du har fundet en uoverensstemmelse.
1. Kontrollér de data, der vises i sektionen **Lagertransaktioner**. Hvis du bemærker uoverensstemmelser mellem en indkøbsordrelinje og dens lagertransaktioner, skal du vælge en af følgende kommandoer i handlingsruden afhængigt af, hvor du ser uoverensstemmelserne:

    - **Genberegn \> Genberegn leveringsrest** – Opdater automatisk statusserne for indkøbsordrelinje og -hoved. Denne funktion virker kun for indkøbsordrelinjer på lager (det vil sige linjer, hvor varen er en lagervare). Varer, der ikke er på lager, og fastvægtvarer understøttes ikke i øjeblikket.
    - **Genberegn \> Genberegn fakturarest** – Opdater automatisk statusserne for indkøbsordrelinje og -hoved. Denne funktion virker kun for indkøbsordrelinjer på lager (det vil sige linjer, hvor varen er en lagervare). Varer, der ikke er på lager, og fastvægtvarer understøttes ikke i øjeblikket.
    - **Genberegn \> Genberegn status** – Genberegn status for den valgte linje. Denne beregning er baseret på den eksisterende logik. Status for indkøbsordrehovedet opdateres derfor efter behov på grundlag af status for den nye indkøbsordrelinje.

1. Hvis du stadig kan se uoverensstemmelser i restantal, kan du bruge følgende felter til at redigere dem direkte efter behov:

    - Levér rest
    - Restlevering til lager
    - Fakturarestmængde
    - Fakturarest for lager
