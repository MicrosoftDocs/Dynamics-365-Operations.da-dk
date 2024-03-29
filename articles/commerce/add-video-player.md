---
title: Videoafspillermodul
description: Denne artikel omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 919446981f7439d61b01deb57b206cd457eed919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269288"
---
# <a name="video-player-module"></a>Videoafspillermodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Videoafspillermodulet bruges til at understøtte videoafspilning. Den kan føjes til en hvilken som helst side, som videoindholdet uploades til og vises i CMS (Content Management system). Videoafspillermodulet understøtter medietypen .mp4.

## <a name="video-player-module"></a>Videoafspillermodul

Videoafspillermodulet kan bruges til at vise videoer på et e-handels-websted. Det understøtter alle afspilningsmuligheder, f.eks. afspilning, pause, fuld størrelse, lydbeskrivelser og undertekster. Videoafspillermodulet understøtter også tilpasning af undertekster, så de opfylder Microsofts tilgængelighedsstandarder. Du kan f. eks. tilpasse skriftstørrelsen og baggrundsfarven.

Videoafspillermodulet understøtter også sekundære lydspor. I forbindelse med at en video uploades til CMS, kan der også uploades et sekundært lydspor. Videoafspillermodulet kan derefter afspille det sekundære lydspor, hvis en bruger vælger det.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Eksempler på videoafspillermoduler i e-handel

- Instruktionsvideoer på sider med produktoplysninger eller marketingsider
- Kampagnevideoer eller videoer om politikker på en hvilken som helst marketingside
- Marketingvideoer, der fremhæver produktfunktioner på sider med produktdetaljer eller marketingsider

Det følgende billede viser et eksempel på et videoafspillermodul på en startside.

![Eksempel på et videoafspillermodul.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Egenskaber for videoafspillermodul

| Egenskabsbetegnelse         | Værdi                               | Betegnelse |
|-----------------------|-------------------------------------|-------------|
| Overskrift               | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard bruges **H2** overskriften, men koden kan ændres efter behov for at opfylde tilgængelighedskravene. |
| RTF             | Afsnitstekst | Modulet understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. hyperlinks og fed, understreget og kursiv tekst. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding                  | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Modulet understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |
| Undertekst              | Overskrift, tekst eller link | Der kan tilføjes yderligere sammenhæng for videoafspillermodulet, f.eks. en forfatter eller et designernavn, eller links til personlige blogs. |
| Automatisk afspilning             | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen automatisk. |
| Slå mikrofon fra                  | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, deaktiveres lyden. Standardværdien for denne afspiller er **Falsk**. I Google Chrome-browseren er automatisk afspilning af videoer som standard slået fra, og lyden afspilles kun, hvis brugeren afspiller videoen manuelt. |
| Løkke                  | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen gentagne gange i en løkke. |
| Medier                 | Videofilens sti og navn | Den videofil, der afspilles af videoafspilleren. |
| Afspil i fuldskærmstilstand       | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen i fuldskærmstilstand. |
| Udløser til midlertidig afbrydelse af afspilning    | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises afspil/pause-knappen på videoen. |
| Knapper til videoafspiller | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises alle videoafspillerens kontrolelementer. Disse kontrolelementer omfatter knapper til afspilning og pause, en statusindikator og valg af undertekster. |
| Skjul plakatbillede     | **Sand** eller **Falsk**               | En video kan have en plakatramme. Når værdien for denne egenskab er angivet til **Sand**, er plakatrammen skjult. |
| Maskeringsniveau            | Et tal mellem **0** og **100** | Den maske, der anvendes på videoen til stylingen. |

> [!IMPORTANT]
> Egenskaberne **Overskrift**, **Tekst**, **Link** og **Undertekst** er tilgængelige pr. Dynamics 365 Commerce version 10.0.20.

## <a name="add-a-video-player-module-to-a-page"></a>Føje et videoafspillermodul til en side

> [!NOTE] 
> Før du opretter et videoafspillermodul, skal du først uploade en video til mediebiblioteket.

Hvis du vil føje et videoafspillermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** under **Skabelonnavn** skal du angive **Videoafspillerskabelon** og derefter vælge **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Videoafspiller** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Angiv **Videoafspillerside** under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg den **Videoafspillerskabelon**, du oprettede, under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du vil redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**.
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Videoafspiller** og derefter **OK**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
