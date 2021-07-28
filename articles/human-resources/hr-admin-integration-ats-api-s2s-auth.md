---
title: Server til server-godkendelse for ATS-integrations-API
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere server til server-godkendelse for integrationer med Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System).
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ed76d22ab6b917c931220f3ba462f4f14cae207
ms.sourcegitcommit: bd684c9eb6de718573e6be5479e1832fe614d919
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6373055"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Server til server-godkendelse for ATS-integrations-API

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere server til server-godkendelse for programintegrationer med Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System). Der er et par sikkerhedslag, som skal administreres for tjenesteprincipalen for at få adgang til den virtuelle Microsoft Dataverse-tabel og tilknyttede data. Brugeren skal have adgang til den virtuelle Dataverse-tabel i Microsoft Power Platform og adgang til dataene i Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Give adgang til virtuelle Dataverse-tabeller i Power Platform

Det første trin, der skal udføres for at give adgang til de virtuelle Dataverse-tabeller i Power Platform, er at konfigurere programmet i Power Platform til godkendelse i forhold til virtuelle Dataverse-tabelslutpunkter. Disse trin beskrives i [Microsoft Dataverse-vejledningen for udviklere](/powerapps/developer/data-platform).

  - Til registrering af en app for enkelt lejer: [Brug server til server-godkendelse for enkelt lejer](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Til registrering af en app for flere lejere: [Brug server til server-godkendelse for flere lejere](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Oprette en sikkerhedsrolle for ATS-integrationer

Et af trinnene, der skal udføres efter oprettelsen af programbrugeren, er at tildele brugeren en sikkerhedsrolle, der definerer den adgang, programmet skal have til slutpunkterne. Dette er trin 7 i [Oprettelse af programbruger](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) registrering af en app for en enkelt lejer og [Oprette en sikkerhedsrolle for programbrugeren](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) til registreringer med flere lejere. 

Den rolle, som du tildeler programbrugeren til, skal have adgang til de dataenheder, der bruges til din ATS-integration. Den findes ikke som standard, så der skal oprettes en ny sikkerhedsrolle. Den nye rolle kan oprettes ved at følge de trin, der er beskrevet under [Oprette en sikkerhedsrolle](/power-platform/admin/create-edit-security-role#create-a-security-role).

For den nye rolle skal den relevante adgang som minimum tildeles til følgende enheder under fanen **Brugerdefinerede enheder** for den nye rolle. Bemærk, at du muligvis skal tilføje flere enheder, hvis integrationen bruger mere omfattende programdata. Når den nye rolle er oprettet, kan den tildeles til programbrugeren.

  - Basisarbejder (mshr)
  - Kandidat, der kan ansættes (mshr)
  - Certifikatkompetence (mshr)
  - Certifikattype (mshr)
  - Virksomhed
  - Kompensationsjobfunktion (mshr)
  - Kompensationsjobtype (mshr)
  - Land/områder (mshr)
  - Afdeling (mshr)
  - Uddannelsekompetencer (mshr)
  - Uddannelsesgrad (mshr)
  - Uddannelser (mshr)
  - Uddannelseskrav (mshr)
  - Identifikation (mshr)
  - Identifikationstype (mshr)
  - Institution (mshr)
  - Udstedende organ (mshr)
  - Jobkompensation (mshr)
  - Job (mshr)
  - Uddannelsesniveau (mshr)
  - Partkontakter (mshr)
  - Personer (mshr)
  - Personadresser (mshr)
  - Personscreening (mshr)
  - Stillingstype (mshr)
  - Stillinger V2 (mshr)
  - Kompetence inden for erhvervserfaring (mshr)
  - Rangeringsniveau (mshr)
  - Klassifikationsmodeller (mshr)
  - Årsagskoder (mshr)
  - Rekrutteringsanmodning (mshr)
  - Lokation af rekrutteringsanmodning (mshr)
  - Stilling til rekrutteringsanmodning (mshr)
  - Rekrutteringsanmodningsfærdigheder (mshr)
  - Screeningstype (mshr)
  - Færdighedskompetencer (mshr)
  - Færdigheder (mshr)
  - Titler (mshr)
  - Veteranstatus (mshr)
  - Arbejder (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Tildele ansøgningstilladelser til Human Resources-data

Det andet trin er at sikre, at programmet får de relevante tilladelser til dataene i Human Resources, ved at knytte det til en bruger i programmet Human Resources. For en applikationsbruger sker server til server-kald via virtuelle Dataverse-tabeller i forbindelse med identiteten for den bruger (app) i Dataverse, som aktiverer handlingen. Adaptertjenesten for den virtuelle tabel søger derefter efter den tilknyttede bruger i Human Resources og kører forespørgslen for den pågældende bruger. Det betyder, at en bruger skal oprettes i Human Resources med de korrekt tildelte roller for at give adgang til de data, som integrationsapplikationen har brug for.

Human Resources-brugeren skal også tildeles de korrekte tilladelser til dataene i Human Resources. Rollen **Rekrutteringsprogram** (HcmRecruitingIntegrator) er tilgængelig med rettigheder til de primære enheder, der kræves for at integrere med rekrutteringsdata. Programbrugeren på siden **Brugere** kan tildeles denne rolle for at give den rette adgang til dataene. Du kan finde flere oplysninger om sikkerhedsroller i Human Resources i [Rollebaseret sikkerhed](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Oprette den nye bruger med de rette tilladelser

Hvis du vil oprette den nye bruger med de rette tilladelser, skal du udføre disse trin:

  1. Åbn siden **Brugere** i Human Resources, og vælg **Ny**.
  2. Angiv et **bruger-id** og et **brugernavn** til den nye programbruger. Du kan for eksempel skrive "RecruitingIntegration".

      > [!NOTE]
      > Hvis appen ikke har en Microsoft Azure Active Directory-brugerkonto eller mailadresse (Azure AD), kan du skrive noget i stil med "RecruitingApp" i brugerens felt for mailadresse og udbyder.

  3. Vælg handlingen **Tildel roller** i oversigtspanelet **Brugers roller**.
  4. I ruden **Tildel brugere roller** skal du vælge **Rekrutteringsprogram** og vælge **OK**.
  5. Gem den nye brugerpost.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Knytte den nye bruger i Human Resources til programmet

Når brugeren er oprettet, skal der oprettes en post for programmet i formularen **Azure Active Directory-programmer** for at knytte appen til Human Resources-brugeren.

  1. Åbn formularen **Azure Active Directory-programmer**, og vælg **Ny**.
  2. Angiv klient-id'et for den programbruger, der er oprettet til programmet, i feltet **Klient-id**.
  3. Angiv navnet på integrationsprogrammet i feltet **Navn**.
  4. Vælg den nye Human Resources-bruger, der er oprettet til rekrutteringsintegrationen, i feltet **Bruger-id**.
  5. Gem den nye post.

Derefter har programmet adgang til Human Resources-data, men kun de data, der kræves til integrationer med rekrutteringsprogrammet.

## <a name="see-also"></a>Se også

[Rekruttere jobkandidater](hr-personnel-recruit.md)<br>
[Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Brug Microsoft Dataverse Web-API](/powerapps/developer/data-platform/webapi/overview)<br>
[Opret og opdater de indstillinger, der er angivet ved hjælp af Web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
