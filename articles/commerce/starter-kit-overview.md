---
title: Oversigt over modulbibliotek
description: Dette emne indeholder en oversigt over modulbiblioteket til Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b3440c046ff055c8afa012c80c56aba741fef27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985555"
---
# <a name="module-library-overview"></a>Oversigt over modulbibliotek

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over modulbiblioteket til Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Dynamics 365 Commerce-modulbiblioteket er en samling af moduler, der kan bruges til at bygge et e-handels-websted. Moduler har både aspekter af brugergrænseflade og funktionsmåder.

Du kan anvende temaer på modulerne i modulbiblioteket for at ændre deres udseende og funktionalitet. Temaerne bruger overlappende typografiark (CSS). Der findes et tema for et fiktivt e-handels-websted med navnet "Fabrikam" som en del af modulbiblioteket, der kan bruges som reference.

## <a name="module-library-modules"></a>Modulbibliotekets moduler

Følgende typer moduler findes i modulbiblioteket:

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
