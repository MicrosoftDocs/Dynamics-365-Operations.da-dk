---
title: Nyheder eller ændringer i Dynamics 365 for Talent (14. marts 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38641d6a84340112ce15335533795ed7faf91123
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517641"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (14. marts 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Der indgår mindre fejlrettelser i denne version.

## <a name="changes-in-onboarding"></a>Ændringer i Onboarding
Der indgår mindre fejlrettelser i denne version.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
**Build 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Resultatstyring virker ikke i alle scenarier, når der anvendes duplikerede sikkerhedsroller
Der blev i forbindelse med denne udgivelse foretaget ændringer, som tillader resultatstyringscenarier, når der anvendes ude-af-boksen-roller eller duplikerede roller.

### <a name="mass-assign-checklists-to-workers"></a>Kontrollister til medarbejdere i forbindelse med massetildeling
Med denne ændring er det muligt for dig at vælge flere medarbejder og bulktildele en eller flere kontrollister til de pågældende medarbejdere. 

### <a name="platform-update-24"></a>Platform update 24
Yderligere oplysninger om Platform update 24 finder du i [Nyheder eller ændringer i Dynamics 365 for Finance and Operations Platform update 24 (marts 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Væsentlige ændringer i platform 24 omfatter: 

- Påmindelser er aktiveret i Talent.
- Opdateringsnavigationslinjen er nu tilpasset overskriften i Office.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Opdateringer af kontorlokaliteter flytter indholdet til toppen af arbejderens liste
Med den nuværende udgivelse vil en ændring af kontorets lokalitet ikke længere flytte indholdet for den arbejder, du kigger på, når du tildeler en kontorlokalitet.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Slutdatoen for tildelingen af en stilling fremgår ikke korrekt af arbejderens ansættelses- og transaktionshandlinger
Slutdatoer for tildelingen af en stilling vises nu korrekt på grundlag af brugerens foretrukne tidszonen, når denne foretager handlingerne.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service-jobenheden tillader ikke, at felterne "Jobtype" og "Jobfunktion" opdateres
Common Data Service-enheder synkroniseres nu korrekt, når de opdateres via Common Data Service.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)
I mange organisationer har de ansvarlige for kompensationer og frynsegoder muligvis kun har adgang til visse kompensationsposter. Disse kan være til ledere eller medarbejdere i bestemte områder. Med denne ændring kan Personale administrere og vedligeholde kompensationsplaner for forskellige medarbejdergrupper i organisationen. Du kan tildele sikkerhedsroller til faste og variable planer, som bestemmer adgangen til planerne og medarbejderdata tilknyttet til planerne, såsom løn eller bonusposter. Alene roller med den godkendte adgang kan behandle kompensation for de pågældende medarbejdere.

###  <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med platformsopdatering 24 kan brugerne oprette påmindelsesregler, som automatisk udsender e-mailbeskeder til kontaktpersoner, når de udløses af en hændelse.

### <a name="duplicate-employee-check-interface-changes"></a>Duplikerede medarbejderkontroller: ændringer i grænsefladen
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over, hvor mange der blev fundet. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. For at undgå at forstyrre indtastningen af data åbner dubletformularen ikke automatisk.
