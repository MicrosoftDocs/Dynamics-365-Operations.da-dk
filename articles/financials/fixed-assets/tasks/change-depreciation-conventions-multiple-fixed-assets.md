---
title: Ændre afskrivningsprincipper for flere anlægsaktiver
description: Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840067"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="9a62f-103">Ændre afskrivningsprincipper for flere anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="9a62f-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a62f-104">Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="9a62f-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="9a62f-105">Denne opgaveguide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9a62f-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="9a62f-106">Gå til Anlægsaktiver > Periodiske opgaver > Masseopdatering</span><span class="sxs-lookup"><span data-stu-id="9a62f-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="9a62f-107">Klik på rullelisten i feltet Afskrivningsmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9a62f-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9a62f-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9a62f-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9a62f-109">Indtast en dato i feltet Placeret først i ydelsen.</span><span class="sxs-lookup"><span data-stu-id="9a62f-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="9a62f-110">Indtast en dato i feltet Placeret sidst i ydelsen.</span><span class="sxs-lookup"><span data-stu-id="9a62f-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="9a62f-111">Kun aktiver, der er del af den valgte afskrivningsmode, og som er taget i brug mellem disse datoer, opdateres.</span><span class="sxs-lookup"><span data-stu-id="9a62f-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="9a62f-112">Vælg en indstilling i feltet Aktuelt afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="9a62f-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="9a62f-113">Kun aktiver, der har det aktuelle afskrivningsprincip, opdateres.</span><span class="sxs-lookup"><span data-stu-id="9a62f-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="9a62f-114">Vælg en indstilling i feltet Nyt afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="9a62f-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="9a62f-115">Bekræft, at rapporten udskrives til den ønskede destination.</span><span class="sxs-lookup"><span data-stu-id="9a62f-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="9a62f-116">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="9a62f-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="9a62f-117">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="9a62f-117">Click Filter.</span></span>
10. <span data-ttu-id="9a62f-118">Vælg Anlægsaktivgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="9a62f-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="9a62f-119">Klik på rullelisten i feltet Kriterier for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9a62f-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9a62f-120">Vælg den ønskede anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a62f-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="9a62f-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9a62f-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9a62f-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9a62f-122">Click OK.</span></span>
15. <span data-ttu-id="9a62f-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9a62f-123">Click OK.</span></span>
    *  <span data-ttu-id="9a62f-124">Resultaterne af processen vises i rapporten Masseopdatering.</span><span class="sxs-lookup"><span data-stu-id="9a62f-124">Results of the process are shown on the Mass update report.</span></span>     

