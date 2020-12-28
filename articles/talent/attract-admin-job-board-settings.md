---
title: Aktiver Broadbean-integration i Attract
description: Dette emne forklarer, hvordan du konfigurerer Microsoft Dynamics 365 Talent - Attract til at slå job op på eksterne jobportaler som Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460746"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="e89bc-103">Aktiver Broadbean-integration i Attract</span><span class="sxs-lookup"><span data-stu-id="e89bc-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e89bc-104">Du vil gerne have, at dine ledige stillinger ses af så mange kvalificerede kandidater som muligt.</span><span class="sxs-lookup"><span data-stu-id="e89bc-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="e89bc-105">Rekrutteringswebsteder såsom Broadbean kan hjælpe dig med at nå dette mål.</span><span class="sxs-lookup"><span data-stu-id="e89bc-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="e89bc-106">Microsoft Dynamics 365 Talent: Attract giver dig nu mulighed for at slå job op på Broadbean, og Microsoft stiller løbende nye tilbud til rådighed på dette område.</span><span class="sxs-lookup"><span data-stu-id="e89bc-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="e89bc-107">For at slå jobs op på eksterne websteder skal du have [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="e89bc-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="e89bc-108">Hvis du vil opslå job til Broadbean via Attract, skal du have et Broadbean-abonnement.</span><span class="sxs-lookup"><span data-stu-id="e89bc-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="e89bc-109">Denne funktion findes på nuværende tidspunkt i prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="e89bc-109">This feature is currently in preview.</span></span> <span data-ttu-id="e89bc-110">Hvis du ønsker at prøve det, skal du [slå det til i administratorindstillingerne i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="e89bc-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="e89bc-111">Konfigurer integrationen af Broadbean</span><span class="sxs-lookup"><span data-stu-id="e89bc-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="e89bc-112">Log på Attract som administrator.</span><span class="sxs-lookup"><span data-stu-id="e89bc-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="e89bc-113">Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Administration**.</span><span class="sxs-lookup"><span data-stu-id="e89bc-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="e89bc-114">Kontakt Broadbean, og indtast dine oplysninger i felterne **Brugernavn**, **Klient-id** og **Krypteringstoken**.</span><span class="sxs-lookup"><span data-stu-id="e89bc-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="e89bc-115">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e89bc-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="e89bc-116">Dine legitimationsoplysninger til Broadbean er følsomme og fortrolige.</span><span class="sxs-lookup"><span data-stu-id="e89bc-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="e89bc-117">Opbevar og del dem derfor ansvarligt.</span><span class="sxs-lookup"><span data-stu-id="e89bc-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="e89bc-118">Alle med en administratorrolle i Attract kan se disse legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e89bc-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="e89bc-119">Microsoft og Attract er ikke involveret i dannelsen og vedligeholdelsen af disse værdier.</span><span class="sxs-lookup"><span data-stu-id="e89bc-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="e89bc-120">Det er dit ansvar at ajourføre dem i Attract og arbejde sammen med Broadbean om at løse alle problemer vedrørende dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e89bc-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
