---
title: Sammenligning af funktioner i skyen og i det lokale miljø
description: Emnet viser, hvilke funktioner der understøttes i skyen og lokalt.
author: sericks007
manager: AnnBe
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 309131f0d7390288a46f84b1375bd87922407159
ms.sourcegitcommit: a017fc0583a894382b959e22511231dd07d4254a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959888"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Sammenligning af funktioner i skyen og i det lokale miljø

[!include [banner](../includes/banner.md)]

Dette emne viser en sammenligning af funktioner, der er tilgængelige i skyen, med on-premises for følgende programmer:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Oplysninger om [udviklings- og administrationsfunktionerne](cloud-prem-comparison.md#development-and-administration-features) er også medtaget.

I følgende tabel vises programområderne. Understøttelse af skyen og lokalt er angivet for funktionen som helhed. Hvis der er specifikke funktioner, som afviger fra det overordnede område, er funktionerne angivet på en separat linje i kolonnen Funktion.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Areal**             | **Funktion**                | **Sky** | **I det lokale miljø** |
|---------------------|-----------------------------|-----------|-----------------|
| Overholdelse og certificeringer        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1-certificering                                                                | Ja       | Nr.              |
| Datastyring og -integration      |                                                                                           | Ja       | Ja             
|                                      | Eksportere data til dit eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport af trinvise opdateringer til en dataenhed                                 | Ja       | Ja              |
|                                      | Dataintegrationer                                                                         | Ja       | Ja             |
| Dokumentstyring                  |                                                                                           | Ja       | Ja             |
| Økonomistyring                 |                                                                                           | Ja       | Ja             |
| Hjælp                                 |                                                                                           | Ja       | Nej              |
| Personale                      |                                                                                           | Ja       | Ja             |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronisk rapportering (ER)                                                                 | Ja       | Ja             |
|                                      | ER: integration med LCS                                                                  | Ja       | Nr.              |
|                                      | ER: integration med SharePoint                                                           | Ja       | Nr.              |
|                                      | ER: integration med Regulatory Configuration Services (RCS)                              | Ja       | Nr.              |
|                                      | ER: anvender lokalt filsystem til at lagre ER-konfigurationer, der kan tilgås via ER-lagre | Ingen        | Ja             |
|                                      | Integration med PowerBI.com                                                              | Ja       | Ingen              |
|                                      | Integration med Power BI Desktop                                                          | Ingen        | Ja             |
|                                      | Analytiske arbejdsområder                                                                     | Ja       | Ingen              |
|                                      | Intelligent forretningsproces: anbefalinger                                             | Ja       | Nr.              |
|                                      | Udarbejde Power BI-rapporter med OData ved hjælp af Power BI Desktop eller funktioner i Excel PowerQuery    | Ja       | Nr.              |
|                                      | SQL Server Reporting Services (SSRS) understøtter udskalering                                 | Ja       | Nr.              |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Nr.              |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Forretningsprocesser, der kan konfigureres                                                           | Ja       | Nr.              |
| Lokaliseringer                        |                                                                                           | Ja       | Ja             |
| Mobilapp, arbejdsområder og platform |                                                                                           | Ja       | Ja             |
| Office-integration                   |                                                                                           | Ja       | Ja             |
| Organisationsadministration          |                                                                                           | Ja       | Ja             |
| Løn                              |                                                                                           | Ja       | Ja             |
|                                      | Direkte indbetaling                                                                            | Ja       | Nr.              |
| Projektstyring og regnskab    |                                                                                           | Ja       | Ja             |
| Sikkerhed                             |                                                                                           | Ja       | Ja             |
| Servicestyring                   |                                                                                           | Ja       | Ja             |
| Webklient                           |                                                                                           | Ja       | Ja             |
|                                      | Arbejdsrutineoptager - gemme eller indlæse opgaveregistreringer fra BPM-biblioteket                         | Ja       | Nej              |
| Support                              |                                                                                           | Ja       | Ja             |
|                                      | Adgang til support via menuen Hjælp og Support                                             | Ja       | Nr.              |
|                                      | Forretningshændelser                                                                           | Ja       | Ja (enten er internetforbindelse påkrævet, eller brugerdefinerede slutpunkter skal implementeres for at sende/modtage forretningshændelser via intranet)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Areal**                | **Funktion**             | **Sky** | **I det lokale miljø** |
|-------------------------|-------------------|-----------|-----------------|
| Aktivstyring                     |                                                                                           | Ja       | Ingen |
| Overholdelse og certificeringer        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1-certificering                                                                | Ja       | Nr.              |
| Omkostningsregnskab                      |                                                                                           | Ja       | Ja             |
|                                      | Indholdspakke om driftsregnskab til Power BI                                                 | Ja       | Nr.              |
|                                      | Appen Driftsregnskabsarbejdsområde til mobil                                                  | Ja       | Nr.              |
| Omkostningsstyring                      |                                                                                           | Ja       | Ja             |
|                                      | Indholdspakke for Power BI til omkostningsstyring                                                 | Ja       | Nr.              |
| Datastyring og -integration      |                                                                                           | Ja       | Ja             |
|                                      | Konfigurationsdrevet udvidelse                                                            | Ja       | Nej              |
|                                      | Eksportere data til dit eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport af trinvise opdateringer til en dataenhed                                 | Ja       | Ja              |
|                                      | Dataintegrationer                                                                         | Ja       | Ja             |
| Dokumentstyring                  |                                                                                           | Ja       | Ja             |
| Hjælp                                 |                                                                                           | Ja       | Nr.              |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronisk rapportering (ER)                                                                 | Ja       | Ja             |
|                                      | ER: integration med LCS                                                                  | Ja       | Nr.              |
|                                      | ER: integration med SharePoint                                                           | Ja       | Nr.              |
|                                      | ER: integration med Regulatory Configuration Services (RCS)                              | Ja       | Nr.              |
|                                      | ER: anvender lokalt filsystem til at lagre ER-konfigurationer, der kan tilgås via ER-lagre | Ingen        | Ja             |
|                                      | Integration med PowerBI.com                                                              | Ja       | Ingen              |
|                                      | Integration med Power BI Desktop                                                          | Ingen        | Ja             |
|                                      | Analytiske arbejdsområder                                                                     | Ja       | Ingen              |
|                                      | Intelligent forretningsproces: anbefalinger                                             | Ja       | Nr.              |
|                                      | Udarbejde Power BI-rapporter med OData ved hjælp af Power BI Desktop eller funktioner i Excel PowerQuery    | Ja       | Nr.              |
|                                      | SQL Server Reporting Services (SSRS) understøtter udskalering                                 | Ja       | Nej              |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Nej              |
| Lagerstyring                 |                                                                                           | Ja       | Ja             |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Forretningsprocesser, der kan konfigureres                                                           | Ja       | Nej              |
| Lokaliseringer                        |                                                                                           | Ja       | Ja             |
| Produktion                        |                                                                                           | Ja       | Ja             |
| Varedisponering og prognose      |                                                                                           | Ja       | Ja             |
| Planlægningsoptimering                |                                                                                           | Ja       | Ingen              |
| Mobilapp, arbejdsområder og platform |                                                                                           | Ja       | Ja             |
| Office-integration                   |                                                                                           | Ja       | Ja             |
| Organisationsadministration          |                                                                                           | Ja       | Ja             |
| Indkøb og forsyning             |                                                                                           | Ja       | Ja             |
|                                      | Kobling til eksternt katalog for indkøbsrekvisitioner                                   | Ja       | Nr.              |
|                                      | Power BI-rapporter for købsforbrugsanalyse                                                  | Ja       | Nr.              |
| Administration af produktoplysninger       |                                                                                           | Ja       | Ja             |
| Produktmasterdata                  |                                                                                           | Ja       | Ja             |
| Produktion                           |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for produktionsperformance                                                   | Ja       | Nr.              |
| Projektstyring og regnskab    |                                                                                           | Ja       | Ja             |
| Salg                                |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for salgs- og rentabilitetsperformance                                      | Ja       | Nr.              |
| Sikkerhed                             |                                                                                           | Ja       | Ja             |
| Servicestyring                   |                                                                                           | Ja       | Ja             |
| Administration af leveringskæde              |                                                                                           | Ja       | Ja             |
| Transportstyring            |                                                                                           | Ja       | Ja             |
| Kreditorsamarbejde                 |                                                                                           | Ja       | Nr.              |
| Lagerstedsstyring                 |                                                                                           | Ja       | Ja             |
|                                      | Lagerstedsapp til mobil                                                                      | Ja       | Ja             |
|                                      | Power BI-lagerstedsrapporter                                                              | Ja       | Nr.              |
| Webklient                           |                                                                                           | Ja       | Ja             |
|                                      | Arbejdsrutineoptager - gemme eller indlæse opgaveregistreringer fra BPM-biblioteket                         | Ja       | Nej              |
| Support                              |                                                                                           | Ja       | Ja             |
|                                      | Adgang til support via menuen Hjælp og Support                                             | Ja       | Nr.              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Du kan se en liste over funktioner, der er tilgængelige i lokale installationer, i [Commerce-egenskaber, der er tilgængelige i lokale installationer](../../../retail/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Areal**         | **Funktion**         | **Sky** | **I det lokale miljø** |
|------------------|---------------------|-----------|-----------------|
| Alle personaleområder | Alle personalefunktioner | Ja       | Nr.              |

## <a name="development-and-administration-features"></a>Udviklings- og administrationsfunktioner

| **Areal**                   | **Funktion**                               | **Sky** | **I det lokale miljø** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Opbygge og teste             |                                           | Ja       | Ja             |
| Udvidelsesmuligheder              |                                           | Ja       | Ja             |
| Overvågning og telemetri   |                                           | Ja       | Ja             |
| Platformkompatibilitet     |                                           | Ja       | Ja             |
| Servicering                  |                                           | Ja       | Ja             |
|                            | Service af miljøer                    | Ja       | Ingen              |
| Sporingsparser               |                                           | Ja       | Ja             |
| PerfTimer                  |                                           | Ja       | Ja\*           |
| Opgrader                    |                                           | Ja       | Ja             |
|                            | Opgrader                                   | Ja       | Ingen              |
|                            | Opgradering og understøttelse af tidligere versioner | Ja       | Ingen              |
| Visual Studio-udvikling  |                                           | Ja       | Ja             |

\* I lokale miljøer viser PerfTimer kun resultater for klienten.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]