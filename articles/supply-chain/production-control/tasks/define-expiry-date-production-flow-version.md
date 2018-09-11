--- 
title: "Definere en udløbsdato for en produktionsflowversion"
description: "For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5e12843f9ab12c039c962a9033e3c0187c46bb15
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="60fc3-103">Definere en udløbsdato for en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="60fc3-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60fc3-104">For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="60fc3-105">Det er ikke nødvendigt at deaktivere versionen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="60fc3-106">Angiv en udløbsdato for at afslutte en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="60fc3-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="60fc3-107">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="60fc3-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="60fc3-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="60fc3-109">Vælg et produktionsflow med en version, der allerede er defineret.</span><span class="sxs-lookup"><span data-stu-id="60fc3-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="60fc3-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="60fc3-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="60fc3-111">Click Edit.</span></span>
5. <span data-ttu-id="60fc3-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="60fc3-113">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="60fc3-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="60fc3-114">For udløbsdatoen starter der ikke eller deaktiveres der ikke en ny version.</span><span class="sxs-lookup"><span data-stu-id="60fc3-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="60fc3-115">Det vil heller ikke længere være muligt at oprette eller starte job for denne produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="60fc3-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="60fc3-116">Du kan stadig fuldføre igangsatte job efter udløbsdatoen.</span><span class="sxs-lookup"><span data-stu-id="60fc3-116">You can still complete started jobs after the expiration date.</span></span>  


