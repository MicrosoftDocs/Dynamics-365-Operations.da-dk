---
title: Eksempelforespørgsel til ansøger til ansættelse
description: Dette emne indeholder en eksempelforespørgsel til kandidaten, der skal ansættes en enhed i Dynamics 365 Human Resources.
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
ms.openlocfilehash: d2fc08586914fd3815b0da062f24d83ac550302f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467619"
---
# <a name="example-query-for-candidate-to-hire"></a>Eksempelforespørgsel til ansøger til ansættelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder en eksempelforespørgsel til kandidaten, der skal ansættes en enhed i Dynamics 365 Human Resources.

Dette emne viser et eksempel på, hvordan du kan bruge *dybdeindlæg* til at oprette alle detaljer til en ny kandidatpost med en enkelt API-handling. Du kan finde flere oplysninger om dybdeindlæg i [Oprette relaterede enhedsposter i én handling](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Enheden **mshr_hcmcandidatetohireentity** er entydig på grund af dens relation til enheden **mshr_dirpersonentity**. Mange af egenskaberne i **mshr_hcmcandidatetohireentity** (f.eks. **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) er afledt af posten **mshr_dirpersonentity** . Hvis du bogfører en ny kandidatpost for **mshr_hcmcandidatetohireentity** uden brug af dybdeindlæg, kan du definere værdier for disse egenskaber direkte i posten **mshr_hcmcandidatetohireentity**. Den tilknyttede post **mshr_dirpersonentity** oprettes uden tilknytning til de definerede værdier for egenskaberne. Du kan derefter oprette alle andre relaterede enhedsposter (f.eks. færdigheder eller uddannelse) som separate API-opkald.

Men hvis du vil bruge dybdeindlæg til at oprette alle relaterede enheder i én operation, skal de egenskaber, der er specifikke for **mshr_dirpersonentity**-enheden, være defineret på dette indlejrede niveau for handlingen.

Dette eksempel viser, hvordan du kan oprette en kandidatpost, posten for den tilknyttede person og personens færdigheder og uddannelse i tre indlejrede niveauer ved hjælp af dybdeindlæg i en enkelt API-handling.

> [!NOTE]
> Eksemplet indeholder ikke alle egenskaber for hver enkelt API-enheder. Det er forenklet til demonstrationsformål.

**Anmodning**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Svar**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]