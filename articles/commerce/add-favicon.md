---
title: Tilføj en favicon
description: I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295074"
---
# <a name="add-a-favicon"></a>Tilføj en favicon

[!include [banner](includes/banner.md)]

I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.

## <a name="overview"></a>Oversigt

Et favoritikon er en lille grafikfil, der bl.a. vises under en webbrowserfane, på adresselinjen, i browserhistorikken og i bogmærker eller favoritter. Det anbefales, at du føjer et favoritikon til dit websted, fordi det repræsenterer og forstærker dit varemærke og hjælper med at skelne dit websted fra andre websteder, som kunderne besøger.

Du kan føje flere favoritikoner med forskellig størrelse og filtype til webstedet, men i dette emne vises det, hvordan du tilføjer et enkelt favoritikon. Du bruger imidlertid den samme proces og placering ved tilføjelse af flere favoritikoner.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Overføre et favoritikon til webstedets aktivsamling

Benyt følgende fremgangsmåde for at overføre et favoritikon til webstedets aktivsamling.

1. Vælg **Mediebibliotek** i navigationsruden til venstre.
1. Vælg **Upload \> Upload medieelementer** på kommandolinjen.
1. I vinduet Stifinder skal du gå til den favoritikonbilledfil, du vil uploade, vælge den og derefter vælge **Åbn**.
1. Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.
1. Hvis du vil udgive billedet umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload**.

    > [!NOTE]
    > Hvis du ikke markerer afkrydsningsfeltet **Publicer medieelementer efter upload**, skal du vende tilbage til siden **Medieelementer** og publicere favoritikonet manuelt senere.

1. Vælg **OK**.
1. Kopiér favoritikonets offentlige URL-adresse i egenskabsruden til højre. Du kommer til at bruge denne URL-adresse senere.

## <a name="create-the-html-for-your-favicon"></a>Oprette HTML-koden til dit favoritikon

Du opretter HTML-koden til favoritikonet ved hjælp af følgende HTML-streng. I attributten **href** skal du erstatte **Public\_URL\_for\_your\_favicon** med den offentlige URL-adresse, du kopierede tidligere.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a>Oprette et sidefragment, der indeholder en metakode til dit favoritikon

Følg disse trin for at oprette et sidefragment, der indeholder et metatag til dit favoritikon.

1. Gå til **Sidefragmenter**, og vælg derefter **Ny**.
1. Vælg **Metakoder** i dialogboksen **Nyt sidefragment** som det modul, sidefragmentet er baseret på.
1. Angiv et navn til sidefragmentet, og vælg derefter **OK**.
1. Vælg det underordnede **Standardmetamoder** i fragmenthierarkitræet.
1. Vælg **Tilføj** under **Metakoder** i ruden til højre, og angiv derefter den HTML-streng, du oprettede til favoritikonet tidligere. 
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere sidefragmentet.

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a>Føj sidefragmentet for metakoder til HTML-hovedsektionen for dine sider

Følge disse trin for at føj sidefragmentet for metakoder til HTML-**hoved**sektionen for dine sider.

1. Gå til **Skabeloner**, åbn skabelonen for de sider, du vil føje dit favoritikon til, og vælg derefter **Rediger**.
1. Vælg ellipseknappen (**...**) i skabelonhierarkitræet til højre for containeren i **HTML-hovedet**, og vælg derefter **Tilføj sidefragment**.
1. Vælg det sidefragment for metakoder, du oprettede tidligere, i dialogboksen **Vælg sidefragment**, og vælg derefter **OK**.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.

> [!NOTE]
> Hvis webstedet bruger mere end én skabelon, skal du føje sidefragmentet for metakoder til dem alle.

Når du får vist sider, der er baseret på den skabelon, du har føjet til sidefragmentet for metakoder, burde du nu kunne se favoritikonet på browserfanen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

