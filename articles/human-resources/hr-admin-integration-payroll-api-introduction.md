---
title: Introduktion til lønintegrations-API
description: Dette emne beskriver API til Dynamics 365 Human Resources-lønintegration.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058554"
---
# <a name="payroll-integration-api-introduction"></a>Introduktion til lønintegrations-API

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette dokument beskriver API til Dynamics 365 Human Resources-lønintegration. API muliggør strømlinet totalintegration mellem Human Resources og partnerlønsystemer. Den integrerede erfaring begynder i Human Resources med medarbejderprofil, løn og fradrag og oplysninger om bidrag. Når du ansætter en medarbejder og angiver de nødvendige profil- og lønoplysninger i Human Resources, trækkes disse oplysninger ind i lønsystemet, som skal bruges ved behandling af løn. Opdateringer, der er foretaget for medarbejderen eller lønoplysninger, trækkes også ind til brug i senere lønkørsler.

![Lønintegrationsflow](media/hr-admin-integration-payroll-api-introduction-flow.png)

Human Resources har følgende komponenter for at aktivere integrationen:

- Funktioner, der markerer en medarbejder som klar til løn
- En API til integration, der åbner op for de nye funktioner for integration af applikationer

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Denne API er baseret på Microsoft Dataverse (tidligere Common Data Service). Al RESTful interaktion med denne API sker via Microsoft Dataverse Web-API, der bruger OData. Denne API er et undersæt af Dataverse Web-API. Dataverse Web-API definerer egenskaber som f.eks. godkendelse, servicespecifikationer, batch, samtidighedsstyring og håndtering af fejl.

Yderligere generelle oplysninger om Microsoft Dataverse Web-API finder du i:

- [Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Brug Microsoft Dataverse Web-API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse-vejledning for udvikler](/powerapps/developer/data-platform)

Denne dokumentation inkluderer oplysninger og udviklervejledning til brug af Dataverse Web-API'en, herunder følgende emner:

- [Godkende med Microsoft Dataverse med Web-API'en](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Udføre handlinger ved hjælp af Web-API'en](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Bruge Postman med Web-API'en](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Bruge sporing af ændringer til at synkronisere data med eksterne systemer](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle tabeller i Dataverse Human Resources

Slutpunkterne for lønintegrations-API bruger funktionerne for den virtuelle Microsoft Dataverse-tabelplatform. Som standard anvendes de virtuelle tabeller og de tilknyttede API-slutpunkter ikke i Human Resources-miljøer, hvilket gør det muligt for organisationer at bestemme, hvilke OData-slutpunkter der vises for miljøet. Hvis du vil bruge API'en, skal de virtuelle tabeller for Human Resources-enhederne oprettes for miljøet.

Oplysninger om generering af virtuelle tabeller til API finder du i [Konfigurere Dataverse-virtuelle tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datamodel

I følgende diagram vises forholdene i API grafisk. Flere typer har fremmede nøgler til andre allerede eksisterende enheder i Human Resources, som ikke illustreres her. Dette dokument indeholder oplysninger om enheder, der er specifikke for scenarier til lønintegration. Men der er mange andre enheder i Dataverse Web-API til Human Resources, som også kan være relevante for din integration. Nogle af disse enheder refereres til i relationer med fremmede nøgler eller navigationsegenskaber.

![Lønintegration, API-datamodel](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a>Lønmedarbejder og relaterede enheder

Enheder:

- [Medarbejders løn](hr-admin-integration-payroll-api-payroll-employee.md)
- [Lønarbejderadresse](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Plan for fast løn](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Lønstillingsjob](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Lønstilling](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Se også

[Generere og gennemse lønenheder](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Konfigurere Human Resources-parametre](hr-setup-parameters.md)<br>
[Konfigurere delte Human Resources-parametre](hr-setup-shared-parameters.md)<br>
[Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Brug Microsoft Dataverse Web-API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]