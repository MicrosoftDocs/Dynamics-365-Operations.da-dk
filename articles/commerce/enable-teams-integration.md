---
title: Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842633"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="3b1f4-103">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3b1f4-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3b1f4-104">Dette emne beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="3b1f4-105">Hvis du vil klargøre Teams med oplysninger fra Dynamics 365 Commerce og synkronisere funktionerne til opgavestyring mellem Teams og POS-programmet (POS), skal du aktivere integrationsfunktionerne i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="3b1f4-106">Når du aktiverer integration med Teams, giver du dit samtykke til at dele dine data med Teams.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="3b1f4-107">Data, der deles med Teams, kan være i et andet land dine Commerce-data, og de kan være underlagt forskellige overholdelser af angivne standarder.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="3b1f4-108">Der er flere oplysninger i [Microsofts Sikkerhedscenter](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="3b1f4-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="3b1f4-109">Du kan finde oplysninger om Microsofts politikker for beskyttelse af personlige oplysninger i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="3b1f4-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="3b1f4-110">Aktivere Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3b1f4-110">Enable Teams integration</span></span>

<span data-ttu-id="3b1f4-111">Før du kan aktivere Microsoft Teams-integration med Commerce, skal du registrere Teams-programmet hos din lejer på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="3b1f4-112">Du kan registrere Teams-programmet hos din lejer på Azure-portalen ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="3b1f4-113">Følg trinnene i [Hurtig start: Registrer en app på Microsofts id-platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) for at registrere Teams-programmet hos din lejer på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="3b1f4-114">Kopiér værdien af **Program-id (klient)** fra siden **Oversigt** for den registrerede app.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="3b1f4-115">Du skal bruge denne værdi til at aktivere Team-integration i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="3b1f4-116">Kopiér den certifikatværdi, der blev angivet, da du [tilføjede et certifikat](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) i trin 1.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="3b1f4-117">Certifikatet kaldes også den offentlige nøgle eller programnøglen.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="3b1f4-118">Du skal bruge denne værdi til at aktivere Team-integration i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="3b1f4-119">Hvis du vil aktivere Teams-integration i Commerce-hovedkontoret, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3b1f4-120">Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="3b1f4-121">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3b1f4-122">Angiv indstillingen **Aktivér Microsoft Teams-integration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="3b1f4-123">I felterne **Program-id** og **Programnøgle** skal du angive de værdier, du fik, da du registrerede Teams-programmet på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="3b1f4-124">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="3b1f4-125">I følgende illustration vises et eksempel på konfigurationen af Teams-integration i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Konfiguration af Teams-integration i Commerce-hovedkontoret](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="3b1f4-127">Deaktivere Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3b1f4-127">Disable Teams integration</span></span>

<span data-ttu-id="3b1f4-128">Hvis du vil deaktivere Microsoft Teams-integration i Commerce-hovedkontoret, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3b1f4-129">Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="3b1f4-130">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="3b1f4-131">Angiv indstillingen **Aktivér Microsoft Teams-integration** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="3b1f4-132">Ryd værdierne i felterne **Program-id** og **Programnøgle**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="3b1f4-133">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="3b1f4-134">Når du har deaktiveret Teams-integration med Commerce, viser POS-terminaler ikke længere opgaver, der er udgivet fra Teams-programmet.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b1f4-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3b1f4-135">Additional resources</span></span>

[<span data-ttu-id="3b1f4-136">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3b1f4-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="3b1f4-137">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3b1f4-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="3b1f4-138">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="3b1f4-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="3b1f4-139">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3b1f4-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="3b1f4-140">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3b1f4-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="3b1f4-141">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="3b1f4-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
