---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (august 2018)
description: Dette emne beskriver funktioner, der er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: andreabichsel
manager: AnnBe
ms.date: 08/27/2018
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
ms.author: anbichse
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 30646de08bd5ea4b2da05bfc38da7edc320a3331
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690094"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-august-2018"></a>Nyheder eller ændringer i Dynamics 365 Talent - Core HR (august 2018)

**Build 8.1.104**

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent: Core HR.

## <a name="view-expiring-records-in-manager-self-service"></a>Se udløbende poster i Selvbetjening for leder

Du kan du se udløbende poster i Selvbetjening for leder. Med nye indstillinger er det muligt at konfigurere, hvilke oplysninger ledere kan få vist. Disse indstillinger omfatter:

-   Certifikater

-   Identifikationsnumre

-   Prøvetid

-   Screeninger

-   Test

Denne funktion giver dig også mulighed for at angive det interval af dage, hvor du vil søge efter udløbende poster.

## <a name="configurable-transfer-actions"></a>Overførselshandlinger, der kan konfigureres

Du kan konfigurere de indstillinger efter rolle, der skal være tilgængelige, under angivelsen af en anmodning om dataoverførsel. Denne funktion giver ekstra fleksibilitet på tværs af rollerne i en organisation.

For eksempel har ledere, der anmoder om medarbejderoverførsler, ikke nødvendigvis adgang til at foreslå eller angive kompensationsbeløb eller vælge den opgaveliste, der skal knyttes til anmodningen om overførslen. I dette tilfælde kan ledere oprette og sende anmodninger om overførsel, men kan ikke angive kompensations- eller opgavelistetildelinger. I denne samme konfiguration kan HR tildele de nye værdier for kompensation samt tilknytte eventuelle yderligere kontrollister, der skal fuldføres på grund af fuldførelsen af overførslen.

De nye konfigurationsindstillinger er som standard indstillet til ikke at ændre egenskaberne før denne opdatering.

## <a name="leave-and-absence"></a>Orlov og fravær

Der findes nu flere datofelter i Orlov og fravær.

Med denne funktion kan du indstille grundlaget for periodiseringsperioder på planniveau til at bruge bestemte medarbejderdatoer. Andre datoer end planstartdatoen kan bruges under orlovsperiodiseringsprocessen. Indstillinger for bestemte datoer for medarbejdere omfatter følgende værdier:

-   Brugerdefineret (tilgængelig før denne opdatering)

-   Jubilæumsdato

-   Oprindelig ansættelsesdato

-   Anciennitetsdato

-   Justeret startdato for medarbejder

-   Startdato for medarbejder

Når indstillingen er konfigureret til at bruge en af de specifikke datoer for medarbejderen, bruge registreringsprocessen den angivne dato til at beregne periodiseringsperioder. Grundlaget for periodiseringsperioder vises også på medarbejderens plantilmelding og kan hjælpe dig med at forstå, hvad der bruges i forbindelse med periodiseringen.

## <a name="microsoft-word-integration"></a>Microsoft Word-integration

I hele Core HR er dokumentskabeloner blevet aktiveret. Med denne funktion kan du oprette breve og rapporter, der er baseret på Word-skabeloner, som du opretter.

Du kan finde flere oplysninger om denne funktion i [Selvstudium til Office-integration](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).


## <a name="other-fixes"></a>Andre rettelser

Denne version indeholder også en række fejlrettelser, tilføjelse af nye objekter, rettelser af eksisterende objekter og ændringer af oversatte etiketter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]