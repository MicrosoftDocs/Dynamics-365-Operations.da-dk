---
title: Standardordreindstillinger for dimensioner og produktvarianter
description: Standardindstillinger for ordre definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn.
author: t-benebo
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 5cdba1b3aaa121eed3b8f870d21aa7e58d2c7b14aa25563cd437d3769b35e872
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750046"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standardordreindstillinger for dimensioner og produktvarianter

[!include [banner](../includes/banner.md)]

Standardindstillinger for ordrer i Dynamics 365 Supply Chain Management definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum- og maksimumantal, flere antal og standard antal, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn. Standardordreindstillinger bruges, når du opretter indkøbsordrer, salgsordrer, flytteordrer, lagerkladder og ved varedisponering til at generere ordreforslag. Standardindstillinger for ordre kan være varespecifikke, lokationsspecifikke, specifikke for produktvariant eller produktdimensionsbestemte.

Benyt følgende fremgangsmåde for at definere standardindstillingerne for produktordrer.

1. Gå til **Administration af produktoplysninger** &gt; **Produkter** &gt; **Frigivne produkter**.
1. Vælg det relevante produkt i gitteret.
1. Benyt en af følgende fremgangsmåder i handlingsruden for at åbne siden **Standardordreindstillinger** for det valgte produkt:

    - På fanen **Plan** i gruppen **Ordreindstillinger** skal du vælge **Standardordreindstillinger**.
    - På fanen **Administrer lager** i gruppen **Ordreindstillinger** skal du vælge **Standardordreindstillinger**.

1. Konfigurer indstillingerne som beskrevet i resten af dette emne.

## <a name="default-order-settings"></a>Standardindstillinger for ordre

Der findes tre typer standardordreindstillinger for køb, salg og lager. Standardordreindstillingerne for køb bruges, når du opretter:

- Indkøbsordrelinjer
- Linjer i købsaftale
- Tilbudsanmodningslinjer
- Indkøbsrekvisitionslinjer
- Genopfyldningslinjer til konsignation (delvist understøttet, se note)
- Indkøbsordreforslag

> [!NOTE]
> I forbindelse med genopfyldningsordrelinjer til konsignation er de eneste indstillinger fra oversigtspanelet **Indkøbsordre** på siden **Standardindstillinger for ordre**, der anvendes, feltet **Standardsted**, feltet **Standardlagersted** og afkrydsningsfeltet **Stoppet**.

Standardordreindstillingerne for salg bruges, når du opretter:

- Salgsordrelinjer
- Linjer i salgsaftale
- Salgstilbudslinjer
- Returordrelinjer og vareerstatningslinjer
- Behovsprognoselinjer

Salgsordres standardindstillinger gælder også, når du opretter:

- Varebehov for projekt
- Varebehov på serviceordre

Standardordreindstillingerne for lager bruges, når du opretter:

- Lagerkladder
- Flytteordrer
- Planlagte flytteordrer

Lagerordres standardindstillinger gælder også, når du opretter:

- Karantæneordrer
- Kvalitetsordrer
- Produktionsordrer
- Styklistelinjer
- Produktionsordreforslag

## <a name="full-definition-of-a-released-product"></a>Fuld definition af et frigivet produkt

Når du opretter en transaktion, skal du angive den fulde definition af et frigivet produkt på linjen, så Supply Chain Management kan forsøge at identificere standardordreindstillingerne. I den fulde definition af et frigivet produkt angives varenummeret og alle de aktive produktdimensioner, f.eks. konfiguration, størrelse, typografi, version og farve, er på transaktionen. Hvis du f.eks. manuelt opretter en indkøbsordrelinje for en frigiet produktvariant, skal du angive alle nødvendige produktdimensioner, før lokationen, lagerstedet, mængderne og gennemløbstiden vises som standard på ordrelinjen. 

