---
title: Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424642"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="b79a4-103">Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="b79a4-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b79a4-104">Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="b79a4-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="b79a4-105">Den viser, hvordan du kan bemyndige, at der skal anvendes hjørnebeskyttelse på en højttaler, hvis brugeren har valgt et frontgitter i metal.</span><span class="sxs-lookup"><span data-stu-id="b79a4-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="b79a4-106">Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b79a4-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="b79a4-107">Oprette en udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="b79a4-107">Create an expression constraint</span></span>
1. <span data-ttu-id="b79a4-108">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="b79a4-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="b79a4-109">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="b79a4-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="b79a4-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b79a4-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b79a4-111">I dette eksempel bruges højttalermodellen af topkvalitet.</span><span class="sxs-lookup"><span data-stu-id="b79a4-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="b79a4-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b79a4-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b79a4-113">Udvid afsnittet Begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="b79a4-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="b79a4-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="b79a4-114">Click Add.</span></span>
7. <span data-ttu-id="b79a4-115">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="b79a4-115">Click Create.</span></span>
8. <span data-ttu-id="b79a4-116">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="b79a4-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="b79a4-117">Indtast udtryk</span><span class="sxs-lookup"><span data-stu-id="b79a4-117">Enter expression</span></span>
1. <span data-ttu-id="b79a4-118">Klik på udtrykket Rediger.</span><span class="sxs-lookup"><span data-stu-id="b79a4-118">Click Edit expression.</span></span>
    * <span data-ttu-id="b79a4-119">Hvis du låser op brugergrænsefladen i opgaveregistrering på dette tidspunkt, kan du bruge IntelliSense og listen over symboler til at opbygge begrænsningsudtrykket.</span><span class="sxs-lookup"><span data-stu-id="b79a4-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="b79a4-120">I feltet ConstraintBody skal du angive 'Implies[FrontGrill=="Metal", CornerProtection] '.</span><span class="sxs-lookup"><span data-stu-id="b79a4-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="b79a4-121">Logikken for dette udtryk siger: Hvis kølergitteret er af metal, skal hjørnebeskyttelsesindstillingen være markeret.</span><span class="sxs-lookup"><span data-stu-id="b79a4-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="b79a4-122">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="b79a4-122">Click Validate.</span></span>
    * <span data-ttu-id="b79a4-123">Valideringsfunktionen kører gennem begrænsningsudtrykket og kontrollerer for syntaksfejl.</span><span class="sxs-lookup"><span data-stu-id="b79a4-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="b79a4-124">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="b79a4-124">Click Close.</span></span>
5. <span data-ttu-id="b79a4-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b79a4-125">Click OK.</span></span>

