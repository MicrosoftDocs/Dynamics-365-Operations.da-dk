---
title: Konfigurer LinkedIn-integration med Attract
description: Dette emne forklarer, hvordan du konfigurerer LinkedIn-integration for Microsoft Dynamics 365 Talent - Attract, så du nemt kan slå job op på LinkedIn fra Attract, så dine rekrutteringsmedarbejdere kan synkronisere deres rekrutteringsoplysninger med en kandidats LinkedIn-profil.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460709"
---
# <a name="set-up-linkedin-integration-with-attract"></a>Konfigurer LinkedIn-integration med Attract

[!include [banner](includes/banner.md)]

Hjælp dine rekrutteringsmedarbejdere og ansættelsesansvarlige med at tiltrække de bedste talenter ved at konfigurere LinkedIn-integration med Microsoft Dynamics 365 Talent: Attract. Attract giver dig mulighed for at slå job direkte op til LinkedIn, det største professionelle onlinenetværk.

Job, som du slår op på LinkedIn via Attract, er gratis jobopslag, som leveres uden nogen ekstraomkostninger for dit firma. Disse opslag er kun tilgængelige via LinkedIn-softwarepartnere som f.eks. Attract. De vises ikke i panelet **Karriere** på din virksomheds LinkedIn-side, fordi der kun vises betalte opslag der. De vises dog, når potentielle kandidater ser alle ledige job. De gratis jobopslag vises også i LinkedIn-jobsøgninger.

Attract giver to måder for interaktion med LinkedIn, så du kan få hjælp til at rekruttere kandidater fra dette populære karrierewebsted:

- Slå job op på LinkedIn fra Attract.
- Rekruttér kandidater fra LinkedIn i Attract.

