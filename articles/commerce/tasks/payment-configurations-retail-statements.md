---
title: " Betalingskonfigurationer for detailopgørelser"
description: Denne procedure viser konfigurationer af betalingsmetoder for Commerce-butikker, der påvirker, hvordan opgørelser oprettes og bogføres.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982309"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="23d3e-103"> Betalingskonfigurationer for detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="23d3e-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23d3e-104">Denne procedure viser konfigurationer af betalingsmetoder for Commerce-butikker, der påvirker, hvordan opgørelser oprettes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="23d3e-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="23d3e-105">Denne registrering anvender demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="23d3e-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="23d3e-106">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="23d3e-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="23d3e-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="23d3e-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="23d3e-108">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23d3e-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="23d3e-109">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="23d3e-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="23d3e-110">Klik på Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="23d3e-110">Click Payment methods.</span></span>
6. <span data-ttu-id="23d3e-111">Udvid eller skjul sektionen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="23d3e-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="23d3e-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="23d3e-112">Click Edit.</span></span>
    * <span data-ttu-id="23d3e-113">Vælg, om de beløb, der er modtaget for denne betalingsmetode, skal bogføres på en finanskonto eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="23d3e-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="23d3e-114">Vælg den konto, som beløb, der er modtaget til denne betalingsmetode, skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="23d3e-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="23d3e-115">Vælg en konto for at bogføre eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det beløb, der er optalt for denne betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="23d3e-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="23d3e-116">I dette felt angiver du et beløb til at styre, når differencebeløbet skal bogføres til en anden differencekonto.</span><span class="sxs-lookup"><span data-stu-id="23d3e-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="23d3e-117">Du kan bruge til at spore store forskelle.</span><span class="sxs-lookup"><span data-stu-id="23d3e-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="23d3e-118">Vælg en konto til bogføring af eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det optalte beløbs, når den overstiger den værdi, der er defineret i feltet "Maksimale differencebeløb".</span><span class="sxs-lookup"><span data-stu-id="23d3e-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="23d3e-119">Vælg "Ja" for at bogføre beløb til indsættelse i bank på en separat konto.</span><span class="sxs-lookup"><span data-stu-id="23d3e-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="23d3e-120">I dette felt kan du vælge, om beløb til indsættelse i bank skal bogføres på en finanskonto eller en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="23d3e-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="23d3e-121">Vælg den konto, som beløb til indsættelse i bank skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="23d3e-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="23d3e-122">Vælg den bankposteringstype, der skal bruges ved bogføring af beløb til indsættelse i bank på bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="23d3e-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="23d3e-123">Vælg "Ja" for at bogføre deponering til pengeskab på en separat konto.</span><span class="sxs-lookup"><span data-stu-id="23d3e-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="23d3e-124">Vælg om deponeringer til pengeskab skal bogføres på finanskontoen eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="23d3e-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="23d3e-125">Vælg den konto, som deponeringer til pengeskab skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="23d3e-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="23d3e-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="23d3e-126">Click Save.</span></span>

