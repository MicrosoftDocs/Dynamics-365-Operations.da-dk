---
title: Definere kanalspecifikke rabatter
description: "Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Definere kanalspecifikke rabatter

Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal. 

<a name="channel-specific-discounts"></a>Kanalspecifikke rabatter
--------------------------

Detailhandlere tilbyder ofte forskellige rabatter på forskellige kanaler. Dette er muligvis ske til adressen lokale markedsbetingelser eller imødegå konkurrerende detailhandlere.

Bruger prisgrupper til at definere kanal-specifikke rabatter, detail- og handel i Microsoft Dynamics 365 for operationer. Prisgrupper kan tildeles til en eller flere af følgende enheder: kanaler, kataloger, tilhørsforhold og fordelskundeprogrammer. I denne artikel beskrives kanaler, men de samme begreber gælder for katalograbatter, tilhørsforhold med rabatter og fordelskunderabatter.

## <a name="price-groups"></a>Prisgrupper
\[titeltekst-id = "vedhæftet fil\_256084" Juster = "alignnone" bredde = "640"\][![pris grupper](./media/price-groups-1024x608.png)](./media/price-groups.png) pris gruppe links til Retail\[/billedtekst\]

Ovenstående diagram viser forholdet mellem objekter, der kan være på en transaktion (kanal, katalog, tilhørsforhold, debitor, fordelskundekort) og forskellige rabattyper, der kan konfigureres. Alle transaktionerne finder sted i en kanal, så kanalen er garanteret at være til stede i en transaktion. De resterende enheder er valgfri. På de enkelte masterdatasider er der et link til en relateret prisgruppeside, hvor du kan få vist og tilføje prisgrupper efter behov. En prisgruppe anvendes til at knytte fire forskellige typer enheder til rabatter, prisjusteringer og samhandelsaftaler. Vi anbefaler, at du planlægger en strategi for, hvordan du navngiver din prisgrupper for at holde dem organiseret. En mulighed ville være at bruge et bogstav eller tal præfiks eller suffiks til at skelne mellem de forskellige typer. For eksempel 1-xxxxx for kanal prisgrupper og 2-xxxxx for kataloget prisgrupper. Der er fire undersøgelsessider med fokus på hver af de detailenheder, der kan have rabatter tilknyttet.

-   **Detailkanalsprisgrupper **–Denne side viser en liste over kanaler og rabatter, der er kædet sammen for hver prisgruppe.
-   **Katalogprisgrupper **–Denne side viser en liste over kataloger og rabatter, der er kædet sammen for hver prisgruppe.
-   **Prisgrupper for fordelskunder **–Denne side viser en liste over fordelskundeprogrammer og rabatter, der er kædet sammen for hver prisgruppe.
-   **Prisgrupper for tilhørsforhold **–Denne side viser en liste over tilhørsforhold og rabatter, der er kædet sammen for hver prisgruppe.

## <a name="example-channel-discount-set-up"></a>Rabatopsætning for eksempelkanal
Følgende eksempel illustrerer de opgaver, der er involveret i oprettelse af en kanalrabat.

1.  I dette eksempel har du en kanal kaldet **Horsens**, og du vil oprette en ny rabat, kaldet **I skole igen.**
2.  Da strategien for prissætning og rabat indeholder muligheden for kanalrabatter, opretter du altid en kanalspecifikke prisgruppe, når du opretter en kanal.
3.  Du har prisgruppen **Horsens-PG**, og den er tildelt til kanalen **Horsens**.
4.  Når du har oprettet den nye **I skole igen**-rabat, skal du klikke på **Prisgrupper** øverst på **Rabat** siden. Siden **Detailprisgrupper** åbnes. Klik derefter på **ny** , og vælg prisgruppen **Horsens-PG**.
5.  Du kan nu aktivere rabatten og sende den til kanalen.

 

<a name="see-also"></a>Se også
--------

[Price adjustments and discounts](price-adjustments-discounts.md)

