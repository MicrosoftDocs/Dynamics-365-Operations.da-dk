---
title: Administrere ændringer af tekniske produkter
description: Dette emne indeholder oplysninger om styring af tekniske ændringer. Styring af tekniske ændringer omfatter strukturerede processer til administration af ændringer i tekniske produkter, fra forslag, anmodninger over ændringer til gennemgang og godkendelse af ændringer, vurdering af deres indflydelse på eksisterende transaktioner og opfølgning på dem.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 55952a9b1c25b806ee4a21ef1982c5b15a41adeb9c9bfdf2fccb8c9da242ffdb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714324"
---
# <a name="manage-changes-to-engineering-products"></a>Administrere ændringer af tekniske produkter

[!include [banner](../includes/banner.md)]

Styring af tekniske ændringer omfatter strukturerede processer til administration af ændringer i tekniske produkter. Du kan bruge processen *anmodning om teknisk ændring* til at foreslå og anmode om ændringer og derefter bruge processen *teknisk ændringsordre* til at foretage disse ændringer. Brugerne kan oprette tekniske ændringsanmodninger eller tekniske ændringsordrer, og der er derefter en proces til at gennemgå og godkende dem, vurdere deres indflydelse på eksisterende transaktioner og følge op på dem.

## <a name="engineering-change-requests"></a>Tekniske ændringsanmodninger

Ved hjælp af processen til anmodning om teknisk ændring kan du registrere anmodninger om ændringer fra alle de relevante afdelinger i dit firma. Det er ligegyldigt, om du arbejder som ingeniør eller i produktion, forsyning, lagersted eller salgsafdeling: Alle kan bruge en anmodning om en teknisk ændring til at anmode om en ændring. Denne ændring kan være en idé til et nyt produkt, et problem, som du har opdaget, mens du arbejdede med et eksisterende produkt, et forslag til forbedring af et eksisterende produkt eller noget andet.

Når nogen sender en anmodning om ændring, administreres *gennemsyns- og godkendelses*-processen af en arbejdsproces, der angiver, hvem der skal godkende ændringen (f.eks. produktejeren).

Hvis du vil oprette en arbejdsproces til tekniske ændringsordrer eller tekniske ændringsanmodninger, skal du gå til **Teknisk ændringsstyring \> Tekniske arbejdsprocesser**. Vælg **Ny**, vælg, om arbejdsprocessen skal bruges til at gennemgå tekniske ændringsordrer eller anmodninger om teknisk ændring, og konfigurer derefter arbejdsprocessen.

