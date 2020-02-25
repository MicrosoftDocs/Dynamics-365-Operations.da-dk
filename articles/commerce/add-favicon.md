---
title: Tilføj en favicon
description: I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001526"
---
# <a name="add-a-favicon"></a>Tilføj en favicon


[!include [banner](includes/banner.md)]

I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.

## <a name="overview"></a>Oversigt

Et favoritikon er en lille grafikfil, der bl.a. vises under en webbrowserfane, på adresselinjen, i browserhistorikken og i bogmærker eller favoritter. Det anbefales, at du føjer et favoritikon til dit websted, fordi det repræsenterer og forstærker dit varemærke og hjælper med at skelne dit websted fra andre websteder, som kunderne besøger.

Du kan føje flere favoritikoner med forskellig størrelse og filtype til webstedet, men i dette emne vises det, hvordan du tilføjer et enkelt favoritikon. Du bruger imidlertid den samme proces og placering ved tilføjelse af flere favoritikoner.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Overføre et favoritikon til webstedets aktivsamling

Benyt følgende fremgangsmåde for at overføre et favoritikon til webstedets aktivsamling.

1. Gå til **Aktiver \> Overfør \> Overfør aktiver**.
1. Find og vælg favoritikonet i det lokale filsystem.
1. Angiv en titel, og vælg derefter **OK**. 
1. Kopiér favoritikonets offentlige URL-adresse i egenskabsruden til højre.

> [!NOTE]
> Hvis du ikke vælger indstillingen **Publicer aktiver efter overførsel**, skal du vende tilbage til siden **Aktiver** senere og publicere favoritikonet manuelt.

## <a name="create-the-html-for-the-favicon"></a>Opret HTML-kode til favoritikonet

Du opretter HTML-koden til favoritkonet ved hjælp af følgende HTML-kodestykke. I attributten **href** skal du erstatte **"Public\_URL\_for\_your\_favicon"** med den offentlige URL-adresse, som du kopierede tidligere.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Føj HTML-koden til favoritikonet til elementet \<head\> for dine sider

Du føjer et favoritikon til dit websted ved at bruge samme fremgangsmåde, der bruges til at føje enhver HTML-type/ethvert HTML-script til elementet **\<head\>** for siderne på webstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Vælg et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