Ikke alle standardparametre til ordreindstillinger anvendes ved oprettelse af ordre- eller kladdelinjer. Antal og leveringstider vises kun som standard, når det er relevant. Eksempelvis ved optælling en kladdelinje vises lokation og lagersted som standard, når linjen er oprettet. Derfor er der intet standardantal eller kontrol af multiplum eller minimum udført ved oprettelse af linjen eller bogføring af kladden. 

Systemet forsøger altid at finde en standardlokation og et lagersted, når der oprettes en ordre eller kladdelinje. Lokation vises ikke altid som standard fra ordreindstillinger. For eksempel når du opretter en salgsordre eller en indkøbsordre, bruges lokationen fra ordrehovedet automatisk på ordrelinjerne. Når du opretter en styklistelinje, bruges lokationen i styklistens hoved. Når lokationen er bestemt, bruges den til at finde lokationsspecifikke ordreindstillinger, der kan bruges som standard for lagerstedet. 

Standardordretypen, købet og lagerleveringstiderne kan tilsidesættes af disponeringsregler for varen på siden **Varedisponering**. Selvom standardordreindstillingerne ikke tillader en skelnen mellem produktion og overflytningstid, kan disponeringsreglerne for varen tillade den. Men opsætningen af varedisponering bruges kun af Varedisponering (MPR), når du opretter planlagte produktions- og planlagte flytteordrer og vil ikke gælde, når du manuelt opretter produktions- og flytteordrer. 

## <a name="default-order-settings-rules"></a>Standardregler for ordreindstillinger

Du kan definere generelle standardindstillinger for ordre og et vilkårligt antal standardregler for ordreindstilling, der kun gælder på visse betingelser, såsom lokation eller en bestemt produktdimension eller kombination af produktdimensioner. Du kan ikke definere lagerstedsspecifikke ordreindstillinger.

### <a name="rank-in-default-order-settings"></a>Rangering af indstillinger for standardordrer

Standardregler for ordreindstillinger har rang. Jo højere rang, desto vigtigere er reglen, hvilket betyder, at den har en højere prioritet og anvendes før regler med lavere rang. Generelle standardordreindstillingerne har rang nul, som ikke kan ændres. Der kan kun være én regel med rang 0. Regler kan have samme rang, forudsat at dimensionerne, de gælder for, er forskellige. Dette er nyttigt til modellering af lokationsspecifikke ordreindstillinger. Når en ny standardregel for ordreindstillinger oprettes, bliver værdierne for ordreværdier, stopflaget osv. arvet fra reglen med rang nul, men kan tilsidesættes.

### <a name="default-order-settings-for-released-products"></a>Standardordreindstillinger for frigivne produkter

Du kan definere generelle ordreindstillinger eller lokationsspecifikke ordreindstillinger for specifikke frigivne produkter. Generelle ordreindstillinger har altid rang nul. Hvis du opretter nye salgs-, købs- og lagerordreindstillinger samlet på samme tid, anbefaler vi, at du bruger **Detaljevisning** på siden **Standardindstillinger for ordre**. Hvis du vil skifte til detaljeret visning, skal du gå til **Indstillinger** &gt; **Sideindstillinger** &gt; **Skift visning** &gt; **Detaljevisning**.

### <a name="site-specific-order-settings"></a>Lokationsspecifikke ordreindstillinger.

Du kan oprette lokationsspecifikke ordreindstillinger ved at vælge **Ny**. I **Detaljevisning** skal du indtaste lokationen i feltet **Lokation** i sektionen **Indstillinger gældende for**. I **Gittervisning** skal du angive lokationen i kolonnen **Lokation**. Den nye regel tildeles automatisk en ny rangeringsværdi, der er større end 0 (nul). Du kan oprette lige så mange lokationsspecifikke regler, du har brug for. Hvis du vil angive, at de er lige vigtige, kan du tildele samme rangeringsværdi til alle lokationsspecifikke regler.

