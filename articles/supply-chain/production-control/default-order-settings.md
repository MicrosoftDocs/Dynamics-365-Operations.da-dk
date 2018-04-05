---
title: Standardordreindstillinger for dimensioner og produktvarianter
description: "Standardindstillinger for ordre definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: d0e8d1ac8b775f9c728d6bfa6ba219dd889bf8a2
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standardordreindstillinger for dimensioner og produktvarianter

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Standardindstillinger for ordre i Microsoft Dynamics 365 for Finance and Operations definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn. Standardordreindstillinger bruges, når du opretter indkøbsordrer, salgsordrer, flytteordrer, lagerkladder og ved varedisponering til at generere ordreforslag. Standardindstillinger for ordre kan være varespecifikke, lokationsspecifikke, specifikke for produktvariant eller produktdimensionsbestemte.

Du kan definere standardindstillinger af ordre på siden **Standardindstillinger for ordre**. Hvis du vil åbne denne side, skal du gå til **Administration af produktoplysninger** &gt; **Produkter** &gt; **Frigivne produkter** &gt; **Vælg et frigivet produkt** &gt; i handlingsruden **Plan** eller **Styr lager** &gt; **Ordreindstillinger** &gt; **Standardindstillinger for ordre**.

## <a name="default-order-settings"></a>Standardindstillinger for ordre
Der findes tre typer standardordreindstillinger for køb, salg og lager. Standardordreindstillingerne for køb bruges, når du opretter:

-   Indkøbsordrelinjer
-   Linjer i købsaftale
-   Tilbudsanmodningslinjer
-   Indkøbsrekvisitionslinjer
-   Genopfyldningslinjer til konsignation
-   Indkøbsordreforslag

Standardordreindstillingerne for salg bruges, når du opretter:

-   Salgsordrelinjer
-   Linjer i salgsaftale
-   Salgstilbudslinjer
-   Returordrelinjer og vareerstatningslinjer
-   Behovsprognoselinjer

Salgsordres standardindstillinger gælder også, når du opretter:

-   Varebehov for projekt
-   Varebehov på serviceordre

Standardordreindstillingerne for lager bruges, når du opretter:

-   Lagerkladder
-   Flytteordrer
-   Planlagte flytteordrer

Lagerordres standardindstillinger gælder også, når du opretter:

-   Karantæneordrer
-   Kvalitetsordrer
-   Produktionsordrer
-   Styklistelinjer
-   Produktionsordreforslag

## <a name="full-definition-of-a-released-product"></a>Fuld definition af et frigivet produkt
Når du opretter en postering, skal du angive den fulde definition af et frigivet produkt på linjen, før Finance and Operations forsøger at identificere standardordreindstillingerne. Fuld definitionen af frigivet produkt betyder, at varenummeret og alle de aktive produktdimensioner, f.eks. konfiguration, størrelse, typografi og farve, er angivet på posteringen. For eksempel hvis du manuelt opretter en indkøbsordrelinje for en frigiet produktvariant, skal du angive alle nødvendige produktdimensioner, før lokation, lagersted, mængder og gennemløbstid vises som standard på ordrelinjen. 

Ikke alle standardparametre til ordreindstillinger anvendes ved oprettelse af ordre- eller kladdelinjer. Antal og leveringstider vises kun som standard, når det er relevant. Eksempelvis ved optælling en kladdelinje vises lokation og lagersted som standard, når linjen er oprettet. Naturligvis bliver ingen antalstandard eller kontrol af flere eller minimum udført ved oprettelse af linjen eller bogføring af kladden. 

Systemet forsøger altid at finde en standardlokation og et lagersted, når der oprettes en ordre eller kladdelinje. Lokation vises ikke altid som standard fra ordreindstillinger. For eksempel når du opretter en salgsordre eller en indkøbsordre, bruges lokationen fra ordrehovedet automatisk på ordrelinjerne. Når du opretter en styklistelinje, bruges lokationen i styklistens hoved. Når lokationen er bestemt, bruges den til at finde lokationsspecifikke ordreindstillinger, der kan bruges som standard for lagerstedet. 

