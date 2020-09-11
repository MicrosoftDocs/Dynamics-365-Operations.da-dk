---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686808"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Tilføje scriptkode til sider på websteder for at understøtte telemetri

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.

## <a name="overview"></a>Oversigt

Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering. Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics. De fleste webanalysepakker kræver, at du tilføjer scriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle siderne på dit websted.

> [!NOTE]
> Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Oprette et sidefragment, der kan genbruges, til scriptkoden

Et sidefragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Oprette et sidefragment, der kan genbruges, til den indbyggede scriptkode

Udfør følgende trin for at oprette et sidefragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg **Indbygget script** i dialogboksen **Nyt sidefragment**.
1. Angiv et navn til fragmentet under **Sidefragmentnavn**, og vælg derefter **OK**.
1. Vælg modulet **Indbygget standardscript** under det sidefragment, du har oprettet.
1. Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Oprette et sidefragment, der kan genbruges, til den eksterne scriptkode

Udfør følgende trin for at oprette et sidefragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg **Eksternt script** i dialogboksen **Nyt sidefragment**.
1. Angiv et navn til fragmentet under **Sidefragmentnavn**, og vælg derefter **OK**.
1. Vælg modulet **Eksternt standardscript** under det sidefragment, du har oprettet.
1. Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Føje et sidefragment, der indeholder scriptkode, til en skabelon

Udfør følgende trin for at føje et sidefragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.

1. Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.
1. Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.
1. Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj sidefragment**.
1. Vælg det fragment, du har oprettet til scriptkoden.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Føje et eksternt script eller indbygget script til en skabelon

Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et sidefragment først.

### <a name="add-an-inline-script-directly-to-a-template"></a>Føje et indbygget script til en skabelon

Hvis du vil føje et indbygget script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.
1. Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.
1. Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.
1. Vælg **Indbygget script** i dialogboksen **Tilføj modul**.
1. Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

### <a name="add-an-external-script-directly-to-a-template"></a>Føje et eksternt script til en skabelon

Hvis du vil føje et eksternt script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.
1. Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.
1. Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.
1. Vælg **Eksternt script** i dialogboksen **Tilføj modul**.
1. Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)
