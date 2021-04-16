---
title: Behandle varer undervejs
description: I dette emne beskrives, hvordan du kan arbejde med ordrer på varer undervejs. Når en ordre eller fragt er konfigureret til at bruge varer undervejs, kan varer faktureres, før de er modtaget på lagerstedet til forbrug.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9a1316de8d79f3ce34bb28812993d096cbd0c2ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823403"
---
# <a name="goods-in-transit-processing"></a>Behandle varer undervejs

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du kan arbejde med ordrer på varer undervejs. Denne ordretype bruges kun i modulet **Landingsomkostninger**. Når en ordre eller fragt er konfigureret til at bruge varer undervejs, skal du ikke vente på, at varer er modtaget på lagerstedet, før du kan fakturere dem. Varerne faktureres i stedet, når de forlader leverandørens lagersted eller oprindelseshavn, og de økonomiske omkostninger registreres, når fragten starter. Denne funktionalitet giver dig mulighed for at tage ejerskab over lageret, da varer ofte bliver organisationens ejendom, når de forlader forsendelseshavnen.

Når der bruges varer undervejs, modtages de økonomisk opdaterede varer på et midlertidigt lagersted, der kaldes et lagersted for varer undervejs. Varerne bliver derefter på dette lagersted, indtil de kan modtages på det endelige destinationslagersted (det lagersted, der er defineret på indkøbslinjen). De kan ikke fjernes manuelt.

Så længe varerne er undervejs, er de ikke tilgængelige på lageret og kan ikke plukkes fra lageret til en levering. Du kan dog få vist lagerbeholdningen for varer undervejs. Du kan også bruge varerne til varedisponering. I dette tilfælde skal du bruge den bekræftede leveringsdato på indkøbsordrelinjen som den forventede dato for, hvornår lageret vil være tilgængeligt for forbrug.

I følgende afsnit beskrives den opsætning, der kræves for at behandle lagerbeholdning og fragt ved hjælp af begrebet og funktionaliteten af varer undervejs.

## <a name="terms-of-delivery"></a>Leveringsbetingelse

Når du aktiverer modulet **Landingsomkostninger**, er standardenheden for *leveringsbetingelserne* udvidet, så den understøtter funktionen for varer undervejs.

Når indstillingen **Styring af varer undervejs** er angivet til *Ja* for de relevante leveringsbetingelser, overføres varerne til lagerstedet for varer undervejs. Denne handling udløses kun, hvis lagertilgangen ikke behandles, før en faktura behandles. Når leveringsbetingelserne for en ordre er angivet til at bruge varer undervejs, kan brugerne ikke længere bogføre en produktkvittering for indkøbsordren. Hvis de prøver, opstår der en fejl. Fejlmeddelelsen viser, at de skal bruge funktionen varer undervejs for at fortsætte.

