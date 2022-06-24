---
title: Styring af attributter og attributgrupper
description: Denne artikel beskriver, hvordan du kan bruge attributter som et værktøj til at beskrive et produkt og dets egenskaber via brugerdefinerede felter.
author: ashishmsft
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: cd74cb7795366bdca80e47d79a9591af69a16daf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876658"
---
# <a name="manage-attributes-and-attribute-groups"></a>Styring af attributter og attributgrupper

[!include [banner](includes/banner.md)]

*Attributter* er en måde til at beskrive et produkt og dets egenskaber yderligere via brugerdefinerede felter (f.eks. **Hukommelsesstørrelse**, **Harddiskkapacitet**, **Er Energy star-kompatibel** og så videre). Attributter kan være tilknyttet forskellige Commerce-enheder, såsom produktkategorier og -kanaler, og du kan angive standardværdier for dem. Produkter arver derefter attributterne og standardværdierne, når de bliver knyttet til produktkategorierne eller kanalerne. Standardværdierne kan tilsidesættes på hvert enkelt produktniveau i kanalniveauet eller i et katalog.


Et typisk tv-produkt kan f.eks. have følgende attributter.

| Kategori   | Egenskab                | Tilladte værdier          | Standardværdi |
|------------|--------------------------|-----------------------------|---------------|
| Tv og video | Mærke                    | Alle gyldige mærkeværdier       | None          |
| Tv         | Skærmstørrelse              | 20-80 tommer                | None          |
|            | Lodret opløsning      | 480i, 720p, 1080i eller 1080p | 1080p         |
|            | Skærmens opdateringshastighed      | 60 Hz, 120 Hz eller 240 Hz       | 60 Hz          |
|            | HDMI-inputs              | 0-10                        | 3             |
|            | DVI-inputs               | 0-10                        | 1             |
|            | Sammensat inputs         | 0-10                        | 2             |
|            | Komponent-inputs         | 0-10                        | 1             |
| LCD        | 3D-klar                 | Ja eller Nej                   | Ja           |
|            | 3D-aktiveret               | Ja eller Nej                   | Nej            |
| Plasma     | Driftstemperatur fra      | 32-110 grader              | 32            |
|            | Driftstemperatur til        | 32-110 grader              | 100           |
| Projection | Garanti på projektionsrør | 6, 12 eller 18 måneder         | 12            |
|            | \# på projektionsrør   | 1-5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Attributter og attributtyper

Attributterne baseres på *attributtyper*. Attributtypen identificerer den type data, der kan angives for en bestemt attribut. Følgende attributtyper understøttes:

- **Valuta** – Denne type understøtter en valutaværdi. Den kan være afgrænset (dvs. den kan understøtte et værdiinterval), eller den kan være åben.
- **DateTime** – Denne type understøtter en dato- og klokkeslætsværdi. Den kan afgrænses eller være åben.
- **Decimal** – Denne type understøtter en numerisk værdi, der indeholder decimalpladser. Den understøtter også en måleenhed. Den kan afgrænses eller være åben.
- **Heltal** – Denne type understøtter en numerisk værdi. Den understøtter også en måleenhed. Den kan afgrænses eller være åben.
- **Tekst** – Denne type understøtter en tekstværdi. Den understøtter også et foruddefineret sæt af mulige værdier (dvs. *fasttekst*).
- **Boolesk** – Denne type understøtter en binær værdi (**sand** eller **falsk**).
- **Reference** – Denne type refererer til andre attributter.

### <a name="set-up-attribute-types"></a>Konfigurer attributtyper

1. Log på back-office-klienten som produktchef.
2. Gå til **Administration af produktoplysninger** &gt; **Opsætning** &gt; **Kategorier og attributter** &gt; **Attributtyper**.
3. Opret to attributtyper for typen **Tekst**, vælg **Ja** i indstillingen **Fast liste**, og tilføj derefter en liste over værdier:

    - Navngiv én attributtype **Linseform**, og tilføj følgende værdier: **Ellipse**, **Firkant** og **Rektangel**.
    - Navngiv den anden attributtype **Solbrillemærke**, og tilføj følgende værdier: **Ray ban**, **Aviator** og **Oakley**.

