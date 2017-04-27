---
title: Nomenklatur for produktnummer
description: "Dette emne beskriver, hvordan du kan konfigurere en produktnummernomenklatur til at erstatte det faste format [Produktmasternummer – Konfiguration – Størrelse – Farve – Type], med et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og afgrænsere i tekst efter eget valg. Du kan også oprette en nomenklatur for at identificere konfigurationer, der er oprettet af begrænsningsbaseret produktkonfiguration. Disse nomenklaturer kan indeholde attributter efter eget valg."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Nomenklatur for produktnummer

[!include[banner](../includes/banner.md)]


Dette emne beskriver, hvordan du kan konfigurere en produktnummernomenklatur til at erstatte det faste format [Produktmasternummer – Konfiguration – Størrelse – Farve – Type], med et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og afgrænsere i tekst efter eget valg. Du kan også oprette en nomenklatur for at identificere konfigurationer, der er oprettet af begrænsningsbaseret produktkonfiguration. Disse nomenklaturer kan indeholde attributter efter eget valg.

Med den nye nomenklatur fpr produktvariantnummer kan du medtage segmenter i dine produktvariant-id'er. Disse segmenter kan indeholde produktmasternummer, produktdimensioner, nummerserier, tekstkonstanter og attributter. Med denne funktion kan du hurtigt finde en bestemt produktvariant, når du opretter en salgsordre for indkøbsordre.

## <a name="nomenclature-of-predefined-product-variants"></a>Nomenklatur for foruddefinerede produktvarianter
Der oprettes produktvarianter for produktmastere efter en af de tre konfigurationsteknologier:

-   Foruddefinerede varianter
-   Begrænsningsbaseret
-   Dimensionsbaseret

Hver produktvariant har et nummer, og med nomenklaturen for produktvariantidentifikation kan du vælge de segmenter, der skal medtages i hvert produktvariantnummer. Du kan vælge følgende segmenter på siden **Produktnomenklatur**.

-   Produktmasternummer
-   Nummerserieværdi
-   Tekstkonstant
-   Produktdimensioner
    -   Variantkonfiguration
    -   Farve
    -   Størrelse
    -   Skabelon

Når en nomenklatur for produktvariantidentifikation er defineret, kan den være knyttet til en produktdimensionsgruppe. Alle de produktmastere, der refererer til denne produktdimensionsgruppe, vil derfor blive tildelt produktvariantnumre efter nomenklaturen. Det er også muligt at tildele nomenklatur for produktvariantidentifikation direkte til en produktmaster, i hvilket tilfælde de produktvarianter, der tilhører denne master, tildeles produktvariantnumre efter nomenklaturen.

### <a name="example"></a>Eksempel

En T-shirt (TS1234) er produceret i 3 forskellige størrelser (S, M, L), 4 forskellige farver (rød, grøn, blå, gul) og 2 typer (Polo, V), der giver i alt 24 mulige produktvarianter. En nomenklatur for produktvariantidentifikation er oprettet med følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant: '-'
3.  Farve
4.  Tekstkonstant: '-'
5.  Størrelse
6.  Tekstkonstant: '-'
7.  Skabelon

Produktvariantnummeret for Rød, Small, Polo vil være: TS1234-Rød-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenklatur for begrænsningsbaserede konfigurationer
En dedikeret nomenklatur kan bygges for konfigurationsproduktdimensionen for begrænsningsbaserede konfigurationer. Du kan vælge følgende segmenter på siden **Produktnomenklatur**.

-   Nummerserieværdi
-   Tekstkonstant
-   Attributværdi 

Hver komponent i en produktkonfigurationsmodel kan have sin egen konfigurationsnomenklatur. Kun de attributter, der tilhører komponenten, kan anvendes. Attributter fra underkomponenter eller brugerkrav er ikke tilgængelige.

### <a name="example"></a>Eksempel

En produktkonfigurationsmodel har en rodkomponent med to attributter.

-   Materiale (plast, træ, stål)
-   Længde (10... 100)

En konfigurationsnomenklatur er defineret ved hjælp af følgende segmenter:

1.  Attributværdi: Materiale
2.  Tekstkonstant: 'AAA'
3.  Attributværdi: Længde

Konfigurations-id for træmateriale med en længde på 78 får følgende konfigurations-id: TræAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenklatur for dimensionsbaserede konfigurationer
En dedikeret nomenklatur kan bygges for konfigurationsproduktdimensionen for dimensionsbaserede konfigurationer. Du kan vælge følgende segmenter på siden **Produktnomenklatur**.

-   Nummerserieværdi
-   Tekstkonstant
-   Vare i konfigurationsgruppe

En konfigurationsnomenklatur kan defineres for en stykliste.

### <a name="example"></a>Eksempel

En stykliste har 4 styklistelinjer, der er opdelt i 2 variantgrupper.

