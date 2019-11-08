---
title: Annullere lagerstedsarbejde for undtagelseshåndtering
description: I dette emne beskrives den funktion til annullering af arbejdet, der giver lagerstedets tilsynsførende mulighed for at håndtere blokeret arbejde.
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625853"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="11d69-103">Annullere lagerstedsarbejde for undtagelseshåndtering</span><span class="sxs-lookup"><span data-stu-id="11d69-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11d69-104">Med funktionen Annuller arbejde i Microsoft Dynamics 365 Supply Chain Management kan administratorbrugeren annullere specifikt lagerstedsarbejde, der er i gang, men som blokeres af systemet eller ikke kan fuldføres på grund af usædvanlige omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="11d69-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="11d69-105">Denne funktionalitet er et attraktivt og sikkert alternativ til SQL-korrigerende scripts, der reparerer uoverensstemmende data.</span><span class="sxs-lookup"><span data-stu-id="11d69-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="11d69-106">Mens disse scripts typisk benyttes af IT-fagfolk, kan funktionen Annuller arbejde bruges af brugere i firmaet, der har administratorrettigheder.</span><span class="sxs-lookup"><span data-stu-id="11d69-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="11d69-107">Du kan få adgang til funktionen Annuller arbejde via **Lokationsstyring** \> **Periodiske opgaver** \> **Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="11d69-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="11d69-108">Angiv arbejds-id'et for det arbejde, du vil annullere, i dialogboksen **Annuller arbejde**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="11d69-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="11d69-109">Lagerstedsarbejde, der kan annulleres</span><span class="sxs-lookup"><span data-stu-id="11d69-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="11d69-110">Under pluk af lagersted kan arbejdere støde på situationer, hvor de har registreret antal som plukket fra en lagerlokation til deres brugerlokation, men de kan ikke registrere Læg på lager-handlingen.</span><span class="sxs-lookup"><span data-stu-id="11d69-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="11d69-111">Inkonsekvente lagerdata er ofte, men ikke altid, årsagen til, at arbejdet er blokeret.</span><span class="sxs-lookup"><span data-stu-id="11d69-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="11d69-112">I modsætning til den almindelige annullerings funktion, der kan åbnes med knappen **Annuller** i arbejdshovedet, kræver funktionen Annuller arbejde ikke, at den sidste fuldførte arbejdslinje er en linje af typen **Læg på lager**.</span><span class="sxs-lookup"><span data-stu-id="11d69-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="11d69-113">Med andre ord kan funktionen Annuller arbejde køres med annulleringslogik, selvom vareantallet på en arbejdslinje befinder sig på en brugerlokation.</span><span class="sxs-lookup"><span data-stu-id="11d69-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="11d69-114">For arbejde, der skal annulleres af driftsårsager, skal lagerstedsbrugerne fortsætte med at bruge den almindelige annulleringsfunktion på arbejdssiden.</span><span class="sxs-lookup"><span data-stu-id="11d69-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="11d69-115">Det er kun arbejde af typen **Salg**, **Flytteafgang**, **Råvarepluk** eller **Genopfyldning**, der kan annulleres ved hjælp af funktionen Annuller arbejde.</span><span class="sxs-lookup"><span data-stu-id="11d69-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="11d69-116">Annulleringslogik køres ikke for frosset råvareplukarbejde eller arbejde, der kan annulleres ved hjælp af den almindelige annulleringsfunktion (se den foregående bemærkning).</span><span class="sxs-lookup"><span data-stu-id="11d69-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="11d69-117">For at fjerne blokeringen af arbejdet annullerer systemet eventuelle resterende arbejdslinjer og reparerer de lagerstedsdata, der er tilknyttet det arbejds-id, som brugeren har angivet.</span><span class="sxs-lookup"><span data-stu-id="11d69-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="11d69-118">De almindelige lagerhåndteringsoperationer, der omfatter det berørte vareantal, kan derefter genoptages.</span><span class="sxs-lookup"><span data-stu-id="11d69-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="11d69-119">Hvis du vil lægge den berørte vare på en bestemt lokation, efter at arbejdet er annulleret, skal brugeren bruge en lagerbevægelse eller antalsregulering på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="11d69-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
