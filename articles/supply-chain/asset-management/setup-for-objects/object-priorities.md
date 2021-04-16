---
title: Aktivers tjenesteniveauer
description: I dette emne beskrives aktivtjenesteniveauer i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4163d059fda4ae0120d5c989e744c5a5fe0f5892
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808279"
---
# <a name="asset-service-levels"></a><span data-ttu-id="b6a2e-103">Aktivers tjenesteniveauer</span><span class="sxs-lookup"><span data-stu-id="b6a2e-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b6a2e-104">I dette emne beskrives aktivtjenesteniveauer i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="b6a2e-105">Aktivers tjenesteniveauer er relateret til aktiver og overføres til vedligeholdelsesanmodninger og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="b6a2e-106">De bruges til at beregne prioriteringen af arbejdsordrer i forbindelse med arbejdsordreplanlægning.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="b6a2e-107">Aktivers tjenesteniveauer kan ændres, hvis der er behov for ændringer.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="b6a2e-108">Du finder flere oplysninger om den opsætning, der er relateret til beregningen af rangeringsresultater for planlægning af arbejdsordre under [Parametre for Styring af aktiver](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b6a2e-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="b6a2e-109">Du skal oprette mindst én standardpost for tjenesteniveauet for aktivet.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="b6a2e-110">Denne standardpost bruges, hvis der ikke findes andre match under planlægning af arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="b6a2e-111">**Eksempel 1:** det tjenesteniveau, der som standard bruges, hvis der ikke findes andre match.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="b6a2e-112">I denne post skal du kun vælge et tjenesteniveau.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="b6a2e-113">**Eksempel 2:** et højt tjenesteniveau, der bruges til at planlægge job til en Volvo-lastbilmotor.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="b6a2e-114">I denne post vælger du en relevant aktivtype (f.eks **Lastbilmotor**), en producent (**Volvo**) og et tjenesteniveau.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="b6a2e-115">Konfigurer aktivers tjenesteniveauer</span><span class="sxs-lookup"><span data-stu-id="b6a2e-115">Set up asset service levels</span></span>

1. <span data-ttu-id="b6a2e-116">Vælg **Styring af aktiver** \> **Opsætning** \> **Tjenesteniveau for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="b6a2e-117">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="b6a2e-118">Afhængigt af det detaljeringsniveau, der kræves for aktiv tjenesteniveauet, skal du foretage relevante valg i felterne **Arbejdssted**, **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Arbejdsordretype** og **Tjenesteniveau**.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a2e-119">Når tjenesteniveauet for et aktiv bruges til vedligeholdelsesanmodninger og arbejdsordrer, gennemgår Styring af aktiver alle poster på et aktivs tjenesteniveau for at kontrollere, om der er et muligt match.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="b6a2e-120">Den kontrollerer altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="b6a2e-121">Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="b6a2e-122">Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Aktiv** osv.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="b6a2e-123">Som du kan se i layoutet for siden **Tjenesteniveauer for aktiver**, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="b6a2e-124">Hvis der ikke findes et match, bruges standardposten, som ikke har nogen markeringer i de pågældende felter.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="b6a2e-125">I feltet **Tjenesteniveau** skal du vælge et nummer, der angiver tjenesteniveauet (prioritet).</span><span class="sxs-lookup"><span data-stu-id="b6a2e-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="b6a2e-126">Hvis du ændrer en registrering af tjenesteniveauet for aktivet på siden **Tjenesteniveauer for aktiv**, efter at du allerede har brugt den på en arbejdsordre, opdateres tjenesteniveauet på vedligeholdelsesanmodninger og arbejdsordrer ikke i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="b6a2e-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]