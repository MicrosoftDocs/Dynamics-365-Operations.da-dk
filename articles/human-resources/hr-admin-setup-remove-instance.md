---
title: Fjern en forekomst
description: Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a384801060b2b684f7908daaac2311edd27c773a
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621374"
---
# <a name="remove-an-instance"></a><span data-ttu-id="3844a-103">Fjern en forekomst</span><span class="sxs-lookup"><span data-stu-id="3844a-103">Remove an instance</span></span>

<span data-ttu-id="3844a-104">Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3844a-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="3844a-105">Fjerne et testdrevmiljø</span><span class="sxs-lookup"><span data-stu-id="3844a-105">Remove a test drive environment</span></span>

<span data-ttu-id="3844a-106">Testdrev til Personale er klargjort med en 60-dages udløbspolitik.</span><span class="sxs-lookup"><span data-stu-id="3844a-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="3844a-107">Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3844a-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="3844a-108">Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3844a-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="3844a-109">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="3844a-109">Select **Environments**.</span></span>
3. <span data-ttu-id="3844a-110">Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="3844a-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="3844a-111">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="3844a-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="3844a-112">Det eksisterende testdrevmiljø fjernes.</span><span class="sxs-lookup"><span data-stu-id="3844a-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="3844a-113">Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø.</span><span class="sxs-lookup"><span data-stu-id="3844a-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="3844a-114">Fjerne et produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="3844a-114">Remove a production environment</span></span>

<span data-ttu-id="3844a-115">Det antages i artiklen, at du har købt Personale via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="3844a-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="3844a-116">Da der er indeholdt et enkelt Personale-miljø i hvert enkelt Power Apps-miljø, er der to indstillinger, der skal overvejes.</span><span class="sxs-lookup"><span data-stu-id="3844a-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="3844a-117">Den første indstilling omfatter fjernelse af hele Power Apps-miljøet, den anden mulighed omfatter kun fjernelse af Personale.</span><span class="sxs-lookup"><span data-stu-id="3844a-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="3844a-118">Den første indstilling foretrækkes, når du har oprettet et Power Apps-miljø udtrykkeligt med henblik på klargøring af Personale, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer.</span><span class="sxs-lookup"><span data-stu-id="3844a-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="3844a-119">Den anden mulighed er kun relevant, når du har et etableret Power Apps-miljø, der er udfyldt med omfattende data, som udnyttes i Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="3844a-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="3844a-120">Før du fjerner Power Apps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Personale.</span><span class="sxs-lookup"><span data-stu-id="3844a-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="3844a-121">Bemærk også, at Power Apps-standardmiljøerne ikke kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="3844a-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="3844a-122">Sådan fjernes hele Power Apps-miljøet, herunder Personale og de tilknyttede apps og flows:</span><span class="sxs-lookup"><span data-stu-id="3844a-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="3844a-123">Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3844a-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="3844a-124">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="3844a-124">Select **Environments**.</span></span>
3. <span data-ttu-id="3844a-125">Vælg det miljø, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="3844a-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="3844a-126">Vælg **Slet**, og bekræft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="3844a-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="3844a-127">Vent, indtil sletningen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3844a-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="3844a-128">Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Personale.</span><span class="sxs-lookup"><span data-stu-id="3844a-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="3844a-129">Vælg det Personale-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="3844a-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="3844a-130">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="3844a-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="3844a-131">Marker den forekomst, du vil fjerne.</span><span class="sxs-lookup"><span data-stu-id="3844a-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="3844a-132">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="3844a-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="3844a-133">Hvis du vil fjerne et Personale-miljø fra et eksisterende Power Apps-miljø, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="3844a-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="3844a-134">Bemærk, at behovet for at involvere support og kontakte Personale DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.</span><span class="sxs-lookup"><span data-stu-id="3844a-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="3844a-135">Kontakt Support for at starte en anmodning til fjernelse.</span><span class="sxs-lookup"><span data-stu-id="3844a-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="3844a-136">Support-teamet igangsætter en anmodning om fjernelse hos Personale DevOps-teamet.</span><span class="sxs-lookup"><span data-stu-id="3844a-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="3844a-137">Fortsæt, når du får besked om, at miljøet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="3844a-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="3844a-138">Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Personale.</span><span class="sxs-lookup"><span data-stu-id="3844a-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="3844a-139">Vælg det Personale-projekt, der indeholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="3844a-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="3844a-140">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="3844a-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="3844a-141">Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="3844a-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="3844a-142">Vælg **Fjern forekomst**, og bekræft sletningen.</span><span class="sxs-lookup"><span data-stu-id="3844a-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="3844a-143">Gendanne et ikke-permanent slettet miljø</span><span class="sxs-lookup"><span data-stu-id="3844a-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="3844a-144">Hvis du sletter det Power Apps-miljø, som personalemiljøet er forbundet med, vil status for personalemiljøet i tjenesten Lifecycle Services være **Ikke-permanent slettet**.</span><span class="sxs-lookup"><span data-stu-id="3844a-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="3844a-145">I dette tilfælde kan brugere ikke oprette forbindelse til personale.</span><span class="sxs-lookup"><span data-stu-id="3844a-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="3844a-146">Sådan gendannes miljøet:</span><span class="sxs-lookup"><span data-stu-id="3844a-146">To restore the environment:</span></span>

1. <span data-ttu-id="3844a-147">Følg vejledningen i [Gendanne Power Apps-miljøet](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3844a-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="3844a-148">Kontakt support for at gendanne personalemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3844a-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="3844a-149">Du kan finde flere oplysninger under [Få support](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="3844a-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="3844a-150">Power Apps-miljøer gemmes kun i syv dage efter sletning.</span><span class="sxs-lookup"><span data-stu-id="3844a-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="3844a-151">Du skal gendanne miljøet inden for perioden på syv dage.</span><span class="sxs-lookup"><span data-stu-id="3844a-151">You must recover the environment within the seven day period.</span></span>
