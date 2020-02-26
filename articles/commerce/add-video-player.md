---
title: Videoafspillermodul
description: Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025637"
---
# <a name="video-player-module"></a>Videoafspillermodul


[!include [banner](includes/banner.md)]

Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Videoafspillermodulet bruges til at understøtte videoafspilning. Den kan føjes til en hvilken som helst side, som videoindholdet uploades til og vises i CMS (Content Management system). Videoafspillermodulet understøtter medietypen .mp4.

## <a name="video-player-module"></a>Videoafspillermodul

Videoafspillermodulet kan bruges til at vise videoer på et e-handels-websted. Det understøtter alle afspilningsmuligheder, f.eks. afspilning, pause, fuld størrelse, lydbeskrivelser og undertekster. Videoafspillermodulet understøtter også tilpasning af undertekster, så de opfylder Microsofts tilgængelighedsstandarder. Du kan f. eks. tilpasse skriftstørrelsen og baggrundsfarven.

Videoafspillermodulet understøtter også sekundære lydspor. I forbindelse med at en video uploades til CMS, kan der også uploades et sekundært lydspor. Videoafspillermodulet kan derefter afspille det sekundære lydspor, hvis en bruger vælger det.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Eksempler på videoafspillermoduler i e-handel

- Instruktionsvideoer på sider med produktoplysninger eller marketingsider
- Kampagnevideoer eller videoer om politikker på en hvilken som helst marketingside
- Marketingvideoer, der fremhæver produktfunktioner på sider med produktdetaljer eller marketingsider

### <a name="video-player-module-properties"></a>Egenskaber for videoafspillermodul

| Egenskabsbetegnelse         | Værdi                               | Beskrivelse |
|-----------------------|-------------------------------------|-------------|
| Automatisk afspilning             | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen automatisk. |
| Slå mikrofon fra                  | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, deaktiveres lyden. Standardværdien for denne afspiller er **Falsk**. I Google Chrome-browseren er automatisk afspilning af videoer som standard slået fra, og lyden afspilles kun, hvis brugeren afspiller videoen manuelt. |
| Løkke                  | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen gentagne gange i en løkke. |
| Medier                 | Videofilens sti og navn | Den videofil, der afspilles af videoafspilleren. |
| Afspil i fuldskærmstilstand       | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen i fuldskærmstilstand. |
| Udløser til midlertidig afbrydelse af afspilning    | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises afspil/pause-knappen på videoen. |
| Knapper til videoafspiller | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises alle videoafspillerens kontrolelementer. Disse kontrolelementer omfatter knapper til afspilning og pause, en statusindikator og valg af undertekster. |
| Skjul plakatbillede     | **Sand** eller **Falsk**               | En video kan have en plakatramme. Når værdien for denne egenskab er angivet til **Sand**, er plakatrammen skjult. |
| Maskeringsniveau            | Et tal mellem **0** og **100** | Den maske, der anvendes på videoen til stylingen. |

## <a name="add-a-video-player-module-to-a-page"></a>Føje et videoafspillermodul til en side

> [!NOTE] 
> Før du opretter et videoafspillermodul, skal du først uploade en video til mediebiblioteket.

Hvis du vil føje et videoafspillermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **videoafspillerskabelon**.
1. Tilføj et containermodul på pladsen **Hoved** på standardsiden.
1. Tilføj videoafspiller- og atmosfæreskabende videoafspiller-modulet i containermodulet.
1. Afslut redigeringen af skabelonen, og udgiv den.
1. Brug den indholdsskabelon, som du har oprettet, til at oprette en side med navnet **videoafspillerside**.
1. Tilføj et videoafspillermodul på pladsen **Hoved** på den nye side.
1. Vælg **Tilføj en video**i egenskabsruden for videoafspillermodulet.
1. Vælg en video i dialogboksen **Medievælger**, og vælg derefter **Upload nyt medieelement**.
1. Gem siden, og se en forhåndsvisning af den. Nu vises videomodulet på siden. Du kan ændre flere indstillinger for at tilpasse funktionsmåden af modulet.
1. Afslut redigeringen af siden, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)
