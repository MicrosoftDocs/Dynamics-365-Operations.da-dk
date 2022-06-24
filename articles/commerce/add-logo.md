---
title: Tilføje et logo
description: Denne artikel indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 624cd6f7000f5038b9996eb94caf79719d07f99f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871774"
---
# <a name="add-a-logo"></a>Tilføje et logo

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.

Når du bygger dit websted, er en af de første ting, du sandsynligvis vil gøre at tilføje dit virksomheds- eller brandlogo til webstedets header. Dynamics 365 Commerce-online modulbiblioteket indeholder et modul, der gør denne opgave nem.

Du kan føje et logo direkte til en skabelon, et layout eller en side. På denne måde kan du nemt ændre det logo, der vises på bestemte sider eller grupper af sider. Denne artikel dækker dog det hyppigst forekommende scenarie, hvor du føjer dit logo til et sidehovedfragment, der kan genbruges på tværs af alle siderne på dit websted.

## <a name="prerequisites"></a>Forudsætninger

Før du kan føje et logo til alle siderne på dit websted, skal du fuldføre disse trin.

1. Upload dit logo til mediebiblioteket.
1. Opret et sidehovedfragment. Du kan finde flere oplysninger om, hvordan du opretter og bruger fragmenter i [Arbejd med fragtmenter](work-with-fragments.md).
1. Medtag sidehovedfragmentet i skabelonen, som bruges til layoutet og modulinstillingerne for siderne på dit websted. Du kan finde flere oplysninger om skabeloner i [Arbejd med skabeloner](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Tilføj et logo til et sidehovedfragmentet.

Følg disse trin for at tilføje et logo til sidehovedfragmentet på dit websted.

1. Vælg **Fragmenter** i navigationsruden til venstre.
1. Vælg det sidehovedfragment, du oprettede tidligere, og vælg derefter **Rediger**.
1. Udvid sidehovedmodulet.
1. Angiv et billede og et link til logoet i egenskabsruden for sidehovedmodulet. 
1. Gem sidehovedfragmentet, afslut redigeringen, og udgiv det.

Når du har udgivet det opdaterede sidehovedfragment, vises dit logo på alle de webstedssider, som bruger den skabelon, der indeholder sidehovedfragmentet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføje en favicon](add-favicon.md)

[Tilføje en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
