---
title: Handlingssøgning
description: I denne artikel beskrives handlingssøgningsfunktionen. Med handlingssøgning kan du finde og køre handlinger på en side.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d01247aa356625cb759306e5ead2afd3cdeb840f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191310"
---
# <a name="action-search"></a>Handlingssøgning

[!include [banner](../includes/banner.md)]

I denne artikel beskrives handlingssøgningsfunktionen. Med handlingssøgning kan du finde og køre handlinger på en side.

## <a name="introduction"></a>Introduktion

Sider viser primært kommandoer i handlingsruder, både standardhandlingsruden, som vises øverst på en side, og værktøjslinjerne, der vises i forskellige afsnit på siden. I tidligere versioner kan du med en nøgletipfunktion hurtigt få adgang til en knap i en handlingsrude ved at trykke på Alt-tasten og derefter en række bogstaver.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

De vigtigste tip er ikke længere tilgængelige, men er blevet erstattet af handlingssøgningsfunktionen. Med denne nye funktion kan du hurtigt søge efter og køre en knap fra alle synlige handlingsruder.

## <a name="using-action-search"></a>Brug af handlingssøgning

Hvis du vil bruge handlingssøgefunktionen, skal du følge disse trin.

1. Klik på feltet **handlingssøgning** i handlingsruden. (Feltet **handlingssøgning** indeholder et forstørrelsesglasikonet.)
2. Skriv hele navnet eller en del af navnet på den knap, du vil køre. Du kan også søge ved hjælp af ord fra knappens "sti". (Se næste afsnit i denne artikel for at få flere oplysninger). Typisk vises en knap omtrent øverst på listen over resultater, når du har skrevet to til fire tegn.
3. Søg efter og kør knappen på listen over resultater (ved hjælp af musen eller tastaturet).

Når knappen er kørt, returneres fokus til din sidste position på siden, så du kan fortsætte med at arbejde.

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøgning ved at trykke på Ctrl+/ eller Alt+Q. Tryk på tastaturgenvejen igen for at returnere fokus til din sidste position på siden.

## <a name="understanding-the-results-list"></a>Om listen over resultater

Ofte skal du kende både placeringen af en knap og dens sammenhæng for fuldt ud at forstå formålet med denne knap. Derfor vises yderligere oplysninger for hvert element på listen over resultater for at hjælpe dig med at forstå, præcis hvilke knapper der vises på listen. Især vises knappens "sti". Stien kan indeholde etiketter til de følgende elementer i brugergrænsefladen, alt efter hvad der er relevant:

- Fanen Handlingsrude
- Knapgruppe
- Menuknappen (Hvis knappen er inde i en menuknap)
- Menuseparator (Hvis knappen er inde i en navngivet gruppe inde i en menuknap)
- Gruppe eller fane på siden (f.eks navnet på et oversigtspanel)

Du har for eksempel indtastet **tot** i feltet **handlingssøgning** og er nu at undersøge listen over resultater. Den første post for en knap, der hedder **Totaler**, er fremhævet. Også knapstien **Salgsordre** &gt; **Vis** vises. **Salgsordredelen** af stien svarer til fanen **Salgsordre** fane i handlingsruden, og **visningsdelen** af stien svarer til gruppen **Visning** under denne fane. På samme måde fortæller stien til knappen **Slutrabat** (**Sælg** &gt; **Beregn**) dig, at denne knap er placeret i gruppen **Beregn** under fanen **Sælg** i handlingsruden. Derfor hjælper disse oplysninger dig til at forstå, nøjagtigt hvilken knap der udløses af handlingssøgningen (hvis du vælger denne knap på resultatlisten).

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

I det forrige eksempel viste handlingssøgning resultater fra standardhandlingsruden øverst på en side. Handlingssøgning viser også resultaterne fra synlige værktøjslinjer, der er placeret andre steder på siden. For eksempel søger du efter knappen **Disponibel lagerbeholdning**, der er placeret i oversigtspanelet **Salgsordrelinjer**. I dette tilfælde fortæller knapstien i resultatlisten (**Salgsordrelinjer** &gt; **Lager** &gt; **Vis**) dig, at knappen er placeret under overskriften **Vis** på menuknappen **Lager** i oversigtspanelet **Salgsordrelinjer**.

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Handlingssøgning vs. navigationsøgning

Hvor handlingssøgning har til formål at finde og udføre handlinger på en side, er der en separat søgemekanisme til at søge efter og navigere til sider. Du kan få flere oplysninger om denne funktion i artiklen [Navigationssøgning](navigation-search.md).
