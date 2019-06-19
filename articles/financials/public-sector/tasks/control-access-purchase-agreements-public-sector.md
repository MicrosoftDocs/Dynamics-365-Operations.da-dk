---
title: Kontrollere adgang til købsaftaler i den offentlige sektor
description: Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementFinDimensionAccess_PSN
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6e3d335b021c366accdca50ed7ce496cefaa47e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557238"
---
# <a name="control-access-to-purchase-agreements-in-the-public-sector"></a><span data-ttu-id="99cb4-103">Kontrollere adgang til købsaftaler i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="99cb4-103">Control access to purchase agreements in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99cb4-104">Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale.</span><span class="sxs-lookup"><span data-stu-id="99cb4-104">You can make sure that only approved departments can access a purchase agreement.</span></span> <span data-ttu-id="99cb4-105">Du kan også begrænse det beløb, som hver afdeling kan bruge forhold til købsaftalen.</span><span class="sxs-lookup"><span data-stu-id="99cb4-105">You can also limit the amount that each department can spend against the purchase agreement.</span></span> <span data-ttu-id="99cb4-106">For at kunne gøre det skal kontostrukturen og de økonomiske dimensioner for afdelingsadgang indstilles i formularen Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="99cb4-106">In order to do this, the account structure and financial dimensions for department access must be set on the Accounts payable parameters form.</span></span> <span data-ttu-id="99cb4-107">Denne procedure er oprettet for franske offentlige organisationer med data fra PSUS-demofirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="99cb4-107">This procedure was created for French public sector organizations using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="99cb4-108">Gå til Kreditor > Indkøbsordrer > Købsaftaler.</span><span class="sxs-lookup"><span data-stu-id="99cb4-108">Go to Accounts payable > Purchase orders > Purchase agreements.</span></span>
2. <span data-ttu-id="99cb4-109">Vælg den indkøbsordre, du vil styre adgangen til, på listen.</span><span class="sxs-lookup"><span data-stu-id="99cb4-109">In the list, select the purchase agreement that you want to control access to.</span></span>
3. <span data-ttu-id="99cb4-110">Klik på Købsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="99cb4-110">On the Action Pane, click Purchase agreement.</span></span>
4. <span data-ttu-id="99cb4-111">Klik på Afdelingsadgang.</span><span class="sxs-lookup"><span data-stu-id="99cb4-111">Click Department access.</span></span>
5. <span data-ttu-id="99cb4-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="99cb4-112">Click New.</span></span>
6. <span data-ttu-id="99cb4-113">Klik på rullelisten i feltet Afdeling for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="99cb4-113">In the Department field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="99cb4-114">Vælg den økonomiske dimension for en afdeling, der har adgang til denne købsaftale, på listen.</span><span class="sxs-lookup"><span data-stu-id="99cb4-114">In the list, select the financial dimension for a department that has access to this purchase agreement.</span></span>
8. <span data-ttu-id="99cb4-115">Angiv det samlede beløb, som denne afdeling er autoriseret til at frigive fra denne købsaftale, i feltet Godkendt beløb.</span><span class="sxs-lookup"><span data-stu-id="99cb4-115">In the Authorized amount field, enter the total amount that this department is authorized to release from this purchase agreement.</span></span>
    * <span data-ttu-id="99cb4-116">Tilføj flere afdelinger, indtil alle autoriserede afdelinger er føjet til købsaftalen.</span><span class="sxs-lookup"><span data-stu-id="99cb4-116">Add additional departments until all authorized departments have been added to the purchase agreement.</span></span>  
9. <span data-ttu-id="99cb4-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="99cb4-117">Click Save.</span></span>

