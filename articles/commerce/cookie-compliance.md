---
title: Cookie-overholdelse
description: Dette emne beskriver overvejelser om cookie-overholdelse og de standardpolitikker, der er inkluderet i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088381"
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
| \_msdyn365___muid_                            | Bruges, hvis Eksperimenteren er aktiveret for miljøet. Anvendes som et bruger-id til eksperimentformål. |
| \_msdyn365___exp_                             | Bruges, hvis Eksperimenteren er aktiveret for miljøet. Bruges til at måle belastningsjustering for ydeevne.         |
| d365mkt                                       | Bruges, hvis placeringsbaseret registrering til sporing af en brugers IP-adresse til forslag til butiksplacering er aktiveret i Commerce-webstedsgeneratoren på **Webstedsindstillinger > Generelt > Aktivér placeringsbaseret butiksregistrering**.      |

Hvis en bruger vælger sociale medielinks på et websted, spores cookies i nedenstående tabel også i deres browser.


| Domæne                      | Cookie               | Betegnelse                                                  | Kildetekst                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Synkronisering af LinkedIn-annonce-id                                      | LinkedIn-feed og indsigtskode                                |
| .linkedin.com               | li_sugr                  | Browseridentifikator                                           | LinkedIn-indsigtskode, hvis IP-adressen ikke er i et angivet land |
| .linkedin.com               | BizographicsOptOut       | Angiver frameldingsstatus for tredjepartssporing.              | LinkedIn-gæstekontrolelementer og sider til framelding i branche           |
| .linkedin.com               | \_guid                    | Browseridentifikator for Google-annoncer.                            | LinkedIn-feed                                                |
| .linkedin.com               | li_oatml                 | Medlem af indirekte identifikator til konverteringssporing, omdirigering og analyser. | LinkedIn-annoncer og indsigtskoder                                |
| Forskellige førstepartsdomæner | li_fat_id                | Medlem af indirekte identifikator til konverteringssporing, omdirigering og analyser. | LinkedIn-annoncer og indsigtskoder                                |
| .adsymptotic.com            | U                        | Browseridentifikator                                           | LinkedIn-indsigtskode, hvis IP-adressen ikke er i et angivet land |
| .linkedin.com                | bcookie                  | Browser-id-cookie                                            | Anmodninger til LinkedIn                                         |
| .linkedin.com                | bscookie                 | Sikker browser-cookie                                        | Anmodninger til LinkedIn                                         |
| .linkedin.com               | lang                     | Angiver landestandard og standardsprog.                                 | Anmodninger til LinkedIn                                         |
| .linkedin.com                | lidc                     | Bruges til ruteplanlægning.                                             | Anmodninger til LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Adobe-målgruppeadministrator-cookie                                                     | Angiv til id-synkronisering                                              |
| .linkedin.com               | \_ga                      | Google Analytics-cookie                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics-cookie                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics-cookie                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Cookies indeholder bruger-id'et for den bruger, der aktuelt er logget på.  |   Facebook                                                           |
| .facebook.com               | datr                     | Bruges til at identificere den webbrowser, der bruges til at oprette forbindelse til Facebook uafhængigt af den bruger, der er logget på. | Facebook                                                             |
| .facebook.com               | wd                       | Gemmer dimensionerne i browservinduet og bruges af Facebook til at optimere gengivelsen af siden. | Facebook                                                             |
| .facebook.com               | xs                       | Et tocifret tal, der repræsenterer sessionsnummeret. Den anden del af værdien er en sessionshemmelighed. |  Facebook                                                            |
| .facebook.com               | fr                       | Indeholder en entydig browser og et bruger-id, der bruges til målrettet annoncering. |  Facebook                                                            |
| .facebook.com               | sb                       | Bruges til at forbedre Facebook-venneforslag.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Cookies indeholder bruger-id'et for den bruger, der aktuelt er logget på.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Cookies indeholder bruger-id'et for den bruger, der aktuelt er logget på.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Cookie indeholder sider, når brugeren vælger knappen Pinterest.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Cookie indeholder sider, når brugeren vælger knappen Pinterest.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Indeholder et bruger-id og tidsstempel for, hvornår cookien blev oprettet. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Cookie indeholder sider, når brugeren vælger knappen Pinterest.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Cookie indeholder sider, når brugeren vælger knappen Pinterest.      | Pinterest                                                             |
| .pinterest.com              | Lokalt lager            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Servicemedarbejdere          |                                                              |  Pinterest                                                            |


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
