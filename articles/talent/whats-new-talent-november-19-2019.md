---
title: Nyheder eller ændringer i Dynamics 365 Talent (19. november 2019)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527138"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (19. november 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2621. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Platform update 31 til Finance and Operations-apps

Du kan finde flere oplysninger under [Forhåndsvisning af funktioner i Platform update 31 til Finance and Operations-apps (januar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Administration af funktioner (383856)

Arbejdsområdet **Administration af funktioner** indeholder en oversigt over de funktioner, der er leveret i hver udgave. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem. Du kan finde flere oplysninger om Administration af funktioner under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet **Administration af funktioner**, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.
 
På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet **Administration af funktioner**).
 
Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet **Administration af funktioner** angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Meddelelsen vises, når der findes en annulleret handling for en stilling (382887)

Følgende meddelelse vises ikke længere, når du vælger en bestemt stilling, og en annulleret handling er tilgængelig for stillingen: **Der er en ufuldstændig handling i gang for stillingen xxxxxx**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>I undervisningsanalyser viser Kursustypen og -statussen ugyldige data (381151)

Denne uges udgivelse opdaterede undervisningsanalyser, således at de viser **Kursustype** og **Status** korrekt.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Personalenummeret burde blive vist i formularbanneret Ny arbejder (383832)

I formularen **Ny arbejder** vises **Personalenummeret** nu i banneret for hurtig reference.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Startdatoen for stilling bestemmer den Jobpost, der skal bruges, når der hentes et kompensationsniveau under en ansættelse (350361)

I denne udgivelse bestemmer **Kompensationens startdato** det niveau, der er tildelt det nye job.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Tilpassede pluklistefelter i Stillingstabellen synkroniseres ikke til Common Data Service (387503)

Med denne udgivelse synkroniseres plukliste-elementerne nu med Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Enhed for arbejderadresse synkroniseres ikke med Common Data Service under import af nye data (349673)

I denne uges udgivelse synkroniseres adressedata nu med Common Data Service, mens nye data importeres.

## <a name="in-preview"></a>Som eksempel

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]