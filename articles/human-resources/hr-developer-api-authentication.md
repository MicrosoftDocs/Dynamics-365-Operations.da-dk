---
title: Godkendelse
description: Denne artikel indeholder oversigtsoplysninger om, hvordan du kan godkende med API'en (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f09e9f9e19c5a59918e2801f6d25f72bee090a2b
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534183"
---
# <a name="authentication"></a>Godkendelse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel indeholder oversigtsoplysninger om, hvordan du kan godkende med API'en (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.

## <a name="overview"></a>Oversigt

Data-API'en til personale er en OData-implementering. Du kan finde flere oplysninger i [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Dit program skal godkendes som en godkendt kalder, før API'en vil behandle anmodninger fra dit program.

## <a name="fundamentals"></a>Grundlæggende

Hvis du vil kalde data-API'en, skal programmet hente et adgangstoken fra Microsoft-identitetsplatformen. Det pågældende adgangstoken indeholder oplysninger om dit program og den tilladelse, det skal kalde ressourcer i personale.

### <a name="access-token"></a>Adgangstoken

Adgangstokens, der er udstedt af Microsoft-identitetsplatformen, er base64-kodede webtokens (JWT'er) af typen JavaScript Object Notation (JSON). De indeholder oplysninger (krav) om, at data-API'en (og andre web-API'er, der er sikret med Microsoft-identitetsplatformen) bruger til at validere kalderen og sikre, at kalderen har de korrekte tilladelser til at udføre den handling, de anmoder om. Under opkald kan du behandle adgangstoken som uigennemsigtige. Du bør altid overføre adgangstokens via en sikker kanal, f.eks. TLS (Transport Layer Security) og HTTPS (Hypertext Transfer Protocol Secure).

Her er et eksempel på et adgangstoken, der udstedes af Microsoft-identitetsplatformen.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Hvis du vil kalde data-API'en, skal du tilknytte adgangstokenet som et bærertoken til godkendelsesheaderen i HTTP-anmodningen. Her er et eksempel.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Registrere et nyt program ved hjælp af Azure-portalen

1. Log på [Microsoft Azure-portalen](https://portal.azure.com) med en arbejds- eller skolekonto eller en personlig Microsoft-konto.

2. Hvis din konto giver dig adgang til mere end én lejer, skal du vælge din konto i øverste højre hjørne og angive din portalsession til den Azure Active Directory (Azure AD)-lejer, du ønsker.

3. Vælg tjenesten **Azure Active Directory** i venstre rude, og vælg derefter **Appregistreringer \> Ny registrering**.

4. Når siden **Registrer et program** vises, skal du angive dit programs registreringsoplysninger:

    - **Navn**: Angiv et meningsfuldt programnavn, der vises for brugerne af appen.
    - **Understøttede kontotyper**: Vælg de typer konti, som appen skal understøtte.

        | Understøttede kontotyper | Beskrivelse |
        |-------------------------|-------------|
        | Kun konti i denne organisationsmappe | Vælg denne indstilling, hvis du bygger et LOB-program (line-of-business). Denne indstilling er ikke tilgængelig, medmindre du registrerer appen i en mappe.<p>Denne indstilling er knyttet **Azure AD kun én lejer**.</p><p>Denne indstilling er standardindstillingen, medmindre du registrerer appen uden for en mappe. I dette tilfælde er standardindstillingen **Azure AD flere lejere og personlige Microsoft-konti**.</p> |
        | Konti i en hvilken som helst organisationsmappe | Vælg denne indstilling for at henvende dig til alle erhvervs- og undervisningskunder.<p>Denne indstilling er knyttet **Azure AD kun flere lejere**.</p><p>Hvis du har registreret appen som **Azure AD kun én lejer**, kan du bruge bladet **Godkendelses** til at opdatere den til **Azure AD kun flere lejere** og derefter til **Azure AD kun én lejer** igen.</p> |
        | Konti i alle organisationsmapper og personlige Microsoft-konti | Vælg denne indstilling for at henvende dig til det bredeste antal kunder.<p>Denne indstilling er knyttet til **Azure AD flere lejere og personlige Microsoft-konti**.</p><p>Hvis du har registreret appen som **Azure AD flere lejere og personlige Microsoft-konti**, kan du ikke ændre denne indstilling på brugergrænsefladen. Du skal i stedet bruge programmanifesteditoren til at ændre de understøttede kontotyper.</p> |

    - **Omdirigerings-URI ( valgfrit)** – Vælg den type app, du bygger: **Web** eller **Offentlig klient (mobil og skrivebord**). Angiv derefter omdirigerings-URI'en (eller svar-URL-adressen) til appen.

        - Angiv basis-URL-adressen til appen i forbindelse med webapps. `http://localhost:31544` kan f.eks. være URL-adressen til en webapp, der kører på din lokale computer. Brugere anvender derefter denne URL-adresse til at logge på en webklientapp.
        - For offentlige klientapps skal du angive den URI, som Azure AD bruger til at returnere tokensvar. Angiv en værdi, der er specifik for din app, f.eks. `myapp://auth`.

        Hvis du vil have vist specifikke eksempler for webapps eller indbyggede apps, skal du se lynvejledningerne på [Microsoft-identitetsplatformen (tidligere Azure Active Directory for udviklere)](/azure/active-directory/develop/#quickstarts).

5. Vælg **Tilføj en tilladelse** under **API-tilladelser**. Derefter kan du søge efter **Dynamics 365 Human Resources** under fanen **API'er, som min organisation bruger** og føje tilladelsen **bruger\_repræsentation** til din app. Program-id'et for personale er f9be0c49-aa22-4ec6-911a-c5da515226ff. Brug dette id til at sikre, at du har valgt det rette program.

6. Vælg **Registrer**.

   [![Registrering af en ny app i Azure-portalen.](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD tildeler et entydigt program-id (klient-id) til din app og fører dig til siden **Oversigt** for din app. Hvis du vil føje flere egenskaber til din app, kan du vælge andre konfigurationsindstillinger, f.eks. indstillinger for mærkning og for certifikater og hemmeligheder.

## <a name="retrieving-an-access-token"></a>Hente et adgangstoken

Hvordan du specifikt henter et adgangstoken til kald af data-API'en til personale, afhænger af, hvilke teknologier du bruger til at udvikle dit klientprogram. Du kan f.eks. [afprøve et tredjepartsprogram](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (som f.eks. Postman), udvikle et C#-konsolprogram eller en webtjeneste eller bygge en javascript-/TypeScript-klient.

Eksempel på C#-klientprogram:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

Når du har hentet et adgangstoken, skal du overføre tokenet i godkendelsesheaderen som et bærertoken sammen med de enkelte anmodninger, du sender til data-API'en, som beskrevet ovenfor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
