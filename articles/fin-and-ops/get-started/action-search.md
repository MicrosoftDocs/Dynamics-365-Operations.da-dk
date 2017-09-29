---
title: "Handlingssøgning"
description: "I dette emne beskrives handlingssøgningsfunktionen i Microsoft Dynamics 365 for Finance and Operations. Med handlingssøgning kan du finde og køre handlinger på en side."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: cd024f2bc06fca9c21ea41fbed44efbc519cee94
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="action-search"></a>Handlingssøgning

[!include[banner](../includes/banner.md)]


I dette emne beskrives handlingssøgningsfunktionen i Microsoft Dynamics 365 for Finance and Operations. Med handlingssøgning kan du finde og køre handlinger på en side.

<a name="introduction"></a>Introduktion
------------

Siderne i Microsoft Dynamics 365 for Finance and Operations viser primært kommandoer i handlingsruder, både standardhandlingsruden, som vises øverst på en side, og værktøjslinjerne, der vises i forskellige afsnit af siden. I tidligere versioner kan du med en nøgletipfunktion hurtigt få adgang til en knap i en handlingsrude ved at trykke på Alt-tasten og derefter en række bogstaver. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) I den aktuelle version af Finance and Operations er nøgletip dog ikke længere tilgængelige, men er blevet erstattet af handlingssøgningsfunktionen. Med denne nye funktion kan du hurtigt søge efter og køre en knap fra alle synlige handlingsruder.

## <a name="using-action-search"></a>Brug af handlingssøgning
Hvis du vil bruge handlingssøgefunktionen, skal du følge disse trin.

1.  Klik på feltet **handlingssøgning** i handlingsruden. (Feltet **handlingssøgning** indeholder et forstørrelsesglasikonet.)
2.  Skriv hele navnet eller en del af navnet på den knap, du vil køre. Du kan også søge ved hjælp af ord fra knappens "sti". (Se næste afsnit i denne artikel for at få flere oplysninger). Typisk vises en knap omtrent øverst på listen over resultater, når du har skrevet to til fire tegn.
3.  Søg efter og kør knappen på listen over resultater (ved hjælp af musen eller tastaturet).

Når knappen er kørt, returneres fokus til din sidste position på siden, så du kan fortsætte med at arbejde. 

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøgning ved at trykke på Ctrl+/ eller Alt+Q. Tryk på tastaturgenvejen igen for at returnere fokus til din sidste position på siden.

## <a name="understanding-the-results-list"></a>Om listen over resultater
Ofte skal du i Finance and Operations kende både placeringen af en knap og dens sammenhæng for fuldt ud at forstå formålet med denne knap. Derfor vises yderligere oplysninger for hvert element på listen over resultater for at hjælpe dig med at forstå, præcis hvilke knapper der vises på listen. Især vises knappens "sti". Stien kan indeholde etiketter til de følgende elementer i brugergrænsefladen, alt efter hvad der er relevant:

-   Fanen Handlingsrude
-   Knapgruppe
-   Menuknappen (Hvis knappen er inde i en menuknap)
-   Menuseparator (Hvis knappen er inde i en navngivet gruppe inde i en menuknap)
-   Gruppe eller fane på siden (f.eks navnet på et oversigtspanel)

Du har for eksempel indtastet **tot** i feltet **handlingssøgning** og er nu at undersøge listen over resultater. Den første post for en knap, der hedder **Totaler**, er fremhævet. Også knapstien **Salgsordre** &gt; **Vis** vises. **Salgsordre**-delen af stien svarer til fanen **Salgsordre** i handlingsruden, og **Vis**-delen af stien svarer til gruppen **Vis** under denne fane. På samme måde viser stien til knappen **Slutrabat** (**Sælg** &gt; **Beregn**), at denne knap er placeret i gruppen **Beregn** under fanen **Sælg** i handlingsruden. Derfor hjælper disse oplysninger dig til at forstå, nøjagtigt hvilken knap der udløses af handlingssøgningen (hvis du vælger denne knap på resultatlisten). 

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

I det forrige eksempel viste handlingssøgning resultater fra standardhandlingsruden øverst på en side. Handlingssøgning viser også resultaterne fra synlige værktøjslinjer, der er placeret andre steder på siden. For eksempel søger du efter knappen **Disponibel lagerbeholdning**, der er placeret i oversigtspanelet **Salgsordrelinjer**. I dette tilfælde fortæller knapstien i resultatlisten (**Salgsordrelinjer** &gt; **Lager** &gt; **Vis**) dig, at knappen er placeret under overskriften **Vis** på menuknappen **Lager** i oversigtspanelet **Salgsordrelinjer**. 

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Handlingssøgning vs. navigationsøgning
Hvor handlingssøgning har til formål at finde og udføre handlinger på en side, er der en separat søgemekanisme til at søge efter og navigere til sider i Finance and Operations. Du kan få flere oplysninger om denne funktion i artiklen [Navigationssøgning](navigation-search.md).



