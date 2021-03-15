---
title: Produktdimensioner
description: Der er fem produktdimensioner – farve, konfiguration, størrelse, typografi og version. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres.
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 285e9d2d184a899f1ffa502d59a853ba83cda491
ms.sourcegitcommit: 2093c9dc31d1b60b3114085d9cef48fdbbb0ca0d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2021
ms.locfileid: "5118675"
---
# <a name="product-dimensions"></a>Produktdimensioner

[!include [banner](../includes/banner.md)]

Der er fem produktdimensioner: farve, konfiguration, størrelse, typografi og version. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres.

Produktdimensioner er egenskaber, der identificerer en produktvariant. Du kan bruge kombinationer af produktdimensioner til at definere produktvarianter. Du skal definere mindst én produktdimension for en produktmaster for at oprette en produktvariant.

## <a name="product-variants"></a>Produktvarianter

Produktvarianter kaldes også varer. En vare er et fysisk produkt, som ikke er det samme som en service. Det er også muligt at definere en produktmaster af servicetypen. Ved hjælp af servicetypen kan du angive produktvarianter, der omfatter services. For eksempel kan du angive en produktmaster for konsulentbistand og produktvarianter for arbejde, der udføres af erfarne konsulenter og yngre konsulenter.

## <a name="product-dimensions"></a>Produktdimensioner

En produktvariant kan genereres på basis af produktdimensionsværdierne.

Der kan oprettes produktdimensionsværdier for størrelse, farve og typografi på følgende placeringer:

- Siden **Størrelse** (**Administration af produktoplysninger \> Konfiguration \> Dimensions- og variantgrupper \> Størrelser**)
- Siden **Farve** (**Administration af produktoplysninger \> Konfiguration \> Dimensions- og variantgrupper \> Farver**)
- Siden **Typografi** (**Administration af produktoplysninger \> Konfiguration \> Dimensions- og variantgrupper \> Typografier**)

Produktets dimensionsværdier for konfigurationsdimensionen oprettes typisk ved hjælp af enten Variantstyring eller Dimensionsbaseret konfiguration. 

Produktversioner oprettes normalt for bestemte versioner, efterhånden som produktet udvikler sig i løbet af sin livscyklus. Produktversioner beskrives i detaljer senere i dette emne.

Produktdimensioner kan også oprettes og vedligeholdes på siden **Produktdimensioner**, der kan åbnes fra følgende steder:

- Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**. Vælg **Produktdimensioner** i handlingsruden.
- Gå til **Administration af produktoplysninger \> Produkter \> Alle produkter og produktmastere**. Vælg en produktmaster. Vælg **Produktdimensioner** i handlingsruden.
- Gå til **Administration af produktoplysninger \> Frigivne produkter**. Vælg en produktmaster. Vælg **Produktdimensioner** i gruppen **Produktmaster** under fanen **Produkt** i handlingsruden.

Antallet af varianter, der kan oprettes for en vare, er begrænset af antallet af mulige kombinationer af produktdimensioner.

> [!TIP]
> Når du bruger et produkt f.eks. på en ordrelinje, skal du vælge produktdimensioner for at identificere den produktvariant, som du vil arbejde med.

## <a name="example"></a>Eksempel

Et firma sælger denimbukser. Til varen *Cowboybukser* bruges produktdimensionerne for farve og størrelse. Cowboybukserne sælges i tre forskellige farver og seks forskellige størrelser. Farverne er blå, sort og brun. Størrelserne er XS, S, M, L, XL og XXL. Ikke alle størrelser fås i alle tre farver. Hvis alle kombinationer var tilgængelige, ville der være 18 forskellige typer cowboybukser. I dette eksempel produceres der imidlertid kun følgende ni kombinationer af produktvarianter.

| Farve | Størrelse |
|-------|------|
| Blå  | XS   |
| Blå  | L    |
| Blå  | M    |
| Sort | M    |
| Sort | L    |
| Sort | XL   |
| Brun | L    |
| Brun | XL   |
| Brun | XXL  |

## <a name="the-version-product-dimension"></a>Produktdimensionen for version

Version er en produktdimension, der er beregnet til at hjælpe dig med at vedligeholde og spore flere versioner af et produkt overalt i forsyningskæden. Versionssporing er vigtig for de producenter, der opererer i en verden af konstant kortere produktlivscyklusser, øgede krav til kvalitet og pålidelighed og øget fokus på produktsikkerhed.

Som en standardproduktdimension fungerer versionen på samme måde som de eksisterende produktdimensioner (størrelse, typografi, farve og konfiguration). Derfor kan du bruge den til andre formål ud over at spore produktversioner.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Aktivere versionsdimensionen

#### <a name="before-you-turn-on-the-version-dimension"></a>Før du aktiverer versionsdimensionen

Når du aktiverer versionsdimensionen, kan nogle funktioner blive brudt eller holde op med at fungere som forventet, hvis du har installeret andre løsninger, der føjer tilpasninger til lagerdimensionerne. Hvis versionsdimensionen skal kunne fungere fuldt ud, kan det være nødvendigt at opdatere disse løsninger, så de omfatter versionsdimensionen i deres referencer til lagerdimensionerne.

Når du tester løsningerne for at sikre kompatibilitet med versionsdimensionen, skal du kigge efterfølgende elementer:

