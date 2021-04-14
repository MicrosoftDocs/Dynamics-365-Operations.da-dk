---
title: Hvornår et datacenter skal nulstilles
description: I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, og forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754138"
---
# <a name="when-to-reset-a-data-mart"></a>Hvornår et datacenter skal nulstilles

Nulstilling af et datacenter kan være tidskrævende. Afhængigt af forholdene er denne handling muligvis ikke den løsning, der er brug for. I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, samt forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Hvornår skal du nulstille et datacenter?
Overvej følgende spørgsmål, før du nulstiller et datacenter. Hvis du svarer ja til et eller flere spørgsmål, kan det være en fordel for din organisation at nulstille datacenteret.

- Applikationsdatabasen blev gendannet, men databasen for datacenteret blev ikke gendannet.
- Du kan se forkerte data i en regnskabsperiode, hvilket ikke er resultatet af en fejl i rapportdesignet.
- Du kan se forkerte data for en regnskabsperiode, og poster vises under Integrationsforsøg på siden **Integrationsstatus** i Rapportdesigner (start Rapportdesigneren, og vælg **Værktøjer > Integrationsstatus**).
- Du har åbnet en supporthændelse, og en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Hvornår er det ikke relevant at nulstille et datacenter?
Der er nogle forhold, hvor vi ikke anbefaler, at du nulstiller et datacenter. Blandt andet: 

- Når årsagen ikke er angivet i dette emne.
- Du oplever ydeevneproblemer forbundet med datasynkronisering. I dette tilfælde hjælper det sandsynligvis ikke at nulstille datacenter.
- Hvis oplever har et tilbagevendende nulstillingsmønster af en af følgende årsager: 
  - **Manglende data** – Du skal først eliminere fejl i rapportdesignet og fejl i tidsindstillingen for datasynkronisering. Du bemærker f.eks., at faktaoversigten ikke har kørt, siden de manglende data blev bogført.
  - **Låst integrationstilstand** – Hvis integrationen er langsom eller virker låst, kan du ikke løse fejlen ved at nulstille datacenteret.
  - **Forsøg på nulstilling mislykkedes** – Hvis der er foretaget et antal forsøg på at fuldføre en nulstilling, og dette mislykkedes på grund af manglende data, anbefales det, at du åbner en supporthændelse og samarbejder med en supporttekniker for at analysere din situation, inden du forsøger at nulstille datacenteret igen.
  - **Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret. Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Hvad en nulstilling af datacenteret ikke gør  
- En nulstilling starter kun, når eksisterende opgaver er fuldført. Derved sikres, at gamle data ikke indsættes. På dette tidspunkt vil du muligvis få vist en meddelelse som f.eks. "Nulstillingen af datacenteret kunne ikke behandles på grund af en aktiv opgave. Prøv igen senere."
- Nulstillingen deaktiverer integrationsopgaverne og sletter alle data i datacenteret. Integrationen er aktiveret igen.

> [!NOTE]
> Følgende punkter angiver to ting, som en nulstilling af et datacenter *ikke* vil gøre. <br>
> - Nulstillinger fjerner ikke rapportdesign. <br>
> - Nulstillinger rydder ikke firma- eller brugerdata, medmindre disse er valgt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]