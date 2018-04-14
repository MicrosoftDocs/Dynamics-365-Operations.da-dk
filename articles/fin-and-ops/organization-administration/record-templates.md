---
title: Postskabeloner
description: Denne artikel introducerer begrebet postskabeloner, og forklarer, hvordan de kan bruges til at oprette poster, der deler oplysninger.
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 298f34871265dbf5c437dcdc6c05270b4e2a9a9d
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="record-templates"></a><span data-ttu-id="5731d-103">Postskabeloner</span><span class="sxs-lookup"><span data-stu-id="5731d-103">Record templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5731d-104">Denne artikel introducerer begrebet postskabeloner, og forklarer, hvordan de kan bruges til at oprette poster, der deler oplysninger.</span><span class="sxs-lookup"><span data-stu-id="5731d-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="5731d-105">Med postskabeloner kan du hurtigere oprette poster i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5731d-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5731d-106">Du kan kun oprette postskabeloner for nogle af posttyperne i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5731d-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="5731d-107">Forestil dig f.eks., at du indtaster lejeoplysninger for et biludlejningsfirma, der er placeret i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="5731d-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="5731d-108">Da de fleste af kunderne sandsynligvis er fra San Francisco-området, ville det være rart, hvis du automatisk kunne udfylde værdier i felterne **Stat**, **Land** og **By** på udlejningsblanketten.</span><span class="sxs-lookup"><span data-stu-id="5731d-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="5731d-109">Du kan kun anvende skabeloner for de områder i Finance and Operations, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="5731d-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="5731d-110">Men du får vist alle skabelontitler, der er synlige, når du opretter en ny post, og det samme gør andre brugere, hvis du opretter skabeloner, der er tilgængelige for alle brugere.</span><span class="sxs-lookup"><span data-stu-id="5731d-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="5731d-111">Det bør du have med i dine overvejelser, når du navngiver skabeloner.</span><span class="sxs-lookup"><span data-stu-id="5731d-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="5731d-112">Undgå f.eks. at bruge navne, der indeholder ord som "provision", hvis det er fortroligt, at nogle medarbejdere i virksomheden, har provisionsbaseret løn.</span><span class="sxs-lookup"><span data-stu-id="5731d-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="5731d-113">Når en eller flere skabeloner, som du har adgang til, findes til en bestemt form, og du forsøger at oprette en ny post i formen, vises siden **Vælg en skabelon til**.</span><span class="sxs-lookup"><span data-stu-id="5731d-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="5731d-114">Når du vælger en skabelon på listen, oprettes den nye post, som indeholder standardoplysninger, der er baseret på den skabelon, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="5731d-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="5731d-115">Hvis du ikke vil bruge skabeloner, når du opretter nye poster, skal du markere afkrydsningsfeltet **Spørg ikke igen** på siden **Vælg en skabelon for**.</span><span class="sxs-lookup"><span data-stu-id="5731d-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="5731d-116">Hvis du vil have vist dialogboksen til valg af skabeloner igen, skal du højreklikke på en post, klikke på **Postoplysninger** og derefter klikke på **Vis skabelonvalg**.</span><span class="sxs-lookup"><span data-stu-id="5731d-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