1. **Funktionalitet:** Fremfor alt vurderes alle tilpasninger, der vedrører lagerdimensionerne, for at sikre, at de kan fungere sammen med versionsdimensionen.
1. **Referencer til lagerdimensioner:** Se, om der er referencer til lagerdimensionerne (dvs. steder hvor der refereres eksplicit til dimensionerne). Referencer til `InventDimId` skal fungere som standard, men hold øje med referencer til typografi eller farve. Du skal f.eks. kontrollere følgende elementer:

    - API-kald i udvidede klasser
    - Alle referencer til specifikke lagerdimensioner i udvidelseskode (denne kode skal have en flydende tilgang til versionsdimensionen sammen med typografi, farve og størrelsesdimensioner).

1. **Referencer til forældede API-kald:** I sin introduktion til versionsdimensionen har Microsoft forsøgt at gøre så få API'er som muligt forældede. De få API'er, der er gjort forældede, giver en advarsel, når du aktiverer konfigurationsnøglen **Produktdimension – version**. Opkald til disse API'er skal være rettet i dine udvidede løsninger, før du kan slå versionsdimensionen til i et produktionssystem. Her er de versionsspecifikke forældede API'er:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Kort:** Hvis der er tilknyttet lagerdimensioner, skal den tilsvarende relationstilknytning til disse tilknytninger opdateres, så de omfatter versionsdimensionen. Se efter tabeller, hvor felterne omfatter lagerdimensioner, i de udvidede model- eller tabeludvidelser.
1. **Microsoft Dynamics 365 Commerce-funktionalitet:** Når den er slået til, vises versionsdimensionen i hele den Commerce-specifikke kode i Dynamics 365 Supply Chain Management. Versionsdimensionen understøttes dog endnu ikke af Commerce-kanaldatabasen eller i POS- eller e-Commerce-programmerne. Disse Commerce-specifikke programmer understøtter ikke brugere, der sælger/sender eller returnerer/modtager lagerbeholdning efter versionsdimension. Opslagsfunktionerne for lagertilgængelighed skelner ikke mellem lagerbeholdning efter versionsdimension i Commerce-apps. Denne funktionsmåde ligner konfigurationsdimensionens aktuelle funktionsmåde i hele Commerce.

#### <a name="turn-on-the-version-dimension"></a>Aktivere versionsdimensionen

Før du kan bruge versionsdimensionen, skal den være aktiveret i dit system. Denne opgave kræver administratorrettigheder.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. Aktiver den funktion, der hedder *Produktdimension for version*. (Få flere oplysninger i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Indstil systemet til [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Under fanen **Konfigurationsnøgler** skal du udvide **Handel** og markere afkrydsningsfeltet for **Produktdimension – version**.
1. Deaktiver [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Områder, hvor versionsdimensionen ikke understøttes

Følgende områder understøtter ikke versionsdimensionen (du kan stadig bruge disse områder, men du kan ikke føje versionsnummererede produkter (produkter, hvor versionsdimensionen bruges) til dem). Du kan f.eks. ikke føje en versionsnummereret vare til et kreditorkatalog. Det skyldes, at hvis du føjer produkter med versionsdimensionen til disse områder, ville det medføre skadelige ændringer.

- Månedlig opgørelse for omkostningsobjekt
- Erklærings-cache for omkostningsobjekt
- MCR-salgsstatistik pr. vare
- Kreditorkataloger
- EcoResProductDimensionGroupEntity

Desuden understøtter funktionerne til ordreoprettelse og ordrebehandling i Commerce (f. eks. til POS, Callcenter og e-handelsordrer) ikke versionsdimensionen. Der er ingen bekræftet tidslinje for, hvornår Commerce-ordrer vil blive udvidet til at understøtte den.

### <a name="functional-characteristics-of-the-version-dimension"></a>Funktionelle egenskaber for versionsdimensionen

Versionsdimensionen fungerer på samme måde som andre produktdimensioner. På grund af dens særlige karakter, og fordi den er beregnet til at vedligeholde og spore flere versioner af et produkt, opfører den sig lidt anderledes. Her er nogle af forskellene og lighederne:

- **Der findes ingen versionsgruppe.**

    Selvom begrebet grupper findes for størrelse, farve og typografi (farvegruppe, størrelsesgruppe og typografigruppe), findes der ingen gruppe for versioner. Grupper giver dig mulighed for at foruddefinere de gældende værdier, så når du f.eks. tildeler en farvegruppe til et produkt, kan produktet bruge alle farverne i den pågældende farvegruppe. Dette begreb gælder ikke for versionsdimensionen, da de versioner, som et produkt ikke har brug for, er foruddefineret, når produktet oprettes. I stedet oprettes der versioner i løbet af produktets levetid, når de er påkrævet. Hvis produktets form, tilpasning og funktion ikke ændres, vil du typisk oprette en ny version i stedet for et nyt produkt.

- **Produktvariantforslag fungerer, som de gør nu.**

    Forslag til produktvarianter opretter forslag til alle versionsdimensionsværdier, ligesom de gør for andre dimensioner. Processen for oprettelse og frigivelse af produktversioner er den samme som for produkter, der bruger andre dimensioner. Når du opretter en produktversion, vil den første version (V1) blive oprettet som en produktdimension, og varianterne vil blive frigivet. Efterhånden som produktændringerne og en ny version er nødvendig, vil den nye versionsværdi (V2) blive tilføjet, og de krævede varianter vil blive frigivet. Der er ingen forventning om, at alle versioner (V1, V2 og V3) vil blive oprettet forud for produktet.

> [!IMPORTANT]
> Hvis du aktiverer og bruger versionsdimensionen, kan nogle af de løsninger, der refererer til lagerdimensionerne, holde op med at fungere som forventet. Hvis du vil bekræfte og rette disse problemer, skal du kontakte den uafhængige softwareleverandør (ISV) for de påvirkede løsninger. Du kan finde flere oplysninger i [Aktivere versionsdimensionen](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]