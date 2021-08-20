---
title: Nomenklatur for produktvariantnumre og -navne
description: Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format.
author: roxanadiaconu
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 87b78b3003a13586b10fac57fb1d39f004efdf1f81c23420614eb3abd1e4a016
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761038"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Nomenklatur for produktvariantnumre og -navne

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format. Den nye nomenklatur har et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og tekstafgrænsningstegn efter eget valg. Du kan også oprette en nomenklatur for produktnavne. Endelig kan du også oprette en nomenklatur til at identificere konfigurationer, der er oprettet af den begrænsningsbaserede produktkonfigurator. Disse nomenklaturer kan indeholde attributter efter eget valg.

De nye nomenklaturer for produktvariantnumre og produktvariantnavne giver dig mulighed for at medtage segmenter i id'erne for produktvarianter. Disse segmenter kan indeholde produktmasternummer og -navn, produktdimensions-id'er og -navne, nummerserier, tekstkonstanter og attributter. Med denne funktion kan du hurtigt finde en bestemt produktvariant, når du opretter en salgsordre eller en indkøbsordre. Du opretter nomenklaturer til både produktvariantnumre og produktvariantnavne ved hjælp af siden **Produktnomenklatur**. Klik på **Administration af produktoplysninger** &gt; **Konfiguration** for at åbne denne side.

## <a name="nomenclature-of-predefined-product-variants"></a>Nomenklatur for foruddefinerede produktvarianter
Der oprettes produktvarianter for produktmastere efter en af de tre konfigurationsteknologier:

-   Foruddefinerede varianter
-   Begrænsningsbaseret
-   Dimensionsbaseret

Hver produktvariant har et nummer og et navn, og nomenklaturerne for produktvariantidentifikation giver dig mulighed for at vælge de segmenter, der skal medtages i hvert produktvariantnummer eller -navn. Du kan vælge følgende segmenter på siden **Produktnomenklatur**:

-   Produktmasternummer
-   Produktmasternavn
-   Nummerserieværdi
-   Tekstkonstant
-   Produktdimensioner
    -   Konfigurations-id eller -navn
    -   Farve-id eller -navn
    -   Størrelses-id eller -navn
    -   Type-id eller -navn

Når du har defineret en nomenklatur for produktvariantidentifikationsnummer, kan du knytte den til en produktdimensionsgruppe. Alle de produktmastere, der refererer til denne produktdimensionsgruppe, vil derfor blive tildelt produktvariantnumre efter nomenklaturen. Men nomenklaturer for produktvariantnavn kan dog ikke knyttes til produktdimensionsgrupper. Du kan også tildele en nomenklatur for produktvariantidentifikation direkte til en produktmaster. I dette tilfælde tildeles de produktvarianter, der hører til produktmasteren, produktvariantnumre og -navne i overensstemmelse med nomenklaturerne.

### <a name="example"></a>Eksempel

En T-shirt (TS1234), der produceres i tre størrelser (S, M, L), fire farver (rød, grøn, blå, gul) og to typer (Polo, V). Derfor er der 24 mulige produktvarianter (= 3 × 4 × 2). Du opretter en nomenklatur for produktvariantnumre, der har følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant: "-"
3.  Farve
4.  Tekstkonstant: "-"
5.  Størrelse
6.  Tekstkonstant: "-"
7.  Type

I dette tilfælde vil produktvariantnummeret for en rød, small, polo T-shirt være TS1234-Rød-Small-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Nomenklatur for begrænsningsbaserede konfigurationer
Til begrænsningsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen. Du kan vælge følgende segmenter på siden **Produktnomenklatur**:

-   Nummerserieværdi
-   Tekstkonstant
-   Attributværdi

Hver komponent i en produktkonfigurationsmodel kan have sin egen konfigurationsnomenklatur. Kun de attributter, der tilhører komponenten, kan anvendes. Attributter fra underkomponenter eller brugerkrav kan ikke anvendes.

### <a name="example"></a>Eksempel

En produktkonfigurationsmodel har en rodkomponent, der har to attributter:

-   Materiale (plast, træ, stål)
-   Længde (10... 100)

Du opretter en konfigurationsnomenklatur, der har følgende segmenter:

1.  Attributværdi: Materiale
2.  Tekstkonstant: "AAA"
3.  Attributværdi: Længde

I dette tilfælde vil konfigurations-id'et for træmateriale, der har en længde på 78, være WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Nomenklatur for dimensionsbaserede konfigurationer
Til dimensionsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen. Du kan vælge følgende segmenter på siden **Produktnomenklatur**:

-   Nummerserieværdi
-   Tekstkonstant
-   Vare i konfigurationsgruppe

Du kan definere en konfigurationsnomenklatur for en stykliste.

### <a name="example"></a>Eksempel

En stykliste indeholder fire styklistelinjer, der er opdelt i to konfigurationsgrupper:

-   Styklistelinje: M0007, Standardkabinet
    -   Variantgruppe: Kabinet
