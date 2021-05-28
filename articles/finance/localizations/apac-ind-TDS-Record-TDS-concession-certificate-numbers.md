---
title: Registrere certifikatnumre for skattekoncession
description: Dette emne forklarer, hvordan du registrerer koncessionscertifikatnumre for kildeskat (TDS – Tax Deducted at Source), der er udstedt til kreditorer.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023106"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="7afc7-103">Registrere certifikatnumre for skattekoncession</span><span class="sxs-lookup"><span data-stu-id="7afc7-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7afc7-104">Dette emne forklarer, hvordan du registrerer koncessionscertifikatnumre for kildeskat (TDS – Tax Deducted at Source), der er udstedt til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="7afc7-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="7afc7-105">Gå til **Skat \> Indirekte skatter \> A-skat \> Koncessioner for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="7afc7-106">Vælg **Kildeskat** i feltet **Skattetype** for at registrere koncessionscertifikater for skattetypen Kildeskat.</span><span class="sxs-lookup"><span data-stu-id="7afc7-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="7afc7-107">Vælg **Alt+N** under fanen **Oversigt** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="7afc7-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="7afc7-108">[![Overskriften på den nye linje](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="7afc7-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="7afc7-109">Vælg den kildeskattekode, som kreditorens koncessionscertifikater udstedes for, i feltet **Kode for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="7afc7-110">Feltet **Kodenavn for A-skat** viser navnet på kildeskattekoden.</span><span class="sxs-lookup"><span data-stu-id="7afc7-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="7afc7-111">I felterne **Fra dato** og **Til dato** skal du definere gyldighedsperioden for koncessionscertifikater, der bruger kildeskattekoden til at beregne kildeskat for kreditoren på koncessionelt grundlag.</span><span class="sxs-lookup"><span data-stu-id="7afc7-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="7afc7-112">Angiv eventuelle bemærkninger i feltet **Bemærkninger**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="7afc7-113">Angiv koden for det juridiske område, som skattekoncessionscertifikatet aktiveres under, i feltet **Afsnit**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="7afc7-114">Hvis afsnitskoden er 197, vises værdien "A" i kolonnen "Årsag til ikke-fradrag/lavere fradrag" i Formular 26Q og kolonnen "Årsag til ikke-fradrag/lavere fradrag/bruttoberegning (eventuelt)" i Formular 27Q.</span><span class="sxs-lookup"><span data-stu-id="7afc7-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="7afc7-115">Hvis afsnitskoden er 197A, vises værdien "B" begge steder.</span><span class="sxs-lookup"><span data-stu-id="7afc7-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="7afc7-116">Vælg oversigtspanelet **Certifikat** for at registrere certifikatnumre for skattekoncession til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="7afc7-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="7afc7-117">Vælg den kreditorkonto, som skattekoncessionscertifikatet er udstedt for, i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="7afc7-118">Definer gyldighedsperioden for skattekoncessionscertifikatet i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="7afc7-119">Beregningen af kildeskat på koncessionelt grundlag er baseret på den periode, hvor certifikatet oprettes for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="7afc7-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="7afc7-120">Angiv skattekoncessionens certifikatnummer i feltet **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="7afc7-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="7afc7-121">[![Oversigtspanelet Certifikat](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="7afc7-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="7afc7-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7afc7-122">Close the page.</span></span>
