---
title: Konfigurere firmaoplysninger i Microsoft Dynamics 365 for Talent - Attract
description: Dette emne forklarer, hvordan du konfigurerer firmaoplysninger og branding for Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c5b051497777a01ab304736f1d454391b5d98e63
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739558"
---
# <a name="configure-company-information"></a>Konfigurere firmaoplysninger
[!include[banner](../includes/banner.md)]

Administration i Microsoft Dynamics 365 for Talent: Attract indeholder konfigurationsindstillingerne, muligheder for integration og opsætningsindstillinger til programmet Attract.

## <a name="company-information"></a>Firmaoplysninger

Angiv et visningsnavn til firmaet, og tilføj et firmalogo. Det viste navn og logoet kan derefter bruges til job, stillinger og under onboardingoplevelsen.

## <a name="linkedin-integration"></a>Integration af LinkedIn

Konfigurer integrationen med LinkedIn Recruiter System Connect(RSC). Når du har oprette forbindelse til LinkedIn ved hjælp af dine LinkedIn-legitimationsoplysninger, kan du synkronisere en kandidats LinkedIn-profil, ansøgninger, samtalefeedback og ansættelsesteamnoter. Der kræves en fuld LinkedIn Recruiter-medarbejderlicens. Yderligere oplysninger om LinkedIn Recruiter finder du her [Recruiter System Connect (RSC) – FAQ](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Brugerrettigheder

Tildele roller til brugere i din organisation. Følgende roller er tilgængelige: **Administrator**, **Rekrutteringsmedarbejder**, **Ansvarlig for ansættelse** og **Skrivebeskyttet**. Du kan finde flere oplysninger om brugerrettigheder i [Sikkerheds- og rollestyring i Attract](./security-attract.md).

## <a name="feature-management"></a>Administration af funktioner

Når der tilføjes nye funktioner, kan de frigives i en offentlig prøveversion. Funktioner i offentlige prøveversioner opfylder ikke alle krav til en tjeneste. Når du modtager dem, accepterer du dele dine data med eksterne systemer. Det kan være, at din organisation ikke kræver alle de nye funktioner, der er frigivet. Du kan slå funktionerne i den offenlige prøveversion fra og til, afhængigt af organisationens behov.

## <a name="template-management"></a>Skabelonstyring

En processkabelon indeholder alle de aktiviteter, der skal medtages som en del af ansættelsesprocessen for et job. Din organisation kan give alle teammedlemmer eller kun administratorer adgang til at oprette ansættelsesskabeloner. For at give teammedlemmerne mulighed for at oprette deres egne ansættelsesprocesskabeloner skal du aktivere funktionen Skabelonstyring. Du kan finde flere oplysninger om processkabeloner i [Processkabeloner i Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>Mailskabelonindstillinger

Organisationer kan oprette mailskabeloner til forskellige scenarier. Du kan vælge det sidehovedbillede, der skal medtages i mailskabelonerne. Det valgte sidehoved vises derefter i alle mailskabeloner. I skabelonens sidefod kan du tilføje et link til din organisations erklæring om beskyttelse af personlige oplysninger og vilkår for anvendelse af kommunikation. Du kan finde flere oplysninger i [Mailskabeloner i Attract](./email-templates.md).

## <a name="offer-process"></a>Tilbudsproces

Du kan konfigurere godkendelsesprocessen for jobtilbud. For eksempel kan du angive, om et tilbud skal godkendes, før det sendes til en kandidat. Du kan også angive, at godkendere skal skrive en kommentar til deres tilbudsbeslutning.

Der findes to godkendelsesarbejdsgange: **Parallel** og **Sekventiel**.

- **Parallel** – Godkendelser sendes til alle godkendere på samme tid.
- **Sekventiel** - Godkendelser sende til godkenderne i en bestemt rækkefølge.

Du kan også konfigurere indstillinger, der er relateret til kandidatoplevelsen. F.eks. kan du med én indstilling angive, om kandidater kan afvise et tilbud uden yderligere diskussion. Hvis du vælger **Nej** i indstillingen **Tillad kandidater at afvise et tilbud uden yderligere forklaring**, er knappen **Afslå tilbud** for kandidaterne. Hvis du vælger **Ja** i denne indstilling, kan kandidaterne afslå tilbuddet ved at vælge en årsag og derefter vælge **Afslå tilbud**.

Du kan også angive og gennemtvinge en udløbsdato for tilbud. Hvis du vælger **Ja** i indstillingen **Kræv en udløbsdato for alle tilbud**, udløber tilbud efter det antal timer eller dage, du angiver.

Du kan finde flere oplysninger om tilbudsstyring i [Konfigurere tilbudsstyring](./offer-setup.md).
