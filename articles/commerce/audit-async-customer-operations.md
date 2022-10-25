---
title: Overvåge synkronisering af kundeoperationer i headquarters
description: Denne artikel forklarer, hvordan du kan overvåge synkroniseringen af kundehandlinger i Microsoft Dynamics 365 Commerce headquarters for at løse eventuelle problemer for webstedets brugere.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691063"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Overvåge synkronisering af kundeoperationer i headquarters

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel forklarer, hvordan du kan overvåge synkroniseringen af kundehandlinger i Microsoft Dynamics 365 Commerce headquarters for at løse eventuelle problemer for webstedets brugere.

Når organisationer begynder at indføre muligheden for at oprette og redigere kunder asynkront, har webstedsadministratorer brug for at kunne se og udføre fejlfinding baseret på brugeranmodninger eller procesfejl på webstedet. I disse scenarier skal webstedsadministratorer kunne overvåge oprettelse og redigering af kunder og rette eventuelle fejl ved hjælp af en selvbetjeningsmodel.

## <a name="customer-synchronization-status"></a>Status af kundesynkronisering

Når du tilmelder asynkron tilstand af kundestyring og de tilhørende funktioner, skal administratorer af Commerce headquarters oprette og planlægge et tilbagevendende batchjob til **P-job**, jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** og **1010**-jobbet, så alle asynkrone kunder konverteres til synkrone kunder i Commerce headquarters. Synkroniseringen af kundestyringsoperationer finder sted, når disse job køres. Yderligere oplysninger finder du i [Asynkron oprettelsestilstand for kunde](async-customer-mode.md).

Som virksomhedsejer kan du udføre følgende handlinger:

- Se alle oprettelses-/redigeringsoperationer for webstedsbrugere. Detaljerne omfatter status og et tidsstempel.
- Filtrere operationer ved at bruge et eller flere af kundetabelfelterne og -værdierne til at indsnævre overvågningsloggen.
- Se korte beskrivelser af ændringer sammen med statusdetaljer for at forstå operationer på et højt niveau.
- I forbindelse med fejl skal du redigere og rette problematiske felter og derefter gemme og synkronisere specifikke kundehandlinger.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Elementer på siden Status af kundesynkronisering

Hvis du vil se en liste over alle synkroniseringshandlinger, skal du gå til **Retail og Commerce \> Kunder \> Status af kundesynkronisering** i Commerce headquarters. I følgende illustration vises et eksempel på siden med **Status af kundesynkronisering**.

![Siden Status af kundesynkronisering i Commerce headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Listen over kundesynkroniseringshandlinger til venstre på siden **Status af kundesynkronisering** indeholder som standard følgende kolonner:

- Kanalnavn
- Debitorkonto
- Asynkron kundekonto
- Tidsstempel for handling
- Status af kundesynkronisering

Øverst til højre på siden vises kundekontooplysninger som f.eks. **Debitorkonto**, **Retail Async-handling**, **Status af kundesynkronisering** og **Seneste kendte fejl**.

Afsnittet **Ændringsbeskrivelse** indeholder en beskrivelse af den type operation i kundestyring, der kørte (f.eks. kundeoprettelse, kontoopdatering eller synkroniseringsfejl med detaljer).

Sektionen **Kundeattributter** indeholder et gitter, der viser alle kundeattributter sammen med gamle og nye værdier. Du kan redigere dette afsnit, hvis du vil ændre kundeattributværdierne for at rette fejl og derefter synkronisere igen.
