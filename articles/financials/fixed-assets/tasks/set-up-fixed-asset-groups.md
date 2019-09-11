---
title: Konfigurere anlægsaktivgrupper
description: I dette emne beskrives, hvordan du opretter en ny anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867529"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="fd92c-103">Konfigurere anlægsaktivgrupper</span><span class="sxs-lookup"><span data-stu-id="fd92c-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd92c-104">I dette emne beskrives, hvordan du opretter en ny anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="fd92c-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="fd92c-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="fd92c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="fd92c-106">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Opsætning > Anlægsaktivgrupper**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="fd92c-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-107">Select **New**.</span></span>
3. <span data-ttu-id="fd92c-108">Indtast en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="fd92c-109">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="fd92c-110">Autonummerer anlægsaktiver og Nummerseriekode i **Anlægsaktiv**-gruppen tilsidesætter indstillingerne for parametrene for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="fd92c-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="fd92c-111">Du kan ændre den her, hvis aktiver i denne anlægsaktivgruppe får anden nummerering end andre grupper.</span><span class="sxs-lookup"><span data-stu-id="fd92c-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="fd92c-112">Vælg **Bøger**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-112">Select **Books**.</span></span>
6. <span data-ttu-id="fd92c-113">Indtast eller vælg en værdi i feltet **Bog**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="fd92c-114">Hvis feltet **Beregn afskrivning** er indstillet til **Ja**, medtages aktivbogen i afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="fd92c-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="fd92c-115">Hvis **Beregn afskrivning** er indstillet til **Nej**, afskrives aktivet ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="fd92c-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="fd92c-116">Angiv aktivets levetid i år.</span><span class="sxs-lookup"><span data-stu-id="fd92c-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="fd92c-117">Bemærk, at værdien i feltet **Afskrivningsperioder** beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="fd92c-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="fd92c-118">Vælg en indstilling i feltet **Afskrivningsprincip**.</span><span class="sxs-lookup"><span data-stu-id="fd92c-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="fd92c-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fd92c-119">Close the page.</span></span>

