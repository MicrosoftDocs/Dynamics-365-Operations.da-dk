---
title: Tekstblokmodul
description: Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025591"
---
# <a name="text-block-module"></a>Tekstblokmodul


[!include [banner](includes/banner.md)]

Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et tekstblokmodul er et modul, der bruges til at tilføje tekstindhold. Det kan være oplysninger og kampagneindhold.

Tekstblokmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side. De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Eksempler på tekstblokmoduler i e-handel

Tekstblokmoduler kan bruges på følgende måder:

* Til at få vist produktfunktioner på en side med produktdetaljer.
* Til oplysninger på en hvilken som helst side. De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".
* Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer (f. eks. "Gratis levering af ordrer over $50").
* For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").

## <a name="text-block-module-properties"></a>Egenskaber for Tekstblokmodul

| Egenskabsnavn     | Value                                            | Beskrivelse |
|-------------------|--------------------------------------------------|-------------|
| RTF         | RTF                                        | Afsnitstekst. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst. |
| Brugerdefineret klassenavn | Klassenavn for overlappende typografiark (CSS)        | Navnet på en brugerdefineret CSS-klasse, som en udvikler leverer til at formatere dette modul. Klassenavnet skal defineres i temapakken. |
| Skrifttypens størrelse         | **Lille**, **Mellem**, **Stor**eller **Ekstra stor** | Indholdets skriftstørrelse. |

## <a name="add-a-text-block-module-to-a-page"></a>Føj et tekstblokmodul til en side

Hvis du vil føje et tekstblokmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **Indholdsskabelon**. 
1. På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.
1. Afslut redigeringen af skabelonen, og udgiv den.
1. Brug den indholdsskabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsside**.
1. Tilføj et containermodul på pladsen **Hoved** på den nye side.
1. Angiv egenskaben **Bredde** til **Fyld container**i egenskabsruden for containermodulet.
1. Føj et tekstblokmodul til containermodulet. 
1. Føj tekst til **RTF-tekst**-feltet i egenskabsruden af tekstblokmodulet.
1. Afslut redigeringen af siden, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)

