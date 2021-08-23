---
title: Oversigt over produktanbefalinger
description: Dette emne indeholder generelle oplysninger om produktanbefalinger. Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, og endda produkter, som de oprindeligt ikke havde tænkt sig at købe.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 667c26a8ab7665f9eb1e2cc91217338fc0eb00d6c9c21ba7b4a7e5a203e41410
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763758"
---
# <a name="product-recommendations-overview"></a>Oversigt over produktanbefalinger

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan bruges til at få vist produktanbefalinger på e-handels-webstedet og POS-enheden. Produktanbefalinger er varer, som en kunde kan være interesseret i. Anbefalingerne er baseret på indkøbstendenser fra andre kunder i onlinebutikker og fysiske butikker.

Produktanbefalinger gør det nemt og hurtigt for kunderne at finde produkter, som de ønsker, mens de har en god oplevelse. Krydssalg og mersalg kan også bruges til at hjælpe kunder med at finde flere produkter, end de oprindeligt havde tænkt sig at købe. Når anbefalingerne bruges til at forbedre produktregistrering, kan de skabe flere konverteringsmuligheder, bidrage til at øge salgsindtægterne og endda forbedre kundetilfredshed og -fastholdelse.

I e-handel er produktanbefalingerne baseret på Microsofts anbefalinger fra teknologier for maskinel indlæring i stor målestok.

Denne tjeneste er et tilføjelsesprogrammet til Dynamics 365 Commerce. Du kan finde flere oplysninger ved at hente den seneste [licensvejledning til Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).


## <a name="recommendation-service"></a>Anbefalingstjeneste

Tjenesten Produktanbefalinger anvender kunstig intelligens- og maskinlæringsteknologier (AI-ML) på følgende måde:

- Data i det format, der kræves af anbefalingstjenesten, udtrækkes fra Commerce-driftsdatabasen og sendes til Azure Data Lake Storage eller til enhedslageret.
- Anbefalingstjenesten bruger de lagrede data til at træne anbefalingsmodellerne for listerne **Personer synes også om**, **Ofte købt sammen**, **Nyt**, **Mest solgte** og **Mest populære**.

## <a name="scenarios"></a>Scenarier

Produktanbefalinger er tilgængelige for følgende scenarier:

- **På en butiksside til gennemsyn eller landingsside i e-handel**: Hvis kunder eller butiksansatte besøger en butiks side, kan anbefalingsprogrammet foreslå produkter på de nye lister **Nyt**, **Mest solgte** og **Mest populære**.
- **På siden Produktdetaljer:** Hvis kunder eller butiksansatte besøger siden **Produktdetaljer**, foreslår anbefalingsprogrammet yderligere varer, der formentlig også er interessante at købe. Disse varer vises på listen **Personer synes også om**.
- **På siden Transaktion eller ved kassen:** Anbefalingsprogrammet foreslår varer på basis af hele listen med varer i kurven. Disse varer vises på listen **Ofte købt sammen**.
- **Personlige anbefalinger:** Forhandlere kan give kunder, der er logget på, en personligt **udvalgt** liste samt nye funktioner, der gør det muligt at tilpasse eksisterende listescenarier efter den pågældende kunde. Du kan få mere at vide i [Aktivere tilpassede anbefalinger.](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Typer af produktanbefalinger

I følgende tabel beskrives de forskellige typer automatiske produktanbefalinger, der er tilgængelige for detailhandlere med henblik på implementering i deres Dynamics 365 Commerce-løsning via [modulet Produktsamling](product-collection-module-overview.md). Detailhandlende kan også vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling.

| Produktsamlingsmodul  | Type | Beskrivende tekst |
|----------------------------|------|-------------|
| Nye                        | Algoritmisk | Dette modul viser en liste over de nyeste produkter, der for nyligt er blevet udvalgt til kanaler og kataloger. |
| Bedst sælgende               | Algoritmisk | Dette modul viser en liste over produkter, der er rangeret efter det højeste salgsantal. |
| Tendenser                   | Algoritmisk | Dette modul viser en liste over de mest populære produkter i et givet tidsinterval, sorteret efter højeste salg.  |
| Ofte købt sammen | AI-ML | Dette modul anbefaler en liste over produkter, der ofte købes sammen med indholdet af den aktuelle bruger kurv. |
| Folk kan også godt lide           | AI-ML | Dette modul anbefaler produkter til et bestemt basisprodukt baseret på forbrugernes købsmønstre. |
| Muligheder til dig              | AI-ML | Dette modul anbefaler en personlig liste over produkter, der er baseret på købsmønstre for den bruger, der er logget på. For en gæstebruger vil denne liste være skjult. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
