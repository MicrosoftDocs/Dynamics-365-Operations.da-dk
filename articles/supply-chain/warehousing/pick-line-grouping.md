---
title: Pluklinjegruppering
description: Dette emne indeholder en oversigt over pluklinjegruppering.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 076a4dfdc49525eef616d1008073371be1dd4a248cd6f16d395b544ae70e7531
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757488"
---
# <a name="pick-line-grouping"></a>Pluklinjegruppering

[!include [banner](../includes/banner.md)]

Med pluklinjegruppering kan flere arbejdslinjer, der har samme vare og lokation, kombineres til et enkelt pluk, der præsenteres for brugeren på mobilenheden. Derfor kan lagermedarbejderne modtage de mest mulige effektive instruktioner, men den påkrævede adskillelse af linjer (f.eks. for forskellige containere og ordrer) kan stadig bibeholdes i systemet.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Aktivere funktionen pluklinjegruppering

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Pluklinjegruppering*

## <a name="set-up-pick-line-grouping"></a>Opsætning af pluklinjegruppering

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Navn for menupunkt** indtastes *Salgsgruppelinjeplukning*.
1. I feltet **Titel** indtastes *Salgsgruppelinjeplukning*. Denne titel vises i menuen på mobilenheden.
1. Vælg **Arbejde** i feltet *Tilstand*.
1. Angiv indstillingen **Brug eksisterende arbejde** til *Ja*.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - I feltet **Styret af** skal du vælge *Brugerstyret*.
    - Angiv indstillingen **Generer nummerplade** til *Ja*.
    - Angiv indstillingen **Gruppepluk** til *Ja*.
    - Acceptér standardværdierne for alle de andre indstillinger.

1. Følg disse trin for at konfigurere de gyldige arbejdsklasser for menupunktet mobilenhed:

    1. I oversigtspanelet **Arbejdsklasser** skal du vælge **Ny**.
    2. I feltet **Arbejdsklasse-id** skal du vælge enten *Salg* eller *Salgsordrepluk*, afhængigt af det lagersted, du vil bruge. Vælg *Salgsordrepluk* for dette scenario.

        Feltet **Arbejdsordretype** er automatisk angivet til *Salgsordrer*.

### <a name="set-up-a-mobile-device-menu"></a>Opsætning af en mobilenhedsmenu

Følg disse trin for at føje det menupunkt, du lige har oprettet, til menuen **Udgående**.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Rediger** i handlingsruden.
1. I listeruden vises alle eksisterende menuer for mobilenheder. Vælg *Udgående* på listen.
1. På listen **Tilgængelige menuer og menupunkter** skal du finde og vælge menupunktet *Salgsgruppelinjeplukning*, du har oprettet.
1. Vælg den højre pileknap for at flytte menupunktet *Salgsgruppelinjeplukning* til listen **Menustruktur**.
1. Brug knapperne Pil op og Pil ned til at flytte menupunktet til den ønskede placering i menustrukturen.
1. Vælg **Gem** i handlingsruden.

### <a name="set-up-a-work-template"></a>Opsætning af en arbejdsskabelon

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.
1. Find og vælg den arbejdsskabelon, der skal bruges sammen med denne funktion, i gitteret **Oversigt**. I dette scenario skal du vælge skabelonen *51 Pluk til midlertidigt lager*.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditoren skal du på fanen **Sortering** vælge **Tilføj** og derefter indstille følgende værdier for den nye række:

    - Vælg *Midlertidige arbejdstransaktioner* i kolonnen **Tabel**.
    - Vælg *Midlertidige arbejdstransaktioner* i kolonnen **Afledt tabel**.
    - I kolonnen **Felt** skal du vælge *Varenummer*.
    - I kolonnen **Søgeretning** skal du vælge *Stigende*.

1. Vælg **OK** for at lukke dialogboksen gemme dine valg.
1. Du får vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?" Vælg **Ja** for at fortsætte.

> [!IMPORTANT]
> Hvis funktionen pluklinjegruppering skal fungere, skal arbejdslinjerne sorteres efter vare-ID. Hvis de linjer, der har de samme elementer, ikke sorteres en efter en, grupperes de ikke.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opret plukarbejde

