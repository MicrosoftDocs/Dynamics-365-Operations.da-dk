---
title: Oprette og tildele en handelspartnerkode i den offentlige sektor
description: Opret en handelspartnerkode, og tildel den til en offentlig myndighed, som din organisation handler med.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustGroup, CustTradingPartnerCode, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cde49d331daa90ddbaed8216a772662323a166d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235573"
---
# <a name="create-and-assign-a-trading-partner-code-in-the-public-sector"></a><span data-ttu-id="b5f41-103">Oprette og tildele en handelspartnerkode i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="b5f41-103">Create and assign a trading partner code in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5f41-104">Opret en handelspartnerkode, og tildel den til en offentlig myndighed, som din organisation handler med.</span><span class="sxs-lookup"><span data-stu-id="b5f41-104">Create a trading partner code and assign it to a government agency that your organization does business with.</span></span> <span data-ttu-id="b5f41-105">Kundeposten for agenturet skal være oprettet, før du kan udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="b5f41-105">The customer record for the agency must exist before you can perform this task.</span></span> <span data-ttu-id="b5f41-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="b5f41-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>


## <a name="create-a-trading-partner-code"></a><span data-ttu-id="b5f41-107">Oprette en handelspartnerkode</span><span class="sxs-lookup"><span data-stu-id="b5f41-107">Create a trading partner code</span></span>
1. <span data-ttu-id="b5f41-108">Gå til Debitor > Opsætning > Handelspartnerkoder.</span><span class="sxs-lookup"><span data-stu-id="b5f41-108">Go to Accounts receivable > Setup > Trading partner codes.</span></span>
2. <span data-ttu-id="b5f41-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b5f41-109">Click New.</span></span>
3. <span data-ttu-id="b5f41-110">Indtast en værdi i feltet Handelspartnerkode.</span><span class="sxs-lookup"><span data-stu-id="b5f41-110">In the Trading partner code field, type a value.</span></span>
    * <span data-ttu-id="b5f41-111">Handelspartnerkoder for regeringskontorer defineres af det amerikanske finans- og skatteministerium.</span><span class="sxs-lookup"><span data-stu-id="b5f41-111">The trading partner codes for government agencies are defined by the United States Department of the Treasury.</span></span>  
4. <span data-ttu-id="b5f41-112">Skriv navnet på den myndighed, der bruger denne kode, i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b5f41-112">In the Description field, type the name of the agency that uses this code..</span></span>
5. <span data-ttu-id="b5f41-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b5f41-113">Click Save.</span></span>

## <a name="assign-a-trading-partner-code"></a><span data-ttu-id="b5f41-114">Tildele en handelspartnerkode</span><span class="sxs-lookup"><span data-stu-id="b5f41-114">Assign a trading partner code</span></span>
1. <span data-ttu-id="b5f41-115">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="b5f41-115">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b5f41-116">Find og vælg den myndighed, en handelspartnerkode skal tildeles til, på listen.</span><span class="sxs-lookup"><span data-stu-id="b5f41-116">In the list, find and select the agency to assign a trading partner code to.</span></span>
3. <span data-ttu-id="b5f41-117">Klik for at følge linket i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="b5f41-117">Click to follow the link in the Name field.</span></span>
4. <span data-ttu-id="b5f41-118">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b5f41-118">Click Edit.</span></span>
5. <span data-ttu-id="b5f41-119">Vis eller skjul sektionen Diverse detaljer.</span><span class="sxs-lookup"><span data-stu-id="b5f41-119">Expand the Miscellaneous details section.</span></span>
6. <span data-ttu-id="b5f41-120">Vælg handelspartnerkoden for denne myndighed i feltet Handelspartnerkode.</span><span class="sxs-lookup"><span data-stu-id="b5f41-120">In the Trading partner code field, select the trading partner code for this agency..</span></span>
7. <span data-ttu-id="b5f41-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b5f41-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]