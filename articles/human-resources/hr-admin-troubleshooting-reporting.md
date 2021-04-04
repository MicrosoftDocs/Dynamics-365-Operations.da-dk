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
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463280"
---
# <a name="reporting-options"></a><span data-ttu-id="22912-103">Rapporteringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="22912-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="22912-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="22912-104">**Environment details**</span></span>

<span data-ttu-id="22912-105">Dette problem gælder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="22912-105">This issue applies to all environments.</span></span>

<span data-ttu-id="22912-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="22912-106">**Symptom**</span></span>

<span data-ttu-id="22912-107">Kunden vil gerne tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller oprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="22912-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="22912-108">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="22912-108">**Issue**</span></span>

<span data-ttu-id="22912-109">Brugeren kan ikke tilpasse de integrerede Microsoft Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="22912-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="22912-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="22912-110">**Solution**</span></span>

- <span data-ttu-id="22912-111">Human Resources-data, der sendes til Dataverse, kan indrapporteres via Power Apps Dataverse-connector til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="22912-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="22912-112">Bemærk, at Dataverse indeholder et undersæt af Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="22912-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="22912-113">Du kan finde flere oplysninger om Power BI og dashboards under [Oprette Power BI-rapporter og dashboards med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="22912-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="22912-114">Elektronisk rapportering (ER) er tilgængelig til nogle rapporter i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="22912-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="22912-115">Kundestyrede tilpasninger kan udføres via ER-konfigurationsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="22912-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="22912-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjælp af de forskellige dataenheder, som Human Resources leverer via Microsoft Office-integration.</span><span class="sxs-lookup"><span data-stu-id="22912-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="22912-117">**Langsigtet løsning**</span><span class="sxs-lookup"><span data-stu-id="22912-117">**Long-term solution**</span></span>

<span data-ttu-id="22912-118">Yderligere indstillinger for Power BI bliver gjort tilgængelige, og flere data og enheder bliver en del af Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22912-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]