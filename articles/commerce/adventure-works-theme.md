---
title: Oversigt over Adventure Works-tema
description: Dette emne giver et overblik over emnet Adventure Works og beskriver, hvordan det anvendes på webstedssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5bade39b1b327a0784272669ce074d9762a318c2cad6d4105f0d186c91d2593f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733222"
---
# <a name="adventure-works-theme-overview"></a>Oversigt over Adventure Works-tema

[!include [banner](includes/banner.md)]

Dette emne giver et overblik over emnet Adventure Works og beskriver, hvordan det anvendes på webstedssider i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce har et internettema for e-handel med navnet Adventure Works. Med emnet Adventure Works er du med til at tage godt fra de forskellige produkter, der er under udvikling, og som er optimeret til en god og bedre kostoplevelse. Den giver et moderne udseende, nye layout og effekterne ved animation for at give e-handelskunderne engagerende onlineindkøbsoplevelse.

## <a name="trial-environments-in-commerce"></a>Prøvemiljøer i Commerce

Hvis du vil se, hvordan Adventure Works-temaet ser ud, når det implementeres for B2C-websteder (business-to-consumer) og B2B- websteder (business-to-business), skal du besøge følgende prøvewebsteder:

- [Adventure Works B2C-websted](https://www.adventure-works.com/)
- [Adventure Works B2B-websted](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Temaegenskaber

Adventure Works-temaet indeholder følgende nye egenskaber:

- Videoafspillermodulet understøtter nu funktionaliteter til overskrift, afsnit og link, så der kan tilføjes flere historier.
- Overførslen af indhold er forbedret gennem animation.
- Handlingen "Tilføj til indkøbsvogn" aktiverer indkøbsvognen i stedet for at give en besked.
- Modulet Hurtig visning er en rude, der dias i både skrivebords- og mobilvisningsporte.
- Webstedsiderne har fået nye layout. 
- Marketingindhold kan konfigureres for indkøbsvognen og mini-indkøbsvognen, når de er tomme.
- Mini-indkøbsvognen kan vise reklamemeddelelser som f.eks. "Gratis forsendelse på ordrer over $50".
- Beskrivelseskort vises på sider for søgning og kategorier.

Adventure Works-temaet indeholder nu følgende historiemoduler i modulbiblioteket Commerce:

- [Modul til feltliste](tile-list-module.md)
- [Interaktiv funktionsmodul](interactive-feature-module.md)
- [Aktivt billedmodul](active-image-module.md)
- [Abonnementsmodul](subscribe-module.md)
- [Modul til billedliste](image-list-module.md)

Adventure Works-emnet er fuldstændigt gennemført og giver en optimeret erfaring med visning af skrivebords-, mobil- og tabletvisningsporte.

> [!IMPORTANT]
> Emnet Adventure Works og de nye moduler er tilgængelige pr. Dynamics 365 Commerce version 10.0.20.

I følgende illustration vises et eksempel på en startside, der bruger emnet Adventure Works.

![Eksempel på en startside, der bruger emnet Adventure Works](./media/aw_b2c.PNG)

I følgende illustration vises et eksempel på en listeside, der bruger emnet Adventure Works.

![Eksempel på en listeside, der bruger emnet Adventure Works](./media/Aw_list.PNG)

I følgende illustration vises et eksempel på en produktdetaljeside (PDP), der bruger emnet Adventure Works.

![Eksempel på en produktdetaljeside (PDP), der bruger emnet Adventure Works](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Brug emnet Adventure Works til B2B-websteder

Adventure Works-emnet er også referencetemaet for business-to-business (B2B-websteder). Alle B2B-moduler og -arbejdsgange er startet med emnet Adventure Works. Du kan finde flere oplysninger om, hvordan du konfigurerer et B2B-websted, i [konfigurationen af B2B-websted](./b2b/set-up-b2b-site.md).

I følgende illustration vises et eksempel på en B2B-startside, der bruger emnet Adventure Works.

![Eksempel på en B2B-startside, der bruger emnet Adventure Works](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Theme-udvidelser

Adventure Works-emnet indeholder flere themeudvidelser, f.eks. **Udvidelser til Visning** og **Moduldefinitionsudvidelser**. Gennemtemaet Adventure Works kan bruges som referencetema for at opbygge lignende udvidelser. Listesiden med emnet Adventure Works er f.eks. implementeret som en visningsudvidelse, der har en vandret forfiner. (Modsat bruges en afgrænsning i venstre rude i fabrikamtemaet).

På samme måde omfatter andre moduler moduldefinitionsudvidelser. [Modulet med ikonet for indkøbsvognen](cart-icon-module.md) indeholder f.eks. to ekstra oplysninger om **tom indkøbsvogn** og **kampagneindhold**, som implementeres ved hjælp af moduldefinitionsudvidelser. Desuden er der føjet en ny egenskab til **Mobillogo** til overskriftsmodulet for at understøtte et logo på mobile viewports. Denne egenskab implementeres som en overskriftsmoduldefinitionsudvidelse.

Du kan finde flere oplysninger om themeudvidelser i [Theme-udvidelser](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Installere Adventure Works-temaet

Du kan finde oplysninger om, hvordan du installerer Adventure Works-temaet under [Installere Adventure Works-temaet](install-adventure-works.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Modul til feltliste](tile-list-module.md)

[Interaktivt funktionsmodul](interactive-feature-module.md)

[Modulet Aktivt billede](active-image-module.md)

[Modulet Abonnement](subscribe-module.md)

[Modulet billedliste](image-list-module.md)

[Theme-udvidelser](e-commerce-extensibility/theme-module-extensions.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Oprette et B2B-e-handelswebsted](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
