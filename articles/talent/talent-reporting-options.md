---
title: Rapporteringsindstillinger i Talent
description: I dette emne beskrives, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.
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
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "950053"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="95319-103">Rapporteringsindstillinger i Talent</span><span class="sxs-lookup"><span data-stu-id="95319-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95319-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="95319-104">**Environment details**</span></span>

<span data-ttu-id="95319-105">Dette problem gælder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="95319-105">This issue applies to all environments.</span></span>

<span data-ttu-id="95319-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="95319-106">**Symptom**</span></span>

<span data-ttu-id="95319-107">Kunden vil gerne tilpasse Microsoft Dynamics 365 for Talent-rapporter eller oprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="95319-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="95319-108">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="95319-108">**Issue**</span></span>

<span data-ttu-id="95319-109">Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="95319-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="95319-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="95319-110">**Solution**</span></span>

- <span data-ttu-id="95319-111">De Core HR-data, der sendes til Common Data Service, kan indrapporteres via PowerApps' Common Data Service-connector til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="95319-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="95319-112">Bemærk, at Common Data Service indeholder et undersæt af Core HR-data.</span><span class="sxs-lookup"><span data-stu-id="95319-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="95319-113">Du kan finde flere oplysninger om Power BIog dashboards i [Oprette Power BI-rapporter og dashboards med PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="95319-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="95319-114">Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Talent.</span><span class="sxs-lookup"><span data-stu-id="95319-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="95319-115">Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="95319-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="95319-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Talent leverer via Microsoft Office-integration.</span><span class="sxs-lookup"><span data-stu-id="95319-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="95319-117">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="95319-117">**Long-term solution**</span></span>

<span data-ttu-id="95319-118">Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="95319-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
