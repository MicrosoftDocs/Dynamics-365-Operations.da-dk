---
title: Tekniske attributter og søgning efter tekniske attributter
description: I dette emne forklares det, hvordan du kan bruge tekniske attributter til at angive alle ikke-standardegenskaber for at sikre, at alle produktmasterdata kan registreres i systemet. Det forklarer også, hvordan du kan bruge teknisk attributsøgning til nemt at finde produkter baseret på de registrerede egenskaber.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f8803e46ce6f104a5afee64faaf393a2df47a61
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568105"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Tekniske attributter og søgning efter tekniske attributter

[!include [banner](../includes/banner.md)]

Du bør bruge tekniske attributter til at angive alle ikke-standardegenskaber for at sikre, at alle produktmasterdata kan registreres i systemet. Det kan derefter bruge teknisk attributsøgning til nemt at finde produkter baseret på de registrerede egenskaber.

## <a name="create-engineering-attributes-and-attribute-types"></a>Oprette tekniske attributter og attributtyper

Tekniske produkter har typisk mange kendetegn og egenskaber, du skal registrere. Selvom du kan registrere nogle af egenskaberne ved hjælp af standardproduktfelterne, kan du også oprette nye tekniske egenskaber efter behov. Du kan definere dine egne *tekniske attributter* og gøre dem en del af produktdefinitionen.

Hver tekniske attribut skal tilhøre en *attributtype*. Dette krav findes, fordi hver enkelt tekniske attribut skal have en *datatype*, der definerer de typer af værdier, som den kan indeholde. En teknisk attributtype kan være en standardtype (f.eks. fri tekst, heltal eller decimaltal) eller en brugerdefineret type (f.eks. tekst, der har et bestemt sæt værdier at vælge mellem). Du kan genbruge hver enkelt attributtype med et hvilket som helst antal tekniske attributter.

### <a name="set-up-engineering-attribute-types"></a>Konfigurere tekniske attributtyper

Udfør følgende trin for at se, oprette eller redigere en teknisk attributtype.

1. Gå til **Teknisk ændringsstyring \> Konfiguration \> Attributter \> Attributtyper**.
1. Vælg en eksisterende attributtype i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny attributtype.
1. Angiv følgende felter:

    - **Navn på attributtype** – Angiv et navn for attributtypen.
    - **Type** – Vælg en standarddatatype (*Valuta*, *Dato/klokkeslæt*, *Decimal*, *Heltal*, *Tekst*, *Boolesk* eller *Reference*).
    - **Fast liste** – Denne indstilling er kun tilgængelig, hvis du angiver feltet **Type** til *Tekst*. Angiv *Ja* for at definere specifikke værdier for attributter af denne type. I dette tilfælde oprettes der en rulleliste. Du kan bruge oversigtspanelet **Værdi** til at fastlægge de værdier, der er tilgængelige for denne attributtype. Angiv indstillingen til *Nej* for at tillade brugere at angive enhver værdi. I dette tilfælde oprettes der et inputfelt.
    - **Værdiinterval** – Denne indstilling er kun tilgængelig, hvis du angiver feltet **Type** til *Heltal*, *Decimal* eller *Valuta*. Angiv *Ja* for at oprette de minimum- og maksimumværdier, der vil blive accepteret for attributter af denne type. Du kan bruge oversigtspanelet **Interval** til at fastlægge minimum- og maksimumværdierne og (for valuta) den valuta, der gælder for de angivne grænser. Angiv denne indstilling til *Nej* for at acceptere enhver værdi. 
    - **Måleenhed** – Dette felt er kun tilgængeligt, hvis du angiver feltet **Type** til *Heltal* eller *Decimal*. Vælg den måleenhed, der gælder for denne attributtype. Hvis der ikke kræves en enhed, skal dette felt være tomt.

### <a name="set-up-engineering-attributes"></a>Konfigurere tekniske attributter

Udfør følgende trin for at se, oprette eller redigere en teknisk attribut.

1. Gå til **Teknisk ændringsstyring \> Konfiguration \> Attributter \> Tekniske attributter**.
1. Vælg en eksisterende attribut i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny attribut.
1. Angiv følgende felter:

    - **Navn** – Angiv et navn til attributten. Dette navn vises kun på siden **Tekniske attributter**. Alle andre steder i systemet vises værdien i feltet **Fuldt navn** for at identificere attributten.
    - **Attributtype** – Vælg en attributtype, som du har defineret i forrige afsnit.
    - **Fuldt navn** – Angiv et navn, der identificerer attributten i systemet (undtagen på siden **Tekniske attributter**). 
    - **Beskrivelse** – Indtast en beskrivelse af attributten.
    - **Hjælp-tekst** – Angiv Hjælp-tekst, der fortæller andre brugere, hvad attributten er til.
    - **Standardværdi** – Angiv en standardværdi for attributten. De indstillinger, der vises, afhænger af den valgte attributtype.
    - **Valuta** – Hvis den valgte attributtype er en valuta, skal du vælge den valuta, som attributten skal acceptere og vise værdier i.

