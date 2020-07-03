---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446907"
---
# <a name="cookie-compliance"></a>Cookie-overholdelse

[!include [banner](includes/banner.md)]

Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Beskyttelse af personlige oplysninger er en vigtig faktor, når der gøres brug af sporingsteknologier, som påvirker e-handelskunder. På grund af standarderne for overholdelse af beskyttelse af personlige oplysninger, såsom den generelle forordning om databeskyttelse (GDPR) i Den Europæiske Union (EU), skal retningslinjer for elektronisk beskyttelse af personlige oplysninger tages i betragtning for alle websteder, der er aktive i dag. Da mange e-Commerce-websteder som standard er tilgængelige globalt, er det vigtigt, at du gennemgår overholdelsesstandarderne for dit e-Commerce-websted.

Hvis du vil vide mere om de grundlæggende principper, som Microsoft gør brug af for cookie-overholdelse, skal du besøge [Microsoft Trust Center](https://www.microsoft.com/trust-center). På dette websted kan du også få flere oplysninger om overholdelsesområder samt beskyttelse af personlige oplysninger.

I følgende tabel vises den aktuelle referenceliste over cookies, der er placeret efter Dynamics 365 Commerce-websteder.

| Cookie-navn                               | Brug                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Gem Microsoft Azure Active Directory-godkendelsescookies (Azure AD) for enkeltlogon (SSO). Gemmer krypterede hovedoplysninger om bruger (navn, efternavn, mail). |
| &#95;msdyn365___cart&#95;                           | Gem indkøbsvogn-id, der bruges til at hente en liste over produkter, der er føjet til forekomsten af indkøbskurv. |
| &#95;msdyn365___ucc&#95;                            | Samtykkesporing af cookie-overholdelse af angivne standarder.                          |
| ai_session                                  | Registrerer, hvor mange sessioner af brugeraktivitet der har omfattet visse sider og funktioner i appen. |
| ai_user                                     | Registrerer, hvor mange personer der har brugt appen og dens funktioner. Brugerne tælles ved hjælp af anonyme id'er. |
| b2cru                                       | Gemmer URL-adresser til omdirigering dynamisk.                              |
| JSESSIONID                                  | Bruges af betalings-connector Adyen til at lagre brugersession.       |
| OpenIdConnect.nonce.&#42;                       | Godkendelse                                               |
| x-ms-cpim-cache:.&#42;                          | Bruges til at vedligeholde anmodningstilstanden.                      |
| x-ms-cpim-csrf                              | CRSF-token (forfalskning af anmodning på tværs af websteder), der bruges til beskyttelse fra CRSF.     |
| x-ms-cpim-dc                                | Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver. |
| x-ms-cpim-rc.&#42;                              | Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver. |
| x-ms-cpim-slice                             | Bruges til at dirigere anmodninger til den relevante forekomst af produktionens godkendelsesserver. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Bruges til vedligeholdelse af SSO-sessionen.                        |
| x-ms-cpim-trans                             | Bruges til sporing af posteringer (antallet af åbne faner, der godkender mod et B2C-websted (Business-to-Consumer)), herunder den aktuelle postering. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilgængelighedsfunktioner og -egenskaber](accessibility.md)

[Oversigt over overholdelse](compliance-overview.md)

[Tilføje en side med politik om beskyttelse af personlige oplysninger](add-privacy-page.md)

[Erstatte bruger-id'er, der er tilknyttet sporede indholdsændringer](replace-IDs-tracked-changes.md)
