---
title: Planlægge oprydning af data i salgshistorikken
description: Denne artikel beskriver, hvordan du kan hjælpe med at forbedre systemets ydeevne ved at planlægge den periodiske oprydning af salgsopdateringshistorikken, så den kører med et regelmæssigt interval.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335497"
---
# <a name="schedule-sales-history-data-cleanup"></a>Planlægge oprydning af data i salgshistorikken

[!include [banner](../includes/banner.md)]

Som en del af standardoperationen genererer og gemmer Microsoft Dynamics 365 Supply Chain Management data til opdatering af salgshistorikken løbende. Med tiden kan der akkumuleres en stor mængde forældede data i salgshistorikken i systemet. Disse akkumulerede data kan forårsage problemer med ydeevnen og funktioner, når dokumenter, der er relateret til salgsordrer, bogføres. (Disse dokumenter omfatter salgsordrebekræftelser, salgsfølgesedler, salgspluklister og fakturaer). Derfor skal du konfigurere og planlægge den periodiske opgave *Oprydning af salgsopdateringshistorik*, så den kører med et regelmæssigt interval. Denne opgave fjerner alle data i salgshistorikken, som du ikke længere har brug for.

Hvis du bruger den periodiske opgave *Oprydning af salgsopdateringshistorik*, anbefales det, at du aktiverer funktionen *Forbedringer af ydeevnen for oprydning i salgshistorikken*, hvilket gør opgaven mere effektiv. (Men du kan også køre opgaven uden at aktivere denne funktion).

## <a name="turn-on-the-sales-history-cleanup-features"></a>Aktivere funktionerne til oprydning af salgshistorikken

Hvis du vil konfigurere og bruge den periodiske opgave *Oprydning af salgsopdateringshistorik* sammen med alle de funktioner, der er beskrevet i denne artikel, skal du aktivere *Forbedringer af ydeevnen for oprydning i salgshistorikken* og *Ryd op i historik for salgsopdatering baseret på alder* i Funktionsstyring, som beskrevet i følgende undersektioner.

### <a name="sales-history-cleanup-performance-improvements"></a>Forbedringer af ydeevnen for oprydning i salgshistorikken

**Oprydning i salgshistorikken** kan tage lang tid, hvis den køres sjældent i miljøer med en stor mængde salgsopdateringer. I disse situationer kan funktionen til *forbedring af performance for salgshistorikken* hjælpe med at reducere varigheden af kørslen og forbedre pålideligheden.

Funktionen forbedrer det eksisterende oprydningsjob på følgende måder:

- Oprydningen opdeles i batches (du kan ændre batchstørrelsen via tilpasninger).
- Den kører i maksimalt 2 timer (du kan ændre varigheden via tilpasninger).
- Hvor det er muligt, bruges databasefunktionerne til at minimere låsning og til at undgå at forbinde transaktionstabeller under oprydning.

Når funktionen er aktiveret, køres **oprydningen af historikken for salgsopdatering** (**Salgs og marketing \> Periodiske opgaver \> Oprydning \> Oprydning af salgsopdateringhistorik**) som før, men med bedre ydeevne og højst 2 timer. Det betyder, at det kan være nødvendigt at køre flere gange for at rydde op i alle data for en bestemt tidsramme til tilbageholdelse.

Før du kan bruge denne funktion, skal den være aktiveret for dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Salg og marketing*
- **Funktionsnavn:** *Forbedringer af ydeevnen i oprydningssalgshistorik*

### <a name="clean-up-sales-update-history-based-on-age"></a>Ryd op i historik for salgsopdatering baseret på alder

Med funktionen *Ryd op i historik for salgsopdatering baseret på alder* kan du angive den maksimale alder for poster, der skal beholdes, når du kører den periodiske opgave *Oprydning af salgsopdateringshistorik*. Ældre poster slettes. Dette er nyttigt, når du konfigurerer, at opgaven skal køres periodisk, da alderen altid beregnes i forhold til den dato, hvor opgaven køres. Uden denne funktion kan du kun angive en bestemt dato for de ældste poster, der skal beholdes.

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Ryd op i historik for salgsopdatering baseret på alder* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Konfigurere og planlægge den periodiske opgave til oprydning af salgshistorik

Følg disse trin for at konfigurere og planlægge den periodiske opgave *Oprydning af salgshistorik*.

1. Analysér din virksomheds behov for at finde ud af, hvor mange dages posteringsdata til salgsordrer du skal beholde. Det anbefales normalt, at du kører oprydningsopgaven hver tredje måned og højst hver sjette måned.
1. Gå til **Salg og marketing \> Periodiske opgaver \> Oprydning \> Oprydning af salgsopdateringshistorik**.
1. Angiv følgende felter i oversigtspanelet **Parametre** i dialogboksen **Oprydning af salgsopdateringshistorik**:

    - **Oprydning** – Vælg en af følgende værdier for at angive den type poster, der skal ryddes op:

        - **Udført** – Slet kun poster, der er fuldt behandlet. Da du sikkert ikke har yderligere brug for disse poster, er denne indstilling den sikreste.
        - **Udført og fejlbehæftet** – Slet både fuldt behandlede poster og poster, hvor der er opstået en fejl. Denne indstilling er den mest almindelige. Du kan få brug for at undersøge og rette fejlbehæftede poster i stedet for at få dem ryddet op automatisk. Mange firmaer vælger dog også at rydde op i disse poster efter en måned, fordi de sandsynligvis ikke længere er relevante på det pågældende tidspunkt.
        - **Alle** – Slet udførte, fejlbehæftede og ventende poster. Ventende poster er gyldige, men de er endnu ikke fuldt behandlet. I de fleste tilfælde vil du højst sandsynligt ikke have, at de slettes automatisk. I nogle situationer kan du dog vælge at få dem slettet automatisk, når der er gået et bestemt tidsrum.

    - **Behold poster baseret på alder** – Angiv, om du vil rydde op i poster baseret på deres alder på den dag, hvor opgaven køres, eller slette poster, der blev oprettet før en fastlagt dato. Hvis du planlægger oprydningen som en tilbagevendende opgave, skal du angive denne indstilling til *Ja*, da alderen altid beregnes i forhold til den dato, hvor opgaven køres.

        - Angiv denne indstilling til *Ja* for at aktivere feltet **Maksimumalder**. Du bruger dette felt til at angive posternes maksimale alder for at blive beholdt, hver gang opgaven køres. Feltet **Oprettet indtil** ignoreres.
        - Angiv denne indstilling til *Nej* for at aktivere feltet **Oprettet indtil**. Du bruger dette felt til at angive posternes ældste oprettelsesdato for at blive beholdt, når opgaven køres. Feltet **Maksimumalder** ignoreres.

    - **Oprettet indtil** – Denne indstilling gælder kun, når indstillingen **Behold poster baseret på alder** er angivet til *Nej*. Angiv posternes ældste oprettelsesdato for at blive beholdt, når opgaven køres. Poster, der blev oprettet før denne dato, slettes.
    - **Maksimumalder** – Denne indstilling gælder kun, når indstillingen **Behold poster baseret på alder** er angivet til *Ja*. Angiv posternes maksimale alder (i dage) for at blive beholdt, hver gang opgaven køres. Ældre poster slettes.

1. Angiv, hvordan, hvornår og hvor ofte opgaven skal køres, i oversigtspanelet **Kør i baggrunden**. Brug disse indstillinger til at implementere den plan, du fastlagde i trin 1. Felterne fungerer på samme måde som for andre typer af [batchjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK** for at anvende dine indstillinger og dialogboksen.
