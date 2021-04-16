---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796021"
---
# <a name="cookie-compliance"></a>Cookieoverholdelse

[!include [banner](includes/banner.md)]

Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.

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

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookie-samtykke på websted for bruger af et e-handels-websted 

Hvis et e-handels-websteds funktion eller modul bruger en ikke-afgørende cookie, skal en webstedsbrugers samtykke anskaffes, før cookien registreres. Hvis brugere af webstederne skal kunne give samtykke på e-handels-webstedet, skal en websteds forfatter tilføje og konfigurere et cookie-samtykkemodul i sidens sidehovedmodul for at sikre, at samtykke efterspørges og modtages. Brugersamtykke til webstedet skal gives, før en funktion eller et modul, der bruger en ikke-afgørende cookie, kan gengives på en webside.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilgængelighedsfunktioner og -egenskaber](accessibility.md)

[Oversigt over overholdelse](compliance-overview.md)

[Tilføje en side med politik om beskyttelse af personlige oplysninger](add-privacy-page.md)

[Erstatte bruger-id'er, der er knyttet til sporede indholdsændringer](replace-IDs-tracked-changes.md)

[Cookie-samtykkemodul](cookie-consent-module.md) 
 
[Overskriftsmodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
