---
title: Callcenter-salgsfunktioner
description: Dette emne giver et overblik over funktionerne til callcentersalg i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 816bfc8b93f52fe91192874bcc1c8e605e41b582
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021967"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="f6ec9-103">Funktionalitet til callcenter-salg</span><span class="sxs-lookup"><span data-stu-id="f6ec9-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f6ec9-104">I Dynamics 365 Commerce er et callcenter en type kanal, som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="f6ec9-105">Når du definerer en bestemt kanal for dine callcenterenheder, kan systemet binde bestemte datastandarder og ordrebehandlingsstandarder til salgsordrer, der er oprettet af en bruger af callcenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="f6ec9-106">Callcenterfunktioner omfatter avancerede priser og kampagner, kataloger, gavekort, loyalitetsprogrammer og kuponer.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="f6ec9-107">Callcenterordrer bruges også af POS-programmet til at understøtte ordreopfyldningsscenarier på tværs af kanaler.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="f6ec9-108">Det er vigtigt at bemærke, at mens callcentermodulet kan anvendes af andre brancher end Commerce, er den aktuelle version af callcenterprogrammet ikke optimeret til brug i B2B-ordrebehandlingsscenarier eller scenarier, hvor ordrer har en stor mængde salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="f6ec9-109">Det anbefales, at brugere, som vil udnytte callcenterfunktionerne til anden ordrebehandling end behandling af almindelige transaktioner direkte til forbrugeren, tager sig tid til at teste og validere, at aktivering af callcenterfunktionaliteten opfylder deres krav til funktion og ydeevne.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="f6ec9-110">Ud over at understøtte ordreoprettelsen indeholder callcentermodulet også et brugervenligt kundeserviceprogram, der gør det lettere for brugerne at finde debitorkonti og gennemse alle de relaterede kundeordredata og -attributter.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="f6ec9-111">Kundeserviceskærmbilledet er udviklet til at give brugerne hurtig adgang til ordrerelaterede data, som gør det muligt for dem at besvare de mest almindelige ordrerelaterede spørgsmål, der modtages fra debitorer.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="f6ec9-112">Denne side indeholder links til relevant dokumentation, der er relateret til installation, konfiguration og den funktionelle brug af funktionerne i callcenteret.</span><span class="sxs-lookup"><span data-stu-id="f6ec9-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="f6ec9-113">Konfigurere callcenteret</span><span class="sxs-lookup"><span data-stu-id="f6ec9-113">Configure the call center</span></span>

[<span data-ttu-id="f6ec9-114">Konfigurere callcenter-kanaler</span><span class="sxs-lookup"><span data-stu-id="f6ec9-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="f6ec9-115">Konfigurere ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="f6ec9-115">Configure order processing</span></span>

[<span data-ttu-id="f6ec9-116">Konfigurere og arbejde med advarsler om svindel i callcentre</span><span class="sxs-lookup"><span data-stu-id="f6ec9-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="f6ec9-117">Konfigurere og arbejde med callcenter-ordrer på hold</span><span class="sxs-lookup"><span data-stu-id="f6ec9-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="f6ec9-118">Konfigurere betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="f6ec9-118">Configure payment processing</span></span>

[<span data-ttu-id="f6ec9-119">Betalingsmetoder i callcentre</span><span class="sxs-lookup"><span data-stu-id="f6ec9-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="f6ec9-120">Konfigurere leveringsmetoder</span><span class="sxs-lookup"><span data-stu-id="f6ec9-120">Configure delivery modes</span></span>

[<span data-ttu-id="f6ec9-121">Konfigurere callcenterets leveringsmåder og -gebyrer</span><span class="sxs-lookup"><span data-stu-id="f6ec9-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="f6ec9-122">Konfigurere direkte marketing</span><span class="sxs-lookup"><span data-stu-id="f6ec9-122">Configure direct marketing</span></span>

[<span data-ttu-id="f6ec9-123">Callcenter-kataloger</span><span class="sxs-lookup"><span data-stu-id="f6ec9-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="f6ec9-124">Konfigurere RFM-analyse (Recency, Frekvens og Monetær)</span><span class="sxs-lookup"><span data-stu-id="f6ec9-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="f6ec9-125">Konfigurere kontinuitetsprogrammer</span><span class="sxs-lookup"><span data-stu-id="f6ec9-125">Configure continuity programs</span></span>

[<span data-ttu-id="f6ec9-126">Oprette kontinuitetsprogrammer for callcentre</span><span class="sxs-lookup"><span data-stu-id="f6ec9-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
