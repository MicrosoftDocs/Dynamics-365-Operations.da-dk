---
title: Slå jobs op på eksterne karrierewebsteder via Attract
description: Dette emne beskriver, hvordan du anvender Dynamics 365 for Talent - Attract til at slå jobs op på eksterne rekrutteringswebsteder
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/15/2019
ms.locfileid: "993662"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Slå jobs op på eksterne karrierewebsteder via Attract

[!include [banner](../includes/banner.md)]

Du vil gerne have, at dine ledige stillinger ses af så mange kvalificerede kandidater som muligt. Rekrutteringswebsteder såsom Broadbean kan hjælpe dig med at nå dette mål. Microsoft Dynamics 365 Talent: Attract giver dig nu mulighed for at slå jobs op på Broadbean, og Microsoft stiller konstant nye tilbud til rådighed på dette område.

## <a name="post-jobs-to-broadbean"></a>Slå jobs op på Broadbean

Du skal konfigurere integrationen af Broadbean, før du kan slå jobs op på Broadbean.

> [!NOTE]
> - For at slå jobs op på eksterne websteder skal du have [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Denne funktion findes på nuværende tidspunkt i prøveversionen. Hvis du ønsker at prøve det, skal du [slå det til i administratorindstillingerne i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Konfigurer integrationen af Broadbean

1. Log på Attract som administrator.
2. Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Administration**.
3. På fanen **Indstillinger for jobportal** i afsnittet **Aktiver integration af Broadbean** skal du slå integrationen til.
4. Kontakt Broadbean, og indtast dine oplysninger under **Brugernavn, Klient-id, Krypteringstoken**.

> [!WARNING]
> Dine legitimationsoplysninger til Broadbean er følsomme og fortrolige. Opbevar og del dem derfor ansvarligt. Alle med en administratorrolle i Attract kan se disse legitimationsoplysninger.

> [!NOTE]
> Microsoft og Attract er ikke involveret i dannelsen og vedligeholdelsen af disse værdier. Det er dit ansvar at ajourføre dem i Attract og arbejde sammen med Broadbean om at løse alle problemer vedrørende dine legitimationsoplysninger.

### <a name="post-a-job-to-broadbean"></a>Slå et job op på Broadbean

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
2. I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Se**.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Fejlfinding i Broadbean-integrationen

Hvis du har problemer med at slå et job op på Broadbean, kan du prøve disse trin:

1. Kontroller, at de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte.
2. Hvis de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte, skal du kontakte [Broadbean-support](https://www.broadbean.com/resources/support/).
3. Hvis problemet fortsætter, skal du kontakte [Microsoft-support](./talent-support.md).