Standardordretypen, købet og lagerleveringstiderne kan tilsidesættes af disponeringsregler for varen på siden **Varedisponering**. Selvom standardordreindstillingerne ikke tillader en skelnen mellem produktion og overflytningstid, kan disponeringsreglerne for varen tillade den. Men opsætningen af varedisponering bruges kun af MPR, når du opretter planlagte produktions- og planlagte flytteordrer og vil ikke gælde, når du manuelt opretter produktions- og flytteordrer. 

## <a name="default-order-settings-rules"></a>Standardregler for ordreindstillinger
Du kan definere generelle standardindstillinger for ordre og et vilkårligt antal standardregler for ordreindstilling, der kun gælder på visse betingelser, såsom lokation eller en bestemt produktdimension eller kombination af produktdimensioner. Du kan ikke definere lagerstedsspecifikke ordreindstillinger.

### <a name="rank-in-default-order-settings"></a>Rangering af indstillinger for standardordrer

Standardregler for ordreindstillinger har rang. Jo højere rang, desto vigtigere er reglen, hvilket betyder, at den har en højere prioritet og anvendes før regler med lavere rang. Generelle standardordreindstillingerne har rang nul, som ikke kan ændres. Der kan kun være én regel med rang 0. Regler kan have samme rang, forudsat at dimensionerne, de gælder for, er forskellige. Dette er nyttigt til modellering af lokationsspecifikke ordreindstillinger. Når en ny standardregel for ordreindstillinger oprettes, bliver værdierne for ordreværdier, stopflaget osv. arvet fra reglen med rang nul, men kan tilsidesættes.

### <a name="default-order-settings-for-released-products"></a>Standardordreindstillinger for frigivne produkter

Du kan definere generelle ordreindstillinger eller lokationsspecifikke ordreindstillinger for specifikke frigivne produkter. Generelle ordreindstillinger har altid rang nul. Hvis du opretter nye salgs-, købs- og lagerordreindstillinger samlet på samme tid, anbefaler vi, at du bruger **Detaljevisning** på siden **Standardindstillinger for ordre**. Hvis du vil skifte til detaljeret visning, skal du gå til **Indstillinger**-handlingsruden &gt; **Sideindstillinger** &gt; **Skift visning** &gt; **Detaljevisning**.

### <a name="site-specific-order-settings"></a>Stedspecifikke ordreindstillinger

Du kan oprette lokationsspecifikke ordreindstillinger ved at klikke på **Ny**. I **Detaljevisning** skal du udfylde lokationen i **Indstillinger gældende for** &gt; feltet **Lokation**. I **Gittervisning** skal du udfylde lokationen i **Lokation**-kolonnen. Den nye regel får automatisk en ny rangværdi, der er højere end nul. Du kan oprette så mange lokationsspecifikke regler, du vil, og du kan tildele alle reglerne samme rang for at modellere, at de er lige vigtige. 

Hvis du er i **Detaljevisning**, kan du ikke få overblik over de regler, der er oprettet for varen. Skift knappen **Vis/skjul liste** for at se oversigtsoplysninger. Når der oprettes en ordrelinje af enhver type, og den ikke har nogen lokation angivet, søger Finance and Operations efter en regel uden angivet lokation. Dette kan hjælpe med at bestemme standardlokationen på ordrelinjen. Denne lokation bruges derefter til at søge efter en lokationsspecifik regel, hvor et standardlagersted kan være angivet. Dette lagersted anvendes på ordrelinjen.

### <a name="specific-order-settings-for-product-dimension"></a>Specifikke ordreindstillinger for produktdimension

Du kan definere ordreindstillingsregler for enhver aktiv produktdimension eller en kombination af aktive produktdimensioner. Hvis et felt til produktdimension er tomt, gælder reglen for alle værdier i produktdimensionen. 

Se på følgende produkteksempel.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produktnavn**                                    | Fotoelektrisk sensor                    |
| **Varenummer**                                     | XW56                                    |
| **Konfiguration** (bruges til at modellere lystypen) | C1-Synligt rødt lys, C2-Infrarødt lys |
| **Skabelon** (bruges til at modellere teknisk revision)  | R1, R2, R3                              |

I dette eksempel antages det, at produktet er indkøbt og ikke fremstillet. Det antages desuden, at konfigurationen C1 bruges mest, så den har kortere leveringstider. 

Opret følgende standardordreindstillinger til modellen i dette scenario.

