---
title: Regnskab i den offentlige sektor i Frankrig
description: I denne artikel beskrives regnskaber for den franske offentlige sektor.
author: rschloma
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19621
ms.assetid: f6bfb9dd-c3a7-48d3-b31d-23e6f27c1323
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1387363463ad5ed6f8c53c49c76994023ed9f806
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836857"
---
# <a name="public-sector-accounting-in-france"></a><span data-ttu-id="4ef41-103">Regnskab i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="4ef41-103">Public sector accounting in France</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ef41-104">I denne artikel beskrives regnskaber for den franske offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="4ef41-104">This article describes public sector accounting in France.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4ef41-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="4ef41-105">Prerequisites</span></span>

<span data-ttu-id="4ef41-106">Funktioner til den offentlige sektor i Frankrig er tilgængelige, når følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="4ef41-106">The French public sector features are available when the following conditions are met:</span></span>

-   <span data-ttu-id="4ef41-107">Konfigurationsnøglen **Offentlig sektor** og undernøglen **Franske myndighedskrav** vælges.</span><span class="sxs-lookup"><span data-stu-id="4ef41-107">The **Public Sector** configuration key and the **French regulatory** subkey are selected.</span></span>
-   <span data-ttu-id="4ef41-108">Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="4ef41-108">The **Use French public sector accounting rules** option is selected on the **Budgeting parameters** page.</span></span>
-   <span data-ttu-id="4ef41-109">Standardkoden for land/område er Frankrig.</span><span class="sxs-lookup"><span data-stu-id="4ef41-109">The default country/region code is France.</span></span>

<span data-ttu-id="4ef41-110">Yderligere konfigurationstrin for bestemte funktioner er omfattet af artiklen for hver funktion.</span><span class="sxs-lookup"><span data-stu-id="4ef41-110">Additional setup steps for specific features are covered in the article for each feature.</span></span>

## <a name="french-public-sector-topics"></a><span data-ttu-id="4ef41-111">Emner for den franske offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="4ef41-111">French public sector topics</span></span>
-   <span data-ttu-id="4ef41-112">[Mandat de paiement](emea-fra-mandats-de-paiement.md): Direktøren bruger mandat de paiement til at underrette og autorisere bogholderen til at betale et specifikt beløb til en anden enhed.</span><span class="sxs-lookup"><span data-stu-id="4ef41-112">[Mandats de paiement](emea-fra-mandats-de-paiement.md): The director uses the mandat de paiement to notify and authorize the accountant to pay a specific amount to another entity.</span></span>
-   <span data-ttu-id="4ef41-113">[Spærringer for kreditorfakturabetaling](emea-fra-vendor-invoice-payment-holds-public-sector.md): De almindelige processer, der vedrører betalingsspærringer af kreditorfakturaer, er suppleret for franske enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="4ef41-113">[Vendor invoice payment holds](emea-fra-vendor-invoice-payment-holds-public-sector.md): The standard processes related to payment hold for vendor invoices are augmented for French entities in the public sector.</span></span>
-   <span data-ttu-id="4ef41-114">[Titres de recette](emea-fra-titres-de-recette-public-sector.md): Direktøren bruger titres de recette til at underrette og autorisere bogholderen til at opkræve et specifikt beløb fra en anden enhed.</span><span class="sxs-lookup"><span data-stu-id="4ef41-114">[Titres de recette](emea-fra-titres-de-recette-public-sector.md): The director uses the titre de recette to notify and authorize the accountant to collect a specific amount from another entity.</span></span>
-   <span data-ttu-id="4ef41-115">[Forpligtelser](emea-fra-commitments-public-sector.md): Forpligtelser bruges til at reservere budgetterede beløb.</span><span class="sxs-lookup"><span data-stu-id="4ef41-115">[Commitments](emea-fra-commitments-public-sector.md): Commitments are used to reserve budgeted amounts.</span></span> <span data-ttu-id="4ef41-116">Derved kan en organisation udtrykkeligt kan spore budgetreservationer til administration og rapportering i hele udgiftscyklussen.</span><span class="sxs-lookup"><span data-stu-id="4ef41-116">This allows an organization to explicitly track budget reservations for management and reporting throughout the expenditure cycle.</span></span>
-   <span data-ttu-id="4ef41-117">[Indkøb og forsyning](emea-fra-procurement-sourcing-public-sector.md):</span><span class="sxs-lookup"><span data-stu-id="4ef41-117">[Procurement and sourcing](emea-fra-procurement-sourcing-public-sector.md):</span></span>
    -   <span data-ttu-id="4ef41-118">De standardfunktioner, der vedrører købsaftaler, suppleres for franske enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="4ef41-118">The standard features related to purchase agreements are augmented for French entities in the public sector.</span></span> <span data-ttu-id="4ef41-119">For eksempel kan du oprette trancher og partier, styre adgangen til afdelinger, administrere kreditorcertificeringer og konfigurere de største kontrahenter, medkontrahenter og underleverandører.</span><span class="sxs-lookup"><span data-stu-id="4ef41-119">For example, you can create tranches and lots, control department access, manage vendor certifications, and set up prime contractors, co-contractors, and subcontractors.</span></span> <span data-ttu-id="4ef41-120">Disse funktioner gør det nemmere at opfylde kravene i Code des Marchés Publics.</span><span class="sxs-lookup"><span data-stu-id="4ef41-120">These capabilities help you meet the requirements of the Code des Marchés Publics.</span></span>
    -   <span data-ttu-id="4ef41-121">For at opfylde offentlige lovgivningsmæssige krav i Frankrig skal du angive forbrugsgrænser for køb i de indkøbskategorier, som er defineret af Clé de Contrôle Marché.</span><span class="sxs-lookup"><span data-stu-id="4ef41-121">To meet public sector regulatory requirements in France, set spending thresholds for purchases in the procurement categories that are defined by the Clé de Contrôle Marché.</span></span> <span data-ttu-id="4ef41-122">Med en **Forbrugsgrænser efter kategori**-politikregel, der bruges sammen med indkøbspolitikregler, kan du bruge attributter for ikrafttrædelsesdato, estimerede udgiftsbeløb og tærskelbeløb til at understøtte krævede indkøbspraksis.</span><span class="sxs-lookup"><span data-stu-id="4ef41-122">A **Spending thresholds by category** policy rule that is used with purchasing policies lets you use effective date attributes, predicted expenditure amounts, and threshold amounts to support required procurement practices.</span></span> <span data-ttu-id="4ef41-123">Politikreglen sikrer også en effektiv brug af offentlige midler.</span><span class="sxs-lookup"><span data-stu-id="4ef41-123">The policy rule also ensures the efficient and effective use of public funds.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]