---
title: Nyheder eller ændringer i Dynamics 365 Talent (3. december 2019)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528687"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (3. december 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2646. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Arbejdsområdet **Administration af funktioner** indeholder en oversigt over de funktioner, der er leveret i hver udgave. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem. Du kan finde flere oplysninger om Administration af funktioner under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet **Administration af funktioner**, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.
 
På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet **Administration af funktioner**).
 
Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet **Administration af funktioner** angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Planlæg periodisk batchjob til oprydning af historik (332528)

Med denne ændring kører **Batchjobhistorik** hver nat og fjerner oversigtsemner for batchjob, som er ældre end 30 dage.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent reagerer ikke i arbejderhandlinger, når identifikationsnummerets længde ikke svarer til identifikationstypen (390971)

Denne udgivelse korrigerer problemet, når identifikationsnummerets længde ikke svarer til definitionen inden for identifikationstypen. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Fast løn opdaterer ikke niveau med ændringer af positionsoplysninger (348085)

I denne uges udgivelse bestemmer **Startdato for kompensation** det job, der er tilknyttet stillingen på det pågældende tidspunkt, når der oprettes en ny fast lønspost for en medarbejder.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Listerne Arbejdere, Medarbejdere og Kontrahenter viser Arbejdertype som Begge, når de kun skal være Arbejder eller Kontrahent (384473)

Denne ændring afspejler præcist, hvilken type arbejder der er indtastet (kontrahent eller medarbejder).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>E-mailnotifikationer for nye ansættelseshandlinger indeholder ikke navneoplysninger på grund af sikkerhedspolitikker (383402)

Denne ændring retter de oplysninger, der vises i felterne fornavn eller efternavn i pladsholderne for arbejdsprocessen, når avanceret sikkerhed er aktiveret.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Systemet tillader to heldags orlovsanmodninger for samme dag (379284)

Med denne ændring kan du ikke udstede to orlovsanmodninger for samme dag. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Listen adresseændringer skal sorteres efter ikrafttrædelsesdato (352798)

Med denne ændring sorteres adresseændringslisten nu efter **Ikrafttrædelsesdato**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Orlovsanmodninger skal tillade sletninger fra Common Data Service til Talent (376999)

Med denne ændring kan udkast og annullerede orlovsanmodninger slettes fra Common Data Service og derefter fjernes fra Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Sletning af indtjeningskoder er tilladt, når den samme indtjeningskode tildeles en medarbejder (371792)

I denne version skal du først fjerne indtjeningskoden fra medarbejderen, før du sletter indtjeningskoden fra systemet.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Arbejdsgangen for orlov og fravær med to godkendelsesstadier er ikke fuldført (391116)

Med denne ændring fortsætter arbejdsgangen orlov og fravær gennem alle trin, når der er konfigureret mere end én godkendelsesfase for anmodningen.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Udstedelsesdato synkroniseres ikke med Common Data Service, når den opdateres eller indtastes i Talent (397361)

Denne ændring korrigerer et problem, hvor udstedelsesdatoen for **Personidentifikations**-poster ikke blev synkroniseret med Common Data Service fra Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Hierarki-cirkulære referencefejl, der er udstedt ved tildeling af en leder til en stilling (386659)

Denne ændring korrigerer et entydigt scenarie, hvor der vises en cirkulær referencefejl, når en ny leder tildeles en stilling.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-enheder, der nu understøtter brugerdefinerede felter

Følgende Common Data Service-enheder understøtter nu brugerdefinerede felter:

| Navn | Enhed |
| --- | --- |
| Bankkontoudbetalinger | cdm_bankaccountdisbursement |
| Frekvens for frynsegodeberegning | cdm_benefitcalculationfrequency |
| Frynsegoders Beregningsfrekvens, betalingsperiode | cdm_benefitcalculationfrequencypayperiod |
| Frynsegodeberegningssats | cdm_benefitcalculationrate |
| Oplysninger om frynsegodeberegningssats | cdm_benefitcalculationratedetail |
| Frynsegodeindstilling | cdm_benefitoption |
| Frynsegodeplan | cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Frynsegodetype | cdm_benefittype |
| Forretningsproceskalender | cdm_businessprocesscalendar |
| Tildeling af forretningsprocesgruppe | cdm_businessprocessgroupassignment |
| Opgavegruppe for forretningsprocesbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprocesstadie | cdm_businessprocessstage |
| Kontrollisteskabelonhoved | cdm_businessprocesstemplateheader |
| Kontrollisteskabelonopgave | cdm_businessprocesstemplatetask |
| Regnskab | cdm_company |
| Kompensation - fast struktur | cdm_compensationfixedplan |
| Kompensationsgitter | cdm_compensationgrid |
| Kompensationsniveau | cdm_compensationlevel |
| Kompensation - lønfrekvens | cdm_compensationpayfrequency |
| Opsætning af kompensationsreferencepunkt | cdm_compensationreferencepointsetup |
| Opsætningslinje for kompensationsreferencepunkt | cdm_compensationreferencepointsetupline |
| Kompensationsområde | cdm_compensationregion |
| Kompensationsstruktur | cdm_compensationstructure |
| Variabel kompensationsplan | cdm_compensationvariableplan |
| Niveau i variabel kompensationsplan | cdm_compensationvariableplanlevel |
| Type af variabel kompensationsplan | cdm_compensationvariableplantype |
| Afdeling | cdm_department |
| Ansættelse | cdm_employment |
| Etnisk oprindelse | cdm_ethnicorigin |
| Hændelse for fast løn | cdm_fixedcompensationevent |
| Stilling | cdm_job |
| Jobfunktion | cdm_jobfunction |
| Stilling | cdm_jobposition |
| Jobtype | cdm_jobtype |
| Sprog | cdm_language |
| Orlovsbanktransaktion | cdm_leavebanktransaction |
| Orlovstilmelding | cdm_leaveenrollment |
| Orlovsplan | cdm_leaveplan |
| Orlovsanmodning | cdm_leaverequest |
| Detaljer om orlovsanmodning | cdm_leaverequestdetail |
| Orlovstype | cdm_leavetype |
| Orlovstypens årsagskode | cdm_leavetypereasoncode |
| Betalingscyklus | cdm_paycycle |
| Lønperiode | cdm_payperiod |
| Lønkode | cdm_payrollearningcode |
| Udstedende organ for personidentifikation | cdm_personidentificationissuingagency |
| Stillingstype | cdm_positiontype |
| Arbejdertildeling til stilling | cdm_positionworkerassignmentmap |
| Årsagskode | cdm_reasoncode |
| Færdighedstype | cdm_skilltype |
| Skatteområde | cdm_taxregion |
| Fordelingsregel | cdm_vestingrule |
| Veteranstatus | cdm_veteranstatus |
| Arbejdskalender | cdm_workcalendar |
| Arbejdskalenderdag | cdm_workcalendarday |
| Arbejdskalenderfridag |cdm_workcalendarholiday |
| Ferielinje i arbejdskalender | cdm_workcalendarholidayline |
| Tidsinterval i arbejdskalender | cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Arbejdstråd | cdm_worker |
| Arbejders adresse | cdm_workeraddress |
| Arbejders bankkonto | cdm_workerbankaccount |
| Arbejders faste løn | cdm_workerfixedcompensation |
| Arbejders personlige oplysninger | cdm_workerpersonaldetail |
| Personidentifikationsnummeret for arbejder | cdm_workerpersonidentificationnumber |
| Personidentifikationstype for arbejder | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Som eksempel

Prøveversionsfunktioner er kun tilgængelige i **Sandkasse**-miljøer.

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]