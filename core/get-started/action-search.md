---
title: "Handlingssøgning"
description: "I denne artikel beskrives søgefunktionen handling i Microsoft Dynamics 365 for operationer. Handling søgning kan du finde og køre handlinger på en side."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Handlingssøgning

I denne artikel beskrives søgefunktionen handling i Microsoft Dynamics 365 for operationer. Handling søgning kan du finde og køre handlinger på en side.

<a name="introduction"></a>Introduktion
------------

Siderne i Microsoft Dynamics 365 for operationer fremvise primært kommandoer i Handlingsruder, både standard handlingsruden, der vises øverst på en side og de værktøjslinjer, der vises i forskellige dele af siden. I tidligere versioner kan en nøgle-tip-funktionen du hurtigt få adgang til en knap eller en handlingsrude ved at trykke på Alt-tasten og derefter en række breve. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png), i den aktuelle version af Dynamics 365 for operationer nøgle tip er ikke længere tilgængelige, men er blevet erstattet af søgefunktionen handling. Med denne nye funktion kan du hurtigt søge efter og køre en knap fra alle synlige handlingsruder.

## <a name="using-action-search"></a>Brug af handlingssøgning
Hvis du vil bruge handlingssøgefunktionen, skal du følge disse trin.

1.  Klik på feltet **handlingssøgning** i handlingsruden. (Feltet **handlingssøgning** indeholder et forstørrelsesglasikonet.)
2.  Skriv hele eller en del af navnet på den knap, du vil køre. Du kan også søge ved hjælp af ord fra en knap "sti." (Se næste afsnit i denne artikel for at få flere oplysninger). Typisk vises en knap nær toppen af listen over resultater, når du har skrevet to til fire tegn.
3.  Søg efter og kør knappen på listen over resultater (ved hjælp af musen eller tastaturet).

Når knappen er kørt, returneres fokus til din sidste position på siden, så du kan fortsætte med at arbejde. 

[![handling søgefelt](./media/action-search-field.png)](./media/action-search-field.png)

Du kan også starte handlingssøgning ved at trykke på Ctrl+/ eller Alt+Q. Tryk på tastaturgenvejen igen for at returnere fokus til din sidste position på siden.

## <a name="understanding-the-results-list"></a>Om listen over resultater
Ofte i Dynamics 365 for operationer, skal du kende placeringen, og som led i en knap til fuldt ud at forstå formålet med denne knap. Derfor vises yderligere oplysninger for hvert element på listen over resultater, kan hjælpe dig med at forstå, præcis som knapperne vises på listen. Især vises knappens "sti". Stien kan indeholde etiketter til de følgende elementer i brugergrænsefladen, alt efter hvad der er relevant:

-   Fanen Handlingsrude
-   Knapgruppe
-   Menuknappen (Hvis knappen er inde i en menuknap)
-   Menuseparator (Hvis knappen er inde i en navngivet gruppe inde i en menuknap)
-   Gruppe eller fane på siden (f.eks navnet på et oversigtspanel)

Du har for eksempel indtastet **tot** i feltet **handlingssøgning** og er nu at undersøge listen over resultater. Den første post for en knap, der hedder **totaler**, er fremhævet. En knap sti i **salgsordre**&gt;**se** vises også. Den **salgsordre** del af stien, der svarer til den **salgsordre** fane i handlingsruden, og den **visning** del af stien, der svarer til den **Vis** under denne fane. På samme måde, stien til den **Slutrabat** knap (**sælger**&gt;**Beregn**) oplyser, at denne knap er placeret i den **Beregn** i den **sælger** fane i handlingsruden. Derfor hjælper disse oplysninger dig med at forstå, nøjagtigt hvilken knap udløser handling søgning (Hvis du vælger knappen på resultatlisten). 

[![handling-search-felt-med-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

I det forrige eksempel viste handlingssøgning resultater fra standardhandlingsruden øverst på en side. Handlingssøgning viser også resultaterne fra synlige værktøjslinjer, der er placeret andre steder på siden. For eksempel, du søger efter den **beholdninger** knap, der er placeret på den **salgsordrelinjer** oversigtspanelet. I dette tilfælde knappen stien i resultatlisten (**salgsordrelinjer**&gt;**lager**&gt;**Vis**) fortæller dig, at knappen er placeret under den **Vis** overskrift på den **lager** -menuknap i den **salgsordrelinjer** oversigtspanelet. 

[![på for lagerbeholdning](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Handlingssøgning vs. navigationsøgning
Handling søgning har til formål at finde og udføre handlinger på en side, er der en separat søgning mekanisme til at søge efter og navigere til siderne i Dynamics 365 for operationer. Yderligere oplysninger om denne funktion finder du på [Navigation Søg](navigation-search.md) artikel.


