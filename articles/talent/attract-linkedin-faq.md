---
title: Ofte stillede spørgsmål om integration af LinkedIn
description: Dette emne besvarer spørgsmål, du måtte have om integration mellem LinkedIn og Microsoft Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460655"
---
# <a name="linkedin-integration-faq"></a>Ofte stillede spørgsmål om integration af LinkedIn

[!include [banner](includes/banner.md)]

LinkedIn er verdens største faglige professionelle onlinenetværk. Microsoft Dynamics Talent: Attract kan integreres med LinkedIn for at give dig adgang til verdens største talenter. Attract giver dig mulighed for at slå job direkte op på LinkedIn, og det giver dig også mulighed for at trække kandidatoplysninger fra LinkedIn til Attract.

## <a name="for-recruiters-and-hiring-managers"></a>For rekrutteringsmedarbejdere og ansættelsesansvarlige

Her er svar på ofte stillede spørgsmål om, hvordan man bruger Attract og LinkedIn sammen.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Hvilke LinkedIn-funktioner får jeg med Attract?

Attracts integration med LinkedIn giver dig mulighed for at udføre følgende opgaver:

- [Slå job op på LinkedIn](./attract-post-jobs-to-linkedin.md) (som gratis begrænsede jobopslag).
- [Rekrutter kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Konfigurer integration med LinkedIn til Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Hvad har jeg brug for, før jeg kan slå job op på LinkedIn?

Din administrator skal [konfigurere LinkedIn-integration i Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Derefter er du klar til at gå i gang.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Hvordan slår jeg job op på LinkedIn fra Attract?

Når du har oprettet et job i Attract, skal du bare vælge **Slå op nu**-knappen, der svarer til LinkedIn. For mere information, se [Slå job op på LinkedIn fra Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Kan jeg få kandidatoplysninger fra LinkedIn i Attract?

Ja. Hvis du ser en egnet kandidat på LinkedIn, kan du nemt eksportere kandidatens oplysninger til Attract. Du kan finde flere oplysninger i [Rekrutter kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Hvordan kan jeg få hjælp til at få adgang til LinkedIn fra Attract?

Hvis du har problemer med at logge på eller slå job op på LinkedIn fra Attract, kan du finde hjælp i [Fejlfinding af integration med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

Oplever du andre problemer med Attract, skal du se [Få support til Microsoft Dynamics 365 Talent](./talent-support.md). For hjælp med LinkedIn skal du se [LinkedIn-supportsiden](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Til administratorer og udviklere

Her er svar på ofte stillede spørgsmål om, hvordan man konfigurerer integration mellem Attract og LinkedIn.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Hvordan konfigurerer jeg Attract, så rekrutteringsmedarbejdere og ansættelsesansvarlige kan slå job op på LinkedIn?

Du kan konfigurere de tilgængelige muligheder under fanen **LinkedIn-integration** i Administration. Du kan finde flere oplysninger i [Konfigurer integration med LinkedIn til Microsoft Dynamics 365 Talent -Attract](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Kan jeg eksportere kandidatoplysninger fra LinkedIn?

Ja, men du skal først konfigurere integration med LinkedIn Recruiter. Du kan finde flere oplysninger i [Konfigurer integration med LinkedIn til Microsoft Dynamics 365 Talent -Attract](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Hvordan kan jeg slå job op på Premium Job Slots på LinkedIn?

Selvom Attract leverer en kraftfuld løsning til jobopslag på LinkedIn, kan du opleve, at du har brug for yderligere fleksibilitet. For eksempel vil du måske gerne kunne slå Premium Job Slots op udover de gratis begrænsede opslag, eller du vil måske have, at LinkedIn skal behandle dine batchjobopslag mere end én gang om dagen.

#### <a name="types-of-linkedin-job-posts"></a>Typer af LinkedIn-jobopslag

LinkedIn tilbyder følgende typer jobopslag:

- **Limited Listing** – Gratis jobannoncer, der vises i søgeresultater, når kandidater søger job på LinkedIn og på en virksomheds LinkedIn-side. Limited Listings er målrettet mod aktive jobsøgende. Denne type af opslag er den type, som Attract leverer til LinkedIn. Du kan ikke promovere Limited Listing-job på LinkedIn. Hvis du vil promovere gratis Limited Listings-opslag, skal du bruge LinkedIn til at aktivere Job Wrapping. For mere information om Job Wrapping se [Begrænsede lister kontra Premium-jobmuligheder til job-wrapping](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) og [Job Wrapping Plus - Ofte stillede spørgsmål](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Premium Job Slot** – Købte opslag, der vises forskellige steder på tværs af LinkedIn, såsom LinkedIn-feed, mails og **Jobs You Might be Interested in** (Job, du måske vil være interesseret i ). Premium Job Slots er målrettet mod passive kandidater, men de vises også i jobsøgninger.

Attract slår job op på LinkedIn som gratis Limited Listings-opslag. Hvis du vil bruge Premium Job Slots, skal du bruge Job Wrapping igennem LinkedIn Recruiter. Job Wrapping kræver en job wrapping-kontrakt med LinkedIn. Du kan finde flere oplysninger under [Job Wrapping gennem LinkedIn Recruiter - Oversigt](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Frekvensen af batchbehandling på LinkedIn

LinkedIn behandler jobopslag i en batch gennem Attract én gang om dagen. Det kan derfor tage op til 48 timer, før job vises på LinkedIn, efter at de er blevet slået op via Attract. Hvis du har brug for, at job vises tidligere på LinkedIn, eller hvis du har brug for yderligere fleksibilitet, kan du bruge Recruiter System Connect-API'en (application programming interface) fra LinkedIn. Du kan finde flere oplysninger under [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Tabel med muligheder for jobopslag på LinkedIn

I følgende tabel beskrives de forskellige muligheder for jobopslag på LinkedIn. Den indeholder fordelene ved de enkelte muligheder og yderligere oplysninger.

|  | Attract | Job Wrapping via LinkedIn Recruiter | Recruiter System Connect-API |
|---|---|---|---|
| **Beskrivelse** | Attract slår job op på LinkedIn som et XML-feed. | Firma har kontrakt med LinkedIn og leverer et XML-feed til jobopslag. | Kunden bruger API til at synkronisere oplysninger mellem Attract og LinkedIn Recruiter. |
| **Hvilken type job kan jeg slå op?** | Limited Listing (gratis opslag) | Premium Job Slot eller Limited Listing | Limited Listing (gratis opslag) |
| **Kan jeg promovere jobbet på LinkedIn?** | Nej | Premium Job Slots: ja<br>Limited Listings: nej | Nej |
| **Hvor ofte slår LinkedIn job op?** | En gang om dagen | En gang om dagen | Flere gange om dagen, som det er defineret af API'en |
| **Anbefalet af LinkedIn?** | Nej | Ja | Nej |
| **Hvad skal jeg bruge?** | Køb af Attract | En job wrapping-kontrakt med LinkedIn og køb af Premium Job Slots | En API-aftale med LinkedIn | 
| **Hvor kan jeg finde yderligere oplysninger?** | [Konfigurer integration med LinkedIn til Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md) | [Job Wrapping via LinkedIn Recruiter - Oversigt](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Du behøver ikke en LinkedIn Recruiter System Connect-licens for at kunne slå job op på LinkedIn med Attract.

## <a name="see-also"></a>Se også

[Konfigurer integration med LinkedIn til Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md)

[Slå job op på LinkedIn fra Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[Rekrutter kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Fejlfinding af integration med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
