---
title: Konfigurer opdeling af opgaver
description: Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982400"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="fdf7f-103">Konfigurer opdeling af opgaver</span><span class="sxs-lookup"><span data-stu-id="fdf7f-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fdf7f-104">Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="fdf7f-105">Dette begreb kaldes opdeling af opgaver.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="fdf7f-106">Du ønsker f.eks. ikke, at den samme person både skal bekræfte modtagelsen af varer og behandle betalingen til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="fdf7f-107">Opdeling af opgaver hjælper dig med at mindske risikoen for svig og også med at registrere fejl eller uregelmæssigheder.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="fdf7f-108">Du kan også bruge opdeling af opgaver til at gennemtvinge politikker for intern kontrol.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="fdf7f-109">Fuldfør følgende procedure for at oprette en regel.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="fdf7f-110">Du skal være systemadministrator for at kunne fuldføre proceduren.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="fdf7f-111">Det demodatafirma, der bruges til at oprette denne procedure, er DAT.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="fdf7f-112">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Opdeling af opgaver > Regler for opdeling af opgaver.**</span><span class="sxs-lookup"><span data-stu-id="fdf7f-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="fdf7f-113">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-113">Click **New**.</span></span>
3. <span data-ttu-id="fdf7f-114">Skriv en værdi for reglen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="fdf7f-115">Klik på rullelisten i feltet **Første pligt** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fdf7f-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="fdf7f-117">Vælg den første programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="fdf7f-118">Klik på rullelisten i feltet **Anden pligt** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="fdf7f-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="fdf7f-120">Vælg den anden programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="fdf7f-121">Vælg en indstilling i feltet **Alvorsgrad**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="fdf7f-122">Vælg alvorligheden af den risiko, der forekommer, når den samme bruger eller rolle udfører begge opgaver.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="fdf7f-123">Indtast en værdi i feltet **Sikkerhedsrisiko**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="fdf7f-124">Angiv en beskrivelse af sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="fdf7f-125">Indtast en værdi i feltet **Sikkerhedsmitigering**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="fdf7f-126">Angiv en beskrivelse af de handlinger, du udfører for at reducere sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="fdf7f-127">Du kan f.eks. mindske risikoen ved at foretage en mere detaljeret gennemgang af processen, ved at gennemføre en månedlig evaluering på lederniveau eller ved at dele ressourcer med andre afdelinger.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="fdf7f-128">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fdf7f-128">Click **Save**.</span></span>

