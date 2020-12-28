---
title: Deaktivere en produktionsflowversion
description: Når en aktiv produktionsflowversion ikke længere er nødvendig, kan den være deaktiveret.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e818d3d75be8b24531afc6280ae0c37eca4de23
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424334"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="629d7-103">Deaktivere en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="629d7-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="629d7-104">Når en aktiv produktionsflowversion ikke længere er nødvendig, kan den være deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="629d7-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="629d7-105">Du skal kun bruge denne indstilling, hvis alle kanban-regler og aktiviteter er afsluttet og ikke aktiveres igen.</span><span class="sxs-lookup"><span data-stu-id="629d7-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="629d7-106">Bemærk, at udløbsdatoen for alle kanban-regler, der er relateret til denne version af produktionsflowet, opdateres med dags dato og det aktuelle klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="629d7-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="629d7-107">Hvis du vil redigere en aktiv produktionsflowversion, kan du overveje at angive en udløbsdato for den aktive version og oprette en ny version.</span><span class="sxs-lookup"><span data-stu-id="629d7-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="629d7-108">Det gør det muligt at fortsætte dine produktionsoperationer, mens du udarbejder den nye version og relaterede kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="629d7-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="629d7-109">For at få en aktiv produktionsflowversion til at udløbe skal du angive en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="629d7-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="629d7-110">Det betyder, at deaktivering er mere en undtagelse end en regel.</span><span class="sxs-lookup"><span data-stu-id="629d7-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="629d7-111">I denne procedure skal du bruge en produktionsflow med en version, der kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="629d7-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="629d7-112">Prøv ikke dette i et produktionsmiljø, medmindre du er 100 % sikker på, at versionen er helt forældet.</span><span class="sxs-lookup"><span data-stu-id="629d7-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="629d7-113">Deaktivere en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="629d7-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="629d7-114">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="629d7-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="629d7-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="629d7-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="629d7-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="629d7-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="629d7-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="629d7-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="629d7-118">Klik på Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="629d7-118">Click Deactivate.</span></span>
    * <span data-ttu-id="629d7-119">Fortsæt ikke, hvis du ikke er 100 % sikker på, at denne version af produktionsflowet er forældet.</span><span class="sxs-lookup"><span data-stu-id="629d7-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="629d7-120">Hvis du klikker på OK, udløber alle aktive kanban-regler, og alle produktions- og genopfyldningsaktiviteter for denne version af produktionsflowet standser øjeblikkeligt.</span><span class="sxs-lookup"><span data-stu-id="629d7-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="629d7-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="629d7-121">Click OK.</span></span>

