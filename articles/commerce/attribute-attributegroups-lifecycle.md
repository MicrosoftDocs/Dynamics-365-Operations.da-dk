---
title: Styring af attributter og attributgrupper
description: Denne artikel beskriver, hvordan du administrerer attributter og attributgrupper, så produkterne og deres karakteristika beskrives i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386966"
---
# <a name="manage-attributes-and-attribute-groups"></a>Styring af attributter og attributgrupper

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du administrerer attributter og attributgrupper, så produkterne og deres karakteristika beskrives i Microsoft Dynamics 365 Commerce.

Med *Attributter* kan du beskrive et produkt og dets egenskaber via brugerdefinerede felter. Det kan f.eks. være hukommelsesstørrelse, harddiskkapacitet og overholdelse af Energy Star.

Attributter kan være tilknyttet forskellige Commerce-enheder, såsom produktkategorier og -kanaler, og du kan angive standardværdier for dem. Produkter arver derefter attributterne og standardværdierne, når de bliver knyttet til produktkategorierne eller kanalerne. Standardværdierne for attributter kan tilsidesættes på hvert enkelt produktniveau i kanalniveauet eller i et katalog.

Et typisk tv-produkt kan f.eks. have følgende attributter.

| Kategori   | Egenskab           | Tilladte værdier                        | Standardværdi |
|------------|---------------------|-------------------------------------------|---------------|
| Tv og video | Brand               | Alle gyldige mærkeværdier                     | Ingen          |
| TV         | Skærmstørrelse         | 20-85 tommer                              | 55 tommer     |
|            | Lodret opløsning | 4K (2160p), Fuld HD (1080P) eller HD (720p) | 4K (2160p)    |
|            | Skærmens opdateringshastighed | 60 Hz, 120 Hz eller 240 Hz                     | 60 Hz          |
|            | HDMI-inputs         | 0-10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Attributter og attributtyper

Attributterne baseres på *attributtyper*. Attributtypen identificerer den type data, der kan angives for en bestemt attribut. Følgende attributtyper understøttes i Commerce:

- **Valuta** – Denne type understøtter en valutaværdi. Den kan være afgrænset (dvs. den kan understøtte et værdiinterval), eller den kan være åben.
- **DateTime** – Denne type understøtter en dato- og klokkeslætsværdi. Den kan afgrænses eller være åben.
- **Decimal** – Denne type understøtter en numerisk værdi, der indeholder decimalpladser. Den understøtter også en måleenhed. Den kan afgrænses eller være åben.
- **Heltal** – Denne type understøtter en numerisk værdi. Den understøtter også en måleenhed. Den kan afgrænses eller være åben.
- **Tekst** – Denne type understøtter en tekstværdi. Det understøtter også et foruddefineret sæt mulige værdier, når indstillingen **Fast liste** er aktiveret.
- **Boolesk** – Denne type understøtter en binær værdi (**sand** eller **falsk**).
- **Reference** – Denne type refererer til andre attributter.

> [!NOTE]
> På grund af [begrænsningerne i Azure-søgeindekset](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) understøttes **Decimal-attributtypen** ikke for skydrevne søgeerfaringer. Azure Cognitive Search understøtter ikke konvertering af **decimalattributtyper** til felttyperne **Edm.Double**-destinationsindeks, da denne konvertering ville reducere præcisionen.

### <a name="set-up-attribute-types"></a>Konfigurer attributtyper

Hvis du vil konfigurere attributtyper, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Administration af produktoplysninger \> Opsætning \> Kategorier og attributter \> Attributtyper**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Attributtypen** angives **Tasketype**.
1. Vælg **Tekst** i feltet **Type**.
1. Angiv indstillingen **Fast liste** til **Ja**.
1. Vælg **Tilføj** i oversigtspanelet **Værdier**.
1. I den nye række skal du i feltet **Værdi** angive **Taske**.
1. Tilføj fem rækker mere. I **værdifeltet** for de enkelte værdier skal du angive en anden værdi: **Håndtaske**, **Pung**, **Rygsæk**, **Messenger-taske** eller **Tegnebog**.
1. Vælg **Gem** i handlingsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Attributtypen** angives **solbrillemærke**.
1. Vælg **Tekst** i feltet **Type**.
1. Angiv indstillingen **Fast liste** til **Ja**.
1. Vælg **Tilføj** i oversigtspanelet **Værdier**.
1. I den nye række skal du i feltet **Værdi** angive **Ray Ban**.
1. Tilføj to rækker mere. Angiv en anden værdi i feltet **Værdi** i hver af dem: **Aviator** eller **Oakley**.
1. Vælg **Gem** i handlingsruden.

