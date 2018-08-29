---
title: "Fjerne Talent-miljøer"
description: "Dette emne fører dig gennem processen med at fjerne et testdrev eller et produktionsmiljø til Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 5080f1ec182b8cbdf281967185a1afeb9887f682
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="remove-talent-environments"></a><span data-ttu-id="85c2b-103">Fjerne Talent-miljøer</span><span class="sxs-lookup"><span data-stu-id="85c2b-103">Remove Talent environments</span></span>

<span data-ttu-id="85c2b-104">Dette emne fører dig gennem processen med at fjerne et testdrev eller et produktionsmiljø til Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="85c2b-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="85c2b-105">Fjerne et testdrevmiljø</span><span class="sxs-lookup"><span data-stu-id="85c2b-105">Removing a test drive environment</span></span>

<span data-ttu-id="85c2b-106">Testdrev til Talent er klargjort med en 60-dages udløbspolitik.</span><span class="sxs-lookup"><span data-stu-id="85c2b-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="85c2b-107">Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="85c2b-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="85c2b-108">Naviger til [PowerApps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="85c2b-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="85c2b-109">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="85c2b-109">Select **Environments**.</span></span>
3. <span data-ttu-id="85c2b-110">Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="85c2b-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="85c2b-111">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="85c2b-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="85c2b-112">Det eksisterende testdrevmiljø fjernes.</span><span class="sxs-lookup"><span data-stu-id="85c2b-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="85c2b-113">Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø.</span><span class="sxs-lookup"><span data-stu-id="85c2b-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="85c2b-114">Fjerne et produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="85c2b-114">Removing a production environment</span></span>

<span data-ttu-id="85c2b-115">Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="85c2b-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="85c2b-116">Da der er "indeholdt" et enkelt Talent-miljø i hver enkelt PowerApps-miljø, er der to indstillinger, der skal overvejes.</span><span class="sxs-lookup"><span data-stu-id="85c2b-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="85c2b-117">Den første indstilling omfatter fjernelse af hele PowerApps-miljøet, den anden mulighed omfatter kun fjernelse af Talent.</span><span class="sxs-lookup"><span data-stu-id="85c2b-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="85c2b-118">Den første indstilling foretrækkes, når du har oprettet et PowerApps-miljø udtrykkeligt med henblik på klargøring af Talent, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer.</span><span class="sxs-lookup"><span data-stu-id="85c2b-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="85c2b-119">Den anden mulighed er kun relevant, når du har et etableret PowerApps-miljø, der er udfyldt med omfattende data, som udnyttes i PowerApps og processer.</span><span class="sxs-lookup"><span data-stu-id="85c2b-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="85c2b-120">Før du fjerner PowerApps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Talent.</span><span class="sxs-lookup"><span data-stu-id="85c2b-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="85c2b-121">Bemærk også, at PowerApps-standardmiljøerne ikke kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="85c2b-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="85c2b-122">Sådan fjernes hele PowerApps-miljøet, herunder Talent og de tilknyttede apps og processer:</span><span class="sxs-lookup"><span data-stu-id="85c2b-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="85c2b-123">Naviger til [PowerApps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="85c2b-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="85c2b-124">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="85c2b-124">Select **Environments**.</span></span>
3. <span data-ttu-id="85c2b-125">Vælg det miljø, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="85c2b-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="85c2b-126">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="85c2b-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="85c2b-127">Vent, indtil sletningen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="85c2b-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="85c2b-128">Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Talent.</span><span class="sxs-lookup"><span data-stu-id="85c2b-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="85c2b-129">Vælg det Talent-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="85c2b-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="85c2b-130">I LCS-projektet skal du vælge feltet **Administration af Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="85c2b-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="85c2b-131">Marker den forekomst, du vil fjerne.</span><span class="sxs-lookup"><span data-stu-id="85c2b-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="85c2b-132">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="85c2b-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="85c2b-133">Hvis du vil fjerne et Talent-miljø fra et eksisterende PowerApps-miljø, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="85c2b-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="85c2b-134">Bemærk, at behovet for at involvere support og kontakte Talent DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.</span><span class="sxs-lookup"><span data-stu-id="85c2b-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="85c2b-135">Kontakt Support for at starte en anmodning til fjernelse.</span><span class="sxs-lookup"><span data-stu-id="85c2b-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="85c2b-136">Support-teamet igangsætter en anmodning om fjernelse hos Talent DevOps-teamet.</span><span class="sxs-lookup"><span data-stu-id="85c2b-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="85c2b-137">Fortsæt, når du får besked om, at miljøet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="85c2b-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="85c2b-138">Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Talent.</span><span class="sxs-lookup"><span data-stu-id="85c2b-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="85c2b-139">Vælg det Talent-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="85c2b-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="85c2b-140">I LCS-projektet skal du vælge feltet **Administration af Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="85c2b-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="85c2b-141">Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="85c2b-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="85c2b-142">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="85c2b-142">Select **Remove instance** and confirm your decision.</span></span> 


