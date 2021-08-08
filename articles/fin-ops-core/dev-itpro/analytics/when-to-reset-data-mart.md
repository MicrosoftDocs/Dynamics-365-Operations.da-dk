---
title: Ofte stillede spørgsmål om nulstilling af datacenter
description: Dette emne indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter.
author: jinniew
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 90abe1fc3e84e0a9777f3eabd790a4b7e9b509c5
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638261"
---
# <a name="data-mart-resets-faq"></a>Ofte stillede spørgsmål om nulstilling af datacenter

Dette emne indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter. En nulstilling af datacenteret kan være en tidskrævende proces, og afhængigt af omstændighederne er det muligvis ikke den løsning, der kræves. Dette emne indeholder derfor oplysninger om situationer, hvor nulstilling af et datacenter kan være en hjælp, og situationer, hvor det sandsynligvis ikke vil hjælpe.

## <a name="what-is-a-data-mart-reset"></a>Hvad er nulstilling af et datacenter?

Hvis du nulstiller et datacenter, deaktiveres integrationsopgaverne, alle dataene i datacenteret slettes, og integration aktiveres igen.

For at sikre, at gamle datacentre ikke indsættes, kan nulstilling af et datacenter først startes, når de eksisterende opgaver er fuldført. Hvis du forsøger at nulstille datacenteret, før alle opgaver er fuldført, får du muligvis vist en meddelelse som f.eks. "Nulstilling af datacenteret kunne ikke udføres på grund af en aktiv opgave. Prøv igen senere."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Hvornår skal jeg nulstille et datacenter?

Hvis en eller flere af følgende forhold gælder for din situation, kan din organisation med fordel nulstille et datacenter:

- Programdatabasen er gendannet.
- Du har åbnet en supportanmodning, og en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin.
 
> [!NOTE]
> Processen til nulstilling af et datacenter påvirkes af antallet af finans- og budgetposteringer i databasen. Afhængigt af antallet af posteringer i systemet kan en datanulstilling fuldføres på helt ned til 15 minutter, eller det kan tage op til fire timer. Hvis nulstillingen tager mere end fire timer, anbefales det dog, at du kontakter Support.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Hvornår skal et datacenter ikke nulstilles?

Her er nogle af de situationer, hvor vi ikke anbefaler, at du nulstiller datacenteret:

- Du oplever forskellige ydeevneproblemer, der er forbundet med datasynkronisering.
- Du har et tilbagevendende nulstillingsmønster af en af følgende årsager:

    - **Manglende data** – Hvis du bemærker, at der mangler data, skal du åbne en supportanmodning hos Microsoft for at gennemse rapportformatet og eventuelle problemer med datasynkronisering.
    - **Låst integrationstilstand**
    - **Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret. Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg nulstiller datacenteret, mister jeg så rapporter, som jeg allerede har udarbejdet?

Nr. Dine rapporter gemmes i SQL-tabeller, der ikke påvirkes af, at dataene nulstilles. Hvis du er bange for at miste rapporter, som du har oprettet, kan du sikkerhedskopiere de design, du ikke ønsker at miste. Du kan sikkerhedskopier design ved at åbne Report Designer og gå til **Firma \> Firmaer \> Komponenter \> Eksportér**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Skal alle brugere forlade systemet, før jeg kan nulstille datacenteret?

Nr. Brugere kan fortsætte med at arbejde i systemet, mens et datacenter nulstilles. Brugere vil dog ikke kunne få adgang til rapporter, der er oprettet ved hjælp af Financial Reporter, før nulstillingen er fuldført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
