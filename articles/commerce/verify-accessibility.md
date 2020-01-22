---
title: Bekræft tilgængelighed af sideindhold
description: Dette emne beskriver, hvordan du kontrollerer tilgængeligheden af sideindhold i Microsoft Dynamics 365 Commerce.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945985"
---
# <a name="verify-page-content-accessibility"></a>Bekræft tilgængelighed af sideindhold

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kontrollerer tilgængeligheden af sideindhold i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Når du er færdig med at ændre en side, skal du sørge for, at indholdet er tilgængeligt for alle på internettet. I Commerce-oprettelsesværktøjerne kan du nemt kontrollere tilgængeligheden af sideindhold ved hjælp af den integrerede [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjeneste. Denne tjeneste bekræfter dit sideindhold i forhold til de seneste retningslinjer for hjælp til handicappede [World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).

Integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) skal være aktiveret på lejer- eller webstedsniveau, før du kan bruge den.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Aktivér Microsoft Accessibility Insights for alle webstederne i din lejer

Hvis du vil aktivere integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) for alle Commerce-websteder i din lejer, skal du følge disse trin.

> [!NOTE]
> For at tilgå lejerindstillinger skal du være logget på Commerce som systemadministrator.

1. Log ind på Commerce som systemadministrator.
1. I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.
1. Under **Lejerindstillinger** skal du vælge **Funktioner**.
1. Angiv indstillingen **Tilgængelighedskontrol** til **Til**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Aktivér Microsoft Accessibility Insights for et enkelt websted

Hvis du vil aktivere integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) for et enkelt Commerce-websted, skal du følge disse trin.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.
1. Under **Indstillinger for webstedet** skal du vælge **Funktioner**.
1. Angiv indstillingen **Tilgængelighedskontrol** til **Til**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Kontroller tilgængeligheden af indholdet på startsiden

Hvis du vil bruge den integrerede [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjeneste til at scanne og kontrollere indholdet på din startside i Commerce, skal du følge disse trin.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Sider** i navigationsruden til venstre.
1. Find og vælg startsiden for at åbne den i sideeditoren.
1. Vælg **Kontrollér tilgængelighed** på kommandolinjen. Siden **Kontroller tilgængelighed** vises.
1. Gennemse rapportens indhold, når scanningen er fuldført.
1. Hvis en kontrol mislykkedes, skal du markere hvert mislykket kontrolelement for at udvide det, så du kan få vist flere oplysninger.
1. Hvis du vil lukke rapporten, når du er færdig med at gennemse den, skal du rulle ned til bunden af siden **Kontrollér tilgængelighed** og vælge **OK**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)