Hvis du er i **Detaljevisning**, kan du ikke få overblik over de regler, der er oprettet for varen. Brug knappen **Vis/skjul liste** for at se oversigtsoplysninger. Når der oprettes en ordrelinje af enhver type, og den ikke har nogen lokation angivet, søger Supply Chain Management efter en regel uden angivet lokation. Dette hjælper med at bestemme standardlokationen på ordrelinjen. Denne lokation bruges derefter til at søge efter en lokationsspecifik regel, hvor et standardlagersted kan være angivet. Dette lagersted anvendes på ordrelinjen.

### <a name="specific-order-settings-for-product-dimension"></a>Specifikke ordreindstillinger for produktdimension

Du kan definere ordreindstillingsregler for enhver aktiv produktdimension eller en kombination af aktive produktdimensioner. Hvis et felt til produktdimension er tomt, gælder reglen for alle værdier i produktdimensionen. 

Se på følgende produkteksempel.

| Post                                                | Værdi                                   |
|-----------------------------------------------------|-----------------------------------------|
| **Produktnavn**                                    | Fotoelektrisk sensor                    |
| **Varenummer**                                     | XW56                                    |
| **Konfiguration** (bruges til at modellere lystypen) | C1-Synligt rødt lys, C2-Infrarødt lys |
| **Version** | V1, V2, V3                              |

I dette eksempel antages det, at produktet er indkøbt og ikke fremstillet. Det antages desuden, at konfigurationen C1 bruges mest, så den har kortere leveringstider. 

Opret følgende standardordreindstillinger til modellen i dette scenario.

| Ranger | Lokation | Variantkonfiguration | Version | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Når en indkøbsordrelinje eller en planlagt indkøbsordre oprettes for varen XW56, konfigurationen C1, betragtes gennemløbstiden som 2 uanset versionen eller den lokation, hvor linjen placeres. Lad os antage, at alle versioner udover V3 er standset.

Du kan oprette følgende standardregler for ordreindstillinger:

| Ranger | Lokation | Variantkonfiguration | Version | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | V1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De to regler for standsning af de gamle versioner har samme placering. Derfor er de lige vigtige. Fordi begge regler har en højere rangering end reglen for konfigurationen C1, tilsidesætter de reglen for konfigurationen C1. 

Dette eksempel forklarer behovet for rang. Hvis rangeringen ikke anvendes, når en indkøbsordre oprettes for konfigurationen C1 og versionen V2, vil de to regler, der er defineret for V2 og C1, være tvetydige. For at løse tvetydigheden, søger Supply Chain Management gennem regler i faldende rækkefølge efter rang og anvender den første relevante regel. I det aktuelle eksempel, hvor der oprettes en indkøbsordrelinje for konfigurationen C1 og versionen V2, modtager brugeren en advarsel om, at varen er på hold, og at dette skyldes versionsværdien. Hvis reglen for konfigurationen havde en højere rangering end reglen for versionen, oprettes der af en korrekt indkøbsordrelinje for konfigurationen C1 og versionen V2, og brugeren vil modtage en meddelelse om "vare på hold". 

Se på følgende standardregler for ordreindstilling.

| Ranger | Lokation | Variantkonfiguration | Version | Standardsted | Standardlagersted | Køb - Tilsidesæt standardlagringsdimensioner | Lagersted for indkøb |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systemet kører gennem regelsættet to gange for at fastslå lokation og lagersted. Når der oprettes en indkøbsordrelinje for konfigurationen C1, versionen V2, bestemmes lokationen baseret på den regel, der har en rangering på 10. Systemet søger derefter efter en regel for lokation 2 for at bestemme et lagersted. Reglen 20 er fundet, og fordi den har en højere rangering, vil lagerstedet på indkøbsordrelinjen være 22 og ikke 21.

Som en generel retningslinje får specifikke regler og regler for dimensioner, der er vigtigere end andre dimensioner, højere rang, mens mere generiske regler får lavere rang. 

