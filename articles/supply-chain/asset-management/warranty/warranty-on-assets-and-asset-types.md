---
title: Garantier for aktiver og aktivtyper
description: I dette emne beskrives, hvordan du konfigurerer garantier for aktiver og aktivtyper i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c0359bfe31b3d01f28028bb17d5d30af39a1db9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021597"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="bf326-103">Garantier for aktiver og aktivtyper</span><span class="sxs-lookup"><span data-stu-id="bf326-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="bf326-104">I dette emne beskrives, hvordan du konfigurerer garantier for aktiver og aktivtyper i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="bf326-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="bf326-105">Konfigurere en garanti for en aktivtype</span><span class="sxs-lookup"><span data-stu-id="bf326-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="bf326-106">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivtype** \> **Aktivtyper**.</span><span class="sxs-lookup"><span data-stu-id="bf326-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="bf326-107">I ruden til venstre skal du vælge den aktivtype, som en leverandørgarantiaftale skal knyttes til, og derefter skal du vælge **Standarder for aktivtype**.</span><span class="sxs-lookup"><span data-stu-id="bf326-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="bf326-108">Vælg aftalen i feltet **Leverandørgaranti** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="bf326-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="bf326-109">Konfigurere en garanti for et aktiv</span><span class="sxs-lookup"><span data-stu-id="bf326-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="bf326-110">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bf326-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="bf326-111">Vælg aktivet, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bf326-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="bf326-112">I oversigtspanelet **Leverandør** i sektionen **Leverandørgaranti** skal du vælge garantiaftalen i feltet **Garanti**.</span><span class="sxs-lookup"><span data-stu-id="bf326-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="bf326-113">Vælg start- og slutdatoerne i felterne **Garantistart** og **Garantiafslutning**.</span><span class="sxs-lookup"><span data-stu-id="bf326-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="bf326-114">Hvis der er valgt en dato i feltet **Garantistart** på en arbejdsordre, bliver garantien gyldig for arbejdsordren på den pågældende dato.</span><span class="sxs-lookup"><span data-stu-id="bf326-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="bf326-115">Når du opretter en arbejdsordre, indstilles feltet **Garantistart** automatisk til oprettelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="bf326-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="bf326-116">Du kan dog ændre datoen, så den svarer til f.eks. startdatoen for en garantiaftale.</span><span class="sxs-lookup"><span data-stu-id="bf326-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Siden Arbejdsordre](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="bf326-118">Når du opretter en arbejdsordre for et aktiv, der er dækket af en leverandørgaranti, modtager du en besked om garantiaftalen, hvis arbejdsordren har en forventet startdato i løbet af garantiperioden.</span><span class="sxs-lookup"><span data-stu-id="bf326-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="bf326-119">Du kan derefter annullere arbejdsordren efter behov.</span><span class="sxs-lookup"><span data-stu-id="bf326-119">You can then cancel the work order, as you require.</span></span>