| Ranger | Sted | Variantkonfiguration | Skabelon | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Når en indkøbsordrelinje eller en planlagt indkøbsordre oprettes for XW56, konfiguration C1, betragtes leveringstiden 2 uanset revision eller lokation, hvor linjen er placeret. Lad os antage, at alle revisioner udover R3 er standset.

Du kan oprette følgende standardregler for ordreindstillinger:

| Ranger | Sted | Variantkonfiguration | Skabelon | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | R1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De to regler til at stoppe de gamle revisioner har samme rangorden, hvilket betyder, at de er lige vigtige. Begge af dem har en højere rang end reglen for konfiguration C1, hvilket betyder, at de tilsidesætter reglen til C1-konfiguration. 

Dette eksempel forklarer behovet for rang. Hvis der oprettes en indkøbsordre for konfiguration C1 og revision R2, er, i mangel af rang, de to regler, der er defineret for R2 og C1, tvetydige. For at løse tvetydigheden, søger Finance and Operations gennem regler i faldende rækkefølge efter rang og anvender den første relevante regel. I det aktuelle eksempel, når der oprettes en indkøbsordrelinje for konfiguration C1 og revision R2, får brugeren en advarsel om, at varen er på hold, og at dette er forårsaget af revisionsværdien. Hvis reglen for konfigurationen havde en højere rang end den til revision, ville oprettelsen af en indkøbsordrelinje for konfiguration C1 og revision R2 have lykkedes, og ingen meddelelse "vare på hold" ville være givet til brugeren. 

Se på følgende standardregler for ordreindstilling.

| Ranger | Sted | Variantkonfiguration | Skabelon | Standardsted | Standardlagersted | Køb - Tilsidesæt standardlagringsdimensioner | Lagersted for indkøb |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systemet kører gennem regelsættet to gange for at fastslå lokation og lagersted. Når der oprettes en indkøbsordrelinje for konfiguration C1, typografi R2, bestemmes lokationen baseret på reglen med rang 10. Derefter søger systemet efter en regel for lokation 2 for at bestemme et lagersted. Reglen 20 er fundet, og fordi den har en højere rang, bliver lagerstedet på købsordrelinjen 22, og ikke 21. 

Som en generel retningslinje får specifikke regler og regler for dimensioner, der er vigtigere end andre dimensioner, højere rang, mens mere generiske regler får lavere rang. 

Reglen med rang nul fungerer som et sikkerhedsnet. Hvis ingen andre regler findes, bruges standardindstillinger for ordre fra regel nul. 

Da rangnummeret er så vigtigt, har **Standardindstillinger for ordre**-handlingsruden funktioner til at flytte en regel op eller ned og til at omnummerere reglerne, så de altid er i trin på 10. 

Antallet af regler, der er oprettet for et frigivet produkt, kan være mange. For at få en bedre ide om, hvad hver enkelt regel tilsidesætter, og hvorfor det er nødvendigt, anbefales du at bruge **Gittervisning** på siden **Standardindstillinger for ordre**. Du kan aktivere gittervisning ved at gå til **Indstillinger**-handlingsruden &gt; **Sideindstillinger** &gt; **Skift visning** &gt; **Gittervisning**. Antallet af kolonner, der vises i gitteret, kan være ret afgørende, især i forbindelse med salgs- og lagerfaner. Hvis du vil begrænse antallet kolonner, der vises i gitteret, kan grupper af kolonner skjules eller vises ved hjælp af knapperne i menuen **Standardindstillinger for ordre** &gt; **Kolonnevisning**.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifikke ordreindstillinger for frigiven produktvariant

Hvis regelsystemet for standardordreindstillinger er for tungt, er der mulighed for at definere standardordreindstillingerne for hver produktvariant. Følgende eksempler viser, hvordan det ser ud til produktet og de tilfælde, der er beskrevet ovenfor.

| Ranger | Sted | Variantkonfiguration | Skabelon | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | R1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Rang har i dette tilfælde ingen virkelig betydning, så du kan vælge at skjule den. Denne løsning giver potentielt et vedligeholdelsesproblem. Dog kan du overveje at bruge denne opsætning, hvis du skal integrere med Product Lifecycle Management-systemer (PLM).




