---
title: Nyheder eller ændringer i Dynamics 365 Talent (21. januar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528116"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Nyheder eller ændringer i Dynamics 365 Talent (21. januar 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract. Vi har tilføjet funktionalitet i Attract for at under støtte vores nylige meddelelse [Opbygning af en mere succesfuld arbejdsstyrke med Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Downloade miljødata

Administratorer kan downloade data fra deres miljø. Dataene eksporteres i JSON-standardformat med alle job, kandidater og konfigurationer, der er eksporteret i en zip-fil. Du kan finde flere oplysninger under [Eksportere data fra Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Begrænse adgangen til miljøer for brugere, der ikke er administratorer

Administratorer kan nu begrænse adgangen til miljøet for brugere, der ikke er administratorer. Denne handling kan ikke fortrydes. Du kan finde flere oplysninger under [Begrænse adgangen til Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Eksportere onboardingguider

Brugerne kan nu eksportere alle deres onboardingguider og onboardingskabeloner i Word-dokumentformat. Du kan finde flere oplysninger under [Eksportere data fra Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2726. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Det seneste årlige kompensationsfelt i kontrolansættelsesformen er ikke konsistent (392092)

Denne version indeholder en ændring, der konsekvent vil vise den seneste valuta baseret på firmavælgeren i formularen **Kontrollér ansættelse**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Feltet Kendt som er føjet til modtageropslaget for feedback (407789)

Når der gives feedback om ydeevnen, gav opslag for arbejdere ikke tilstrækkeligt med oplysninger til at afgøre, om feedback gik til den korrekte person. Vi har tilføjet en **Kendt som**-kolonne for at hjælpe med at identificere medarbejderens entydige navn.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo-posten oprettes uden en tilknytning til en arbejder (394526)

Denne frigivelse omfatter en ændring, der ikke skriver HCMWorkerPayrollInfo-poster uden at referere til en medarbejder.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Afdeling kan redigeres, når der navigeres fra stillingshierarki (341001)

Når sikkerheden er konfigureret til at nægte adgang til redigering af afdelinger, deaktiveres redigering, når der navigeres til formen **Afdelinger** i alle scenarier.

## <a name="coming-soon"></a>Kommer snart

Der vil snart være en ny Common Data Service-løsning med følgende ændringer:

| Beskrivelse | Forskydning |
| --- | --- |
| Ændringer i objektet **Job/Stilling** | <ul><li>**Kompensationsområde** er tilføjet</li><li>**Økonomiske dimensioner** er tilføjet</li></ul> |
| Ændringer i objektet **Arbejder** | <ul><li>**Navnerækkefølge** er tilføjet</li><li>**Arbejder hjemmefra** er tilføjet</li><li>**Sprog** er tilføjet</li><li>**Anciennitetsdato** er tilføjet</li><li>**Jubilæumsdato** er tilføjet</li><li>**Oprindelig ansættelsesdato** er tilføjet</li></ul> |
| Ændringer af objektet **Ansættelse** | <ul><li>**Økonomiske dimensioner** er tilføjet</li><li>**Årsag til fratrædelse** er tilføjet</li><li>**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</li><li>**Datoer for prøvetid** er tilføjet</li></ul> |
| Ændringer i objektet **Arbejders adresse** | <ul><li>**Gadenavn** er tilføjet</li><li>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning</li></ul> |
| Nye konfigurationsobjekter til variabel kompensation | <ul><li>**Type af variabel kompensationsplan**</li><li>**Kompensation - variabel struktur**</li><li>**Fordelingsregler**</li><li>**Niveau i variabel kompensationsplan**</li></ul> |
| Nyt objekt **Arbejderkalender for ansættelse** | <ul><li>**Arbejdskalenderobjekt** er tilføjet</li></ul> |
