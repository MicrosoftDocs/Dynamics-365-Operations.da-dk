---
title: Konfigurer anlægsaktivgrupper
description: Denne procedure viser, hvordan du opretter en ny anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48784ef4eb12a4a1cae3387e3a45afdf34f2a0fd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546426"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="eed9c-103">Konfigurer anlægsaktivgrupper</span><span class="sxs-lookup"><span data-stu-id="eed9c-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eed9c-104">Denne procedure viser, hvordan du opretter en ny anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="eed9c-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="eed9c-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="eed9c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="eed9c-106">Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="eed9c-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="eed9c-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="eed9c-107">Click New.</span></span>
3. <span data-ttu-id="eed9c-108">Indtast en værdi i feltet Anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="eed9c-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="eed9c-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="eed9c-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eed9c-110">Autonummerer anlægsaktiver og Nummerseriekode i anlægsaktivgruppen tilsidesætter indstillingerne for parametrene for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="eed9c-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="eed9c-111">Du kan ændre den her, hvis aktiver i denne anlægsaktivgruppe får anden nummerering end andre grupper.</span><span class="sxs-lookup"><span data-stu-id="eed9c-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="eed9c-112">Klik på Bøger.</span><span class="sxs-lookup"><span data-stu-id="eed9c-112">Click Books.</span></span>
6. <span data-ttu-id="eed9c-113">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="eed9c-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="eed9c-114">Hvis feltet Beregn afskrivning er angivet til Ja, medtages aktivbogen i afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="eed9c-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="eed9c-115">Hvis Beregn afskrivning er angivet til Nej, afskrives aktivet ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="eed9c-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="eed9c-116">Angiv aktivets levetid i år.</span><span class="sxs-lookup"><span data-stu-id="eed9c-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="eed9c-117">Bemærk, at værdien i feltet Afskrivningsperioder beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="eed9c-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="eed9c-118">Vælg en indstilling i feltet Afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="eed9c-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="eed9c-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="eed9c-119">Close the page.</span></span>

