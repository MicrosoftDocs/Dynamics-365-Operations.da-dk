---
title: Ofte stillede spørgsmål til produktvariantoversættelser
description: Dette emne beskriver, hvordan du administrerer oversættelser for produkter, produktdimensionsværdier og produktattributter.
author: cvocph
manager: tfehr
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a79f7dccd518ce1d0e7c937a1a7934b474c4b37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999625"
---
# <a name="product-related-translations-faq"></a>Ofte stillede spørgsmål til produktvariantoversættelser

[!include [banner](../includes/banner.md)]

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

## <a name="how-do-i-create-translations-for-product-related-information"></a>Hvordan kan jeg oprette oversættelser for produkt-relaterede oplysninger?
Hvis du vil oprette oversættelser for et projekt, skal du følge disse trin:
1.  Klik på **Administration af produktoplysninger** &gt; **Almindelige** &gt; **Frigivne produkter**.
2.  Vælg et produkt, og klik på **Oversættelser** i gruppen **Sprog** i handlingsruden.
3.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide feltet **Sprog** og derefter klikke på **OK**.
4.  Brug gruppen **Oversat tekst** til at indtaste oversættelser i felterne **Beskrivelse** og **Produktnavn**.

Hvis du vil oprette oversættelser for produktattributter, skal du følge disse trin:
1.  Klik på **Administration af produktoplysninger** &gt; **Almindelige** &gt; **Frigivne produkter**.
2.  Under **Konfiguration** skal du klikke på **Attributter** og derefter klikke på **Attributter**.
3.  På siden **Attributter** skal du klikke på **Oversæt**.
4.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide feltet **Sprog** og derefter klikke på **OK**.
5.  Brug gruppen **Oversat tekst** til at indtaste oversættelser i felterne **Beskrivelse** og **Fulde navn** og **Hjælpetekst**.

Hvis du vil oprette oversættelser for produktdimensionsværdier, skal du følge disse trin:
1.  Klik på **Administration af produktoplysninger** &gt; **Almindelige** &gt; **Frigivne produkter**.
2.  Vælg et produkt, og klik derefter på **Produktdimensioner**.
3.  Vælg et af linkene for produktdimensioner: **Konfigurationer**, **Størrelser**, **Farver** eller **Skabelon**.
4.  Vælg en dimensionsværdi, og klik derefter på **Oversæt**.
5.  På siden **Oversættelse af tekst** skal du i feltet **Sprog** vælge et sprog. Hvis du vil tilføje flere sprog, skal du udvide feltet **Sprog** og derefter klikke på **OK**.
6.  Brug gruppen **Oversat tekst** til at indtaste oversættelser i felterne **Navn** og **Beskrivelse**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Kan navne på produktvarianter oversættes?
Produktvarianter er baseret på dimensionerne af et frigivet produkt. Navnene på produktvarianter er baseret på en kombination af dimensionsværdier. Når de dimensionsværdier, der er tilknyttet en produktvariant, oversættes, vises navnet på produktvarianten i den oversatte version.  

**Eksempel**  

Dit produkt er en T-shirt, der fås i forskellige størrelser og farver, og variantnavnene er baseret på følgende oplysninger:
-   Produktnummer: \#3
-   Dimensioner: størrelse og farve
-   Værdier for størrelsesdimensioner: små, mellemstore og store
-   Værdier for farvedimension: rød, grøn, sort

Navnet på en produktvariant, der er baseret på dimensionsværdierne Små og Rød, er **\#3: Små:Rød**.  

En kunde ønsker at købe nogle små, røde T-shirts, og navnet på T-shirten skal vises på fransk på fakturaen. Du oversætter dimensionsværdierne, Små og Rød, til fransk, og navnet på produktvarianten er **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Følg disse trin for at angive det foretrukne sprog for en kunde:
<ol><br/><li>Klik på <strong>Salg og marketing</strong> &gt; <strong>Generelt</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle</strong> <strong>kunder</strong>.</li>
<li>Dobbeltklik på en kunde for at åbne siden <strong>Kunder</strong>. Under fanen <strong>Generelt</strong> skal du vælge <strong>sproget</strong> i feltet <strong>Sprog</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Hvad sker der, hvis en kunde har et foretrukket sprog, for hvilket der findes ikke nogen oversættelser?
Hvis oversættelser ikke er tilgængelige på kundens foretrukne sprog, vises navne og beskrivelser på det globale sprog i din egen virksomhed.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kan jeg administrere oversættelser for en serie dimensionsværdier på samme tid?
Dimensionsværdierne er produktspecifikke, og du kan administrere oversættelser for dimensionsværdierne for hvert produkt. Hvis du opretter en dimensionsværdigruppe og opretter oversættelser for værdierne i værdigruppen, er det dog nemmere at administrere oversættelserne.   

**Eksempel**  

Din virksomhed producerer T-shirts i forskellige stilarter, og de fås alle i størrelserne Small, Medium og Large. Størrelserne samles i én dimensionsværdigruppe. Når der tilføjes en ny T-shirt-stil, kan du knytte den til den dimensionsværdigruppe, der bruges til størrelser, så alle størrelser er tilgængelige for produktet. Du kan også når som helst tilføje eller ændre oversættelser for størrelser i dimensionsværdigruppen.  

En dimensionsværdi, der er knyttet til et produkt via en dimensionsvariantgruppe, skal vedligeholdes fra produktvariantgruppen.   
Følg disse trin for at oprette en dimensionsværdigruppe:
1.  Klik på **Administration af produktoplysninger** &gt; **Konfiguration** &gt; **Variantgrupper**.
2.  Vælg **Størrelse** **Grupper**, **Farvegrupper** eller **Typegrupper**.
3.  Klik på **Ny**, og angiv derefter et navn til gruppen i feltet **Størrelses** **gruppe**, **Farvegruppe** eller **Typografigruppe**. Klik på **Størrelser**, **Farver** eller **Typer** for at oprette linjer til grupperne.
4.  På siden **Størrelses** **gruppelinjer**, **Farve** **gruppe** **linjer** eller **Typografigruppelinjer** skal du klikke på **Ny** og derefter oprette størrelser, farver og typografier for grupperne.

Følg disse trin for at administrere oversættelser af værdier for en dimensionsværdigruppe:
1.  Følg trinnene i forrige procedure for at oprette en dimensionsværdigruppe og åbne siden **Størrelsesgruppelinjer**, **Farvegruppelinjer** eller **Typografigruppelinjer**.
2.  Klik på **Oversættelse af tekst**. På siden **Oversættelse af tekst** skal du i gruppen **Oversat tekst** indtaste oversættelser i felterne **Navn** og **Beskrivelse**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Hvornår kan oversættelser af produktrelaterede oplysninger administreres?
Du kan administrere oversættelser af produktrelaterede oplysninger når som helst. Når oversættelser opdateres for en dimensionsværdi, der er knyttet til et produkt, opdateres produktoplysninger, uanset om produktet har transaktioner.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]