---
title: Konfigurer integration med Finance
description: I denne artikel beskrives de funktioner, der kan bruges i integration mellem Dynamics 365 Human Resources og Dynamics 365 Finance.
author: andreabichsel
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ac4c15b4dbf60f378ba325adedb377e12585481a
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889950"
---
# <a name="configure-integration-with-finance"></a>Konfigurere integration med Finance

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Hvis du vil integrere Dynamics 365 Human Resources med Dynamics 365 Finance, kan du bruge skabelonen Human Resources til Finance i [Dataintegrator](/powerapps/administrator/data-integrator). Skabelonen Human Resources til Finance aktiverer dataflow for job, stillinger og arbejdere. Skabelonen gør det muligt at overføre data fra Human Resources til Finance, men tillader ikke, at data overføres fra Finance til Human Resources.

![Integrationsflow fra Human Resources til Finance](./media/hr-admin-integration-finance-flow.png)

Human Resources til Finance-løsningen giver følgende typer datasynkronisering:

- Vedligehold job i Human Resources, og synkroniser dem fra Human Resources til Finance
- Vedligehold stillinger og stillingstildelinger i Human Resources, og synkroniser dem fra Human Resources til Finance
- Vedligehold ansættelser i Human Resources, og synkroniser dem fra Human Resources til Finance
- Vedligehold arbejdere og arbejderadresser i Human Resources, og synkroniser dem fra Human Resources til Finance

## <a name="system-requirements-for-human-resources"></a>Systemkrav til Human Resources

Integrationsløsningen kræver følgende versioner af Human Resources og Finance: 

- Dynamics 365 Human Resources på Dataverse
- Dynamics 365 Finance version 7.2 og nyere

## <a name="template-and-tasks"></a>Skabelon og opgaver

Sådan åbnes skabelonen Human Resources til Finance.

1. Åbn [Power Apps Administration](https://admin.powerapps.com/). 

2. Vælg **Projekter**, og vælg derefter **Nyt projekt** i øverste højre hjørne. Opret et nyt projekt for hver juridisk enhed, som du vil integrere i Finance.

3. Vælg **Human Resources (Dataverse for Human Resources til Finance)** for at synkronisere poster fra Human Resources til Finance.

Skabelonen bruger følgende underliggende opgaver til at synkronisere poster fra Human Resources til Finance:

- **Jobfunktioner til Kompensation – jobfunktion**
- **Afdelinger til driftsenhed**
- **Jobtyper til Kompensation – jobtype**
- **Job til job**
- **Job til Stillingsdetaljer**
- **Stillingstyper til stillingstype**
- **Jobstillinger til basisstilling**
- **Jobstillinger til stillingsoplysninger**
- **Jobstillinger til Stillingsvarighed**
- **Jobstillinger til Stillingshierarkier**
- **Arbejdere til arbejder**
- **Ansættelser til ansættelse**
- **Ansættelser til ansættelsesoplysninger**
- **Arbejdertildeling til medarbejderopgaver for stilling**
- **Arbejderadresser til arbejderens postadresse V2**

## <a name="template-mappings"></a>Tilknytninger af skabelon

I følgende tabeller med skabelontilknytninger indeholder opgavenavnet de enheder, der bruges i de enkelte programmer. Kilden (Human Resources) er i venstre side, og destinationen (Finance) er til højre.

### <a name="job-functions-to-compensation-job-function"></a>Jobfunktioner til Kompensation – jobfunktion

| Dataverse-tabel (kilde) | Enheden Finance (destination) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job  funktionsnavn)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | BESKRIVELSE   (BESKRIVELSE)                 |

### <a name="departments-to-operating-unit"></a>Afdelinger til driftsenhed

| Dataverse-tabel (kilde)           | Enheden Finance (destination) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAVN (NAVN)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Jobtyper til Kompensation – jobtype

| Dataverse-tabel (kilde)   | Enheden Finance (destination) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | BESKRIVELSE   (BESKRIVELSE)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Job til job

