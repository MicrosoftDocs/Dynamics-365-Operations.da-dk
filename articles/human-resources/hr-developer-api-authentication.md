---
title: Godkendelse
description: Denne artikel indeholder oversigtsoplysninger om, hvordan du kan godkende med API'en (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.
author: andreabichsel
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4e73438170294863b7aa092cf1fc027787f57c70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054374"
---
# <a name="authentication"></a><span data-ttu-id="bfd22-103">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="bfd22-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bfd22-104">Denne artikel indeholder oversigtsoplysninger om, hvordan du kan godkende med API'en (Application Programming Interface) for Microsoft Dynamics 365 Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="bfd22-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="bfd22-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="bfd22-105">Overview</span></span>

<span data-ttu-id="bfd22-106">Data-API'en til personale er en OData-implementering.</span><span class="sxs-lookup"><span data-stu-id="bfd22-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="bfd22-107">Du kan finde flere oplysninger i [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="bfd22-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="bfd22-108">Dit program skal godkendes som en godkendt kalder, før API'en vil behandle anmodninger fra dit program.</span><span class="sxs-lookup"><span data-stu-id="bfd22-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="bfd22-109">Grundlæggende</span><span class="sxs-lookup"><span data-stu-id="bfd22-109">Fundamentals</span></span>

<span data-ttu-id="bfd22-110">Hvis du vil kalde data-API'en, skal programmet hente et adgangstoken fra Microsoft-identitetsplatformen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="bfd22-111">Det pågældende adgangstoken indeholder oplysninger om dit program og den tilladelse, det skal kalde ressourcer i personale.</span><span class="sxs-lookup"><span data-stu-id="bfd22-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="bfd22-112">Adgangstoken</span><span class="sxs-lookup"><span data-stu-id="bfd22-112">Access token</span></span>

