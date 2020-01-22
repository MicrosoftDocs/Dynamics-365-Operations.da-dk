---
title: Tilføj et logo
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914611"
---
# <a name="add-a-logo"></a>Tilføj et logo

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Når du bygger dit websted, er en af de første ting, du sandsynligvis vil gøre at tilføje dit virksomheds- eller brandlogo til webstedets header. Dynamics 365 Commerce-online startsæt indeholder et modul, der gør denne opgave nem.

Du kan føje et logo direkte til en skabelon, et layout eller en side. På denne måde kan du nemt ændre det logo, der vises på bestemte sider eller grupper af sider. Dette emne dækker dog det hyppigst forekommende scenarie, hvor du føjer dit logo til et sidehovedfragment, der kan genbruges på tværs af alle siderne på dit websted.

## <a name="prerequisites"></a>Forudsætninger

Før du kan føje et logo til alle siderne på dit websted, skal du fuldføre disse trin.

1. Overfør dit logo til den digitale aktivmanager, som du kan få adgang til fra siden **Aktiver**.
1. Opret et sidehovedfragment. Du kan finde flere oplysninger om, hvordan du opretter og bruger fragmenter i [Arbejd med fragtmenter](work-with-fragments.md).
1. Medtag sidehovedfragmentet i skabelonen, som bruges til layoutet og modulinstillingerne for siderne på dit websted. Du kan finde flere oplysninger om skabeloner i [Arbejd med skabeloner](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Tilføj et logo til et sidehovedfragmentet.

Følg disse trin for at tilføje et logo til sidehovedfragmentet på dit websted.

1. Vælg **Fragmenter** i navigationsruden til venstre, og vælg derefter det sidehovedfragmentet, du har oprettet.
2. Vælg **Check ud**.
3. Udvid pladsen **Sidehoved** og **Logo**.
4. Vælg ellipseknappen (**...**) for pladsen til **Logo**, og vælg derefter **Tilføj modul**.
5. Vælg logomodulet.
6. Derefter skal du konfigurere logomodulet i egenskabsruden til højre, så det afbilleder dit logo.
7. Gem sidehovedfragmentet, check det ind, og publicer det.

Når du har udgivet det opdaterede sidehovedfragment, vises dit logo på alle de webstedssider, som bruger den skabelon, der indeholder sidehovedfragmentet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Vælg et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

