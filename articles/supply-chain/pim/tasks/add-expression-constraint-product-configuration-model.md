---
title: Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920875"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="aae72-103">Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="aae72-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aae72-104">Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="aae72-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="aae72-105">Den viser, hvordan du kan bemyndige, at der skal anvendes hjørnebeskyttelse på en højttaler, hvis brugeren har valgt et frontgitter i metal.</span><span class="sxs-lookup"><span data-stu-id="aae72-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="aae72-106">Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="aae72-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="aae72-107">Oprette en udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="aae72-107">Create an expression constraint</span></span>

1. <span data-ttu-id="aae72-108">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="aae72-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="aae72-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="aae72-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aae72-110">I dette eksempel bruges højttalermodellen af topkvalitet.</span><span class="sxs-lookup"><span data-stu-id="aae72-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="aae72-111">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aae72-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="aae72-112">Udvid sektionen **Begrænsninger**.</span><span class="sxs-lookup"><span data-stu-id="aae72-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="aae72-113">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="aae72-113">Select **Add**.</span></span>
7. <span data-ttu-id="aae72-114">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="aae72-114">Select **Create**.</span></span>
8. <span data-ttu-id="aae72-115">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="aae72-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="aae72-116">Indtast udtryk</span><span class="sxs-lookup"><span data-stu-id="aae72-116">Enter expression</span></span>

1. <span data-ttu-id="aae72-117">Vælg **Rediger udtryk**.</span><span class="sxs-lookup"><span data-stu-id="aae72-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="aae72-118">Hvis du låser op brugergrænsefladen i opgaveregistrering på dette tidspunkt, kan du bruge IntelliSense og listen over symboler til at opbygge begrænsningsudtrykket.</span><span class="sxs-lookup"><span data-stu-id="aae72-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="aae72-119">I feltet **ConstraintBody** skal du indtaste 'Implies[FrontGrill=="Metal", CornerProtection]'.</span><span class="sxs-lookup"><span data-stu-id="aae72-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="aae72-120">Logikken for dette udtryk siger: Hvis kølergitteret er af metal, skal hjørnebeskyttelsesindstillingen være markeret.</span><span class="sxs-lookup"><span data-stu-id="aae72-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="aae72-121">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="aae72-121">Select **Validate**.</span></span>
    * <span data-ttu-id="aae72-122">Valideringsfunktionen kører gennem begrænsningsudtrykket og kontrollerer for syntaksfejl.</span><span class="sxs-lookup"><span data-stu-id="aae72-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="aae72-123">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="aae72-123">Select **Close**.</span></span>
5. <span data-ttu-id="aae72-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aae72-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]