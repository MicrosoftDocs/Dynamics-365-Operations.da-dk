---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.
author: twheeloc
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8378418bdd0f4cb3f22b38a44e35179aad3ca33
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534227"
---
# <a name="dataverse-tables"></a>Dataverse-tabeller


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.

> [!NOTE]
> Enheder under Human Resources svarer til Dataverse-tabeller. Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Følgende Dataverse-tabeller er tilgængelige baseret på Human Resources-enheder.

## <a name="benefit-tables"></a>Frynsegodetabeller

| Navn | Tabellen |
| --- | --- |
| Frekvens for personalegodeberegning | cdm_benefitcalculationfrequency |
| Frynsegoders Beregningsfrekvens, betalingsperiode | cdm_benefitcalculationfrequencypayperiod |
| Frynsegodeberegningssats | cdm_benefitcalculationrate |
| Oplysninger om frynsegodeberegningssats | cdm_benefitcalculationratedetail |
| Frynsegodeindstilling | cdm_benefitoption |
| Frynsegodeplan | cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Human Resourcesgodetype | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Tabeller for forretningsprocesopgaver

| Navn | Tabellen |
| --- | --- |
| Forretningsproceskalender | cdm_businessprocesscalendar |
| Tildeling af forretningsprocesgruppe | cdm_businessprocessgroupassignment |
| Opgavegruppe for forretningsprocesbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprocesstadie | cdm_businessprocessstage |
| Kontrollisteskabelonhoved | cdm_businessprocesstemplateheader |
| Tjeklisteskabelonopgave | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Kompensationstabeller

| Navn | Tabellen |
| --- | --- |
| Fast lønstruktur | cdm_compensationfixedplan |
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
| Hændelse for fast løn | cdm_fixedcompensationevent |
| Fordelingsregel | cdm_vestingrule |
| Arbejders faste løn | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Organisationstabeller

| Navn | Tabellen |
| --- | --- |
| Afdeling | cdm_department |
| Ansættelse | cdm_employment |
| Firma | cdm_company |
| Stilling | cdm_job |
| Jobfunktion | cdm_jobfunction |
| Stilling | cdm_jobposition |
| Stillingstype | cdm_positiontype |
| Arbejdertildeling til stilling | cdm_positionworkerassignmentmap |
| Stillingsdimension | cdm_jobpositiondimension|
| Jobtype | cdm_jobtype |
| Sprog | cdm_language |
| Stilling | cdm_title |

> [!NOTE]
> Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Dataverse. Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Dataverse til HR. 

## <a name="leave-and-absence-tables"></a>Orlov og fravær-tabeller

| Navn | Tabellen |
| --- | --- |
| Orlovsbanktransaktion | cdm_leavebanktransaction |
| Orlovstilmelding | cdm_leaveenrollment |
| Orlovsplan | cdm_leaveplan |
| Orlovsanmodning | cdm_leaverequest |
| Detaljer om orlovsanmodning | cdm_leaverequestdetail |
| Orlovstype | cdm_leavetype |
| Orlovstypens årsagskode | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Løntabeller

| Navn | Tabellen |
| --- | --- |
| Betalingscyklus | cdm_paycycle |
| Lønperiode | cdm_payperiod |
| Lønkode | cdm_payrollearningcode |
| Bankkontoudbetalinger | cdm_bankaccountdisbursement |
| Skatteområde | cdm_taxregion |

## <a name="worker-tables"></a>Arbejdertabeller

| Navn | Tabellen |
| --- | --- |
| Arbejdstråd | cdm_worker |
| Arbejderadresse | cdm_workeraddress |
| Arbejders personlige oplysninger | cdm_workerpersonaldetail |
| Personidentifikationsnummeret for arbejder | cdm_workerpersonidentificationnumber |
| Personidentifikationstype for arbejder | cdm_workerpersonidentificationtype |
| Arbejdskalender | cdm_workcalendar |
| Arbejdskalenderdag | cdm_workcalendarday |
| Arbejdskalenderfridag |cdm_workcalendarholiday |
| Ferielinje i arbejdskalender | cdm_workcalendarholidayline |
| Tidsinterval i arbejdskalender | cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Arbejderbankkonto | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Opsætningstabeller for arbejdere

| Navn | Tabellen |
| --- | --- |
| Veteranstatus | cdm_veteranstatus |
| Etnisk oprindelse | cdm_ethnicorigin |
| Årsagskode | cdm_reasoncode |
| Udstedende organ for personidentifikation | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetencetabeller

| Navn | Tabellen |
| --- | --- |
| Kompetencetype | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabelrelationsmodeller

### <a name="worker"></a>Arbejdstråd

![Arbejder.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stilling og job

![Stilling og job.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Personalegoder

![Personalegoder.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensation

![Kompensation.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Forlad

![Orlov.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbejdskalender

![Arbejdskalender.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Se også

[Vælg en dataintegrationsteknologi](hr-admin-integration-choose-technology.md)<br>
[Konfigurere Dataverse-integration](hr-admin-integration-common-data-service.md)<br>
[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Ofte stillede spørgsmål om Virtuelle tabeller i Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiopdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
