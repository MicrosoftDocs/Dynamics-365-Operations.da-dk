---
title: Oversigt over positive betalinger
description: "Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5b88b940e7a590ff99b6ab8a99ce45d32dfe0505
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="ffb99-103">Oversigt over positive betalinger</span><span class="sxs-lookup"><span data-stu-id="ffb99-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ffb99-104">Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank.</span><span class="sxs-lookup"><span data-stu-id="ffb99-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="ffb99-105">Positiv betaling bruges til at generere en elektronisk liste over checks, der kan indløses i en bank.</span><span class="sxs-lookup"><span data-stu-id="ffb99-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="ffb99-106">Positive betalingsfiler kan hjælpe banker med at forebygge checkbedrageri.</span><span class="sxs-lookup"><span data-stu-id="ffb99-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="ffb99-107">Du konfigurerer en positiv betaling til at generere en elektronisk liste over checks, hver gang checks udskrives.</span><span class="sxs-lookup"><span data-stu-id="ffb99-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="ffb99-108">Når checken derefter skal indløses hos banken, sammenligner banken checken med den liste over checks, du tidligere har fremsendt.</span><span class="sxs-lookup"><span data-stu-id="ffb99-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="ffb99-109">Hvis checken svarer til en check på listen, indløser banken den.</span><span class="sxs-lookup"><span data-stu-id="ffb99-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="ffb99-110">Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="ffb99-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="ffb99-111">Positiv betaling er også kendt som SafePay.</span><span class="sxs-lookup"><span data-stu-id="ffb99-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="ffb99-112">Filer til positiv betaling kan indeholde følsomme oplysninger om beløbsmodtagere og checkbeløb.</span><span class="sxs-lookup"><span data-stu-id="ffb99-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="ffb99-113">Sørg derfor for, at du bruger passende de sikringsforanstaltninger fra det tidspunkt, hvor filerne genereres, indtil de modtages af banken.</span><span class="sxs-lookup"><span data-stu-id="ffb99-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="ffb99-114">Filer til positive betalinger overføres i henhold til overførselsinstruktionerne for webbrowseren.</span><span class="sxs-lookup"><span data-stu-id="ffb99-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="ffb99-115">Filer til positiv betaling oprettes ved hjælp af dataenheder.</span><span class="sxs-lookup"><span data-stu-id="ffb99-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="ffb99-116">Før du genererer en fil til positiv betaling, skal du angive transformationsformaterne for den XML-filer, der oversætter dataene til et format, som banken kan anvende.</span><span class="sxs-lookup"><span data-stu-id="ffb99-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="ffb99-117">For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele formatet for positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="ffb99-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="ffb99-118">Når du har genereret betalinger, kan du oprette en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ffb99-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="ffb99-119">Du kan også samtidig generere filer til positiv betaling for flere juridiske enheder og bankkonti.</span><span class="sxs-lookup"><span data-stu-id="ffb99-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="ffb99-120">Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank.</span><span class="sxs-lookup"><span data-stu-id="ffb99-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="ffb99-121">Du kan derefter bekræfte filen til positiv betaling i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="ffb99-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="ffb99-122">Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="ffb99-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="ffb99-123">For hver check i filen til positiv betaling, nulstilles derefter det felt, der angiver, om checken er inkluderet i en fil til positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="ffb99-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="ffb99-124">Yderligere oplysninger finder du i afsnittet [Konfigurer og generer filer til positive betalinger](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="ffb99-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




