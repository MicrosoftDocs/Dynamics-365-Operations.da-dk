---
title: Ofte stillede spørgsmål til et bilag
description: Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i funktionen Ét bilag. Ét bilag til økonomikladder (finanskladde, anlægsaktivkladde, kreditorbetalingskladde osv.) giver dig mulighed for at angive flere reskontrotransaktioner i forbindelse med et enkelt bilag.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: a0cbc9e1f70bd41157e2ed70f78c8129671a6a04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234159"
---
# <a name="one-voucher-faq"></a><span data-ttu-id="36202-104">Ofte stillede spørgsmål til et bilag</span><span class="sxs-lookup"><span data-stu-id="36202-104">One voucher FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36202-105">Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i funktionen Ét bilag.</span><span class="sxs-lookup"><span data-stu-id="36202-105">This topic answers frequently asked questions about the One voucher functionality.</span></span> <span data-ttu-id="36202-106">Et bilag til finanskladder giver dig mulighed for at angive flere transaktioner for reskontro inden for rammerne af et enkelt bilag.</span><span class="sxs-lookup"><span data-stu-id="36202-106">One voucher for financial journals lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="36202-107">De kladder, der kan medtages i bilaget, kan bl.a. være finanskladder, anlægsaktivkladder og kreditorbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="36202-107">The journals that you can include in that voucher can be general journals, fixed asset journals, and vendor payment journals, among others.</span></span>

## <a name="when-will-the-one-voucher-functionality-be-deprecated"></a><span data-ttu-id="36202-108">Hvornår frarådes funktionen Ét bilag?</span><span class="sxs-lookup"><span data-stu-id="36202-108">When will the One voucher functionality be deprecated?</span></span>

<span data-ttu-id="36202-109">Selvom Microsoft ikke kan give et præcist estimat over, hvornår funktionen Ét bilag frarådes, vil der højst sandsynligt gå to år, før afskrivningen finder sted.</span><span class="sxs-lookup"><span data-stu-id="36202-109">Although Microsoft can't provide an accurate estimate about when the One voucher functionality will be deprecated, it will likely be at least two years before the deprecation occurs.</span></span>

<span data-ttu-id="36202-110">Som det fremgår af dokumentationen til Ét bilag, kan flere forretningsbehov kun opfyldes ved hjælp af ét bilag.</span><span class="sxs-lookup"><span data-stu-id="36202-110">As is noted in the One voucher documentation, numerous business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="36202-111">Microsoft skal sikre, at alle de identificerede forretningskrav stadig kan opfyldes i systemet, når funktionaliteten frarådes.</span><span class="sxs-lookup"><span data-stu-id="36202-111">Microsoft must ensure that all the identified business requirements can still be met in the system after the functionality is deprecated.</span></span> <span data-ttu-id="36202-112">Derfor vil der sandsynligvis skulle tilføjes nye funktioner for at udfylde funktionelle kløfter.</span><span class="sxs-lookup"><span data-stu-id="36202-112">Therefore, new features will probably have to be added to fill functional gaps.</span></span>

<span data-ttu-id="36202-113">Når alle funktionelle huller er udfyldt, kommunikerer Microsoft, at det frarådes at bruge funktionen.</span><span class="sxs-lookup"><span data-stu-id="36202-113">After all functional gaps are filled, Microsoft will communicate that the feature will be deprecated.</span></span> <span data-ttu-id="36202-114">Afskrivningen vil dog ikke være gældende i mindst ét år efter den pågældende kommunikation.</span><span class="sxs-lookup"><span data-stu-id="36202-114">However, the deprecation won't be effective for least one year after that communication.</span></span>

<span data-ttu-id="36202-115">Yderligere oplysninger finder du i [Ét bilag-dokumentation](one-voucher.md).</span><span class="sxs-lookup"><span data-stu-id="36202-115">For more information, see the [One voucher documentation](one-voucher.md).</span></span>

## <a name="what-will-the-solution-that-replaces-one-voucher-look-like"></a><span data-ttu-id="36202-116">Hvordan vil den løsning, der erstatter ét bilag, se ud?</span><span class="sxs-lookup"><span data-stu-id="36202-116">What will the solution that replaces One voucher look like?</span></span>

<span data-ttu-id="36202-117">Microsoft kan ikke tilbyde en bestemt løsning, da de enkelte funktionskløfter er forskellige og skal evalueres ud fra forretningsbehovet.</span><span class="sxs-lookup"><span data-stu-id="36202-117">Microsoft can't provide a specific solution, because each feature gap is different and must be evaluated based on the business requirements.</span></span> <span data-ttu-id="36202-118">Nogle funktionelle kløfter vil sandsynligvis blive erstattet af funktioner, der er med til at opfylde bestemte forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="36202-118">Some functional gaps will likely be replaced with features that help meet specific business requirements.</span></span> <span data-ttu-id="36202-119">Andre huller kan dog udfyldes ved fortsat at gøre det muligt at angive oplysninger i en kladde, som ved anvendelse af ét bilag, men systemet kan efterhånden spore flere detaljer efter behov.</span><span class="sxs-lookup"><span data-stu-id="36202-119">However, other gaps might be filled by continuing to allow for entry in a journal, as when One voucher is used, but enhancing the system to track more detail as required.</span></span>

## <a name="where-can-i-track-the-progress-of-the-feature-gaps-being-filled"></a><span data-ttu-id="36202-120">Hvor kan jeg spore status for de funktionskløfter, der udfyldes?</span><span class="sxs-lookup"><span data-stu-id="36202-120">Where can I track the progress of the feature gaps being filled?</span></span>

<span data-ttu-id="36202-121">Hvad der er med hver ny funktion, skal kunder ændre dokumentationen for frigivelsesplanen og dokumentationen for nyheder eller ændringer.</span><span class="sxs-lookup"><span data-stu-id="36202-121">As for every new feature, customers must watch the Release plan and "What's new or changed" documentation.</span></span> <span data-ttu-id="36202-122">Hver funktion vil blive føjet til disse dokumenter, og et notat angiver, at funktionen er påkrævet for at opfylde et forretningskrav, der tidligere krævede funktionen Ét bilag.</span><span class="sxs-lookup"><span data-stu-id="36202-122">Each feature will be added to these documents, and a note will indicate that the feature is required to meet a business requirement that previously required the One voucher functionality.</span></span>

## <a name="when-the-deprecation-date-is-identified-where-will-it-be-communicated"></a><span data-ttu-id="36202-123">Når datoen for afskrivningen identificeres, hvor kommunikeres den så?</span><span class="sxs-lookup"><span data-stu-id="36202-123">When the deprecation date is identified, where will it be communicated?</span></span>

<span data-ttu-id="36202-124">Når ét bilag afskrives, er det en vigtig ændring, der kommunikeres i vidt omfang.</span><span class="sxs-lookup"><span data-stu-id="36202-124">The deprecation of One voucher is a significant change that will be widely communicated.</span></span> <span data-ttu-id="36202-125">Den kommunikeres via produktdokumentationen, et blogpost og meddelelser, der er relevante for Microsoft, langt forud for den dato, hvor afskrivningen træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="36202-125">It will be communicated through the product documentation, a blog post, and announcements at applicable Microsoft conferences, well in advance of the date when the deprecation takes effect.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]