---
title: Tærskel for genopfyldning af zone
description: Ved zonebaseret genopfyldning bruges en opfyldningsstrategi for minimum/maksimum (min./maks.), men den evaluerer hele lagerzoner i stedet for kun individuelle lokationer. Lagercheferne kan derfor hurtigere finde ud af, når der kræves yderligere lagerplads i en plukzone.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dde844d38448b2de5c5e0c9b2da4a16405f83c0d72f3a20b9e29afe84d322ac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743476"
---
# <a name="zone-threshold-replenishment"></a>Tærskel for genopfyldning af zone

[!include [banner](../includes/banner.md)]

Ved zonebaseret genopfyldning bruges en opfyldningsstrategi for minimum/maksimum (min./maks.) [genopfyldning](replenishment.md), men den evaluerer hele lagerzoner i stedet for kun individuelle lokationer. Lagercheferne kan derfor hurtigere finde ud af, når der kræves yderligere lagerplads i en plukzone.

Konfigurationen for denne funktion ligner konfigurationen af lokationsbaseret genopfyldning. Men når du konfigurerer en skabelon for min.-/maks.-genopfyldning, kan du også angive, om tærsklen skal evalueres pr. lokation eller pr. zone. Hvis du konfigurerer evaluering, der er baseret på zoner, skal du føje bestemte zoner til zoneudvælgelsesforespørgslen.

Som lokationsbaseret min./maks.-genopfyldning er den zonebaserede min./maks.-genopfyldning baseret på konfigurationen af en minimumtærskel for lager, der udløser oprettelsen af genopfyldningsarbejde for udvalgte varer. Dette genopfyldningsarbejde vil øge lageret op til den angivne tærskel for zonens maksimumtærskel.

> [!NOTE]
> Processer til zonegenopfyldning for produktvarianter understøttes ikke i den aktuelle version.


I modsætning til lokationsbaseret min./maks.-genopfyldning kræver zonebaseret min/maks.-genopfyldning ikke faste lokationer for at vurdere, om lokationer skal opbevare en bestemt vare. Derfor giver zonebaseret opfyldning mulighed for at bruge min./maks.-genopfyldning, selvom du ikke har faste lokationer for hver vare eller varevariant på lagerstedet. Når et antal i zonen falder til under den angivne minimumstærskel, oprettes genopfyldningsarbejde. Lokationsvejledninger bestemmer, hvilken specifik lokation lageret skal lægges på.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Aktivér funktionen til tærskel for genopfyldning af zone

Før du kan bruge funktionen *Tærskel for genopfyldning af zone*, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Tærskel for genopfyldning af zone*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Konfigurer zonebaseret genopfyldning

Hvis du vil konfigurere zonebaseret genopfyldning, skal du konfigurere flere dele af systemet. I dette afsnit introduceres de forskellige indstillinger og de demodataværdier, du kan angive, hvis du vil arbejde dig gennem scenariet sidst i dette emne.

### <a name="set-up-directive-codes"></a>Konfigurere vejledningskoder

[Vejledningskoder](control-warehouse-location-directives.md) gør, at du kan være mere specifik, når du definerer den lokationsskabelon, der bruges i en arbejdsskabelon. Hver kode opretter en fælles værdi, som du kan referere til, når du konfigurerer hver type skabelon.

#### <a name="view-and-edit-directive-codes"></a>Få vist og redigere vejledningskoder

Hvis du vil have vist eller redigere dine vejledningskoder, skal du gå til **Lokationsstyring \> Konfiguration \> Vejledningskoder**.

#### <a name="prepare-demo-data-directive-codes"></a>Forberede vejledningskoder til demodata

I dette eksempel vises, hvordan du forbereder en vejledningskode. Hvis du planlægger at arbejde dig gennem scenariet i slutningen af dette emne, skal du bruge de demoværdier, der angives her. Ellers skal du bruge dine egne værdier.

1. Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.
1. Gå til **Lokationsstyring \> Opsætning \> Vejledningskoder**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Vejledningskode:** _Zonegenopfyldning_
    - **Vejledningsbeskrivelse:** _Zonegenopfyldning_

1. Vælg **Gem** for at gemme den nye kode.