![Attributtyper-side.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Konfigurer en attribut

Hvis du vil konfigurere en attribut, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Administration af produktoplysninger \> Opsætning \> Kategorier og attributter \> Attributter**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Navn** skal du skrive **Tasketype**.
1. I feltet **Attributtypen** angives **Tasketype**.
1. Vælg **Gem** i handlingsruden.

![Attributter-side.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Attributmetadata

I *Attributmetadata* kan du vælge indstillinger for at angive, hvordan attributterne for hvert produkt skal fungere. Du kan f.eks. angive, om attributter er påkrævede, om de kan bruges til søgninger, og om de kan bruges som filter.

For produkter kan metadataattributindstillingerne tilsidesættes på kanalniveau.

Som du har muligvis bemærket, indeholder siden **Attributter** flere indstillinger, der vedrører attributmetadata. Hvis du f.eks. angiver indstillingen **Kan redigeres** til **Ja** under **Attributmetadata til Commerce-kanaler**, vises attributten med henblik på redigering eller filtrering af produkter på søgeresultater og gennemsøgningssider for kategorier. Hvis du vil konfigurere en attribut, der kan redigeres, skal du først vælge **Filterindstillinger** i Handlingsruden og derefter bekræfte filterindstillinger til attributten.

## <a name="filter-settings-for-attributes"></a>Filterindstillinger for attributter

Med filterindstillinger for attributter kan du definere, hvordan filtrene for attributter vises i POS. Du kan få adgang til filterindstillingerne for en attribut ved at vælge attributten på siden **Attributter** og derefter vælge **Filterindstillinger** i handlingsruden.

Siden **Filterindstillinger** indeholder følgende felter:

- **Navn** – Dette felt er som standard indstillet til navnet på attributten. Du kan imidlertid ændre værdien.
- **Visningsindstilling** – Der er følgende tilgængelige indstillinger:

    - **Enkelt værdi** – Denne indstilling er tilgængelig for følgende attributtyper: **Boolesk**, **Valuta**, **Decimal**, **Heltal** og **Tekst**. Den giver kun mulighed for at markere en enkelt værdi for afgrænsninger på produktlistesider, f.eks. gennemsøgning af kategorier og sider med produktsøgningsresultater.
    - **Flere værdier** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal**, **Heltal** og **Tekst**. Med denne indstilling kan du vælge flere værdier for denne attribut, som du vil forbedre, i klienten.

- **Vis kontrolelement** – Der er følgende tilgængelige indstillinger:

    - **Liste** – Denne indstilling er tilgængelig for alle attributtyper.
    - **Afgrænsning** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.
    - **Skyder** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.
    - **Skyder med søjler** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.

- **Grænseværdi** – Denne indstilling er nødvendig, hvis du valgte **Interval** som visningskontrolelementtype. Du kan angive værdier ved hjælp af et semikolon (;) som afgrænser.

    For en attribut for **Taskerumfang**, der har attributtypen **Heltal** kan grænseværdien være **10; 20; 50; 100; 200; 500; 1000; 1000; 5000**. I dette tilfælde indeholder POS følgende intervaller. Intervaller, der ikke har nogen produkter i resultatet, vises nedtonet.

    - Mindre end 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eller derover

Filterindstillinger for attributter gælder kun for produktattributter og kan bruges til at forfine resultaterne af gennemsøgning af produkter og kategorier. De gælder ikke for kundesøgning eller ordresøgning, men de samme attributter kan bruges til at hjælpe kunder eller bestillingsoplysninger.

I standardmodulerne til Commerce er der ingen standardunderstøttelse til **Vis kontrolelement**-filterindstillinger som f.eks. **Område**, **Skyder** og **Skyder med søjler**. Indstillingerne for **Område** og **Skyder** understøttes fortsat for POS-løsninger, mens indstillingen **Skyder med søjler** er tilgængelig for ældre SharePoint online udstillingsvinduer og fortsat er tilgængelige for tredjepartsintegration og tilpassede scenarier.

Det anbefales, at foruddefinerede attributter har en attribut af typen **Tekst**, hvor indstillingen **Fast-liste** er aktiveret, og at du holder listen overskuelig (op til 100-200 entydige værdier). Hvis en afgrænsningerne har 1.000 eller flere entydige værdier, er det mere passende at bruge en attribut af typen **Tekst**, hvor indstillingen **Fast-liste** er deaktiveret.

Oversættelser er vigtige for attributnavne og deres værdier. For attributter af typen **Tekst**, hvor indstillingen **Fast-liste** er aktiveret, kan du definere oversættelser for attributværdierne under **Attributtype**. For hver anden attributtype kan du definere oversættelser på den side, hvor du definerer attributværdierne. For en attribut af typen **Tekst** kan du f.eks. definere oversættelser for standardværdien på attributtens attributside **Attributter**. Men hvis du tilsidesætter standardværdien på produktniveau, kan du definere oversættelser for attributten på siden **Produktattributter** for produktet.

Når en attribut er markeret som foruddefineret for en kanal, skal du ikke opdatere attributtypen. Ellers påvirker du publiceringen af produktdata til søgeindekset. Det anbefales i stedet, at du opretter en ny attribut til en ny type afgrænser og trækker den forrige attribut tilbage ved at fjerne den fra andre attributgrupper.

Søg efter attributter understøttes, men henter kun resultater for nøjagtige forekomster af søgeord. En **materialeattribut** har f.eks. værdien **Cashmere-bomuld**. Hvis en kunde søger efter "Kontant", hentes der ingen produkter, der har **Cashmere-bomuld** som materiale. Men hvis en kunde søger efter "Cashmere," "Bomuld" eller "Cashmere Bomuld", hentes de produkter, der har **Cashmere-bomuld** som materiale.

### <a name="additional-attribute-metadata-options"></a>Ekstra indstillinger for attributmetadata

> [!NOTE]
> Disse indstillinger for attributmetadata gælder kun for ældre SharePoint online udstillingsvindue og ekstern integration. Du kan finde flere oplysninger om disse attribut-metadataindstillinger under [Oversigt over søgeskemaet i SharePoint Server 2013](/SharePoint/search/search-schema-overview).

Følgende yderligere indstillinger for attributmetadata er også tilgængelige på siden **Attributter**:

- Søgbar
- Kan hentes
- Kan forespørges
- Sorterbar
- Ignorer bogstavstørrelse og format
- Komplet match

Disse indstillinger var oprindeligt beregnet til at forbedre søgefunktion for ældre SharePoint-baserede online udstillingsvinduer. De gælder ikke nødvendigvis for Commerce e-handelswebsteder eller POS-terminaler. Da konsolløs integration fortsat understøttes, er disse indstillinger tilgængelige for eksport af attributmetadata ved hjælp af SDK (Commerce software development kit). Du kan bruge Commerce SDK til at placere produkter i et brugerdefineret, optimeret eksternt søgeindeks. På denne måde kan du sikre dig, at det kun er attributter, der skal indekseres, der indekseres.

## <a name="attribute-groups"></a>Attributgrupper

En *attributgruppe* bruges til at gruppere de individuelle attributter for en komponent eller en underkomponent i en produktkonfigurationsmodel. En attribut kan medtages i mere end en attributgruppe. Attributgrupper kan hjælpe brugerne med at konfigurere produkter, fordi de forskellige valgmuligheder er arrangeret i en bestemt kontekst. Attributgrupper kan tildeles til kategorier eller kanaler. Du kan også angive standardværdier for attributter i en attributgruppe.

![Attributgrupper-side.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Oprette en ny attributgruppe

Hvis du vil oprette en attributgruppe, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Administration af produktoplysninger \> Opsætning \> Kategorier og attributter \> Attributgrupper**.
1. Opret en attributgruppe, der hedder **Moderigtige skjorter**.
1. Tilføj følgende attributter: **CleaningMethod**, **CollarType**, **Samling** og **Design.**

> [!NOTE]
> Visningsordreværdierne for attributter i attributgruppen har ingen indflydelse på eller gælder for rækkefølgen af afgrænsningsgrupper i resultaterne for søgning og kategorisøgning. De gælder kun for scenariet "ordreattributter".

### <a name="assign-attribute-groups-to-categories"></a>Tildele attributgrupper til kategorier

En eller flere attributgrupper kan tilknyttes kategorinoder i følgende typer kategorihierarkier:

- Produkthierarki for handel
- Navigationshierarki for kanal
- Supplerende hierarkiprodukter efter kategori

Når produkter kategoriseres i kategorier, der er knyttet til attributgrupper, arver de de attributter, der er inkluderet i disse attributgrupper.

![Oversigtspanelet Produktattributgrupper på siden Commerce-produkthierarki.](media/AGRetailProdHierarchy_2022Series.png)

Følg disse trin for at tildele attributgrupper til kategorierne i Commerce-produkthierarkiet.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Detail og handel \> Produkter og kategorier \> Commerce-produkthierarki**.
1. Vælg **Mode**-navigationshierarki.
1. Under **Herretøj** skal du vælge kategorien **Bukser** og derefter i oversigtspanelet **Produktattributgrupper** tilføje en attributgruppe med navnet **Bælter til mænd**.
1. Vælg kategorien **Moderigtige solbriller**, og kontroller de nye attributter i attributgruppen **Modesolbriller** ved at vælge **Vis attributter**. Attributgruppen skal vise de nye attributter **Linseform** og **Solbrillemærke**.
1. Vælg kategorien **Bukser**, og kontroller attributterne for attributgruppen **Bælter til mænd** ved at vælge **Vis attributter**. Attributgruppen skulle vise attributterne **Bæltemærke, mænd**, **Bæltemateriale** og **Bæltestørrelse**.

Den samme basisprocedure kan også bruges til at tildele attributgrupper til kategorier i kategorihierarki for kanalnavigation og supplerende produktkategorihierarki. I trin 2 skal du dog bruge en af følgende stier, afhængigt af det hierarki, du vil tildele attributgrupper til:

- **Kategorihierarki for kanalnavigation:** Gå til **Detail og Commerce \> Kategori- og produktstyring \> Kanalnavigationskategorier**.
- **Supplerende produktkategorihierarki:** Gå til **Detail og Commerce \> Kategori- og produktstyring \> Supplerende produktkategorier**.

> [!NOTE]
> Kontrollér, at du kun tilknytter attributgrupper i et kategorihierarki i oversigtspanelet **Produktattributgrupper**, og ikke i oversigtspanelet **Kategoriattributværdier**. Hvis der vises attributter i oversigtspanelet **Kategoriattributværdier**, skal du vælge **Rediger kategorihierarki** i handlingsruden. Vælg derefter kategorinoderne i oversigtspanelet **Kategoriattributgrupper**, og vælg **Fjern**. Der er ingen understøttelse af, at du henter attributter efter kategori via Commerce Scale Unit.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Identificer tilgængelige og foruddefinerede attributter for handelskanaler til standardproduktsamlingen

Når du har knyttet forskellige attributgrupper til kategorier i forskellige hierarkier (handelsprodukthierarki eller kanalnavigationskategorier) og definerede attributværdier for hvert produkt på baggrund af kategoritilknytninger, skal du aktivere **showattributten på kanalflaget** for at gøre disse attributter kan vises i en bestemt kanal.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg **Angiv attributmetadata**, og vælg derefter en attribut i venstre rude.
1. I oversigtspanelet **Kanalproduktattributter** (ikke i oversigtspanelet **Kategoriattributter**) skal du angive indstillingen **Vis attribut på kanal** til **Ja** for at gøre attributten synlig.
1. Hvis du også vil have, at attributten skal kunne defineres, kan du angive indstillingen **Kan redigeres** til **ja**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Kontrollere synligheden af dimensionsbaserede afgrænsninger, f.eks. størrelse, typografi og farve

Produktdimensioner, f.eks. størrelse, typografi og farve, er de mest almindelige afgrænsninger. Hvis du vil gøre disse produktdimensioner tilgængelige som afgrænsninger, skal du tilknytte en attributgruppe på kanalniveau, der indeholder en reference til en attributtype, der automatisk arver værdier fra produktdimensionsværdier.

Du kan angive, at produktdimensioner skal kunne vises og defineres ved at opdatere flag på siden **kanalkategorierne og produktattributter**. Vælg rodnoden i navigationsruden, og indstil derefter attributten **Vis attribut på kanal** til **Ja** for attributterne **Størrelse**, **Typografi** og **Farve** i oversigtspanelet **Kanalproduktattributter**. Hvis du vil have, at disse attributter skal kunne defineres, kan du angive indstillingen **Kan redigeres** til **ja** for alle.

![Angive attributmetadata til dimensionsjustere.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Hvis du vil aktivere attributterne, så de er tilgængelige i den demo-databaserede Houston-kanal, skal du følge trinnene i dette eksempelprocedure.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg **Houston** kanalen.
1. I handlingsruden skal du vælge **Angiv attributmetadata**.
1. Vælg kategorinoden **Mode**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter** for hver attribut.
1. Vælg kategorinoden **Modetilbehør**, vælg kategorien **Moderigtige solbriller**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter for hver attribut**.
1. Vælg kategorinoden **Herretøj**, vælg kategorien **Bukser**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter for hver attribut**.
1. Når du har opdateret attributmetadataene for de ønskede attributter og afgrænsningerne, skal du sikre dig, at du gemmer ændringerne og kører jobbet **Publicer kanalopdateringer**. Når opdateringerne derefter er publiceret, skal du køre følgende job: **1070** (**Kanalkonfiguration**), **1040** (**produkter**) og **1150** (**katalog**).

> [!NOTE]
> - Hvis din virksomhed kræver, at du ofte tilføjer eller fjerner produkter i navigationshierarkiet, eller at du foretager ændringer, som f.eks. opdatering af visningsordreværdier, tilføjelse af nye kategorier og tilføjelse af nye attributgrupper til kategorier, anbefales det, at du konfigurerer jobbet **Udgiv kanalopdateringer**, der skal køres som et ofte forekommende batchjob. Alternativt kan du udløse jobbet **publicering af kanalopdateringer** og derefter følgende Commerce Data Exchange (CDX)-jobs: **1070** (**Kanalkonfiguration**), **1040** (**produkter**) og **1150** (**katalog)**.
> - Der vises en **Arv**-indstilling, hvor du kan angive, at denne kanal skal arve attributgrupperne fra sin overordnede kanal i hierarkiet. Hvis du vælger **Ja** i indstillingen **Arv**, arver den underordnede kanalnode alle attributgrupper og alle attributter i disse attributgrupper.
> - Hvis knappen **Angiv attributmetadata** i handlingsruden ikke er tilgængelig, skal du kontrollere, at **navigationshierarkiet** er knyttet til din kanal i oversigtspanelet **Generelt**.
> - Du må ikke tilknytte nogen attributgrupper undtagen dimensionsbaserede attributgrupper på et kanalniveau (f.eks. under **attributgrupper** på siden **Kanalkategorier og produktattributter**).
> - Efter introduktionen af understøttelse af kundespecifikke B2B-kataloger (business-to-business) i Commerce version 10.0.27 forventede du at identificere opsætningerne af afgrænsning og attribut for hvert B2B-katalog på samme måde, som det beskrives i denne artikel.

## <a name="override-attribute-values"></a>Tilsidesætte attributværdier

Standardværdierne for attributter kan tilsidesættes for individuelle produkter på produktniveau. Standardværdierne kan også tilsidesættes for individuelle produkter i specifikke kataloger, der er målrettet specifikke kanaler.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Tilsidesætte attributværdierne for et enkelt produkt

Hvis du vil tilsidesætte attributværdierne for et enkelt produkt, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Detail og Commerce \> Kategori og produktstyring \> Frigivne produkter efter kategori**.
1. Vælg **Mode \> Modetilbehør \> Modesolbriller**.
1. Vælg det påkrævede produkt i gitteret. Vælg derefter **Produktattributter** i gruppen **Konfigurer** under fanen **Produkt** i handlingsruden.
1. Vælg en attribut i venstre rude, og opdater derefter dens værdi i højre rude.

![Side med værdier for produktattribut.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Tilsidesætte attributværdierne for alle produkter i et katalog

Hvis du vil tilsidesætte attributværdierne for alle produkter i et katalog, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Detail og Commerce \> Administration af kataloger \> Alle kataloger**.
1. Vælg **Fabrikam Base Catalog**-kataloget.
1. Vælg **Mode \> Modetilbehør \> Modesolbriller**.
1. I oversigtspanelet **Produkter** skal du vælge det krævede produkt og derefter vælge **Attributter** over produktgitteret.
1. Opdater værdierne for de påkrævede attributter i følgende oversigtspaneler:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Tilsidesætte attributværdierne for alle produkter i en kanal

Hvis du vil tilsidesætte attributværdierne for alle produkter i en kanal, skal du følge trinnene i dette eksempel.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg **Houston** kanalen.
1. I oversigtspanelet **Produkter** skal du vælge det krævede produkt og derefter vælge **Attributter** over produktgitteret.
1. Hvis der ikke findes nogen produkter, kan du tilføje produkter ved at vælge **Tilføj** i oversigtspanelet **Produkter** og derefter vælge de ønskede produkter i dialogboksen **Tilføj produkter**.
1. Opdater værdierne for de påkrævede attributter i følgende oversigtspaneler:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Definer variantspecifikke attributværdier, og definer flere værdier for produktattributter

Hvis du vil definere variantspecifikke attributværdier og definere flere værdier for produktattributter, skal du følge trinnene i dette eksempelprocedure.

1. Log på Commerce Headquarters som markedsføringschef.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg **Houston** kanalen.
1. I oversigtspanelet **Produkter** skal du vælge den krævede produktvariant og derefter vælge **Attributter** over produktgitteret.
1. Hvis der ikke findes nogen produkter, kan du tilføje produkter ved at vælge **Tilføj** i oversigtspanelet **Produkter** og derefter vælge de ønskede produktvarianter i dialogboksen **Tilføj produkter**.
1. Opdater værdierne for de påkrævede attributter i følgende oversigtspaneler:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

#### <a name="example-of-variant-specific-attribute-configuration"></a>Eksempel på variantspecifik attributkonfiguration
        
I dette eksempel er **P001-Master**-produktet et multiplum af aktiviteter med tre varianter: **Løb**, **Gang** og **Trekking**. For hver variant skal du definere værdien af **aktivitetsattributten** entydigt. I oversigtspanelet **Produkter** i **kanalkategorier og produktattributter** for din kanal definerer du **aktivitetsattributværdien** for varianterne, som vist i følgende tabel.

| Variant     | Aktivitetsattributværdi |
|-------------|--------------------------|
| P001-Master | Sport                   |
| P001-1      | Kører                  |
| P001-2      | Gå                  |
| P001-3      | Trekking                 |

Hvis en bruger søger efter "sko", vises **P001-Master-produktet** i søgeresultaterne. Hvis du har konfigureret **aktivitetsattributten** som foruddefineret, viser **Aktivitetsafgrænsning** kun **Sport** som en værdi, der kan defineres, da denne værdi blev defineret for **aktivitetsattributten** på produktniveau **P001-Master**.

Attributter på variantniveau er som standard beregnet til kun at blive brugt på sider med produktdetaljer. Når du vælger en bestemt produktvariant til en PDP, opdateres produktspecifikationerne på den pågældende PDP for den pågældende variant.

Hvis afgrænsninger skal hente attributværdier, der er defineret på produktvariantniveau, skal du definere en attribut på produktmasterniveau, markere afkrydsningsfeltet **Tillad flere værdier** og angive attributtypen til **Tekst**.

Derefter skal du fastsætte alle mulige værdier for dine produktvarianter. For den **aktivitetsattribut**, der bruges i dette eksempel, kan de mulige værdier være **Løbende**, **Gang**, **Hiking**, **Trekking**, **Camping**, **Vandsport** eller **Vintersport**.

Når du har bestemt, hvad variantattributværdierne skal være, kan du definere dem på produktmasterniveau ved at bruge rørseparerede værdier. For **aktivitetsattributten** kan du definere attributværdien i produktmasteren som **Løb|Gang|Hiking|Trekking|Camping|vandsport|Vintersport**.

Derefter kan du for hver variant definere attributværdier ved at angive enten rørseparerede værdier eller enkelte værdier. For **aktivitetsattributten** kan du konfigurere en individuel produktvariant til **Løb|Gang|Hiking**, **Løb**, **Løb|Hiking|Vandsport** osv.

Når du har defineret variantattributværdierne, skal du vælge **Publicer kanalopdateringer** på siden **Kanalkategorier og produktattributter** i handlingsruden, og derefter køre jobbene **1150**, **1040** og **1070**.

Når jobbene er fuldført, og søgeindekset er opdateret, skal alle forventede værdier vises i søgeresultaterne og resultaterne af gennemsøgning af kategorier.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
