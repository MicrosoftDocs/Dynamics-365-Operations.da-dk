---
title: Systembaseret arbejdsrækkefølge
description: Denne artikel giver oplysninger om systembaseret arbejdsrækkefølge. Denne funktionalitet gør det muligt at sortere og filtrere de arbejdsordrer, som systemet fremsender til brugere til afvikling. Det er nyttigt i situationer, hvor der kræves yderligere kriterier for at drive plukprocessen på lagerstedet.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 1dab8d8bdace046f0f061713600fd1eab69e7c12
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335459"
---
# <a name="system-directed-work-sequencing"></a>Systembaseret arbejdsrækkefølge

[!include [banner](../includes/banner.md)]

Systembaseret arbejdsrækkefølge gør det muligt at sortere og filtrere de arbejdsordrer, som systemet fremsender til brugere til afvikling. Det er nyttigt i situationer, hvor yderligere kriterier (f. eks. leveringstiden, plukzonen, lokationsprofilen eller en kombination af forskellige kriterier) er nødvendige for at drive lagerstedets plukproces.

Denne funktion udvider den aktuelle systembaserede plukfunktionalitet ved at tilføje en systembaseret forespørgselsrækkefølge, hvor brugerne kan angive en sekvens og en eller flere forespørgsler, der evaluerer alle de oprettede arbejdsordrer. Det er kun de arbejdsordrer, der opfylder de kriterier, der er angivet i opsætningen af menupunktet i mobilenheden, der registreres og vises.

Denne funktionalitet giver dig derfor mulighed for yderligere optimering af lagerplukprocesser, da den identificerer arbejdsordrer, der opfylder de angivne kriterier, tildeler dem til det korrekte menupunkt i den mobile enhed og viser dem derefter for en arbejder, baseret på et bestemt kompetencesæt, plukudstyr eller et andet krav.

> [!NOTE]
> Hvis der er brug for andre kriterier, skal der bruges flere menupunkter i mobilenheder.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Aktivér funktionen Systembaseret arbejdsrækkefølge for hele virksomheden

Før du kan bruge funktionen Systembaseret arbejdsrækkefølge, skal den være aktiveret for dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Systembaseret arbejdsrækkefølge for hele virksomheden*

