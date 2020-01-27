---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914533"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Tilføje scriptkode til sider på websteder for at understøtte telemetri

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.

## <a name="overview"></a>Oversigt

Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering. Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics. De fleste webanalysepakker kræver, at du tilføjer klientside-scriptkode i elementet **\<head\>** i HTML-koden for alle siderne på dit websted.

> [!NOTE]
> Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Oprette et fragment, der kan genbruges, til scriptkoden

Når du har oprettet et fragment til scriptkoden, kan det genbruges på tværs af alle sider på dit websted.

1. Gå til **Fragmenter \> Nyt sidefragment**.
2. Vælg **Eksternt script**, angiv et navn til fragmentet, og vælg derefter **OK**.
3. Vælge det underordnede **script-injektor**-modul til det fragment, du lige har oprettet, i fragmenthierarkiet.
4. Tilføj klientsidescriptet i egenskabsruden til højre, og angiv andre konfigurationsindstillinger efter behov.

## <a name="add-the-fragment-to-templates"></a>Føje fragmentet til skabeloner

1. Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.
2. Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.
3. Vælg ellipseknappen (**...**) for pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.
4. Vælg det fragment, du har oprettet til scriptkoden.
5. Gem skabelonen ind, og tjek den ind.

> [!NOTE]
> Når du er færdig, skal du publicere fragmentet og masterskabelonen. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Vælg et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

