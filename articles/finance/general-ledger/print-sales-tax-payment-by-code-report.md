---
title: Udskriv rapporten Momsbetaling efter kode
description: Dette emne indeholder oplysninger om de indstillinger og handlinger, der kræves for at udskrive rapporten Momsafregning efter kode i regnskabs- eller momskodevalutaen.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6f66db74867bdd3e9b4364e247058e0534191f2e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205054"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="fab7a-103">Udskriv rapporten Momsbetaling efter kode</span><span class="sxs-lookup"><span data-stu-id="fab7a-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fab7a-104">Hvis du vil udskrive rapporten **Momsbetaling efter kode**, skal du gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsrapportér** \> **Momsbetaling efter kode**.</span><span class="sxs-lookup"><span data-stu-id="fab7a-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="fab7a-105">Som standard genereres rapportbeløb i regnskabsvalutaen for den juridiske enhed for alle rapporteringskoder, der er konfigureret på siden **Momsrapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="fab7a-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="fab7a-106">Du kan også generere denne rapport, så den viser momsafregningsbeløbene i valutaerne for momskoder for alle rapporteringskoder, der er knyttet til momskoder på siden **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="fab7a-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="fab7a-107">Slå funktionen til</span><span class="sxs-lookup"><span data-stu-id="fab7a-107">Turn on the feature</span></span>

<span data-ttu-id="fab7a-108">I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktion: **Generér rapport over momsbetaling efter kode i momskodevalutaen**.</span><span class="sxs-lookup"><span data-stu-id="fab7a-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="fab7a-109">Kør rapporten</span><span class="sxs-lookup"><span data-stu-id="fab7a-109">Run the report</span></span>

1. <span data-ttu-id="fab7a-110">Gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsrapporter** \> **Momsbetaling efter kode**.</span><span class="sxs-lookup"><span data-stu-id="fab7a-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="fab7a-111">Vælg en af følgende værdier i feltet **Rapportvaluta**:</span><span class="sxs-lookup"><span data-stu-id="fab7a-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="fab7a-112">**Regnskabsvaluta** – Udskriv rapport beløbene i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="fab7a-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="fab7a-113">**Momskodevaluta** – Udskriv rapport beløbene i valutaerne for momskoder.</span><span class="sxs-lookup"><span data-stu-id="fab7a-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialogboksen Momsafregning pr. kode](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="fab7a-115">I følgende illustration vises et eksempel på den rapport, der genereres.</span><span class="sxs-lookup"><span data-stu-id="fab7a-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="fab7a-116">Rapporten viser, at rapporteringskode **101** har valutaen **EUR**, hvis feltet **Momsvaluta** er angivet til **EUR** for den momskode, som rapporteringskoden er tildelt.</span><span class="sxs-lookup"><span data-stu-id="fab7a-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Eksempel på rapporten Momsbetaling efter kode](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]