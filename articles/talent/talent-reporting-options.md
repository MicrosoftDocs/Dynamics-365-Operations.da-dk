---
title: Rapporteringsindstillinger i Talent
description: "I dette emne beskrives, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="83fc2-103">Rapporteringsindstillinger i Talent</span><span class="sxs-lookup"><span data-stu-id="83fc2-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83fc2-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="83fc2-104">**Environment details**</span></span>

<span data-ttu-id="83fc2-105">Dette problem gælder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="83fc2-105">This issue applies to all environments.</span></span>

<span data-ttu-id="83fc2-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="83fc2-106">**Symptom**</span></span>

<span data-ttu-id="83fc2-107">Kunden vil gerne tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="83fc2-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="83fc2-108">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="83fc2-108">**Issue**</span></span>

<span data-ttu-id="83fc2-109">Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="83fc2-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="83fc2-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="83fc2-110">**Solution**</span></span>

- <span data-ttu-id="83fc2-111">De Core HR-data, der strømmer til Common Data Service for Apps, kan rapporteres via PowerApps CDS-forbindelsen til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="83fc2-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="83fc2-112">Bemærk, at Common Data Service for Apps indeholder et undersæt af Core HR-data.</span><span class="sxs-lookup"><span data-stu-id="83fc2-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="83fc2-113">Du kan finde flere oplysninger om Power BI og dashboards, i [Oprette Power BI-rapporter og dashboards med PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="83fc2-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="83fc2-114">Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Talent.</span><span class="sxs-lookup"><span data-stu-id="83fc2-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="83fc2-115">Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="83fc2-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="83fc2-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Talent leverer via Microsoft Office-integration.</span><span class="sxs-lookup"><span data-stu-id="83fc2-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="83fc2-117">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="83fc2-117">**Long-term solution**</span></span>

<span data-ttu-id="83fc2-118">Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service for Apps.</span><span class="sxs-lookup"><span data-stu-id="83fc2-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

