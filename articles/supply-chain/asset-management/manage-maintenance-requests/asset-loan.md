---
title: Lånte aktiver
description: I dette emne beskrives, hvordan du kan registrere lånte aktiver i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cba680d0ad626e0275539d7478a83639a9d22635
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424692"
---
# <a name="asset-loans"></a><span data-ttu-id="5cdab-103">Lånte aktiver</span><span class="sxs-lookup"><span data-stu-id="5cdab-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5cdab-104">Hvis din virksomhed modtager aktiver til reparations- eller vedligeholdelsesopgaver fra enten interne lokationer eller kunder, og hvis du midlertidigt låner aktiver ud til disse lokationer eller kunder, kan Styring af aktiver registrere de lånte aktiver.</span><span class="sxs-lookup"><span data-stu-id="5cdab-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="5cdab-105">Registrere lånte aktiver på en vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="5cdab-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="5cdab-106">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="5cdab-107">Vælg den vedligeholdelsesanmodning, du vil registrere et lånt aktiv på, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="5cdab-108">Vælg **Send lånt aktiv** på siden **Anmodning**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="5cdab-109">Vælg aktivet, og angiv den forventede tilbageleveringsdato.</span><span class="sxs-lookup"><span data-stu-id="5cdab-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="5cdab-110">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="5cdab-111">Du kan kun sende et lånt aktiv, hvis et aktiv af samme aktivtype er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="5cdab-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="5cdab-112">Det aktiv, du låner ud, skal have en livscyklustilstand, der gør det muligt at bruge det som et lånt aktiv, f.eks. **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="5cdab-113">Når det lånte aktiv er registreret, opdateres aktivets livscyklustilstand automatisk til eksempelvis **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="5cdab-114">Hvis du vil have vist en liste over alle de aktiver, du har udlånt til andre lokationer eller kunder, skal du vælge **Styring af aktiver** \> **Almindeligt** \> **Lånt aktiv** \> **Alle lånte aktiver**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="5cdab-115">Hvis afkrydsningsfeltet **Afsluttet** er markeret for et aktiv, er aktivet registreret som returneret til dit firma.</span><span class="sxs-lookup"><span data-stu-id="5cdab-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Administrere vedligeholdelsesanmodninger](media/06-manage-maintenance-requests.png)

<span data-ttu-id="5cdab-117">På siden **Aktive lånte aktiver** kan du få vist en liste over alle de lånte aktiver, der endnu ikke er returneret til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="5cdab-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="5cdab-118">Registrere lånte aktiver som returneret</span><span class="sxs-lookup"><span data-stu-id="5cdab-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="5cdab-119">Vælg **Styring af aktiver** \> **Almindelig** \> **Lånt aktiv** \> **Aktive lånte aktiver**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="5cdab-120">Vælg det lånte aktiv, du vil registrere som returneret, og vælg derefter **Returner lånt aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="5cdab-121">Angiv datoen og tidspunktet i feltet **Returneret**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="5cdab-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cdab-122">Select **OK**.</span></span>
5. <span data-ttu-id="5cdab-123">Opdater listesiden **Aktive lånte aktiver**, og bemærk, at det lånte aktiv ikke længere vises på listen.</span><span class="sxs-lookup"><span data-stu-id="5cdab-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