### <a name="set-up-replenishment-templates"></a>Konfigurer genopfyldningsskabeloner

[Min/Max er genopfyldningsskabeloner](tasks/set-up-min-max-replenishment-process.md) er den primære mekanisme til opretholdelse af optimale niveauer på pluklokationer. I disse skabeloner skal du konfigurere de regler, der skal bruges til genopfyldning af lageret på lagerstedet. Den genopfyldning, som skabelonerne kan bruges til, omfatter zonebaseret genopfyldning.

#### <a name="view-and-edit-replenishment-templates"></a>Få vist og rediger genopfyldningsskabeloner

En genopfyldningsskabelon er et sæt regler, der styrer, hvornår og hvordan en lokation skal genopfyldes. Du kan vælge en skabelon til at styre, hvornår og hvordan genopfyldningen skal udføres. Du kan få vist eller redigere dine genopfyldningsskabeloner ved at gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Forberede en genopfyldningsskabelon til demodata

I dette eksempel vises, hvordan du forbereder en genopfyldningsskabelon. Hvis du planlægger at arbejde dig gennem scenariet i slutningen af dette emne, skal du bruge de demoværdier, der angives her. Ellers skal du bruge dine egne værdier.

1. Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.
1. Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.
1. Vælg **Rediger** for at sætte siden i redigeringstilstand.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret **Oversigt**.
1. Angiv følgende værdier i den nye række. Accepter standardværdierne for alle andre felter.

    - **Genopfyldningsskabelon:** _Zone – min./maks. genopfyld._
    - **Beskrivelse:** _Min./maks. genopfyldning for zone_
    - **Genopfyldningstype:** _minimum eller maksimum_

1. Vælg **Gem**.
1. Mens den nye række stadig er markeret i gitteret **Oversigt**, skal du vælge **Ny** over **Detaljer for genopfyldningsskabelon** for at tilføje en række, der er knyttet til genopfyldningsskabelonen *Zone – min./maks. genopfyld.*, du netop har oprettet.
1. Angiv følgende værdier i den nye række:

    - **Løbenummer:** Angiv _1_.
    - **Beskrivelse:** Angiv _Genopfyldning af plukzone_.
    - **Opfyldningsenhed:** Vælg _hver_.
    - **Anmodningstype** Lad dette felt stå tomt.
    - **Vejledningskode:** Dette felt knytter genopfyldningsskabelonen sammen med en lokationsvejledning. Vælg den vejledningskode til demodata, du oprettede tidligere (_Zonegenopfyldning_).
    - **Arbejdsskabelon:** Lad feltet stå tomt.
    - **Minimumantal:** Dette felt angiver det antal, som opfyldning skal udløses på. Angiv _50_.
    - **Maksimumantal:** Dette felt angiver det maksimale antal af en vare, der kan være til stede i en zone. Oprettet genopfyldningsarbejde vil øge lagerbeholdningen til dette antal. Angiv _150_.
    - **Enhed:** Dette felt angiver enheden for minimum- og maksimumværdier. Vælg _hver_.
    - **Efterspørgselsstigning:** Vælg _Rund op_.
    - **Genopfyld tomme faste lokationer:** Markér dette afkrydsningsfelt.
    - **Genopfyld kun faste lokationer:** Ryd dette afkrydsningsfelt.
    - **Produktforespørgselstilstand:** Vælg _Produktforespørgsel_.
    - **Tærskelområde for genopfyldning:** Dette felt definerer, om skabelonen skal evalueres pr. zone eller efter en bestemt lokation. Vælg _Zone_.
    - **Lagersted:** Vælg _61_.

1. Vælg **Vælg produkter** over gitteret **Detaljer for genopfyldningsskabelon**.
1. I dialogboksen **Produktforespørgsel** skal du på fanen **Område** vælge **Tilføj** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** _Varer_
    - **Afledt tabel:** _Varer_
    - **Felt:** _Varenummer_
    - **Kriterier:** _A0001_

1. Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.
1. Vælg **Vælg zoner til genopfyldning** over gitteret **Detaljer for genopfyldningsskabelon**.
1. I dialogboksen **Zoneforespørgsel** skal du på fanen **Område** føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** _Lagerstedszone_
    - **Afledt tabel:** _Lagerstedszone_
    - **Felt:** _Zone-id_
    - **Kriterier:** _PRODUKTION_

1. Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.

### <a name="set-up-location-directives"></a>Konfigurer lokationsvejledninger

I modsætning til lokationsbaseret min./maks.-genopfyldning kræver zonebaseret min./maKS.-genopfyldning, at du konfigurerer både lokationsvejledninger for pluk og lokationsvejledninger for læg på lager, fordi systemet evaluerer hele zonen i stedet for blot pluklokationen til udgående arbejde.

#### <a name="view-and-edit-location-directives"></a>Få vist og redigere lokationsvejledninger

Hvis du vil have vist eller redigere dine lokationsvejledninger, skal du gå til **Lokationsstyring \> Konfiguration \> Lokationsvejledninger**.

Du kan se eksempler, der viser, hvordan du kan bruge indstillingerne til at oprette de lokationsvejledninger til pluk og lokationsvejledninger til læg på lager, i næste afsnit.

#### <a name="prepare-demo-data-location-directives"></a>Forberede lokationsvejledninger til demodata

Hvis du vil forberede demodata, så de kan bruges i scenariet sidst i dette emne, skal du oprette to lokationsvejledninger: et til pluk og et til læg på lager.

##### <a name="create-a-replenishment-pick-directive"></a>Oprette en plukkevejledning for genopfyldning

1. Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.
1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I venstre rude skal du angive feltet **Arbejdsordretype** til _Genopfyldning_.
1. Vælg **Ny** i handlingsruden for at oprette en ny vejledning.
1. Angiv følgende værdier:

    - **Løbenummer:** Accepter standardværdien.
    - **Navn:** Angiv _Zonepluk_.
    - **Arbejdstype:** Vælg _Pluk_.
    - **Lokation:** Vælg _6_.
    - **Lagersted:** Vælg _61_.
    - **Vejledningskode:** Lad feltet være tomt.
    - **Multi-SKU:** Angiv denne indstilling til _Nej_.

1. Vælg **Gem** for at oprette en vejledning, der har de indstillinger, som du har konfigureret indtil nu.
1. Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** Angiv _1_.
    - **Fra antal:** Angiv _0_.
    - **Til antal:** Angiv _10000000_.
    - **Enhed:** Lad feltet være tomt.
    - **Find antal:** Vælg _Ingen_.
    - **Begræns efter enhed:** Ryd dette afkrydsningsfelt.
    - **Rund op til enhed:** Fjern markeringen i dette afkrydsningsfelt.
    - **Find emballagemængde:** Fjern markeringen i dette afkrydsningsfelt.
    - **Tillad opdeling:** Markér dette afkrydsningsfelt.

1. Vælg **Gem** for at gemme den nye linje.
1. Mens den nye linje stadig er markeret i gitteret **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger i lokationsvejledning** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Løbenummer:** Angiv _1_.
    - **Navn:** Angiv _Pluk fra masse_.
    - **Anvendelse af fast lokation:** Vælg _Faste og ikke-faste lokationer_.
    - **Tillad negativ lagerbeholdning:** Fjern markeringen i dette afkrydsningsfelt.
    - **Batch aktiveret:** Fjern markeringen i dette afkrydsningsfelt.
    - **Strategi:** Vælg _Ingen_.

1. Vælg **Gem** for at gemme den nye handling.
1. Mens den nye handling stadig er valgt, skal du vælge **Rediger forespørgsel** over gitteret **Handlinger i lokationsvejledning**.
1. Der vises en forespørgselsdialogboks, hvor du kan vælge de lokationer, der skal genopfyldes fra. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** _Lokationer_
    - **Afledt tabel:** _Lokationer_
    - **Felt:** _Zone-id_
    - **Kriterier:** _BULK_

1. Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.
1. Vælg **Gem** for at gemme din lokationsvejledning.

##### <a name="create-a-replenishment-put-directive"></a>Oprette en læg på lager-vejledning for genopfyldning

