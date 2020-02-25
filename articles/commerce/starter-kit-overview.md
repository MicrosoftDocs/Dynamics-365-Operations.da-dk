---
title: Oversigt over startsæt
description: Dette emne indeholder en oversigt over startsættet til Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1960e1354744fe1034783177ba331f5877d0bee7
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025896"
---
# <a name="starter-kit-overview"></a>Oversigt over startsæt


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over startsættet til Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Dynamics 365 Commerce-startsættet er en samling af moduler, der kan bruges til at bygge et e-handels-websted. Moduler har både aspekter af brugergrænseflade og funktionsmåder.

Du kan anvende temaer på modulerne i startsættet for at ændre deres udseende og funktionalitet. Temaerne bruger overlappende typografiark (CSS). Der findes et tema for et fiktivt e-handels-websted med navnet "Fabrikam" som en del af startsættet, der kan bruges som reference.

## <a name="starter-kit-modules"></a>Moduler i startsæt

Følgende typer moduler findes i startsættet:

- **Containermodul** – Et containermodul er et simpelt modul, der fungerer som vært for andre moduler. Det styrer layoutet for de moduler, der ligger i det.
- **Marketingmoduler** – Marketingmoduler omfatter indholdsblok, tekstblok, videoafspiller og karruselmoduler. Alle disse moduler kan bruges til at vise indhold. De kan placeres på en hvilken som helst side og styres af data fra CMS-indholdsstyringssystemet (Content Management System).
- **Sidehoved- og sidefodsmoduler** – Sidehoved- og sidefodsmoduler vises i sidehovedet og sidefoden på alle webstedssider. Disse moduler kan konfigureres efter behov ved hjælp af egenskaber.
- **Søgemoduler** – Produkter kan opdages ved hjælp af søgemodulet i sidehovedet. Søgeresultaterne vises på siden med søgeresultater. Der kan også registreres produkter på kategorisider, som er dedikerede sider til hver kategori, der understøttes i kanalens navigationshierarki. Desuden kan afgrænsningsmoduler bruges til at filtrere resultater yderligere i søgeresultater og på kategorisider.
- **Sidemoduler for produktdetaljer** – Sider med produktdetaljer bruger flere moduler til at vise produktoplysninger. I købefeltmodulet kan kunder få vist produkter og føje dem til indkøbsvognen. Andre moduler som f.eks. modulet til tekniske specifikationer viser produktoplysningerne. Modulet til vurderinger og anmeldelser kan bruges til at se og angive vurderinger.
- **Køb online, afhent i butikken-modulet** – Køb online, afhent i butikken-modulet er integreret med Bing Kort. Det kan bruges til at finde butikker i nærheden, hvor kunder kan afhente produkter, som de har købt.
- **Købsmoduler** – Købsmoduler indeholder indkøbsvognsmodulet, som kan bruges til at lægge varer i indkøbsvognen. Betalingsmodulet registrerer leveringsadressen, leveringsindstillinger og gavekort, fordelskundeprogram og kreditkortoplysninger, så en ordre kan behandles. Når en ordre er afgivet, kan ordrebekræftelsesmodulet bruges til at vise bekræftelsesoplysningerne.
- **Kontostyringsmoduler** – I logonmodulet kan kunder logge på en eksisterende konto, og tilmeldingsmodulet giver dem mulighed for at oprette en ny konto. Når en konto er oprettet, kan modulet for ordrehistorik bruges til at få vist de seneste ordrer, og modulet med ordredetaljer kan bruges til at få vist ordredetaljer.
- **Anbefalinger-modul** – Anbefalinger vises ved hjælp af modulet til produktplacering. Dette modul understøtter algoritmer og redaktionelle lister, der kan vises på alle sider.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulet Container](add-container-module.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
