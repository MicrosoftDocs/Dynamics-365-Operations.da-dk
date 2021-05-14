---
title: Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser
description: Dette emne beskriver, hvordan du konfigurerer arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956597"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="8967f-103">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8967f-104">Dette emne beskriver, hvordan du konfigurerer arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="8967f-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="8967f-105">Uoverensstemmelser skal godkendes, før brugerne kan begynde at angive oplysninger, f.eks. rettelser eller operationer.</span><span class="sxs-lookup"><span data-stu-id="8967f-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="8967f-106">Før brugere kan godkende eller afvise uoverensstemmelser, skal deres bruger-id (brugerpost) knyttes til en arbejderpost.</span><span class="sxs-lookup"><span data-stu-id="8967f-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="8967f-107">Du kan vælge at konfigurere arbejdere, der er ansvarlige for kvalitet, og derefter tillade, at én arbejder godkender arbejde på vegne af en anden arbejder.</span><span class="sxs-lookup"><span data-stu-id="8967f-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="8967f-108">Aktivere en bruger til at håndtere af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="8967f-109">Før en bruger kan godkende eller afvise uoverensstemmelser, skal du knytte brugerens bruger-id (brugerpost) til en arbejderpost.</span><span class="sxs-lookup"><span data-stu-id="8967f-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="8967f-110">Godkendelsesfelterne vil derefter blive udfyldt automatisk, og den aktuelle bruger bliver automatisk udfyldt for timesedlen.</span><span class="sxs-lookup"><span data-stu-id="8967f-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="8967f-111">Før brugeren kan bruge dokumentnoter, skal du aktivere dokumenthåndtering i indstillingerne for brugeren.</span><span class="sxs-lookup"><span data-stu-id="8967f-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="8967f-112">Gå til **Systemadministration \> Brugere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="8967f-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="8967f-113">Find og åbn den bruger, der skal kunne godkende eller afvise uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="8967f-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="8967f-114">Angiv feltet **Person** til navnet på den arbejder, der er knyttet til den aktuelle brugerpost.</span><span class="sxs-lookup"><span data-stu-id="8967f-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="8967f-115">Vælg **Brugerindstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8967f-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="8967f-116">På siden **Indstillinger** for den aktuelle brugerpost skal du angive indstillingen **Aktiver dokumenthåndtering** til **Ja** under fanen *Indstillinger*.</span><span class="sxs-lookup"><span data-stu-id="8967f-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="8967f-117">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="8967f-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="8967f-118">Definere arbejdere, der er ansvarlige for kvalitet</span><span class="sxs-lookup"><span data-stu-id="8967f-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="8967f-119">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Arbejdere, der er ansvarlige for kvalitet**.</span><span class="sxs-lookup"><span data-stu-id="8967f-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="8967f-120">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8967f-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="8967f-121">Vælg den arbejder, der angiver kvalitetsdata i feltet **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="8967f-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="8967f-122">Vælg den arbejder, som den valgte arbejder angiver arbejde på vegne af, i feltet **Ansvarlig arbejder**.</span><span class="sxs-lookup"><span data-stu-id="8967f-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="8967f-123">Når der oprettes og opdateres uoverensstemmelser, angives denne arbejder som standard i felter for **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="8967f-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8967f-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8967f-124">Additional resources</span></span>

- [<span data-ttu-id="8967f-125">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="8967f-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="8967f-126">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="8967f-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="8967f-127">Kvalitetsgebyrer</span><span class="sxs-lookup"><span data-stu-id="8967f-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="8967f-128">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="8967f-129">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="8967f-130">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="8967f-131">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="8967f-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="8967f-132">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="8967f-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