1. På siden **Lokationsvejledninger** skal du i venstre rude kontrollere, at feltet **Arbejdsordretype** stadig er angivet til _Genopfyldning_.
1. Vælg **Ny** i handlingsruden for at oprette en anden vejledning.
1. Angiv følgende værdier:

    - **Løbenummer:** Accepter standardværdien.
    - **Navn:** Angiv _Zone-læg på lager_.
    - **Ordretype:** Vælg _Læg på lager_.
    - **Lokation:** Vælg _6_.
    - **Lagersted:** Vælg _61_.
    - **Vejledningskode:** Vælg _Zonegenopfyldning_ for at knytte denne lokationsvejledning direktiv til den opfyldningsskabelon, du har oprettet tidligere ved hjælp af den kode, du har oprettet tidligere.
    - **Multi-SKU:** Angiv denne indstilling til _Nej_.

1. Vælg **Gem** for at oprette en vejledning, der har de indstillinger, som du har konfigureret indtil nu.
1. Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** Angiv _1_.
    - **Fra antal:** Angiv _0_.
    - **Til antal:** Angiv _10000000_.
    - **Enhed:** Lad feltet være tomt.
    - **Find antal:** Vælg _Ingen_.
    - **Begræns efter enhed:** Ryd dette afkrydsningsfelt.
    - **Rund op til enhed:** Fjern markeringen i dette afkrydsningsfelt.
    - **Find emballagemængde:** Fjern markeringen i dette afkrydsningsfelt.
    - **Tillad opdeling:** Markér dette afkrydsningsfelt.

1. Vælg **Gem** for at gemme den nye linje.
1. Mens den nye linje stadig er markeret i gitteret **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger i lokationsvejledning** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Løbenummer:** Angiv _1_.
    - **Navn:** Angiv _Zone-læg på lager_.
    - **Anvendelse af fast lokation:** Vælg _Faste og ikke-faste lokationer_.
    - **Tillad negativ lagerbeholdning:** Fjern markeringen i dette afkrydsningsfelt.
    - **Batch aktiveret:** Fjern markeringen i dette afkrydsningsfelt.
    - **Strategi:** Vælg _Konsolider_.

1. Vælg **Gem** for at gemme den nye handling.
1. Mens den nye handling stadig er valgt, skal du vælge **Rediger forespørgsel** over gitteret **Handlinger i lokationsvejledning**.
1. Der vises en forespørgselsdialogboks, hvor du kan vælge den zone, der skal genopfyldes til. Denne zone skal være den samme som den zone, der er angivet i genopfyldningsskabelonen. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** _Lokationer_
    - **Afledt tabel:** _Lokationer_
    - **Felt:** _Zone-id_
    - **Kriterier:** _PRODUKTION_

1. Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.
1. Vælg **Gem** for at gemme din lokationsvejledning.

## <a name="scenario"></a>Scenario

Dette afsnit indeholder et eksempel på et scenarie, der viser, hvordan du kan arbejde med funktionen.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Forbered de eksempeldata, der kræves i eksempelscenariet

Før du går i gang med at arbejde med scenariet, skal du aktivere eksempeldata og konfigurere funktionen som beskrevet i dette afsnit og i forudgående afsnit i dette emne.

#### <a name="use-the-usmf-legal-entity"></a>Brug den juridiske enhed USMF

Hvis du vil arbejde gennem scenariet ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

#### <a name="prepare-additional-sample-data"></a>Forberede yderligere eksempeldata

