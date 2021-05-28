---
title: Konfigurere skattekomponenter for skattetypen Kildeskat
description: Dette emne beskriver, hvordan du opretter komponenter for A-skat i forbindelse med kildeskat (TDS – Tax Deducted at Source). Det beskriver også, hvordan du definerer den grænseværdi, der bruges til at beregne kildeskatten for hver skattekomponent.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023113"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="cae47-104">Konfigurere skattekomponenter for skattetypen Kildeskat</span><span class="sxs-lookup"><span data-stu-id="cae47-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cae47-105">Dette emne beskriver, hvordan du opretter komponenter for A-skat i forbindelse med kildeskat (TDS – Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="cae47-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="cae47-106">Skattekomponenterne er Kildeskat, Tillægsafgift, PE-Cess og SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="cae47-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="cae47-107">Dette emne beskriver også, hvordan du definerer den tærskel, der bruges til at beregne kildeskatten for hver skattekomponent.</span><span class="sxs-lookup"><span data-stu-id="cae47-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="cae47-108">Derudover kan du definere en tærskel for fritagelse, der bruges til at beregne kildeskat for hver skattekomponent.</span><span class="sxs-lookup"><span data-stu-id="cae47-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="cae47-109">Følg disse trin for at konfigurere skattekomponenter.</span><span class="sxs-lookup"><span data-stu-id="cae47-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="cae47-110">Gå til **Skat \> Opsætning \> A-skat \> Komponenter for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="cae47-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="cae47-111">[![Siden Komponenter for A-skat](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="cae47-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="cae47-112">Vælg **Kildeskat** i feltet **Skattetype** for at konfigurere komponenter for A-skat for skattetypen Kildeskat.</span><span class="sxs-lookup"><span data-stu-id="cae47-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="cae47-113">Vælg **Ny** i handlingsruden for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="cae47-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="cae47-114">Angiv et navn for komponenten for A-skat i feltet **Komponent for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="cae47-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="cae47-115">Vælg den komponentgruppe for A-skat, som skattekomponenten skal knyttes til, i feltet **Komponentgruppe for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="cae47-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="cae47-116">Indtast en beskrivelse af kildeskattekomponenten i feltet **Beskrivelse** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="cae47-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="cae47-117">Vælg **Tærskel** i handlingsruden for at åbne siden **Tærskel**, hvor du kan definere den tærskel, der skal bruges til at beregne kildeskat for skattekomponenten.</span><span class="sxs-lookup"><span data-stu-id="cae47-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="cae47-118">Brug felterne **Fra dato** og **Til dato** til at definere den periode, som tærsklen gælder for.</span><span class="sxs-lookup"><span data-stu-id="cae47-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="cae47-119">I feltet **Tærskel** i oversigtspanelet **Generelt** skal du angive det grænsebeløb, der bruges til beregning af kildeskat for skattekomponenten.</span><span class="sxs-lookup"><span data-stu-id="cae47-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="cae47-120">Skatten fratrækkes kun ved kilden, når det akkumulerede fakturabeløb overskrider tærsklen.</span><span class="sxs-lookup"><span data-stu-id="cae47-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="cae47-121">Hvis grænsebeløbet f.eks. er 10.000, beregnes kildeskatten, når det akkumulerede fakturabeløb overstiger 10.000 (er 10.001 eller mere).</span><span class="sxs-lookup"><span data-stu-id="cae47-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="cae47-122">I feltet **Tærskel for fritagelse** skal du angive grænsebeløbet for fritagelse, som skal bruges til beregning af kildeskat for skattekomponenten.</span><span class="sxs-lookup"><span data-stu-id="cae47-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="cae47-123">Skatten på en fakturalinje fratrækkes kun ved kilden, når beløbet overskrider tærsklen for fritagelse.</span><span class="sxs-lookup"><span data-stu-id="cae47-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="cae47-124">Hvis grænsebeløbet for fritagelse f.eks. er 5.000, beregnes kildeskatten på en specifik fakturalinje, hvis beløbet på fakturalinjen overstiger 5.000 (er 5.001 eller mere).</span><span class="sxs-lookup"><span data-stu-id="cae47-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="cae47-125">[![Siden Tærskel](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="cae47-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="cae47-126">Grænseværdien for fritagelse skal være mindre end eller lig med grænsebeløbet.</span><span class="sxs-lookup"><span data-stu-id="cae47-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="cae47-127">Skatten fratrækkes for en transaktion, hvis transaktionsbeløbet overstiger tærsklen for fritagelse, selvom det akkumulerede fakturabeløb ikke overstiger den tærskel, der er angivet i feltet **Tærskel**.</span><span class="sxs-lookup"><span data-stu-id="cae47-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="cae47-128">Luk siden **Tærskel** for at vende tilbage til siden **Komponenter for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="cae47-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="cae47-129">Vælg **Kopiér** i handlingsruden for at åbne dialogboksen **Kopiér komponenter for A-skat**, så du kan kopiere de komponenter for kildeskat, der er konfigureret for én komponentgruppe til en anden komponentgruppe for kildeskat.</span><span class="sxs-lookup"><span data-stu-id="cae47-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="cae47-130">I feltet **Fra** skal du vælge den komponentgruppe for kildeskat, som skattekomponenterne skal kopieres fra.</span><span class="sxs-lookup"><span data-stu-id="cae47-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="cae47-131">Vælg den komponentgruppe for A-skat, du vil kopiere komponenter for kildeskat til, i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="cae47-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cae47-132">Almindelige skattekomponenter, der er knyttet til begge komponentgrupper for kildeskat, kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="cae47-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="cae47-133">Vælg **OK** for at kopiere og oprette skattekomponenter for den anden komponentgruppe for kildeskat på siden **Komponenter for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="cae47-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="cae47-134">[![Dialogboksen Kopier komponenter for A-skat](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="cae47-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="cae47-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cae47-135">Close the page.</span></span>