Hvis du vil arbejde med oplysninger om leveringsbetingelser for varer undervejs, skal du gå til **Indkøb og forsyning \> Konfiguration \> Distribution \> Leveringsbetingelser**. Følgende tabel indeholder en beskrivelse af de felter, som modulet **Landingsomkostninger** føjer til siden **Leveringsbetingelser** for at understøtte funktionaliteten for varer undervejs. Begge felter findes i oversigtspanelet **Generelt**. Yderligere oplysninger om de andre felter på denne side finder du i [Leveringsbetingelser (formular)](https://technet.microsoft.com/library/aa575567.aspx).

| Felt | Beskrivelse |
|---|---|
| Forsendelseshavn er obligatorisk | Angiv denne indstilling til *Ja*, hvis der skal være en forsendelseshavn, når leveringsbetingelserne gælder. |
| Styring af varer i transit | Angiv denne indstilling til *Ja*, hvis du vil bruge styring af varer undervejs, når leveringsbetingelserne gælder. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Lagersteder for varer undervejs og underlevering

Når du aktiverer modulet **Landingsomkostninger**, er standardenheden for *lagersteder* udvidet, så indkøbsordrer kan faktureres, mens varerne findes på et lagersted for varer undervejs.

Landingsomkostninger tilføjer to nye typer lagersted: *varer undervejs* og *underlevering*. Lagersteder af begge typer kan vælges som standardlagersteder. En vellykket behandling af ordrerne for varer undervejs kræver, at både lagerstedet for varer undervejs og lagerstedet for underlevering er konfigureret på siden **Lagersteder**. For hvert standardlagersted, der skal bruges sammen med Landingsomkostninger og varer undervejs, skal lagerstedet for varer undervejs og lagerstedet for underlevering vælges for de tilgængelige lagersteder af hver type.

Lagerstedstypen *varer undervejs* knyttes til stedet for varer undervejs, og dette lagersted bruges til behandling af varerne i ordrer for varer undervejs, før de modtages på det endelige destinationslagersted. Generelt er ét lagersted for varer undervejs tilstrækkeligt for hver lokation, hvis Lokation og Lagersted er de eneste lagerdimensioner, der bruges til lagerstyring. Hvis lagerdimensionen Lokation også bruges, skal der konfigureres et lagersted for varer undervejs for hver kombination af lokation og lagersted, så standardlokationen også kan angives.

Du kan arbejde med indstillinger for varer undervejs til lagerstederne ved at gå til **Lagerstyring \> Konfiguration \> Lageropdeling \> Lagersteder**. Følgende tabel indeholder en beskrivelse af de felter, som modulet **Landingsomkostninger** føjer til siden **Lagersteder** for at understøtte funktionaliteten for varer undervejs. Begge felter findes i oversigtspanelet **Generelt**. Du kan finde oplysningerne om de andre felter på siden under [Lagersteder (formular)](https://technet.microsoft.com/library/aa620570.aspx).

| Felt | Beskrivelse |
|---|---|
| Lagersted for varer i transit | Identificer de lagersteder for varer undervejs, der er knyttet til hovedlagerstedet. |
| Lagersted til underlevering | Identificer de lagersteder for underlevering, der er knyttet til hovedlagerstedet. |

## <a name="posting-rules-for-landed-cost"></a>Bogføringsregler for landingsomkostninger

Landingsomkostninger tilføjer to nye bogføringsregler, du kan konfigurere. Disse bogføringsregler bruges til økonomisk at bogføre fakturabeløbene for den direkte indkøbsordre for at identificere ejerskabet af varerne, når de forlader oprindelsesstedet. Denne proces erstatter begrebet *varer, der er modtaget, men ikke faktureret*, da varerne faktureres, før de modtages. <!-- KFM: Add a link to the related scenario when available. -->

Du kan arbejde med bogføringsprofiler ved at gå til **Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**. Under fanen **Indkøbsordre** er der følgende nye bogføringsregler tilgængelige:

- **Landingsomkostning, varer undervejs** – Angiv bogføringsreglerne for styring af varer undervejs.
- **Landingsomkostning, periodisering af omkostningsgebyr** – Angiv bogføringsreglerne for periodisering af gebyrkonto.

## <a name="goods-in-transit-orders"></a>Ordrer på varer undervejs

Du kan gennemse og administrere ordrer for varer undervejs direkte i modulet **Landingsomkostninger**. Du kan behandle ordrer for varer undervejs direkte fra siden **Order på varer undervejs**. Du kan også gå til den fragt, der er tilknyttet ordrer for varer undervejs, og behandle hele fragten, forsendelsescontaineren eller folioen. Når du fakturerer en fragt og opretter ordrer for varer undervejs, oprettes der en ny ordre for varer undervejs for hver kombination af lager- og lagerdimensioner, der er knyttet til indkøbsordrelinjen.

Til at administrere varer undervejs bruger Landingsomkostninger en totrinsprocedure:

1. En vare modtages, når en lagerfaktura behandles, og tildeles statussen *Undervejs*.
1. Ordren for varer undervejs behandles på siden **Ordrer for varer undervejs** og modtages derefter på det lagersted, der er angivet på indkøbsordren. På dette tidspunkt ændres status til *Modtaget*.

Du kan arbejde med ordrer for varer undervejs ved at gå **Landingsomkostninger \> Periodiske opgaver \> Ordrer for varer undervejs**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Modtage lagerbeholdning fra lagerstedet for varer undervejs

Du kan modtage varer fra en ordre for varer undervejs på mange måder, afhængigt af systemopsætningen.

### <a name="in-transit-receiving"></a>Modtagelse af varer undervejs

Du kan modtage varer undervejs fra en af følgende sider:

- Vælg linjen **Ordrer for varer undervejs**, og vælg derefter **Modtag** i handlingsruden.
- Vælg eller åbn en fragt på siden **Alle fragter**. I handlingsruden under fanen **Administrer** i gruppen **Varer undervejs** skal du derefter vælge **Modtag varer undervejs**.
- Vælg eller åbn en forsendelsescontainer på siden **Alle forsendelsescontainere**. I handlingsruden under fanen **Administrer** i gruppen **Varer undervejs** skal du derefter vælge **Modtag varer undervejs**.
- Vælg eller åbn en folio på siden **Alle folioer**. I handlingsruden under fanen **Administrer** i gruppen **Varer undervejs** skal du derefter vælge **Modtag varer undervejs**.

> [!NOTE]
> Modtagelse af varer undervejs bruges normalt i situationer, hvor lokationer og batch-/seriesporing ikke anvendes.

### <a name="arrival-journal"></a>Modtagelseskladde

Du kan også modtage varer ved at oprette en modtagelseskladde. Du kan oprette en modtagelseskladde direkte fra fragtsiden. Den bedste fremgangsmåde, som din organisation har fastlagt, bestemmer, om modtagelseskladden bruges til at modtage varer.

1. Åbn fragten, containeren eller folioen.
1. I handlingsruden under fanen **Administrer** i gruppen **Funktioner** skal du vælge **Opret modtagelseskladde**.
1. Angiv følgende værdier i dialogboksen **Opret modtagelseskladde**:
    - **Initialiser antal** – Angiv denne indstilling til *Ja* for at angive antallet fra antallet undervejs. Hvis denne indstilling er angivet til *Nej*, angives der ikke et standardantal fra linjerne til varer undervejs.
    - **Opret fra varer undervejs** – Angiv denne indstilling til *Ja*, hvis du vil tage antal fra de valgte linjer undervejs for den valgte fragt, container eller folio.
    - **Opret fra ordrelinjer** – Angiv denne indstilling til *Ja* for at angive standardantallet i modtagelseskladden fra indkøbsordrelinjerne. Standardantallet i modtagelseskladden kan kun angives på denne måde, hvis antallet på indkøbsordrelinjen svarer til antallet i ordren for varer undervejs.

1. Kør processen for modtagelseskladden som beskrevet i [Registrere varetilgange med en varemodtagelseskladde](https://technet.microsoft.com/library/aa571129.aspx).

> [!NOTE]
> Modtagelseskladden bruges normalt i situationer, hvor der bruges lokationer og batch-/seriesporing, men hvor lokationsstyring ikke bruges.
>
> Standardtilgangslokationerne bør ikke angives på ordrelinjerne, hvis der angives en læg-lokation i modtagelseskladden.

## <a name="warehouse-management"></a>Lokationsstyring

Når du aktiverer modulet **Landingsomkostninger**, ændres flere sider i modulet **Lokationsstyring**, så ordrebehandling (specifikt behandling af varer undervejs) kan ske via modulet **Landingsomkostninger**. Dette afsnit viser de felter og processer, der er tilføjet i modulet **Lokationsstyring**.

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

Varer kan modtages via en mobilenhed, hvis menuen for mobilenhed og modulet **Lokationsstyring** er konfigureret til at modtage varer i en ordre for varer undervejs. Dette afsnit indeholder en beskrivelse af den opsætning, der er knyttet til modtagelse af varer undervejs.

Hvis du vil konfigurere mobilenheder til behandling af varer undervejs, skal du gå til **Lokationsstyring \> Konfiguration \> Mobilenhed \> Menupunkter i mobilenhed**.

Landingsomkostninger føjer følgende arbejdsprocesser til menupunkterne for mobilenheden for at understøtte behandlingen af varer undervejs:

- Varemodtagelse af varer i transit
- Modtagelse og placering af varer undervejs

Konfigurationsindstillingerne for disse processer ligner indstillingerne for [arbejdsoprettelsesprocesser for modtagelse og placering af indkøbsordrer](https://technet.microsoft.com/library/dn553216.aspx). I processen *Modtagelse og placering af varer undervejs* tilføjes dog også følgende felt.

- **Aktivér fuldført forsendelsescontainer** – Hvis denne indstilling er angivet til *Ja*, når arbejdsstedet læg-arbejdet er fuldført, indeholder mobilappen Lokationsstyring en ekstra indstilling med navnet **Forsendelsescontainer fuldført**. Når denne indstilling er valgt, vil arbejderen blive bedt om at bekræfte, at containeren er fuldført. På dette tidspunkt vil alle korte tilgange blive behandlet som en undertransaktion.

### <a name="location-directives"></a>Lokationsvejledninger

Landingsomkostninger tilføjer en ny arbejdsordretype med navnet *Varer undervejs* på siden **Lokationsvejledninger**. Denne arbejdsordretype skal konfigureres på samme måde som [arbejdsordretyperne for indkøbsordrer](https://technet.microsoft.com/library/dn553184.aspx).

### <a name="work-templates"></a>Arbejdsskabeloner

Landingsomkostninger tilføjer en ny arbejdsordretype med navnet *Varer undervejs* på siden **Arbejdsskabeloner**. Denne arbejdsordretype skal konfigureres på samme måde som [arbejdsskabeloner for indkøbsordrer](https://technet.microsoft.com/library/dn553184.aspx).

