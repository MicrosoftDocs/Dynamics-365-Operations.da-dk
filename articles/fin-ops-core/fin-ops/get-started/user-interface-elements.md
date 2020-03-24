---
title: Brugergrænsefladeelementer
description: I dette emne beskrives brugergrænsefladeelementerne i appen.
author: tlefor
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 37c5a6c20a6e77a50ece01046ee28074c927bd76
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091817"
---
# <a name="user-interface-elements"></a>Brugergrænsefladeelementer

I dette emne beskrives de brugergrænsefladeelementer, der benyttes i appen. Før brugerne kan navigere i grænsefladen, er det vigtigt at kende navnene og funktionerne for de elementer, der udgør grænsefladen.

## <a name="overview"></a>Overblik

- **Handlingsrude** - Linjen under navigationslinjen. Her kan du vælge faner for at ændre poster, der vises på siden. Du kan redigere og gemme posterne her.  
- **Faktaboks** - Du kan få vist oplysninger og følge aktiviteterne for bestemte poster i denne rude.  
- **Faktaboksrude** Her kan du rulle gennem forskellige aspekter af en post, der skal vises i faktaboksen.  
- **Filterrude** – På nogle sider kan du åbne denne rude ved at vælge **Vis filtre**. Det giver dig mulighed for at indsnævre de resultater, der er synlige på siden.  
- **Navigationslinje** - Linjen øverst i grænsefladen. Den indeholder **Dynamics 365-portalen**, **Søg**, **firmavælger**, **Handlingscenter**, **Indstillinger**, **Hjælp og support** og brugerprofilen.  
- **Navigationsliste** - På nogle sider kan du rulle gennem denne rude for at finde en bestemt post. Når indstillingen er valgt, vises detaljerne for posten på siden.  
- **Navigationsrude** - Ruden længst til venstre. Herfra kan du finde en hvilken som helst side i produktet.  
- **Side** - Det centrale fokus i grænsefladen. Valg foretaget i de andre komponenter i brugergrænsefladen har indflydelse på, hvilke poster der vises her.  
- **Rude** - Ruden længst til højre. Ruden åbnes i nogle tilfælde, når aspekter af en post skal ændres og gemmes.  
- **Fane** - Ved referencer til handlingsruden er det en menu med indstillinger, der vises, når du vælger en angivet indstilling i handlingsruden.  

![Følgende billede viser placeringen af disse elementer i grænsefladen.](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a>Faner, felter og sektioner

En *fane* kan vælges på siden, hvor den åbner et andet aspekt af en post på samme side. Ofte giver det dig mulighed for at ændre visse *felter* eller elementer i brugergrænsefladen, der tillader skrevet input. 

Et *oversigtspanel* er en fane, hvor det er muligt at se flere faner på én gang. Du kan udvide et oversigtspanel ved at vælge den nedadgående pil i højre side af panelet.

![Følgende billede viser et eksempel på faner og oversigtspaneler.](media/user-interface-02.png)

En *sektion* minder om en fane. Ordet "sektion" bruges ofte til at beskrive et hvilket som helst område af en side, hvor en bestemt kategori af oplysninger organiseres. I følgende billede er Opsummering, Ordrer og favoritter og Links alle eksempler på sektioner.

![Følgende billede viser et eksempel på faner og en sektion.](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a>Dialogbokse og rullemenuer

En *dialogboks* er en rude, der åbnes, når der foretages bestemte valg for at ændre eller oprette en post. Dialogbokse indeholder felter, hvor du kan indtaste input. Nogle gange kan du i et bestemt felt vælge en nedadgående pil, der åbner en liste over indstillinger, du kan vælge mellem. Dette kaldes en *rullemenu*. På følgende billede indeholder felterne **Type** og **Debitorgruppe** muligheden for at åbne en rullemenu.

![Følgende billede viser et eksempel på en dialogboks.](media/user-interface-04.png)

I nogle tilfælde åbnes en dialogboks tæt på en bestemt knap, når du vælger den. Dette kaldes en *rulledialogboks*. På følgende billede er knappen **Pr. dato** valgt, hvilket har åbnet en rulledialogboks.

![Følgende billede viser et eksempel på en rulledialogboks.](media/user-interface-05.png)

## <a name="notifications"></a>Beskeder

Visse ændringer af de objekter, du overvåger, vises som *beskeder*. Med beskeder kan du blive underrettet, når en bestemt kundes oplysninger er blevet ændret, eller du kan få en advarsel, når systemet ikke kan acceptere input, du har tilføjet i bestemte felter. Du kan få mere at vide om, hvordan du kan tilpasse, hvad du modtager beskeder om, i [Oversigt over påmindelser](../get-started/alerts-overview.md).

Beskeder vises på mange forskellige måder.
- **Billedforklaring** - Denne vises ved siden af et felt, en fane eller en anden knap med en forklaring på, hvad funktionen bruges til. 
- **Handlingscenter** - Der vises en boks med beskeden ved siden af handlingscenterknappen på navigationslinjen. Du kan få vist detaljer om beskeden ved at vælge **Handlingscenter**.  
- **Meddelelseslinje** - Denne linje vises under handlingsruden.  

Følgende billede viser eksempler på disse typer beskeder.

![Følgende billede viser eksempler på beskeder.](media/user-interface-06.png)

- **Meddelelsesboks** - Boksen vises oven over grænsefladen, og du skal interagere med den, før du kan fortsætte med at bruge produktet.  

![Følgende billede viser et eksempel på en meddelelsesboks.](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a>Værktøjslinjer, gitre og lister

En *værktøjslinje* indeholder værktøjer, du kan bruge til f.eks. at tilføje felter eller fjerne poster. Nogle gange vises der en værktøjslinje på siden over et *gitter*. Dette område, gitteret, er den betegnelse, der bruges om rækker af poster med forskellige datakolonner. Der er ikke værktøjslinjer over alle gitre.

En *liste* er den betegnelse, der bruges om en samling poster, som du kan rulle gennem. Du kan placere disse poster på siden ved at markere dem. Ofte vil dette åbne et gitter.

![Følgende billede viser eksempler på værktøjslinjer, gitre og lister.](media/user-interface-08.png)
