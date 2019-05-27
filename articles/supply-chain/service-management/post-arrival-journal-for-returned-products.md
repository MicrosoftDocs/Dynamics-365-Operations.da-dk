---
title: Bogføre modtagelseskladde for returnerede produkter
description: Bogføre modtagelseskladde for returnerede produkter.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75f37ce016acb4b479a9cf4dff205562ce00f02c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545307"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="e6d4a-103">Bogføre modtagelseskladde for returnerede produkter</span><span class="sxs-lookup"><span data-stu-id="e6d4a-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e6d4a-104">Hvis du skal behandle varer, der er sendt retur, skal du først kontrollere det returnerede vareantal og opdatere antalsfeltet i varemodtagelseskladden.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="e6d4a-105">Derefter skal du vælge en dispositionskode eller angive, at de returnerede varer skal inspiceres.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="e6d4a-106">Når du har udført disse trin, kan du bogføre varemodtagelseskladden for returordren.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="e6d4a-107">Klik på **Lagerstyring** \> **Periodisk** \> **Modtagelsesoversigt**.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="e6d4a-108">I filteret **Opsætningsnavn** skal du vælge **Returordre**.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="e6d4a-109">Hvis listen over modtagere er lang, skal du bruge felterne i området **Afgrænsning** til at indsnævre listen.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="e6d4a-110">Find linjen for den returordre, du vil bogføre, markér afkrydsningsfeltet **Vælg til modtagelse** for linjen, og klik derefter på **Start modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="e6d4a-111">Klik på **Kladder** \> **Vis modtagelser fra tilgange** for at åbne formularen **Lokationskladde**.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="e6d4a-112">Vælg en kladde, og klik derefter på <STRONG>Linjer</STRONG> for at få vist detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="e6d4a-113">Foretag de nødvendige opdateringer, og klik derefter på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="e6d4a-114">Når kladden er bogført, er de returnerede varer registreret i lageret, og det angives i formularen **Returordrer**, at varerne er modtaget på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="e6d4a-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6d4a-115">Se også</span><span class="sxs-lookup"><span data-stu-id="e6d4a-115">See also</span></span>

<span data-ttu-id="e6d4a-116">[Lokationskladde (form)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e6d4a-116">[Location journal (form)](https://technet.microsoft.com/en-us/library/aa584822\(v=ax.60\))</span></span>

  


