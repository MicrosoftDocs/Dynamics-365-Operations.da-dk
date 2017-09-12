---
title: "Systemdefinerede og brugerdefinerede tabelbegrænsninger"
description: "I denne artikel forklares de to typer tabelbegrænsninger for komponenter i en produktkonfigurationsmodel – brugerdefineret og systemdefineret. Tabelbegrænsninger repræsenterer matrixer af tilladte attributkombinationer, hvor hver række definerer et sæt mulige attributværdier."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9bce875b5688c3b2449262437091e28dbcb740f0
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="3bd3b-104">Systemdefinerede og brugerdefinerede tabelbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="3bd3b-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3bd3b-105">I denne artikel forklares de to typer tabelbegrænsninger for komponenter i en produktkonfigurationsmodel – brugerdefineret og systemdefineret.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="3bd3b-106">Tabelbegrænsninger repræsenterer matrixer af tilladte attributkombinationer, hvor hver række definerer et sæt mulige attributværdier.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="3bd3b-107">Tabelbegrænsninger repræsenterer matrixer af kombinationerne af attributter, der er tilladt for komponenter i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="3bd3b-108">Hver række i tabellen definerer et sæt mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="3bd3b-109">Der findes to typer begrænsninger i en produktkonfigurationsmodel:</span><span class="sxs-lookup"><span data-stu-id="3bd3b-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="3bd3b-110">**Udtryksbegrænsning** – Opret et udtryk, der definerer forbindelser mellem attributter for at sikre, at der kun kan vælges kompatible værdier under produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="3bd3b-111">**Tabelbegrænsning** – Opret en tabel, der definerer alle de kombinationer, der er tilladt for et bestemt sæt attributter.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="3bd3b-112">Der findes to typer tabelbegrænsninger: brugerdefinerede tabelbegrænsninger og systemdefinerede tabelbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="3bd3b-113">I denne artikel beskrives brugerdefinerede og systemdefinerede tabelbegrænsninger for komponenter i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="3bd3b-114">Brugerdefinerede tabelbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="3bd3b-114">User-defined table constraints</span></span>
<span data-ttu-id="3bd3b-115">En begrænsning for en brugerdefineret tabel er en matrixtype, der kan bruges til at beskrive kombinationer af de attributværdier, der er defineret af attributtyper.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="3bd3b-116">Hvis du f.eks. producerer højttalere, kan du medtage kolonner til kabinetfinish og frontgitter i den brugerdefinerede tabelbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="3bd3b-117">Attributtypen for kabinetfinish har fire værdier, og attributtypen for frontgitter har tre værdier.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="3bd3b-118">Så hvis der ikke bruges betingelser, er der 4 × 3 = 12 mulige kombinationer.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="3bd3b-119">Men i dette eksempel er kun seks tilladte kombinationer, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="3bd3b-120">Disse oplysninger vises under fanen **Tilladte kombinationer** på siden **Rediger tabelbegrænsning**.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="3bd3b-121">Kabinetfinish</span><span class="sxs-lookup"><span data-stu-id="3bd3b-121">Cabinet finish</span></span> | <span data-ttu-id="3bd3b-122">Frontgitter</span><span class="sxs-lookup"><span data-stu-id="3bd3b-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="3bd3b-123">Sort</span><span class="sxs-lookup"><span data-stu-id="3bd3b-123">Black</span></span>          | <span data-ttu-id="3bd3b-124">Sort</span><span class="sxs-lookup"><span data-stu-id="3bd3b-124">Black</span></span>       |
| <span data-ttu-id="3bd3b-125">Sort</span><span class="sxs-lookup"><span data-stu-id="3bd3b-125">Black</span></span>          | <span data-ttu-id="3bd3b-126">Metal</span><span class="sxs-lookup"><span data-stu-id="3bd3b-126">Metal</span></span>       |
| <span data-ttu-id="3bd3b-127">Egetræ</span><span class="sxs-lookup"><span data-stu-id="3bd3b-127">Oak</span></span>            | <span data-ttu-id="3bd3b-128">Sort</span><span class="sxs-lookup"><span data-stu-id="3bd3b-128">Black</span></span>       |
| <span data-ttu-id="3bd3b-129">Rosentræ</span><span class="sxs-lookup"><span data-stu-id="3bd3b-129">Rosewood</span></span>       | <span data-ttu-id="3bd3b-130">Hvid</span><span class="sxs-lookup"><span data-stu-id="3bd3b-130">White</span></span>       |
| <span data-ttu-id="3bd3b-131">Hvid</span><span class="sxs-lookup"><span data-stu-id="3bd3b-131">White</span></span>          | <span data-ttu-id="3bd3b-132">Sort</span><span class="sxs-lookup"><span data-stu-id="3bd3b-132">Black</span></span>       |
| <span data-ttu-id="3bd3b-133">Hvid</span><span class="sxs-lookup"><span data-stu-id="3bd3b-133">White</span></span>          | <span data-ttu-id="3bd3b-134">Hvid</span><span class="sxs-lookup"><span data-stu-id="3bd3b-134">White</span></span>       |

<span data-ttu-id="3bd3b-135">Brugerdefinerede tabelbegrænsninger defineres af statisk tabelinput, der fungerer på samme måde som en udtryksbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="3bd3b-136">Når du bruger en brugerdefineret tabelbegrænsning, er fordelen, at det ofte er nemmere at oprette tabellerne, og de er nemmere at forstå og vedligeholde end lange udtryksbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="3bd3b-137">Systemdefinerede tabelbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="3bd3b-137">System-defined table constraints</span></span>
<span data-ttu-id="3bd3b-138">En systemdefineret tabelbegrænsning opretter en dynamisk tilknytning mellem en attributtype og et felt i en tabel.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="3bd3b-139">Når en systemdefineret tabelbegrænsning medtages i en produktkonfigurationsmodel, sikrer tilknytningen, at dataene i tabellen vises i stedet for værdierne for attributtypen.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="3bd3b-140">Resultatet er en dynamisk begrænsning, fordi tabellens indhold kan ændres, f.eks. af andre moduler.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="3bd3b-141">Når du opretter en systemdefineret tabelbegrænsning, skal du vælge en tabel, eventuelt definere den forespørgsel, der skal bruges, og derefter knytte attributtyper til felterne i den valgte tabel.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="3bd3b-142">Felttyperne svar svare til attributtyperne.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="3bd3b-143">Før en tabelbegrænsning kan træde i kraft på en model til produktkonfiguration, skal tabelbegrænsningen medtages i en begrænsning på en af modellens komponenter.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="3bd3b-144">Fremgangsmåden er at oprette en ny begrænsning, vælge typen af tabelbegrænsning og derefter vælge den tabelbegrænsningsdefinition, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="3bd3b-145">Endelig skal alle felter i tabelbegrænsningen knyttes til attributterne i produktkonfigurationsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3bd3b-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="3bd3b-146">Se også</span><span class="sxs-lookup"><span data-stu-id="3bd3b-146">See also</span></span>
--------

[<span data-ttu-id="3bd3b-147">Nøglebegreber i produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="3bd3b-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




