---
title: Søge efter produkter og produktvarianter under ordreindtastning
description: Brug feltet **Varenummer** til at søge efter produkter og produktvarianter, når du manuelt opretter en salgsordrelinje eller en indkøbsordrelinje. Her kan du hurtigt finde produktvarianter, når du kun har konfigurationsstrengen eller en af produktdimensionerne tilgængelige.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, PurchTablePart, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 72190c5f58b241abe9f4a458b6c366dfec3787f0bb32d24f73a7e9e21dbb58b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714926"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Søge efter produkter og produktvarianter under ordreindtastning

[!include [banner](../includes/banner.md)]

Brug feltet **Varenummer** til at søge efter produkter og produktvarianter, når du manuelt opretter en salgsordrelinje eller en indkøbsordrelinje.  Her kan du hurtigt finde produktvarianter, når du kun har konfigurationsstrengen eller en af produktdimensionerne tilgængelige.

Nogle gange er for meget af noget ikke den bedste situation at være i, og det er især tilfældet, hvis du sælger en række produkter, der minder om hinanden, og du prøver at huske varenumre eller produktnavne for at finde det rigtige produkt til en salgsordre. Du kan bruge feltet **Varenummer** på en salgsordrelinje eller en indkøbsordrelinje som et søgefelt. Du kan indtaste en del af et produktnavn, et nummer eller en dimension og få et opslag, som indeholder alle de elementer, der svarer til søgeordet.

## <a name="how-search-works"></a>Sådan fungerer søgning
Når du søger efter produkter eller produktvarianter, er det vigtigt at forstå, hvordan søgefunktionen finder de produkter, der svarer til den tekst, du skriver. De vigtigste søgeregler for at få søgeresultater er:

-   Søgeresultater returnerer enhver tilsvarende post og ignorerer det felt, hvor søgeteksten er indtastet.
-   Søgeteksten skal være til stede i den tilsvarende post i fuld længde.
-   Der opstår et match, selvom søgeteksten er fundet i midten af en tekststreng i den tilsvarende post. Den behøver ikke at forekomme i begyndelsen af en tekststreng.
-   Søgeteksten behandles som én tekststreng, selvom den indeholder mellemrum.

### <a name="examples"></a>Eksempler

Følgende eksempler bruger produkter og produktvarianter til at illustrere, hvordan søgning håndteres i forskellige scenarier. **Forudsætning:** Under **Salg og marketing &gt; Opsætning &gt; Søg &gt; Søgeparametre &gt; Søgetype** skal du vælge indstillingen **Fuldt match**.

| Produkttype     | Produktnavn    | Vis produktnummer | varenummer | Variantkonfiguration |
|------------------|-----------------|------------------------|-------------|---------------|
| Specifikt produkt | SpeakerMidRange | D0001                  | D0001       | Ikke relevant            |
| Produktvariant  | Aktiv højttaler  | D0010:::Sort:         | D0010       | 000005        |
| Produktvariant  | Aktiv højttaler  | D0010:::Hvid:         | D0010       | Hvid         |

Hvis du skriver "højt" i feltet **Varenummer**, får du alle de ovennævnte produkter som resultat i opslaget. Hvis du skriver 'sort' i feltet **Varenummer**, får du det andet produkt som resultat, fordi den har teksten 'sort' i det viste produktnummer. Disse to eksempler viser, at søgningen ikke kun er i starten af feltet. Der findes et match, selvom søgeteksten findes i den tilsvarende post i midten af en tekststreng.  

Hvis du skriver '05' får du kun den anden produktvariant, fordi den har '05' i konfigurationen. Dette viser, at søgningen er på tværs af alle aktiverede felter på siden **Søgekriterier**.  

Hvis du skriver 'højt 05', får du ikke nogen resultater. Dette skyldes, at der søges efter den fulde tekst, der er angivet. Søgningen forsøger ikke at finde 'højt' og derefter indsnævre resultaterne til dem, der indeholder '05'.  