Når du har valgt den juridiske enhed **USMF**, skal du tilføje de ekstra eksempeldata, der kræves, som beskrevet i afsnittet [Konfigurer zonebaseret genopfyldning](#setup) tidligere i dette emne.

#### <a name="check-your-on-hand-inventory"></a>Kontrollér dit disponible lager

Udfør følgende trin for at sikre, at systemet har et tilstrækkeligt lager til at understøtte eksempelscenariet.

1. Kontroller, at der er et disponibelt lager for vare *A0001* på to forskellige lokationer i plukzonen (*PRODUKTION*), der er angivet i genopfyldningsskabelonen. Det samlede lager skal dog være mindre end det krævede minimumantal (*50*), der er angivet på genopfyldningsskabelonen. På denne måde kan du simulere, hvordan beregningen finder sted for hele zonen i stedet for en enkelt lokation. **Brug en af lagerstedsprocesserne til at regulere lageret efter behov.**
1. Sørg for, at der er tilstrækkeligt lager til vare *A0001* på en massevarelokation, der er angivet i lokationsvejledningen til zone-pluk, hvor genopfyldningsarbejdet skal plukke varerne fra zone-id'et *MASSE*. Det samlede lager skal være mere end det krævede maksimantal (*150*), der er angivet i genopfyldningsskabelonen.
1. Valgfrit, men anbefalet: Udfør følgende trin for at oprette en lagerreguleringskladde:

    1. Gå til **Lokationsstyring \> Kladdeposteringer \> Varer \> Lagerregulering**.
    1. Vælg **Ny**.
    1. Vælg **61** i dialogboksen **Opret lagerkladde** i feltet *Lagersted*.
    1. Vælg **OK**.
    1. I oversigtspanelet **Kladdelinjer** skal du bruge knappen **Ny** til at føje tre linjer til gitteret og angive følgende værdier. Vælg **Gem**, når du er færdig med at definere hver linje.

        - **Linje 1:**

            - **Varenummer:** *A0001*
            - **Lokation:** *6*
            - **Lagersted:** *61*
            - **Lokation:** *02A01R1S1B*
            - **Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.
            - **Antal:** *1000*

        - **Linje 2:**

            - **Varenummer:** *A0001*
            - **Lokation:** *6*
            - **Lagersted:** *61*
            - **Lokation:** *07A01R2S1B*
            - **Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.
            - **Antal:** *15*

        - **Linje 3:**

            - **Varenummer:** *A0001*
            - **Lokation:** *6*
            - **Lagersted:** *61*
            - **Lokation:** *07A01R1S1B*
            - **Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.
            - **Antal:** *10*

    1. Vælg **Valider** i handlingsruden. Løs eventuelle fejl, der findes, før du går videre til næste trin.
    1. I handlingsruden skal du vælge **Bogfør** for at postere lageret til lagerstedet.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Eksempelscenarie: Kør zonebaseret min-/maks.-genopfyldning

Når alle de nødvendige eksempeldata er på plads, kan du udløse genopfyldning ved at følge disse trin.

1. Gå til **Lokationsstyring \> Genopfyldning \> Genopfyldninger**.
1. I dialogboksen **Genopfyldning** skal du i oversigtspanelet **Poster, der skal indgå** vælge **Filter**.
1. I dialogboksen **Forespørgsel** skal du under fanen **Område** redigere standardtabelrækken på følgende måde:

    - **Tabel:** Vælg _Genopfyldningsskabeloner_.
    - **Afledt tabel:** Vælg _Genofyldningsskabeloner_.
    - **Felt:** Vælg _Genopfyldningsskabelon_.
    - **Kriterier:** Vælg _Zone – min./maks. genopfyld._. Denne genopfyldningsskabelon er den genopfyldningsskabelon, du oprettede, mens du forberedte demodataene til dette scenarie.

1. Vælg **OK** for at gemme forespørgslen, og gå tilbage til dialogboksen **Genopfyldning**.
1. Vælg **OK** for at køre opfyldningsskabelonen.

Genopfyldningsarbejdet er nu oprettet til at plukke lager fra *MASSE*-zonen og genopfylde det zonen *PRODUKTION*.

## <a name="notes-and-tips"></a>Noter og tip

Her er nogle få noter og tip til arbejdet med funktionen:

- Hvis du vil konfigurere genopfyldningsarbejde, der går til den ønskede zone, kan du sammenkæde linjer i genopfyldningsskabelonen og lokationsvejledningerne på en af følgende måder:

    - Rediger forespørgslen efter lokationsvejledningens overskrift, og filtrer de valgte linjer på genopfyldningsskabelonen.
    - Brug en vejledningskode på linjen i genopfyldningsskabelonen, og kæd den sammen med læg på lager-lokationsvejledningen.

- Hvis du bruger dynamiske lokationer, oprettes genopfyldningsarbejdet enten for den første tilgængelige lokation eller for en lokation, der allerede indeholder lager, hvis handlingen i lokationsvejledningen er konfigureret til at bruge strategien **Konsolider**.
- Hvis du bruger faste lokationer i stedet for zoner, skal du bruge [standard-min./maks. for genopfyldning](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]