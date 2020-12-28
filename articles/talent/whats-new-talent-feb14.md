---
title: Nyheder eller ændringer i Dynamics 365 Talent (14. februar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460696"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (14. februar 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Der indgår mindre fejlrettelser i denne version.

## <a name="changes-in-onboarding"></a>Ændringer i Onboarding
Der indgår mindre fejlrettelser i denne version.
 
## <a name="changes-in-core-hr"></a>Ændringer i Core HR 
**Build 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Enheden Fast løn til medarbejder eksportere ikke alle poster
Med denne ændring eksporterer enheden **Fast løn til medarbejder** nu alle poster. Enheden kan bruges til at oprette og opdatere eksisterende faste lønposter for medarbejdere. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Slutdatoen for ansættelsen bruger ikke indstillinger for medarbejders foretrukken tidszone
Slutdato for ansættelser bruger nu den tidszone, brugeren foretrækker til at oprette eller afslutte ansættelse i et firma.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Britiske adresser vises i Analyser som adresser i den østlige del af Schweiz
Der er foretaget en ændring i denne version for at rette fejljustering i adresser i **Personalestyring** "antal beskæftigede pr. lokalitet"-rapporten.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Fratrædelseskode udfyldes ikke i posten for tildeling af arbejderstilling, når stillingen afsluttes
Der er foretaget en ændring for at anvende standardkoden for "Årsag til fratrædelse", når medarbejderens stillingstildeling afsluttes.

### <a name="new-entity-created-for-job-compensation-levels"></a>Ny enhed, der er oprettet for jobkompensationsniveauer
Et nyt datastyringsobjekt (DMF) er blevet oprettet. Objektet bruges til oprettelse og opdatering til kompensationsniveauer, markedsværdier og undersøgelsesoplysninger for hvert job, der er defineret i systemet.