1. Hvis den valgte attributtype er et heltal eller et decimaltal, vises oversigtspanelet **Interval**. I oversigtspanelet skal du indstille følgende felter:

    - **Tolerancehandling** – Vælg, hvordan systemet skal reagere, hvis en bruger indtaster en værdi uden for det angivne interval. Hvis du vælger *Advarsel*, vises der en advarsel, men brugeren kan gemme værdien. Hvis du vælger *Ikke tilladt*, vises en advarsel, og værdien kan ikke gemmes, før brugeren har rettet den.
    - **Minimum** – Angiv den anbefalede eller tilladte minimumværdi.
    - **Maksimum** – Angiv den anbefalede eller tilladte maksimumværdi.

### <a name="engineering-attribute-inheritance"></a>Teknikerattributarv

I forbindelse med produktstrukturer, f.eks. styklister eller formler, kan de markerede attributter overføres fra de overordnede varer til de overordnede varer. Du kan tænke på denne proces som "tilbageføre nedarvning."

#### <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Produktionsordreforslag til planlægningsoptimering*.

#### <a name="attribute-inheritance-example"></a>Eksempel på attributnedarvning

For et fødevareprodukt, som f.eks. et fødevareprodukt, der fungerer som omkostning, skal systemet registrere hver af de elementer, som produktet indeholder. Det kan modelleres som et teknikerprodukt, der indeholder en formel. Denne formel indeholder ingredienserne i den nye formel, som f.eks. mel, mælk, nødder og nødder. I dette eksempel har firmaet to modeller, der kan identificeres, én med forskellige modeller, og én, der ikke gør.

Den kage, der indeholder laktose, har følgende attributter på ingrediensniveau:

- Ingrediens "mel" attribut "varer" = ja
- Ingrediens "mælk"-attribut " måltid" = ja
- Ingrediens "nødder" attribut "nødder" = ja

Den kage, der ikke indeholder laktose, indeholder laktosefri mælk og har følgende attributter på ingrediensniveau:

- Ingrediens "mel" attribut "varer" = ja
- Ingrediens "mælk": attribut "laktose" = nej
- Ingrediens "nødder" attribut "nødder" = ja

Da disse produkter oftest ligner hinanden, kan det være en god ide at overføre disse attributter fra de børn (de to variationer) til det overordnede produkt (den grundlæggende produktvariant). Hvis du vil implementere denne "omvendt nedarvning", kan du bruge funktionen *Attribut-nedarvning*. Denne funktionalitet er defineret for hver [teknikerversion](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Knytte tekniske attributter til en teknisk produktkategori

Visse tekniske attributter gælder for alle produkter, mens andre er specifikke for de enkelte produkter eller produktkategorier. Elektriske attributter er f.eks. ikke nødvendige for mekaniske produkter. Du kan derfor konfigurere *tekniske produktkategorier*. En teknisk produktkategori opretter en samling af tekniske attributter, der skal være en del af definitionen for produkter, der tilhører den pågældende kategori. Du kan også angive, hvilke tekniske attributter der skal være obligatoriske, og om der er en standardværdi.

Du kan finde flere oplysninger om, hvordan du arbejder med tekniske produktkategorier, herunder oplysninger om, hvordan du knytter attributter til kategorier, i [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Angive attributværdier for tekniske attributter

De tekniske attributter, der er tilknyttet en teknisk produktkategori, vises, når du opretter et nyt teknisk produkt, der er baseret på den pågældende kategori. På det tidspunkt kan du angive værdier for attributterne. Senere kan disse værdier ændres på siden **Teknisk version** eller som en del af en teknisk ændringsstyring i en teknisk ændringsordre. Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Oprette et teknisk produkt

Hvis du vil oprette et teknisk produkt, skal du åbne siden **Frigivne produkter**. Vælg derefter **Teknisk produkt** i gruppen **Nyt** under fanen **Produkt** i handlingsruden.

Du skal angive den tekniske kategori, som produktet tilhører. Kategorien angiver alle standardværdier og egenskaber for produktet. Den vil også angive de attributter, der gælder for produktet. Når kategorien er valgt, angives der værdier for attributterne. Du kan derefter redigere disse værdier.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Søge efter produkter ved hjælp af tekniske attributværdier

Du kan bruge teknisk attributsøgning til at finde produkter ved at søge efter deres tekniske attributters værdier. Derfor kan du nemt finde tekniske produkter baseret på deres egenskaber. Du kan søge i de produkter, der tilhører en teknisk produktkategori, eller du kan søge på tværs af alle tekniske produkter.

Søgningen er tilgængelig på produkters masterdatasider og fra transaktionselementer i systemet, f.eks. salgsordrer. I forbindelse med et transaktionselement kan du bruge siden **Teknisk attributsøgning** til at søge efter et produkt. Du kan derefter bruge knappen **Tilføj som ny linje** til at føje produktet til salgsordrelinjerne. Produkter i søgeresultaterne kan også føjes direkte til ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
