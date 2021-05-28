---
title: Opdatere certifikatnumre og -datoer for TDS-posteringer
description: Dette emne forklarer, hvordan du opdaterer de numre og datoer på refusionscertifikater, der er registreret for kreditor-, debitor- og finanskonti for afgifter fratrukket ved kilden (TDS).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023114"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="5a6a9-103">Opdatere certifikatnumre og -datoer for TDS-posteringer</span><span class="sxs-lookup"><span data-stu-id="5a6a9-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a6a9-104">Dette emne forklarer, hvordan du opdaterer de numre og datoer på refusionscertifikater, der er registreret for kreditor-, debitor- og finanskonti for afgifter fratrukket ved kilden (TDS).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="5a6a9-105">Du kan få vist certifikaterne for TDS-transaktioner på siden **Refusionscertifikater**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="5a6a9-106">Du kan opdatere certifikaterne ved hjælp af siden **Opdater certifikater**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="5a6a9-107">Følg disse trin for at opdatere certifikatnumre og -datoer for TDS-posteringer.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="5a6a9-108">Gå til **Moms \> Opgørelser \> A-skat \> Opdater certifikat**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="5a6a9-109">[![Siden Opdater certifikat](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="5a6a9-110">Vælg **TDS** i feltet **Skattetype** i sektionen **Vælg** på siden **Opdater certifikat**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="5a6a9-111">Vælg debitors eller kreditors TDS-certifikatnummer i feltet **Certifikatnummer**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a6a9-112">I feltet **Certifikatnummer** vises kun TDS-certifikatnumre, som ikke er markeret i afkrydsningsfeltet **Lukket** på siden **Refusionscertifikater**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="5a6a9-113">I feltet **Certifikatdato** vises certifikatdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="5a6a9-114">Feltet **Kontotype** viser den kontotype, som TDS-certifikatnummeret er modtaget for, og feltet **Navn** viser navnet på kontoen.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="5a6a9-115">Vælg start- og slutdatoerne for den periode, TDS-transaktionerne skal vises for, i felterne **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="5a6a9-116">Vælg **Vis data** for at få vist de TDS-transaktioner, der blev bogført i den valgte periode.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="5a6a9-117">Under fanen **Oversigt** viser gitteret i den øverste rude følgende oplysninger om hver TDS-transaktion, der er bogført for kreditoren eller debitoren i den valgte periode:</span><span class="sxs-lookup"><span data-stu-id="5a6a9-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="5a6a9-118">**Bilag** – Bilagsnummeret på skattetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="5a6a9-119">**Dato** – Datoen for TDS-transaktionen.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="5a6a9-120">**Beløb** – Det fakturabeløb, som kildeskat blev beregnet for.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="5a6a9-121">**Skattebeløb** – Det kildeskattebeløb, der er beregnet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="5a6a9-122">Hvis du vil flytte specifikke TDS-posteringer fra det øverste gitter til det nederste gitter, skal du vælge posteringerne og derefter vælge **Medtag**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="5a6a9-123">Alternativt kan du vælge **Medtag alle** for at flytte alle TDS-posteringer fra det øverste gitter til det nederste gitter.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="5a6a9-124">Hvis du vil flytte specifikke TDS-posteringer eller alle TDS-transaktioner fra det nederste gitter til det øverste gitter, skal du bruge knappen **Udelad** eller knappen **Udelad alle**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="5a6a9-125">Vælg **Opdater** for at opdatere felterne **Certifikatnummer** og **Certifikatdato** for TDS-posteringer i nederste gitter.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="5a6a9-126">Gå til **Moms \> Indirekte skatter \> A-skat \> Refusionscertifikat**, og vælg **Forespørgsel** for at få vist de opdaterede posteringslinjer, der har de nye certifikatnumre, på siden **Certifikatposteringer**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="5a6a9-127">[![Siden Certifikatposteringer](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