| Dataverse-tabel (kilde)                           | Enheden Finance (destination)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | BESKRIVELSE   (BESKRIVELSE)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Job til Stillingsdetaljer

| Dataverse-tabel (kilde)                             | Enheden Finance (destination) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Jobtype (Jobtypenavn))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Jobfunktion (Jobfunktionsnavn)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Standardfuldtidsækvivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Stillingstyper til stillingstype

| Dataverse-tabel (kilde)       | Enheden Finance (destination) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | BESKRIVELSE   (BESKRIVELSE)                 |
| cdm_classification   (cdm_classification) | KLASSIFIKATION   (KLASSIFIKATION)           |

### <a name="job-positions-to-base-position"></a>Jobstillinger til basisstilling

| Dataverse-tabel (kilde)           | Enheden Finance (destination) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Stillingsnummer) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Jobstillinger til stillingsoplysninger

| Dataverse-tabel (kilde)              | Enheden Finance (destination)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Stillingsnummer)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Job (Navn))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | BESKRIVELSE   (BESKRIVELSE)                       |
| cdm_departmentid.cdm_departmentnumber   (Afdeling (Afdelingsnavn)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Stillingstype (Navn))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Tilgængelig for tildeling)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Gyldig fra)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Gyldig til)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Fuldtidsækvivalent)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Jobstillinger til Stillingsvarighed

| Dataverse-tabel (kilde)             | Enheden Finance (destination) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Stillingsnummer)   | POSITIONID (POSITIONID)                      |
| Beregnet   Aktivering (Beregnet aktivering) | VALIDFROM (VALIDFROM)                        |
| Beregnet   Pension (Beregnet pension) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Jobstillinger til Stillingshierarkier

| Dataverse-tabel (kilde)        | Enheden Finance (destination) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Stillingsnummer)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Gyldig fra)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Gyldig til)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Arbejdere til arbejder
| Dataverse-tabel (kilde)           | Enheden Finance (destination)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | FØDSELSDATO   (FØDSELSDATO)                           |
| cdm_gender   (cdm_gender)                     | KØN (KØN)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Ansættelser til ansættelse

| Dataverse-tabel (kilde)                             | Enheden Finance (destination) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Ansættelser til ansættelsesoplysninger

| Dataverse-tabel (kilde)                             | Enheden Finance (destination)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Arbejdertildeling til medarbejderopgaver for stilling

| Dataverse-tabel (kilde)                             | Enheden Finance (destination)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Stillingsnummer)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Gyldig fra)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Gyldig til)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Arbejderadresser til arbejderens postadresse V2

| Dataverse-tabel (kilde)                             | Enheden Finance (destination)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Integrationsovervejelser

Ved integration fra Human Resources til Finance vil integrationen forsøge at sammenligne poster baseret på id'et. Hvis posterne stemmer overens, overskrive Dataintegrator dataene i Finance med værdierne i Human Resources. Der kan dog opstå et problem, hvis disse logisk er forskellige poster, og det samme id blev oprettet i enten Human Resources eller Finance baseret på den pågældende nummerserie.

Dette problem kan opstå for **Arbejder**, som bruger **Personalenummeret** til at foretage sammenligningen, og **Stillinger**. Der bruges ikke nummerserier til job. Det betyder, at hvis det samme job-id findes i både Human Resources og Finance, overskriver Human Resources-oplysningerne oplysningerne i Dynamics 365 Finance. 

Hvis du vil undgå problemer med identiske id'er, kan du enten føje et præfiks til [nummerserien](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) eller angive et startnummer på nummerserien, der ligger ud over området for det andet system. 

Det lokations-id, der bruges til en arbejderadresse, er ikke del af en nummerserie. Når en arbejders adresse integreres fra Human Resources til Finance, kan der blive oprettet en dublet af adresseposten, hvis arbejderadressen allerede findes i Finance. 

Følgende illustration viser et eksempel på en skabelontilknytning i Dataintegrator. 

![Tilknytning af skabelon](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]