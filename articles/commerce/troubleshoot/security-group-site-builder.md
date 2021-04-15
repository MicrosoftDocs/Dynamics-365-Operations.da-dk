---
title: Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801501"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="2ba13-103">Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation</span><span class="sxs-lookup"><span data-stu-id="2ba13-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ba13-104">Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.</span><span class="sxs-lookup"><span data-stu-id="2ba13-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="2ba13-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2ba13-105">Description</span></span>

<span data-ttu-id="2ba13-106">Når du opretter e-handelskomponenterne som en del af implementeringsprocessen af en ny e-commerce-lejer, der omfatter komponenten Commerce-webstedsgenerator, vises Azure AD-sikkerhedsgruppen ikke som en indstilling i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ba13-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="2ba13-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="2ba13-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="2ba13-108">Klargør e-handelswebstedet med en bruger i den korrekte lejer</span><span class="sxs-lookup"><span data-stu-id="2ba13-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="2ba13-109">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2ba13-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="2ba13-110">Under den lejer, som LCS-projektet til dit e-handelswebsted er klargjort til, skal du følge instruktionerne i [Opret en basisgruppe og tilføj medlemmer ved hjælp Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="2ba13-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="2ba13-111">Gå til [LCS](https://lcs.dynamics.com/), og log på med en konto, der deler samme lejer som den Azure AD-sikkerhedsgruppe, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="2ba13-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="2ba13-112">Kontoen skal have adgang til for at få vist Azure AD-sikkerhedsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2ba13-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="2ba13-113">Gennemfør opsætningstrinnene for at konfigurere e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="2ba13-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="2ba13-114">Når du klargør e-handelskomponenterne, skal sikkerhedsgruppen nu vises som en mulighed i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ba13-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="2ba13-115">Hvis du vil sikre dig, at feltet i dialogboksen er udfyldt med listen over sikkerhedsgrupper, skal du vælge **Enter**, når du har indtastet navnet på den Azure AD-sikkerhedsgruppe, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="2ba13-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="2ba13-116">Søgeresultaterne viser alle Azure AD-sikkerhedsgrupper, der starter med søgeteksten, og som brugeren har adgang til.</span><span class="sxs-lookup"><span data-stu-id="2ba13-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="2ba13-117">Du kan bruge en kortere søgeudsigt for at give mere generelle søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="2ba13-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ba13-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2ba13-118">Additional resources</span></span>

[<span data-ttu-id="2ba13-119">Oprette en basisgruppe og tilføje medlemmer ved hjælp af Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ba13-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="2ba13-120">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="2ba13-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
