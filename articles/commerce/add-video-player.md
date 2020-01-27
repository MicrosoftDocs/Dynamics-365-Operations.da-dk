---
title: Videoafspillermodul
description: Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885895"
---
# <a name="video-player-module"></a>Videoafspillermodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Videoafspillermoduler bruges til at understøtte videoafspilning. Der findes to videoafspillermoduler i startsættet til butikken: atmosfæreskabende videoafspiller-modulet og videoafspillermodulet. Begge afspillere understøtter medietypen. mp4.

## <a name="ambient-video-player-module"></a>Atmosfæreskabende videoafspiller-modul

Atmosfæreskabende videoafspiller-modul understøtter korte informationsvideoer. Det skal bruges til videoer, der er mindre end fem sekunder lange. Denne spiller understøtter begrænsede videoafspilningsfunktioner, f. eks. afspilning og pause.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Eksempler på atmosfæreskabende videoafspiller-moduler i e-handel

- Korte informationsvideoer, der fremhæver nye produkter på hjemmesiden
- Korte informationsvideoer, der fremhæver produktfunktioner på en side med produktdetaljer

### <a name="ambient-video-player-module-properties"></a>Egenskaber for atmosfæreskabende videoafspiller-modul

| Egenskabsbetegnelse     | Værdi                 | Beskrivelse |
|-------------------|-----------------------|-------------|
| Automatisk afspilning          | **Sand** eller **Falsk** | Når værdien er angivet til **Sand**, afspilles videoen automatisk. |
| Slå mikrofon fra              | **Sand** eller **Falsk** | Når værdien er angivet til **Sand**, deaktiveres lyden. Standardværdien for denne afspiller er **Sand**. I Google Chrome-browseren er videolyden som standard slået fra, og lyden afspilles kun, hvis brugeren afspiller videoen manuelt. |
| Løkke              | **Sand** eller **Falsk** | Når værdien er angivet til **Sand**, afspilles videoen gentagne gange i en løkke. |
| Medier             |  Videofilens sti og navn | Den videofil, der afspilles af videoafspilleren. |
| Afspilningskontrolelementer | **Sand** eller **Falsk** | Når værdien er angivet til **Sand**, vises afspil/pause-knappen på videoen. Hvis værdien er angivet til **Falsk**, vises afspil/pause-knappen ikke, men brugerne kan stadig afbryde og genoptage videoen ved hjælp af tastaturet. |

## <a name="video-player-module"></a>Videoafspillermodul

Videoafspillermodulet kan bruges til at vise videoer på et e-handels-websted. Det understøtter alle afspilningsmuligheder, f. eks. afspilning, pause, fuld størrelse og undertekster. Videoafspillermodulet understøtter også tilpasning af undertekster, så de opfylder Microsofts tilgængelighedsstandarder. Du kan f. eks. tilpasse skriftstørrelsen og baggrundsfarven.

Videoafspillermodulet understøtter også sekundære lydspor. I forbindelse med at en video overføres, kan der også overføres et sekundært lydspor. Videoafspillermodulet kan derefter afspille det sekundære lydspor, hvis en bruger vælger det.

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
| Afspilningskontrolelementer     | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises afspil/pause-knappen på videoen. Hvis værdien er angivet til **Falsk**, vises afspil/pause-knappen ikke, men brugerne kan stadig afbryde og genoptage videoen ved hjælp af tastaturet. |
| Afspil i fuldskærmstilstand       | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, afspilles videoen i fuldskærmstilstand. |
| Kontrolelementer              | **Sand** eller **Falsk**               | Når værdien er angivet til **Sand**, vises alle kontrolelementer. Disse kontrolelementer omfatter knapper til afspilning og pause, en statusindikator og undertekster. |
| Skjul plakatramme     | **Sand** eller **Falsk**               | En video kan have en plakatramme. Når værdien for denne egenskab er angivet til **Sand**, er plakatrammen skjult. |
| Maskeringsniveau            | Et tal mellem **0** og **100** | Den maske, der anvendes på videoen til stylingen. |
| Typografi for fuldskærmsikon | **Firkant** eller **Pil**             | Typografien for det fuldskærmsikon, der vises i videoafspilleren. |

## <a name="add-a-video-player-module-to-a-page"></a>Føje et videoafspillermodul til en side

Hvis du vil føje et videoafspillermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **videoafspillerskabelon**.
1. Tilføj et containermodul på pladsen **Hoved** på standardsiden.
1. Tilføj videoafspiller- og atmosfæreskabende videoafspiller-modulet i containermodulet.
1. Tjek skabelonen ind, og publicer den.
1. Brug den indholdsskabelon, som du netop har oprettet, til at oprette en side med navnet **videoafspillerside**.
1. Tilføj et atmosfæreskabende videoafspiller-modul på pladsen **Hoved** på den nye side.
1. Gå til **Medier** i indstillingerne for atmosfæreskabende videoafspiller-modulet, og overfør en videofil. Du kan ændre **Automatisk afspilning**, **Løkke** og andre egenskaber efter behov.
1. Gem siden, og se en forhåndsvisning af den.
1. Tilføj et videoafspillermodul på pladsen **Hoved** på den nye side.
1. Gå til **Medier** i indstillingerne for videoafspillermodulet, og overfør en videofil.
1. Gem siden, og se en forhåndsvisning af den. Du kan nu se begge videomoduler på siden. Du kan ændre flere indstillinger for at tilpasse funktionsmåden for de enkelte moduler.
1. Tjek siden ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Påmindelsesmodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-modul](add-hero-module.md)