-   Styklistelinje: M0007, Standardkabinet
    -   Variantgruppe: Kabinet
-   Styklistelinje: M0008, Kabinet af topkvalitet
    -   Variantgruppe: Kabinet
-   Styklistelinje: M0021, Forgitter af stof
    -   Variantgruppe: Forgitter
-   Styklistelinje: M0022, Forgitter af metal
    -   Variantgruppe: Forgitter

En konfigurationsnomenklatur er defineret ved hjælp af følgende segmenter:

1.  Variantgruppe: Kabinet
2.  Tekstkonstant: '&'
3.  Variantgruppe: Forgitter

Konfigurations-id for et standardkabinet med forgitter af stof bliver: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Nomenklaturen for en kombination af konfigurationer og produktvarianter
Når du bruger enten begrænsningsbaseret eller dimensionsbaseret konfigurationsteknologi til at konfigurere produktvarianter for en produktmaster, kan produktvarianterne-får produktvariantnumre, der omfatter nomenklaturen fra konfigurationsdimensionen. Hvis du vil konfigurere varianter, skal du følge disse trin:

1.  Definer en nomenklatur for produktvariantnummer, som indeholder konfigurationsdimensionen på siden **Produktnomenklatur**.
2.  Tildel en produktdimensionsgruppe med konfigurationsdimensionen denne nomenklatur.
3.  Definer en konfigurationsnomenklatur for komponenter eller styklister, der skal bruges til at konfigurere produktvarianter.

### <a name="example-for-constraint-based-configurations"></a>Eksempel på begrænsningsbaserede konfigurationer

I dette eksempel kan du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant '\_'
3.  Variantkonfiguration

Konfigurationsnomenklaturen kan bestå af følgende segmenter:

1.  Attributværdi: Materiale
2.  Tekstkonstant: 'AAA'
3.  Attributværdi: Længde

Du kan angive følgende værdier for segmenter:

-   Produktmasternummer = M0099
-   Materiale = Plast
-   Længde = 12

Produktvariantnummeret bliver: M0099\_PlastAAA12.

### <a name="example-for-dimension-based-configurations"></a>Eksempel på dimensionsbaserede konfigurationer

I dette eksempel kan du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:

1.  Produktmasternummer
2.  Tekstkonstant '//'
3.  Variantkonfiguration

Konfigurationsnomenklaturen kan bestå af følgende segmenter:

1.  Variantgruppe: Kabinet
2.  Tekstkonstant: '&'
3.  Variantgruppe: Forgitter

Du kan angive følgende værdier for segmenter:

-   Produktmasternummer = D0123
-   Kabinet = M0008
-   Frontgitter = M0022

Produktvariantnummeret bliver: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummerkonflikter
Det er muligt at konfigurere en nomenklatur for produktvariantnummer, der ikke resulterer i unikke produktvariantnumre. Eksempelvis kan dette ske, hvis en aktiv produktdimension ikke er inkluderet i nomenklaturen for en produktmaster, der bruger foruddefineret variantkonfigurationsteknologi. Konflikter håndteres forskelligt for de forskellige konfigurationsteknologier.

### <a name="predefined-variants"></a>Foruddefinerede varianter

Der opstår en fejl, hvis du forsøger manuelt eller automatisk at generere produktvarianter, hvor en eller flere afsluttes med samme produktvariantnummer. For at undgå dette skal du bruge alle aktive produktdimensioner i produktdimensionsgruppen eller medtage en nummerserie for at sikre, at produktvariantnumrene er entydige.

### <a name="constraint-based-configurations"></a>Begrænsningsbaserede konfigurationer

Afhængigt af nomenklaturen vil systemet forsøge at skal tildele en konfiguration et ikke-entydigt produktvariantnummer. I dette tilfælde bruges nummerserien for konfigurationsdimensionen som produktvariantnummer i stedet. Hvis dette sker, får du en advarsel. For at undgå dette skal du medtage nok attributter i nomenklaturen for at sikre entydighed, og sørg for, at indstillingen **Genbrug** er slået til for komponenten.

### <a name="dimension-based-configurations"></a>Dimensionsbaserede konfigurationer

Konfigurationsprocessen omfatter et trin, hvor systemet foreslår en konfigurationsværdi i overensstemmelse med nomenklaturen. I dette trin kan du manuelt ændre konfigurationsværdien. Når du gemmer konfigurationen, undersøges det, om konfigurationsværdien er entydig. Hvis dette ikke er tilfældet, vises en fejl. Du skal angive en unik konfigurationsværdi for at gemme konfigurationen.



<a name="see-also"></a>Se også
--------

[Opret en nomenklatur for produktnumre for foruddefinerede produktvarianter (opgaveguide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Opret en nomenklatur for produktnumre for konfigurerede produktvarianter (opgaveguide)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




