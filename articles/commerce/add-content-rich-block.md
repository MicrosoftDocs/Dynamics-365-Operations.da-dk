---
title: Tekstblokmodul
description: Denne artikel omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270476"
---
# <a name="text-block-module"></a>Tekstblokmodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et tekstblokmodul er et modul, der bruges til at tilføje tekstindhold. Det kan være oplysninger og kampagneindhold.

Tekstblokmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side. De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Eksempler på tekstblokmoduler i e-handel

Tekstblokmoduler kan bruges på følgende måder:

* Til at få vist produktfunktioner på en side med produktdetaljer.
* Til oplysninger på en hvilken som helst side. De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".
* Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer (f. eks. "Gratis levering af ordrer over $50").
* For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").

Det følgende billede viser et eksempel på et tekstblokmodul, der bruges på en startside.

![Eksempel på et tekstblokmodul.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Egenskaber for Tekstblokmodul

| Egenskabsbetegnelse     | Værdi                                            | Betegnelse |
|-------------------|--------------------------------------------------|-------------|
| RTF         | RTF                                        | Afsnitstekst. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst. |
| Brugerdefineret klassenavn | Klassenavn for overlappende typografiark (CSS)        | Navnet på en brugerdefineret CSS-klasse, som en udvikler leverer til at formatere dette modul. Klassenavnet skal defineres i temapakken. |
| Skrifttypens størrelse         | **Lille**, **Mellem**, **Stor** eller **Ekstra stor** | Indholdets skriftstørrelse. |

## <a name="add-a-text-block-module-to-a-page"></a>Føj et tekstblokmodul til en side

Hvis du vil føje et tekstblokmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Indholdsskabelon**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Standardside** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Angiv **Indholdsside** under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg **Indholdsskabelon** under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du vil redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**. 
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. Angiv egenskaben **Bredde** til **Fyld container** i egenskabsruden for containermodulet.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Tekstblok** og derefter **OK**. 
1. Føj tekst til **RTF-tekst**-feltet i egenskabsruden af tekstblokmodulet.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
