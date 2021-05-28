---
title: Dynamics 365-globaliseringstjenester
description: Dette emne giver en oversigt over Microsoft Dynamics 365-globaliseringstjenester.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018801"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="6f99c-103">Dynamics 365-globaliseringstjenester</span><span class="sxs-lookup"><span data-stu-id="6f99c-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f99c-104">Følgende globaliseringstjenester kan konfigureres til at udvide de egenskaber, der findes i nogle Microsoft Dynamics 365-onlinetjenester:</span><span class="sxs-lookup"><span data-stu-id="6f99c-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="6f99c-105">**RCS (Regulatory Configuration Service)** understøtter konfigurationen af forskellige typer elektroniske dokumenter og rapporter.</span><span class="sxs-lookup"><span data-stu-id="6f99c-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="6f99c-106">RCS leverer en udvidet version af ER-designeren (elektronisk rapportering), hvor konfigurationslageret er en enkeltstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="6f99c-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="6f99c-107">Du kan finde flere oplysninger under [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f99c-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="6f99c-108">**Elektronisk fakturering** samler konfigurerbare formater for transformationer, digitale signaturer og konfigurerbare integrationer for forbindelse til eksterne webtjenester, herunder certificering og håndtering af svar.</span><span class="sxs-lookup"><span data-stu-id="6f99c-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="6f99c-109">Du kan finde flere oplysninger i [Elektronisk fakturering](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f99c-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="6f99c-110">**Momsberegning** giver større fleksibilitet ved at understøtte flere moms-id'er, bestemmelse af momskode, designeren til momsberegning og et kørselsprogram for at overholde komplekse momsregler på globalt plan.</span><span class="sxs-lookup"><span data-stu-id="6f99c-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="6f99c-111">Du kan finde flere oplysninger under [Momsberegning](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f99c-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="6f99c-112">Disse globaliseringstjenester leverer standardintegration med følgende Dynamics 365-onlinetjenester.</span><span class="sxs-lookup"><span data-stu-id="6f99c-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="6f99c-113">Onlinetjeneste</span><span class="sxs-lookup"><span data-stu-id="6f99c-113">Online service</span></span> | <span data-ttu-id="6f99c-114">RCS</span><span class="sxs-lookup"><span data-stu-id="6f99c-114">RCS</span></span> | <span data-ttu-id="6f99c-115">Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="6f99c-115">Electronic Invoicing</span></span> | <span data-ttu-id="6f99c-116">Momsberegning (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6f99c-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="6f99c-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="6f99c-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="6f99c-118">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-118">Yes</span></span> | <span data-ttu-id="6f99c-119">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-119">Yes</span></span> | <span data-ttu-id="6f99c-120">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-120">Yes</span></span> | 
| <span data-ttu-id="6f99c-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6f99c-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="6f99c-122">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-122">Yes</span></span> | <span data-ttu-id="6f99c-123">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-123">Yes</span></span> | <span data-ttu-id="6f99c-124">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-124">Yes</span></span> | 
| <span data-ttu-id="6f99c-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="6f99c-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="6f99c-126">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-126">Yes</span></span> | <span data-ttu-id="6f99c-127">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-127">Yes</span></span> | <span data-ttu-id="6f99c-128">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="6f99c-128">Not applicable</span></span> | 
| <span data-ttu-id="6f99c-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6f99c-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="6f99c-130">Ja</span><span class="sxs-lookup"><span data-stu-id="6f99c-130">Yes</span></span> | <span data-ttu-id="6f99c-131">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="6f99c-131">Not applicable</span></span> | <span data-ttu-id="6f99c-132">Ikke anvendelig</span><span class="sxs-lookup"><span data-stu-id="6f99c-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="6f99c-133">På grund af forskelle i tilgængeligheden af Azure-geografiske steder (geolokationer) for RCS kan konfiguration af denne tjeneste bevirke, at der overføres kundedata uden for det geografiske område, der er valgt for den relevante Dynamics 365-onlinetjeneste.</span><span class="sxs-lookup"><span data-stu-id="6f99c-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="6f99c-134">Du kan finde flere oplysninger i [Dynamics 365 og Power Platform : Tilgængelighed, dataplacering, sprog og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="6f99c-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>