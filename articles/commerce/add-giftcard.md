---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261559"
---
# <a name="gift-card-module"></a>Gavekortmodul

[!include [banner](includes/banner.md)]

I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Gavekort er en almindelig form for betaling, og gavekortmodulet kan bruges i modulet til betaling ved kassen til at acceptere gavekort. Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.

Du kan flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex, i [Support for eksterne gavekort](./dev-itpro/gift-card.md)

## <a name="module-properties"></a>Modulegenskaber

- **Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard. Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato. Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.

Understøttede værdier:
-   Pinkode
-   Udløbsdato
-   Pinkode og udløbsdato 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Indstillinger for websted for gavekortmoduler

I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser**er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**. Denne indstilling understøtter tre værdier:
- **Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.
- **SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort. Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.
- **Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.

## <a name="add-a-gift-card-module-to-a-page"></a>Føje et gavekortmodul til en side

Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Betalingsmodul](add-checkout-module.md)

[Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md)