![Attributtyper.](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Konfigurer en attribut

1. Log på back-office-klienten som produktchef.
2. Gå til **Administration af produktoplysninger** &gt; **Opsætning** &gt; **Kategorier og attributter** &gt; **Attributter**.
3. Opret en attribut med navnet **Linse**.
4. Indstil feltet **Attributtype** til **Linseform**.

![attributter.](media/Attribute.png)

## <a name="attribute-metadata"></a>Attributmetadata

I *Attributmetadata* kan du vælge indstillinger for at angive, hvordan attributterne for hvert produkt skal fungere. Du kan f.eks. angive, om attributter er påkrævede, om de kan bruges til søgninger, og om de kan bruges som filter.

For produkter kan metadataattributindstillingerne tilsidesættes på kanalniveau. Denne egenskab beskrives senere i denne artikel.

Som du har muligvis bemærket, indeholder siden **Attributter** indstillinger, der vedrører attributmetadata. Under **Attributmetadata for POS** påvirker indstillingen **Kan redigeres** attributværdiernes funktionsmåde i POS eller den måde, som systemet håndterer disse attributværdier på. Kun attributter, hvor du kan indstille **Kan redigeres** til **Ja**, kan bruges til forbedring eller filtrering af produkter i POS.

Her er de resterende indstillinger for attributmetadata på siden **Attributter**:

- Søgbar
- Kan hentes
- Kan forespørges
- Sorterbar
- Tillad flere værdier
- Ignorer bogstavstørrelse og format
- Komplet match

Disse indstillinger var oprindeligt beregnet til at forbedre online storefrontens søgefunktion. Selvom Commerce ikke som standard indeholder online storefronten, indeholder det SDK'et (Software Development Kit) til eCommerce-publicering. Kunder kan bruge dette SDK til at placere produkter i et søgeindeks efter eget valg. Selvom produktdataene er importeret, skal kunder stadig kunne skelne søgbare data, data, der kan forespørges på, osv. På denne måde kan de opbygge et optimalt indeks for at sikre, at de kun indekserer attributter, der *efter deres opfattelse* der skal indekseres.

Du kan finde oplysninger om formålet med disse resterende indstillinger under [Oversigt over søgeskemaet i SharePoint Server 2013](/SharePoint/search/search-schema-overview).

## <a name="filter-settings-for-attributes"></a>Filterindstillinger for attributter

Med filterindstillinger for attributter kan du definere, hvordan filtrene for attributter vises i POS. Du kan få adgang til filterindstillingerne for en attribut ved at vælge attributten på siden **Attributter** og derefter vælge **Filterindstillinger** i handlingsruden.

Siden **Visningsindstillinger for filter** indeholder følgende felter:

- **Navn** – Dette felt er som standard indstillet til navnet på attributten. Du kan imidlertid ændre værdien.
- **Visningsindstilling** – Der er følgende tilgængelige indstillinger:

    - **Enkelt værdi** – Denne indstilling er tilgængelig for følgende attributtyper: **Boolesk**, **Valuta**, **Decimal**, **Heltal** og **Tekst**. Med denne indstilling kan du vælge en enkelt værdi for disse attributter, som du vil forbedre, i klienten.
    - **Flere værdier** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal**, **Heltal** og **Tekst**. Med denne indstilling kan du vælge flere værdier for denne attribut, som du vil forbedre, i klienten.

- **Vis kontrolelement** – Der er følgende tilgængelige indstillinger:

    - **Liste** – Denne indstilling er tilgængelig for alle attributtyper.
    - **Afgrænsning** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.
    - **Skyder** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.
    - **Skyder med søjler** – Denne indstilling er tilgængelig for følgende attributtyper: **Valuta**, **Decimal** og **Heltal**.

- **Grænseværdi** – Denne indstilling er nødvendig, hvis du valgte **Interval** som visningskontrolelementtype. Du kan angive værdier ved hjælp af et semikolon (;) som afgrænser.

    F.eks. for filteret **Rumfang af pose** kan en tærskelværdi være **10; 20; 50; 100; 200; 500; 1000; 5000**. I dette tilfælde indeholder POS følgende intervaller. Intervaller, der ikke har nogen produkter i resultatet, vises nedtonet.

    - Mindre end 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eller derover

![Filterindstillinger for attribut.](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Attributgrupper

Når attributter er defineret, kan de tildeles til attributgrupper. En *attributgruppe* bruges til at gruppere de individuelle attributter for en komponent eller en underkomponent i en produktkonfigurationsmodel. En attribut kan medtages i mere end en attributgruppe. Attributgrupper kan hjælpe brugerne med at konfigurere produkter, fordi de forskellige valgmuligheder er arrangeret i en bestemt kontekst. Attributgrupper kan tildeles til kategorier eller kanaler.

Du kan også angive standardværdier for attributter, der indgår i en attributgruppe. For eksempel kan du føje en attribut for farve til en attributgruppe og vælge **Blå** som standardattributværdien. I dette tilfælde, når attributgruppen føjes til et produkt, der omfatter farve, som en af attributterne, vises **Blå** som standardfarven for det pågældende produkt.

![Attributgrupper.](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Oprette en ny attributgruppe

1. Log på back-office-klienten som produktchef.
2. Gå til **Administration af produktoplysninger** &gt; **Opsætning** &gt; **Kategorier og attributter** &gt; **Attributgrupper**.
3. Opret en attributgruppe, der hedder **Moderigtige solbriller**.
4. Tilføj følgende attributter: **Linseform** og **Solbrillemærke**.

### <a name="assign-attribute-groups-to-categories"></a>Tildele attributgrupper til kategorier

En eller flere attributgrupper kan knyttes til kategorinoder i følgende typer kategorihierarkier: Commerce-produkthierarki, kategorihierarki for kanalnavigation og supplerende produktkategorihierarki. Når produkter derefter kategoriseres, arver de de attributter, der indgår i attributgrupperne.

![Produkthierarki – produktattributgrupper.](media/AGRetailProdHierarchy.PNG)

Følg disse trin for at tildele attributgrupper til kategorierne i Commerce-produkthierarkiet.

1. Log på back-office-klienten som produktchef.
2. Gå til **Retail og Commerce** &gt; **Kategori- og produktstyring** &gt; **Commerce-produkthierarki**.
3. Vælg **Modenavigationshierarki**.
4. Under **Herretøj** skal du vælge kategorien **Bukser** og derefter i oversigtspanelet **Produktattributgrupper** tilføje en attributgruppe med navnet **Bælter til mænd**.
5. Vælg kategorien **Moderigtige solbriller**, og kontroller de nye attributter i attributgruppen **Modesolbriller** ved at vælge **Vis attributter**.

    Attributgruppen skal vise de nye attributter **Linseform** og **Solbrillemærke**.

6. Under **Herretøj** skal du vælge kategorien **Bukser** og kontrollere attributterne for attributgruppen **Bælter til mænd** ved at vælge **Vis attributter**.

    Attributgruppen skulle vise attributterne **Bæltemærke, mænd**, **Bæltemateriale** og **Bæltestørrelse**.

> [!NOTE]
> Denne procedure kan også bruges til at tildele attributgrupper til kategorier i Kategorihierarki for kanalnavigation og Supplerende produktkategorihierarki. Brug følgende navigationsstier i trin 2:
>
> - Retail og Commerce &gt; Kategori og produktstyring &gt; Navigationskategorier for kanal
> - Retail og Commerce &gt; Kategori og produktstyring &gt; Supplerende produktkategorier

### <a name="assign-attribute-groups-to-stores"></a>Tildele attributgrupper til butikker

En eller flere attributgrupper kan knyttes til en eller flere butikker i butikhierarkiet. Når produkter derefter forbedres for specifikke butikker, arver produkterne de attributter, der indgår i attributgrupper.

1. Log på back-office-klienten som produktchef.
2. Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **Kanalkategorier og produktattributter**.
3. Du kan tildele attributgrupper til Houston-kanalen:

    1. Vælg **Houston** kanalen.
    2. I oversigtspanelet **Attributgruppe** skal du vælge **Tilføj** og derefter i feltet **Navn** skal du vælge **SharePointProvisionedProductAttributeGroup**.
    3. Vælg **Tilføj** igen og derefter i feltet **Navn** skal du vælge **Bælter til mænd**.
    4. Vælg **Tilføj** igen og derefter i feltet **Navn** skal du vælge **Moderigtige solbriller**.

        > [!NOTE]
        > Der vises en indstilling, hvor du kan angive, at denne kanal skal arve attributgrupperne fra sin overordnede kanal i hierarkiet. Hvis du vælger **Ja** i indstillingen **Arv**, arver den underordnede kanalnode alle attributgrupper og alle attributter i disse attributgrupper.

4. Aktiver attributterne, så de er tilgængelige i Houston-kanalen:

    1. I handlingsruden skal du vælge **Angiv attributmetadata**.
    2. Vælg kategorinoden **Mode**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter** for hver attribut.
    3. Vælg kategorinoden **Modetilbehør**, vælg kategorien **Moderigtige solbriller**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter for hver attribut**.
    4. Vælg kategorinoden **Herretøj**, vælg kategorien **Bukser**, og vælg derefter **Medtag attribut** i oversigtspanelet **Kanalproduktattributter for hver attribut**.

![Kanalkategorier og produktattributter – Attributgrupper.](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Tilsidesætte attributværdier

Standardværdierne for attributter kan tilsidesættes for individuelle produkter på produktniveau. Standardværdierne kan også tilsidesættes for individuelle produkter i specifikke kataloger, der er målrettet specifikke kanaler.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Tilsidesætte attributværdierne for et enkelt produkt

1. Log på back-office-klienten som produktchef.
2. Gå til **Retail og Commerce** &gt; **Kategori og produktstyring** &gt; **Frigivne produkter efter kategori**.
3. Vælg kategorinoden **Mode** &gt; **Modetilbehør** &gt; **Moderigtige solbriller**.
4. Vælg det påkrævede produkt i gitteret. Vælg derefter **Produktattributter** i gruppen **Konfigurer** under fanen **Produkt** i handlingsruden.
5. Vælg en attribut i venstre rude, og opdater derefter dens værdi i højre rude.

![Siden Produktdetaljer – produktattributgrupper.](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Tilsidesætte attributværdierne for produkter i et katalog

1. Log på back-office-klienten som produktchef.
2. Gå til **Retail og Commerce** &gt; **Administration af kataloger** &gt; **Alle kataloger**.
3. Vælg **Fabrikam Base Catalog**-kataloget.
4. Vælg kategorinoden **Mode** &gt; **Modetilbehør** &gt; **Moderigtige solbriller**.
5. I oversigtspanelet **Produkter** skal du vælge det krævede produkt og derefter vælge **Attributter** over produktgitteret.
6. Opdater værdierne for de påkrævede attributter i følgende oversigtspaneler:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

    > [!NOTE]
    > Hvis der er oprettet delte produktmedier og delte produktattributter, gælder de for alle produkter.

![Attributgrupper for katalogprodukt.](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Tilsidesætte attributværdierne for produkter i en kanal

1. Log på back-office-klienten som produktchef.
2. Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **Kanalkategorier og produktattributter**.
3. Vælg **Houston** kanalen.
4. I oversigtspanelet **Produkter** skal du vælge det krævede produkt og derefter vælge **Attributter** over produktgitteret.

    > [!NOTE]
    > Hvis der ikke findes nogen produkter, kan du tilføje produkter ved at vælge **Tilføj** i oversigtspanelet **Produkter** og derefter vælge de ønskede produkter i dialogboksen **Tilføj produkter**.

5. Opdater værdierne for de påkrævede attributter i følgende oversigtspaneler:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

    > [!NOTE]
    > Hvis der er oprettet delte produktmedier og delte produktattributter, gælder de for alle produkter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]