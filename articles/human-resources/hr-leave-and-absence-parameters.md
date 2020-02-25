---
title: Konfigurere parametre for orlov og fravær
description: Definer personaleparametre for orlov og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008469"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="c8f7c-103">Konfigurere parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="c8f7c-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="c8f7c-104">Før du opretter orlovs- og fraværsplaner i Dynamics 365 Human Resources, er det en god ide at kontrollere indstillingerne for alle relaterede personaleparametre, herunder:</span><span class="sxs-lookup"><span data-stu-id="c8f7c-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="c8f7c-105">Nummerserie for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="c8f7c-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="c8f7c-106">FMLA-indstillinger (Family Medical and Leave Act)</span><span class="sxs-lookup"><span data-stu-id="c8f7c-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="c8f7c-107">Indstillinger for medarbejderselvbetjening for anmodninger om orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="c8f7c-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="c8f7c-108">Parametre for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="c8f7c-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="c8f7c-109">Få vist og skift personaleparametre</span><span class="sxs-lookup"><span data-stu-id="c8f7c-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="c8f7c-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c8f7c-111">Vælg **Personaleparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c8f7c-112">Under fanen **Nummerserier** skal du kontrollere **Nummerseriekode** for **Orlovsanmodnings-id** og ændre den efter behov.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="c8f7c-113">Denne indstilling bestemmer den rækkefølge, der bruges til automatisk tildeling af id'er til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="c8f7c-114">Under fanen **FMLA** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="c8f7c-115">Under fanen **Medarbejderselvbetjening** skal du angive, om ledere kan angive orlovs- og fraværsanmodninger på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="c8f7c-116">Under fanen **Orlov og fravær** skal du kontrollere FMLA-indstillingerne og ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="c8f7c-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="c8f7c-118">Konfigurere kalenderparametre</span><span class="sxs-lookup"><span data-stu-id="c8f7c-118">Configure calendar parameters</span></span>

<span data-ttu-id="c8f7c-119">Hvis du har aktiveret funktionen til forhåndsvisning af orlovs- og fraværskalender, skal du konfigurere yderligere parametre.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="c8f7c-120">I forbindelse med eksempelversionen den 3. februar 2020 er det kun **ventende anmodninger om orlov**, der er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="c8f7c-121">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c8f7c-122">Vælg **Personaleparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c8f7c-123">Under fanen **Kalender** skal du ændre kalenderindstillingerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="c8f7c-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c8f7c-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8f7c-125">Se også</span><span class="sxs-lookup"><span data-stu-id="c8f7c-125">See also</span></span>

- [<span data-ttu-id="c8f7c-126">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="c8f7c-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
