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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab158a9f96054f7478a331b6165c01432311eb7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213371"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="8b32c-103">Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="8b32c-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b32c-104">Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="8b32c-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="8b32c-105">Den viser, hvordan du kan bemyndige, at der skal anvendes hjørnebeskyttelse på en højttaler, hvis brugeren har valgt et frontgitter i metal.</span><span class="sxs-lookup"><span data-stu-id="8b32c-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="8b32c-106">Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8b32c-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="8b32c-107">Oprette en udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="8b32c-107">Create an expression constraint</span></span>
1. <span data-ttu-id="8b32c-108">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="8b32c-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8b32c-109">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="8b32c-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="8b32c-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8b32c-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b32c-111">I dette eksempel bruges højttalermodellen af topkvalitet.</span><span class="sxs-lookup"><span data-stu-id="8b32c-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="8b32c-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8b32c-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8b32c-113">Udvid afsnittet Begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="8b32c-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="8b32c-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b32c-114">Click Add.</span></span>
7. <span data-ttu-id="8b32c-115">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="8b32c-115">Click Create.</span></span>
8. <span data-ttu-id="8b32c-116">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="8b32c-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="8b32c-117">Indtast udtryk</span><span class="sxs-lookup"><span data-stu-id="8b32c-117">Enter expression</span></span>
1. <span data-ttu-id="8b32c-118">Klik på udtrykket Rediger.</span><span class="sxs-lookup"><span data-stu-id="8b32c-118">Click Edit expression.</span></span>
    * <span data-ttu-id="8b32c-119">Hvis du låser op brugergrænsefladen i opgaveregistrering på dette tidspunkt, kan du bruge IntelliSense og listen over symboler til at opbygge begrænsningsudtrykket.</span><span class="sxs-lookup"><span data-stu-id="8b32c-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="8b32c-120">I feltet ConstraintBody skal du angive 'Implies[FrontGrill=="Metal", CornerProtection]'.</span><span class="sxs-lookup"><span data-stu-id="8b32c-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="8b32c-121">Logikken for dette udtryk siger: Hvis kølergitteret er af metal, skal hjørnebeskyttelsesindstillingen være markeret.</span><span class="sxs-lookup"><span data-stu-id="8b32c-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="8b32c-122">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="8b32c-122">Click Validate.</span></span>
    * <span data-ttu-id="8b32c-123">Valideringsfunktionen kører gennem begrænsningsudtrykket og kontrollerer for syntaksfejl.</span><span class="sxs-lookup"><span data-stu-id="8b32c-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="8b32c-124">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="8b32c-124">Click Close.</span></span>
5. <span data-ttu-id="8b32c-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8b32c-125">Click OK.</span></span>

