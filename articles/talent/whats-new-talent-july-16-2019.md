---
title: Nyheder eller ændringer i Dynamics 365 for Talent (16. juli 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ac0990a72224395cf109c7eb42cbb48ece2a0b4f
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795190"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-16-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (16. juli 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Kommer snart i Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Jobgodkendelser vises på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id'et, jobtitlen, andre godkendere og datoen, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig skal godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-enheder, der nu understøtter brugerdefinerede felter

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Mål og gennemgange er ikke synlige i Chefselvbetjening

Denne uges ændringer giver nu mulighed for at se og redigere mål og gennemgange af niveauer i Chefselvbetjening.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Formen Mål kan ikke lukkes, når en bruger redigerer et målfelt

Denne udgivelse retter et problem, hvor målformen ikke kan lukkes, når du vælger **Luk**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Oprettelse af nye mål og lagring viser fejl

Denne udgivelse retter et problem, når der gemmes mål i medarbejder- og chefselvbetjening.

### <a name="unable-to-add-a-field-to-position-details"></a>Et felt kan ikke føjes til stillingsdetaljer 

I denne version understøttes brugerdefinerede felter nu på stillingsdetaljer.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Der kan ikke defineres udløbsdato for lønkoden via datastyring

Ændringer giver dig nu mulighed for at angive udløbsdatoer for lønkoder i datastyring.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nye brugerdefinerede felter synkroniseres ikke hurtigt nok

Ydeevnen for synkronisering af brugerdefinerede felter til Common Data Service er forbedret med denne uges udgivelse.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Objekteksport til databasejobs mislykkes med fejlmeddelelsen "Format af initialiseringsstreng stemmer ikke overens med specifikationen med start ved indeks 0."

Denne version retter problemet, hvor databasebatchjobbene mislykkes. Sådan opdaterer du manuelt:

1. Gå til **Datastyring**.
2. Vælg **Konfigurer enhedseksport til database**.
3. Genindtast forbindelsesstrengen til måldatabasen, og vælg **Gem**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>Konfigurationen af SMTP-mail mislykkes pludseligt med fejlmeddelelsen: "SMTP-serveren kræver en sikker forbindelse, eller klienten blev ikke godkendt".

Denne version retter en SMTP-mailkonfiguration, som pludselig mislykkes. Sådan opdaterer du manuelt:

1. Gå til **Systemadministration**.
2. Vælg **E-mail-parametre**.
3. Vælg **SMTP-indstillinger**. 
4. Genindtast det brugernavn og den adgangskode, der bruges til SMTP-serveren, og vælg **Gem**.

## <a name="in-preview"></a>Som eksempel

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Visningsfunktioner er kun aktiverede i sandkasseforekomster

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**. Forekomster af typen **Sandkasse** giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange forskellige typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Få vist performanceoplysninger for direkte og udvidede underordnede i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye fornyede gennemgange. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede.
