---
title: Afbrudt forbindelse til Talent-klient
description: I dette emne beskrives, hvad du skal gøre, hvis kundens forbindelse til det lokale miljø afbrydes, og kunden ikke kender årsagen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898451"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="1256c-103">Afbrudt forbindelse til Talent-klient</span><span class="sxs-lookup"><span data-stu-id="1256c-103">Talent client disconnects</span></span>

<span data-ttu-id="1256c-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="1256c-104">**Environment details**</span></span> 

<span data-ttu-id="1256c-105">Dette problem kan opstå i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="1256c-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="1256c-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="1256c-106">**Symptom**</span></span> 

<span data-ttu-id="1256c-107">Kundens forbindelse til det lokale miljø afbrydes, og kunden kender ikke årsagen.</span><span class="sxs-lookup"><span data-stu-id="1256c-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="1256c-108">Kunden modtager en af følgende fejlmeddelelser:</span><span class="sxs-lookup"><span data-stu-id="1256c-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="1256c-109">Din forbindelse er blevet afbrudt.</span><span class="sxs-lookup"><span data-stu-id="1256c-109">We've lost your connection.</span></span> <span data-ttu-id="1256c-110">Klik på Luk for at fortsætte med at arbejde.</span><span class="sxs-lookup"><span data-stu-id="1256c-110">Click Close to continue working.</span></span>
- <span data-ttu-id="1256c-111">Du ser ud til at have mistet netværksforbindelsen. Klik på Prøv igen.</span><span class="sxs-lookup"><span data-stu-id="1256c-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="1256c-112">**Rødt flag**</span><span class="sxs-lookup"><span data-stu-id="1256c-112">**Red flag**</span></span>

<span data-ttu-id="1256c-113">Dette problem opstår ofte, når brugerne er i implementeringsstadiet, sammenligner oplysninger på tværs af produktions- og testmiljøer og glemmer, at de skifter fra den ene session til den anden.</span><span class="sxs-lookup"><span data-stu-id="1256c-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="1256c-114">Hvis brugerne er på dette stadie, vil de højst sandsynligt opleve dette problem.</span><span class="sxs-lookup"><span data-stu-id="1256c-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="1256c-115">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="1256c-115">**Issue**</span></span> 

<span data-ttu-id="1256c-116">**Browsertyper:** Google Chrome, Internet Explorer og Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1256c-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="1256c-117">Microsoft Dynamics 365 Talent afbryder brugerne, når to forskellige sessioner er åbne på samme tid for den samme bruger, og den samme browsertype.</span><span class="sxs-lookup"><span data-stu-id="1256c-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="1256c-118">(F.eks. har bruger A åbnet både miljø 1 og miljø 2 i Chrome). Det er ligegyldigt, om brugerne åbner andre browservinduer eller andre faner.</span><span class="sxs-lookup"><span data-stu-id="1256c-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="1256c-119">Hvis de samme brugerlegitimationsoplysninger bruges til at logge på både miljø 1 og miljø 2 på samme tid og i samme browsertype, så afbryder Talent forbindelsen til en af sessionerne.</span><span class="sxs-lookup"><span data-stu-id="1256c-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="1256c-120">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="1256c-120">**Solution**</span></span>

<span data-ttu-id="1256c-121">Kontroller, at det kun ét miljø er åbent ad gangen for en bestemt browsertype.</span><span class="sxs-lookup"><span data-stu-id="1256c-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="1256c-122">Brugerne kan åbne flere sessioner til det samme miljø (dvs. flere faner i den samme browser).</span><span class="sxs-lookup"><span data-stu-id="1256c-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="1256c-123">Brugere, som vil springe mellem to miljøer på samme tid, skal åbne de enkelte miljøer i hver sin browsertyper.</span><span class="sxs-lookup"><span data-stu-id="1256c-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="1256c-124">(F.eks. kan bruger A få vist miljø 1 i Chrome og miljø 2 i Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="1256c-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
