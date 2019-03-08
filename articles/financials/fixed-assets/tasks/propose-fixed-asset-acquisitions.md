---
title: Foreslå anskaffelser af anlægsaktiver
description: Denne procedure viser, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i anlægsaktivkladden.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "350636"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="154cd-103">Foreslå anskaffelser af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="154cd-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="154cd-104">Denne procedure viser, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i anlægsaktivkladden.</span><span class="sxs-lookup"><span data-stu-id="154cd-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="154cd-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="154cd-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="154cd-106">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="154cd-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="154cd-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="154cd-107">Click New.</span></span>
3. <span data-ttu-id="154cd-108">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="154cd-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="154cd-109">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="154cd-109">Click Lines.</span></span>
5. <span data-ttu-id="154cd-110">Klik på Forslag.</span><span class="sxs-lookup"><span data-stu-id="154cd-110">Click Proposals.</span></span>
6. <span data-ttu-id="154cd-111">Klik på Anskaffelsesforslag.</span><span class="sxs-lookup"><span data-stu-id="154cd-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="154cd-112">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="154cd-112">Click Filter.</span></span>
8. <span data-ttu-id="154cd-113">Klik på Nulstil for at rydde tidligere værdier.</span><span class="sxs-lookup"><span data-stu-id="154cd-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="154cd-114">Vælg rækken med anlægsaktivnummeret.</span><span class="sxs-lookup"><span data-stu-id="154cd-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="154cd-115">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="154cd-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="154cd-116">Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.</span><span class="sxs-lookup"><span data-stu-id="154cd-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="154cd-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="154cd-117">Click OK.</span></span>
12. <span data-ttu-id="154cd-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="154cd-118">Click OK.</span></span>
    * <span data-ttu-id="154cd-119">Bekræft de oprettede transaktionslinjer.</span><span class="sxs-lookup"><span data-stu-id="154cd-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="154cd-120">Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="154cd-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="154cd-121">Klik på fanen Bøger.</span><span class="sxs-lookup"><span data-stu-id="154cd-121">Click the Books tab.</span></span>
14. <span data-ttu-id="154cd-122">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="154cd-122">Click Post.</span></span>

