---
title: Aktivere Power BI til Global Inventory Accounting
description: Dette emne indeholder en beskrivelse af, hvordan du aktiverer Microsoft Power BI til Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273131"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="f9322-103">Aktivere Power BI til Global Inventory Accounting</span><span class="sxs-lookup"><span data-stu-id="f9322-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="f9322-104">Du kan fastgøre felter, dashboards og rapporter fra din [PowerBI.com](https://powerbi.com/)-konto til arbejdsområdet i Microsoft Dynamics 365-programmet.</span><span class="sxs-lookup"><span data-stu-id="f9322-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f9322-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f9322-105">Prerequisites</span></span>

<span data-ttu-id="f9322-106">Følgende forudsætninger skal være tilstede, før du kan aktivere Power BI-rapportering:</span><span class="sxs-lookup"><span data-stu-id="f9322-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="f9322-107">Du skal være systemadministrator i Dynamics 365-programmet.</span><span class="sxs-lookup"><span data-stu-id="f9322-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="f9322-108">Du skal have en [PowerBI.com](https://powerbi.com/)-konto.</span><span class="sxs-lookup"><span data-stu-id="f9322-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="f9322-109">Du skal have mindst ét dashboard og én rapport i Power BI-kontoen.</span><span class="sxs-lookup"><span data-stu-id="f9322-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="f9322-110">Du skal være administrator for din Azure Active Directory-konto (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f9322-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="f9322-111">Domænet Azure AD skal være det samme domæne, som du har brugt til din [PowerBI.com](https://powerbi.com/)-konto.</span><span class="sxs-lookup"><span data-stu-id="f9322-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="f9322-112">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f9322-112">Setup</span></span>

<span data-ttu-id="f9322-113">Følg disse trin for at konfigurere Power BI-integrationen.</span><span class="sxs-lookup"><span data-stu-id="f9322-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="f9322-114">Log på [Microsoft Dynamics LifeCycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="f9322-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="f9322-115">Gå til **Delt aktivbibliotek**, vælg **Power BI-rapportmodel** som aktivtype, og hent pakken **Global Inventory Accounting**.</span><span class="sxs-lookup"><span data-stu-id="f9322-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="f9322-116">Log på [PowerBI.com](https://app.powerbi.com/), og overfør Power BI-rapportfilen for **Global Inventory Accounting** ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="f9322-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="f9322-117">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f9322-117">Select **New**.</span></span>
    1. <span data-ttu-id="f9322-118">Vælg **Overfør en fil**.</span><span class="sxs-lookup"><span data-stu-id="f9322-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="f9322-119">Vælg Power BI-rapportfilen for **Global Inventory Accounting**.</span><span class="sxs-lookup"><span data-stu-id="f9322-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="f9322-120">Konfigurer Power BI-rapporten for **Global Inventory Accounting** ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="f9322-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="f9322-121">Gå til **Mit arbejdsområde**, find datasættet til Global Inventory Accounting, og vælg derefter **Indstillinger** i menuen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f9322-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="f9322-122">Udvid **Parametre** i **Indstillinger for Global Inventory Accounting**, og opdater alle parametre efter behov.</span><span class="sxs-lookup"><span data-stu-id="f9322-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="f9322-123">Registrer programmet som beskrevet i [Konfigurere PowerBI.com-integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="f9322-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="f9322-124">Integrer Power BI-rapporten for **Global Inventory Accounting** i Dynamics 365 Supply Chain Management ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="f9322-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="f9322-125">Gå til **Systemadministration \> Konfiguration \> PowerBI.com-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f9322-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="f9322-126">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f9322-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="f9322-127">Vælg **Aktivér PowerBI.Com-integration**.</span><span class="sxs-lookup"><span data-stu-id="f9322-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="f9322-128">I feltet **Program-id** skal du angive program-id'et.</span><span class="sxs-lookup"><span data-stu-id="f9322-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="f9322-129">I feltet **Programnøgle** skal du angive programnøglen.</span><span class="sxs-lookup"><span data-stu-id="f9322-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="f9322-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f9322-130">Select **Save**.</span></span>

1. <span data-ttu-id="f9322-131">Opdater siden, så Power BI-logondialogboksen vises.</span><span class="sxs-lookup"><span data-stu-id="f9322-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="f9322-132">Vælg **Åbn rapportkatalog** under fanen **Indstillinger**, og vælg derefter den Power BI-rapportfil til **Global Inventory Accounting**, som du overførte tidligere.</span><span class="sxs-lookup"><span data-stu-id="f9322-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="f9322-133">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="f9322-133">Refresh the page.</span></span> <span data-ttu-id="f9322-134">Du bør se, at rapporten er blevet tilføjet.</span><span class="sxs-lookup"><span data-stu-id="f9322-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="f9322-135">Under **Power BI-rapporter** skal du vælge linket **Global Inventory Accounting**.</span><span class="sxs-lookup"><span data-stu-id="f9322-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="f9322-136">Du kan finde flere oplysninger i [Konfigurere PowerBI.com-integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="f9322-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
