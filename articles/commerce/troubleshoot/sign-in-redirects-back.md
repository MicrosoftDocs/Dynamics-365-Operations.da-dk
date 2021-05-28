---
title: Log på link igen til et e-handelswebsted
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når et link, der logges på, omdirigeres tilbage til e-handelswebstedet i stedet for at gå til siden, hvor det logges på.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020597"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="75751-103">Log på link igen til et e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="75751-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75751-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når et link, der logges på, omdirigeres tilbage til e-handelswebstedet i stedet for at gå til siden, hvor det logges på.</span><span class="sxs-lookup"><span data-stu-id="75751-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="75751-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="75751-105">Description</span></span>

<span data-ttu-id="75751-106">Når du har konfigureret en ny Microsoft Azure Active Directory B2C-lejer (Azure AD-B2C) i Commerce-webstedsgenerator, bliver de brugere, der vælger **Log på**-linket, omdirigeret tilbage til den primære e-commerce-landingsside uden at gå til logonsiden.</span><span class="sxs-lookup"><span data-stu-id="75751-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="75751-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="75751-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="75751-108">Bekræft, at svar-URL-adressen er konfigureret korrekt i Azure AD B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="75751-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="75751-109">Bekræft, at svarets URS-adresse er konfigureret korrekt i Azure AD B2C-programmet ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="75751-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="75751-110">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="75751-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="75751-111">Vælg det Azure AD B2C-program, du har oprettet til adgangen til dit websted.</span><span class="sxs-lookup"><span data-stu-id="75751-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="75751-112">Vælg det program, du oprettede i Azure AD B2C-opsætningen.</span><span class="sxs-lookup"><span data-stu-id="75751-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="75751-113">Under **Svar URL-adresse** skal du sørge for, at listen indeholder poster for både URL-adressen for webstedets domæne og den URL-adresse, der genereres af e-handel, som vist i eksemplet i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="75751-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C Svar til URL-adresseindgange](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="75751-115">Både URL-adressen til webstedet og den url-adresse, der genereres ved e-handel, skal være i et gyldigt URL-format, der ikke inkluderer foranstillede eller efterfølgende skråstreger.</span><span class="sxs-lookup"><span data-stu-id="75751-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75751-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="75751-116">Additional resources</span></span>

[<span data-ttu-id="75751-117">Registrer en webstedsansøgning i Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="75751-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="75751-118">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="75751-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)