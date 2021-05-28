---
title: Tilbageføre indstillinger på kladder og linjer
description: Dette emne omhandler, hvorfor en tilbageførselspost, der er angivet i en finanskladde, muligvis ikke inkluderes i den bogførte transaktion.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028554"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="b327b-103">Tilbageføre indstillinger på kladder og linjer</span><span class="sxs-lookup"><span data-stu-id="b327b-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b327b-104">Dette emne omhandler, hvorfor en tilbageførselspost, der er angivet i en finanskladde, muligvis ikke inkluderes i den bogførte transaktion.</span><span class="sxs-lookup"><span data-stu-id="b327b-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="b327b-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="b327b-105">Symptom</span></span>

<span data-ttu-id="b327b-106">En finanskladde omfatter en tilbageførselspost og tilbageførselsdato i kladden.</span><span class="sxs-lookup"><span data-stu-id="b327b-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="b327b-107">Når du bogfører kladden, tilbageføres ingen af bilagene.</span><span class="sxs-lookup"><span data-stu-id="b327b-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="b327b-108">Hvorfor sker det?</span><span class="sxs-lookup"><span data-stu-id="b327b-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="b327b-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="b327b-109">Resolution</span></span>

<span data-ttu-id="b327b-110">Når kladden bogføres, behandles tilbageførslen kun med indstillingerne for **Tilbageførselspost** og **Tilbageførselsdato** i sektionen **Linjer** på bilaget.</span><span class="sxs-lookup"><span data-stu-id="b327b-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="b327b-111">Denne metode giver en kladde mulighed for at medtage visse bilag, der er markeret til tilbageførsel, mens andre ikke er.</span><span class="sxs-lookup"><span data-stu-id="b327b-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="b327b-112">Værdierne fra kladden bruges kun som standard, når der tilføjes *nye* linjer.</span><span class="sxs-lookup"><span data-stu-id="b327b-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="b327b-113">Ændring af værdierne i kladden påvirker ikke eksisterende linjer.</span><span class="sxs-lookup"><span data-stu-id="b327b-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="b327b-114">I dette eksempel er bilagslinjerne blevet angivet først.</span><span class="sxs-lookup"><span data-stu-id="b327b-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="b327b-115">Når du angiver linjedetaljerne, inden du angiver kladden som tilbageførsel, anvendes angivelsen som en tilbageførsel og dato ikke på eksisterende linjer.</span><span class="sxs-lookup"><span data-stu-id="b327b-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="b327b-116">Ændring af tilbageførselsposten eller tilbageførselsdatoen på en eksisterende linjekvittering, der ændres til andre linjer i samme bilag.</span><span class="sxs-lookup"><span data-stu-id="b327b-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="b327b-117">Hvis ydeevnen skal optimeres, opdateres gitteret ikke, når der er foretaget ændringer af linjen til andre linjer.</span><span class="sxs-lookup"><span data-stu-id="b327b-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="b327b-118">Du kan få vist de opdaterede værdier ved at opdatere gitteret.</span><span class="sxs-lookup"><span data-stu-id="b327b-118">You can display the updated values by refreshing the grid.</span></span>


