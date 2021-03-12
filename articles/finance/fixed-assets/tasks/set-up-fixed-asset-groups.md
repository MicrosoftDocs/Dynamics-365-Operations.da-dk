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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4eead36e1274194b151b230767a4d6385173b12f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994834"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="f0d30-103">Konfigurere anlægsaktivgrupper</span><span class="sxs-lookup"><span data-stu-id="f0d30-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0d30-104">I dette emne beskrives, hvordan du opretter en ny anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0d30-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="f0d30-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="f0d30-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f0d30-106">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Opsætning > Anlægsaktivgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="f0d30-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-107">Select **New**.</span></span>
3. <span data-ttu-id="f0d30-108">Indtast en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="f0d30-109">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="f0d30-110">Autonummerer anlægsaktiver og Nummerseriekode i **Anlægsaktiv**-gruppen tilsidesætter indstillingerne for parametrene for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="f0d30-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="f0d30-111">Du kan ændre den her, hvis aktiver i denne anlægsaktivgruppe får anden nummerering end andre grupper.</span><span class="sxs-lookup"><span data-stu-id="f0d30-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="f0d30-112">Vælg **Bøger**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-112">Select **Books**.</span></span>
6. <span data-ttu-id="f0d30-113">Indtast eller vælg en værdi i feltet **Bog**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="f0d30-114">Hvis feltet **Beregn afskrivning** er indstillet til **Ja**, medtages aktivbogen i afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="f0d30-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="f0d30-115">Hvis **Beregn afskrivning** er indstillet til **Nej**, afskrives aktivet ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="f0d30-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="f0d30-116">Angiv aktivets levetid i år.</span><span class="sxs-lookup"><span data-stu-id="f0d30-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="f0d30-117">Bemærk, at værdien i feltet **Afskrivningsperioder** beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="f0d30-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="f0d30-118">Vælg en indstilling i feltet **Afskrivningsprincip**.</span><span class="sxs-lookup"><span data-stu-id="f0d30-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="f0d30-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0d30-119">Close the page.</span></span>