Yderligere oplysninger om arbejdsprocesser finder du i [Oversigt over arbejdsgangssystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Du kan finde flere oplysninger om produktejere under [Produktejere](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Opret en ny anmodning om teknisk ændring

Hvis du vil oprette en anmodning om en teknisk ændring, skal du følge et af disse trin.

- Gå til **Teknisk ændringsstyring \> Fælles \> Teknisk ændringsstyring \> Tekniske ændringsanmodninger**, og vælg derefter **Ny** i handlingsruden.
- Åbn siden **Produktdetaljer** for et eksisterende teknisk produkt. I handlingsruden under fanen **Teknisk** i gruppen **Teknisk ændringsstyring** skal du vælge **Teknisk ændringsanmodning \> Ny teknisk ændringsanmodning**.

Der oprettes en ny ændringsanmodning. Nu kan du i hvert oversigtspanel angive felterne som beskrevet i følgende underafsnit.

#### <a name="general-fasttab"></a>Oversigtspanelet Generelt

I oversigtspanelet **Generelt** kan du angive en grundlæggende beskrivelse af ændringsanmodningen. I følgende tabel forklares felterne i dette oversigtspanel.

| Felt | Beskrivelse |
|---|---|
| Ændringsanmodning | Angiv et navn til anmodningen om teknisk ændring. |
| Stilling | Angiv tekst, der kort beskriver eller identificerer ændringerne i anmodningen. |
| Prioritet | Vælg en værdi for at angive, hvor høj prioriteten af ændringen er. Du kan tilpasse de tilgængelige værdier for dit firma efter behov. (Yderligere oplysninger finder du i [Fastlægge fælles værdier til styring af tekniske ændringer](engineering-change-management-setup.md)). |
| Kategori | Vælg en værdi for at beskrive den type ændring, du anmoder om. Du kan tilpasse de tilgængelige værdier for dit firma efter behov. (Yderligere oplysninger finder du i [Fastlægge fælles værdier til styring af tekniske ændringer](engineering-change-management-setup.md)). |
| Alvorlighed | Vælg en værdi for at angive alvorsgraden af det problem, der skal løses ved at implementere anmodningen. Du kan tilpasse de tilgængelige værdier for dit firma efter behov. (Yderligere oplysninger finder du i [Fastlægge fælles værdier til styring af tekniske ændringer](engineering-change-management-setup.md)). |
| Anmodet af | Navnet på den bruger, som oprettede anmodningen. |
| Til | Dato for oprettelse af anmodningen. |
| Status | Status for anmodningen. Når der oprettes en anmodning, er statussen *Oprettet*. Når anmodningen godkendes, ændres status til *Godkendt*. Hvis der er oprettet en relateret ændringsordre til anmodningen, ændres status til *Fulgt op på*. |
| Ændringsordre | Nummeret på ændringsordren, hvis ændringsanmodningen blev fulgt op via en ændringsordre. |

#### <a name="information-fasttab"></a>Oversigtspanelet Oplysninger

I oversigtspanelet **Oplysninger** kan du tilføje flere oplysninger om anmodningen.

Hvis du vil føje en række til gitteret, skal du vælge **Ny** på værktøjslinjen oven over gitteret og derefter vælge en af følgende indstillinger:

- **Fil** – Upload en fil.
- **Billede** – Upload en billedfil.
- **Note** – Angiv en note direkte i gitteret.
- **URL-adresse** – Angiv en URL-adresse direkte i gitteret.

I følgende tabel forklares felterne i hver række.

| Felt | Beskrivelse |
|---|---|
| Dato og klokkeslæt for oprettelse | Dato og klokkeslæt for oprettelse af rækken. |
| Type | Den type oplysninger, rækken blev oprettet til (fil, billede, note eller URL-adresse). |
| Beskrivelse | Angiv en beskrivelse af rækken. |
| Restriktion | En værdi, der angiver, om de oplysninger, der er tilføjet, kommer fra en intern eller ekstern kilde. |
| Vedlagt | Et markeret afkrydsningsfelt angiver, at rækken indeholder en vedhæftet fil (eller vedhæftet billede). Hvis du vil hente den vedhæftede fil, skal du markere rækken og derefter vælge **Åbn** på værktøjslinjen oven over gitteret. |

#### <a name="products-fasttab"></a>Oversigtspanelet Produkter

I oversigtspanelet **Produkter** kan du angive alle de produkter, der påvirkes af ændringsanmodningen. Brug knapperne på værktøjslinjen til at føje produkter til gitteret eller fjerne produkter.

Denne liste er udelukkende til orientering. Derfor kan du tilføje så mange relaterede produkter, som du anser for relevante. Hvis du opretter en anmodning om ændring på siden **Produktdetaljer** for et eksisterende produkt, skal det pågældende produkt vises i oversigtspanelet **Produkter**, når du har gemt anmodningsposten.

#### <a name="source-fasttab"></a>Oversigtspanelet Kilde

I oversigtspanelet **Kilde** kan du spore udgangspunktet for ændringsanmodningen. Det er nyttigt, hvis du f.eks. vil se, om ændringsanmodningen er oprettet ud fra en salgsordre, hvem der har oprettet den, og hvilket firma den blev oprettet i.

### <a name="evaluate-the-business-impact-of-a-change-request-and-send-notifications"></a>Evaluere forretningseffekten af en anmodning om ændring og sende beskeder

Når du gennemgår en anmodning om ændringer, kan du søge efter afhængigheder. På denne måde kan du vurdere virkningen af den ønskede ændring på åbne transaktioner, f.eks. salgsordrer, produktionsordrer og disponibel lagerbeholdning. Mens du gennemgår anmodninger om ændringer, kan du sende en besked til de personer, der er ansvarlige for at opfylde de forskellige typer relaterede ordrer.

#### <a name="review-affected-transactions-block-selected-transactions-and-send-notifications"></a>Gennemse berørte transaktioner, blokere valgte transaktioner og sende beskeder

Hvis du vil gennemse berørte transaktioner, blokere valgte transaktioner og sende beskeder, skal du følge disse trin.

1. Gå til **Teknisk ændringsstyring \> Fælles \> Teknisk ændringsstyring \> Tekniske ændringsanmodninger**.
1. Du skal enten åbne en eksisterende anmodning om ændring eller vælge **Ny** i handlingsruden for at oprette en ny ændringsanmodning.
1. I handlingsruden skal du vælge en af følgende knapper under fanen **Ændringsanmodning** i gruppen **Forretningseffekt**:

    - **Søg** – Scanner alle åbne transaktioner og åbner derefter dialogboksen **Forretningskonsekvenser for åbne transaktioner**, som viser alle de transaktioner, der påvirkes af ændringen.
    - **Se forrige søgning** – Åbn dialogboksen **Forretningskonsekvenser for åbne transaktioner**, som viser resultaterne af den forrige søgning. (Der foretages ingen ny søgning).

1. Dialogboksen **Forretningskonsekvenser for åbne transaktioner** indeholder et sæt faner, som hver især viser en liste over berørte transaktioner af en bestemt type (**Salgsordrer**, **Indkøbsordrer**, **Produktionsordrer**, **Lager** osv.). Hver fane viser også et tal, der angiver antallet af berørte transaktioner af den pågældende type. Vælg en fane for at få vist den relevante liste.
1. Hvis du vil arbejde med en transaktion på listen, skal du markere den og derefter vælge en af følgende knapper på værktøjslinjen:

    - **Vis transaktion** – Åbn den valgte transaktionspost.
    - **Bloker ordre** – Denne knap er kun tilgængelig under fanen **Salgsordrer**. Markér den for at blokere den valgte salgsordre.
    - **Bloker linje** – Denne knap er kun tilgængelig under fanen **Købsordrer**. Markér den for at blokere den valgte købsordrelinje.
    - **Giv den ansvarlige besked** – Denne knap er kun tilgængelig under fanen **Salgsordrer**. Markér den for at sende en ændringsbesked til den bruger, der er angivet som ansvarlig for den valgte salgsordre.
    - **Giv ordregiver besked** – Denne knap er kun tilgængelig under fanen **Købsordrer**. Markér den for at sende en ændringsbesked til den bruger, der er angivet som ordregiver for den valgte købsordre.
    - **Giv produktion besked** – Denne knap er kun tilgængelig under fanen **Produktionsordrer**. I modsætning til salgsordrer og indkøbsordrer har produktionsordrer ikke en enkelt bruger, der er angivet som ansvarlig for dem fra start til slut. I stedet overtager forskellige tilsynsførende eller planlæggere normalt ejerskab for en bestemt lokation eller for en bestemt del af produktionen (for eksempel for bestemte ressourcer eller ressourcegrupper). Når du vælger denne knap, modtager alle brugere, der er ansvarlige for en ressource, der er relateret til den valgte produktionsordre, derfor en ændringsbesked.
    - **Giv klargører besked** – Denne knap er kun tilgængelig under fanen **Indkøbsrekvisition**. Markér den for at sende en ændringsbesked til den bruger, der er angivet som klargører for den valgte indkøbsrekvisition.
    - **Giv den salgsansvarlige besked** – Denne knap er kun tilgængelig under fanen **Tilbud**. Markér den for at sende en ændringsbesked til den bruger, der er angivet som ansvarlig for det valgte tilbud.
    - **Kassér** – Denne knap er kun tilgængelig under fanen **Lager**. Markér den for at angive kassere det valgte lager.
    - **Vis historik** – Åbn en historik over handlinger, der er udført på den valgte transaktion, ved at bruge dialogboksen **Forretningskonsekvenser for åbne transaktioner**. Historikken viser for eksempel, om der er sendt beskeder, eller om transaktioner er blevet blokeret. 
    - **Vis alle transaktioner** – Åbn den fulde liste over alle transaktioner, ikke kun de åbne transaktioner.

#### <a name="review-and-process-change-notifications-for-transactions"></a>Gennemse og behandle ændringsbeskeder for transaktioner

Du kan læse og behandle de ændringsbeskeder, du modtager, på følgende måder:

- Medmindre der er tale om produktionsordrer, vises ændringsbeskeder for de transaktioner, du er ansvarlig for, i handlingscenter. Knappen **Vis meddelelser** (klokkesymbol) i højre side af navigationslinjen angiver, hvornår en meddelelse er tilgængelig for dig i handlingscenteret. Vælg knappen **Vis meddelelser** for at åbne handlingscenteret og gennemse meddelelserne.
- Hvis du vil have vist alle produktionsordrer, som en teknisk besked er sendt for, skal du gå til **Produktionsordrer \> Produktionsordrer \> Alle produktionsordrer**. I handlingsruden under fanen **Produktionsordre** skal du derefter vælge **Tekniske beskeder** i gruppen **Teknisk ændringsanmodning** for at åbne siden **Tekniske beskeder**.
- I forbindelse med produktionsordrer kan du vælge kun at gennemse de ændringsbeskeder, der gælder for de produktionsressourcer, du administrerer. I arbejdsområdet **Administration af produktion** i handlingsruden skal du vælge **Konfigurer mit arbejdsområde** for at filtrere siden, så der kun vises oplysninger om de produktionsenheder, grupper og/eller ressourcer, du administrerer. I sektionen **Oversigt** viser et felt med navnet **Produktionsordrer med ændrede produkter** en optælling over beskeder, der opfylder dine filterindstillinger. Vælg dette felt for at åbne siden **Tekniske beskeder**, som viser den fulde liste over transaktioner, der opfylder kriterierne for dit filter.

Når du gennemser beskeder om produktionsordrer på siden **Tekniske beskeder**, kan du følge links til relaterede ændringsordrer eller produktionsordrer ved at vælge kolonneværdier eller bruge de relaterede kommandoer i handlingsruden. Når du er færdig med at evaluere en ændring, og når du har annulleret eller ændret produktionsordrer efter behov, kan du markere en besked som løst. Vælg beskeden, og vælg derefter **Løs** i handlingsruden. Beskeden fjernes fra alle brugeres visninger.

### <a name="create-a-change-order-from-a-change-request"></a>Oprette en ændringsordre ud fra en ændringsanmodning

En tekniker, der gennemgår en anmodning om teknisk ændring, kan oprette en teknisk ændringsordre direkte fra siden **Tekniske ændringsanmodninger**. Vælg **Kopiér link og produkter** i gruppen **Teknisk ændringsordre** under fanen **Ændringsanmodning** i handlingsruden.

## <a name="engineering-change-orders"></a>Tekniske ændringsordrer

Tekniske ændringsordrer giver strukturerede processer til foretagelse af ændringer i tekniske produkter. Du foreslår ændringer ved hjælp af en kopi af de teknisk relevante data. De egentlige masterdata påvirkes ikke. Du kan finde flere oplysninger om teknisk relevante data i [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

Du kan oprette en teknisk ændringsordre, der er baseret på en godkendt anmodning om teknisk ændring. Teknikere kan også oprette tekniske ændringsordrer fra bunden. Du kan medtage flere produkter på en enkelt teknisk ændringsordre ved at følge et af disse trin:

- Vælg produkter manuelt.
- Brug styklisten til at medtage produkter, der ligger lavt i produktstrukturen (dvs. underordnede).
- Brug en hvor er det brugt-søgning for at inkludere produkter, der ligger højt i produktstrukturen (dvs. overordnede).

Når forslaget til ændringer er fuldført, vil gennemsyns- og godkendelsesprocessen blive håndteret af en arbejdsproces. Du kan konfigurere forskellige arbejdsprocesser med udgangspunkt i prioritet og alvorsgrad.

Hvis du vil oprette en arbejdsproces til tekniske ændringsordrer eller tekniske ændringsanmodninger, skal du gå til **Teknisk ændringsstyring \> Tekniske arbejdsprocesser**. Vælg **Ny**, vælg, om arbejdsprocessen skal bruges til at gennemgå tekniske ændringsordrer eller anmodninger om teknisk ændring, og konfigurer derefter arbejdsprocessen.

Yderligere oplysninger om arbejdsprocesser finder du i [Oversigt over arbejdsgangssystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Her er nogle typiske interessenter, der måske skal godkende en teknisk ændringsordre:

- **Produktejere** – Du kan finde flere oplysninger om produktejere under [Produktejere](product-owner.md).
- **Ansvarlig teamleder** – I feltet **Tekniker** i **Overskrift**-visningen af den tekniske ændringsordre vises den tekniker, der oprettede den tekniske ændringsordre. Hvis teknikeren tilhører team, der er defineret i systemet, viser feltet **Ansvarlig** lederen af det pågældende team.
- **Økonomiafdeling** – Økonomiafdelingen skal muligvis gennemgå de sager, hvor ændringen omfatter høje omkostninger.

Du kan vælge, om den tekniske ændringsordre skal behandles direkte, når den er godkendt, som en del af arbejdsprocessen, eller om behandlingen skal udføres senere som et manuelt trin. Under behandlingen af en teknisk ændringsordre opdateres tekniske data på det faktiske produkt.

Mens du gennemgår en anmodning om ændring, skal du i handlingsruden under fanen **Ændringsanmodning** i gruppen **Forretningseffekt** vælge **Søg** for at vurdere effekten af den foreslåede ændring på åbne transaktioner, f.eks. salgsordrer, produktionsordrer og lagerbeholdning. Resultaterne vises i dialogboksen **Forretningskonsekvenser for åbne transaktioner**, hvor du kan vælge påvirkede transaktioner og derefter bruge kommandoerne på værktøjslinjen til at få vist flere oplysninger, give besked til den ansvarlige bruger eller blokere transaktionen.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Tekniske ændringsordrer i tekniske virksomheder eller driftsselskaber

Som det er beskrevet i [Tekniske virksomheder og regler for ejerskab af data](engineering-org-data-ownership-rules.md), varierer de produktdata, du kan redigere, afhængigt af den type juridiske enhed, du arbejder i (en teknisk virksomhed i forhold til et driftsselskab). Regler for ejerskab af data anvendes også på tekniske ændringsordrer. Derfor kan der foretages forskellige typer ændringer, afhængigt af den juridiske enhed, hvor du opretter en teknisk ændringsordre. Her er nogle eksempler:

- I forbindelse med tekniske ændringsordrer i et *teknisk virksomhed* kan du foretage grundlæggende ændringer af de tekniske data. Du kan f.eks. oprette nye versioner af et produkt, ændre et produkts struktur via styklisten og ændre dens tekniske attributværdier. Vælg en af følgende værdier i feltet **Effekt** for hvert berørt produkt:

    - **Ingen** – Opdater den eksisterende produktversion (i version-opdatering).
    - **Ny version** – Opret en ny version, der er baseret på den valgte produktversion.
    - **Nyt produkt** – Opret et helt nyt produkt, der er baseret på den valgte produktversion.
    - **Ny variant** – Opret en ny variant, der er baseret på den valgte produktversion. Dens stykliste- og ruteoplysninger kopieres.

- I forbindelse med tekniske ændringsordrer i et *driftsselskab* kan du ændre produktets logistiske data. Du kan f.eks. forbedre den eksisterende stykliste med indstillinger for forsyning, tilføje lokale ruter eller lokale styklister og endda forbedre en stykliste ved at tilføje nye styklistelinjer til lokale emballager, smørevæsker eller instruktioner på det lokale sprog. De forbedringer, som brugerne foretager i driftsselskabet, bevares, når der sendes nye opdateringer fra den tekniske virksomhed. Yderligere oplysninger finder du i [Tekniske virksomheder og regler for ejerskab af data](engineering-org-data-ownership-rules.md).

    Når der behandles tekniske ændringsordrer i den tekniske virksomhed, bliver produkterne kun oprettet og/eller opdateret i den tekniske virksomhed. Hvis produktmasterdataene også skal opdateres, skal du derfor også frigive produkterne til driftsselskaber.

- Du kan frigive produkter direkte fra tekniske ændringsordrer. Åbn ændringsordren, og vælg derefter **Frigiv produktstruktur** i gruppen **Produktfrigivelser** under fanen **Ændringsordre** i handlingsruden. Processen fungerer på samme måde, som når du frigiver produkter fra siden **Frigivne produkter**. Yderligere oplysninger finder du under [Frigive produktstrukturer](release-product-structure.md).
- Du kan få produkter frigivet automatisk ud fra tekniske ændringsordrer på baggrund af følgende faktorer:

    - Genudgivelser til virksomheder, hvor produkterne tidligere er blevet frigivet. Vælg **Søg** for at scanne alle tidligere frigivelser, og vælg derefter **Vis** for at få vist resultaterne. På siden **Vis** vises de tidligere produktudgivelser, og du kan vælge, hvilke produkter der skal genudgives. Luk derefter **Vis**-siden, og vælg **Proces** for at frigive de valgte produkter igen.
    - Automatiske versionsindstillinger i frigivelseskontrollen til den tekniske produktkategori. Du kan udføre denne frigivelse som en del af arbejdsprocessen. Når blokken **Hent frigivelsesforslag** bruges, fyldes frigivelsesforslaget med genudgivelsesforslag (se det foregående listeelement), og produkter vil blive frigivet til firmaer, hvis afkrydsningsfeltet **Frigiv automatisk** er markeret i frigivelseskontrollen for den tekniske produktkategori. Du kan vælge **Vis** for at få vist resultaterne som beskrevet i det forrige listeelement. Produkterne frigives også, når blokken **behandle frigivelsesforslag** anvendes. Hvis du kun vælger at hente frigivelsesforslaget som del af arbejdsprocessen, kan du starte frigivelsen manuelt ved at vælge **Proces**, som beskrevet i det forrige listeelement.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Følge op på en anmodning om teknisk ændring via en teknisk ændringsordre

Så snart en teknisk ændringsanmodning er godkendt, kan du følge op på den via en om teknisk ændringsordre. Du kan kombinere flere anmodninger om teknisk ændring i en enkelt teknisk ændringsordre. En enkelt teknisk ændringsordre kan også omfatte flere produkter. (Du bruger typisk denne fremgangsmåde, når den samme ændring skal anvendes på flere produkter). Du kan dog ikke oprette flere tekniske ændringsordrer ud fra en enkelt anmodning om en teknisk ændring.

Hvis du vil følge op på en anmodning om ændring via en ændringsordre, skal du åbne ændringsanmodningen og derefter vælge **Kopiér link og produkter** i gruppen **Teknisk ændringsordre** under fanen **Ændringsordre** i handlingsruden. Du kan derefter vælge en eksisterende teknisk ændringsordre, som ændringsanmodningen skal tilknyttes, eller du kan oprette en ny teknisk ændringsordre for den pågældende anmodning.

## <a name="engineering-change-order-report"></a>Rapport vedrørende tekniske ændringsordrer

I rapporter om teknisk ændringsordre beskrives de ændringer, der er foretaget i en teknisk ændringsordre. De er nyttige både under og efter gennemsyns- og godkendelsesprocessen.

Hvis du vil have vist en rapport over en teknisk ændringsordre, skal du åbne den relevante ændringsordre og derefter vælge **Rapport for teknisk ændringsordre** i gruppen **Vis** under fanen **Ændringsordre** i handlingsruden.

## <a name="fields-on-an-engineering-change-order"></a>Felter i en teknisk ændringsordre

De fleste af felterne på tekniske ændringsordrer er de samme som felterne for frigivne produkter, tekniske versioner, dokumenter, styklister (linjer) og ruter (operationer). Felterne i følgende tabel er dog kun til ændringsordrer.

| Felt | Beskrivelse |
|---|---|
| Årsager til den tekniske ændring | Vælg årsagen til, at det berørte produkt skal ændres. |
| Ændringsbeskrivelse | Angiv en beskrivelse af ændringen. |
| Krævet specialværktøj | Angiv, om der kræves specialværktøj for at anvende ændringen. |
| Fordeling af teknisk materiale | Vælg en materialedispositionskode for ethvert affald, der produceres, når ændringen anvendes. |
| Kundegodkendelse kræves | Angiv, om kundegodkendelse er påkrævet, før ændringen kan træde i kraft. |
| Modtagne kundegodkendelser | Angiv status for kundens godkendelse. |
| Miljø, sundhed og sikkerhed | Angiv, om miljøets tilstands- og sikkerhedsregler gælder for ændringen. Hvis de gør, kan du derefter vælge de relevante regler. |

Du kan bruge knappen **Vedligehold/kopiér ændringsoplysninger** til at kopiere ændringsoplysninger mellem berørte produkter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
