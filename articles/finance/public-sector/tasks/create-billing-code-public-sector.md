---
title: Oprette en faktureringskode for den offentlige sektor
description: Brugerdefinerede felter til faktureringskoder gør det muligt at indsamle værdier for faktureringskodefelter, når der oprettes fritekstfakturaer.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCustomField
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2fc90010890a4ae55dead4ff4a90e8e8391397d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246829"
---
# <a name="create-a-billing-code-for-the-public-sector"></a><span data-ttu-id="9279e-103">Oprette en faktureringskode for den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="9279e-103">Create a billing code for the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9279e-104">Brugerdefinerede felter til faktureringskoder gør det muligt at indsamle værdier for faktureringskodefelter, når der oprettes fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="9279e-104">Billing code custom fields allow you to collect values for billing code fields when free text invoices are created.</span></span> <span data-ttu-id="9279e-105">Når du har tildelt det brugerdefinerede felt til faktureringskoder, kan brugerne få adgang til feltet, når faktureringskoden vælges på en fritekstfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="9279e-105">After you assign the custom field to billing codes, users can access the field when the billing code is selected on a free text invoice line.</span></span> <span data-ttu-id="9279e-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="9279e-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="9279e-107">Gå til Debitor > Opsætning > Brugerdefinerede felter for faktureringskode.</span><span class="sxs-lookup"><span data-stu-id="9279e-107">Go to Accounts receivable > Setup > Billing code custom fields.</span></span>
2. <span data-ttu-id="9279e-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9279e-108">Click New.</span></span>
3. <span data-ttu-id="9279e-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9279e-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9279e-110">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="9279e-110">In the Type field, select an option.</span></span>
    * <span data-ttu-id="9279e-111">Når du vælger en indstilling, ændres felterne i sektionen Beskrivelse til de indstillinger, der er tilgængelige for denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="9279e-111">When you select an option, the fields in the Description section will change to the settings available for that option.</span></span>  
    * <span data-ttu-id="9279e-112">Angiv standardværdien for dette brugerdefinerede felt og andre værdier, der skal bruges, i afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="9279e-112">In the Details section, enter the default value for this custom field and any other values that are needed.</span></span>  
5. <span data-ttu-id="9279e-113">Åbn afsnittet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9279e-113">Open the Description section.</span></span>
6. <span data-ttu-id="9279e-114">Valgfrit: I feltet Beskrivelse af forbrug kan du beskrive, hvordan det brugerdefinerede felt skal bruges.</span><span class="sxs-lookup"><span data-stu-id="9279e-114">Optional: In the Usage description field, describe how the custom field should be used.</span></span> <span data-ttu-id="9279e-115">Oplysningerne anvendes kun internt.</span><span class="sxs-lookup"><span data-stu-id="9279e-115">This information is for internal purposes only.</span></span> <span data-ttu-id="9279e-116">De er ikke synlige for brugeren.</span><span class="sxs-lookup"><span data-stu-id="9279e-116">It is not visible to the user.</span></span>
7. <span data-ttu-id="9279e-117">Åbn referencesektionen Faktureringskode.</span><span class="sxs-lookup"><span data-stu-id="9279e-117">Open the Billing code references section.</span></span> <span data-ttu-id="9279e-118">Når du tildeler dette brugerdefinerede felt til en faktureringskode, vises den faktureringskoden her.</span><span class="sxs-lookup"><span data-stu-id="9279e-118">When you assign this custom field to a billing code, the billing code will be listed here.</span></span>
8. <span data-ttu-id="9279e-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9279e-119">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]