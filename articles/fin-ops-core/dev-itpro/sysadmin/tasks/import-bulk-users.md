---
title: Importere brugere fra Azure Active Directory
description: Systemadministratorer kan bruge denne procedure til at importere valgte brugere manuelt eller til at importere et stort antal brugere fra Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679808"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="c47ed-103">Importere brugere fra Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c47ed-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="c47ed-104">Importere valgte brugere</span><span class="sxs-lookup"><span data-stu-id="c47ed-104">Import select users</span></span>

<span data-ttu-id="c47ed-105">Systemadministratorer kan bruge denne procedure til at importere et valgte brugere fra Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c47ed-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="c47ed-106">Brugeren importeres med det aktuelle sessionsfirma som standardfirma.</span><span class="sxs-lookup"><span data-stu-id="c47ed-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="c47ed-107">Du skal ændre det aktuelle firma, hvis det er relevant, før du importerer brugere.</span><span class="sxs-lookup"><span data-stu-id="c47ed-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="c47ed-108">Gå til **Systemadministration > Brugere > Brugere**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="c47ed-109">Klik på **Importér brugere**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-109">Click **Import users**.</span></span>
4. <span data-ttu-id="c47ed-110">Vælg de brugere, der skal importeres, og vælg **Importér brugere**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="c47ed-111">Når importen er fuldført, skal du tildele roller til brugere.</span><span class="sxs-lookup"><span data-stu-id="c47ed-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="c47ed-112">Masseimportere brugere</span><span class="sxs-lookup"><span data-stu-id="c47ed-112">Import users in bulk</span></span>

<span data-ttu-id="c47ed-113">Systemadministratorer kan bruge denne procedure til at importere et stort antal brugere fra Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c47ed-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="c47ed-114">Bemærk, at det ikke er muligt at vælge brugere, når du bruger indstillingen Batchimport.</span><span class="sxs-lookup"><span data-stu-id="c47ed-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="c47ed-115">Køre importen som et batchjob</span><span class="sxs-lookup"><span data-stu-id="c47ed-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="c47ed-116">Brugeren importeres med det aktuelle sessionsfirma som standardfirma.</span><span class="sxs-lookup"><span data-stu-id="c47ed-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="c47ed-117">Du skal ændre det aktuelle firma, hvis det er relevant, før du importerer brugere.</span><span class="sxs-lookup"><span data-stu-id="c47ed-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="c47ed-118">Gå til **Systemadministration > Brugere > Brugere**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="c47ed-119">Klik på **Batchimport**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="c47ed-120">Udvid sektionen **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="c47ed-121">Vælg \*\*Ja i feltet **Batchbehandling**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="c47ed-122">Indtast eller vælg en værdi i feltet **Batchgruppe**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="c47ed-123">Dette trin er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="c47ed-123">This is an optional step.</span></span>  
7. <span data-ttu-id="c47ed-124">Vælg **Ja** i feltet **Privat**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="c47ed-125">Dette trin er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="c47ed-125">This is an optional step.</span></span>  
8. <span data-ttu-id="c47ed-126">Vælg **Ja** i feltet **Kritisk job**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="c47ed-127">Dette trin er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="c47ed-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="c47ed-128">Vælg en indstilling i feltet \*\*Overvågning.</span><span class="sxs-lookup"><span data-stu-id="c47ed-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="c47ed-129">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-129">Click **OK**.</span></span>

<span data-ttu-id="c47ed-130">Når importen er fuldført, skal du tildele roller til brugere.</span><span class="sxs-lookup"><span data-stu-id="c47ed-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="c47ed-131">Køre i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="c47ed-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="c47ed-132">Vælg **Batchimport**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="c47ed-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c47ed-133">Select **OK**.</span></span>
