---
title: Konfigurere leasingparametre (prøveversion)
description: Dette emne beskriver konfigurationsindstillingerne for aktivleasing, f. eks. sikkerhedsoplysninger og regnskabsindstillinger.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff0aa5fd0b78814dfa5bb00d6d5ef2984c566d14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971397"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="ffc3e-103">Konfigurere leasingparametre</span><span class="sxs-lookup"><span data-stu-id="ffc3e-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffc3e-104">Flere konfigurationsindstillinger har indflydelse på, hvordan aktivleasing fungerer.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="ffc3e-105">Disse indstillinger omfatter kladdenavne, generelle parametre og indstillinger for posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="ffc3e-106">Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="ffc3e-107">Under fanen **Leasingaftaler** skal du vælge oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="ffc3e-108">Parameteren **Tillad manuel klassificeringstilsidesættelse** bestemmer, om leasingklassifikationen kan tilsidesættes, før betalingsplanen bekræftes.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="ffc3e-109">Parameteren **Batch på tværs af enheder** bestemmer, om du kan bogføre i andre juridiske enheder fra den aktuelle juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="ffc3e-110">Hvis denne parameter er slået til, kan du oprette kladdeposteringer for de juridiske enheder, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="ffc3e-111">Angiv indstillingen til **Tillad sletning af bekræftede leasingaftaler** til **Ja** for at tillade, at leasingaftaler, der har bekræftede betalingsplaner, skal slettes.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="ffc3e-112">Leasingaftaler kan ikke slettes, hvis der er knyttet bogførte eller ikke-bogførte posteringer til dem, uanset indstillingen af denne funktion.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="ffc3e-113">Du kan ikke gendanne en leasingaftales post, efter at den er slettet.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="ffc3e-114">Hvis du overfører poster til en slettet leasingaftale, enten manuelt eller gennem dataenheder, behandles de overførte oplysninger som nye, ikke som en opdatering til en eksisterende leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="ffc3e-115">Hvis du angiver denne indstilling til **Ja**, og kartotekets overførselstype er **Kumulativ catch-up-indstilling A eller B**, indstiller systemet feltet for **Trinvis lånerate** til værdien af feltet **Trinvis lånerate ved overgang** på siden **Opsætning af kartotek**.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="ffc3e-116">Hvis denne indstilling er angivet til **Nej**, angives satsen for hovedleasingaftalen til værdien i feltet **Trinvis lånesats** på siden **Kartotekoplysninger**, uanset hvilken overførselstype kartoteket er.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="ffc3e-117">Marker feltet **Tillad, at tilbageførsler for den lukkede version af kartoteket angives** til **Ja**, hvis du vil tillade, at afskrivningsudgiftsposteringerne tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="ffc3e-118">Udgiftsposteringer kan tilbageføres, også selvom kartotekets version er lukket.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ffc3e-119">Det anbefales, at du beholder denne indstilling angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="ffc3e-120">Indstillingen af denne funktion bruges som en validering og kontrol for at forhindre, at et lukket kartotek afskrives ved en fejltagelse.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="ffc3e-121">Hvis du holder indstillingen angivet til **Nej**, kan du hjælpe med at bevare den bogførte nettoværdi og fremtidige afskrivningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="ffc3e-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
