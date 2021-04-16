---
title: Ændre afskrivningsprincipper for flere anlægsaktiver
description: Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a71b24b0c2ea072aeff8c994cfdac10bc57b64c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823974"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="05e42-103">Ændre afskrivningsprincipper for flere anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="05e42-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05e42-104">Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="05e42-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="05e42-105">Denne opgaveguide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="05e42-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="05e42-106">Gå til Anlægsaktiver > Periodiske opgaver > Masseopdatering</span><span class="sxs-lookup"><span data-stu-id="05e42-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="05e42-107">Klik på rullelisten i feltet Afskrivningsmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="05e42-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="05e42-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="05e42-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="05e42-109">Indtast en dato i feltet Placeret først i ydelsen.</span><span class="sxs-lookup"><span data-stu-id="05e42-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="05e42-110">Indtast en dato i feltet Placeret sidst i ydelsen.</span><span class="sxs-lookup"><span data-stu-id="05e42-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="05e42-111">Kun aktiver, der er del af den valgte afskrivningsmode, og som er taget i brug mellem disse datoer, opdateres.</span><span class="sxs-lookup"><span data-stu-id="05e42-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="05e42-112">Vælg en indstilling i feltet Aktuelt afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="05e42-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="05e42-113">Kun aktiver, der har det aktuelle afskrivningsprincip, opdateres.</span><span class="sxs-lookup"><span data-stu-id="05e42-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="05e42-114">Vælg en indstilling i feltet Nyt afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="05e42-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="05e42-115">Bekræft, at rapporten udskrives til den ønskede destination.</span><span class="sxs-lookup"><span data-stu-id="05e42-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="05e42-116">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="05e42-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="05e42-117">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="05e42-117">Click Filter.</span></span>
10. <span data-ttu-id="05e42-118">Vælg Anlægsaktivgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="05e42-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="05e42-119">Klik på rullelisten i feltet Kriterier for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="05e42-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="05e42-120">Vælg den ønskede anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="05e42-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="05e42-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="05e42-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="05e42-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="05e42-122">Click OK.</span></span>
15. <span data-ttu-id="05e42-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="05e42-123">Click OK.</span></span>
    *  <span data-ttu-id="05e42-124">Resultaterne af processen vises i rapporten Masseopdatering.</span><span class="sxs-lookup"><span data-stu-id="05e42-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]