-   Styklistelinje: M0008, Kabinet af topkvalitet
    -   Variantgruppe: Kabinet
-   Styklistelinje: M0021, Forgitter af stof
    -   Variantgruppe: Forgitter
-   Styklistelinje: M0022, Forgitter af metal
    -   Variantgruppe: Forgitter

Du opretter en konfigurationsnomenklatur, der har følgende segmenter:

1.  Variantgruppe: Kabinet
2.  Tekstkonstant: "&"
3.  Variantgruppe: Forgitter

I dette tilfælde vil konfigurations-id'et for et standardkabinet, der har et frontgitter af stof, være M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Nomenklaturen for en kombination af produktvarianter og -konfigurationer
Når du bruger enten begrænsningsbaseret eller dimensionsbaseret konfigurationsteknologi til at konfigurere produktvarianter for en produktmaster, kan produktvariantnumrene for produktvarianterne omfatte nomenklaturen fra konfigurationsdimensionen. Hvis du vil konfigurere varianter, skal du følge disse trin.

1.  Definer en nomenklatur for produktvariantnummer, som indeholder konfigurationsdimensionen på siden **Produktnomenklatur**.
2.  Tildel nomenklaturen til en produktdimensionsgruppe, der har konfigurationsdimensionen.
3.  Definer en konfigurationsnomenklatur for komponenter eller styklister, der skal bruges til at konfigurere produktvarianterne.

Du kan også oprette en nomenklaturer for produktvariantnavne. Produktvariantnavnene kan konfigureres til at indeholde konfigurations-id'et eller -navnet.

### <a name="example-for-constraint-based-configurations"></a>Eksempel på begrænsningsbaserede konfigurationer

I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant "\_"
3.  Variantkonfiguration

Konfigurationsnomenklaturen består af følgende segmenter:

1.  Attributværdi: Materiale
2.  Tekstkonstant: "AAA"
3.  Attributværdi: Længde

Du kan angive følgende værdier for segmenter:

-   Produktmasternummer = **M0099**
-   Materiale = **Plast**
-   Længde = **12**

I dette tilfælde er produktvariantnummeret M0099\_PlastAAA12.

### <a name="example-for-dimension-based-configurations"></a>Eksempel på dimensionsbaserede konfigurationer

I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant "//"
3.  Variantkonfiguration

Konfigurationsnomenklaturen består af følgende segmenter:

1.  Variantgruppe: Kabinet
2.  Tekstkonstant: "&"
3.  Variantgruppe: Forgitter

Du kan angive følgende værdier for segmenter:

-   Produktmasternummer = **D0123**
-   Kabinet = **M0008**
-   Frontgitter = **M0022**

I dette tilfælde er produktvariantnummeret D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummerkonflikter
I nogle tilfælde resulterer en nomenklatur for produktvariantnummer, som du konfigurerer, muligvis ikke i entydige produktvariantnumre. F.eks. er produktvariantnumrene ikke entydige, hvis én aktiv produktdimension ikke er inkluderet i nomenklaturen for en produktmaster, der bruger foruddefineret variantkonfigurationsteknologi. Hvordan du håndterer konflikter varierer, afhængigt af konfigurationsteknologien.

### <a name="predefined-variants"></a>Foruddefinerede varianter

Der opstår en fejl, hvis du forsøger manuelt eller automatisk at generere produktvarianter, hvor en eller flere produktvarianter ender med at have det samme produktvariantnummer. Hvis du vil undgå denne situation, skal du bruge alle aktive produktdimensioner i produktdimensionsgruppen. Du kan også inkludere en nummerserie for at sikre, at produktvariantnumrene er entydige.

### <a name="constraint-based-configurations"></a>Begrænsningsbaserede konfigurationer

Afhængigt af nomenklaturen vil systemet muligvis forsøge at tildele en konfiguration et ikke-entydigt produktvariantnummer. I dette tilfælde bruger systemet i stedet for nummerserien for konfigurationsdimensionen som produktvariantnummer, og du får vist advarsel. Hvis du vil undgå dette scenarie, skal du medtage tilstrækkelig mange attributter i nomenklaturen til at sikre entydige produktvariantnumre. Du skal også kontrollere, at indstillingen **Genbrug** er slået til for komponenten.

### <a name="dimension-based-configurations"></a>Dimensionsbaserede konfigurationer

Under ét trin af konfigurationsprocessen, foreslår systemet en konfigurationsværdi i overensstemmelse med nomenklaturen. I dette trin kan du manuelt ændre konfigurationsværdien. Når du gemmer konfigurationen, undersøges det, om konfigurationsværdien er entydig. Hvis den indtastede værdi ikke er entydig, får du vist en fejlmeddelelse. Du skal angive en unik konfigurationsværdi for at kunne gemme konfigurationen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et produktnummernomenklatur for foruddefinerede produktvarianter](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Opret en nomenklatur for produktnumre for konfigurerede produktvarianter](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]