## <a name="setup"></a>Konfiguration

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil arbejde gennem scenariet ved hjælp af de værdier, der vises i denne artikel, skal du arbejde på et system, hvor [standarddemodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**. I scenariet bruges lagersted *51* fra demodata.

> [!IMPORTANT]
> Før du frigiver ordrerne til lageret, skal du sørge for, at pluklokationerne har tilstrækkelig lagerbeholdning af alle varerne på ordrerne.
>
> Standard-USMF-data skal understøtte dette scenarie. Hvis du ikke bruger demodata, skal du gennemse indstillingen **Lokationsvejledning** for at finde ud af, hvilke pluklokationer der skal bruges til salgsordrepluk. Hvis du skal justere lagerbeholdning, kan du oprette manuelle bevægelser, bruge genopfyldning eller anvende en anden proces.

### <a name="set-up-a-mobile-device-menu-item"></a>Opsætning af et mobilenhedsmenupunkt

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Salgspluk – system** på listen over mobilenhedsmenupunkter. Det påkrævede menupunkt skal findes i forvejen. 
1. Bekræft følgende indstillinger:

    - I oversigtspanelet **Generelt** skal feltet **Styret af** indstilles til *Systembaseret*.
    - I oversigtspanelet **Arbejdsklasser** vises følgende indstillinger.

        | Arbejdsklasse-id | Arbejdsordretype |
        |---|---|
        | Sales | Salgsordre |
        | Salgsordrepluk | Salgsordre |

1. Vælg **Systembaserede arbejdssekvensforespørgsler** i handlingsruden.
1. Vælg **Rediger**.
1. Slet den eksisterende linje, og bekræft derefter handlingen ved at vælge **Ja**.
1. Vælg **Ny** i handlingsruden for at oprette en linje.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** *1*
    - **Beskrivelsesfelt:** *Arbejdsantal mindre end 20 og faldende*

1. Vælg **Gem**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Under fanen **Joinforbindelser** skal du udvide join-hierarkiet for at få vist tabellen **Arbejdslinjer**.
1. Vælg tabeljoinet **Arbejdslinjer**.
1. Vælg **Tilføj tabeljoin**.
1. Find og vælg den række, der har følgende indstillinger, på den liste, der vises:

    - **Join-tilstand:** *n:1*
    - **Relation:** *Lokationer (lokation)*

1. Vælg **Vælg**.

    Lokationer føjes til tabeljoinet.

1. På fanen **Sortering** skal du vælge **Tilføj** for at tilføje en ny linje.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdsantal* (i den viste meddelelsesboks skal du vælge **Ja** for at føje sortering til dette felt).
    - **Søgeretning:** *Faldende*

1. Vælg fanen **Område**.

    Hvis der kun skal medtages bestemte arbejdskriterier i rækkefølgen, kan du angive dem under fanen **Område**. I dette eksempel vil du kun medtage det arbejde, hvor antallet er mindre end 20 ea (den laveste måleenhed).

    Bemærk, at der allerede er inkluderet nogle linjer. Disse linjer skal ikke fjernes.

1. Vælg **Tilføj** for at tilføje en linje.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdsantal for lager*
    - **Kriterier:** *\<20* (mindre end 20)

1. Vælg **Tilføj** for at tilføje en anden linje.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdstype*
    - **Kriterier:** *Pluk*

1. Vælg **Tilføj** for at tilføje en anden linje.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Lokationsprofil-id*
    - **Kriterier:** *!STADIE*

        > [!IMPORTANT]
        > Sørg for at medtage udråbstegnet (*!*) foran *STADIE*.

1. Vælg **OK** for at gemme og lukke forespørgslen.
1. Vælg **Gem**.
1. Luk siden for at vende tilbage til siden **Mobilenhedsmenupunkter**.

> [!NOTE]
> Denne opsætning definerer de kriterier, der skal bruges til at føde det kvalificerede arbejde til mobilenhedsmenupunktet. Hvis du føjer flere kriterielinjer til forespørgslen, vil systemet bruge den forespørgselslinje, der har det laveste løbenummer først. Med andre ord vises alt det kvalificerede arbejde for løbenummer 1 for brugeren først og derefter alt arbejde for løbenummer 2. Hvis et bestemt område og sortering skal bruges sammen, skal de derfor angives i den samme systembaserede arbejdssekvensforespørgsel.
>
> Denne opsætning vil hente alle de ressourcer, der har mindst én linje, hvor antallet er mindre end 20 ea. Hvis arbejdet har en linje, hvor antallet er nøjagtigt 20 ea eller mere end 20 ea, vil det derfor være gyldigt, hvis der også er mindst én linje, hvor antallet er mindre end 20 ea.

### <a name="location-directives"></a>Lokationsvejledninger

Hvis du bruger standarddata fra Contoso, kræver forespørgslen til handling i lokationsvejledning ikke ændringer. Hvis du vil være sikker på, at lokationsvejledninger registrerer varerne på salgsordrerne, når du anvender funktionen i et miljø, der ikke er Contoso, skal du oprette en ny lokalitetsvejledning. Udfør følgende trin for at kontrollere indstillingerne i demomiljøet.

1. Gå til **Lagerstedsstyring** \> **Opsætning** \> **Lokationsvejledninger**.
1. I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.
1. Vælg lokationsvejledningen med navnet *51 Pluk*.
1. Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg linjen for handlingen **Pluk**.
1. Vælg **Rediger forespørgsel** over gitteret.
1. Gennemgå forespørgslen **Område**.

    1. Find den linje, hvor feltet **Felt** er angivet til *Lokation*.
    2. Kontroller, at feltet **Afgrænsning** er tomt (dvs. der er ingen begrænsninger).

## <a name="scenario"></a>Scenario

### <a name="create-sales-order-picking-work"></a>Oprette arbejde med salgsordrepluk

Inden der køres systembaseret plukning, skal der oprettes noget udgående arbejde. I dette scenarie opretter du fire salgsordrer, der er baseret på de angivne systembaserede arbejdssekvensforespørgsler.

Du kan reservere lagerantal for hver salgsordre. Det reserverede lager kan derfor ikke trækkes fra lagerstedet i forbindelse med andre ordrer, medmindre lagerreservationen eller en del af lagerreservationen annulleres.

Du skal derefter frigive hver salgsordre til lagerstedet for at oprette det udgående arbejde.

#### <a name="sales-order-1"></a>Salgsordre 1

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** i handlingsruden for at oprette en salgsordre 1.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til sektionen **Kunde**, indstil feltet **Debitorkonto** til *US-004*.
    - I sektionen **Generelt** skal du indstille **Lagersted** til *51*.

1. Vælg **OK** for at lukke dialogboksen. Notér dig salgsordrenummeret.
1. Føj en linje til den nye salgsordre, og angiv følgende værdier:

    - **Varenummer:** *M9200*
    - **Antal:** *20*

1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere lageret.
1. Luk siden **Reservation**.
1. I handlingsruden skal du på fanen **Lagersted** vælge **Frigiv til lagersted** for at oprette lagerstedet.

    Du modtager orienterende meddelelser, der viser bølge-id'et og forsendelses-id'et, der blev oprettet for salgsordren.

#### <a name="sales-order-2"></a>Salgsordre 2

1. Vælg **Ny** i handlingsruden for at oprette en salgsordre 2.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-007*
    - **Lagersted:** *51*

1. Vælg **OK** for at lukke dialogboksen. Notér dig salgsordrenummeret.
1. Føj en linje til den nye salgsordre, og angiv følgende værdier:

    - **Varenummer:** *M9200*
    - **Antal:** *5*

1. Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:

    - **Varenummer:** *M9201*
    - **Antal:** *1*

1. Reservér lager for begge linjer.
1. Frigive ordren til lagerstedet.

#### <a name="sales-order-3"></a>Salgsordre 3

1. Vælg **Ny** i handlingsruden for at oprette en salgsordre 3.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-009*
    - **Lagersted:** *51*

1. Vælg **OK** for at lukke dialogboksen. Notér dig salgsordrenummeret.
1. Føj en linje til den nye salgsordre, og angiv følgende værdier:

    - **Varenummer:** *M9200*
    - **Antal:** *7*

1. Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:

    - **Varenummer:** *M9202*
    - **Antal:** *8*

1. Reservér lager for begge linjer.
1. Frigive ordren til lagerstedet.

#### <a name="sales-order-4"></a>Salgsordre 4

1. Vælg **Ny** i handlingsruden for at oprette en salgsordre 4.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-010*
    - **Lagersted:** *51*

1. Vælg **OK** for at lukke dialogboksen. Notér dig salgsordrenummeret.
1. Føj en linje til den nye salgsordre, og angiv følgende værdier:

    - **Varenummer:** *M9200*
    - **Antal:** *25*

1. Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:

    - **Varenummer:** *M9202*
    - **Antal:** *10*

1. Reservér lager for begge linjer.
1. Frigive ordren til lagerstedet.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Hent arbejds-id'er for det arbejde, der er oprettet

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Filtrer på feltet **Lagersted**, så der kun vises arbejde for lagersted *51*.
1. Der skal være oprettet fire arbejds-id'er. Noter arbejds-id'et for hver salgsordre.

    | Salgsordre-id | Arbejds-id | Arbejdsantal |
    |---|---|---|
    | Salgsordre 1 | Arbejds-id 1 | 20 ea |
    | Salgsordre 2 | Arbejds-id 2 | 6 ea (summen af begge linjer) |
    | Salgsordre 3 | Arbejds-id 3 | 15 ea (summen af begge linjer) |
    | Salgsordre 4 | Arbejds-id 4 | 35 ea (summen af begge linjer) |

Før du kører processen på mobilenheden, skal du sørge for, at kun det arbejde, du netop har oprettet, har statussen *Åben* for lagersted *51* og arbejdsordretypen *Salgsordre*. Ellers kan testresultaterne variere, fordi systembaseret plukning vil omfatte alt berettiget arbejde.

1. Gå til **Lokationsstyring \> Arbejde \> Udgående \> Åbent salgsarbejde**.
1. Gå til gitteret **Åbent salgsarbejde**, filtrer efter feltet **Lagersted**, så kun arbejde for lagersted *51* vises.
1. Bekræft, at det kun er de fire arbejds-id'er, du har oprettet tidligere, der vises.
1. Luk siden **Arbejde**.

### <a name="mobile-device-flow-execution"></a>Udførelse af mobilenhedsproces

På basis af opsætningen føder systemet brugeren arbejde, der er sorteret fra det højeste linjeantal til det laveste. Antallet på hver linje vil være mindre end 20 ea.

Husk, at denne opsætning vil hente alle de ressourcer, der har mindst én linje, hvor antallet er mindre end 20 ea. Hvis arbejdet derfor har en anden linje, hvor antallet er nøjagtigt 20 ea. eller mere end 20 ea., vil det også være gyldigt.

#### <a name="mobile-app"></a>Mobilapp

1. Log på lagerstedsappen som en bruger på lagersted *51*.
1. Gå til **Udgående \> Salgsplukning – System**.

    Pluktrinnet for arbejds-id *4* vises. Dette arbejds-id vises først på grund af opsætningen af den systembaserede forespørgselsrækkefølge, hvor du angav, at arbejdet skal sorteres baseret på faldende linjeantal i arbejdet.

1. Afslut den krævede plukning, og læg den på lager for at lukke arbejds-id'et.

    Derefter vises arbejds-id *3*. En af dens arbejdslinjer er den næste i rækkefølgen baseret på linjeantallet i arbejdet.

1. Afslut plukningen, og læg den på lager for at lukke arbejds-id'et.

    Derefter vises arbejds-id *2*. Dette arbejdes pluklinje er den næste i rækkefølgen.

1. Afslut plukningen, og læg den på lager for at lukke arbejds-id'et.

    Der bør ikke vises yderligere arbejde for dig. Arbejds-id *1* er ikke gyldigt for dette mobilenhedsmenupunkt, fordi forespørgslen angiver, at arbejdsoverskrifter kun tages i betragtning, hvis antallet på arbejdslinjerne er mindre end 20 ea.

## <a name="tips"></a>Tip!

De systembaserede arbejdsrækkefølgeforespørgsler er *inklusive*. Det er vigtigt, at du husker dette i forbindelse med nogle af opsætningerne. Du ønsker f. eks., at et bestemt menupunkt kun skal behandle arbejde, hvor arbejdsenheden er *ea*, og du angiver denne begrænsning under fanen **Område** i forespørgslen. I dette tilfælde vil alle de opgaver, hvor mindst én arbejdslinje har arbejdsenheden indstillet til *ea*, blive overført til arbejderen. Dette arbejde kan derfor også omfatte arbejde, hvor arbejdslinjer har en anden arbejdsenhed end *ea* (f.eks. *kasse* eller *palle*). Forespørgslen udelader kun det arbejde, hvor ingen linjer for arbejdslinjen er angivet til *ea*.

I eksemplet med dette scenarie blev arbejds-id *4* derfor også hentet af forespørgslen. Da den blev oprettet, blev der tilføjet to linjer: en til 25 ea og en anden til 10 ea. Arbejdet blev stadig vist for brugeren, fordi mindst én arbejdslinje har et antal på mindre end 20 ea.

Afhængigt af scenariet kan du forhindre dette ved at bruge arbejdspauser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]