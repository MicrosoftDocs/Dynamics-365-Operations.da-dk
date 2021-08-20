---
title: Frigive produktstrukturer
description: I dette emne forklares det, hvordan du kan frigive hele produktstrukturer ud over at frigive produkter sammen med deres tekniske versioner. På denne måde kan du sikre dig, at teknisk relevante produktdata nemt kan genbruges i forskellige juridiske enheder.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 1134b24aa3f7ada72ba837b525d2cea33b3e6287da0f8611f60152672c1ee6f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743620"
---
# <a name="release-product-structures"></a>Frigive produktstrukturer

[!include [banner](../includes/banner.md)]

Hvis du vil sikre dig, at teknisk relevante produktdata nemt kan genbruges i forskellige juridiske enheder, kan du frigive hele produktstrukturer samt frigive produkter sammen med deres tekniske versioner. Derfor kan du frigive styklistestrukturer på flere niveauer sammen med den overordnede vare i en enkelt frigivelseshandling. Hvis det er tilfældet, frigives styklisten og produkterne på lavere niveau også.

Tekniske produkter oprettes og vedligeholdes af deres tekniske virksomhed på en sådan måde, at de opfylder kvalitetskravene, mens de designes. Hvert driftsselskab, der fremstiller et produkt, skal bruge samme produkt og underliggende stykliste. Afhængigt af produktionsanlægget kan ruten oprettes lokalt. I dette tilfælde kan du ikke frigive en rute sammen med produktet. For juridiske enheder, der sælger produkterne, men ikke producerer dem, er styklisten muligvis ikke påkrævet.

For at gøre processen mere effektiv kan alle teknisk relevante data frigives til andre driftsselskaber på samme tid. Disse data omfatter produktstrukturen. Under frigivelsesprocessen kan du vælge, hvilke dele af produktdataene der skal frigives.

Yderligere oplysninger om tekniske virksomheder og driftsselskaber finder du i [Tekniske virksomheder og regler for ejerskab af data](engineering-org-data-ownership-rules.md).

Bemærk, at du kan frigive både standardprodukter og tekniske produkter sammen med produktstrukturen. Under denne proces frigives hele produktstrukturen, også styklisten og ruten fra det firma, som produkterne frigives i.

