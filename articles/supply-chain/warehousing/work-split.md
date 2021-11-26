---
title: Arbejdsopdeling
description: Dette emne indeholder oplysninger om arbejdsopdelingsfunktionen. Med denne funktionalitet kan du opdele store arbejdsordrer i flere mindre arbejdsordrer, som du derefter kan tildele til flere lagermedarbejdere. På denne måde kan det samme arbejde plukkes samtidig af flere lagermedarbejdere.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8b06164a81a18548cf9d98ea2f577b5783145100
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778251"
---
# <a name="work-split"></a>Arbejdsopdeling

[!include [banner](../includes/banner.md)]

Med arbejdsopdelingsfunktionen kan du opdele store arbejds-id'er (dvs. arbejdsordrer med flere linjer) i flere mindre arbejds-id'er, som du derefter kan tildele til flere lagermedarbejdere. På denne måde kan det samme arbejdsnummer plukkes samtidig af flere lagermedarbejdere.

> [!IMPORTANT]
> Du kan kun opdele arbejdsordrer, der har statussen *Åben* eller *Igangværende*.

## <a name="turn-on-the-work-split-functionality"></a>Aktivere funktionen til opdeling af arbejde

Før du kan bruge funktionen til opdeling af arbejde, skal du aktivere funktionen og dens forudsætning i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.

