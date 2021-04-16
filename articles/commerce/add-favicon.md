---
title: Tilføj en favicon
description: I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.
author: bicyclingfool
ms.date: 08/31/2020
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
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797713"
---
# <a name="add-a-favicon"></a>Tilføje et favoritikon

[!include [banner](includes/banner.md)]

I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.

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

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Oprette et fragment, der indeholder en metakode til dit favoritikon

Følg disse trin for at oprette et fragment, der indeholder en metakode til dit favoritikon.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg **Metakoder** i dialogboksen **Nyt fragment** som det modul, fragmentet er baseret på.
1. Angiv et navn til fragmentet, og vælg derefter **OK**.
1. Vælg det underordnede **Standardmetamoder** i fragmenthierarkitræet.
1. Vælg **Tilføj** under **Metakoder** i ruden til højre, og angiv derefter den HTML-streng, du oprettede til favoritikonet tidligere. 
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere fragmentet.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Føj fragmentet for metakode til HTML-hovedsektionen på dine sider

Følge disse trin for at føj fragmentet for metakoder til sektionen for HTML-**hoved** på dine sider.

1. Gå til **Skabeloner**, åbn skabelonen for de sider, du vil føje dit favoritikon til, og vælg derefter **Rediger**.
1. Vælg ellipseknappen (**...**) i skabelonhierarkitræet til højre for containeren i **HTML-hovedet**, og vælg derefter **Tilføj fragment**.
1. Vælg det fragment for metakoder, du oprettede tidligere, i dialogboksen **Vælg fragment**, og vælg derefter **OK**.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.

> [!NOTE]
> Hvis webstedet bruger mere end én skabelon, skal du føje fragmentet for metakoder til dem alle.

Når du får vist sider, der er baseret på den skabelon, du har føjet til fragmentet for metakoder, burde du nu kunne se favoritikonet på browserfanen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
