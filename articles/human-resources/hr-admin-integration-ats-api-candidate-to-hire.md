---
title: Kandidat, der kan ansættes
description: Dette emne beskriver den kandidat, der skal ansætte enhed i Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0ddf7bd403c926b231f9e010280083d1638b3ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795039"
---
# <a name="candidate-to-hire"></a>Kandidat, der kan ansættes

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver den kandidat, der skal ansætte enhed i Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmcandidatetohireentity

## <a name="description"></a>Beskrivelse

Denne enhed indeholder kandidatoplysninger, der bruges til at oprette en medarbejder i Dynamics 365 Human Resources. Den bruges til at læse alle kandidatposter og oprette interne og eksterne kandidatposter, så du kan oprette personlige oplysninger om den nye kandidat.

Når du opretter en ekstern kandidatpost, der skal være en ny personpost i systemet, skal du ikke definere et partnummer (person), som du bogfører en ny kandidatpost. Den nye personenhedspost oprettes med den nye kandidatpost.

Når du opretter en intern kandidatpost (en kandidat til den stilling, der allerede har en medarbejderpost i firmaet), skal du definere nummeret på parten (personen) for den post, der allerede findes for personen med den mshr_partynumber-egenskab på kandidatposten, i stedet for at definere de personlige oplysninger (f.eks. navn, køn eller fødselsdato), der skal bruges til at oprette en ny personpost.

## <a name="json-representation"></a>JSON-repræsentation

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Id for kandidat til ansættelsesenhed**<br>mshr_hcmcandidatetohireentityid<br>Guid | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Et systemgenereret entydigt id til enhedsposten. |
| **Kandidat-id**<br>mshr_candidateid<br>Streng | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Et entydigt id for enheden. |
| **Partnummer**<br>mshr_partynumber<br>Streng | Skrivebeskyttet<br>Påkrævet | Partens (person) nummer for kadidatens personpost. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>Guid | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid af mshr_direpersonentity | Det systemgenererede entydige id for partens (person) kandidatpost. |
| **Parttype**<br>mshr_partytype<br>mshr_dirpartytype indstilling | Skrivebeskyttet<br>Påkrævet | Postens parttype, som det er defineret i indstillingen til mshr_dirpartytype. For denne enhed vil typen altid være "Person". |
| **Rekrutteringsanmodnings-id**<br>mshr_recruitingrequestid<br>Streng | Skriv én gang<br>Valgfri | Refererer til den rekrutteringsanmodning, som kandidaten opfylder. |
| **Værdi for rekrutteringsanmodnings-id**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | Læse/skrive<br>Valgfri<br>Fremmed nøgle: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity | Det systemgenererede entydige id for rekrutteringsanmodningen, som kandidaten opfylder. |
| **Stillings-id**<br>mshr_positionid<br>Streng | Læse/skrive<br>Valgfri | Id for den stilling, som kandidaten tages i betragtning til. |
| **Stillings-id-værdi**<br>_mshr_fk_position_if_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmpositionv2entityid af mshr_hcmpositionv2entity | Systemgenereret id for den stilling, som kandidaten tages i betragtning til. |
| **Fornavn**<br>mshr_firstname<br>Streng | Læse/skrive<br>Påkrævet | Kandidatens fornavn. |
| **Mellemnavn**<br>mshr_middlename<br>Streng | Læse/skrive<br>Valgfri | Kandidatens mellemnavn. |
| **Præfiks for efternavn**<br>mshr_lastnameprefix<br>Streng | Læse/skrive<br>Valgfri | Præfiks for kandidatens efternavn. |
| **Efternavn**<br>mshr_lastname<br>Streng | Læse/skrive<br>Valgfri | Kandidatens efternavn. |
| **Køn**<br>mshr_gender<br>mshr_hcmpersongender indstilling | Læse/skrive<br>Valgfri | Kandidatens køn. |
| **Fødselsdato**<br>mshr_birthdate<br>Datetime | Læse/skrive<br>Valgfri | Kandidatens fødselsdato. |
| **Kode for statsborgerskab**<br>mshr_citizenshipcountrycode<br>Streng | Læse/skrive<br>Valgfri | Angiver, hvilket land kandidaten er statsborger i. Gyldige landekoder findes mshr_logisticaddresscountryregionentity. |
| **Veteranstatus-id**<br>mshr_veteranstatusid<br>Streng | Læse/skrive<br>Valgfri | Angiver veteranstatus for kandidaten. |
| **Værdi for veteranstatus-id**<br>_mshr_fk_veteranstatus_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmveteranstatusentityid of mshr_hcmveteranstatusentity | Systemgenereret entydig identifikation af enhedsposten for veteranstatus. |
| **Startdato for militærtjeneste**<br>mshr_militaryservicestartdate<br>Datetime | Læse/skrive<br>Valgfri | Startdatoen for kandidatens militærtjeneste. |
| **Slutdato for militærtjeneste**<br>mshr_militaryserviceenddate<br>Datetime | Læse/skrive<br>Valgfri | Slutdatoen for kandidatens militærtjeneste. |
| **Er handicappet veteran**<br>mshr_isdisabledveteran<br>mshr_noyes indstilling | Læse/skrive<br>Valgfri | Angiver om kandidaten har status af handicappet veteran. |
| **Dato for tilgængelighed**<br>mshr_availabilitydate<br>Datetime | Læse/skrive<br>Valgfri | Den første dato, hvor kandidaten er tilgængelig og kan arbejde. |
| **Er villig til at flytte**<br>mshr_iswillingtorelocate<br>mshr_noyes indstilling | Læse/skrive<br>Valgfri | Angiver, om kandidaten er villig til at flytte til stillingen. |
| **Bemærkninger**<br>mshr_comments<br>Streng | Læse/skrive<br>Valgfri | Kommentarer, der skal bruges af rekrutteringsmedarbejderen eller ansættelseschefen. |
| **Resultat af programintegration**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult indstilling | Læse/skrive<br>Påkrævet | Kandidatens status i ansættelsesprocessen i forbindelse med integrationen. |
| **Årsagskode-id for Ansæt ikke**<br>mshr_donothirereasoncodeid<br>Streng | Læse/skrive<br>Valgfri | Du kan vælge at angive en årsagskode, når status (resultat af programintegration) er angivet til "Ikke ansat". |
| **Værdi for årsagskode-id**<br>_mshr_fk_reasoncode_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmreasoncodeentityid of mshr_hcmreasoncodeentity entity | Systemgenereret entydig identifikation af årsagskoden **Ansæt ikke**. |
| **Dataområde-id**<br>mshr_dataareaid<br>Streng | Læse/skrive<br>Valgfri |  Angiver den juridiske enhed (regnskabet). |
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>Guid | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]