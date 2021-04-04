---
title: Administrere orlov
description: Denne procedure fører gennem oprettelse af poster for medarbejderorlov.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c07a14e5d49e5a6979043d19f6031732eadbad1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567158"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="2ba8c-103">Administrere orlov</span><span class="sxs-lookup"><span data-stu-id="2ba8c-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ba8c-104">Denne procedure fører gennem oprettelse af poster for medarbejderorlov.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="2ba8c-105">Du kan spore orlovstid af årsager, som omfatter medicinske, uddannelsesmæssig eller forældrerelaterede aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="2ba8c-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2ba8c-107">Gå til Personale > Arbejdere > Medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="2ba8c-108">Vælg en medarbejder på listen.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="2ba8c-109">Få vist detaljerede oplysninger for den valgte medarbejder ved at vælge medarbejderens navn.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="2ba8c-110">Klik på fanen Ansættelse.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="2ba8c-111">Klik på Orlov.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-111">Click Leave.</span></span>
6. <span data-ttu-id="2ba8c-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-112">Click New.</span></span>
7. <span data-ttu-id="2ba8c-113">Klik på rullelisten i feltet Orlovstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2ba8c-114">Du kan knytte en orlovstype til en lønkode i formen Orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="2ba8c-115">Hvis en orlovstype er knyttet til en lønkode, oprettes der en lønpost med den tilknyttede lønkode under den orlovsperiode, du angiver.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="2ba8c-116">Vælg en orlovstype på listen.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="2ba8c-117">For eksempel: Adoption</span><span class="sxs-lookup"><span data-stu-id="2ba8c-117">For example: Adoption</span></span>  
9. <span data-ttu-id="2ba8c-118">Angiv den dato, hvor orloven skal starte.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="2ba8c-119">Eksempel: "26-10-2015"</span><span class="sxs-lookup"><span data-stu-id="2ba8c-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="2ba8c-120">For eksempel: 26-10-2015</span><span class="sxs-lookup"><span data-stu-id="2ba8c-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="2ba8c-121">Angiv den dato, hvor orloven skal starte.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="2ba8c-122">For eksempel: 20-11-2015</span><span class="sxs-lookup"><span data-stu-id="2ba8c-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="2ba8c-123">Indtast en beskrivelse i notatfeltet.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="2ba8c-124">For eksempel: Orlov på grund af adoption</span><span class="sxs-lookup"><span data-stu-id="2ba8c-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="2ba8c-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2ba8c-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]