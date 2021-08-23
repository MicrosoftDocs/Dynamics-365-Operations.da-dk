---
title: Konfigurere produktdimensionsværdier, der skal vises som prøver
description: I dette emne beskrives, hvordan du konfigurerer produktdimensionsværdier som prøver i Microsoft Dynamics 365 Commerce Headquarters.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: b1cef992b3d4e3889dd1d5dcc21a0d1ba3f55acc166f5003fc79f64fc54a8754
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764608"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Konfigurere produktdimensionsværdier, der skal vises som prøver

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer produktdimensionsværdier som prøver i Microsoft Dynamics 365 Commerce Headquarters. Du kan finde oplysninger om produktdimensioner under [Produktdimensioner](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce understøtter brugen af størrelses-, typografi- og farvedimensioner til at repræsentere produktvarianter. Produktdimensioner har fulde navne, der vises på sider med produktoplysninger (PDP'er), så produktvarianter kan vælges. Eksempler på disse fulde navne omfatter "Lille", "Mellem" og "Stor" for størrelser og "Sort" og "Brun" for farver. Men hvis et produkt understøtter mange variationer, skal der foretages flere valg for at få vist billedet for de enkelte produktvarianter. Det kan derfor være langsomt og kedeligt for kunderne at gennemse og vælge produktvarianter.

Når dimensioner vises som prøver på PDP'er, får kunderne en visuelt eksempelvisning af et produkts variationer. De kan nemt gennemse en lang række farver, mønstre og teksturer og kan hurtigt se forskellige kombinationer af produktvariationer.

Funktionen til visning af dimensionerne som prøver gør det muligt for Commerce at bruge hexadecimale (hex) koder og billeder til at vise dimensioner som prøver. Desuden kan lignende dimensioner, f.eks. farver, grupperes på sider over produktlister. En kunde søger f.eks. efter produkter, der er blå. Hvis de forskellige blå dimensionsværdier er grupperet sammen, viser listen over søgeresultater produkter, der har de forskellige blå nuancer. Dimensionsgruppering forbedrer produktafgrænsningsoplevelsen betydeligt og hjælper kunderne med at finde flere produkter via en enkelt søgeforespørgsel efter produkter.

> [!NOTE]
> Funktionen til visning af dimensionerne som prøver er tilgængelig fra og med Dynamics 365 Commerce version 10.0.20.

I følgende illustration vises et eksempel, hvor farver vises som prøver på en Commerce-PDP.

![Eksempel på farver, der vises som prøver på en side med produktoplysninger.](../dev-itpro/media/swatch_pdp.png)

I følgende illustration vises et eksempel, hvor farver vises som prøver på en Commerce-side med en liste over søgeresultater.

![Eksempel på farver, der vises som prøver på en side med en liste over søgeresultater.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Aktivere funktionen til visning af dimensionerne som prøver i Commerce Headquarters

Hvis du vil aktivere funktionen til visning af dimensionerne som prøver i Commerce Headquarters, skal du gå til **Arbejdsområder \> Funktionsstyring** og aktivere funktionen **Aktivér en mekanisme til at repræsentere dimensioner som farvekort**. Når dette funktionsflag er aktiveret, tilføjes der tre nye felter for hver dimension i de relevante tabeller i Commerce Headquarters: **Hexcode**, **URL** (til billeder) og **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Konfigurere dimensionsværdier i Commerce Headquarters

Funktionen til visning af dimensionerne som prøver understøttes for størrelses-, typografi- og farvedimensioner. Værdier for hexkode- og URL-adresse til billede for de relevante dimensioner kan angives i Commerce-hovedkvarteret. Hvis der ikke er angivet en værdi for hexkode og URL-adresse til billede for en dimension, viser systemet som standard teksten til dimensionens fulde navn.

Konfigurationen kan udføres på et af følgende niveauer:

- **Dimension** – Åbn siden for en dimension i Commerces-hovedkvarteret ved at søge efter **Farve**, **Størrelse** eller **Typografi**. På hver side viser et gitter dimensionsværdierne. Du kan administrere værdier for visningsrækkefølge, hexkode og URL-adressen til billedet. I følgende illustration vises et eksempel på en konfiguration på siden **Farver**.

    ![Eksempel på dimensionskonfiguration på siden Farver.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensionsgruppe** – I Dynamics 365 Commerce kan du bruge egenskaben **RefinerGroup** til at oprette dimensionsgrupper. Hvis der er defineret dimensionsgrupper, skal du åbne den relevante side ved at søge efter **Farvegruppe**, **Størrelsesgruppe** eller **Typografigruppe**. På hver side kan du administrere værdierne for hexkoden, URL-adressen til billede og afgrænsningsgruppen. I følgende illustration vises et eksempel på en konfiguration på siden **Farvegrupper**.

    ![Eksempel på dimensionskonfiguration på siden Farvegrupper.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Produktdimension (under produktoprettelse)** – Når du opretter et nyt produkt, kan du bruge siden **Produktdimensioner** til at angive dimensionsværdierne. For eksisterende produkter er felterne **Hexcode**, **URL** (til billeder) og **RefinerGroup** muligvis allerede angivet. Du kan dog ændre værdierne efter behov. I følgende illustration vises et eksempel på en konfiguration på siden **Produktdimensioner**.

    ![Eksempel på dimensionskonfiguration på siden Produktdimensioner.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Processen til administration af konfigurationer af hexkode og URL-adresse til billeder følger det samme mønster som det, der bruges til at administrere visningsrækkefølgen for dimensioner.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Konfigurere dimensionsværdier ved hjælp af hexkoder

For de fleste farvedimensioner skal der angives en farveværdi for hexkoden på dimensionssider i Commerce-hovedkvarteret. Farven sort skal for eksempel have hexkodeværdien **#00000**. Når Commerce gengiver en webstedsside, repræsenteres hexkoden af en farveprøve.

I følgende illustration vises et eksempel, hvor farvedimensioner konfigureres ved hjælp af hexkodeværdier.

![Eksempel på dimensionskonfiguration, der bruger hexkoder.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Konfigurere dimensionsværdier ved hjælp af URL-adresser til billeder

Nogle farvedimensioner repræsenterer mønstre, ikke dækkende farver. En farvedimension kan for eksempel beskrives som "leopard". I disse tilfælde kan du mere effektivt repræsentere farvedimensionerne ved hjælp af publicerede billeder i stedet for hexdekoder til prøver.

Du skal overføre de enkelte billeder til Commerce-webstedsgenerator og publicere dem. Angiv derefter URL-adressen til billeder for det publicerede billede på de relevante dimensionssider i Commerces-hovedkvarteret. Hvis der er valgt en dimension, der skal vises som en prøve, men der ikke er defineret en hexkode, udfører Commerce et billedopslag, når siden gengives. Hvis billedopslaget mislykkes, viser Commerce teksten for dimensionens fulde navn.

I følgende illustration vises et eksempel, hvor URL-adresser til billeder bruges til konfigurationen på siden **Farver**.

![Eksempel på dimensionskonfiguration, der bruger URL-adresser til billeder.](../dev-itpro/media/swatch_color_urls.PNG)

Du kan bruge en medieskabelon til at definere URL-adresser til billeder på samme måde som til produkt- og kategoribilleder. Når du overfører billeder til webstedsgeneratoren, skal konventioner for filnavn og filstier være konsistente.

I følgende illustration vises et eksempel, hvor URL-adresser til billeder bruges til konfigurationen af en medieskabelon.

![Eksempel på konfiguration af medieskabelon.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Konfigurere dimensionsværdier ved hjælp af både hexkoder og URL-adresser til billeder

For de fleste farvedimensioner kan du konfigurere både hexkoder og URL-adresser til billeder. Reservelogik, der er gengivet i Commerce, vil automatisk søge efter enten en hexkode eller en URL-adresse til billeder for at vise en farveprøve. Hvis du både bruger hexkoder og URL-adresser til billeder til at konfigurere farvedimensioner, kan du nemmere udføre billedadministration, når antallet af farver er stort.

I følgende illustration vises et eksempel, hvor der både bruges hexkoder og URL-adresser til billeder til konfigurationen på siden **Farver**.

![Eksempel på dimensionskonfiguration, der både bruger hexkode og URL-adresser til billeder.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Konfigurere afgrænsningsgrupper

Når du definerer en hexkode eller en URL-adresse til et billede for en dimensionsværdi, kan du også angive en værdi for feltet **RefinerGroup**. Dette felt definerer den dimension, der skal bruges til at gruppere lignende dimensionsværdier i afgrænsningsoplevelsen.

Hvis værdierne for farvedimensionen for eksempel er "blå", "blåt tæppe", "blå vask" og "mørkeblå", knyttes de enkelte værdier til en forskellig hexkode eller URL-adresse til billeder. Derfor vises de enkelte værdier som en forskellige farve på PDP'er og produktkort for de relevante produkter. Men hvis du knytter alle disse farvedimensionsværdier til **RefinerGroup**-værdien **Blå**, genererer en søgning efter "blå" produkter søgeresultater på listesiden for produkter, der har dimensionsfarveværdierne "blå", "blåt tæppe", "blå vask" og "mørkeblå".

Eksemplet i følgende illustration viser forholdet mellem egenskaberne **Farve** og **RefinerGroup** i Commerce-hovedkvarteret.

![Eksempel på administration af afgrænsningsgruppe.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Administrere billeder i Commerce-webstedsgeneratoren

Hvis der bruges URL-adresser til billeder til dimensionsværdier, skal de tilsvarende billeder overføres til Commerce-webstedsgeneratoren. Placeringen af de enkelte billeder skal svare til det filnavn og den mappesti, der er defineret for billedet i Commerce-hovedkvarteret. Billedfiler skal overføres til de relevante kategoriplaceringer i webstedsgeneratoren. Farvebilleder skal for eksempel overføres til kategorimappen **Farve**. Du kan finde flere oplysninger om, hvordan du overfører billeder til webstedsgeneratoren, under [Overføre billeder](../dam-upload-images.md).

I følgende illustration vises et eksempel, hvor dialogboksen **Overfør filer** bruges til at overføre billeder til mediebiblioteket til webstedsgeneratoren. Den fremhæver kategorierne **Størrelse**, **Farve** og **Typografi**, der kan vælges.

![Eksempel på billedfilkategorier under overførsel til mediebiblioteket til webstedsgeneratoren.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Aktivere visning af prøve på webstedssider for e-handel

Før prøver kan vises på webstedssider til e-handel, der kræver valg af dimension, for eksempel PDP'er og listesider, skal du konfigurere indstillinger for dimensionswebsteder i Commerce-hovedkvarteret. Du kan finde flere oplysninger under [Anvende webstedsindstillinger for dimensioner](../dimension-settings.md).

Derudover skal du aktivere egenskaben **Medtag produktattributter i søgeresultater** for søgeresultatmoduler. Hvis webstedet bruger brugerdefinerede kategorisider, skal du opdatere de søgeresultatmoduler, der bruges på disse sider, så egenskaben **Medtag produktattributter i søgeresultater** aktiveres. Du kan få flere oplysninger under [Modul til søgeresultater](../search-result-module.md).

## <a name="inventory-awareness-on-swatches"></a>Lagerbaserede farvekort

Farvekort har en valgfri egenskab, der vises tilgængeligheden af lagerbeholdningen for en produktvariantfarve eller dimension. Et produkt sælges f.eks. i flere størrelser, men nogle størrelser er ikke på lager. I dette tilfælde gengives farvekortene anderledes for varer, der ikke er på lager, for at angive, at de ikke er tilgængelige. Denne egenskab er med til at reducere antallet af kundeklik, der kræves for at bestemme produkttilgængelighed.

Farvekortets funktion for lagertilgængelighed kan konfigureres til brug på både produktoplysningssider og søge- eller kategorilistesider, hvor der vises farvekort. Hvis du vil aktivere den, skal du angive egenskaben **Opdater medie for dimensionsvalg** til **Sand** i [mediegallerimodulet](../media-gallery-module.md). Med denne indstilling kan mediegalleribilleder opdateres, når der vælges dimensioner. 

> [!IMPORTANT]
> Farvekortets funktion for lagertilgængelighed er tilgængelig fra og med Commerce version 10.0.21. Det kræver, at Commerce-modulets bibliotekspakkeversion 9.31 er installeret.

I følgende illustration vises et eksempel på lagerbaseret farvekortstørrelse på en på en produktoplysningsside.

![Eksempel på lagerbaseret farvekortstørrelse på en på en produktoplysningsside](../dev-itpro/media/swatch_inventory.png)

## <a name="display-swatches-in-pos-and-other-channels"></a>Få vist prøver i POS og andre kanaler

Commerce har i øjeblikket ikke en standardimplementering, der understøtter visning af farvekort i POS og andre kanaler. Du kan dog implementere visningsfunktionaliteten for farvekort som en udvidelse, da kanal-API'er returnerer de hexkoder og URL-adresser til billeder, der kræves for at gengive farveprøver.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modul til søgeresultater](../search-result-module.md)

[Anvende webstedsindstillinger for dimensioner](../dimension-settings.md)

[Produktdimensioner](../../supply-chain/pim/product-dimensions.md)

[Overfør billede](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
