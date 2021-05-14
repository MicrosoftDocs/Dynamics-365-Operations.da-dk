---
title: Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen
description: Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938443"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="c5a72-103">Du kan ikke bekræfte en forsendelse på grund af problemer med kalenderen</span><span class="sxs-lookup"><span data-stu-id="c5a72-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="c5a72-104">Fejlkode: TRX2716</span><span class="sxs-lookup"><span data-stu-id="c5a72-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="c5a72-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c5a72-105">Symptoms</span></span>

<span data-ttu-id="c5a72-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="c5a72-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="c5a72-107">Kalendertypen %1 kræver, at aftalen %2 tjekkes ind og ud.</span><span class="sxs-lookup"><span data-stu-id="c5a72-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="c5a72-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="c5a72-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c5a72-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="c5a72-109">Cause</span></span>

<span data-ttu-id="c5a72-110">Der findes aktive aftaler i indlæsningen.</span><span class="sxs-lookup"><span data-stu-id="c5a72-110">Active appointments for the load exist.</span></span> <span data-ttu-id="c5a72-111">Der findes f.eks. en regel, der kræver, at chaufføren tjekker ind.</span><span class="sxs-lookup"><span data-stu-id="c5a72-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="c5a72-112">Belastningen befinder sig derfor i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="c5a72-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5a72-113">Løsning</span><span class="sxs-lookup"><span data-stu-id="c5a72-113">Resolution</span></span>

<span data-ttu-id="c5a72-114">Du skal undersøge sagen og løse eventuelle problemer med de aktive aftaler, der er tilknyttet belastningen.</span><span class="sxs-lookup"><span data-stu-id="c5a72-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="c5a72-115">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="c5a72-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5a72-116">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="c5a72-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c5a72-117">I handlingsruden under fanen **Transport** i gruppen **Aftaler** skal du vælge **Planlægning af aftale**.</span><span class="sxs-lookup"><span data-stu-id="c5a72-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="c5a72-118">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="c5a72-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="c5a72-119">Kontrollér, at chaufførens indtjekning/udtjekning er fuldført for aftalen.</span><span class="sxs-lookup"><span data-stu-id="c5a72-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="c5a72-120">Fuldfør eller annuller aftalen.</span><span class="sxs-lookup"><span data-stu-id="c5a72-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="c5a72-121">Deaktiver indstillingen **Chaufførs indtjekning er er påkrævet** for den relaterede aftaleregel.</span><span class="sxs-lookup"><span data-stu-id="c5a72-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