Du kan se et eksempel på, hvordan du frigiver et produkt, under [Frigive et teknisk produkt til et lokalt firma](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Frigivne data for et produkt, når produktstrukturen for frigivelsen anvendes

Følgende data er inkluderet i frigivelsen af tekniske produkter:

- **Produktdata** – Der oprettes et nyt frigivet produkt.
- **Tekniske versionsdata** – Den tekniske version og de tilhørende data oprettes eller opdateres. Bemærk, at hvis du frigiver den samme tekniske version igen til et driftsselskab, vil de tekniske data blive overskrevet.
- **Tekniske attributter** – Tekniske attributter og deres værdier oprettes eller opdateres.
- **Teknisk styklist** – Den tekniske stykliste og de tilhørende linjer kan oprettes eller opdateres. Du kan finde flere oplysninger om dataejerskab under [Produktejere](product-owner.md).
- **Tekniske ruter** – Tekniske ruter og deres drift oprettes eller opdateres. Du kan finde flere oplysninger om dataejerskab under [Produktejere](product-owner.md).
- **Tekniske dokumenter** – Tekniske dokumenter, der er tilknyttet den tekniske version, oprettes eller opdateres.

Når du aktiverer styring af tekniske ændringer på systemet, er produktstrukturen for frigivelse tilgængelig. Derudover vil standardprodukter indeholde deres styklister og ruter, når de frigives.

## <a name="product-acceptance"></a>Produktgodkendelse

**Accept af produkt** er en nøgle parameter, der påvirker frigivelsesprocessen. Du kan angive denne parameter for hver virksomhed ved at gå til **Teknisk ændringsstyring \> Konfiguration \> Parametre for styring af tekniske ændringer**. Yderligere oplysninger finder du i [Parametre for styring af tekniske ændringer](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatisk accept af produkt

Hver frigivelse af tekniske produkter starter, når nogen fra den tekniske virksomhed vælger et produkt, der skal frigives. Når parameteren **Accept af produkt** er angivet til *Automatisk*, bestemmer brugeren i den tekniske virksomhed, hvilke produktdata der automatisk skal frigives til driftsselskabet. Produktet frigives derefter automatisk til de firmaer, der er valgt i frigivelsesguiden.

### <a name="manual-product-acceptance"></a>Manuel accept af produkt

Hver frigivelse af tekniske produkter starter, når nogen fra den tekniske virksomhed vælger et produkt, der skal frigives. Når parameteren **Accept af produkt** er angivet til *Manuel*, bestemmer brugeren i den tekniske virksomhed, hvilke produktdata der skal frigives til driftsselskabet. En bruger fra hvert driftsselskab gennemgår derefter produktdataene og beslutter, om frigivelsen skal accepteres. Brugeren i driftsselskabet kan angive følgende indstillinger, når dataene modtages:

- Hvis produkterne (opdateringerne) ikke er relevante for driftsselskabet, kan brugeren vælge ikke at acceptere frigivelsen.
- Brugeren kan ændre vareskabelonen for nye produkter.
- Brugeren kan vælge, om produktet skal frigives sammen med styklister og/eller ruter, og om det skal frigives som godkendt og aktivt.
- Brugeren kan ændre produktets ikrafttrædelsesdatoer.

Du kan se et eksempel på, hvordan du accepterer et produkt, under [Gennemse og acceptere produktet, før du frigiver det i det lokale firma](engineering-scenarios.md#accept).

> [!NOTE]
> For standardprodukter kan du frigive fra enhver juridisk enhed til en hvilken som helst anden juridiske enhed. I forbindelse med tekniske produkter er den eneste juridiske enhed, som du kan frigive fra, den tekniske virksomhed.

## <a name="release-policies"></a>Frigivelsespolitikker

Ikke alle driftsselskaber har brug for samme produktdata. Generelt skal driftsselskaber, der fremstiller tekniske produkter, kræve en stykliste, hvorimod et driftsselskab, der kun sælger tekniske produkter, ikke kræver en stykliste. Du kan bruge frigivelsespolitikker til at oprette de parametre, der bruges til frigivelse af produkter.

Du kan finde flere oplysninger om tekniske produktkategorier i [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

Under frigivelsesprocessen kan du have indflydelse på indstillingerne.

## <a name="create-and-manage-product-release-policies"></a>Oprette og administrere politikker for produktfrigivelse

Hvis du vil arbejde med produkters frigivelsespolitikker, skal du gå til **Styring af tekniske ændringer \> Konfiguration \> Politikker for produktfrigivelse**. Udfør derefter ét af følgende trin.

- Hvis du vil oprette en ny politik, skal du vælge **Ny** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil redigere en eksisterende politik, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil slette en eksisterende politik, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter kontrollere, at **Aktiv**-indstillingen er angivet til **Nej**, i oversigtspanelet *Generelt*. Vælg derefter **Slet** i handlingsruden.

### <a name="header"></a>Overordnet

Angiv følgende felter i overskriften på et produkts frigivelsespolitik.

| Felt | Beskrivelse |
|---|---|
| Navn | Angiv et navn til politikken. |
| Beskrivelse | Angiv en beskrivelse af politikken. |

### <a name="general-fasttab"></a>Oversigtspanelet Generelt

Angiv følgende felter i oversigtspanelet **Generelt** på et produkts frigivelsespolitik.

| Felt | Beskrivelse |
|---|---|
| Produkttype | Vælg, om politikken gælder for produkter af typen *Vare* eller *Service*. Du kan ikke ændre denne indstilling, når du har gemt posten. |
| Produktionstype | Dette felt vises kun, når du har aktiveret [administration af formelændringer](manage-formula-changes.md) i systemet. Vælg den produktionstype, som denne frigivelsespolitik gælder for:<ul><li>**Samprodukt** – Brug denne udgivelsespolitik til at administrere samprodukter. Samprodukter produceres under procesproduktion og er ikke versionsnummererede eller tekniske produkter. Frigivelsespolitikker for samprodukter kan være med til at sikre, at vigtige indstillinger, f.eks. **Lagringsdimensionsgruppe** og **Sporingsdimensionsgruppe**, er konfigureret ved hjælp af en skabelon til frigivet produkt, før de frigives til en virksomhed.</li><li>**Biprodukt** – Brug denne udgivelsespolitik til at administrere biprodukter. Biprodukter produceres under procesproduktion og er ikke versionsnummererede eller tekniske produkter. Frigivelsespolitikker for biprodukter kan være med til at sikre, at vigtige indstillinger, f.eks. **Lagringsdimensionsgruppe** og **Sporingsdimensionsgruppe**, er konfigureret ved hjælp af en skabelon til frigivet produkt, før de frigives til en virksomhed.</li><li>**Ingen** – Brug denne politik til at administrere standardprodukter, der ikke er versionsnummererede eller tekniske produkter, samprodukter eller biprodukter.</li><li>**Planlægningsvare** – Brug denne frigivelsespolitik til at administrere planlægningsvarer, der produceres ved hjælp af procesproduktion. Planlægningsvarer bruger formler. De ligner formelvarer, men de bruges kun til at producere samprodukter og biprodukter, ikke færdige produkter.</li><li>**Stykliste** – Brug denne frigivelsespolitik til at administrere tekniske produkter, som ikke bruger formler og typisk (men ikke nødvendigvis) indeholder styklister.</li><li>**Formel** – Brug denne frigivelsespolitik til at administrere færdige varer, der produceres ved hjælp af procesproduktion. Disse varer har en formel, men ikke en stykliste.</li></ul> |
| Anvend skabeloner | Vælg en af følgende indstillinger for at angive, om og hvordan produktfrigivelsesskabeloner skal anvendes, når politikken bruges:<ul><li>**Altid** – Et skabelonfrigivet produkt skal altid bruges til frigivelser. Hvis du vælger denne indstilling, skal du bruge oversigtspanelet **Alle produkter** til at angive den skabelon, der skal bruges til hvert af de firmaer, du frigiver til. Hvis du ikke angiver en skabelon for hvert af de firmaer, der vises i oversigtspanelet **Alle produkter**, vil du modtage en fejl, når du forsøger at gemme politikken.</li><li>**Valgfri** – Hvis der er angivet et skabelonfrigivet produkt for et firma, der er angivet i oversigtspanelet **Alle produkter**, vil den pågældende skabelon blive brugt, når du frigiver til det pågældende firma. Ellers vil der ikke blive anvendt en skabelon. Hvis du vælger denne indstilling, kan du gemme politikken uden at tildele skabeloner til alle firmaer. (Der vises ingen advarsel).</li><li>**Aldrig** – Der bruges intet skabelonfrigivet produkt for noget firma, du frigiver til, selvom en skabelon er angivet for firmaer i oversigtspanelet **Alle produkter**. Skabelonkolonnerne vil ikke være tilgængelige.</li></ul> |
| Aktive | Brug denne indstilling som en hjælp til at vedligeholde dine frigivelsespolitikker. Angiv *Ja* for alle de frigivelsespolitikker, du bruger. Angiv den til *Nej* for at markere en frigivelsespolitik som inaktiv, når den ikke bruges. Bemærk, at du ikke kan inaktivere en frigivelsespolitik, der er tildelt en teknisk produktkategori, og du kan kun slette inaktive frigivelsespolitikker. |

### <a name="all-products-fasttab"></a>Oversigtspanelet Alle produkter

I oversigtspanelet **Alle produkter** skal du tilføje en række for hvert driftsregnskab, du vil bruge denne politik til at frigive til. Brug knapperne i oversigtspanelet **Alle produkter** til at tilføje og fjerne rækker efter behov. For hver række, du tilføjer, skal du angive følgende felter.

> [!NOTE]
> Indstillingerne i oversigtspanelet **Alle produkter** gælder for både tekniske produkter og standardprodukter.

| Felt | Beskrivelse |
|---|---|
| Regnskabs-id | Vælg det regnskabsfirma, som rækken gælder for. Parametrene på rækken gælder, når produkter frigives til dette firma. |
| Frigivet skabelonprodukt | Tilføj en skabelon for produktet. |
| Kopiér godkendelse af stykliste | Markér dette afkrydsningsfelt for at kopiere status for styklistegodkendelse til modtagerfirmaet. |
| Kopiér aktivering af stykliste | Markér dette afkrydsningsfelt for at kopiere status for styklisteaktivering til modtagerfirmaet. |
| Kopiér rutegodkendelse | Markér dette afkrydsningsfelt for at kopiere status for rutegodkendelse til modtagerfirmaet.|
| Kopiér ruteaktivering | Markér dette afkrydsningsfelt for at kopiere status for ruteaktivering til modtagerfirmaet. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Oversigtspanelet Indstillingsparametre for tekniske produkter

Hver gang du tilføjer en række i oversigtspanelet **Alle produkter**, oprettes der også en række, der har en tilsvarende **Regnskabs-id**-værdi, på i oversigtspanelet **Indstillingsparametre for tekniske produkter**. Hvis du derefter fjerner en række fra oversigtspanelet **Alle produkter**, vil den række, der har en tilsvarende **Regnskabs-id**-værdi, også blive fjernet fra oversigtspanelet **Indstillingsparametre for tekniske produkter**.

For hver række, der vises i oversigtspanelet **Indstillingsparametre for tekniske produkter**, skal du angive følgende felter.

> [!NOTE]
> Indstillingerne i oversigtspanelet **Indstillingsparametre for tekniske produkter** gælder kun for tekniske produkter.

| Felt | Beskrivelse |
|---|---|
| Styklisteskabelon | Når der frigives et produkt, der har en stykliste, vil linjerne i den angivne skabelonstykliste blive tilføjet. Dette felt er nyttigt til tilføjelse af lokale komponenter, f.eks. pakning eller vejledning på det lokale sprog. |
| Skabelonrute | Når der frigives et produkt, der har en rute, vil linjerne i den angivne skabelon blive tilføjet. |
| Kopiér gyldighedsdato | Vælg, om gyldighedsdatoer skal kopieres fra det tekniske firma til driftsselskabet, når du frigiver produkter. |
| Automatisk forslag om tilføjelse til frigivelse | Markér dette afkrydsningsfelt for produkter, der automatisk skal frigives i den tekniske ændringsordre. På denne måde kan produkter, der tilhører tekniske produktkategorier, der bruger denne frigivelsespolitik, automatisk frigives til driftsselskaber, hvor denne indstilling er konfigureret. (Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md)).

### <a name="review-each-product-when-you-release-it"></a>Gennemse hvert produkt, når du frigiver det

Når tekniske produkter, der har styklister eller ruter, frigives, angives parametrene til standardværdierne som angivet i frigivelsespolitikken. Som bruger kan du påvirke denne funktionsmåde på frigivelsessiden, når du bruger produktstrukturen for frigivelse.

Hvis du vil frigive tekniske produkter, skal du vælge de produkter, der skal frigives, på siden **Frigivne produkter** og derefter vælge **Frigiv produktstruktur** for at åbne guiden Frigiv. På siden **Vælg tekniske produkter, der skal frigives** vises produkterne. Vælg et enkelt produkt, og vælg derefter **Frigiv detaljer** for at gennemgå produktets frigivelsesoplysninger.

På siden **Frigiv detaljer** kan du ændre værdien af felterne **Modtag stykliste**, **Kopiér styklistegodkendelse**, **Kopiér styklisteaktivering**, **Modtag rute**, **Kopiér rutegodkendelse** og **Kopiér ruteaktivering**. I push-pull-scenariet kan du ændre værdien af de samme felter på den modtagende side, hvis styklisten og ruten er frigivet.

## <a name="product-owners-and-product-releases"></a>Produktejere og produktfrigivelser

Da produktejere ved, hvilke juridiske enheder der har brug for deres produkter, kan et produkt kun frigives af medlemmerne af det pågældende produkts produktejergruppe. Andre brugere kan ikke frigive produkter, som de ikke ejer.

Denne situation gælder kun, når et produkt er valgt direkte til frigivelse. Produkter, der indgår i et andet produkts struktur via en stykliste, *kan* frigives af brugere, der ikke er ejer, når de frigiver det overordnede produkt, hvis de ejer det overordnede produkt.

Produkt X tildeles f.eks. produktejergruppen *Design skabe*. Produkt X er også en del af styklisten for produkt Y, som er knyttet til produktejergruppen *Design højttalere*. Hvis en bruger fra *Design højttalere*-produktejergruppen frigiver produkt Y og dets stykliste, frigives produkt X sammen med produkt Y.

Du kan finde flere oplysninger under [Produktejere](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
