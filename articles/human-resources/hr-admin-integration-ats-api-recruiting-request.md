---
title: Rekrutteringsanmodning
description: Dette emne beskriver rekrutteringsforespørgselsenheden til Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b89d257e3874ad7395c0a2c02f259c2f063aa8d0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500616"
---
# <a name="recruiting-request"></a>Rekrutteringsanmodning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver rekrutteringsforespørgselsenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Beskrivelse

Beskriver en anmodning om at rekruttere til et job.

### <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Rekrutteringsanmodnings-id**<br>mshr_recruitingrequestid<br>*Streng* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Et entydigt id, der kan læses af brugeren, for den anmodning, der vises i HR-ansøgningen. Nummerserie. |
| **Rekrutteringsanmodningsenheds-id**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer rekrutteringsanmodningen. |
| **Dataområde-id**<br>mshr_dataareaid<br>*Streng* | Læse/skrive<br>Valgfri<br> | Angiver den juridiske enhed (firmaet) for rekrutteringsanmodningen. |
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden) til rekrutteringsanmodningen. |
| **Ansætter chef for personalenummer**<br>mshr_hiringmanagerpersonnelnumber<br>*Streng* | Læse/skrive<br>Valgfri | Personalenummeret på den ansættelseschef, der er tilknyttet denne rekrutteringsanmodning. |
| **Værdi for ansættelseschef-id**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmworkerbaseentityid af mshr_hcmworkerbaseentity-enhed | Systemgenereret GUID-værdi til identifikation af den chef, der er knyttet til rekrutteringsanmodningen. |
| **Nummer på rekrutteringspart**<br>mshr_recruiterpartynumber<br>*Streng* | Læse/skrive<br>Valgfri | Persons (part) nummer for den rekrutteringsmedarbejder, der er valg til anmodningen. |
| **Værdi for rekrutterings-id**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_dirpersonentityid af mshr_dirpersonentity-enhed | Systemgenereret GUID-værdi til identifikation af den rekrutteringsmedarbejder, der er knyttet til rekrutteringsanmodningen. |
| **Status**<br>mshr_status<br>*Indstillingen RekrutteringRequestStatus* | Læse/skrive<br>Påkrævet<br> | Angiver status for rekrutteringsanmodning. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskriver anmodningen. |
| **Lokation-id for rekrutteringsanmodning**<br>mshr_recruitingrequestlocationid<br>*Streng* | Læse/skrive<br>Valgfri | Det brugerdefinerede entydige id for den joblokation, der er tilknyttet denne anmodning. |
| **Rekrutteringsværdi for lokation-id**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmrecruitingrequestlocationentityid af mshr_hcmrecruitingrequestlocationentity-enhed | Systemgenereret GUID-værdi til identifikation af den lokation til rekrutteringsanmodning, der er knyttet til anmodningen. |
| **Bemærkninger**<br>mshr_comments<br>*Streng* | Læse/skrive<br>Valgfri | Kommentarer om anmodningen om brug af ansættelse af ledere og rekrutteringsmedarbejdere. |
| **Job ID**<br>mshr_jobid<br>*Streng* | Skriv én gang<br>Påkrævet |   Det brugerdefinerede entydige id for det job, der deles af alle positioner, der er tilknyttet denne anmodning. |
| **Job-id-værdi**<br>_mshr_fk_job_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmjobentityid af mshr_hcmjobentity-enhed | Det systemgenererede entydige id for det job, der deles af alle positioner, der er tilknyttet denne rekrutteringsanmodning. |
| **Titel-id**<br>mshr_titleid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Det brugerdefinerede entydige id for den jobtitel, der er tilknyttet denne anmodning. |
| **Titel-id-værdi**<br>_mshr_fk_title_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmtitleid af mshr_hcmtitleentity-enhed | Det systemgenererede entydige id for titlen til det job, der er valgt til rekrutteringsanmodningen. |
| **Jobfunktion-id**<br>mshr_jobfunctionid<br>*Streng* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_jobfunctionid af mshr_hcmjobfunctionentity-enhed | Det brugerdefinerede entydige id for den jobfunktion, der er tilknyttet denne anmodning. |
| **Standardfuldtidsækvivalent**<br>mshr_defaultfulltimeequivalency<br>*Dobbelt* | Skrivebeskyttet<br>Påkrævet | Den værdi, der svarer i værdi til jobbet, hvor 1,0 repræsenterer en fuldtidsmedarbejder. |
| **Lovpligtig jobkategori**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory*-indstillingen | Skrivebeskyttet<br>Valgfri | EEO-jobkategorien for den jobfunktion, der er valgt til jobbet. Gyldige værdier, der er medtaget i indstillingen HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **Jobtype-id**<br>mshr_jobtypeid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Den type job, der er tilknyttet stillingen. Jobtyperne er brugerdefinerede værdier, som er tilgængelige i mshr_hcmjobtypeentity-enheden. |
| **Jobtype-værdi**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmjobtypeentityid af mshr_hcmjobtypenentity-enhed | Det systemgenererede entydige id for den jobtype, der er tilknyttet jobbet med rekrutteringsanmodningen. |
| **Momsfri status**<br>mshr_exemptstatus<br>*JobExemptStatus*-indstilling | Skrivebeskyttet<br>Valgfri | FLSA-status, der er momsfri, baseret på jobtypen. |
| **Anslået startdato**<br>mshr_estimatedstartdate<br>*Dato* | Læse/skrive<br>Påkrævet | Den dato, hvor det forventes, at en kandidat vil starte med at arbejde. |
| **Ekstern beskrivelse**<br>mshr_externaldescription<br>*Streng* | Læse/skrive<br>Valgfri | En ansøgerbeskrivelse af jobbet/stillingen. | 
| **Laveste kompensationsgrænse**<br>mshr_compensationlowthreshold<br>*Dobbelt* | Læse/skrive<br>Valgfri | nedre grænse for kompensationsniveauet. |
| **Kompensationskontrolpunkt**<br>mshr_compensationcontrolpoint<br>*Dobbelt* | Læse/skrive<br>Valgfri | Kontrolpunkt for kompensationsniveauet. |
| **Højeste kompensationsgrænse**<br>mshr_compensationhighthreshold<br>*Dobbelt* | Læse/skrive<br>Valgfri | Øvre grænse for kompensationsniveauet. |
| **Kompensationsniveau**<br>mshr_compensationlevelid<br>*Streng* | Læse/skrive<br>Valgfri | Jobbets kompensationsniveau. Et job kan konfigureres med flere kompensationsniveauer. Denne attribut angiver det valgte jobkompensationsniveau for denne anmodning. |
| **Jobkompensations-id**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmjobcompensationentityid af mshr_hcmjobcompensationentity-enhed | Systemgenererede entydige id for det kompensationsniveau, der er tilknyttet jobbet med rekrutteringsanmodningen. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
