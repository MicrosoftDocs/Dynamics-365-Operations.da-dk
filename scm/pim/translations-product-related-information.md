---
title: "Produktrelaterede oversættelser, ofte stillede spørgsmål"
description: "Dette emne beskriver, hvordan du administrerer oversættelser for produkter, produktdimensionsværdier og produktattributter."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Produktrelaterede oversættelser, ofte stillede spørgsmål

Dette emne beskriver, hvordan du administrerer oversættelser for produkter, produktdimensionsværdier og produktattributter. 

<a name="what-product-related-data-can-be-translated"></a>Hvilke produkt-relaterede data kan oversættes?
--------------------------------------------

Du kan oprette oversættelser for følgende produkt-relaterede oplysninger:
-   Navne og beskrivelser af produkter.
-   Beskrivelser, fulde navne og værdier for produktattribut Hjælp-tekst.
-   Navne og beskrivelser af produktdimensionsværdier.

Du kan oversætte de produktrelaterede oplysninger til et hvilket som helst sprog, som er tilgængeligt på siden **Oversættelse af tekst**. Du kan finde flere oplysninger i følgende afsnit **Hvordan kan jeg oprette oversættelser for produktrelaterede oplysninger**.

## <a name="where-can-i-view-the-translated-information"></a>Hvor kan jeg se de oversatte oplysninger?
Du kan få vist oversættelser af produkt-relaterede oplysninger i en ekstern kildedokument, f.eks en faktura, der bruger et sprog, hvor der findes oversættelser.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Hvordan opretter oversættelser produktrelaterede oplysninger?
Hvis du vil oprette oversættelser for et projekt, skal du følge disse trin:
1.  Klik på **administration af produktoplysninger**&gt;**almindelige**&gt;**frigivne produkter**.
2.  Vælg et produkt, og i handlingsruden, i det **sprog** skal du klikke på **oversættelser**.
3.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide den **sprog**, og klik derefter på **OK**.
4.  Brug gruppen **Oversat tekst** til at indtaste oversættelser i felterne **Beskrivelse** og **Produktnavn**.

Hvis du vil oprette oversættelser for produktattributter, skal du følge disse trin:
1.  Klik på **administration af produktoplysninger**&gt;**almindelige**&gt;**frigivne produkter**.
2.  Under **Konfiguration** skal du klikke på **Attributter** og derefter klikke på **Attributter**.
3.  På siden **Attributter** skal du klikke på **Oversæt**.
4.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide den **sprog**, og klik derefter på **OK**.
5.  Brug gruppen **Oversat tekst** til at indtaste oversættelser i felterne **Beskrivelse** og **Fulde navn** og **Hjælpetekst**.

Hvis du vil oprette oversættelser for produktdimensionsværdier, skal du følge disse trin:
1.  Klik på **administration af produktoplysninger**&gt;**almindelige**&gt;**frigivne produkter**.
2.  Vælg et produkt, og klik derefter på **Produktdimensioner**.
3.  Vælg et af linkene for produktdimensioner: **Konfigurationer**, **Størrelser**, **Farver** eller **Skabelon**.
4.  Vælg en dimensionsværdi, og klik derefter på **Oversæt**.
5.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide den **sprog**, og klik derefter på **OK**.
6.  I den **oversat tekst** skal du angive oversættelser i den **navn** og **beskrivelse** felter.

## <a name="can-the-names-of-product-variants-be-translated"></a>Kan navne på produktvarianter oversættes?
Produktvarianter er baseret på dimensionerne af et frigivet produkt. Navnene på produktvarianter er baseret på en kombination af dimensionsværdier. Når de dimensionsværdier, der er tilknyttet en produktvariant, oversættes, vises navnet på produktvarianten i den oversatte version.  

**Eksempel**  

Dit produkt er en T-shirt, der fås i forskellige størrelser og farver, og variantnavnene er baseret på følgende oplysninger:
-   Produktnummer: \#3
-   Dimensioner: størrelse og farve
-   Værdier for størrelsesdimensioner: små, mellemstore og store
-   Værdier for farvedimension: rød, grøn, sort

Navnet for en produktvariant, der er baseret på dimension værdier mindre og rød er **\#3:Small:Red**.  

En kunde ønsker at købe nogle små, røde T-shirts, og navnet på T-shirten skal vises på fransk på fakturaen. Du kan oversætte dimensionsværdierne, små og rød, til fransk, og navnet på produktvarianten er **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Følg disse trin for at angive det foretrukne sprog for en kunde:
<ol>  
<li>Klik på <strong>salgs- og</strong>&gt;<strong>almindelige</strong>&gt;<strong>kunder</strong>&gt;<strong>alle</strong> <strong>kunder</strong>.</li>
<li>Dobbeltklik på en kunde for at åbne siden <strong>Kunder</strong>. Under fanen <strong>Generelt</strong> skal du vælge <strong>sproget</strong> i feltet <strong>Sprog</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Hvad sker der, hvis en kunde har et foretrukket sprog, for hvilket der findes ikke nogen oversættelser?
Hvis oversættelser ikke er tilgængelige på kundens foretrukne sprog, vises navne og beskrivelser på det globale sprog i din egen virksomhed.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kan jeg administrere oversættelser for en serie dimensionsværdier på samme tid?
Dimensionsværdierne er produktspecifikke, og du kan administrere oversættelser for dimensionsværdierne for hvert produkt. Hvis du opretter en dimensionsværdigruppe og opretter oversættelser for værdierne i værdigruppen, er det dog nemmere at administrere oversættelserne.   

**Example**  

Din virksomhed producerer T-shirts i forskellige stilarter, og de fås alle i størrelserne Small, Medium og Large. Størrelserne samles i én dimensionsværdigruppe. Når der tilføjes en ny T-shirt-stil, kan du knytte den til den dimensionsværdigruppe, der bruges til størrelser, så alle størrelser er tilgængelige for produktet. Du kan også når som helst tilføje eller ændre oversættelser for størrelser i dimensionsværdigruppen.  

En dimensionsværdi, der er knyttet til et produkt via en dimensionsvariantgruppe, skal vedligeholdes fra produktvariantgruppen.   
Følg disse trin for at oprette en dimensionsværdigruppe:
1.  Klik på **administration af produktoplysninger**&gt;**Setup**&gt;**variantgrupper**.
2.  Vælg **Størrelse** **Grupper**, **Farvegrupper** eller **Typegrupper**.
3.  Klik på **ny**, og angiv derefter et navn til gruppen i den **størrelse****gruppe**, **farvegruppe**, eller **typografigruppe** felt. Klik på **Størrelser**, **Farver** eller **Typer** for at oprette linjer til grupperne.
4.  I den **størrelse****gruppe** linjer, **farve****gruppe****linjer**, eller **typografi gruppelinjer** skal du klikke på **ny**, og opret derefter størrelser, farver og typografier for grupper.

Følg disse trin for at administrere oversættelser af værdier for en dimensionsværdigruppe:
1.  Følg trinnene i forrige procedure for at oprette en dimensionsværdigruppe og åbne siden **Størrelsesgruppelinjer**, **Farvegruppelinjer** eller **Typografigruppelinjer**.
2.  Klik på **Oversættelse af tekst**. I den **tekst oversættelse** side i den **oversat tekst** skal du angive oversættelser i den **navn** og **beskrivelse** felter.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Hvornår kan oversættelser af produktrelaterede oplysninger administreres?
Du kan administrere oversættelser af produktrelaterede oplysninger når som helst. Når oversættelser opdateres for en dimensionsværdi, der er knyttet til et produkt, opdateres produktoplysninger, uanset om produktet har transaktioner.




