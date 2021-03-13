---
title: Rapporteringsindstillinger
description: I denne artikel emne beskrives det, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111900"
---
# <a name="reporting-options"></a><span data-ttu-id="d3140-103">Rapporteringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="d3140-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d3140-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="d3140-104">**Environment details**</span></span>

<span data-ttu-id="d3140-105">Dette problem gælder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="d3140-105">This issue applies to all environments.</span></span>

<span data-ttu-id="d3140-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="d3140-106">**Symptom**</span></span>

<span data-ttu-id="d3140-107">Kunden vil gerne tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="d3140-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="d3140-108">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="d3140-108">**Issue**</span></span>

<span data-ttu-id="d3140-109">Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="d3140-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="d3140-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="d3140-110">**Solution**</span></span>

- <span data-ttu-id="d3140-111">Human Resources-data, der sendes til Dataverse, kan indrapporteres via Power Apps Dataverse-connector til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d3140-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="d3140-112">Bemærk, at Dataverse indeholder et undersæt af Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="d3140-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="d3140-113">Du kan finde flere oplysninger om Power BI og dashboards under [Oprette Power BI-rapporter og dashboards med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="d3140-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="d3140-114">Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3140-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="d3140-115">Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="d3140-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="d3140-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Human Resources leverer via Microsoft Office-integration.</span><span class="sxs-lookup"><span data-stu-id="d3140-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="d3140-117">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="d3140-117">**Long-term solution**</span></span>

<span data-ttu-id="d3140-118">Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3140-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
