---
title: "Afgrænsningstegnet for kontoplaner skal være entydigt"
description: "I Dynamics 365 for Finance and Operations kan ikke du anvende det samme afgrænsningstegn til kontoplanen og dimensionsværdierne. Du skal ændre afgrænsningstegnets værdier efter opgraderingen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e12c47e4acd6aa8a92a909d490da9e590b5fcd20
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="3e527-104">Afgrænsningstegnet for kontoplaner skal være entydigt</span><span class="sxs-lookup"><span data-stu-id="3e527-104">Chart of accounts delimiter must be unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e527-105">Du kan bruge samme afgrænsningstegn til kontoplanen og dimensionsværdierne i Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="3e527-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="3e527-106">I Dynamics 365 for Finance and Operations kan ikke du anvende det samme afgrænsningstegn til kontoplanen og dimensionsværdierne.</span><span class="sxs-lookup"><span data-stu-id="3e527-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="3e527-107">Hvis der er anvendes samme afgrænsningstegn, kan du ændre det efter opgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3e527-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="3e527-108">Denne funktion er tilgængelig i:</span><span class="sxs-lookup"><span data-stu-id="3e527-108">This feature is available in:</span></span>
- <span data-ttu-id="3e527-109">Dynamics 365 for Finance and Operations version 8.0</span><span class="sxs-lookup"><span data-stu-id="3e527-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="3e527-110">Dynamics 365 til Finance and Operations version 7.1, KB 4094701 kan ikke få adgang til de økonomiske dimensioner, når dimensionsværdierne indeholder afgrænsningstegnet for kontoplan</span><span class="sxs-lookup"><span data-stu-id="3e527-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="3e527-111">Dynamics 365 til Finance and Operations version 7.2, KB 4092967 kan ikke vælge underprojekt som en dimension, når formatet for underprojekt indeholder afgrænsningstegnet for dimensioner</span><span class="sxs-lookup"><span data-stu-id="3e527-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="3e527-112">Opdatere afgrænsningstegn</span><span class="sxs-lookup"><span data-stu-id="3e527-112">Update delimiter</span></span>
<span data-ttu-id="3e527-113">Hvis der er en konflikt med kontoplanen, kan afgrænsningstegnet for kontoplanen og formatet for projekt/underprojekt-id ændres.</span><span class="sxs-lookup"><span data-stu-id="3e527-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="3e527-114">Ingen andre afgrænsningstegn kan ændres.</span><span class="sxs-lookup"><span data-stu-id="3e527-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="3e527-115">Du kan ændre afgrænsningstegnet for kontoplanen efter opgradering til Finance and Operations i **Finansparametre** > **Kontoplaner og dimensioner** > **Skift afgrænsningstegn**.</span><span class="sxs-lookup"><span data-stu-id="3e527-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="3e527-116">Hvis der er kun konflikten med formatet for projekt/underprojekt-id, kan du ændre værdien i **Parametre for projektstyring og regnskab** > **Generelt** > **Rediger underprojektformat**.</span><span class="sxs-lookup"><span data-stu-id="3e527-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="3e527-117">Sådan afgør du, om dit miljø kræver opdaterede afgrænsningstegn</span><span class="sxs-lookup"><span data-stu-id="3e527-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="3e527-118">Hvis afgrænsningstegnene i det opgraderede miljø er i konflikt, kan systemet blive ustabilt ved indtastning af værdier ved segmenteret postkontrol eller dimensionspostkontrol.</span><span class="sxs-lookup"><span data-stu-id="3e527-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="3e527-119">Det betyder, at du skal altid bruge opslag eller en pop op-menu ved indtastning af kombinationer af konti og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3e527-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

