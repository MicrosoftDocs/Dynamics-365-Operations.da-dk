---
title: Spore ændringer i rekrutteringsdata
description: Ved at bruge funktionen til procesovervågning kan du spore, hvornår kandidater, jobmuligheder eller jobansøgninger ændres i forbindelse med rapportering eller overholdelse.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460728"
---
# <a name="track-changes-in-recruiting-data"></a>Spore ændringer i rekrutteringsdata

[!include [banner](includes/banner.md)]

Du kan spore ændringer, der er foretaget af kandidater, jobmuligheder eller jobansøgninger ved hjælp af overvågning. Dette er nyttigt i forbindelse med rapportering eller overholdelse.

Du kan få vist de sporede data i Power BI ved hjælp af OData-forbindelseskomponenten. Du kan finde flere oplysninger i [Oprette forbindelse til OData-feeds i Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Spor ændringer
Benyt følgende fremgangsmåde til at konfigurere sporing af ændringer i rekrutteringsdata:

1. Vælg det relevante miljø i [Power Apps](https://web.powerapps.com).

2. Vælg **Indstillinger** (tandhjulsikonet), vælg **Avancerede tilpasninger**, og vælg derefter **Ressourcer** under **Udviklerressourcer**. 

3. Kopier værdien i feltet **Værdi af web-API for forekomst** på siden **Udviklerressourcer**. Værdien kan f.eks. se ud sådan ud: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Du kan derefter forespørge på dataene fra et af følgende objekter:
  - Historik for jobmulighed (msdyn_jobopeninghistories)
  - Historik for jobansøgninger (msdyn_jobapplicationhistories) 
  - Kandidathistorik (msdyn_candidatehistories)

## <a name="data-reported"></a>Rapporterede data

Følgende data er tilgængelige med procesovervågning.

| Rapporterede data | Beskrivelse |
| --- | --- |
| Ændret af (msdyn_ChangedbyId) | Reference til bruger |
| Oprettet den (createdon) |  Dato og klokkeslæt i UTC, da ændringen blev foretaget |
| Ændringstype (msdyn_changetype) | Hvilken ændring der blev foretaget |
| Fælles værdier for ansøgere, jobmuligheder <br></br>og jobansøgninger | Oprettet den<br></br>Opdateret |
| Historik for jobansøgning | Artefakt tilføjet <br></br>Artefakt fjernet |
| Historik over jobmuligheder | OPGAVE: Opslag tilføjet <br></br>OPGAVE: Opslag fjernet <br></br>OPGAVE: Opslag opdateret <br></br>OPGAVE: Deltager tilføjet <br></br>OPGAVE: Deltager fjernet |
| Kandidathistorik | Artefakt tilføjet <br></br>Artefakt fjernet <br></br>Arbejdserfaring tilføjet <br></br>Arbejdserfaring fjernet <br></br>Uddannelse tilføjet <br></br>Uddannelse fjernet <br></br>Færdighed tilføjet <br></br>Færdighed fjernet <br></br>Mærkat tilføjet <br></br>Mærkat fjernet <br></br>Socialt netværk tilføjet <br></br>Socialt netværk fjernet <br></br>Personoplysninger tilføjet <br></br>Personoplysninger opdateret<br></br> |
| Ændrede felter (msdyn_changedfields) | Ændrede felter for JSON-objektvisning. Kan muligvis ikke indeholde værdier for alle felter.<br></br><br></br>Ved "oprettede" og "opdaterede" ændringer vises felterne i den oprettede eller ændrede post.<br></br><br></br>For "tilføjede" ændringstyper vises de pågældende felter i den underordnede post.<br></br><br></br>**Eksempel:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Historik for jobansøgning | Jobansøgning (msdyn_JobapplicatonId)<br></br>Status (msdyn_status) <br></br>Statusårsag (msdyn_statusreason) <br></br>Årsag til afvisning (msdyn_rejectionreason) |
| Historik over jobmuligheder | Jobmulighed (msdyn_JobopeningId) <br></br>Status (msdyn_jobopeningstatus) <br></br>Statusårsag (msdyn_jobopeningstatusreason) |
| Kandidathistorik | Kandidat (msdyn_CandidateId) |


[!INCLUDE[footer-include](../includes/footer-banner.md)]