---
title: Ofte stillede spørgsmål om nulstilling af datacenter
description: Denne artikel indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.search.form: ''
ms.openlocfilehash: 949bf64fefe2dc70541eb5a94518d6b9fe1d3eb8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289870"
---
# <a name="data-mart-resets-faq"></a>Ofte stillede spørgsmål om nulstilling af datacenter

Denne artikel indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter. En nulstilling af datacenteret kan være en tidskrævende proces, og afhængigt af omstændighederne er det muligvis ikke den løsning, der kræves. Denne artikel indeholder derfor oplysninger om situationer, hvor nulstilling af et datacenter kan være en hjælp, og situationer, hvor det sandsynligvis ikke vil hjælpe.

## <a name="what-is-a-data-mart-reset"></a>Hvad er nulstilling af et datacenter?

Hvis du nulstiller et datacenter, deaktiveres integrationsopgaverne, alle dataene i datacenteret slettes, og integration aktiveres igen.

For at sikre, at gamle datacentre ikke indsættes, kan nulstilling af et datacenter først startes, når de eksisterende opgaver er fuldført. Hvis du forsøger at nulstille datacenteret, før alle opgaver er fuldført, får du muligvis vist en meddelelse som f.eks. "Nulstilling af datacenteret kunne ikke udføres på grund af en aktiv opgave. Prøv igen senere."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Hvornår skal jeg nulstille et datacenter?

Hvis en eller flere af følgende forhold gælder for din situation, kan din organisation med fordel nulstille et datacenter:

- **Programdatabasen blev gendannet**
- **Du har åbnet en supportanmodning** – En supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin.
- **Stor procentdel af gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret. Store procentdele af gamle data kan forringe den generelle generering og integrationsydeevne for rapporter, og det medfører ekstra brug af databaseplads. Det anbefales, at du fuldfører en nulstilling af datamart for at fjerne de gamle data, når der er mere end 80 % gamle data i datasættet.
 
> [!NOTE]
> Processen til nulstilling af et datacenter påvirkes af antallet af finans- og budgetposteringer i databasen. Afhængigt af antallet af posteringer i systemet kan en datanulstilling fuldføres på helt ned til 15 minutter, eller det kan tage op til fire timer. Hvis nulstillingen tager mere end fire timer, anbefales det dog, at du kontakter Support.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Hvornår skal et datacenter ikke nulstilles?

Her er nogle af de situationer, hvor vi ikke anbefaler, at du nulstiller datacenteret:

- Du har problemer med ydeevnen af dataintegration.
- Din integration af Financial Reporter er ikke aktiveret. 

    - Det betyder, at finansdata ikke længere synkroniseres til dit Financial Reporting-datacenter. Din Financial Reporter indeholder muligvis ikke opdaterede tal til dine regnskabsrapporter. Dette sker typisk, hvis du ikke har brugt Financial Reporter i lang tid.
    - Du bliver bedt om at aktivere integration ved at nulstille datacenteret. Du kan fortsætte ved at vælge **Ja**. Du kan også vælge at nulstille datacenteret på et senere tidspunkt. Når integrationen er aktiveret, synkroniseres dine finansdata igen i Financial Reporter. 
- Du har et tilbagevendende nulstillingsmønster af en af følgende årsager:

    - **Manglende eller uventede data i rapporten** – Hvis du bemærker, at der mangler data, skal du åbne en supportanmodning hos Microsoft for at gennemse rapportformatet og eventuelle problemer med datasynkronisering.
    - **Låst integrationstilstand** – Hvis du bemærker, at integrationsstatussen ikke kører, kan det skyldes en stor mængde transaktioner i systemet. Denne tilstand løser sig selv. Hvis du bemærker, at intregrationsstatussen er låst i mere end fire timer, skal du åbne en supportanmodning hos Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg nulstiller datacenteret, mister jeg så rapporter, som jeg allerede har udarbejdet?

Nej Dine rapporter gemmes i SQL-tabeller, der ikke påvirkes af, at dataene nulstilles. Hvis du er bange for at miste rapporter, som du har oprettet, kan du sikkerhedskopiere de design, du ikke ønsker at miste. Du kan sikkerhedskopier design ved at åbne Report Designer og gå til **Firma \> Firmaer \> Komponenter \> Eksportér**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Skal alle brugere forlade systemet, før jeg kan nulstille datacenteret?

Nej Brugere kan fortsætte med at arbejde i systemet, mens et datacenter nulstilles. Brugere vil dog ikke kunne få adgang til rapporter, der er oprettet ved hjælp af Financial Reporter, før nulstillingen er fuldført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
