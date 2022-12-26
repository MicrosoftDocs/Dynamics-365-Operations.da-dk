---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838576"
---
# <a name="dataverse-tables"></a>Dataverse-tabeller


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.

> [!NOTE]
> Enheder under Human Resources svarer til Dataverse-tabeller. Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Følgende Dataverse-tabeller er tilgængelige baseret på Human Resources-enheder.

Der er flere oplysninger om kendte problemer i [Søg i Lifecycle Services efter oplysninger om problemer (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Frynsegodetabeller

| Name | Tabellen | Kendte problemer  | Status |
| --- | --- |    --------|----------  |
| Frekvens for personalegodeberegning | cdm_benefitcalculationfrequency |     |     |
| Frynsegoders Beregningsfrekvens, betalingsperiode | cdm_benefitcalculationfrequencypayperiod |     |     |
| Frynsegodeberegningssats | cdm_benefitcalculationrate |    |     |
| Oplysninger om frynsegodeberegningssats | cdm_benefitcalculationratedetail |753225 | Løst  |
| Frynsegodeindstilling | cdm_benefitoption |    |     |
| Frynsegodeplan | cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter) |    |     |
| Human Resourcesgodetype | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Tabeller for forretningsprocesopgaver

| Name | Tabellen |Kendte problemer  | Status |
| --- | --- |   --------|----------   |
| Forretningsproceskalender | cdm_businessprocesscalendar | 751867 | Løst |
| Tildeling af forretningsprocesgruppe | cdm_businessprocessgroupassignment | 751869  751863 | Aktivt|
| Opgavegruppe for forretningsprocesbibliotek | cdm_businessprocesslibrarytaskgroup |751866 | Lukkede |
| Forretningsprocesstadie | cdm_businessprocessstage |      |     |
| Kontrollisteskabelonhoved | cdm_businessprocesstemplateheader |     |     |
| Tjeklisteskabelonopgave | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Kompensationstabeller

| Name | Tabellen |Kendte problemer  | Status |
| --- | --- | ----------      | -------    |
| Fast lønstruktur | cdm_compensationfixedplan |754453 | Lukkede |
| Kompensationsgitter | cdm_compensationgrid |             |     |
| Kompensationsniveau | cdm_compensationlevel |           |     |
| Kompensation - lønfrekvens | cdm_compensationpayfrequency |                  |     |
| Opsætning af kompensationsreferencepunkt | cdm_compensationreferencepointsetup |               |     |
| Opsætningslinje for kompensationsreferencepunkt | cdm_compensationreferencepointsetupline |             |     |
| Kompensationsområde | cdm_compensationregion |                   |     |
| Kompensationsstruktur | cdm_compensationstructure |    754456        | Lukkede    |
| Variabel kompensationsplan | cdm_compensationvariableplan |               |     |
| Niveau i variabel kompensationsplan | cdm_compensationvariableplanlevel |                |     |
| Type af variabel kompensationsplan | cdm_compensationvariableplantype |               |     |
| Hændelse for fast løn | cdm_fixedcompensationevent |               |     |
| Fordelingsregel | cdm_vestingrule |              |     |
| Arbejders faste løn | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Organisationstabeller

| Name | Tabellen |Kendte problemer  | Status |
| --- | --- | ----------      | -------    |
| Afdeling | cdm_department |  752194    | Lukkede    |
| Ansættelse | cdm_employment | 762414  |  Lukkede  |
| Virksomhed | cdm_company |  |     |
| Job | cdm_job |  |     |
| Jobfunktion | cdm_jobfunction |        |     |
| Stilling | cdm_jobposition | 752214      | Lukkede    |
| Stillingstype | cdm_positiontype |            |     |
| Arbejdertildeling til stilling | cdm_positionworkerassignmentmap | 752224    |  Lukkede   |
| Stillingsdimension | cdm_jobpositiondimension|       |     |
| Jobtype | cdm_jobtype |      |     |
| Sprog | cdm_language |        |     |
| Stilling | cdm_title |       |     |

> [!NOTE]
> Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Dataverse. Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Dataverse til HR. 

## <a name="leave-and-absence-tables"></a>Orlov og fravær-tabeller

| Name | Tabellen | Kendte problemer  | Status |
| --- | --- |   ----------      | -------    |
| Orlovsbanktransaktion | cdm_leavebanktransaction |  752252    |    Løst |
| Orlovstilmelding | cdm_leaveenrollment |  752934    |Lukkede     |
| Orlovsplan | cdm_leaveplan |   752232   |   Lukkede  |
| Orlovsanmodning | cdm_leaverequest | 753207     | Lukkede    |
| Detaljer om orlovsanmodning | cdm_leaverequestdetail | 753207     |   Lukkede  |
| Orlovstype | cdm_leavetype |      |     |
| Orlovstypens årsagskode | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Integration med skrivetyper ved hjælp af Dataverse-tabeller for orlov og fravær er kun tilgængelig, når funktionen **Konfigurer flere orlovstyper for en enkelt orlovsplan** er aktiveret i Microsoft Dynamics 365 Finance ved hjælp af **funktionsstyring**. 

## <a name="payroll-tables"></a>Løntabeller

| Name | Tabellen |Kendte problemer  | Status |
| --- | --- |  ----------      | -------    |
| Betalingscyklus | cdm_paycycle |    |     |
| Lønperiode | cdm_payperiod |          |     |
| Lønkode | cdm_payrollearningcode |   754458        |   Lukkede  |
| Bankkontoudbetalinger | cdm_bankaccountdisbursement |    751904     |   Lukkede  |
| Skatteområde | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Arbejdertabeller

| Name | Tabellen |Kendte problemer  | Status |
| --- | --- |----------      | -------    |
| Arbejdstråd | cdm_worker |    751906    |    Lukkede |
| Arbejderadresse | cdm_workeraddress |   754465     |Lukkede     |
| Arbejders personlige oplysninger | cdm_workerpersonaldetail |   751906     |   Lukkede  |
| Personidentifikationsnummeret for arbejder | cdm_workerpersonidentificationnumber |  766704      |   Lukkede  |
| Personidentifikationstype for arbejder | cdm_workerpersonidentificationtype |        |     |
| Arbejdskalender | cdm_workcalendar |        |     |
| Arbejdskalenderdag | cdm_workcalendarday |        |     |
| Arbejdskalenderfridag |cdm_workcalendarholiday |        |     |
| Ferielinje i arbejdskalender | cdm_workcalendarholidayline |        |     |
| Tidsinterval i arbejdskalender | cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter) |        |     |
| Arbejderbankkonto | cdm_workerbankaccount |        |     |

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
