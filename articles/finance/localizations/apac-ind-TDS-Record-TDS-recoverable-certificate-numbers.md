---
title: Registrere certifikatnumre for skatterefundering
description: Dette emne forklarer, hvordan du bruger siden Refusionscertifikater for at registrere certifikatnumrene og datoer på certifikater for kildeskat (TDS – Tax Deducted at Source), der er modtaget for en specifik kreditor-, debitor- og finanskonti.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023104"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="b99ce-103">Registrere certifikatnumre for skatterefundering</span><span class="sxs-lookup"><span data-stu-id="b99ce-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b99ce-104">Dette emne forklarer, hvordan du bruger siden **Refusionscertifikater** for at registrere certifikatnumrene og datoer på certifikater for kildeskat (TDS – Tax Deducted at Source), der er modtaget for en specifik kreditor-, debitor- og finanskonti.</span><span class="sxs-lookup"><span data-stu-id="b99ce-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="b99ce-105">Hvis du vil opdatere skattecertifikatnumre og -datoer, der er registreret for skattetransaktioner på denne side, skal du bruge siden **Opdater certifikat** (**Finans \> Periodisk \> A-skat \> Opdater certifikat**).</span><span class="sxs-lookup"><span data-stu-id="b99ce-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="b99ce-106">Når du er færdig med at opdatere skattecertifikatnumre, skal du lukke dem.</span><span class="sxs-lookup"><span data-stu-id="b99ce-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="b99ce-107">Følg disse trin for at registrere numre og -datoer for skattecertifikater.</span><span class="sxs-lookup"><span data-stu-id="b99ce-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="b99ce-108">Gå til **Skat \> Indirekte skat \> A-skat \> Refusionscertifikater**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="b99ce-109">[![Siden Refusionscertifikater](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="b99ce-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="b99ce-110">Vælg **Kildeskat** i feltet **Skattetype** på siden **Refusionscertifikater**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="b99ce-111">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="b99ce-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="b99ce-112">Angiv skattecertifikatnummeret i feltet **Certifikatnummer**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="b99ce-113">Vælg den kontotype, som skattecertifikatet modtages for, i feltet **Kontotype**: **Kreditor**, **Debitor** eller **Finans**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="b99ce-114">Vælg kreditor-, debitor- eller finanskontonummeret i feltet **Konto** afhængigt af den valgte kontotype.</span><span class="sxs-lookup"><span data-stu-id="b99ce-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="b99ce-115">Feltet **Navn** viser navnet på kreditor-, debitor- eller finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="b99ce-116">Angiv beløbet for skattecertifikatet i feltet **Certifikatbeløb**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="b99ce-117">Angiv certifikatdatoen for certifikatnummeret i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="b99ce-118">Vælg **Forespørgsler** for at åbne siden **Certifikattransaktioner**, hvor du kan få vist de skattetransaktioner, som skattecertifikatnummeret og -datoen opdateres for.</span><span class="sxs-lookup"><span data-stu-id="b99ce-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="b99ce-119">Disse oplysninger kan opdateres på siden **Opdater certifikat** (**Skat \> Angivelser \> A-skat \> Opdater certifikat**).</span><span class="sxs-lookup"><span data-stu-id="b99ce-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="b99ce-120">På siden **Opdater certifikat** vises følgende oplysninger for hver skattetransaktion:</span><span class="sxs-lookup"><span data-stu-id="b99ce-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="b99ce-121">**Dato** – Bogføringsdatoen for skattetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="b99ce-122">**Bilag** – Bilagsnummeret på skattetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="b99ce-123">**Kilde** – Det modul, som skattetransaktionen blev oprettet i.</span><span class="sxs-lookup"><span data-stu-id="b99ce-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="b99ce-124">**Konto** – Det kreditor-, debitor- eller finanskontonummer, som skattetransaktionen er oprettet for.</span><span class="sxs-lookup"><span data-stu-id="b99ce-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="b99ce-125">**Navn** – Navnet på den kreditor-, debitor- eller finanskonton, som skattetransaktionen er oprettet for.</span><span class="sxs-lookup"><span data-stu-id="b99ce-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="b99ce-126">**Beløb** – Det fakturabeløb, som kildeskat blev beregnet for.</span><span class="sxs-lookup"><span data-stu-id="b99ce-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="b99ce-127">**Skattebeløb** – Det kildeskattebeløb, der er beregnet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="b99ce-128">**Certifikatdato** – Den skattecertifikatdato, der blev opdateret for skattetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="b99ce-129">**Certifikatnummer** – Det skattecertifikatnummer, der blev opdateret for skattetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="b99ce-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="b99ce-130">På siden **Refusionscertifikater** skal du markere afkrydsningsfeltet **Lukket** for at lukke skattecertifikatnummeret, når du er færdig med at opdatere det for skattetransaktioner på siden **Opdater certifikat**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="b99ce-131">Hvis du vil markere afkrydsningsfeltet **Lukket** for alle poster på siden, skal du markere **Markér alle**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b99ce-132">Skattecertifikatnumre, som afkrydsningsfeltet **Lukket** er markeret for, er ikke tilgængelige på siden **Opdater certifikat**.</span><span class="sxs-lookup"><span data-stu-id="b99ce-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