<span data-ttu-id="bfd22-113">Adgangstokens, der er udstedt af Microsoft-identitetsplatformen, er base64-kodede webtokens (JWT'er) af typen JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="bfd22-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="bfd22-114">De indeholder oplysninger (krav) om, at data-API'en (og andre web-API'er, der er sikret med Microsoft-identitetsplatformen) bruger til at validere kalderen og sikre, at kalderen har de korrekte tilladelser til at udføre den handling, de anmoder om.</span><span class="sxs-lookup"><span data-stu-id="bfd22-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="bfd22-115">Under opkald kan du behandle adgangstoken som uigennemsigtige.</span><span class="sxs-lookup"><span data-stu-id="bfd22-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="bfd22-116">Du bør altid overføre adgangstokens via en sikker kanal, f.eks. TLS (Transport Layer Security) og HTTPS (Hypertext Transfer Protocol Secure).</span><span class="sxs-lookup"><span data-stu-id="bfd22-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="bfd22-117">Her er et eksempel på et adgangstoken, der udstedes af Microsoft-identitetsplatformen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="bfd22-118">Hvis du vil kalde data-API'en, skal du tilknytte adgangstokenet som et bærertoken til godkendelsesheaderen i HTTP-anmodningen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="bfd22-119">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="bfd22-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="bfd22-120">Registrere et nyt program ved hjælp af Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="bfd22-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="bfd22-121">Log på [Microsoft Azure-portalen](https://portal.azure.com) med en arbejds- eller skolekonto eller en personlig Microsoft-konto.</span><span class="sxs-lookup"><span data-stu-id="bfd22-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="bfd22-122">Hvis din konto giver dig adgang til mere end én lejer, skal du vælge din konto i øverste højre hjørne og angive din portalsession til den Azure Active Directory (Azure AD)-lejer, du ønsker.</span><span class="sxs-lookup"><span data-stu-id="bfd22-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="bfd22-123">Vælg tjenesten **Azure Active Directory** i venstre rude, og vælg derefter **Appregistreringer \> Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="bfd22-124">Når siden **Registrer et program** vises, skal du angive dit programs registreringsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="bfd22-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="bfd22-125">**Navn**: Angiv et meningsfuldt programnavn, der vises for brugerne af appen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="bfd22-126">**Understøttede kontotyper**: Vælg de typer konti, som appen skal understøtte.</span><span class="sxs-lookup"><span data-stu-id="bfd22-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="bfd22-127">Understøttede kontotyper</span><span class="sxs-lookup"><span data-stu-id="bfd22-127">Supported account types</span></span> | <span data-ttu-id="bfd22-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bfd22-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="bfd22-129">Kun konti i denne organisationsmappe</span><span class="sxs-lookup"><span data-stu-id="bfd22-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="bfd22-130">Vælg denne indstilling, hvis du bygger et LOB-program (line-of-business).</span><span class="sxs-lookup"><span data-stu-id="bfd22-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="bfd22-131">Denne indstilling er ikke tilgængelig, medmindre du registrerer appen i en mappe.</span><span class="sxs-lookup"><span data-stu-id="bfd22-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="bfd22-132">Denne indstilling er knyttet **Azure AD kun én lejer**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="bfd22-133">Denne indstilling er standardindstillingen, medmindre du registrerer appen uden for en mappe.</span><span class="sxs-lookup"><span data-stu-id="bfd22-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="bfd22-134">I dette tilfælde er standardindstillingen **Azure AD flere lejere og personlige Microsoft-konti**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="bfd22-135">Konti i en hvilken som helst organisationsmappe</span><span class="sxs-lookup"><span data-stu-id="bfd22-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="bfd22-136">Vælg denne indstilling for at henvende dig til alle erhvervs- og undervisningskunder.</span><span class="sxs-lookup"><span data-stu-id="bfd22-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="bfd22-137">Denne indstilling er knyttet **Azure AD kun flere lejere**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="bfd22-138">Hvis du har registreret appen som **Azure AD kun én lejer**, kan du bruge bladet **Godkendelses** til at opdatere den til **Azure AD kun flere lejere** og derefter til **Azure AD kun én lejer** igen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="bfd22-139">Konti i alle organisationsmapper og personlige Microsoft-konti</span><span class="sxs-lookup"><span data-stu-id="bfd22-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="bfd22-140">Vælg denne indstilling for at henvende dig til det bredeste antal kunder.</span><span class="sxs-lookup"><span data-stu-id="bfd22-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="bfd22-141">Denne indstilling er knyttet til **Azure AD flere lejere og personlige Microsoft-konti**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="bfd22-142">Hvis du har registreret appen som **Azure AD flere lejere og personlige Microsoft-konti**, kan du ikke ændre denne indstilling på brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="bfd22-143">Du skal i stedet bruge programmanifesteditoren til at ændre de understøttede kontotyper.</span><span class="sxs-lookup"><span data-stu-id="bfd22-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="bfd22-144">**Omdirigerings-URI ( valgfrit)** – Vælg den type app, du bygger: **Web** eller **Offentlig klient (mobil og skrivebord**).</span><span class="sxs-lookup"><span data-stu-id="bfd22-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="bfd22-145">Angiv derefter omdirigerings-URI'en (eller svar-URL-adressen) til appen.</span><span class="sxs-lookup"><span data-stu-id="bfd22-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="bfd22-146">Angiv basis-URL-adressen til appen i forbindelse med webapps.</span><span class="sxs-lookup"><span data-stu-id="bfd22-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="bfd22-147">`http://localhost:31544` kan f.eks. være URL-adressen til en webapp, der kører på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="bfd22-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="bfd22-148">Brugere anvender derefter denne URL-adresse til at logge på en webklientapp.</span><span class="sxs-lookup"><span data-stu-id="bfd22-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="bfd22-149">For offentlige klientapps skal du angive den URI, som Azure AD bruger til at returnere tokensvar.</span><span class="sxs-lookup"><span data-stu-id="bfd22-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="bfd22-150">Angiv en værdi, der er specifik for din app, f.eks. `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="bfd22-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="bfd22-151">Hvis du vil have vist specifikke eksempler for webapps eller indbyggede apps, skal du se lynvejledningerne på [Microsoft-identitetsplatformen (tidligere Azure Active Directory for udviklere)](/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="bfd22-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="bfd22-152">Vælg **Tilføj en tilladelse** under **API-tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="bfd22-153">Derefter kan du søge efter **Dynamics 365 Human Resources** under fanen **API'er, som min organisation bruger** og føje tilladelsen **bruger\_repræsentation** til din app.</span><span class="sxs-lookup"><span data-stu-id="bfd22-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="bfd22-154">Program-id'et for personale er f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="bfd22-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="bfd22-155">Brug dette id til at sikre, at du har valgt det rette program.</span><span class="sxs-lookup"><span data-stu-id="bfd22-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="bfd22-156">Vælg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="bfd22-156">Select **Register**.</span></span>

   <span data-ttu-id="bfd22-157">[![Registrering af en ny app i Azure-portalen](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bfd22-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="bfd22-158">Azure AD tildeler et entydigt program-id (klient-id) til din app og fører dig til siden **Oversigt** for din app.</span><span class="sxs-lookup"><span data-stu-id="bfd22-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="bfd22-159">Hvis du vil føje flere egenskaber til din app, kan du vælge andre konfigurationsindstillinger, f.eks. indstillinger for mærkning og for certifikater og hemmeligheder.</span><span class="sxs-lookup"><span data-stu-id="bfd22-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="bfd22-160">Hente et adgangstoken</span><span class="sxs-lookup"><span data-stu-id="bfd22-160">Retrieving an access token</span></span>

<span data-ttu-id="bfd22-161">Hvordan du specifikt henter et adgangstoken til kald af data-API'en til personale, afhænger af, hvilke teknologier du bruger til at udvikle dit klientprogram.</span><span class="sxs-lookup"><span data-stu-id="bfd22-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="bfd22-162">Du kan f.eks. [afprøve et tredjepartsprogram](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (som f.eks. Postman), udvikle et C#-konsolprogram eller en webtjeneste eller bygge en javascript-/TypeScript-klient.</span><span class="sxs-lookup"><span data-stu-id="bfd22-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="bfd22-163">Eksempel på C#-klientprogram:</span><span class="sxs-lookup"><span data-stu-id="bfd22-163">Example C# client application:</span></span>
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

<span data-ttu-id="bfd22-164">Når du har hentet et adgangstoken, skal du overføre tokenet i godkendelsesheaderen som et bærertoken sammen med de enkelte anmodninger, du sender til data-API'en, som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="bfd22-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]