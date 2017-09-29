---
title: Definere kanalspecifikke rabatter
description: "Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: d40c37628f03a7605e04b95339072a67806f2fa1
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="define-channel-specific-discounts"></a>Definere kanalspecifikke rabatter

[!include[banner](includes/banner.md)]


Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal. 

<a name="channel-specific-discounts"></a>Kanalspecifikke rabatter
--------------------------

Detailhandlere tilbyder ofte forskellige rabatter i forskellige kanaler. Dette er sker muligvis for at adressere de lokale markedsbetingelser eller for at imødegå konkurrerende detailhandlere.

Microsoft Dynamics 365 for Retail bruger prisgrupper til at definere kanalspecifikke rabatter. Prisgrupper kan tildeles til en eller flere af følgende enheder: kanaler, kataloger, tilhørsforhold og fordelskundeprogrammer. I denne artikel beskrives kanaler, men de samme begreber gælder for katalograbatter, tilhørsforhold med rabatter og fordelskunderabatter.

## <a name="price-groups"></a>Prisgrupper

[![Prisgrupper](./media/price-groups-1024x608.png)](./media/price-groups.png)

Ovenstående diagram viser forholdet mellem enheder, der kan være på en transaktion (kanal, katalog, tilhørsforhold, debitor, fordelskundekort), og de forskellige rabattyper, der kan konfigureres. Alle transaktionerne finder sted i en kanal, så kanalen vil garanteret være til stede i en transaktion. De resterende enheder er valgfri. På de enkelte masterdatasider er der et link til en relateret prisgruppeside, hvor du kan få vist og tilføje prisgrupper efter behov. En prisgruppe anvendes til at relatere fire forskellige typer enheder til rabatter, prisjusteringer og samhandelsaftaler. Vi anbefaler, at du planlægger en strategi for, hvordan du navngiver dine prisgrupper for at holde dem organiseret. En mulighed ville være at bruge et bogstav eller talpræfiks eller -suffiks til at skelne mellem de forskellige typer. For eksempel 1-xxxxx for kanalprisgrupper og 2-xxxxx for katalogprisgrupper. Der er fire undersøgelsessider med fokus på hver af de detailenheder, der kan have rabatter tilknyttet.

-   **Detailkanalsprisgrupper**–Denne side viser en liste over kanaler og rabatter, der er kædet sammen for hver prisgruppe.
-   **Katalogprisgrupper**–Denne side viser en liste over kataloger og rabatter, der er kædet sammen for hver prisgruppe.
-   **Prisgrupper for fordelskunder**–Denne side viser en liste over fordelskundeprogrammer og rabatter, der er kædet sammen for hver prisgruppe.
-   **Prisgrupper for tilhørsforhold**–Denne side viser en liste over tilhørsforhold og rabatter, der er kædet sammen for hver prisgruppe.

## <a name="example-channel-discount-set-up"></a>Rabatopsætning for eksempelkanal
Følgende eksempel illustrerer de opgaver, der er involveret i oprettelse af en kanalrabat.

1.  I dette eksempel har du en kanal kaldet **Horsens**, og du vil oprette en ny rabat, kaldet **I skole igen.**
2.  Da strategien for prissætning og rabat indeholder muligheden for kanalrabatter, opretter du altid en kanalspecifikke prisgruppe, når du opretter en kanal.
3.  Du har prisgruppen **Horsens-PG**, og den er tildelt til kanalen **Horsens**.
4.  Når du har oprettet den nye **I skole igen**-rabat, skal du klikke på **Prisgrupper** øverst på **Rabat** siden. Siden **Detailprisgrupper** åbnes. Klik derefter på **ny** , og vælg prisgruppen **Horsens-PG**.
5.  Du kan nu aktivere rabatten og sende den til kanalen.

 

<a name="see-also"></a>Se også
--------

[Prisjusteringer og rabatter](price-adjustments-discounts.md)



