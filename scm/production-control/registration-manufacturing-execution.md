---
title: "Registrering for produktionsudførelse"
description: "Dette emne beskriver vigtige begreber og udtryk, som du skal kunne forstå for at konfigurere og bruge produktionsudførelse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 81332eed9cf3745442007f98d36bc56e7095d9f8
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="registration-for-manufacturing-execution"></a>Registrering for produktionsudførelse

[!include[banner](../includes/banner.md)]


Dette emne beskriver vigtige begreber og udtryk, som du skal kunne forstå for at konfigurere og bruge produktionsudførelse. 

Produktionsudførelse er primært beregnet til brug i produktionsfirmaer. Arbejderne kan registrere tids- og vareforbrug på produktionsjob på siden **Jobregistrering**. Alle registreringer godkendes og overføres senere til de relevante moduler. Fortløbende godkendelse og overførsel af registreringer giver lederne mulighed for let at spore faktiske omkostninger på produktionsordrer.

## <a name="manufacturing-execution-and-registration-terminology"></a>Produktionsudførelse og registreringsterminologi
Følgende tabel indeholder udtryk, der vedrører produktionsudførelse og relaterede registreringsopgaver.

| Periode                          | Betegnelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Produktionsudførelse       | En funktion, der bruges til at registrere tid, materialeforbrug, omkostninger på produktionsjob, projekter og indirekte aktiviteter. Registrering foretages i en registreringsklient til produktionsudførelse.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Joboversigt                      | På siden **Jobregistrering** kan arbejderne se en liste over job, som de skal udføre på en specifik ressource som f.eks. en maskine. Arbejderne kan registrere tids- og vareforbrug for hvert job eller hver opgave i joboversigten.                                                                                                                                                                                                                                                                                                                                                                           |
| Job i bundter                  | Hvis en arbejder starter mere end ét job samtidig på siden **Jobregistrering**, kaldes det job i bundter. Den tid, der er blevet brugt på job i bundter, kan fordeles på de enkelte job på forskellige måder ved hjælp af fordelingsnøgler.                                                                                                                                                                                                                                                                                                                                                         |
| Pilot-/assistentregistreringer | En arbejder kan registrere sig som assistent på en ressource og kan oprette et lille team, hvor flere arbejdere deltager i de samme produktionsjob. De ressourcer, som arbejderne er tilknyttet som assistenter, kaldes piloter. Den foreløbige ressource skal foretage registreringer. Alle assistenter får automatisk samme registreringer. Hvis en maskine f.eks. fungerer som pilot, kan en arbejder, der er registreret som assistent på denne maskine, foretage registreringer på siden **Jobregistrering**, så både maskinen og de arbejdere, der er tilknyttet som assistenter, får de samme registreringer. |
| Indirekte aktivitet             | En aktivitet eller opgave, der ikke direkte vedrører et produktionsjob eller et projekt, f.eks. et afdelingsmøde, et rengøringsjob eller et vedligeholdelsesjob i produktionshallen. Arbejderne kan foretage registreringer af indirekte aktiviteter på samme måde, som de kan registrere produktionsjob og projekter.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Registreringer i produktionsudførelse
Arbejderne kan foretage forskellige former for registreringer i produktionsudførelse for arbejde, der er udført på produktionsjob. Afhængig af systemopsætningen kan arbejdere eventuelt også foretage registreringer på projektaktiviteter og ikke-produktive opgaver som f.eks. pauser, fravær og indirekte aktiviteter. Her er registreringstyperne:

-   **Komme og gå** (tilgængelig til tid og fremmøde) – medarbejdere stempler ind, når de kommer, og stempler ud, når de går hjem.
-   **Registrere på produktionsjob** – Arbejdere kan foretage registreringer, som f.eks. start af et job og rapporteringstilbagemelding for et job, i produktionsjob, der vises i joboversigten. Arbejdere kan starte flere job samtidig. Det betegnes samling af job i bundter.
-   **Registrere på lager** – Arbejdere kan foretage registreringer af materialer, der bruges i produktionshallen, men som ikke er direkte relateret til produktionsjob. Det kan f.eks. være smørelse, olier og andre materialer, der bruges til at holde gang i maskineriet. Registrering foretages i en lagerkladde.
-   **Registrere på projekter** (tilgængelig til tid og fremmøde) – Arbejdere kan foretage registreringer, som start og afslutning af arbejde på projekter eller projektaktiviteter, der vises i deres jobliste.
-   **Registrer projektgebyrer og projektvarer** (tilgængelig til tid og fremmøde) – Arbejdere kan registrere gebyrer (udgifter), der er tilknyttet et projekt i en projektgebyrkladde, f.eks kilometertal og broafgift. Arbejdere kan også registrere vareforbrug på projekter. Dette afsluttes i en projektvarekladde.
-   **Registrere som assistent for en anden arbejder** – Hvis to eller flere arbejdere skal samarbejde om et produktionsjob eller projekt, kan en arbejder registrere sig som assistent på en maskine eller til en anden arbejder, der derefter fungerer som pilot. Hvis det er nødvendigt, kan piloten vælge en anden arbejder som pilot.
-   **Registrere fravær** (tilgængelig til tid og fremmøde) – Arbejdere kan registrere tid på forskellige fraværskoder, der er oprettet. Det er muligt at angive fravær, hvis en arbejder møder for sent, er nødt til at være fraværende i dagens løb eller går tidligere end angivet i den normale arbejdstidsprofil.
-   **Registrere pauser** (tilgængelig til tid og fremmøde) – I løbet af arbejdsdagen kan arbejdere registrere, at de forlader deres arbejdsstation for at tage en pause. Der kan oprettes flere pausetyper. Når en arbejder vender tilbage og logger på igen, registrerer systemet, at arbejderen er tilbage, og pauseregistreringen ophører.
-   **Registrere indirekte aktiviteter** (tilgængelig til tid og fremmøde) – Indirekte aktiviteter er ikke-produktive aktiviteter, som arbejdere kan være beskæftiget med i dagens løb. Det kan f.eks. være et afdelingsmøde, et gruppemøde eller et vedligeholdelsesjob i produktionshallen. Arbejderne kan foretage registreringer af indirekte aktiviteter, der er konfigureret.
-   **Registrere overtid** (tilgængelig til tid og fremmøde) – Arbejdere, der er blevet bedt om at arbejde længere, kan vælge, om de vil registrere de ekstra timer som flekstid eller overtid.





