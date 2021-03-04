---
title: Arbejdstidskalendere
description: Dette emne beskriver arbejdstidskalendere i Dynamics 365 Human Resources, og hvordan du konfigurerer kalendere.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: e77cc8921f2a8cfa1a48fda589fd20aae00e0fd4
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690070"
---
# <a name="working-time-calendars"></a>Arbejdstidskalendere

Med arbejdstidskalenderen kan du oprette en kalender med de timer og dage, hvor medarbejderne arbejder i din organisation. Kalendere strømliner som standard anmodningsprocessen for fravær i timer eller dage. Når en medarbejder sender en anmodning om fravær, behøver de ikke at tænke på helligdage og lukninger, der er håndteret for dem via arbejdstidskalenderen.

## <a name="setting-up-a-working-time-calendar"></a>Konfigurer en arbejdstidskalender

Kalendere omfatter genereringsoplysninger, de dage og timer, du vil have medtaget, dagene i kalenderen, arbejdstider for disse dage samt tilmeldte medarbejdere. 

Følg disse trin for at konfigurere en kalender:

1. Klik på **Kalendere** på siden **Organisationsadministration**.

2. I handlingsruden skal du vælge **Ny** og indtaste et navn og en beskrivelse.

3. Vælg arbejdsdage for organisationen, og angiv arbejdstid.

4. Tilføj helligdage og lukninger ved hjælp af knappen **Tilføj**.

5. Angiv navnet på og beskrivelsen af helligdage og lukninger, f.eks. danske helligdage og andre lukkedage. Angiv datoerne for helligdage og lukninger. Gem listen over helligdage og lukninger, og luk siden.

6. Vælg listen over helligdage og lukninger i rullemenuen.

7. Hvis dine medarbejdere har ikke-arbejdstid, f.eks. frokostpauser eller andre pauser, kan du tilføje dem også. Vælg **Ikke-arbejdstid**, og angiv navnet og tidsintervallet. Luk siden. 

8. Klik på **Tilføj** for at tilføje ikke-arbejdstiden i din kalender.

9. Under fanen **Dage** skal du vælge **Generér** for at generere dagene i kalenderen. Angiv datointervallet for kalenderen. Dagene og arbejdstiderne oprettes på basis af de arbejdsdage og -tider, der er defineret under genereringsindstillinger, sammen med de datoer, der er valgt.

10. Vælg **Tildel til medarbejdere** i handlingsruden for at tildele medarbejdere en kalender. Vælg de medarbejdere, som du vil tildele denne kalender, og klik derefter på **Tildel**.

Medarbejdere er ikke forpligtet til at have kalendere tildelt. Hvis en arbejdstidskalender er defineret, udelades fridage automatisk i anmodningen. Omfanget i timer eller dage bruger som standard de arbejdstider, der er defineret i kalenderen. Hvis medarbejderen ikke er tildelt en kalender, er alle dage tilgængelige for fravær, og længden af fraværet er ikke standard for anmodningen. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]