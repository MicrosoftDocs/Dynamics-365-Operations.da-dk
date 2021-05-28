---
title: Føje datafelter til momskonfigurationer
description: Dette emne forklarer, hvordan du kan tilpasse momskonfigurationer ved at tilføje datafelter.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022781"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="fad64-103">Føje datafelter til momskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="fad64-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fad64-104">Dette emne forklarer, hvordan du kan tilpasse momskonfigurationer ved hjælp af [datafelter, der tilføjes i momsintegration](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="fad64-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="fad64-105">Tilpasse momsdatamodellen</span><span class="sxs-lookup"><span data-stu-id="fad64-105">Customize the tax data model</span></span>

1. <span data-ttu-id="fad64-106">Gå i Microsoft Dynamics 365 Finance til **Elektronisk rapportering** \> **Momskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="fad64-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="fad64-107">Vælg **Momsdatamodel – Europa** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="fad64-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="fad64-108">Vælg derefter **Opret konfiguration** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fad64-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="fad64-109">I dialogboksens rulleliste skal du vælge indstillingen **Momspligtig dokumentmodel, der er afledt af Navn: Datamodel for moms – Europa, Microsoft**, angive et navn til den nye momsdatamodel og derefter vælge **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="fad64-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="fad64-110">Vælg den momsdatamodel, du netop har oprettet, og vælg derefter **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fad64-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="fad64-111">Udvid datamodeltræet, vælg **Linjer**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fad64-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="fad64-112">Angiv et navn i dialogboksen **Opret node**, angiv en varetype, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="fad64-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="fad64-113">Tilføj eventuelle påkrævede kolonner.</span><span class="sxs-lookup"><span data-stu-id="fad64-113">Add any required columns.</span></span>
8. <span data-ttu-id="fad64-114">Vælg **Gem** i handlingsruden, og vælg derefter **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="fad64-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="fad64-115">Luk siden, og få vist den fuldførte version af momsdatamodellen.</span><span class="sxs-lookup"><span data-stu-id="fad64-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="fad64-116">Tilpasse momskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="fad64-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="fad64-117">Gå i Finance til **Elektronisk rapportering** \> **Momskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="fad64-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="fad64-118">Vælg **Momskonfiguration – Europa** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="fad64-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="fad64-119">Vælg derefter **Opret konfiguration** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fad64-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="fad64-120">I dialogboksens rulleliste skal du vælge indstillingen **Konfiguration af momstjeneste, der er afledt af Navn: Momskonfiguration – Europa, Microsoft**, angive et navn til den nye momskonfiguration og derefter vælge **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="fad64-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="fad64-121">Vælg den momskonfiguration, du netop har oprettet, og vælg derefter **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fad64-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="fad64-122">Vælg den tilpassede momsdatamodel, du oprettede tidligere, i feltet **Datamodel** i sektionen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="fad64-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="fad64-123">Vælg den fuldførte version af momsdatamodellen i feltet **Datamodelversion**.</span><span class="sxs-lookup"><span data-stu-id="fad64-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="fad64-124">Vælg **Tilføj**, og tilføj de nødvendige momsforanstaltninger.</span><span class="sxs-lookup"><span data-stu-id="fad64-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="fad64-125">Vælg **Gem** i handlingsruden, og vælg derefter **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="fad64-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="fad64-126">Luk siden, og få vist den fuldførte version af momskonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="fad64-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="fad64-127">Implementere momsfunktioner i tilpasset momskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="fad64-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="fad64-128">Gå i Regulatory Configuration Services (RCS) til **Globaliseringsfunktioner** \> **Moms**.</span><span class="sxs-lookup"><span data-stu-id="fad64-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="fad64-129">Vælg **Tilføj**, angiv oplysninger om den nye funktion, og vælg derefter **Opret funktion**.</span><span class="sxs-lookup"><span data-stu-id="fad64-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="fad64-130">Vælg funktionen under fanen **Versioner**, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fad64-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="fad64-131">Under fanen **Generelt** skal du vælge den tilpassede momskonfiguration og -version i feltet **Konfigurationsversion**.</span><span class="sxs-lookup"><span data-stu-id="fad64-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="fad64-132">Vælg i dialogboksen **Administrer kolonner** de overskrifts- og linjekolonner, du vil medtage i den brugerdefinerede momsfunktion, og vælg derefter højre piletast for at føje dem til listen **Valgte kolonner**.</span><span class="sxs-lookup"><span data-stu-id="fad64-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
