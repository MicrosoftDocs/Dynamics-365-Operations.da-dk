---
title: Medarbejders løn
description: Denne artikel indeholder detaljer og en eksempelforespørgsel til objektet Lønmedarbejder i Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07fbc76b997600b2c076c00a63d1f6d865326d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872204"
---
# <a name="payroll-employee"></a>Medarbejders løn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver objektet Medarbejders løn for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollemployeeentity.

### <a name="description"></a>Betegnelse

Dette objekt indeholder oplysninger om medarbejderen. Du skal angive [parametrene for lønintegration](hr-admin-integration-payroll-api-parameters.md), før du bruger dette objekt.

>[!IMPORTANT] 
>Felterne **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** er ikke længere tilgængelige på denne enhed. Dette sikrer, at der kun findes én gyldighedsdato for datakilden, som understøtter denne enhed.
>Disse felter vil være tilgængelige på **DirPersonNameHistoricalEntity**, som blev udgivet i Platform-opdatering 43. Der er en OData-relation fra **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Id for juridisk enhed**</br>mshr_legalentityid</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Medarbejderens entydige personalenummer. |
| **Startdato for ansættelse**</br>mshr_employmentstartdate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Startdatoen for medarbejderens ansættelse. |
| **Slutdato for ansættelse**</br>mshr_employmentenddate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet |Slutdatoen for medarbejderens ansættelse.  |
| **Fødselsdato**</br>mshr_birthdate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Medarbejderens fødselsdato. |
| **Køn**</br>mshr_gender</br>[mshr_hcmpersongender indstilling](hr-admin-integration-payroll-api-gender.md) | Skrivebeskyttet | Medarbejderens køn. |
| **Medarbejdertype**</br>mshr_employmenttype</br>[Grupperet indstilling for mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Skrivebeskyttet | Ansættelsestype. |
| **Identifikationstype-id**</br>mshr_identificationtypeid</br>*Streng* |Skrivebeskyttet | Den identifikationstype, der er defineret for medarbejderen. |
| **Identifikationsnummer til**</br>mshr_identificationnumber</br>*Streng* | Skrivebeskyttet |Det identifikationsnummer, der er defineret for medarbejderen. |
| **Klar til at betale**</br>mshr_readytopay</br>[mshr_noyes indstilling](hr-admin-integration-payroll-api-no-yes.md) | Skrivebeskyttet | Angiver, om medarbejderen er markeret som klar til at betale. |
| **Lønmedarbejders enheds-id**</br>mshr_payrollemployeeentityid</br>*GUID* | Systemgenereret | En systemgenereret GUID-værdi (Global Unique Identifier), der identificerer medarbejderen entydigt. |

## <a name="relations"></a>Relationer

|Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Eksempelforespørgsel for lønmedarbejder

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Svar**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
