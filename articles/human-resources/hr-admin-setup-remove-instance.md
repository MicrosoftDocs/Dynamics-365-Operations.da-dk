---
title: Fjerne en forekomst
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008439"
---
# <a name="remove-an-instance"></a><span data-ttu-id="8a0f7-102">Fjerne en forekomst</span><span class="sxs-lookup"><span data-stu-id="8a0f7-102">Remove an instance</span></span>

<span data-ttu-id="8a0f7-103">Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="8a0f7-104">Fjerne et testdrevmiljø</span><span class="sxs-lookup"><span data-stu-id="8a0f7-104">Remove a test drive environment</span></span>

<span data-ttu-id="8a0f7-105">Testdrev til Personale er klargjort med en 60-dages udløbspolitik.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="8a0f7-106">Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="8a0f7-107">Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="8a0f7-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8a0f7-108">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-108">Select **Environments**.</span></span>
3. <span data-ttu-id="8a0f7-109">Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="8a0f7-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="8a0f7-110">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="8a0f7-111">Det eksisterende testdrevmiljø fjernes.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="8a0f7-112">Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="8a0f7-113">Fjerne et produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="8a0f7-113">Remove a production environment</span></span>

<span data-ttu-id="8a0f7-114">Det antages i artiklen, at du har købt Personale via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="8a0f7-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="8a0f7-115">Da der er indeholdt et enkelt Personale-miljø i hvert enkelt Power Apps-miljø, er der to indstillinger, der skal overvejes.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="8a0f7-116">Den første indstilling omfatter fjernelse af hele Power Apps-miljøet, den anden mulighed omfatter kun fjernelse af Personale.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="8a0f7-117">Den første indstilling foretrækkes, når du har oprettet et Power Apps-miljø udtrykkeligt med henblik på klargøring af Personale, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="8a0f7-118">Den anden mulighed er kun relevant, når du har et etableret Power Apps-miljø, der er udfyldt med omfattende data, som udnyttes i Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="8a0f7-119">Før du fjerner Power Apps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Personale.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="8a0f7-120">Bemærk også, at Power Apps-standardmiljøerne ikke kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="8a0f7-121">Sådan fjernes hele Power Apps-miljøet, herunder Personale og de tilknyttede apps og flows:</span><span class="sxs-lookup"><span data-stu-id="8a0f7-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="8a0f7-122">Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="8a0f7-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8a0f7-123">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-123">Select **Environments**.</span></span>
3. <span data-ttu-id="8a0f7-124">Vælg det miljø, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="8a0f7-125">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="8a0f7-126">Vent, indtil sletningen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="8a0f7-127">Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Personale.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="8a0f7-128">Vælg det Personale-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="8a0f7-129">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="8a0f7-130">Marker den forekomst, du vil fjerne.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="8a0f7-131">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="8a0f7-132">Hvis du vil fjerne et Personale-miljø fra et eksisterende Power Apps-miljø, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="8a0f7-133">Bemærk, at behovet for at involvere support og kontakte Personale DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="8a0f7-134">Kontakt Support for at starte en anmodning til fjernelse.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="8a0f7-135">Support-teamet igangsætter en anmodning om fjernelse hos Personale DevOps-teamet.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="8a0f7-136">Fortsæt, når du får besked om, at miljøet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="8a0f7-137">Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Personale.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="8a0f7-138">Vælg det Personale-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="8a0f7-139">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="8a0f7-140">Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="8a0f7-141">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="8a0f7-141">Select **Remove instance** and confirm your decision.</span></span> 