---
title: Oversigt over Adventure Works-tema
description: Dette emne giver et overblik over emnet Adventure Works og beskriver, hvordan det anvendes på webstedssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479425"
---
# <a name="adventure-works-theme-overview"></a>Oversigt over Adventure Works-tema

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne giver et overblik over emnet Adventure Works og beskriver, hvordan det anvendes på webstedssider i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce har et internettema for e-handel med navnet Adventure Works. Med emnet Adventure Works er du med til at tage godt fra de forskellige produkter, der er under udvikling, og som er optimeret til en god og bedre kostoplevelse. Den giver et moderne udseende, nye layout og effekterne ved animation for at give e-handelskunderne engagerende onlineindkøbsoplevelse.

Med emnet Adventure Works findes følgende nye arbejdsgange:

- Modulet videoafspiller understøtter nu overskrift, afsnit og links, så der kan tilføjes flere tilknytninger.
- Handlingen Tilføj til indkøbsvogn aktiverer rullevognen i stedet for at give en besked.
- Modulet Hurtig visning er en rude, der dias i både skrivebords- og mobilvisningsporte.
- Nu kan en tom indkøbsvogn forfremmelser.

Emnet Adventure Works indeholder følgende modulmoduler i modulet Commerce:

- Modulet feltliste
- Interaktivt funktionsmodul
- Modulet Abonnement
- Modulet Aktivt billede
- Modulet billedliste

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

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Modulet feltliste](tile-list-module.md)

[Interaktivt funktionsmodul](interactive-feature-module.md)

[Modulet Aktivt billede](active-image-module.md)

[Modulet Abonnement](subscribe-module.md)

[Modulet billedliste](image-list-module.md)

[Theme-udvidelser](e-commerce-extensibility/theme-module-extensions.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Oprette et B2B-e-handelswebsted](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
