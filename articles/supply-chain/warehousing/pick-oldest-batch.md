---
title: "Pluk det ældste batch på en mobilenhed"
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende indstillingerne for at plukke det ældste batch fra en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="e9c50-103">Pluk det ældste batch på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="e9c50-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9c50-104">Du kan få adgang til konfigurationen af **Pluk den ældste batch** via en menu på mobilenhed, og det giver dig mulighed at tvinge lagermedarbejdere til eller advare dem mod at plukke det ældste batch på deres aktuelle placering.</span><span class="sxs-lookup"><span data-stu-id="e9c50-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="e9c50-105">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="e9c50-105">Where it applies</span></span>
<span data-ttu-id="e9c50-106">Vælg den ældste batch konfigureres i menupunkter på en mobilenhed og påvirker pluk for-batchet under varer.</span><span class="sxs-lookup"><span data-stu-id="e9c50-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="e9c50-107">Sådan indstilles konfigurationen for Pluk den ældste batch</span><span class="sxs-lookup"><span data-stu-id="e9c50-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="e9c50-108">For varer, der er indstillet til at bruge eksisterende arbejde, kan **Pluk den ældste batch** indstilles til **Ingen**, **Advar** eller **Gennemtving** fra en menu på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e9c50-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="e9c50-109">**Ingen**: Arbejdere modtager ingen meddelelser, og de kan plukke ethvert batch på deres placering.</span><span class="sxs-lookup"><span data-stu-id="e9c50-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="e9c50-110">**Advar** og **Gennemtving**: Der vises en liste over batches med den ældste udløbsdato over batchkontrolelementet, når arbejderen vælger et batch.</span><span class="sxs-lookup"><span data-stu-id="e9c50-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="e9c50-111">Hvis placeringen er id-kontrolleret, vises en liste over id'er, der har det ældste batch, over id-kontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="e9c50-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="e9c50-112">**Advar**: Hvis en arbejder vælger et id eller et batch, der ikke findes på listen, er kontrolelement tomt, og der vises en advarsel om, at et ældre batch kan vælges.</span><span class="sxs-lookup"><span data-stu-id="e9c50-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="e9c50-113">Hvis arbejderen vil have mulighed for at fortsætte arbejdet, kan vedkommende vælge det samme id eller batch igen.</span><span class="sxs-lookup"><span data-stu-id="e9c50-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="e9c50-114">**Gennemtving**: Arbejdere kan fortsat modtage meddelelsen om, at et ældre batch skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="e9c50-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

