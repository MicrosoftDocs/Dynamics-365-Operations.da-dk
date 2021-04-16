---
title: Konfigurer opdeling af opgaver
description: Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745735"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="1050c-103">Konfigurer opdeling af opgaver</span><span class="sxs-lookup"><span data-stu-id="1050c-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1050c-104">Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="1050c-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="1050c-105">Dette begreb kaldes opdeling af opgaver.</span><span class="sxs-lookup"><span data-stu-id="1050c-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="1050c-106">Du ønsker f.eks. ikke, at den samme person både skal bekræfte modtagelsen af varer og behandle betalingen til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="1050c-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="1050c-107">Opdeling af opgaver hjælper dig med at mindske risikoen for svig og også med at registrere fejl eller uregelmæssigheder.</span><span class="sxs-lookup"><span data-stu-id="1050c-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="1050c-108">Du kan også bruge opdeling af opgaver til at gennemtvinge politikker for intern kontrol.</span><span class="sxs-lookup"><span data-stu-id="1050c-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="1050c-109">Fuldfør følgende procedure for at oprette en regel.</span><span class="sxs-lookup"><span data-stu-id="1050c-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="1050c-110">Du skal være systemadministrator for at kunne fuldføre proceduren.</span><span class="sxs-lookup"><span data-stu-id="1050c-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="1050c-111">Gå til **Systemadministration** > **Sikkerhed** > **Opdeling af opgaver** > **Regler for opdeling af opgaver**.</span><span class="sxs-lookup"><span data-stu-id="1050c-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="1050c-112">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1050c-112">Click **New**.</span></span>
3. <span data-ttu-id="1050c-113">Skriv en værdi for reglen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1050c-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="1050c-114">Klik på rullelisten i feltet **Første pligt** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1050c-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1050c-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1050c-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="1050c-116">Vælg den første programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="1050c-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="1050c-117">Klik på rullelisten i feltet **Anden pligt** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1050c-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="1050c-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1050c-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="1050c-119">Vælg den anden programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="1050c-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="1050c-120">Vælg en indstilling i feltet **Alvorsgrad**.</span><span class="sxs-lookup"><span data-stu-id="1050c-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="1050c-121">Vælg alvorligheden af den risiko, der forekommer, når den samme bruger eller rolle udfører begge opgaver.</span><span class="sxs-lookup"><span data-stu-id="1050c-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="1050c-122">Indtast en værdi i feltet **Sikkerhedsrisiko**.</span><span class="sxs-lookup"><span data-stu-id="1050c-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="1050c-123">Angiv en beskrivelse af sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="1050c-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="1050c-124">Indtast en værdi i feltet **Sikkerhedsmitigering**.</span><span class="sxs-lookup"><span data-stu-id="1050c-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="1050c-125">Angiv en beskrivelse af de handlinger, du udfører for at reducere sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="1050c-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="1050c-126">Du kan f.eks. mindske risikoen ved at foretage en mere detaljeret gennemgang af processen, ved at gennemføre en månedlig evaluering på lederniveau eller ved at dele ressourcer med andre afdelinger.</span><span class="sxs-lookup"><span data-stu-id="1050c-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="1050c-127">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1050c-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="1050c-128">Overholdelse af reglerne for opdeling af opgaver kontrolleres ikke, når du opretter en regel.</span><span class="sxs-lookup"><span data-stu-id="1050c-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="1050c-129">Du kan oprette en regel, der skaber en konflikt for eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="1050c-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="1050c-130">Eksisterende brugerrolletildelinger kan også være i konflikt med den nye regel.</span><span class="sxs-lookup"><span data-stu-id="1050c-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="1050c-131">Du skal validere overholdelsen af angivne standarder, når du har oprettet eller redigeret en regel.</span><span class="sxs-lookup"><span data-stu-id="1050c-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="1050c-132">Yderligere oplysninger finder du i [Identificere og løse konflikter i opdeling af opgaver](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="1050c-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]