Du kan begrænse antallet af søgeresultater ved hjælp af feltet **Antal resultater** på siden **Salg og marketing &gt; Opsætning &gt; Søg &gt; Søgeparametre**. Hvis du angiver dette felt til 0, returneres alle søgeresultater. Hvis du indstiller det til 10, returneres maksimalt 10 søgeresultater.

## <a name="configure-the-product-search"></a>Konfigurere søgning efter produkt
Før du kan bruge produktets og produktvariantens søgefunktion, skal du følge disse trin for at konfigurere søgning efter produkt. [![3 trin til at konfigurere produktsøgning\_AXAppFall.](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Trin 1: Medtag alle de relevante produkt- og produktvariant-id'er og -dimensioner i søgekriterierne

Eksempler på produkt- og produktvariant-id'er og -dimensioner, som du kan søge efter: **produktnavn, varenummer**, **vist produktnummer, konfiguration, farve, størrelse, typografi, søgenavn, osv**.  

Gå til siden **Salg og marketing &gt; Opsætning &gt; Søg &gt; Søgekriterier**. På siden **Søgekriterier,** kan du definere kriterier for søgning efter kunde, kundeemne og produkt. Sørg for at filtrere siden ved hjælp af søgekriterier for produktet. Du kan gøre dette ved at skifte til **Produkt** i sidens menu.  

Klik på **Ny** i sidens menu for at tilføje det viste produktnummer i søgekriterierne Dette vil tilføje en ny post i gitteret **Søgekriterier**. Åbn **Feltnavn**-kolonneopslaget, og vælg **DisplayProductNumber**. For at tilføje produktets konfiguration i søgekriterierne skal du oprette en ny post i **Søgekriterier**-gitteret og vælge **configId** i kolonnen **Feltnavn**. På samme måde kan du oprette en post med **Feltnavn** **InventColorId** for farvedimensionen, **InventSizeId** for størrelsesdimensionen og **InventStyleId** for typedimensionen.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Trin 2: Udfyld den databasetabel, som bruges til at søge efter produkt

På siden **Søgekriterier** skal du klikke på knappen **Opdater søgedata**. I **Opdater søgedata**-dialogboksen skal du sikre dig, at **Kilde** er angivet til **Produkt**, og klik derefter på **OK**. Systemet vil samle alle de valgte kriterier, der er angivet i trin 1, i én tabel. Hvis du har en masse produkter og produktvarianter, kan denne handling være temmelig langvarig, og der vises muligvis en advarsel. Vi anbefaler, at du planlægger udfyldning af søgetabellen på batchserveren på et tidspunkt, hvor serveren ikke er for optaget.  

Indtil tabellen udfyldes, vil produktsøgning ikke give de korrekte resultater. Hvis du ikke får nogen søgeresultater, skal du kontrollere, at denne tabel er udfyldt.  

Tabellen skal kun udfyldes, når søgekriterierne er blevet ændret. Netop frigivne produkter og varianter føjes automatisk til tabellen. Slettede produkter og varianter fjernes automatisk fra tabellen.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Trin 3: Aktivere opslag for produktsøgning på salgs- og indkøbsordrelinjer

Du kan aktivere denne funktionalitet ved at gå til **Salg og marketing &gt; Opsætning &gt; Søg &gt; Søgeparametre** og indstille **Aktivér opslag for produktsøgning** til **Ja** under fanen **Generelt**.  

Til salgsordrelinjepost er standardfunktionsmåden at åbne siden **Produktsøgning**, når du begynder at skrive i feltet **Varenummer** og trykker på **tabulatortasten**. Siden **Produktsøgning** ændrer konteksten under oprettelse af ordrelinjer og kan betragtes som unødvendigt forstyrrende. Hvis du foretrækker at få søgeresultaterne i et opslag og ikke miste konteksten under indtastning af ordrelinje, kan du bruge søgeopslaget i stedet. Hvis du søger efter et produkt eller en produktvariant, men du ikke markerer noget i opslaget og trykker på **tabulatortasten**, vises siden **Produktsøgning**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]