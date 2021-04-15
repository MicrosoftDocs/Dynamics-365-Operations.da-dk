---
title: Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales
description: Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 364cc5adf0358ffa952750149ad31d62cbd35e87
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751428"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="365ba-103">Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="365ba-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="365ba-104">Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="365ba-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="365ba-105">Dynamics 365 Commerce-prissætningsprogrammet understøtter de fleste B2C-prissætningsscenarier (business-to-consumer), f.eks. prisfastsættelse på butiksniveau, tilknytningsbaseret og loyalitetsbaseret prisfastsættelse, mix og match-rabatter, mængderabatter og tærskelrabatter.</span><span class="sxs-lookup"><span data-stu-id="365ba-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="365ba-106">Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre.</span><span class="sxs-lookup"><span data-stu-id="365ba-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="365ba-107">Når du bruger [dobbeltskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), har du tre muligheder for dine prisfastsættelsesbehov.</span><span class="sxs-lookup"><span data-stu-id="365ba-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="365ba-108">Du kan bruge den statiske prisfastsættelse, der kommer fra prislisten i Dynamics 365 Sales, prissætningsprogrammet i Dynamics 365 Supply Chain Management eller prissætningsprogrammet i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="365ba-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="365ba-109">Blandt disse muligheder er Commerce-prissætningsprogrammet bedst egnet til B2C-scenarier.</span><span class="sxs-lookup"><span data-stu-id="365ba-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="365ba-110">Bruge Commerce-prissætningsprogrammet i Sales</span><span class="sxs-lookup"><span data-stu-id="365ba-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="365ba-111">I øjeblikket kan Commerce-prissætningsprogrammet kun bruges til oprettelse af tilbud i Sales.</span><span class="sxs-lookup"><span data-stu-id="365ba-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="365ba-112">Salgsordreintegration med Commerce-prissætningsprogrammet er endnu ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="365ba-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="365ba-113">Når brugere starter et tilbud i Sales, kopierer dobbeltskrivningsstrukturen tilbudsdetaljerne til Commerce.</span><span class="sxs-lookup"><span data-stu-id="365ba-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="365ba-114">Eventuelle ændringer i eksisterende tilbudslinjer eller tilbudslinjer, der er tilføjet for nylig i Sales, kopieres til Commerce.</span><span class="sxs-lookup"><span data-stu-id="365ba-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="365ba-115">Når brugere vil bruge Commerce-prissætningsprogrammet til at prissætte tilbuddet, kan de vælge **Pristilbud** for at opdatere priser for tilbuddet ud fra Commerce-prissætningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="365ba-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="365ba-116">Priserne opdateres derefter automatisk i både Sales og Commerce.</span><span class="sxs-lookup"><span data-stu-id="365ba-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="365ba-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="365ba-117">Prerequisites</span></span>

- <span data-ttu-id="365ba-118">Før du kan bruge Commerce-prissætningsprogrammet i Sales, skal du følge fremgangsmåderne i [Kundeemne til kontanter i dobbeltskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="365ba-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="365ba-119">Du skal deaktivere evaluering af samhandelsaftale for manuel indtastning ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="365ba-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="365ba-120">Gå til **Debitor \> Opsætning \> Debitorparametre** i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="365ba-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="365ba-121">Under fanen **Priser** i oversigtspanelet **Evaluering af samhandelsaftale** skal du fjerne markeringen i afkrydsningsfeltet **Manuel indtastning**.</span><span class="sxs-lookup"><span data-stu-id="365ba-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="365ba-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="365ba-122">Additional resources</span></span>

[<span data-ttu-id="365ba-123">Kundeemner til kontanter og to skrivninger</span><span class="sxs-lookup"><span data-stu-id="365ba-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]