Du kan konfigurere begge muligheder under fanen **LinkedIn-integration** i Administration. Åbn Administration ved at gå til <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Før du kan bruge LinkedIn Recruiter-integration med Attract, skal du have [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) og [LinkedIn Recruiter-licenser](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

Hvis du har problemer med at slå job op på LinkedIn, kan du finde hjælp i [Fejlfinding af integration med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

Du kan finde oplysninger om andre måder at slå job op på LinkedIn i [Ofte stillede spørgsmål om Attract-integration med LinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Konfigurere jobopslag til LinkedIn

Før du kan slå job op fra Attract til LinkedIn, skal du bruge et [LinkedIn-firma-id](https://aka.ms/findID). Dit LinkedIn-firma-id er en streng med tal, der entydigt identificerer dit firma i LinkedIn. Der er mere information under [Tilknytning af dit LinkedIn-firma-id til LinkedIn-jobportalen - ofte stillede spørgsmål](https://aka.ms/findID).

Attract sender et feed af dine jobopslag til LinkedIn, og LinkedIn kontrollerer for feedet omtrent én gang om dagen. Det kan tage op til 48 timer, før dine job er slået op på webstedet.

Job, der slås op på LinkedIn, vises på live LinkedIn-webstedet. LinkedIn har ikke noget testmiljø til jobopslag. Sørg derfor for, at du ikke ved en fejltagelse slår testjob op. 

1. I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administration**. Du kan også gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Vælg fanen **LinkedIn-integration**.
3. Angiv navnet på din virksomhed under **Firmanavn**, og angiv dit LinkedIn-firma-id under **Firma-id**. Sørg for, at firmanavnet svarer til det navn, der vises på dit firmas LinkedIn-side. Der er mere information om LinkedIn-firma-id under [Tilknytning af dit LinkedIn-firma-id til LinkedIn-jobportalen - ofte stillede spørgsmål](https://www.linkedin.com/help/linkedin/answer/98972).

    Hvis du har brug for at ændre oplysningerne for din organisation, skal du se [Ændre din organisations adresse, tekniske kontakt osv](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Hvis du stadig har problemer, skal du kontakte [LinkedIn-support](https://www.linkedin.com/help/linkedin).

4. Vælg **Gem**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Konfigurer LinkedIn Recruiter med Attract 

Hvis du vil tillade, at rekrutteringsmedarbejdere rekruttere ansøgere fra LinkedIn Recruiter, skal du konfigurere integration med LinkedIn Recruiter i Attract. For at gennemføre konfigurationsprocessen skal du arbejde sammen med den bruger, der er administrator på din organisations LinkedIn Recruiter-kontrakt.

1. I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administration**. Du kan også gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Vælg fanen **LinkedIn-integration**.

    [![Attract-administratorvisning for at starte integrationen af LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Vælg **Tilknyt** for at starte opsætningen. Du vil blive guidet gennem processen for tilmelding til LinkedIn.
4. Hvis du har poster på flere LinkedIn-kontrakter, skal du vælge den kontrakt, som du vil forbinde med Attract-systemet. Hvis du har en post i kun én LinkedIn-kontrakt, er dette trin ikke nødvendigt.
5. Under **Recruiter System Connect (RSC)** skal du klikke på **Request** (Anmod om).

    [![Attract-administratorvisning for at anmode om integration af LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Indstillingen **Recruiter System Connect (RSC)** skal nu vises som **Partner Ready** (Partnerklar). Hvis du kan se **Notify partner** (Informer partner) på denne side, skal du vente et øjeblik, vælge **Notify partner** (Informer partner) og derefter opdatere siden. Indstillingen skulle nu blive vist som **Partner Ready** (Partnerklar).

    [![Attract-administratorvisning til angivelse af Attract-siden af anmodninger, der er fuldført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. For at fuldføre de næste trin skal du have administratorrettigheder til din LinkedIn Recruiter-kontrakt.

    1. Log på LinkedIn ved hjælp af din administratorkonto, og vælg **LinkedIn Recruiter** øverst til højre. 
    2. I menuen **More** (Flere) øverst på siden skal du vælge **Admin Settings** (Administratorindstillinger) og derefter vælge fanen **ATS**.
    3. Hvis du vil aktivere ét-klik-eksport for kun én kontrakt , skal du aktivere **Contract Level access (for every seat on this contract)** (Adgang til kontraktniveau (for hvert sæde i denne kontrakt)). Hvis du vil aktivere det for hele firmaet, skal du aktivere **Company Level access (for every contract in your company)** (Adgang på firmaniveau (for hver kontrakt i firmaet)).

    [![Slå integration af Attract til fra administratorvisning i LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Gå til Attract Administration, og vælg fanen **Integration af LinkedIn**. Indstillingen **Recruiter System Connect (RSC)** skulle nu være vist som **Aktiveret**.

    [![LinkedIn Recruiter-integration er fuldført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Konfigurere Ansøg med LinkedIn i Attract

Du kan give kandidater mulighed for at ansøge om dine job ved hjælp af deres LinkedIn-profiler. Yderligere oplysninger om Ansøg med LinkedIn finder du under [Styrken ved LinkedIn overalt: Ansøg med LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Denne funktion findes på nuværende tidspunkt i prøveversionen. Før du følger disse trin, skal du sikre dig, at Ansøg med LinkedIn er aktiveret. Du kan finde flere oplysninger om aktivering af funktioner til forhåndsvisning under [Få adgang til funktioner i prøveversioner af Microsoft Dynamics 365 Talent](./access-preview-feature.md).

1. I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administration**. Du kan også gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Vælg fanen **LinkedIn-integration**.

    [![Attract-administratorvisning for at starte integrationen af LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Ud for **Ansøg med LinkedIn** skal du vælge **Connect** for at starte opsætningen. Du vil blive guidet gennem resten af processen med LinkedIn.

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om Attract-integration med LinkedIn](./attract-linkedin-faq.md)

[Slå job op på eksterne karrierewebsteder fra Attract](./posting-jobs-external.md)

[Rekrutter kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Oprette, godkende og bogføre job i Attract](./creating-jobs-attract.md)

[Fejlfinding af integration med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]