--- 
title: " Betalingskonfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for betalingsmetoder for detailbutikker, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 51faf6d45fde8aa7e2adad69306891f17c943e85
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="6850d-103"> Betalingskonfigurationer for detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="6850d-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6850d-104">Denne procedure viser konfigurationer for betalingsmetoder for detailbutikker, der påvirker, hvordan detailopgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="6850d-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="6850d-105">Denne registrering anvender demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="6850d-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="6850d-106">Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="6850d-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="6850d-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6850d-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6850d-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6850d-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6850d-109">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6850d-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="6850d-110">Klik på Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="6850d-110">Click Payment methods.</span></span>
6. <span data-ttu-id="6850d-111">Udvid eller skjul sektionen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="6850d-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="6850d-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="6850d-112">Click Edit.</span></span>
    * <span data-ttu-id="6850d-113">Vælg, om de beløb, der er modtaget for denne betalingsmetode, skal bogføres på en finanskonto eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="6850d-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="6850d-114">Vælg den konto, som beløb, der er modtaget til denne betalingsmetode, skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="6850d-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="6850d-115">Vælg en konto for at bogføre eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det beløb, der er optalt for denne betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="6850d-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="6850d-116">I dette felt angiver du et beløb til at styre, når differencebeløbet skal bogføres til en anden differencekonto.</span><span class="sxs-lookup"><span data-stu-id="6850d-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="6850d-117">Du kan bruge til at spore store forskelle.</span><span class="sxs-lookup"><span data-stu-id="6850d-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="6850d-118">Vælg en konto til bogføring af eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det optalte beløbs, når den overstiger den værdi, der er defineret i feltet "Maksimale differencebeløb".</span><span class="sxs-lookup"><span data-stu-id="6850d-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="6850d-119">Vælg "Ja" for at bogføre beløb til indsættelse i bank på en separat konto.</span><span class="sxs-lookup"><span data-stu-id="6850d-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="6850d-120">I dette felt kan du vælge, om beløb til indsættelse i bank skal bogføres på en finanskonto eller en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="6850d-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="6850d-121">Vælg den konto, som beløb til indsættelse i bank skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="6850d-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="6850d-122">Vælg den bankposteringstype, der skal bruges ved bogføring af beløb til indsættelse i bank på bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="6850d-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="6850d-123">Vælg "Ja" for at bogføre deponering til pengeskab på en separat konto.</span><span class="sxs-lookup"><span data-stu-id="6850d-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="6850d-124">Vælg om deponeringer til pengeskab skal bogføres på finanskontoen eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="6850d-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="6850d-125">Vælg den konto, som deponeringer til pengeskab skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="6850d-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="6850d-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6850d-126">Click Save.</span></span>


