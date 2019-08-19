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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daff3a231fbacf803cebf4311d5d98fdd7305ab6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836032"
---
# <a name="create-a-billing-code-for-the-public-sector"></a><span data-ttu-id="ca9fc-103">Oprette en faktureringskode for den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="ca9fc-103">Create a billing code for the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca9fc-104">Brugerdefinerede felter til faktureringskoder gør det muligt at indsamle værdier for faktureringskodefelter, når der oprettes fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-104">Billing code custom fields allow you to collect values for billing code fields when free text invoices are created.</span></span> <span data-ttu-id="ca9fc-105">Når du har tildelt det brugerdefinerede felt til faktureringskoder, kan brugerne få adgang til feltet, når faktureringskoden vælges på en fritekstfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-105">After you assign the custom field to billing codes, users can access the field when the billing code is selected on a free text invoice line.</span></span> <span data-ttu-id="ca9fc-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="ca9fc-107">Gå til Debitor > Opsætning > Brugerdefinerede felter for faktureringskode.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-107">Go to Accounts receivable > Setup > Billing code custom fields.</span></span>
2. <span data-ttu-id="ca9fc-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-108">Click New.</span></span>
3. <span data-ttu-id="ca9fc-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ca9fc-110">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-110">In the Type field, select an option.</span></span>
    * <span data-ttu-id="ca9fc-111">Når du vælger en indstilling, ændres felterne i sektionen Beskrivelse til de indstillinger, der er tilgængelige for denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-111">When you select an option, the fields in the Description section will change to the settings available for that option.</span></span>  
    * <span data-ttu-id="ca9fc-112">Angiv standardværdien for dette brugerdefinerede felt og andre værdier, der skal bruges, i afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-112">In the Details section, enter the default value for this custom field and any other values that are needed.</span></span>  
5. <span data-ttu-id="ca9fc-113">Åbn afsnittet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-113">Open the Description section.</span></span>
6. <span data-ttu-id="ca9fc-114">Valgfrit: I feltet Beskrivelse af forbrug kan du beskrive, hvordan det brugerdefinerede felt skal bruges.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-114">Optional: In the Usage description field, describe how the custom field should be used.</span></span> <span data-ttu-id="ca9fc-115">Oplysningerne anvendes kun internt.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-115">This information is for internal purposes only.</span></span> <span data-ttu-id="ca9fc-116">De er ikke synlige for brugeren.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-116">It is not visible to the user.</span></span>
7. <span data-ttu-id="ca9fc-117">Åbn referencesektionen Faktureringskode.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-117">Open the Billing code references section.</span></span> <span data-ttu-id="ca9fc-118">Når du tildeler dette brugerdefinerede felt til en faktureringskode, vises den faktureringskoden her.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-118">When you assign this custom field to a billing code, the billing code will be listed here.</span></span>
8. <span data-ttu-id="ca9fc-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-119">Click Save.</span></span>

