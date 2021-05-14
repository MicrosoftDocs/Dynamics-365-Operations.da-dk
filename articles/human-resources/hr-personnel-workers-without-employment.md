---
title: Arbejdere uden ansættelse
description: Arbejdere uden fremtidig, aktiv eller historisk ansættelse i organisationen vises i formularen Arbejdere uden ansættelse.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924565"
---
# <a name="workers-without-employment"></a><span data-ttu-id="49dd5-103">Arbejdere uden ansættelse</span><span class="sxs-lookup"><span data-stu-id="49dd5-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="49dd5-104">Arbejdere uden fremtidig, aktiv eller historisk ansættelse i organisationen vises i formularen **Arbejdere uden ansættelse**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="49dd5-105">Arbejdere med denne status kan vises, når du importerer arbejdere uden en ansættelsespost, eller når du sletter en arbejders ansættelse via **Arbejder > Ansættelseshistorik**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="49dd5-106">Formularen **Arbejdere uden ansættelse** er som standard tilgængelig for følgende roller:</span><span class="sxs-lookup"><span data-stu-id="49dd5-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="49dd5-107">Personaleassistent</span><span class="sxs-lookup"><span data-stu-id="49dd5-107">Human Resources Assistant</span></span>
- <span data-ttu-id="49dd5-108">Personalechef</span><span class="sxs-lookup"><span data-stu-id="49dd5-108">Human Resources Manager</span></span>
- <span data-ttu-id="49dd5-109">Rekrutteringsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="49dd5-109">Recruiter</span></span>
- <span data-ttu-id="49dd5-110">Chef for kompensation og frynsegoder</span><span class="sxs-lookup"><span data-stu-id="49dd5-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="49dd5-111">Lønadministrator</span><span class="sxs-lookup"><span data-stu-id="49dd5-111">Payroll Administrator</span></span>
- <span data-ttu-id="49dd5-112">Lønchef</span><span class="sxs-lookup"><span data-stu-id="49dd5-112">Payroll Manager</span></span>
- <span data-ttu-id="49dd5-113">Uddannelseschef</span><span class="sxs-lookup"><span data-stu-id="49dd5-113">Training Manager</span></span>

<span data-ttu-id="49dd5-114">På listen **Arbejdere uden ansættelse** kan du slette de anførte personer.</span><span class="sxs-lookup"><span data-stu-id="49dd5-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="49dd5-115">Denne rettighed gives som standard til rollen Personaleassistent.</span><span class="sxs-lookup"><span data-stu-id="49dd5-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="49dd5-116">Du kan tildele denne rettighed til andre roller med følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="49dd5-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="49dd5-117">Vælg **Systemadministration**, og klik derefter under fanen **Sikkerhedskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="49dd5-118">Filtrer listen **Rettigheder** under fanen **Rettigheder** til **Vedligehold medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="49dd5-119">[![Filtrere listen Rettigheder](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="49dd5-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="49dd5-120">Vælg **Vis menupunkter** i kolonnen **Referencer**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="49dd5-121">Vælg **HcmWorkersWithoutEmployment** i **Vis menupunkter**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="49dd5-122">[![Vælg formular](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="49dd5-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="49dd5-123">Angiv rettigheden **Slet** til **Tildel**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="49dd5-124">Vælg fanen **Ikke-publicerede objekter**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="49dd5-125">Vælg **Publicer alle**.</span><span class="sxs-lookup"><span data-stu-id="49dd5-125">Select **Publish all**.</span></span>

   <span data-ttu-id="49dd5-126">[![Publicer ændringer](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="49dd5-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]