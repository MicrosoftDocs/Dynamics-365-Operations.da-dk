--- 
title: Konfigurer opdeling af opgaver
description: "Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0e20272f09cc8c75bdd93ebcc996cf58b98ccf67
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="81c2f-103">Konfigurer opdeling af opgaver</span><span class="sxs-lookup"><span data-stu-id="81c2f-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81c2f-104">Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="81c2f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="81c2f-105">Dette begreb kaldes opdeling af opgaver.</span><span class="sxs-lookup"><span data-stu-id="81c2f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="81c2f-106">Du ønsker f.eks. ikke, at den samme person både skal bekræfte modtagelsen af varer og behandle betalingen til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="81c2f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="81c2f-107">Opdeling af opgaver hjælper dig med at mindske risikoen for svig og også med at registrere fejl eller uregelmæssigheder.</span><span class="sxs-lookup"><span data-stu-id="81c2f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="81c2f-108">Du kan også bruge opdeling af opgaver til at gennemtvinge politikker for intern kontrol.</span><span class="sxs-lookup"><span data-stu-id="81c2f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="81c2f-109">Fuldfør følgende procedure for at oprette en regel.</span><span class="sxs-lookup"><span data-stu-id="81c2f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="81c2f-110">Du skal være systemadministrator for at kunne fuldføre proceduren.</span><span class="sxs-lookup"><span data-stu-id="81c2f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="81c2f-111">Det demodatafirma, der bruges til at oprette denne procedure, er DAT.</span><span class="sxs-lookup"><span data-stu-id="81c2f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="81c2f-112">Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Regler for opdeling af opgaver.</span><span class="sxs-lookup"><span data-stu-id="81c2f-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="81c2f-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="81c2f-113">Click New.</span></span>
3. <span data-ttu-id="81c2f-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="81c2f-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="81c2f-115">Angiv et navn til reglen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="81c2f-116">Klik på rullelisten i feltet Første opgave for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="81c2f-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="81c2f-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81c2f-118">Vælg den første programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="81c2f-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="81c2f-120">Klik på rullelisten i feltet Anden opgave for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="81c2f-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="81c2f-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81c2f-122">Vælg den anden programadgangsrettighed, der styres af reglen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="81c2f-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="81c2f-124">Vælg en indstilling i feltet Alvorsgrad.</span><span class="sxs-lookup"><span data-stu-id="81c2f-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="81c2f-125">Vælg alvorligheden af den risiko, der forekommer, når den samme bruger eller rolle udfører begge opgaver.</span><span class="sxs-lookup"><span data-stu-id="81c2f-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="81c2f-126">Indtast en værdi i feltet Sikkerhedsrisiko.</span><span class="sxs-lookup"><span data-stu-id="81c2f-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="81c2f-127">Angiv en beskrivelse af sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="81c2f-128">Indtast en værdi i feltet Sikkerhedsmitigering.</span><span class="sxs-lookup"><span data-stu-id="81c2f-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="81c2f-129">Angiv en beskrivelse af de handlinger, du udfører for at reducere sikkerhedsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="81c2f-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="81c2f-130">Du kan f.eks. mindske risikoen ved at foretage en mere detaljeret gennemgang af processen, ved at gennemføre en månedlig evaluering på lederniveau eller ved at dele ressourcer med andre afdelinger.</span><span class="sxs-lookup"><span data-stu-id="81c2f-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="81c2f-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="81c2f-131">Click Save.</span></span>