Før du kan konfigurere pluklinjegruppering, skal du oprette noget kvalificeret udgående arbejde.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Vælg **US-004** i feltet *Debitorkonto*.
1. I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge *51*.
1. Vælg **OK**.
1. Tilføj følgende seks linjer på oversigtspanelet **Salgsordrelinjer**:

    - **Linje 1:** I feltet **Varenummer** skal du vælge *M9200*. Angiv **3** i feltet *Antal*.
    - **Linje 2:** I feltet **Varenummer** skal du vælge *M9201*. Angiv **3** i feltet *Antal*.
    - **Linje 3:** I feltet **Varenummer** skal du vælge *M9202*. Angiv **2** i feltet *Antal*.
    - **Linje 4:** I feltet **Varenummer** skal du vælge *M9200*. Angiv **1** i feltet *Antal*.
    - **Linje 5:** I feltet **Varenummer** skal du vælge *M9200*. Angiv **3** i feltet *Antal*.
    - **Linje 6:** I feltet **Varenummer** skal du vælge *M9202*. Angiv **7** i feltet *Antal*.

    Her er en oversigt over de samlede mængder af hver vare:

    - **Vare M9200:** *7* hver
    - **Vare M9201:** *3* hver
    - **Vare M9202:** *9* hver

1. Før du frigiver ordrerne til lageret, skal du sørge for, at plukstederne har tilstrækkelig lagerbeholdning af alle varerne på alle ordrerne. Gennemse indstillingen **Lokationsvejledning** for at bestemme, hvilke pluksteder der skal bruges til salgsordrepluk. Hvis du bruger miljøet med demodata til Contoso for lagersted *51*, skal du bekræfte, at der er et tilgængeligt lager.

    Du skal nu reservere lageret for hver linje.

1. Vælg en af de linjer, der skal reserveres, på oversigtspanelet **Salgsordrelinjer**.
1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at anvende reservationen. Luk derefter siden.
1. Gentag trin 8 til 10 for de øvrige linjer, der skal reserveres.

    Du skal nu frigive salgsordren til lagerstedet.

1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Du modtager en meddelelse, der viser, at der er oprettet en forsendelse og en bølge, og at bølgen er sendt til kørsel i en batch.

    Når bølgen og alle downstreamjob er fuldført, oprettes der et arbejds-id for arbejde med seks linjer. Linjerne sorteres efter varenummer.

1. Gå til **Lokationsstyring \> Arbejde \> Alt arbejde** for at få vist det oprettede arbejde. Notér værdien i **Arbejds-id**, da du får brug for det i næste procedure.

### <a name="initiate-picking-from-the-mobile-device"></a>Starte plukning fra mobilenheden

1. Log på mobilenheden som en bruger, der er konfigureret til lagersted *51*.
1. På mobilenheden skal du vælge den menu, der indeholder det nye mobilenhedsmenupunkt. Vælg **Udgående** for dette scenario.
1. Vælg menupunktet **Salgsgruppelinjeplukning** for at påbegynde plukningen.
1. Angiv den værdi i **Arbejds-id**, som du noterede i den forrige procedure.

    Du burde nu se et pluktrin, hvor alle pluklinjer for vare *M9200* er grupperet, og modtage en vejledning om at plukke *7* af hver vare *M9200*.

    > [!IMPORTANT]
    > På mobilenheden er plukarbejdet for de tre plukarbejdslinjer samlet i ét pluktrin for brugeren.

1. Bekræft plukningstrinnet.
1. Gå til arbejdssiden for arbejds-id'et, og læg mærke til, at alle tre pluklinjer for vare *M9200* blev lukket samtidigt.
1. Gå tilbage til mobilenheden, og fortsæt med at plukke. Arbejdslinje 4 for vare *M9201* burde vises. Da der kun var én arbejdslinje i ordren, er der intet, der skal samles.
1. Bekræft plukningstrinnet.
1. Det sidste plukningstrin på mobilenheden aggregerer de sidste to pluklinjer fra arbejdsordren.
1. Fuldfør pluktrinnet for *9* hver af vare *M9202*.
1. Bekræft læg på lager-trinnet og eventuelle ekstra pluk-/læg på lager-par for at fuldføre arbejdet.

> [!IMPORTANT]
>
> - Arbejdslinjer kan kun grupperes, hvis de er i rækkefølge.
> - Følgende funktionalitet understøttes ikke:
>
>   - Fastvægtvarer
>
>    Hvis der er nogen fastvægtvarer på arbejdet, får du vist en fejlmeddelelse, før du begynder at plukke.
>
>   - Stykplukning
>   - Arbejdslinjer, der har uafsluttede genopfyldningsarbejde.
>   - Overplukning
>   - Kort plukning med vareomfordeling


[!INCLUDE[footer-include](../../includes/footer-banner.md)]