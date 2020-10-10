---
title: Videoafspillermodul
description: Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 3cf7ead9a5340d5db37a87bdf131ba87681d5a82
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817055"
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

Det følgende billede viser et eksempel på et videoafspillermodul på en startside.

![Eksempel på et videoafspillermodul](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Egenskaber for videoafspillermodul

| Egenskabsbetegnelse         | Værdi                               | Beskrivende tekst |
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

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I diaglogboksen **Ny skabelon** under **Skabelonnavn** skal du angive **Videoafspillerskabelon** og derefter vælge **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Videoafspiller** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge den videoafspillerskabelon, du har oprettet. Under **Sidenavn** skal du angive **Videoafspillerside** og derefter vælge **OK**.
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Videoafspiller** og derefter **OK**.
1. Vælg **Tilføj en video** i egenskabsruden for videoafspillermodulet.
1. Vælg en video i dialogboksen **Medievælger**, og vælg derefter **Upload nyt medieelement**.
1. Vælg en videofil i Stifinder, og vælg derefter **Åbn**.
1. I dialogboksen **Overfør medieelement** skal du angive en titel og andre nødvendige oplysninger og derefter vælge **OK**.
1. I dialogboksen **Medievælger** skal du vælge **Luk**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Nu vises videomodulet på siden. Du kan ændre flere indstillinger for at tilpasse funktionsmåden af modulet.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)
