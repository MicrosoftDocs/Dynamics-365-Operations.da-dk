---
title: Skift arbejdspulje på arbejde
description: I dette emne forklares det, hvordan du kan bruge knappen Skift arbejdspulje for arbejdselementer til at ændre arbejdspuljen for eksisterende arbejde.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 513d74af52c9b3581827b653d58c95d7d1f2f78a75bea03296495fed0ea85de7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771125"
---
# <a name="change-work-pool-on-work"></a>Skift arbejdspulje på arbejde

[!include [banner](../includes/banner.md)]

Du kan bruge arbejdspuljer til at organisere arbejde i grupper. Du kan f.eks. oprette en arbejdsgruppe til at klassificere arbejde, der opstår på et bestemt lagersted.

Funktionen *Skift arbejdspulje på arbejde* tilføjer knappen **Skift arbejdspulje** i handlingsruden for arbejdselementer. Lagercheferne kan derfor nemt ændre arbejdspuljen for eksisterende arbejde. Denne funktion giver cheferne mulighed for hurtigt at reagere på ændringer i lagerstedets produktion, og det er med til at forbedre deres evne til at tilpasse sig skiftende situationer og behovet for at overføre arbejde til en anden arbejdsgruppe.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Aktivere funktionen Skift arbejdspulje på arbejde

Før du begynder at konfigurere eller bruge denne funktion, skal du sørge for, at den er tilgængelig i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Skift arbejdspulje på arbejde*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Konfigurere funktionen Skift arbejdspulje på arbejde

Hvis du vil bruge denne funktion, skal der være konfigureret nogle arbejdspuljer. Du kan også oprette arbejdsskabeloner, så de automatisk tildeler en pulje. Hvis du vil arbejde i det eksempelscenarie, der er angivet senere i dette emne, skal du konfigurere systemet som beskrevet i dette afsnit.

### <a name="set-up-work-pools"></a>Konfigurere arbejdspuljer

Med arbejdspuljer kan du organisere arbejdselementer efter type. Hvis du vil arbejde med funktionen *Skift arbejdspulje på arbejde*, skal du have mindst to tilgængelige arbejdspuljer. Benyt følgende fremgangsmåde for at få vist og tilføje arbejdspuljer.

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdspuljer**.
1. Hvis du arbejder med demonstrationsdata fra **USMF**-firmaet og gerne vil arbejde dig gennem eksempelscenariet senere i dette emne, skal du tilføje to arbejdspulje, der skal have følgende indstillinger:

    - Arbejdspulje 1:

        - **Arbejdspulje-id:** *Webbutik*
        - **Beskrivelse:** *Webbutik*

    - Arbejdspulje 2:

        - **Arbejdspulje-id:** *Callcenter*
        - **Beskrivelse:** *Callcenter*

1. Vælg **Gem** i handlingsruden.

### <a name="set-up-work-templates"></a>Konfigurer arbejdsskabeloner

For hver af dine arbejdsskabeloner kan du angive en standardarbejdspulje, som du har brug for. For hver relevant skabelon kan du tildele en arbejdspulje i kolonnen **Arbejdspulje-id**. I dette tilfælde arver alle de arbejdselementer, der genereres ved hjælp af en bestemt skabelon, automatisk den tildelte arbejdspulje. Hvis du arbejder med demonstrationsdataene fra **USMF**-firmaet og gerne vil arbejde dig gennem eksempelscenariet senere i dette emne, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Vælg **Rediger** i handlingsruden for at sætte siden i redigeringstilstand.
1. Rediger skabelonen ved at angive følgende værdier:

    - **Arbejdsskabelon:** *62 Pluk til pakke*
    - **Arbejdspulje-id:** *Webbutik*

1. Vælg **Gem**.

## <a name="example-scenario"></a>Eksempelscenario

Dette scenarie viser, hvordan du kan ændre behandlingsstrømmen for et eksisterende arbejdselement ved at ændre dets arbejdspulje. Det bruger demodata fra **USMF**-firmaet og de indstillinger, der blev foreslået tidligere i dette emne.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Oprette en salgsordre og frigive den til lagerstedet

1. Bekræft, at der er en tilstrækkelig disponibel lagerbeholdning for varerne *A0001* og *A0002* på lagerstedet *62*. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**, og rediger de filtre, der vises her:

    - Værdien **Lager** begynder med *62*.
    - Værdien **Varenummer** er enten *A001* eller *A002*.

    Demodata skal have et antal på 10 pr. stk.

    Derefter skal du oprette en salgsordre.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-007*
    - **Lagersted:** *62*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *2*

1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
1. Luk siden.
1. Gå til oversigtspanelet **Salgsordrelinjer**, vælg **Tilføj linje** for at føje en anden linje til din salgsordre. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0002*
    - **Antal:** *2*

1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
1. Luk siden.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.
1. Du modtager orienterende meddelelser, der viser bølge-id'et og forsendelses-id'et, der blev oprettet fra frigivelsen. Notér dig bølge-id'et.

### <a name="review-the-outbound-wave"></a>Gennemse den udgående bølge

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Søg efter det bølge-id, der er oprettet ud fra frigivelsen af salgsordren, i gitteret.
1. Vælg bølge-id'et for at få vist detaljerne.
1. Gå til oversigtspanelet **Bølgelinjer**, og sørg for, at forsendelses-id'et vises for salgsordren.

    > [!TIP]
    > Hvis indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** er angivet til *Nej* i opsætningen af forsendelsesbølgeskabelonen, skal du behandle bølgen manuelt ved at vælge **Behandl** under fanen **Bølge** i handlingsruden for at oprette arbejde.

1. Kontrollér, at bølgen er blevet behandlet. Denne behandling opretter det nødvendige arbejde.

### <a name="view-work-details-and-change-the-work-pool"></a>Få vist oplysninger om arbejde og ændre arbejdspuljen

Du kan bruge siden **Arbejdsdetaljer** til at få vist det arbejde, der er oprettet, og til at administrere arbejdspuljen.

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Vælg rækken for det arbejde, der netop er oprettet. Kolonnen **Ordrenummer** viser nummeret på salgsordren.

    Feltet **Arbejdspulje-id** indstilles til det arbejdspulje-id, der blev konfigureret i arbejdsskabelonen.

    > [!TIP]
    > Hvis du ikke kan se feltet **Arbejdspulje-id**, skal du føje kolonnen til gitteret og derefter opdatere siden.

1. Hvis du vil ændre den arbejdspulje, der er knyttet til arbejds-id'et, skal du vælge **Skift arbejdspulje-id** under fanen **Arbejde** i handlingsruden.
1. Gå til dialogboksen **Skift arbejdspulje**, og vælg **Callcenter** i feltet **Arbejdspulje-id** i oversigtspanelet *Parametre*.
1. Vælg **OK** for at anvende ændringen.
1. Bemærk, at værdien i feltet **Arbejdspulje-id** er nu ændret til *Callcenter*.

> [!IMPORTANT]
> Når dialogboksen **Skift arbejdspulje** vises, kan feltet **Arbejdspulje-id** være tomt som standard. Hvis feltet er tomt, når du vælger **OK** for at anvende ændringer, skal du fjerne arbejdspuljen helt fra arbejdet.
>
> Ud over at skifte arbejdspulje kan du bruge denne procedure til at føje en arbejdsgruppe til en arbejdsgang, der ikke har en, eller til at fjerne en arbejdspulje fra et arbejdselement, der har en.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]