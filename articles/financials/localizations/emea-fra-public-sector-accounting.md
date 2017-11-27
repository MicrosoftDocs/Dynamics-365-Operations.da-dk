---
title: Regnskab i den offentlige sektor i Frankrig
description: I denne artikel beskrives regnskaber for den franske offentlige sektor.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 19621
ms.assetid: f6bfb9dd-c3a7-48d3-b31d-23e6f27c1323
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c999055a4e849332a104276ef8d3ea3ce781e2e3
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="public-sector-accounting-in-france"></a><span data-ttu-id="287b4-103">Regnskab i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="287b4-103">Public sector accounting in France</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="287b4-104">I denne artikel beskrives regnskaber for den franske offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="287b4-104">This article describes public sector accounting in France.</span></span>

<a name="prerequisites"></a><span data-ttu-id="287b4-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="287b4-105">Prerequisites</span></span>
-------------

<span data-ttu-id="287b4-106">Funktioner til den offentlige sektor i Frankrig er tilgængelige, når følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="287b4-106">The French public sector features are available when the following conditions are met:</span></span>

-   <span data-ttu-id="287b4-107">Konfigurationsnøglen **Offentlig sektor** og undernøglen **Franske myndighedskrav** vælges.</span><span class="sxs-lookup"><span data-stu-id="287b4-107">The **Public Sector** configuration key and the **French regulatory** subkey are selected.</span></span>
-   <span data-ttu-id="287b4-108">Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="287b4-108">The **Use French public sector accounting rules** option is selected on the **Budgeting parameters** page.</span></span>
-   <span data-ttu-id="287b4-109">Standardkoden for land/område er Frankrig.</span><span class="sxs-lookup"><span data-stu-id="287b4-109">The default country/region code is France.</span></span>

<span data-ttu-id="287b4-110">Yderligere konfigurationstrin for bestemte funktioner er omfattet af artiklen for hver funktion.</span><span class="sxs-lookup"><span data-stu-id="287b4-110">Additional setup steps for specific features are covered in the article for each feature.</span></span>

## <a name="french-public-sector-topics"></a><span data-ttu-id="287b4-111">Emner for den franske offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="287b4-111">French public sector topics</span></span>
-   <span data-ttu-id="287b4-112">[Mandat de paiement](emea-fra-mandats-de-paiement.md) Direktøren bruger mandat de paiement til at underrette bogholderen om, at organisationen er forpligtet til at betale et bestemt beløb til en anden enhed, og til at godkende, at bogholderen betaler beløbet.</span><span class="sxs-lookup"><span data-stu-id="287b4-112">[Mandats de paiement](emea-fra-mandats-de-paiement.md) The director uses the mandat de paiement to notify the accountant that the organization is obligated to pay a specific amount to another entity, and to authorize the accountant to pay that amount.</span></span>
-   <span data-ttu-id="287b4-113">[Spærringer for kreditorfakturabetaling](emea-fra-vendor-invoice-payment-holds-public-sector.md) De almindelige processer, der vedrører betalingsspærringer af kreditorfakturaer, er suppleret for franske enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="287b4-113">[Vendor invoice payment holds](emea-fra-vendor-invoice-payment-holds-public-sector.md) The standard processes that are related to payment holds for vendor invoices are augmented for French entities in the public sector.</span></span>
-   <span data-ttu-id="287b4-114">[Titre de recette](emea-fra-titres-de-recette-public-sector.md) Direktøren bruger titre de recette til at underrette bogholderen om, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed, og til at godkende, at bogholderen opkræver beløbet.</span><span class="sxs-lookup"><span data-stu-id="287b4-114">[Titres de recette](emea-fra-titres-de-recette-public-sector.md) The director uses the titre de recette to notify the accountant that the organization is entitled to collect a specific amount from another entity, and to authorize the accountant to collect that amount.</span></span>
-   <span data-ttu-id="287b4-115">[Forpligtelser](emea-fra-commitments-public-sector.md) Forpligtelser bruges til at reservere budgetterede beløb, så en organisation udtrykkeligt kan spore budgetreservationer til administration og rapportering i hele udgiftscyklussen.</span><span class="sxs-lookup"><span data-stu-id="287b4-115">[Commitments](emea-fra-commitments-public-sector.md) Commitments are used to reserve budgeted amounts so that an organization can explicitly track budget reservations for management and reporting throughout the expenditure cycle.</span></span>
-   [<span data-ttu-id="287b4-116">Indkøb og forsyning</span><span class="sxs-lookup"><span data-stu-id="287b4-116">Procurement and sourcing</span></span>](emea-fra-procurement-sourcing-public-sector.md)
    -   <span data-ttu-id="287b4-117">De standardfunktioner, der vedrører købsaftaler, suppleres for franske enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="287b4-117">The standard features that are related to purchase agreements are augmented for French entities in the public sector.</span></span>  <span data-ttu-id="287b4-118">For eksempel kan du oprette trancher og partier, styre adgangen til afdelinger, administrere kreditorcertificeringer og konfigurere de største kontrahenter, medkontrahenter og underleverandører.</span><span class="sxs-lookup"><span data-stu-id="287b4-118">For example, you can create tranches and lots, control department access, manage vendor certifications, and set up prime contractors, co-contractors, and subcontractors.</span></span> <span data-ttu-id="287b4-119">Disse funktioner gør det nemmere at opfylde kravene i Code des Marchés Publics.</span><span class="sxs-lookup"><span data-stu-id="287b4-119">These capabilities help you meet the requirements of the Code des Marchés Publics.</span></span>
    -   <span data-ttu-id="287b4-120">For at opfylde offentlige lovgivningsmæssige krav i Frankrig skal du muligvis angive forbrugsgrænser for køb i de indkøbskategorier, som er defineret af Clé de Contrôle Marché.</span><span class="sxs-lookup"><span data-stu-id="287b4-120">To meet public sector regulatory requirements in France, you might have to set spending thresholds for purchases in the procurement categories that are defined by the Clé de Contrôle Marché.</span></span> <span data-ttu-id="287b4-121">Med en **Forbrugsgrænser efter kategori**-politikregel, der bruges sammen med indkøbspolitikregler, kan du bruge attributter for ikrafttrædelsesdato, estimerede udgiftsbeløb og tærskelbeløb til at understøtte krævede indkøbspraksis og til at sikre effektiv brug af offentlige midler.</span><span class="sxs-lookup"><span data-stu-id="287b4-121">A **Spending thresholds by category** policy rule that is used with purchasing policies lets you use effective date attributes, predicted expenditure amounts, and threshold amounts to support required procurement practices, and to ensure the efficient and effective use of public funds.</span></span>





