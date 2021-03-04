---
title: Nyheder eller ændringer i Dynamics 365 Talent (1. oktober 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529654"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (1. oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2509. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinet medarbejderangivelse og navigation

Denne funktionalitet er nu tilgængelig i alle miljøer. Hvis du vil aktivere funktionen, skal du gå til **Systemadministration > Links > Opsætning > Systemparametre > Funktioner i prøveversion**. Vælg **Udvidet arbejderform og navigation**. Dette aktiverer disse ændringer for alle brugere. Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.

Du kan finde oplysninger under [Strømlinet medarbejderangivelse og navigation](./streamlined-employee-entry.md). Hvis du vil se videoen med ændringerne, skal du gå til [Oversigt over frigivelsesbølge 2 til Dynamics 365 for Talent i 2019](https://aka.ms/ROGT19RW2ROV).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Du kan aktivere funktioner i prøveversioner i sandkasse- og testmiljøer

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er Produktion eller Sandkasse. Forekomster af typen Sandkasse giver mulighed for tidlig test af nye funktioner. Hvis en af de eksisterende forekomster skal opdateres til Sandkasse-forekomsttypen, skal du kontakte Support for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Kompensationsdato er som standard en anden dato end stillingstildelingen (337694)

Med denne ændring er kompensationens startdato som standard startdatoen for stillingstildelingen.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Kompensation kan ikke afsluttes sammen med dens stillingstildeling (328993)

Med denne ændring kan du afslutte kompensation, når du afslutter stillingstildelingen ved at bruge **Afslut tildeling** på siden **Tildeling af arbejderstillinger**, hvor personalehandlinger er slået til.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Validering af bankkontoen kræver registrerings- og kontonumre alle steder (340403)

Med denne uges ændringer er der tilføjet en ny konfigurationsindstilling til deaktivering af påkrævet validering af **Registreringsnummer** og **Kontonummer**. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>Vedhæftede filer er ikke aktiveret i MSS-performancekladder for feedback om ydeevne (341794)

Med denne uges udgivelse er vedhæftede filer aktiveret for feedbackelementer på siden med performancekladde.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Detaljer om orlovsanmodning synkroniseres ikke fra Common Data Service til Talent (369608)

Med disse ændringer synkroniseres de detaljer om orlovsanmodning, der opdateres i Common Data Service, tilbage til Talent.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Jobbeskrivelsen vises ikke for jobbet på siden Analyse af kompetencekløft (369398)

I denne uges build vises beskrivelsen, når jobbet vælges på siden **Analyse af kompetencekløft**.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Medarbejdere, ledere og personalemedarbejdere kan udskrive en medarbejders performancegennemgang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]