Reglen med rang nul fungerer som et sikkerhedsnet. Hvis ingen andre regler findes, bruges standardindstillinger for ordre fra regel nul. 

Da rangnummeret er så vigtigt, har **Standardindstillinger for ordre**-handlingsruden funktioner til at flytte en regel op eller ned og til at nummerere reglerne igen, så de altid er i trin på 10. 

Antallet af regler, der er oprettet for et frigivet produkt, kan være mange. For at få en bedre forståelse for, hvad hver enkelt regel tilsidesætter, og hvorfor det er nødvendigt, anbefales du at bruge **Gittervisning** på siden **Standardindstillinger for ordre**. Du kan aktivere gittervisning ved at gå til **Indstillinger** &gt; **Sideindstillinger** &gt; **Skift visning** &gt; **Gittervisning**. Antallet af kolonner, der vises i gitteret, kan være ret afgørende, især i forbindelse med salgs- og lagerfaner. Hvis du vil begrænse antallet kolonner, der vises i gitteret, kan grupper af kolonner skjules eller vises ved hjælp af knapperne i menuen **Standardindstillinger for ordre** &gt; **Kolonnevisning**.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifikke ordreindstillinger for frigiven produktvariant

Hvis regelsystemet for standardordreindstillinger er for tungt, er der mulighed for at definere standardordreindstillingerne for hver produktvariant. Følgende eksempel viser, hvordan det ser ud til produktet og de tilfælde, der er beskrevet ovenfor.

| Ranger | Lokation | Variantkonfiguration | Version | Køb - Tilsidesæt standardindstillinger | Leveringstid for indkøb | Køb - Standset | Salg - Tilsidesæt standardindstillinger | Salg - Standset |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | V1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Rang har i dette tilfælde ingen virkelig betydning, så du kan vælge at skjule den. Denne løsning giver potentielt et vedligeholdelsesproblem. Dog kan du overveje at bruge denne opsætning, hvis du skal integrere med Product Lifecycle Management-systemer (PLM).

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Bruge streng validering eller standardvalidering af standardordreantal

Du kan vælge, hvor restriktiv systemet skal være, når der skal valideres mængder, der er angivet i **Standardordreindstillinger** for et produkt. Når du bruger den nye, restriktive indstilling, skal **Standardordreantal** altid være et multiplum af den angivne **Multiplum**-værdi for indkøbsordrer, lager og salgsordrer. Hvis du bruger streng validering, kan du ikke gemme standardindstillinger for ordrer, der ikke overholder dette krav (og der vises en fejl på meddelelseslinjen). 

Streng validering gælder for **Standardordreantal**, der er angivet i oversigtspanelerne **Indkøbsordre**, **Lager** og **Salgsordre** på siden **Indstillinger for standardordre**. Hvert oversigtspanel har sin egen indstilling af **Multiplum**, der bruges til at validere den **Standardordreantal**-værdi, der er angivet for det pågældende oversigtspanel.

### <a name="enable-the-strict-validation-option"></a>Aktivere indstillingen streng validering

Før du kan bruge streng validering, skal indstillingen være aktiveret i dit system. Administratorer kan bruge siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Her er funktionen angivet som:

- **Modul** - *Administration af produktoplysninger*
- **Funktionsnavn** - *Streng validering af standardordreantal*

### <a name="set-the-validation-option"></a>Angive valideringsindstillingen

Sådan angiver du valideringsindstillingen:

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Parametre for administration af produktoplysninger**.
1. Under fanen **Generelt** skal du angive **Validering af standardordreantal** til en af følgende værdier:
    - **Streng** – Vælg denne indstilling for at sikre, at alle værdier af **Standardordreantal** er et multiplum af **Multiplum**-værdien for hvert oversigtspanel (**Indkøbsordre**, **Lager** og **Salgsordre**).
    - **Standard** – Vælg denne indstilling for at bruge standardvalidering (hvilket fungerer på samme måde, som når denne funktion ikke er aktiveret).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]