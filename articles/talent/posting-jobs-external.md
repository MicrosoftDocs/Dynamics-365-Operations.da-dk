---
title: Slå job op på eksterne karrierewebsteder fra Attract
description: Dette emne beskriver, hvordan du anvender Dynamics 365 Talent - til at slå job op på eksterne rekrutteringswebsteder
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 919cec773d5e57e8f5429e31872db7ed658e969b
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008076"
---
# <a name="post-jobs-to-broadbean"></a>Slå jobs op på Broadbean

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract hjælper dig med at få det talent, du har brug for, ved at lade dig foretage jobopslag direkte fra Attract til Broadbean. Når du har [oprettet et job](./creating-jobs-attract.md), skal du bare klikke på en knap for at placere dit job for øjnene af alle potentielle jobkandidater på Broadbean.

Jobopslag til Broadbean kræver en relevant Broadbean-licens. Broadbean tilbyder forskellige produkter og planer. Du kan få mere information om Broadbean-licens og -priser ved at [kontakte Broadbean](https://www.broadbean.com/contact-us/).

Hvis du er en administrator, der har brug for mere information om, hvordan du konfigurerer Broadbean-integration med Attract, kan du se [Angive indstillinger for eksterne jobportaler](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Slå jobs op på Broadbean

Når du har slået Broadbean til, kan rekrutteringsmedarbejdere og administratorer slå et job op på webstedet. Du skal have an URL-adresse til jobrelaterede ansøgninger.

1. I Attract skal du åbne det job, du ønsker at slå op på Broadbean.
2. I afsnittet **Opslag** skal du vælge den knap for **Slå op nu**, der svarer til Broadbean.
3. Følg vejledningen i Broadbean-vinduet.

Attract videregiver følgende oplysninger til Broadbean:

- Anmodnings-id
- Stillingsbetegnelse
- Jobbeskrivelse
- Jobsted
- URL-adressen til ansøgningen
- Oplysninger om rekrutteringsansvarlig

Efter Broadbean har fuldført opslaget, fremgår det af afsnittet **Opslag** under jobbet i Attract, at Broadbean-statussen er angivet til **Opslået**.

> [!NOTE]
> - Broadbean kræver feltet **Industri**. Dette felt er på nuværende tidspunkt angivet til **IT** som standard. Du kan dog ændre værdien til den rette industri i vinduet for jobopslag på Broadbean.
> - Det tager lidt tid, før Broadbean har slået dit job op på alle de valgte jobportaler. Der kan derfor være en mindre forsinkelse, før Attract viser en statusopdatering for jobbet.

### <a name="view-a-broadbean-job-posting"></a>Se et jobopslag på Broadbean

Når du har slået et job op på Broadbean, kan du se det i Attract.

1. I Attract skal du åbne det job, du ønsker at se på Broadbean.
2. Under fanen **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Vis**.

Jobopslaget på Broadbean vises i et nyt vindue.

### <a name="update-a-broadbean-job-posting"></a>Opdater et jobopslag på Broadbean

Du kan opdatere et jobopslag på Broadbean på to måder:

1. I Attract skal du åbne det job, du ønsker at opdatere.
2. I afsnittet **Opslag** skal du vælge den knap for **Opdater opslag**, der svarer til Broadbean.
3. Rediger opslaget i Broadbean-vinduet.

eller

1. I Attract skal du åbne det job, du ønsker at se på Broadbean.
2. I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Se**.
3. I Broadbean-vinduet skal du redigere jobdetaljerne og dernæst slå jobbet op på ny. Jobdetaljerne i Attract ændres ikke.

### <a name="remove-a-broadbean-job-posting"></a>Fjern et jobopslag fra Broadbean

Du kan fjerne et jobopslag fra Broadbean efter behov.

1. I Attract skal du åbne det job, du ønsker at fjerne.
2. I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Fjern opslag**.

Når Broadbean har fjernet jobbet, får Broadbean-elementet i Attract en **Slå op nu**-knap. Fremkomsten af denne knap indikerer, at jobbet er blevet fjernet og kan slås op på ny.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Fejlfinding af jobopslag til Broadbean

Hvis du har problemer med at slå et job op på Broadbean, kan du prøve disse trin:

1. Kontroller, at de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte.
2. Hvis de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte, skal du kontakte [Broadbean-support](https://www.broadbean.com/resources/support/).
3. Hvis problemet fortsætter, skal du kontakte [Microsoft-support](./talent-support.md).

## <a name="see-also"></a>Se også

[Oprette job](./creating-jobs-attract.md)

[Angive indstillinger for eksterne jobportaler](./attract-admin-job-board-settings.md)
