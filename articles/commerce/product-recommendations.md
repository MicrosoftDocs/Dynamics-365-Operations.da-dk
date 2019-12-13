---
title: Oversigt over produktanbefalinger
description: Dette emne indeholder generelle oplysninger om produktanbefalinger. Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, og endda produkter, som de oprindeligt ikke havde tænkt sig at købe.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770040"
---
# <a name="product-recommendations-overview"></a>Oversigt over produktanbefalinger

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce kan bruges til at få vist produktanbefalinger på e-handels-webstedet og POS-enheden. Produktanbefalinger er varer, som en kunde kan være interesseret i. Anbefalingerne er baseret på indkøbstendenser fra andre kunder i onlinebutikker og fysiske butikker.

Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, mens de har en god oplevelse. Krydssalg og mersalg kan også bruges til at hjælpe kunder med at finde flere produkter, end de oprindeligt havde tænkt sig at købe. Når anbefalingerne bruges som hjælp til produktregistrering, kan de skabe flere konverteringsmuligheder, bidrage til at øge salgsindtægterne og endda forbedre kundetilfredshed og -fastholdelse.

I Commerce er produktanbefalingerne baseret på Microsofts anbefalinger fra teknologier for maskinel indlæring i stor målestok.


## <a name="scenarios"></a>Scenarier

Produktanbefalinger er tilgængelige for følgende scenarier:

- **På en butiksside til gennemsyn eller landingsside i e-handel**: Hvis kunder eller butiksansatte besøger en butiks side, kan anbefalingsprogrammet foreslå produkter på de nye lister **Nyt**, **Mest solgte** og **Mest populære**.
- **På siden Produktdetaljer:** Hvis kunder eller butiksansatte besøger siden **Produktdetaljer**, foreslår anbefalingsprogrammet yderligere varer, der formentlig også er interessante at købe. Disse varer vises på listen **Personer synes også om**.
- **På siden Transaktion eller ved kassen:** Anbefalingsprogrammet foreslår varer på basis af hele listen med varer i kurven. Disse varer vises på listen **Ofte købt sammen**.

## <a name="recommendation-service"></a>Anbefalingstjeneste

Produktanbefalinger bruger anbefalingerne fra teknologier for maskinel indlæring på følgende måde:

- Data i det format, der kræves af anbefalingstjenesten, udtrækkes fra Commerce-driftsdatabasen og sendes til enhedslageret.
- Anbefalingstjenesten bruger dataene til at træne anbefalingsmodellerne for listerne **Personer synes også om**, **Ofte købt sammen**, **Nyt**, **Mest solgte** og **Mest populære**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Oprette overvågede lister med produktanbefalinger](create-editorial-recommendation-lists.md)

[Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md)

[Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md)
