---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3916b18c797222c300957fb25cabad78c4fcb9744a29d611a81b0bda3e9834d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724598"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Tilføje scriptkode til sider på websteder for at understøtte telemetri

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.

Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering. Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics. De fleste webanalysepakker kræver, at du tilføjer scriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle siderne på dit websted.

> [!NOTE]
> Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Oprette et fragment, der kan genbruges, til scriptkoden

Et fragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Oprette et fragment, der kan genbruges, til den indbyggede scriptkode

Udfør følgende trin for at oprette et fragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg **Indbygget script** i dialogboksen **Nyt fragment**.
1. Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.
1. Vælg modulet **Indbygget standardscript** under det fragment, du har oprettet.
1. Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Oprette et fragment, der kan genbruges, til den eksterne scriptkode

Udfør følgende trin for at oprette et fragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg **Eksternt script** i dialogboksen **Nyt fragment**.
1. Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.
1. Vælg modulet **Eksternt standardscript** under det fragment, du har oprettet.
1. Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre. Konfigurer derefter andre indstillinger efter behov.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

> [!NOTE]
> Hvis du har aktiveret indholdssikkerhedspolitik (CSP) for webstedet, skal du kontrollere, at alle eksterne URL-adresser er føjet til CSP-direktivet **script-src** i Commerce-webstedsgeneratoren. Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Tilføje et fragment, der indeholder scriptkode, i en skabelon

Udfør følgende trin for at føje et fragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.

1. Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.
1. Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.
1. Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.
1. Vælg det fragment, du har oprettet til scriptkoden.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Føje et eksternt script eller indbygget script til en skabelon

Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et fragment først.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
