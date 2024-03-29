---
title: Arbejdssteder og aktiver
description: Denne artikel beskriver arbejdssteder og aktiver i Styring af aktiver. Styring af aktiver er et avanceret modul til administration af aktiver og vedligeholdsopgaver i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8d155b8bbf981408f6f15e914fc3bb1da25c9c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111070"
---
# <a name="functional-locations-and-assets"></a>Arbejdssteder og aktiver

[!include [banner](../../includes/banner.md)]

 

Denne artikel beskriver arbejdssteder og aktiver i Styring af aktiver. Styring af aktiver er et avanceret modul til administration af aktiver og vedligeholdsopgaver i Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Overblik

Styring af aktiver kan problemfrit integreres med flere moduler i andre programmer til finans og drift. I følgende illustration vises grænsefladerne med andre moduler.

![Diagram, der viser, hvordan aktivstyring integreres med andre moduler.](media/01-overview-image.png)

Styring af aktiver giver dig mulighed for effektivt at administrere og udføre alle opgaver, der er relateret til administration og servicering af mange typer udstyr i din virksomhed. Dette udstyr omfatter maskiner, produktionsudstyr og køretøjer. Styring af aktiver understøtter også løsninger på tværs af adskillige brancher.

I følgende illustration vises en oversigt over de vigtigste funktioner, der dækkes af Styring af aktiver.

![Diagram, der viser de vigtigste funktioner i aktivstyring.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Arbejdssteder og aktiver

Arbejdssteder bruges til at administrere aktiver på lokationer. Denne styring omfatter sporing af aktivomkostninger på arbejdssteder. Arbejdssteder er struktureret hierarkisk, og lokationer kan have underlokationer. Strukturen af arbejdssteder er statisk. Med andre ord kan lokationer ikke skifte sted. Aktiver kan installeres på arbejdssteder og kan efter behov installeres på andre arbejdssteder senere.

Aktivomkostninger følger altid aktivets lokation. Hvis du med andre ord installerer et aktiv på et nyt arbejdssted, bruger aktivet automatisk de økonomiske dimensioner, der er relateret til det nye arbejdssted. Derfor er aktivets omkostninger altid relateret til det arbejdssted, som aktivet aktuelt er installeret på. Denne automatiske håndtering af økonomiske dimensioner hjælper med at sikre en fuldstændig sporing af omkostninger, når din virksomhed kontrollerer og rapporterer om arbejdssteder for projekter.

Den måde, du opbygger hierarkiet af arbejdssteder på, afhænger af virksomhedens krav til vedligeholdelse af internt udstyr eller servicering af kundeudstyr. I følgende figur vises et eksempel på arbejdssteder, der er baseret på geografiske placeringer.

![Diagram, der viser arbejdssteder baseret på geografiske placeringer.](media/03-overview-image.png)

I følgende figur vises et eksempel på arbejdssteder, der er baseret på kunder.

![Diagram, der viser arbejdssteder baseret på kunder.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