Først skal du aktivere den forudsætningsfunktionen *Blokering af arbejde i hele organisationen*, hvis den ikke allerede er aktiveret. Fra og med Supply Chain Management version 10.0.21 er denne funktion obligatorisk, så den er som standard aktiveret og kan ikke deaktiveres igen. I [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vises funktionen dog stadig på følgende måde:

- **Modul:** *Warehouse Management*
- **Funktionsnavn:** *Blokering af arbejde i hele organisationen*

> [!NOTE]
> Når denne funktion er aktiveret, anvendes der automatisk en dataopgradering, når funktionen er aktiveret på tværs af alle juridiske enheder.

Derefter skal du aktivere funktionen *Arbejdsopdeling*, som findes på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Arbejdsopdeling*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Forbedringer af arbejdsdetaljerne og alle arbejdssider

Funktionen *Arbejdsopdeling* føjer følgende to knapper til fanen **Arbejde** i handlingsruden på siderne **Arbejdsdetaljer** og **Alt arbejde**:

- **Opdel arbejde** – Opdel det aktuelle arbejds-id i flere mindre arbejds-id'er, der kan behandles af særskilte arbejdere.
- **Annuller arbejdsopdelt session** – Annuller den arbejdsopdelte session, og gør arbejdet tilgængeligt for behandling.

![Knapperne Opdel arbejde og Annuller arbejdsopdelt session.](media/Work_split_buttons.png "Knapperne Opdel arbejde og Annuller arbejdsopdelt session")

> [!IMPORTANT]
> Knappen **Opdel arbejde** er ikke tilgængelig, hvis en eller flere af følgende betingelser er opfyldt:
>
> - Arbejdsstatussen er noget andet end *Åben* eller *Igangværende*.
> - Et container-id er knyttet til arbejds-id'et. (En container kan ikke opdeles systematisk, fordi den kræver fysiske handlinger).
> - Arbejdet er knyttet til en klynge.
> - Arbejdsordretypen er noget andet end en af følgende typer:
>
>    - Salgsordre
>    - Råvarepluk
>    - Flytteafgang
>
> - Arbejdet opdeles i øjeblikket af en anden bruger. Hvis du forsøger at åbne opdelingssiden for arbejde, der allerede er ved at blive opdelt af en anden bruger, får du vist følgende fejlmeddelelse: "Arbejdet med id \#\#\#\# er ved at blive opdelt. Prøv igen om et par minutter. Hvis du fortsætter med at modtage denne meddelelse, skal du kontakte en tilsynsførende".

En ny årsag til arbejdsblokering, *Opdelt arbejde*, angiver, hvornår arbejds-id'et er ved at blive opdelt. Det vises både på siden **Opdel arbejde** og i mobilappen Lokationsstyring, hvis en bruger forsøger at køre arbejdet. Når der bruges blokeringsårsager, ændres navnet på feltet **Blokeret bølge** fra arbejds-id'et til **Blokeret**.

## <a name="initiate-a-work-split"></a>Starte en opdeling af arbejde

Funktionen tilføjer en ny **Opdel arbejde**-side, der giver brugerne mulighed for at opdele arbejdslinjer fra arbejds-id'et. Når siden åbnes første gang, vises linjer, der har statussen *Åben*, og som er tilgængelige for opdeling. Vælg **Opdel arbejde** i handlingsruden at behandle det valgte arbejde.

Hvis du vil opdele arbejdet, skal du følge disse trin.

1. Åbn en af følgende arbejdssider:

    - **Arbejdsdetaljer** (**Lokationsstyring \> Arbejde \> Arbejdsdetaljer**)
    - **Alt arbejde** (**Lokationsstyring \> Arbejde \> Alt arbejde**)

1. Vælg et arbejds-id, der skal opdeles, i gitteret. Feltet **Arbejdsordretype** skal angives til en af følgende værdier:

    - Salgsordre
    - Råvarepluk
    - Flytteafgang

1. Gå til handlingsrunde og vælg **Opdel arbejde** i gruppen **Arbejde** under fanen **Arbejde**.

    Siden **Opdel arbejde** vises med de åbne arbejdslinjer, som er åbne og kan opdeles. Der vises som standard kun tilgængelige arbejdslinjer. Hvis du vil have vist alle linjer for arbejds-id'et (f.eks. linjer med arbejdstypen *Læg på lager*), skal du markere afkrydsningsfeltet **Vis alle linjer** over gitteret.

    Følgende meddelelse vises: "Brugere kan ikke behandle linjer i arbejdet, før du er færdig med at opdele og lukke denne side".

    Feltet **Årsag til blokering af arbejde** for det aktuelle arbejde vil blive indstillet til *Opdelt arbejde*, og arbejdet vil blive blokeret.

    ![Blokeringsårsag.](media/Blocking_reason.png "Blokeringsårsag")

1. Vælg de linjer, der skal fjernes fra det aktuelle arbejds-id, og føj dem til et nyt arbejds-id. Følgende hændelser forekommer:

    - Når du opdeler arbejdet, annulleres den eller de valgte linjer fra det oprindelige arbejds-id og kopieres derefter til et nyt arbejds-id.
    - Strukturen for den eksisterende arbejdsskabelon og lokationen for læg på lager (og også fremtidige pluk/læg på lager-par) bevares. Værdierne for følgende arbejds-id-felter kopieres fra det oprindelige arbejde til det nye arbejde:

        - Last-id
        - Forsendelses-id
        - Arbejdsordretype
        - Ordrenummer
        - Lokation
        - Lagersted
        - Arbejdsprioritet
        - Arbejdspulje-id
        - Bølge-id
        - Nummer på arbejdsoprettelse

    - Følgende felter kopieres ikke til det nye arbejds-id:

        - **Arbejds-id** – Der genereres et nyt arbejds-id fra den relevante nummerserie.
        - **Arbejdsstatus** – Dette felt er angivet til *Åben*.
        - **Låst af** – Dette felt angives er udgangspunkt tomt.
        - **Målnummerplade-id** – Dette felt er tomt.
        - **Dato og klokkeslæt for oprettelse** – Dette felt er angivet til dags dato og det aktuelle klokkeslæt.
        - **Blokeret bølge/fastfrossen** – Dette felt er genberegnet for det oprindelige arbejds-id og det nye arbejds-id.

1. Vælg **Opdel arbejde** i handlingsruden.

Mens arbejdet opdeles, vises følgende meddelelse: "Behandlingsoperation – Opdel arbejde". Når denne meddelelse er synlig, kan du annullere handlingen ved at vælge **Annuller** i meddelelsesboksen.

Hvis afkrydsningsfeltet **Vis alle linjer** ikke er markeret, vises den linje, der er opdelt og annulleret, ikke længere i gitteret. Hvis afkrydsningsfeltet er markeret, bør du kunne se, at værdien i feltet **Arbejdsstatus** for linjen er ændret til *Annulleret*.

Følgende meddelelse vises for at angive, at det nye arbejds-id er oprettet: "Arbejde \#\#\#\# er oprettet ved at opdele fra det oprindelige arbejde \#\#\#\#".

Andre arbejdslinjer fra det oprindelige arbejds-id (f.eks. *Læg på lager*-linjer) vil blive justeret efter behov, så de afspejler de linjer i arbejdet, der er blevet annulleret. Hvis det oprindelige arbejds-id f.eks. havde en *Læg på lager*-linje for et antal på 15, og *Pluk*-linjer, der har et samlet antal på 10 blev annulleret, vil det nye *Læg på lager*-antal på det oprindelige arbejds-id nu være 5.

Det nye arbejde tildeles ikke straks til en bruger. Du kan dog tildele det til en bruger nu, hvis det er nødvendigt, ved hjælp af standardfunktionerne på siden **Arbejdsdetaljer**.

> [!IMPORTANT]
> Du kan kun opdele arbejds-id'er, der indeholder to eller flere tilgængelige arbejdslinjer. Hvis du vælger **Opdel arbejde**, når der kun er én arbejdslinje, får du vist følgende fejlmeddelelse: "Mindst én arbejdslinje skal forblive i det indledende arbejde". Hvis dette er tilfældet, sker der ingen opdeling.

## <a name="finish-a-work-split"></a>Afslutte en opdeling af arbejde

Hvis du vil afslutte opdeling af arbejde, skal blokeringsårsagen *Opdel arbejde* være fjernet. Der er to måder at gøre dette på:

- Den bruger, der opdeler arbejdet, lukker siden **Opdel arbejde** ved at vælge knappen **Luk** (**X**) i øverste højre hjørne. Når siden lukkes, fjernes blokeringsårsagen *Opdel arbejde*. Den *Blokerede* tilstand for dette arbejde vil blive genberegnet, og hvis der ikke er nogen resterende blokeringsårsager for dette arbejde, vil arbejdet blive fjernet.
- Alle brugere åbner arbejds-id'et og vælger knappen **Annuller opdeling af arbejdssession** i handlingsruden. Årsagen til blokeringen af *Opdel arbejde* vil blive fjernet, og *Blokeret*-tilstand for dette arbejde vil blive genberegnet, ligesom når siden **Opdel arbejde** lukkes.

Når blokeringsårsagen *Opdel arbejde* er fjernet, kan arbejdet køres på mobilenheden, hvis den **blokerede** tilstand er angivet til *Nej* på arbejds-id'et.

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a>Brugerblokering på mobilappen Lokationsstyring

Hvis du forsøger at bruge mobilappen Lokationsstyring til at køre plukarbejde på et arbejds-id, der er ved at blive opdelt, får du vist følgende fejlmeddelelse: "Arbejdet med id \#\#\#\# er ved at blive opdelt". Hvis du modtager denne meddelelse, skal du vælge **Annuller**. Du kan derefter fortsætte med at behandle andet arbejde.

## <a name="other-blocked-operations"></a>Andre blokerede handlinger

Handlinger, der redigerer arbejdslinjer, arbejdslagertransaktioner eller genopfyldningslinks, der er relateret til det arbejde, der opdeles, mislykkes, og følgende fejlmeddelelse vises: "Arbejdet med id \#\#\#\# er ved at blive opdelt".


[!INCLUDE[footer-include](../../includes/footer-banner.md)]