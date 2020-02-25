---
title: Rapporteringsindstillinger
description: I denne artikel emne beskrives det, hvordan du løser problemet, når en kunde ønsker at tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008559"
---
# <a name="reporting-options"></a><span data-ttu-id="69565-103">Rapporteringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="69565-103">Reporting options</span></span>

<span data-ttu-id="69565-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="69565-104">**Environment details**</span></span>

<span data-ttu-id="69565-105">Dette problem gælder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="69565-105">This issue applies to all environments.</span></span>

<span data-ttu-id="69565-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="69565-106">**Symptom**</span></span>

<span data-ttu-id="69565-107">Kunden vil gerne tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="69565-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="69565-108">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="69565-108">**Issue**</span></span>

<span data-ttu-id="69565-109">Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="69565-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="69565-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="69565-110">**Solution**</span></span>

- <span data-ttu-id="69565-111">Personale-data, der sendes til Common Data Service, kan indrapporteres via Power Apps Common Data Service-connector til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="69565-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="69565-112">Bemærk, at Common Data Service indeholder et undersæt af Personale-data.</span><span class="sxs-lookup"><span data-stu-id="69565-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="69565-113">Du kan finde flere oplysninger om Power BI og dashboards under [Oprette Power BI-rapporter og dashboards med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="69565-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="69565-114">Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Personale.</span><span class="sxs-lookup"><span data-stu-id="69565-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="69565-115">Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="69565-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="69565-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Personale leverer via Microsoft Office-integration.</span><span class="sxs-lookup"><span data-stu-id="69565-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="69565-117">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="69565-117">**Long-term solution**</span></span>

<span data-ttu-id="69565-118">Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69565-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
