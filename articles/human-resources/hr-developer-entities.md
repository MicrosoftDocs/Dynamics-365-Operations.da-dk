---
title: Common Data Service-enheder
description: Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530000"
---
# <a name="common-data-service-entities"></a>Common Data Service-enheder

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.

Du kan finde flere oplysninger om Common Data Service i [Hvad er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Følgende HR-ressourcer er tilgængelige i Common Data Service .

## <a name="benefit-entities"></a>Frynsegodeenheder

| Navn | Enhed |
| --- | --- |
| Frekvens for frynsegodeberegning | cdm_benefitcalculationfrequency |
| Frynsegoders Beregningsfrekvens, betalingsperiode | cdm_benefitcalculationfrequencypayperiod |
| Frynsegodeberegningssats | cdm_benefitcalculationrate |
| Oplysninger om frynsegodeberegningssats | cdm_benefitcalculationratedetail |
| Frynsegodeindstilling | cdm_benefitoption |
| Frynsegodeplan | cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Frynsegodetype | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Enheder for forretningsprocesopgaver

| Navn | Enhed |
| --- | --- |
| Forretningsproceskalender | cdm_businessprocesscalendar |
| Tildeling af forretningsprocesgruppe | cdm_businessprocessgroupassignment |
| Opgavegruppe for forretningsprocesbibliotek | cdm_businessprocesslibrarytaskgroup |
| Forretningsprocesstadie | cdm_businessprocessstage |
| Kontrollisteskabelonhoved | cdm_businessprocesstemplateheader |
| Kontrollisteskabelonopgave | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Kompensationsenheder

| Navn | Enhed |
| --- | --- |
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
| Hændelse for fast løn | cdm_fixedcompensationevent |
| Fordelingsregel | cdm_vestingrule |
| Arbejders faste løn | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisationsenheder

| Navn | Enhed |
| --- | --- |
| Afdeling | cdm_department |
| Ansættelse | cdm_employment |
| Regnskab | cdm_company |
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
> Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Common Data Service. Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Common Data Service til HR. 

## <a name="leave-and-absence-entities"></a>Orlovs- og fraværsenheder

| Navn | Enhed |
| --- | --- |
| Orlovsbanktransaktion | cdm_leavebanktransaction |
| Orlovstilmelding | cdm_leaveenrollment |
| Orlovsplan | cdm_leaveplan |
| Orlovsanmodning | cdm_leaverequest |
| Detaljer om orlovsanmodning | cdm_leaverequestdetail |
| Orlovstype | cdm_leavetype |
| Orlovstypens årsagskode | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Lønenheder

| Navn | Enhed |
| --- | --- |
| Betalingscyklus | cdm_paycycle |
| Lønperiode | cdm_payperiod |
| Lønkode | cdm_payrollearningcode |
| Bankkontoudbetalinger | cdm_bankaccountdisbursement |
| Skatteområde | cdm_taxregion |

## <a name="worker-entities"></a>Enheder for arbejder

| Navn | Enhed |
| --- | --- |
| Arbejdstråd | cdm_worker |
| Arbejders adresse | cdm_workeraddress |
| Arbejders personlige oplysninger | cdm_workerpersonaldetail |
| Personidentifikationsnummeret for arbejder | cdm_workerpersonidentificationnumber |
| Personidentifikationstype for arbejder | cdm_workerpersonidentificationtype |
| Arbejdskalender | cdm_workcalendar |
| Arbejdskalenderdag | cdm_workcalendarday |
| Arbejdskalenderfridag |cdm_workcalendarholiday |
| Ferielinje i arbejdskalender | cdm_workcalendarholidayline |
| Tidsinterval i arbejdskalender | cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter) |
| Arbejders bankkonto | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Enheder til opsætning af arbejder

| Navn | Enhed |
| --- | --- |
| Veteranstatus | cdm_veteranstatus |
| Etnisk oprindelse | cdm_ethnicorigin |
| Årsagskode | cdm_reasoncode |
| Udstedende organ for personidentifikation | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Kompetenceenheder

| Navn | Enhed |
| --- | --- |
| Færdighedstype | cdm_skilltype |

## <a name="entity-relationship-models"></a>Enhedsrelationsmodeller

### <a name="worker"></a>Arbejdstråd

![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stilling og job

![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Frynsegoder

![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensation

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Orlov

![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbejdskalender

![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Se også

[Vælg en dataintegrationsteknologi](hr-admin-integration-choose-technology.md)</br>
[Konfigurere Common Data Service-integration](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]